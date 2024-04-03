---
title: Opties voor het bijhouden van conversies voor Zoeken, Sociale & Handel
description: Meer informatie over opties voor het bijhouden van conversies voor Zoeken, Sociale Zaken en Handel.
exl-id: 263da6a4-8d72-4882-8784-290a3be6f8fa
feature: Search Tracking
source-git-commit: c23028701ff0064bae04135d9e7a70da4c85e937
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 0%

---

# Opties voor het bijhouden van conversies voor Zoeken, Sociale &amp; Handel

Met Zoeken, Sociaal en Handel kunt u conversiegegevens gebruiken die op de volgende manieren worden bijgehouden:

* **Adobe Advertising-gevolgde omzettingen:** De adverteerder voegt op elke conversiepagina een Adobe Advertising-volgtag in. De tag verzendt de conversiegegevens naar een trackingserver. U kunt de verouderde pixel van derden of de nieuwere pixel van de eerste partij gebruiken. Zie &quot;[Vergelijking van elke methode voor het bijhouden van conversies](#conversion-tracking-comparison).&quot;

* **Adobe Analytics-conversies:** De adverteerder gebruikt Adobe Analytics tracking voor alle conversies. Voor deze optie is integratie tussen Adobe Advertising en Adobe Analytics vereist. Zie &quot;[Adobe Analytics-conversie bijhouden](conversion-tracking-analytics.md)&quot; voor meer informatie .

* **[!DNL Google Analytics]conversies:** De adverteerder gebruikt de [!DNL Google Analytics] tag gebruiken om alle conversies bij te houden. Zie &quot;[[!DNL Google Ads] conversiegegevens in Zoeken, Sociaal, &amp; Handel](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)&quot; voor meer informatie over de omzettingen die automatisch worden gesynchroniseerd.

* **Conversies door adverteerders bijgehouden:** (Alleen klanten voor zoeken, sociale zaken en handel) De adverteerder verschaft een feed-bestand met een willekeurige combinatie van online- en offlineconversiegegevens. Zie &quot;[Conversie bijhouden met een EF-id-feed](feed-efid.md)&quot; en &quot;[Conversie bijhouden met een transactie-id-feed](feed-transaction-id.md).&quot;

## Vergelijking van elke methode voor het bijhouden van conversies {#conversion-tracking-comparison}

Aangezien het browser koekjesbeleid nog steeds strikter wordt, is het belangrijk om uw huidige het volgen mogelijkheden te begrijpen en uw beste opties voor de langere termijn te identificeren.

| Trackingmethode | Beschrijving | Beperkingen | Voordelen | Aanbevolen? |
|----|----|----|----|----|
| Adobe Analytics | Adverteerders met [Adobe Analytics for Advertising](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) importeren, [!DNL Analytics] standaard- en aangepaste gebeurtenissen voor Adobe Advertising voor rapportage en optimalisatie. | <ul><li>[!DNL Safari] staat slechts een 7-dagen omzettingsraadpleging toe, die bij herhaalde plaatsbezoeken tijdens het raadplegingsvenster wordt teruggesteld.</li><li> Verwacht vergelijkbare beperkingen in [!DNL Chrome] in 2024.</li></ul> | <ul><li>Naadloze integratie met [!DNL Analytics]</li> <li>Betaalde zoekgegevens bekijken in [!DNL Analytics] Analysis Workspace</li><li>Voordelen boven betaalde zoekopdracht</li></ul> | Ja |
| Pixel verouderde Adobe Advertising | Adverteerders voegen verouderde Adobe Advertising-afbeeldingen of JavaScript-pixels toe aan hun conversiepagina&#39;s. De pixel wordt geactiveerd wanneer een gebruiker die op een advertentie heeft geklikt, de pagina bereikt. Deze methode is afhankelijk van cookies van derden. | <ul><li>[!DNL Safari] blokkeert alle conversie-tracking met deze methode.</li><li>Verwacht vergelijkbare beperkingen in [!DNL Chrome] in 2024.</li></ul> | De pixel is al geïmplementeerd. U moet echter [Implementeer de extra ITP-toewijzingstag](itp-conversion-mapping-tag.md).<br><br>Aanbeveling: ga naar de pixel van de eerste partij. | Nee |
| Pixel van eerste Adobe Advertising | Adverteerders doen het volgende: <ul><li>De JavaScript-bibliotheek implementeren voor de [Adobe Experience Cloud ID-service (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) op hun gehele site.</li><li>De Adobe Advertising toevoegen [JavaScript-tags met ITP-toewijzing](itp-conversion-mapping-tag.md) naar elke pagina die een openingspagina kan zijn, door een zoekklik (idealiter op alle pagina&#39;s, omdat de openingspagina&#39;s in de loop der tijd kunnen veranderen). Met de tag kan Adobe Advertising een conversiegebeurtenis bijhouden die plaatsvindt op een pagina die grote getallen omzet in wetenschappelijke notaties op de landingspagina.</li><li>De Adobe Advertising toevoegen [JavaScript-conversietag v3](format-conversion-tag-jsv3.md) naar conversiepagina&#39;s.</li></ul> | <ul><li>[!DNL Safari] staat slechts een 7-dagen omzettingsraadpleging toe, die bij herhaalde plaatsbezoeken tijdens het raadplegingsvenster wordt teruggesteld.</li><li>Verwacht vergelijkbare beperkingen in [!DNL Chrome] in 2022.</li></ul> | [!DNL Safari] houdt omzettingen tijdens de zeven dagen raadpleging. Omdat de terugzoekactie bij herhaalde plaatsbezoeken tijdens het terugzoekvenster wordt teruggesteld, beïnvloedt de beperking niet alle [!DNL Safari] gebruikers. | Nee |
| EFID Feed | De zoekaccounts van de adverteerder zijn zo ingesteld dat doel-URL&#39;s/uiteindelijke URL&#39;s met unieke Adobe Advertising-id&#39;s (tokens) worden gegenereerd. Wanneer een gebruiker op een advertentie klikt, maakt Adobe Advertising een unieke id (`EFID`) en geeft deze weer aan het einde van de laatste URL. Het cliëntsysteem van de adverteerder vangt EFID als unieke herkenningsteken voor omzettingen die uit de klik voortvloeien en verzendt het naar Adobe Advertising in een opbrengstvoer die EFID, transactiedatum, en omzettingmetrisch omvat. De Adobe Advertising gebruikt dan EFID om de omzetting in de originele klik aan te passen. | <ul><li>De adverteerder moet een manier hebben om de EFID vast te leggen en automatische feeds dagelijks naar de Adobe Advertising te sturen.</li><li>Conversies kunnen maximaal 180 dagen (per Adobe Advertising) of binnen de grenzen van het systeem van de adverteerder worden bijgehouden.</li></ul> | <ul><li>Deze methode gebruikt conversiegegevens van de eerste partij, zodat deze niet worden beïnvloed door cookie-beperkingen van derden.</li><li>Online- en offline-conversies kunnen in één feed worden verzonden.</li><li>Er zijn geen codewijzigingen of -codes vereist voor de site.</li></ul> | Ja |
| Transactie-id-feed [mengvoeders] | Adverteerders voegen Adobe Advertising pixels toe die een parameter voor een unieke transactie-id bevatten (`ev_transid=&lt;transid&gt;`) op hun webpagina&#39;s en Adobe Advertising legt de unieke transactie-id vast die is gemaakt wanneer de pixel wordt geactiveerd. Het clientsysteem van de adverteerder legt ook de [!UICONTROL Transaction ID] en stuurt Adobe Advertising een inkomstenbron voor offline omzettingen met aanpassing [!UICONTROL Transaction ID] waarden | <ul><li>Als de adverteerder de verouderde pixel gebruikt, die [!DNL Safari] blokkeert, wordt de id niet vastgelegd voor gebruik voor offline gegevens.</li><li>De feed is niet automatisch.</li></ul> | <ul><li>Als u de pixel van de eerste partij uitvoert, dan [!UICONTROL Transaction ID] is vastgelegd in [!DNL Safari].</li><li>Verschaft het bijhouden van offline/goedgekeurde conversiegebeurtenissen.</li></ul> | Nee |
| [!DNL Google] Conversies | Conversies bijgehouden met [!DNL Google Analytics] -tags worden automatisch via een API-verbinding naar Adobe Advertising geïmporteerd. Elke conversienaam heeft een `&quot;GGL_&quot;` voorvoegsel | <ul><li>[!DNL Google] houdt gewoonlijk geen offlinegegevens bij.</li><li>[!DNL Microsoft® Advertising] conversies zijn niet inbegrepen.</li></ul> | [!DNL Google] gebruikt machinaal leren om te extrapoleren &quot;[gemodelleerde omzettingen](https://support.google.com/google-ads/answer/10081327).&quot; | Nee |

<!--
| [!DNL Microsoft Advertising] Conversions | Conversions tracked with [!DNL Microsoft Advertising] universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | [!DNL Microsoft Advertising] typically doesn't track offline data. [!DNL Google] conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Tags voor conversie naar Adobe Advertising bijhouden](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Analytics-conversie bijhouden](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Conversie bijhouden met een EF-id-feed](/help/search-social-commerce/tracking/feed-efid.md)
>* [Conversie bijhouden met een transactie-id-feed](/help/search-social-commerce/tracking/feed-transaction-id.md)
