---
title: JavaScript-code voor  [!DNL Analytics for Advertising]
description: JavaScript-code voor  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 18bfb32d-2754-44b2-86c1-d102836cc08c
source-git-commit: 94a5b5591aef0aa5ae5d3459d547f52d939d559c
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# JavaScript-code voor [!DNL Analytics for Advertising]

*Advertisers met slechts Advertising DSP*

Voor Advertising DSP houdt de [!DNL Analytics for Advertising] -integratie de weergave en doorklikinteracties van sites bij. Doorklikbezoeken worden bijgehouden aan de hand van de standaard Adobe Analytics-code op uw webpagina&#39;s. De [!DNL Analytics] -code legt de parameters AMO ID en EF ID vast in de URL van de bestemmingspagina en volgt deze in hun respectievelijke gereserveerde [!DNL eVars] . U kunt doorkijkbezoeken volgen door een JavaScript-fragment in uw webpagina&#39;s te implementeren.

In de eerste paginaweergave van een bezoek aan de site controleert de Adobe Advertising JavaScript-code of de bezoeker een advertentie heeft gezien of erop heeft geklikt. Als de gebruiker eerder via een doorklik de site is binnengekomen of geen advertentie heeft gezien, wordt de bezoeker genegeerd. Als de bezoeker een advertentie heeft gezien en niet de plaats via een klik-door tijdens het [ klikt raadplegingsvenster ](/help/integrations/analytics/prerequisites.md#lookback-a4adc) binnen Adobe Advertising is geplaatst, dan gebruikt de code van Adobe Advertising JavaScript of a) de [ Dienst van identiteitskaart van Experience Cloud ](https://experienceleague.adobe.com/docs/id-service/using/home.html) om een supplementaire identiteitskaart (`SDID`) te produceren of b) de Adobe Experience Platform [!DNL Web SDK] `generateRandomID` methode om een `[!DNL StitchID]` te produceren. Een van beide id&#39;s wordt gebruikt om gegevens van Adobe Advertising aan te sluiten op de hit Adobe Analytics van de bezoeker. Adobe Analytics vraagt vervolgens Adobe Advertising om de AMO-id en EF-id die aan de advertentie zijn gekoppeld. De AMO-id en EF-id&#39;s worden vervolgens in hun respectievelijke [!DNL eVars] ingevuld. Deze waarden blijven gedurende een bepaalde periode bestaan (standaard 60 dagen).

[!DNL Analytics] verzendt de metriek van het plaatsverkeer (zoals paginameningen, bezoeken, en bestede tijd) en om het even welke [!DNL Analytics] douane of standaardgebeurtenissen naar Adobe Advertising per uur, gebruikend EF identiteitskaart als sleutel. Deze [!DNL Analytics] metriek loopt dan door het attributiesysteem van Adobe Advertising om de omzettingen aan de klik en de belichtingsgeschiedenis te verbinden.

>[!NOTE]
>
>De Adobe Advertising JavaScript tracking-logica vindt plaats aan de Adobe-zijde en heeft dus vrijwel geen invloed op de laadtijd van de pagina.
>
>De logica voor de [!DNL DCM] gegevensconnector naar [!DNL Analytics] (met [!DNL Google Campaign Manager 360] ) voor Advertising DSP daarentegen vindt plaats aan de clientzijde. Door stitching aan de clientzijde wordt de pagina langzamer geladen en neemt het risico op gegevensverlies toe. Dit gebeurt omdat de [!DNL Analytics] JavaScript [!DNL DoubleClick] moet pingelen en moet wachten totdat [!DNL DoubleClick] de laatste klik-/impressiegegevens doorgeeft aan [!DNL Analytics] . Wanneer uw [!DNL DSP] -team de [!DNL DCM] -gegevensconnector instelt, moet u opgeven hoe lang u de pagina wilt vertragen.

<!--
## Deploying the JavaScript code

All users must deploy the standard JavaScript code.

Users who want to convert first-party segments from their customer data platforms to [!DNL RampIDs] or [!DNL ID5] IDs [!!!!VERIFY that it's not needed for importing segments directly from LiveRamp] must also deploy ID partner-specific JavaScript code to match conversions to view-throughs.

### The standard code

The standard JavaScript library consists of two lines that allow [!DNL Analytics] and Adobe Advertising to communicate with each other. If the [!DNL Analytics for Advertising] integration was completed during the Adobe Advertising implementation, then you should have already received this code with instructions on how to deploy it.

#### Implementations that use the Experience Cloud Identity Service `visitorAPI.js` code

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementations that use the Experience Platform [!DNL Web SDK] `alloy.js`code

### Additional code to import first-party segments to [!DNL RampIDs] and [!DNL ID5] IDs

   * For [!DNL RampIDs], Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

    [MAYBE PUT THIS BELOW] Place the [!DNL LaunchPad] tag on every page of your website, preferably as the first script within the page head tags but as high within the page head tags as possible.

   * For [!DNL ID5] IDs: Contact your Adobe Account Team, who will give you instructions to register for the tag with ID5. Registration is free, but you must sign an agreement. Once you register, a member of ID5’s technical team will provide a unique tag for your organization to implement on your webpages.
-->

## JavaScript-code implementeren

De JavaScript-bibliotheek bestaat uit twee regels waarmee [!DNL Analytics] en Adobe Advertising met elkaar kunnen communiceren. Als de [!DNL Analytics for Advertising] -integratie tijdens de Adobe Advertising-implementatie is voltooid, hebt u deze code al ontvangen met instructies over de implementatie ervan.

### De code

#### Implementaties die de code Experience Cloud Identity Service `visitorAPI.js` gebruiken

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

#### Implementaties die de Experience Platform [!DNL Web SDK] `alloy.js` code gebruiken

```
<script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

### Plaats de code

De functie [!DNL Analytics for Advertising] JavaScript moet na de Experience Cloud ID Service komen, maar voordat de Metingscode van de Analytics App wordt uitgevoerd. Dit zorgt ervoor dat extra identiteitskaart (`SDID`) of `[!DNL StitchID]` inbegrepen in uw vraag van de Analyse is.

![ plaatsing van de Code ](/help/integrations/assets/a4adc-code-placement.png)

### Implementatie van code valideren

U kunt validatie uitvoeren met elk pakketsniffertype (zoals [!DNL Charles] , [!DNL Fiddler] of [!DNL Chrome Developer Tools] ) door de waarden van de vier id&#39;s te vergelijken tussen de aanvraag die naar Adobe Advertising gaat en de aanvraag die naar [!DNL Analytics] gaat, zoals hieronder wordt beschreven.

#### De code bevestigen met [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Open [!DNL Chrome Developer Tools] en klik het **Netwerk** lusje.

1. Laad een websitepagina die de [!DNL Analytics for Advertising] JavaScript bevat.

1. Filter de tab [!UICONTROL Network] op `last` en bekijk twee rijen:

   ![ Filtrerend op laatste ](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * De eerste rij is de aanroep naar de JavaScript-bibliotheek en krijgt de naam `last-event-tag-latest.min.js` .
   * De tweede rij is de vraag die het verzoek naar Adobe Advertising verzendt. Het begint als volgt: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

     Als u de oproep aan Adobe Advertising niet ziet, is het mogelijk niet de eerste paginaweergave van uw bezoek. Voor testdoeleinden kunt u het cookie verwijderen zodat de volgende aanroep de eerste paginaweergave voor het bijbehorende bezoek is:

   1. Zoek op het tabblad Toepassing het `adcloud` -cookie en controleer of het cookie `_les_v` (laatste bezoek) bevat met de waarde `y` en of de tijdstempel voor de UTC-epoche binnen 30 minuten vervalt.
      1. Verwijder het cookie `adcloud` en vernieuw de pagina.

1. (Implementaties die de code Experience Cloud Identity Service `visitorAPI.js` gebruiken) Filter op `/b/ss` om de treffer voor Analytics te zien.

   ![ Filteren op `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementaties die de Experience Platform [!DNL Web SDK] `alloy.js` code) gebruiken filter op `/interact` om te controleren of de lading van de verzoeklading aan Edge Network `advertisingStitchID` bevat.

   ![ Filteren op `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Vergelijk de id-waarden tussen de twee treffers. Alle waarden moeten in de parameters van het vraagkoord behalve rapportreeks ID in de treffer van Analytics zijn, die de weg URL onmiddellijk na `/b/ss/` is.

   | ID | Parameter Analytics | Edge Network | Adobe Advertising-parameter |
   | --- | --- | --- | --- |
   | Experience Cloud IMS Org | `mcorgid` |  | `_les_imsOrgid` |
   | Aanvullende gegevens-id | sdid |  | `_les_sdid` |
   | Titel-id | stitchId | `advertisingStitchID` onder de eigenschap `_adcloud` |  |
   | Analyserapportsuite | De waarde na `/b/ss/` | | `_les_rsid` |
   | Experience Cloud-bezoeker-id | midden |  | `_les_mid` |

   Als de id-waarden overeenkomen, wordt de JavaScript-implementatie bevestigd. Adobe Advertising verzendt de [!DNL Analytics] -server alle eventuele doorklikgegevens of doorkijkgegevens.

#### De code bevestigen met [!DNL Adobe Experience Cloud Debugger]

1. Open [[!DNL Adobe Experience Cloud Debugger] ](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) op uw homepage.
1. Ga naar de tab [!UICONTROL Network] .
1. Klik in de werkbalk [!UICONTROL Solutions Filter] op [!UICONTROL Adobe Advertising] en [!UICONTROL Analytics] .
1. Zoek in de parameterrij [!UICONTROL Request URL - Hostname] naar `lasteventf-tm.everesttech.net` .
1. In de [!UICONTROL Request - Parameters] rij, controle de gegenereerde signalen, gelijkend op Stap 3 in &quot;[ hoe te om de Code met  [!DNL Chrome Developer Tools]](#validate-js-chrome) te bevestigen.&quot;
   * (Implementaties die de code Experience Cloud Identity Service `visitorAPI.js` gebruiken) Zorg ervoor dat de parameter `Sdid` overeenkomt met de parameter `Supplemental Data ID` in het Adobe Analytics-filter.
   * (Implementaties die de Experience Platform-code [!DNL Web SDK] `alloy.js` gebruiken) Zorg ervoor dat de waarde van de parameter `advertisingStitchID` overeenkomt met de `Sdid` die naar de Experience Platform Edge Network wordt verzonden.
   * Als de code niet wordt gegenereerd, controleert u of de Adobe Advertising-cookie is verwijderd op het tabblad [!UICONTROL Application] . Nadat de pagina is verwijderd, vernieuwt u de pagina en herhaalt u het proces.

   ![ [!DNL Analytics for Advertising] JavaScript-code controleren in [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [ Overzicht van  [!DNL Analytics for Advertising]](overview.md)
>* [ Eerste vereisten en belangrijkste informatie voor het uitvoeren van  [!DNL Analytics for Advertising]](prerequisites.md)
