---
title: '[!DNL Analytics] Gegevens in Adobe Advertising'
description: '[!DNL Analytics] Gegevens in Adobe Advertising'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: 94a5b5591aef0aa5ae5d3459d547f52d939d559c
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# [!DNL Analytics] Gegevens in Adobe Advertising

*Advertisers met slechts een integratie Adobe Advertising-Adobe Analytics*

## Analysesegmenten

Alle segmenten die zijn gemaakt in [!DNL Analytics] en gepubliceerd naar Experience Cloud.

Het duurt 24 tot 48 uur om nieuwe segmenten weer te geven in Adobe Advertising. Updates voor bestaande segmenten worden binnen ongeveer acht uur gesynchroniseerd.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Metingen voor betrokkenheid van site

>[!NOTE]
>
>* [!DNL Analytics] geeft gebeurtenissen voor de EF-id [!DNL eVar] door aan Adobe Advertising.  De standaardintegratie steunt het verzenden van berekende metriek of andere dimensies ([!DNL eVars]) in Adobe Advertising niet. Als de berekende metrisch volledig in een douanegebeurtenis kan worden gevangen, echter, dan kan Adobe Advertising de douanegebeurtenis opnemen.
>* [!DNL Analytics] geeft gegevens per uur door aan Adobe Advertising.

* [!UICONTROL Timespent_secs_1stvisit]: Het aantal seconden dat de bezoeker tijdens het eerste bezoek aan de site heeft doorgebracht.
* [!UICONTROL Timespent_secs_total]: Het totale aantal seconden dat aan de site is doorgebracht tijdens alle bezoeken in het venster voor terugzoeken van klikken.
* [!UICONTROL Pageviews_1stvisit]: Het aantal paginaweergaven op de site tijdens het eerste bezoek van de bezoeker.
* [!UICONTROL Pageviews_total]: Het totale aantal paginaweergaven op de site bij alle bezoeken in het venster voor terugzoeken van klikken.
* [[!UICONTROL Bounces] metrisch &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html?lang=nl-NL)
* [[!UICONTROL Visits] metrisch &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=nl-NL)
* [!UICONTROL ef_id_instances]: Het aantal keren dat [!DNL Analytics] een [!UICONTROL EF ID] heeft verzameld.

## Omzettingsmetriek

[!DNL Analytics] geeft de conversiemetriek dagelijks door aan Adobe Advertising.

### Standaardomzettingscijfers

* [[!UICONTROL Revenue] metrisch &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html?lang=nl-NL)
* [[!UICONTROL Orders] metrisch &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html?lang=nl-NL)
* [[!UICONTROL Units] metrisch &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html?lang=nl-NL)
* [[!UICONTROL Carts] metrisch &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html?lang=nl-NL)
* [[!UICONTROL Cart Views] metrisch &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html?lang=nl-NL)
* [[!UICONTROL Checkouts] metrisch &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html?lang=nl-NL)
* [[!UICONTROL Cart Additions] metrisch &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html?lang=nl-NL)
* [[!UICONTROL Cart Removals] metrisch &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html?lang=nl-NL)

### Eigen conversiemetingen

Deze metriek is specifiek voor de rapportreeks, zodat variëren de beschikbare metriek voor elke klant en rapportreeks.

### Aangepaste omzettingsmetriek gemaakt van [!DNL eVars] en [!DNL Props]

De beschikbare meetgegevens variëren per klant. Zie &quot;[&#x200B; de Metriek van de Omzetting van Adobe Analytics  [!DNL eVars]  en  [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md).&quot;

### Gereserveerde omzettingswaarden

Deze metriek is specifiek voor de rapportreeks, zodat variëren de beschikbare metriek voor elke klant en rapportreeks.

>[!MORELIKETHIS]
>
>* [&#x200B; Overzicht van  [!DNL Analytics for Advertising]](overview.md)
>* [&#x200B; Metriek van Adobe Advertising in Analysis Workspace &#x200B;](/help/integrations/analytics/advertising-metrics-in-analytics.md)
