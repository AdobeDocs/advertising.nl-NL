---
title: JavaScript-code voor [!DNL Analytics for Advertising]
description: JavaScript-code voor [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: 7055a9b9d3a68ef2f690e146128d6946e713586a
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# JavaScript-code voor [!DNL Analytics for Advertising]

*Adverteerders met een Adobe Advertising-Adobe Analytics Integration Only*

*Adverteerders DSP alleen reclame*

Voor DSP [!DNL Analytics for Advertising] de integratie houdt mening-door en klik-door plaatsinteractie. Doorklikbezoeken worden bijgehouden aan de hand van de standaard Adobe Analytics-code op uw webpagina&#39;s. de [!DNL Analytics] De parameters AMO ID en EF ID worden in de URL van de bestemmingspagina vastgelegd en in hun respectieve gereserveerde eVars bijgehouden. U kunt doorkijkbezoeken volgen door een JavaScript-fragment in uw webpagina&#39;s te implementeren.

In de eerste paginaweergave van een bezoek aan de site controleert de JavaScript-code voor advertenties van de Adobe om te zien of de bezoeker een advertentie heeft gezien of erop heeft geklikt. Als de gebruiker eerder via een doorklik de site is binnengekomen of geen advertentie heeft gezien, wordt de bezoeker genegeerd. Als de bezoeker een advertentie heeft gezien en de site niet via een doorklikverbinding heeft betreden tijdens het [klik terugkijkvenster](/help/integrations/analytics/prerequisites.md#lookback-a4adc) ingesteld in Adobe Advertising, wordt de JavaScript-code voor Adobe-advertenties (a) gebruikt voor de [Experience Cloud ID-service](https://experienceleague.adobe.com/docs/id-service/using/home.html) om een aanvullende id te genereren (`SDID`) of b) gebruikt de Adobe Experience Platform [!DNL Web SDK] `generateRandomID` methode om een `[!DNL StitchID]`. Een van beide id&#39;s wordt gebruikt om gegevens van Adobe Advertising aan te koppelen aan de Adobe Analytics hit van de bezoeker. Adobe Analytics vraagt vervolgens naar Adobe-advertentie voor de AMO-id en EF-id die aan de advertentie zijn gekoppeld. De AMO-id en EF-id&#39;s worden vervolgens in hun respectieve eVars ingevuld. Deze waarden blijven gedurende een bepaalde periode bestaan (standaard 60 dagen).

[!DNL Analytics] verzendt de metriek van het plaatsverkeer (zoals paginameningen, bezoeken, en bestede tijd) en om het even welk [!DNL Analytics] aangepaste of standaardgebeurtenissen voor Adobe-reclame per uur, waarbij de EF-id als sleutel wordt gebruikt. Deze [!DNL Analytics] De metriek loopt dan door het de attributiesysteem van de Adobe Advertising om de omzettingen aan de klik en de belichtingsgeschiedenis te verbinden.

>[!NOTE]
>
>De JavaScript-traceringslogica voor Adobe-advertenties vindt plaats aan de Adobe-zijde en heeft dus vrijwel geen invloed op de laadtijd van de pagina.
>
>De logica voor de [!DNL DCM] gegevensaansluiting naar [!DNL Analytics] (gebruiken [!DNL Google Campaign Manager 360]) voor DSP op de client. Door stitching aan de clientzijde wordt de pagina langzamer geladen en neemt het risico op gegevensverlies toe. Dit gebeurt omdat de [!DNL Analytics] JavaScript moet pingelen [!DNL DoubleClick] en wachten op [!DNL DoubleClick] om de laatste klik-/afbeeldingsgegevens door te geven aan [!DNL Analytics]. Wanneer uw [!DNL DSP] team stelt [!DNL DCM] gegevensconnector, moet u opgeven hoe lang u de pagina wilt vertragen.

## JavaScript-code implementeren

De JavaScript-bibliotheek bestaat uit twee regels die [!DNL Analytics] en Adobe-reclame om met elkaar te communiceren. Als de [!DNL Analytics for Advertising] De integratie is voltooid tijdens de Adobe Advertising-implementatie en u had deze code al moeten ontvangen met instructies over hoe u deze kunt implementeren.

### De code

#### Implementaties die gebruikmaken van de Experience Cloud Identity Service `visitorAPI.js` code

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

#### Implementaties die het Experience Platform gebruiken [!DNL Web SDK] `alloy.js`code

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

### Plaats de code

De [!DNL Analytics for Advertising] De JavaScript-functie moet na de Experience Cloud-id-service komen, maar voordat de code voor metingen van de Analytics App wordt uitgevoerd, zodat de aanvullende id (`SDID`) of `[!DNL StitchID]` kan in uw vraag van Analytics worden omvat.

![Codeplaatsing](/help/integrations/assets/a4adc-code-placement.png)

### Implementatie van code valideren

U kunt validatie uitvoeren met elk pakketsniffertype (zoals [!DNL Charles], [!DNL Fiddler], of [!DNL Chrome Developer Tools]) door de waarden van de vier id&#39;s te vergelijken tussen de aanvraag voor Adobe Advertising en de aanvraag voor [!DNL Analytics], zoals hieronder beschreven.

#### De code bevestigen met [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Openen [!DNL Chrome Developer Tools] en klik op de knop **Netwerk** tab.

1. Een websitepagina laden die de [!DNL Analytics for Advertising] JavaScript.

1. Filter de [!UICONTROL Network] tab by `last` en bekijk twee rijen:

   ![Filteren op laatste](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * De eerste rij is de aanroep naar de JavaScript-bibliotheek en krijgt de naam `last-event-tag-latest.min.js`.
   * De tweede rij is de oproep die het verzoek naar Adobe Advertising verzendt. Het begint als volgt: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Als je de oproep tot Adobe Advertising niet ziet, is dit mogelijk niet de eerste paginaweergave van je bezoek. Voor testdoeleinden kunt u de cookie verwijderen zodat de volgende aanroep de eerste paginaweergave voor het bijbehorende bezoek wordt:
   1. Zoek op het tabblad Toepassing naar het tabblad `adcloud` cookie, en controleer of de cookie `_les_v` (laatste bezoek) met een waarde van `y` en een tijdstempel voor UTC-tijdperk die over 30 minuten verloopt.
      1. Verwijder de `ad cloud` cookie maken en de pagina vernieuwen.


1. (Implementaties die gebruikmaken van de Experience Cloud Identity Service `visitorAPI.js` code) Filter op `/b/ss` om de Analytics-hit te zien.

   ![Filteren op `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementaties die het Experience Platform gebruiken [!DNL Web SDK] `alloy.js`code) Filter op `/interact` om te verifiëren dat de verzoeklading aan het Netwerk van de Rand bevat `advertisingStitchID`.

   ![Filteren op `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Vergelijk de id-waarden tussen de twee treffers. Alle waarden worden opgenomen in parameters van queryreeksen, behalve de id van de rapportsuite in de hit Analytics. Dit is het URL-pad dat onmiddellijk volgt `/b/ss/`.

   | ID | Parameter Analytics | Edge Network | Adobe-advertentieparameter |
   | --- | --- | --- | --- |
   | Experience Cloud IMS Org | `mcorgid` |  | `_les_imsOrgid` |
   | Aanvullende gegevens-id | sdid |  | `_les_sdid` |
   | Titel-id | stitchId | `advertisingStitchID` onder de `_adcloud` eigenschap |  |
   | Analyserapportsuite | De waarde na `/b/ss/` |  | `_les_rsid` |
   | Experience Cloud-bezoeker-id | midden |  | `_les_mid` |

   Als de id-waarden overeenkomen, wordt de JavaScript-implementatie bevestigd. Adobe Advertising [!DNL Analytics] eventuele doorklikgegevens of doorlopende trackinggegevens op de server te plaatsen.

#### De code bevestigen met [!DNL Adobe Experience Cloud Debugger]

1. Open de [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html) op je homepage.
1. Ga naar de [!UICONTROL Network] tab.
1. In de [!UICONTROL Solutions Filter] werkbalk, klikt u op [!UICONTROL Adobe Advertising] en [!UICONTROL Analytics].
1. In de [!UICONTROL Request URL – Hostname] parameterrij, zoeken `lasteventf-tm.everesttech.net`.
1. In de [!UICONTROL Request – Parameters] rij, controleer de geproduceerde signalen, gelijkend op Stap 3 in &quot;[De code bevestigen met [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (Implementaties die gebruikmaken van de Experience Cloud Identity Service `visitorAPI.js` code) Controleer of de `Sdid` parameter komt overeen met `Supplemental Data ID` in het Adobe Analytics-filter.
   * (Implementaties die het Experience Platform gebruiken [!DNL Web SDK] `alloy.js`code) Controleer of de waarde van de `advertisingStitchID` parameter komt overeen met `Sdid` naar het Experience Platform Edge Network verzonden.
   * Als de code niet wordt gegenereerd, controleert u of de Adobe-advertentiecookie is verwijderd in het dialoogvenster [!UICONTROL Application] tab. Nadat de pagina is verwijderd, vernieuwt u de pagina en herhaalt u het proces.

   ![Controle [!DNL Analytics for Advertising] JavaScript-code in [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Overzicht van [!DNL Analytics for Advertising]](overview.md)
>* [Vereisten en belangrijke Informatie voor het Uitvoeren [!DNL Analytics for Advertising]](prerequisites.md)

