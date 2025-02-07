---
title: HTML5 - creatieve specificatie
description: Verwijs naar de creatieve HTML5 specificatie voor Advertising Creative.
feature: Creative Standard Creatives
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 0%

---

# HTML5 creatieve specificatie voor Advertising Creative

In dit document worden de vereisten en API-ondersteuning voor HTML5-creatieven in [!DNL Creative] beschreven. De API maakt de ontwikkeling mogelijk van HTML5-creatieven waarvan de kenmerken kunnen worden geconfigureerd op het moment van creatieve levering.

## Toepassingsgebied

[!DNL Creative] ondersteunt HTML5-banners met niet-rijke mediacreatieven die binnen ingestelde randen op een pagina worden weergegeven. U kunt de volgende typen HTML5-creatieven gebruiken:

<!--Remove to simplify:

* **Simple HTML5:** Supports a single landing page URL that can be configured during creative creation and trafficking.

* **Static HTML5:** Supports up to 5 landing page URLs that can be configured during creative creation and trafficking.

-->

* **HTML5:** steunt tot 5 het landen pagina URLs die tijdens creatieve verwezenlijking en handel kunnen worden gevormd.

* **Flexibele HTML5:** steunt tot 5 het landen pagina URLs die tijdens creatieve verwezenlijking en handel kunnen worden gevormd, en staat ook creatieve attributen toe om tijdens creatieve verwezenlijking en handel worden gewijzigd.

## Vereisten

### Map- en compressievereisten

* Creative Cloud moet zijn verpakt in een ZIP-bestand (.ZIP-indeling). Geneste ZIP-bestanden worden niet ondersteund, dus neem geen gecomprimeerde map op in de buitenste gecomprimeerde map.

* Het ZIP-bestand moet ten minste één HTML-bestand bevatten, het hoofdweergavebestand voor HTML, dat een verwijzing naar de JavaScript-bibliotheek van [!DNL Creative] bevat. Het hoofdbestand voor HTML kan zich in de hoofdmap of in een submap bevinden.

* Het HTML-hoofdbestand kan een willekeurige naam hebben, zolang het geen speciale tekens bevat, hoewel `index.html` wordt aangeraden.

* Alle ondersteunende elementen die nodig zijn om de uiteindelijke creatieve inhoud te renderen, moeten zich in dezelfde map bevinden als het HTML-weergavebestand of in submappen van de hoofdmap.

* Plaats geen bestanden in de creatieve lijst waarnaar niet wordt verwezen voor die creatieve inhoud.

### Opname van het Advertising Creative JavaScript-bestand

Het HTML-hoofdbestand (en geen andere bestanden) moet een verwijzing naar het JavaScript-bestand `AMOLibrary.js` bevatten. Roep het bestand in de eerste regel van de sectie `<head>` aan met het volgende adres:

`https://ads.everesttech.net/ads/static/local/AMOLibrary.js`

Dit bestand bevat functies om ervoor te zorgen dat gebeurtenissen bij afsluiten lokaal wordt getest zonder problemen.

<!-- Remove to simplify:

### Simple HTML5 creative requirements

#### Support for click-through URLS in simple HTML5

The `<head>` section of the main HTML file must include a JavaScript variable name `clickTag` or `clickTAG`. The value of the variable should be the landing page URL. See the following example.

```
<script type=”text/javascript”>
var clickTag = “http://www.example.com”;
</script>
```

>[!NOTE]
>
>The static URL you include in the HTML5 creative is used for local testing purposes only and will be overwritten. When you upload an HTML5 creative, you'll define the default landing page for the `clickTag` variable. When you assign an uploaded HTML5 creative to an ad experience, you can optionally override the default landing page for the `clickTag` variable, and [!DNL Creative] adds click tracking to the URL when you save the experience.

-->

<!-- Renamed to simplify:
### Static HTML5 creative requirements
-->

### HTML5 creatieve vereisten

#### Ondersteuning voor doorklikURL&#39;s in statische HTML5

##### `amo.registerClick(clkVar, clkUrl)`

Registreert klikthrough URLs en de bijbehorende parameter die wordt gebruikt om elke URL (die als `clickTag` wordt bekend) van verwijzingen te voorzien. Op deze manier wordt de advertentieserver van [!DNL Creative] op de hoogte gebracht waar u klikken op bijhouden wilt toevoegen. U kunt deze API gebruiken om maximaal vijf geklikte markeringsvariabelen, elk met een overeenkomstige het landen pagina URL te registreren.

