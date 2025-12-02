---
title: '[!UICONTROL Campaign Assist Report]'
description: Meer informatie over de [!UICONTROL Campaign Assist Report] .
exl-id: c89b4c9f-16d5-4e1a-a73f-6cc99dd3f526
feature: Search Reports, Search Assist Reports
source-git-commit: 7a87d3c3827125adb97f50986823568c9aef8c24
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 0%

---

# De [!UICONTROL Campaign Assist Report]

*Advertisers met Onderzoek, Sociale, &amp; Commerce klikken het volgen en met omzetting het volgen van Adobe Advertising, Adobe Analytics (met een [!DNL Analytics] integratie), of verstrekt in voer gebruikend een teken (`ef_id`) slechts*

[!UICONTROL Campaign Assist Report] geeft aan welke campagnes het conversieproces hebben ondersteund. De rapporten hoe elk patroon van campagnes de waarvan advertenties tot één of meerdere omzettingen hebben geleid tot uw algemene omzettingen heeft bijgedragen. U kunt bijvoorbeeld zien hoeveel conversies hebben plaatsgevonden toen gebruikers een advertentie zagen vanuit Campagne A, vervolgens op een advertentie klikten vanuit Campagne B en vervolgens een bestelling plaatsten. Op dezelfde manier kunt u zien hoeveel omzettingen hebben plaatsgevonden nadat gebruikers via meer dan tien campagnes op advertenties hebben gereageerd.

De rapportresultaten omvatten samengevoegde gegevens voor elk patroon van campagnes in de omzettingsweg — tot N vroegste campagnes — voor gebeurtenissen die binnen het van de adverteerder [&#x200B; voorkwamen klikt raadplegingsvenster &#x200B;](/help/search-social-commerce/glossary.md#c-d) en [&#x200B; het venster van de imitatieraadpleging &#x200B;](/help/search-social-commerce/glossary.md#i-j). Als u bijvoorbeeld een padgrootte van vijf (5) selecteert, bevat het rapport conversiepaden die maximaal de vijf vroegste campagnes omvatten, met één rij voor elk patroon van campagnes waarvan de gebeurtenissen zijn bijgehouden. Elke rij toont één patroon van campagnes, met inbegrip van de eerste campagne in de weg en de laatste campagne die in omzettingen resulteerde (zelfs als de laatste campagne buiten de gespecificeerde weggrootte is.) Standaard staan de rijen in oplopende volgorde op basis van het aantal campagnes in het pad.

U kunt optioneel voor elke rij geaggregeerde conversiegegevens, inclusief uw aangepaste metriek, opnemen. Wanneer u omzettingen/inkomstenkolommen in het rapport opneemt, dan wordt elk omzettingstype vertegenwoordigd in vier kolommen, die a) het totale aantal omzettingen, b) het percentage van uw algemene omzettingen tonen die aan dat campagnerepatroon werden toegeschreven, c) de gemiddelde latentie in dagen van de eerste gebeurtenis (in de eerste campagne) aan een omzetting, en d) de gemiddelde latentie in dagen van de laatste gebeurtenis (in de laatste campagne) aan een omzetting. Wanneer het omzettingspad meer campagnes dan de gespecificeerde weggrootte omvat, dan omvat het rapport extra rijen die gegevens voor omzettingen groeperen die uit de hogere aantallen campagnes (zoals alle patronen resulteerden die zes campagnes omvatte).

U kunt desgewenst ook het advertentienetwerk en/of het gebeurtenistype na de campagnenaam, zoals `<campaign name> (Google) click` omvatten.

U kunt gegevens van de vorige 18 maanden bekijken.

>[!TIP]
>
>Als uw merktrefwoorden zich in een andere campagne bevinden dan uw algemene trefwoorden, wordt in het rapport aangegeven of uw merktrefwoorden bijdragen aan conversies.

## Beschikbare kolommen

Het volgende is de kolommen die voor elk rapport beschikbaar zijn. De standaardkolommen worden standaard automatisch opgenomen. U kunt de beschikbare douanekolommen van de sectie van Kolommen van de rapportmontages toevoegen.

