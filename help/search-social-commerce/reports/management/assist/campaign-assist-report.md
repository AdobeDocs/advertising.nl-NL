---
title: '[!UICONTROL Campaign Assist Report]'
description: Meer informatie over de [!UICONTROL Campaign Assist Report].
exl-id: 7fbc9c17-c77d-485b-8d51-5e5a153d7a2b
feature: Search Reports, Search Assist Reports
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# De [!UICONTROL Campaign Assist Report]

*Adverteerders met Zoeken, Sociale Zaken &amp; Handel klikken het volgen en met omzetting het volgen van van Adobe Advertising, Adobe Analytics (met [!DNL Analytics] integratie), of verstrekt in voer gebruikend een teken (`ef_id`alleen )*

De [!UICONTROL Campaign Assist Report] Hiermee wordt aangegeven welke campagnes het conversieproces hebben ondersteund. De rapporten hoe elk patroon van campagnes de waarvan advertenties tot één of meerdere omzettingen hebben geleid tot uw algemene omzettingen heeft bijgedragen. U kunt bijvoorbeeld zien hoeveel conversies hebben plaatsgevonden toen gebruikers een advertentie zagen vanuit Campagne A, vervolgens op een advertentie klikten vanuit Campagne B en vervolgens een bestelling plaatsten. Op dezelfde manier kunt u zien hoeveel omzettingen hebben plaatsgevonden nadat gebruikers via meer dan tien campagnes op advertenties hebben gereageerd.

De rapportresultaten omvatten geaggregeerde gegevens voor elk patroon van campagnes in het conversiepad — tot aan de N vroegste campagnes — voor gebeurtenissen die binnen de adverteerders hebben plaatsgevonden [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j). Als u bijvoorbeeld een padgrootte van vijf (5) selecteert, bevat het rapport conversiepaden die maximaal de vijf vroegste campagnes omvatten, met één rij voor elk patroon van campagnes waarvan de gebeurtenissen zijn bijgehouden. Elke rij toont één patroon van campagnes, met inbegrip van de eerste campagne in de weg en de laatste campagne die in omzettingen resulteerde (zelfs als de laatste campagne buiten de gespecificeerde weggrootte is.) Standaard staan de rijen in oplopende volgorde op basis van het aantal campagnes in het pad.

U kunt optioneel voor elke rij geaggregeerde conversiegegevens, inclusief uw aangepaste metriek, opnemen. Wanneer u omzettingen/inkomstenkolommen in het rapport opneemt, dan wordt elk omzettingstype vertegenwoordigd in vier kolommen, die a) het totale aantal omzettingen, b) het percentage van uw algemene omzettingen tonen die aan dat campagnerepatroon werden toegeschreven, c) de gemiddelde latentie in dagen van de eerste gebeurtenis (in de eerste campagne) aan een omzetting, en d) de gemiddelde latentie in dagen van de laatste gebeurtenis (in de laatste campagne) aan een omzetting. Wanneer het omzettingspad meer campagnes dan de gespecificeerde weggrootte omvat, dan omvat het rapport extra rijen die gegevens voor omzettingen groeperen die uit de hogere aantallen campagnes (zoals alle patronen resulteerden die zes campagnes omvatte).

U kunt desgewenst ook het advertentienetwerk en/of het gebeurtenistype na de campagnenaam, zoals `<campaign name> (Google) click`.

U kunt gegevens van de vorige 18 maanden bekijken.

>[!TIP]
>
>Als uw merktrefwoorden zich in een andere campagne bevinden dan uw algemene trefwoorden, wordt in het rapport aangegeven of uw merktrefwoorden bijdragen aan conversies.

## Beschikbare kolommen

Het volgende is de kolommen die voor elk rapport beschikbaar zijn. De standaardkolommen worden standaard automatisch opgenomen. U kunt de beschikbare douanekolommen van de sectie van Kolommen van de rapportmontages toevoegen.