>[!NOTE]
>
>De statische URL&#39;s die u in de creatieve HTML5 opneemt, worden alleen gebruikt voor lokale testdoeleinden en worden overschreven. Wanneer u een creatieve HTML5 uploadt, zult u de standaardlandingspagina voor elke `clickTag` variabele bepalen. Wanneer u een geüploade HTML5 creatief toewijst aan een advertentie-ervaring, kunt u optioneel de standaardopeningspagina voor elke `clickTag` -variabele overschrijven en [!DNL Creative] voegt klik het volgen aan URLs toe wanneer u de ervaring opslaat.

###### Parameters

* `clkVar` — De naam van de klikvariabele (gewoonlijk &quot;clickTag&quot;), ingesloten door dubbele aanhalingstekens.

* `clkUrl` — De URL van de landingspagina voor deze klikvariabele, ingesloten door dubbele aanhalingstekens.

###### Gebruik

Roep `amo.registerClick()` aan in de `<head>` -sectie van het hoofd-HTML-bestand.

###### Voorbeeld

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

De gebeurtenis exit wordt geactiveerd, waardoor de gebruiker wordt omgeleid naar de bestemmingspagina die voor de `clickTag` is geconfigureerd. Tijdens het lokale testen geeft deze functie een waarschuwing aan ontwikkelaars of de URL die aan de functie wordt doorgegeven, is geregistreerd.

###### Parameters

* `clkTag` — De naam van de klikvariabele die u gebruikt om de bestemmingspagina-URL toe te wijzen met behulp van de `amo.registerClick()` functie, ingesloten door enkele aanhalingstekens.

* `event` — (Optioneel) Het JavaScript-gebeurtenisobject click. Hiermee worden de coördinaten van kliks vastgelegd, die verder kunnen worden gebruikt om creatieve prestaties te analyseren.

###### Gebruik

Roep `amo.onAdClick()` aan in de `<body>` -sectie van het hoofd-HTML-bestand.

###### Voorbeelden

`amo.onAdClick('clickTag')` OR `amo.onAdClick('clickTag',clickEvt)`

### Flexibele creatieve HTML5-vereisten

#### Ondersteuning voor doorklikURL&#39;s in flexibele HTML5

##### `amo.registerClick(clkVar, clkUrl)`

Registreert klikthrough URLs en de bijbehorende parameter die wordt gebruikt om elke URL (die als `clickTag` wordt bekend) van verwijzingen te voorzien. Op deze manier wordt de advertentieserver van [!DNL Creative] op de hoogte gebracht waar u klikken op bijhouden wilt toevoegen. U kunt deze API gebruiken om maximaal vijf geklikte markeringsvariabelen, elk met een overeenkomstige het landen pagina URL te registreren.

>[!NOTE]
>
>De statische URL&#39;s die u in de creatieve HTML5 opneemt, worden alleen gebruikt voor lokale testdoeleinden en worden overschreven. Wanneer u een creatieve HTML5 uploadt, zult u de standaardlandingspagina voor elke `clickTag` variabele bepalen. Wanneer u een geüploade HTML5 creatief toewijst aan een advertentie-ervaring, kunt u optioneel de standaardopeningspagina voor elke `clickTag` -variabele overschrijven en [!DNL Creative] voegt klik het volgen aan URLs toe wanneer u de ervaring opslaat.

###### Parameters

* `clkVar` — De naam van de klikvariabele (gewoonlijk &quot;clickTag&quot;), ingesloten door dubbele aanhalingstekens.

* `clkUrl` — De URL van de landingspagina voor deze klikvariabele, ingesloten door dubbele aanhalingstekens.

###### Gebruik

Roep `amo.registerClick()` aan in de `<head>` -sectie van het hoofd-HTML-bestand.

###### Voorbeeld

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

De gebeurtenis exit wordt geactiveerd, waardoor de gebruiker wordt omgeleid naar de bestemmingspagina die voor de `clickTag` is geconfigureerd. Tijdens het lokale testen geeft deze functie een waarschuwing aan ontwikkelaars of de URL die aan de functie wordt doorgegeven, is geregistreerd.

###### Parameters

* `clkTag` — De naam van de klikvariabele die u gebruikt om de bestemmingspagina-URL toe te wijzen met behulp van de `amo.registerClick()` functie, ingesloten door enkele aanhalingstekens.

