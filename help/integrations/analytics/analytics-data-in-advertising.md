---
title: '''[!DNL Analytics] Gegevens in Adobe Advertising"'
description: '''[!DNL Analytics] Gegevens in Adobe Advertising"'
feature: Integration with Adobe Analytics
exl-id: e11b0617-44e3-4f28-a065-aa9f6cf3eb5d
source-git-commit: b382184072af88273570fc045d0bcebe24ed81fb
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# [!DNL Analytics] Gegevens in Adobe Advertising

*Adverteerders met alleen Adobe Advertising-Adobe Analytics-integratie*

## Analysesegmenten

Alle segmenten gemaakt in [!DNL Analytics] en gepubliceerd aan Experience Cloud.

Het duurt 24 tot 48 uur om nieuwe segmenten in de Adobe Advertising weer te geven. Updates voor bestaande segmenten worden binnen ongeveer acht uur gesynchroniseerd.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Metrische gegevens over betrokkenheid site

>[!NOTE]
>
>* [!DNL Analytics] geeft gebeurtenissen voor de EF-id-eVar door aan Adobe Advertising.  De standaardintegratie ondersteunt niet het verzenden van berekende metriek of andere dimensies (eVars) naar Adobe Advertising. Als de berekende metrisch volledig in een douanegebeurtenis kan worden gevangen, echter, dan kan de Adobe Advertising de douanegebeurtenis opnemen.
>* [!DNL Analytics] geeft gegevens door aan Adobe Advertising uur.

* [!UICONTROL Timespent_secs_1stvisit]: Het aantal seconden dat de bezoeker tijdens zijn eerste bezoek aan de site heeft doorgebracht.
* [!UICONTROL Timespent_secs_total]: Het totale aantal seconden dat aan de plaats over alle bezoeken binnen het klikraadplegingsvenster wordt doorgebracht.
* [!UICONTROL Pageviews_1stvisit]: Het aantal paginaweergaven op de site tijdens het eerste bezoek van de bezoeker.
* [!UICONTROL Pageviews_total]: Het totale aantal paginaweergaven op de site voor alle bezoeken in het venster voor terugzoeken van klikken.
* [[!UICONTROL Bounces] metrisch](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] metrisch](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: Het aantal keren dat [!DNL Analytics] verzameld en [!UICONTROL EF ID].

## Conversiedetecties

[!DNL Analytics] geeft conversiemetriek dagelijks door aan Adobe Advertising.

### Standaardomzettingscijfers

* [[!UICONTROL Revenue] metrisch](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] metrisch](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] metrisch](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] metrisch](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] metrisch](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] metrisch](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] metrisch](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] metrisch](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### Aangepaste omzettingscijfers

Deze metriek is specifiek voor de rapportreeks, zodat variëren de beschikbare metriek voor elke klant en rapportreeks.

### Aangepaste omzettingsmaatstaven gemaakt op basis van eVars en Props

De beschikbare meetgegevens variëren per klant. Zie &quot;[Conversiemetriek maken van Adobe Analytics Vars en props](/help/integrations/analytics/conversion-metrics-from-evars.md).&quot;

### Gereserveerde omzettingsstatistieken

Deze metriek is specifiek voor de rapportreeks, zodat variëren de beschikbare metriek voor elke klant en rapportreeks.

>[!MORELIKETHIS]
>
>* [Overzicht van [!DNL Analytics for Advertising]](overview.md)
>* [Adoben Advertising in Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
