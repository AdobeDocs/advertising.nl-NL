---
title: '[!UICONTROL Forecast Accuracy (Actuals) Report]'
description: Meer informatie over de [!UICONTROL Forecast Accuracy (Actuals) Report], inclusief de gegevenskolommen.
exl-id: 659e11c7-5fed-4d91-a73f-7c435d36634f
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# De [!UICONTROL Forecast Accuracy (Actuals) Report]

Dit rapport toont de daadwerkelijke indruk, klik, kosten, en opbrengstgegevens van het advertentienetwerk door dag voor elke portefeuille.

## Beschikbare kolommen

Het volgende is de kolommen die automatisch inbegrepen in elk rapport zijn. U kunt geen extra kolommen toevoegen.

| Kolom | Standaard? | Beschrijving |
|----|----|----|
| [!UICONTROL Portfolio Group Name] | Standaard | De naam van de portfoliogroep waartoe het portfolio behoort. |
| [!UICONTROL Portfolio ID] | Standaard | De numerieke portefeuille-id. |
| [!UICONTROL EF Portfolio Group ID] | Standaard | De numerieke id voor de portfoliogroep waartoe het portfolio behoort. |
| [!UICONTROL Portfolio] | Standaard | Het portfolio. |
| [!UICONTROL Portfolio Status] | Standaard | De status van het portfolio:<ul><li><i>[!UICONTROL Optimize]:</i> De optimalisatiecapaciteit is het verzamelen van klik- en inkomstengegevens voor de relevante campagnes, het modelleren van de gegevens om biedingen te optimaliseren, en het optimaliseren van biedingen en/of campagnebegrotingen (afhankelijk van het optimalisatietype en de strategieën voor campagneaanbiedingen).</li><li><i>[!UICONTROL Active]:</i> De optimalisatiecapaciteit verzamelt klikgegevens en inkomstengegevens voor de relevante campagnes en modelleert de gegevens, maar het optimaliseert geen biedingen of campagnebegrotingen.</li><li><i>[!UICONTROL Inactive]:</i> De optimalisatiecapaciteit verzamelt klikgegevens voor de relevante campagnes voor rapporteringsdoeleinden, maar het modelleert de gegevens noch optimaliseert biedingen of campagnebegrotingen. |
| [!UICONTROL Day of Week] | Standaard | De dag van de gerapporteerde week: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i>, of <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Event Date] | Standaard | De gerapporteerde datum. |
| [!UICONTROL Device] | Standaard | (Google Ads, Microsoft Advertising, Yahoo! Het Netwerk van de vertoning, Yahoo! Japan Ads- en Yahoo Native-campagnes) Het apparaattype waarop advertenties werden weergegeven: <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i>, of <i>[!UICONTROL N/A]</i> (geen waarde). Rijen voor andere advertentienetwerken hebben waarden van <i>[!UICONTROL N/A]</i>.<br><br>Als in zoekcampagnes de trackingsjablonen of doel-URL&#39;s voor de trefwoorden, advertenties en/of extensies parameters bevatten om gegevens per apparaat bij te houden (<code>&amp;ev_dvc={device}&amp;ev_dvm={devicemodel}</code>) op het moment dat op de advertentie werd geklikt, worden de conversiegegevens ook in de rij opgenomen voor elk apparaattype. Anders, als de omzettingsgegevens niet aan een apparatentype kunnen worden toegeschreven, wordt het bijeengevoegd in een afzonderlijke rij met &quot;[!UICONTROL Device]&quot; waarde van <i>[!UICONTROL N/A]</i>. |
| [!UICONTROL Revenue] | Standaard | De totale inkomsten. |
| [!UICONTROL Impressions] | Standaard | De totale indrukken. |
| [!UICONTROL Clicks] | Standaard | Het totaal klikt. |
| [!UICONTROL Cost] | Standaard | De totale kosten. |

>[!MORELIKETHIS]
>
>* [Informatie over modelnauwkeurigheidsrapporten](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [De [!UICONTROL Forecast Accuracy Report]](forecast-accuracy-report.md)
>* [Een rapport over de modelnauwkeurigheid genereren](model-accuracy-report-generate.md)
>* [Instellingen van modelnauwkeurigheidsrapporten](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