| Kolom | Standaard? | Beschrijving |
| ---- | ---- | ---- |
| [!UICONTROL 1st Campaign] t/m [!UICONTROL 5th Campaign] | Standaard | De vijf vroegste campagnes in de omzettingsweg die binnen de adverteerder [&#x200B; voorkwam klikken raadplegingsvenster &#x200B;](/help/search-social-commerce/glossary.md#c-d) en [&#x200B; het venster van de imkerraadpleging &#x200B;](/help/search-social-commerce/glossary.md#i-j).<br><br> als u om het even welke rapportopties omvatte om op het advertentienetwerk, de rekeningsnaam, of gebeurtenistype na de entiteitnaam te wijzen, dan wordt die informatie omvat na de campagnenaam (zoals `"<"campaign name> [Google] [Account1] [impression]`&quot;). |
| [!UICONTROL Path Size] | Standaard | Het aantal campagnes in de omzettingsweg die binnen de adverteerder [&#x200B; voorkwam klikt raadplegingsvenster &#x200B;](/help/search-social-commerce/glossary.md#c-d) en [&#x200B; venster van de imkerraadpleging &#x200B;](/help/search-social-commerce/glossary.md#i-j). |
| [!UICONTROL First Campaign] | Standaard | De eerste campagne in het conversiepad. |
| [!UICONTROL Last Campaign] | Standaard | De laatste campagne die in omzettingen resulteerde (zelfs als het laatste sleutelwoord buiten de gespecificeerde weggrootte is.)<br><br> als u om het even welke rapportopties omvatte om op het advertentienetwerk, de rekeningsnaam, of gebeurtenistype na de entiteitnaam te wijzen, dan wordt die informatie omvat na de campagnenaam (zoals `"<"campaign name> [Google] [Account1] [impression]`&quot;). |
| \[Advertiser-specifieke, aangepaste (afgeleide) metriek\] | Aangepast | De waarde voor douanemetrisch u hebt gecreeerd die van bestaande metriek wordt berekend. |
| \[Specifieke conversiemetriek voor adverteerders\] | Aangepast | Het aantal omzettingen voor een gespecificeerde metrische of metrische plaatsbepaling van de omzetting. |
| [!UICONTROL % of Total] \[metrisch omzetten\] | Automatisch | (Niet beschikbaar in rapportmontages maar automatisch inbegrepen in rapportoutput voor elke inbegrepen omzettingsmetriek) Het aantal omzettingen voor gespecificeerde omzettings metrisch die uit het campagnerepatroon voortkwam. |
| [!UICONTROL 6th Campaign] t/m [!UICONTROL 20th Campaign] | Aangepast | Zesde door 20e campagnes in de omzettingsweg die binnen het paneel van de adverteerder [&#x200B; voorkwam klikken raadplegings achteruit &#x200B;](/help/search-social-commerce/glossary.md#c-d) en [&#x200B; venster van de imitatieraadpleging &#x200B;](/help/search-social-commerce/glossary.md#i-j).<br><br> als u om het even welke rapportopties omvatte om op het advertentienetwerk, de rekeningsnaam, of gebeurtenistype na de entiteitnaam te wijzen, dan wordt die informatie omvat na de campagnenaam (zoals `"<"campaign name> [Baidu] [Account1] [click]`&quot;). |
| [!UICONTROL Avg. Conv. Latency (First Campaign To Conversion)] \[metrisch omzetten\] | Automatisch | (Niet beschikbaar in rapportmontages maar automatisch inbegrepen in rapportoutput voor elke inbegrepen omzettings metrisch) De gemiddelde vertraging in dagen van de eerste gebeurtenis (in de eerste campagne) aan een omzetting. |
| [!UICONTROL Avg. Conv. Latency (Last Campaign To Conversion)] \[metrisch omzetten\] | Automatisch | (Niet beschikbaar in rapportinstellingen maar automatisch opgenomen in de rapportuitvoer) De gemiddelde vertraging in dagen vanaf de laatste gebeurtenis (in de laatste campagne) tot een conversie. |
| [!UICONTROL EF Campaign ID] | Aangepast | De numerieke id die door Search, Social &amp; Commerce wordt toegewezen aan de campagne. |
| [!UICONTROL EF Portfolio Group ID] | Aangepast | De numerieke id voor de portfoliogroep waartoe het portfolio behoort. |
| [!UICONTROL EF Search Engine ID] | Aangepast | De numerieke id die Search, Social en Commerce toewijst aan het advertentienetwerk: <i>[!UICONTROL 3]</i> for [!DNL Google Ads], <i>[!UICONTROL 10]</i> for [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> for [!DNL Meta], <i>[!UICONTROL 86]</i> for [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> for [!DNL Naver], <i>[!UICONTROL 88]</i> for [!DNL Baidu], <i>[!UICONTROL 90]</i> for [!DNL Yandex], <i>[!UICONTROL 94]</i> for [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> for [!DNL Yahoo Native] (afgekeurd) of <i>[!UICONTROL 106]</i> for [!DNL Pinterest] (afgekeurd). |
| [!UICONTROL Portfolio ID] | Aangepast | De numerieke portefeuille-id. |
| [!UICONTROL User SE Account ID] | Aangepast | De numerieke id die door Search, Social &amp; Commerce wordt toegewezen aan het advertentienetwerk. |

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer bijstaat rapporten &#x200B;](assist-report-about.md)
>* [&#x200B; De [!UICONTROL Channel Assist Report]](channel-assist-report.md)
>* [&#x200B; De [!UICONTROL Keyword Assist Report]](keyword-assist-report.md)
>* [&#x200B; sta rapportmontages &#x200B;](assist-report-settings.md) bij
>* [&#x200B; produceer en bijstaat rapport &#x200B;](assist-report-generate.md)