* `event` — (Optioneel) Het JavaScript-gebeurtenisobject click. Hiermee worden de coördinaten van kliks vastgelegd, die verder kunnen worden gebruikt om creatieve prestaties te analyseren.

###### Gebruik

Roep `amo.onAdClick()` aan in de `<body>` -sectie van het hoofd-HTML-bestand.

###### Voorbeelden

`amo.onAdClick('clickTag')` OR `amo.onAdClick('clickTag',clickEvt)`

#### Ondersteuning voor creatieve kenmerken in flexibele HTML5

##### `amo.registerAttribute(key, type, value)`

Definieert kenmerken van de creatieve producten die kunnen worden gewijzigd op het moment dat ze worden gemaakt of gemaakt. U kunt maximaal 20 creatieve kenmerken definiëren die kunnen worden geconfigureerd op het moment dat u creatief gaat werken of ervaring hebt opgedaan.

>[!NOTE]
>
>De waarden die in deze methode worden gedefinieerd, worden alleen gebruikt voor lokale ontwikkeling en worden niet gebruikt in live en serving.

###### Parameters

* `key` — De alfanumerieke naam van het kenmerk. Het moet beginnen met een alfabetisch teken.

* `type` — Het type kenmerk (`TEXT` of `IMAGE`).

* `value` — De waarde van het kenmerk voor testen. Voor kenmerken van het type `IMAGE` moet de waarde het relatieve pad naar het afbeeldingsbestand zijn.

###### Gebruik

Roep `amo.registerAttribute()` aan om één creatief kenmerk, type en waarde te registreren tijdens het testen in de lokale modus. Alle afbeeldingsbestanden die als samplewaarden worden gebruikt, moeten samen met het geüploade pakket in het ZIP-bestand worden verpakt.

##### `amo.attributes`

Een JSON-object waarmee de namen en waarden van variabelen voor het creatieve kenmerk kunnen worden opgevraagd. De objectsleutels zijn de kenmerknamen en de waarden zijn de waarden van die kenmerken.

In de lokale testmodus zijn de sleutel-waardeparen de paren die zijn geregistreerd door de `amo.registerAttribute` API. Voor productie, moeten de creatieve attributenveranderlijke namen en de waarden op het tijdstip van creatieve schepping en handel worden gevormd.

### Vereisten voor Creatieve inhoud

De meeste uitwisselingen van displays die in Advertising DSP beschikbaar zijn, hebben de volgende creatieve vereisten:

* Alle afbeeldingen moeten een effen rand hebben.

* Advertenties uitbreiden is niet toegestaan.

* De openingspagina moet in een nieuw venster worden geopend.

* Het domein van de landingspagina en zijn subdomeinen kunnen niet meer dan 35 karakters zijn. **Nota:** de definitieve het landen pagina URLs wordt bepaald in het DSP en niet in de activa van HTML5 zelf.

* Alle disclaimers op het aanbod van een advertentie moeten in de advertentie zelf worden opgenomen, en niet alleen op de landingspagina.

<!-- * (Dynamic HTML5 creatives) Do not use `window.open` to handle clicks in your code. Always use `amo.onDynAdClick` to handle click-throughs. -->

## Inhoud als een JSON-object en -array voorvertonen

### Inhoud als een JSON-object voorvertonen

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
}
```

### Inhoud als een JSON-array voorvertonen

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
[{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
},

{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-mobile-720x520.png",
"product_url": "http://adobe.com/"
}

]
```

## Voorbeeld HTML5 creatief

### Voorbeeld van mapstructuur (na decompressie)

* index.html

* /assets (map)

   * bg.jpg (JPG, PNG-, SVG- of GIF-afbeelding)

### Voorbeeld van een HTML-bestand (index.html) voor eenvoudige HTML-creatieven

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

### Voorbeeld van HTML-bestand (index.html) voor statische HTML-creatieven

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  amo.registerClick("clickTag2","http://www.example2.com");
  amo.registerClick("clickTag3","http://www.example3.com");
  amo.registerClick("clickTag4","http://www.example4.com");
  amo.registerClick("clickTag5","http://www.example5.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

>[!MORELIKETHIS]
>
>* [ voeg standaardcreatieve creatieve bibliotheek ](/help/creative/creative-libraries/creative-add-standard.md) toe