| Kolom | Standaard? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL 1st Campaign] tot [!UICONTROL 5th Campaign] | Standaard | De vijf oudste campagnes in het conversiepad die binnen de adverteerders plaatsvonden [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j).<br><br>Als u een van de rapportopties hebt opgenomen om het advertentienetwerk, de accountnaam of het gebeurtenistype na de entiteitsnaam aan te geven, wordt die informatie opgenomen na de naam van de campagne (zoals `"<"campaign name> [Google] [Account1] [impression]`&quot;). |
| [!UICONTROL Path Size] | Standaard | Het aantal campagnes in het conversiepad dat is uitgevoerd binnen de adverteerders [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Campaign] | Standaard | De eerste campagne in het conversiepad. |
| [!UICONTROL Last Campaign] | Standaard | De laatste campagne die in omzettingen resulteerde (zelfs als het laatste sleutelwoord buiten de gespecificeerde weggrootte is.)<br><br>Als u een van de rapportopties hebt opgenomen om het advertentienetwerk, de accountnaam of het gebeurtenistype na de entiteitsnaam aan te geven, wordt die informatie opgenomen na de naam van de campagne (zoals `"<"campaign name> [Google] [Account1] [impression]`&quot;). |
| \[Advertiser-specifieke, aangepaste (afgeleide) metriek\] | Aangepast | De waarde voor een aangepaste metrische waarde die u hebt gemaakt en die wordt berekend op basis van bestaande metriek. |
| \[Advertiser-specifieke transactieeigenschappen\] | Aangepast | Het aantal omzettingen voor een gespecificeerde transactiebezit of metrisch van de plaatsovereenkomst. |
| [!UICONTROL % of Total] \[eigenschap transactie\] | Automatisch | (Niet beschikbaar in rapportmontages maar automatisch inbegrepen in rapportoutput voor elk inbegrepen transactiebezit) Het aantal omzettingen voor een gespecificeerde transactiebezit dat uit het campagnetatroon resulteerde. |
| [!UICONTROL 6th Campaign] tot [!UICONTROL 20th Campaign] | Aangepast | De zesde tot en met de twintigste campagne in het conversiepad dat binnen de adverteerders [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j).<br><br>Als u een van de rapportopties hebt opgenomen om het advertentienetwerk, de accountnaam of het gebeurtenistype na de entiteitsnaam aan te geven, wordt die informatie opgenomen na de naam van de campagne (zoals `"<"campaign name> [Baidu] [Account1] [click]`&quot;). |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[eigenschap transactie\] | Automatisch | (Niet beschikbaar in rapportmontages maar automatisch inbegrepen in rapportoutput voor elke inbegrepen transactiebezit) De gemiddelde vertraging in dagen van de eerste gebeurtenis (in de eerste campagne) aan een omzetting. |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[eigenschap transactie\] | Automatisch | (Niet beschikbaar in rapportinstellingen maar automatisch opgenomen in de rapportuitvoer) De gemiddelde vertraging in dagen vanaf de laatste gebeurtenis (in de laatste campagne) tot een conversie. |
| [!UICONTROL EF Campaign ID] | Aangepast | De numerieke id die Search, Social &amp; Commerce toewijst aan de campagne. |
| [!UICONTROL EF Portfolio Group ID] | Aangepast | De numerieke id voor de portfoliogroep waartoe het portfolio behoort. |
| [!UICONTROL EF Search Engine ID] | Aangepast | De numerieke id die Search, Social &amp; Commerce toewijst aan het advertentienetwerk: <i>[!UICONTROL 3]</i> for [!DNL Google Ads], <i>[!UICONTROL 10]</i> for [!DNL Microsoft® Advertising], <i>[!UICONTROL 45]</i> for [!DNL Meta], <i>[!UICONTROL 86]</i> for [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> for [!DNL Naver], <i>[!UICONTROL 88]</i> for [!DNL Baidu], <i>[!UICONTROL 90]</i> for [!DNL Yandex], <i>[!UICONTROL 94]</i> for [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> for [!DNL Yahoo Native] (afgekeurd), of <i>[!UICONTROL 106]</i> for [!DNL Pinterest] (vervangen). |
| [!UICONTROL Portfolio ID] | De numerieke portefeuille-id. |
| [!UICONTROL User SE Account ID] | De numerieke id die Search, Social &amp; Commerce toewijst aan het advertentienetwerk. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Over rapporten voor Help](assist-report-about.md)
>* [De [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [De [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [Rapportinstellingen voor assistentie](assist-report-settings.md)
>* [Een rapport voor assistentie genereren](assist-report-generate.md)
