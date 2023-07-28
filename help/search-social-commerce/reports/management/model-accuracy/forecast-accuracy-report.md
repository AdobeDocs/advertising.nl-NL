---
title: '[!UICONTROL Forecast Accuracy Report]'
description: Leer over het Rapport van de Nauwkeurigheid van de Vooruitzichten, met inbegrip van de gegevenskolommen.
exl-id: 2bb36728-ae14-441b-bcda-fa457f5cf664
feature: Search Reports, Search Model Accuracy Reports
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# De [!UICONTROL Forecast Accuracy Report]

Het rapport toont de nauwkeurigheid van de kosten- en inkomstenmodellen per dag voor gespecificeerde portefeuilles. De standaard omvat de dagelijks voorspelde en werkelijke inkomsten, kosten en klikfuncties — en de nauwkeurigheid van de prognoses — voor elke portefeuille. Het omvat gegevens van campagnes die momenteel aan de portefeuilles in kaart worden gebracht.

U kunt gegevens van de vorige 18 maanden bekijken.

>[!NOTE]
>
>* Dit rapport bevat dezelfde gegevens als het portfolioniveau [!UICONTROL Model Accuracy Report] behalve dat u het over veelvoudige portefeuilles kunt in werking stellen en u kunt de attributieregel veranderen. U kunt het rapport ook in werking stellen en plannen gebruikend douaneparameters, en u kunt het gebruiken om spreadsheetvoer tot stand te brengen.
>
>* De beste manier is om de [!UICONTROL Forecast Accuracy Report] gedurende ten minste de laatste zeven dagen omdat, ongeacht de uitgavenstrategie van de portefeuille, de meeste portefeuilles een inherente trend van de dag van de week zien. De optimalisatiecapaciteit houdt rekening met deze trend en wijst de uitgaven dienovereenkomstig toe.
>
>* Voor kostenramingen wordt een afwijking van 10% in de laatste zeven dagen aanvaardbaar geacht, zodat de feitelijke uitgaven die tussen 90% en 110% van de geraamde uitgaven liggen, fijn zijn. Voor inkomstenprognoses wordt een afwijking van 15% in de laatste zeven dagen aanvaardbaar geacht, zodat de werkelijke inkomsten die tussen 85% en 115% van de geraamde uitgaven liggen, een boete zijn. Prognoses met hogere afwijkingen moeten worden onderzocht.
>
>* Wanneer trefwoorden in de portefeuille gekoppeld zijn aan beperkingen in verband met verschuiving van het bod, wordt de portefeuille hoger of lager uitgegeven dan het totale bedrag dat door de verschuiving van het bod wordt veroorzaakt. Dientengevolge, wijken de voorspelde kostenkolommen van de doeluitgave door de verhoogde of verminderde uitgave af.

## Beschikbare kolommen

Het volgende is de kolommen die voor elk rapport beschikbaar zijn. De standaardkolommen worden standaard automatisch opgenomen. U kunt de beschikbare aangepaste kolommen toevoegen uit de [!UICONTROL Columns] van de rapportinstellingen.

| Kolom | Standaard? | Beschrijving |
|----|----|----|
| [!UICONTROL Portfolio] | Standaard | Het portfolio. |
| [!UICONTROL Day of Week] | Standaard | De dag van de gerapporteerde week: <i>[!UICONTROL Sunday]</i>, <i>[!UICONTROL Monday]</i>, <i>[!UICONTROL Tuesday]</i>, <i>[!UICONTROL Wednesday]</i>, <i>[!UICONTROL Thursday]</i>, <i>[!UICONTROL Friday]</i>, of <i>[!UICONTROL Saturday]</i>. |
| [!UICONTROL Start Date] | Standaard | De eerste dag die werd gerapporteerd. |
| [!UICONTROL End Date] | Standaard | De laatste dag die is gemeld. |
| [!UICONTROL Predicted Revenue] | Standaard | De voorspelde opbrengsten voor de portefeuille. |
| [!UICONTROL Revenue] | Standaard | De werkelijke opbrengsten van de portefeuille. |
| [!UICONTROL Revenue Accuracy] | Standaard | De juistheid van de geraamde ontvangsten, uitgedrukt als een percentage. |
| [!UICONTROL Predicted Cost] | Standaard | De voorspelde kosten voor de portefeuille. |
| [!UICONTROL Cost] | Standaard | De werkelijke kosten voor de portefeuille. |
| [!UICONTROL Cost Accuracy] | Standaard | De nauwkeurigheid van de kostenprognose, uitgedrukt als een percentage. |
| [!UICONTROL Predicted Clicks] | Standaard | Het aantal voorspelde klikken voor de portfolio. |
| [!UICONTROL Clicks] | Standaard | Het werkelijke aantal klikken voor het portfolio. |
| [!UICONTROL Click Accuracy] | Standaard | De nauwkeurigheid van de klikvoorspelling, uitgedrukt als een percentage. |
| [!UICONTROL EF Portfolio Group ID] | Standaard | De numerieke id voor de portfoliogroep waartoe het portfolio behoort. |
| [!UICONTROL Portfolio Group Name] | Standaard | De naam van de portfoliogroep waartoe het portfolio behoort. |
| [!UICONTROL Portfolio ID] | Standaard | De numerieke portefeuille-id. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Informatie over modelnauwkeurigheidsrapporten](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-about.md)
>* [De [!UICONTROL Forecast Accuracy (Actuals) Report]](forecast-accuracy-actuals-report.md)
>* [Een rapport over de modelnauwkeurigheid genereren](model-accuracy-report-generate.md)
>* [Instellingen van modelnauwkeurigheidsrapporten](/help/search-social-commerce/reports/management/model-accuracy/model-accuracy-report-settings.md)
