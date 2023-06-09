---
title: Opties voor het bijhouden van conversies voor Zoeken, Sociale & Handel
description: Meer informatie over opties voor het bijhouden van conversies voor Zoeken, Sociale & Handel.
source-git-commit: 5dadb0bea063f454dcfde46c0a4cc747290767c8
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Opties voor het bijhouden van conversies voor Zoeken, Sociale &amp; Handel

Met Zoeken, Sociaal en Handel kunt u conversiegegevens gebruiken die op de volgende manieren worden bijgehouden:

* **Adobe omzettingen met bijgehouden reclame:** De adverteerder voegt op elke conversiepagina een Adobe-tag voor het bijhouden van advertenties in. De tag verzendt de conversiegegevens naar een trackingserver. U kunt de verouderde pixel van derden of de nieuwere pixel van de eerste partij gebruiken. Zie &quot;[Vergelijking van elke methode voor het bijhouden van conversies](#conversion-tracking-comparison).&quot;

* **Adobe Analytics-conversies:** De adverteerder gebruikt Adobe Analytics tracking voor alle conversies. Voor deze optie is Adobe Advertising-Adobe Analytics-integratie vereist. Zie &quot;[Adobe Analytics-conversie bijhouden](conversion-tracking-analytics.md)&quot; voor meer informatie .

* **[!DNL Google Analytics]conversies:** De adverteerder gebruikt de [!DNL Google Analytics] tag gebruiken om alle conversies bij te houden. Zie &quot;[[!DNL Google Ads] conversiegegevens in Zoeken, Sociaal, &amp; Handel](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)&quot; voor meer informatie over de omzettingen die automatisch worden gesynchroniseerd.

* **Conversies die door adverteerders worden bijgehouden:** (Alleen klanten voor zoeken, sociale zaken en handel) De adverteerder verschaft een feed-bestand met een willekeurige combinatie van online- en offlineconversiegegevens. Zie &quot;[Conversie bijhouden met een EF-id-feed](feed-efid.md)&quot; en &quot;[Conversie bijhouden met een transactie-id-feed](feed-transaction-id.md).&quot;

## Vergelijking van elke methode voor het bijhouden van conversies {#conversion-tracking-comparison}

Aangezien het browser koekjesbeleid nog steeds strikter wordt, is het belangrijk om uw huidige het volgen mogelijkheden te begrijpen en uw beste opties voor de langere termijn te identificeren.

| Trackingmethode | Beschrijving | Beperkingen | Voordelen | Aanbevolen? |
|----|----|----|----|----|
| Adobe Analytics | Adverteerders met [Adobe Analytics for Advertising](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) importeren, [!DNL Analytics] standaard- en aangepaste gebeurtenissen voor Adobe Advertising voor rapportage en optimalisatie. | <ul><li>[!DNL Safari] staat slechts een 7-dagen omzettingsraadpleging toe, die bij herhaalde plaatsbezoeken tijdens het raadplegingsvenster wordt teruggesteld.</li><li> Verwacht vergelijkbare beperkingen in [!DNL Chrome] in 2024.</li></ul> | <ul><li>Naadloze integratie met [!DNL Analytics]</li> <li>Betaalde zoekgegevens bekijken in [!DNL Analytics] Analysis Workspace</li><li>Voordelen boven betaalde zoekopdracht</li></ul> | Ja |
| Pixel verouderde Adobe Advertising | Adverteerders voegen verouderde Adobe Advertising-afbeeldingen of JavaScript-pixels toe aan hun conversiepagina&#39;s. De pixel wordt geactiveerd wanneer een gebruiker die op een advertentie heeft geklikt de pagina bereikt. Deze methode is afhankelijk van cookies van derden. | <ul><li>[!DNL Safari] blokkeert alle conversie-tracking met deze methode.</li><li>Verwacht vergelijkbare beperkingen in [!DNL Chrome] in 2024.</li></ul> | De pixel is al geïmplementeerd. U moet echter [de extra ITP-toewijzingstag implementeren](itp-conversion-mapping-tag.md).<br><br>Aanbeveling: Schakel over naar de pixel van de eerste partij. | Nee |
| Pixel van eerste Adobe Advertising | Adverteerders doen het volgende: <ul><li>De JavaScript-bibliotheek implementeren voor de [Adobe Experience Cloud ID-service (ECID)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) op hun gehele site.</li><li>De Adobe Advertising toevoegen [JavaScript-tags met ITP-toewijzing](itp-conversion-mapping-tag.md) naar elke pagina die een openingspagina kan zijn, door een zoekklik (idealiter op alle pagina&#39;s, omdat de openingspagina&#39;s in de loop der tijd kunnen veranderen). Met de tag kan Adobe Advertising een conversiegebeurtenis bijhouden die plaatsvindt op een pagina die grote getallen omzet in wetenschappelijke notaties op de landingspagina.</li><li>De Adobe Advertising toevoegen [JavaScript-conversietag v3](format-conversion-tag-jsv3.md) naar conversiepagina&#39;s.</li></ul> | <ul><li>[!DNL Safari] staat slechts een 7-dagen omzettingsraadpleging toe, die bij herhaalde plaatsbezoeken tijdens het raadplegingsvenster wordt teruggesteld.</li><li>Verwacht vergelijkbare beperkingen in [!DNL Chrome] in 2022.</li></ul> | [!DNL Safari] houdt omzettingen tijdens de zeven-dagraadpleging bij. Omdat de terugzoekactie bij herhaalde plaatsbezoeken tijdens het terugzoekvenster wordt teruggesteld, beïnvloedt de beperking niet alle [!DNL Safari] gebruikers. | Nee |
| EFID Feed | De zoekaccounts van de adverteerder zijn zo ingesteld dat doel-URL&#39;s/uiteindelijke URL&#39;s met unieke Adobe-id&#39;s (tokens) voor advertenties worden gegenereerd. Wanneer een gebruiker op een advertentie klikt, maakt Adobe Advertising een unieke id (`EFID`) en geeft deze weer aan het einde van de laatste URL. Het clientsysteem van de adverteerder legt de EFID vast als een unieke id voor conversies die het resultaat zijn van de klik en stuurt deze naar Adobe Advertising in een inkomstenbron die de EFID, de transactiedatum en de conversie-eigenschap bevat. De Adobe Advertising gebruikt dan EFID om de omzetting in de originele klik aan te passen. | <ul><li>De adverteerder moet een manier hebben om de EFID vast te leggen en automatische feeds dagelijks naar de Adobe Advertising te sturen.</li><li>Conversies kunnen maximaal 180 dagen (per advertentie van Adobe) of binnen de grenzen van het systeem van de adverteerder worden bijgehouden.</li></ul> | <ul><li>Deze methode gebruikt conversiegegevens van de eerste partij, zodat deze niet worden beïnvloed door cookie-beperkingen van derden.</li><li>Online- en offline-conversies kunnen in één feed worden verzonden.</li><li>Er zijn geen codewijzigingen of -codes vereist voor de site.</li></ul> | Ja |
| Transactie-id-feed [mengvoeders] | Adverteerders voegen Adobe Advertising pixels toe die een parameter voor een unieke transactie-id bevatten (`ev_transid=&lt;transid&gt;`) op hun webpagina&#39;s en Adobe Advertising legt de unieke transactie-id vast die is gemaakt wanneer de pixel wordt geactiveerd. Het clientsysteem van de adverteerder legt ook de [!UICONTROL Transaction ID] en verzendt Adobe Advertising een opbrengstvoer voor off-line omzettingen met aanpassing [!UICONTROL Transaction ID] waarden | <ul><li>Als de adverteerder de verouderde pixel gebruikt, die [!DNL Safari] blokkeert, wordt de id niet vastgelegd voor gebruik voor offlinegegevens.</li><li>De feed is niet geautomatiseerd.</li></ul> | <ul><li>Als u de pixel van de eerste partij uitvoert, dan [!UICONTROL Transaction ID] is vastgelegd in [!DNL Safari].</li><li>Verschaft het bijhouden van offline/goedgekeurde conversiegebeurtenissen.</li></ul> | Nee |
| Google Conversies | Conversies bijgehouden met [!DNL Google Analytics] -tags worden automatisch via een API-verbinding naar Adobe Advertising geïmporteerd. Elke conversienaam heeft een `&quot;GGL_&quot;` voorvoegsel. | <ul><li>Google houdt gewoonlijk geen offline gegevens bij.</li><li>Microsoft® Advertising conversions zijn niet inbegrepen.</li></ul> | Google gebruikt automatisch leren om te extrapoleren &quot;[gemodelleerde omzettingen](https://support.google.com/google-ads/answer/10081327).&quot; | Nee |

<table style="table-layout:auto">

<!--
| Microsoft Advertising Conversions | Conversions tracked with Microsoft Advertising universal event tags (UET) are automatically imported to Adobe Advertising via an API connection. Each conversion name has a &quot;???&quot; prefix. | Microsoft Advertising typically doesn't track offline data. Google conversions aren't included. | ?? | No |
-->

>[!MORELIKETHIS]
>
>* [Informatie over conversietags voor Adobe-advertenties](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Analytics-conversie bijhouden](/help/search-social-commerce/tracking/conversion-tracking-analytics.md)
>* [Conversie bijhouden met een EF-id-feed](/help/search-social-commerce/tracking/feed-efid.md)
>* [Conversie bijhouden met een transactie-id-feed](/help/search-social-commerce/tracking/feed-transaction-id.md)
