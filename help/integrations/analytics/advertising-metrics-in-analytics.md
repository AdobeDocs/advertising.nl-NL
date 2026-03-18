---
title: Adobe Advertising-cijfers in Analysis Workspace
description: Adobe Advertising-cijfers in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: 94a5b5591aef0aa5ae5d3459d547f52d939d559c
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# Adobe Advertising-cijfers in Analysis Workspace

*Advertisers met slechts een integratie Adobe Advertising-Adobe Analytics*

>[!NOTE]
>
>* Adobe Advertising geeft verkeersmaatstaven en -afmetingen door aan [!DNL Analytics] per dag.
>* Met [!DNL Analytics] worden doorklikbewerkingen en doorzoekacties van Adobe Advertising in real-time vastgelegd.
>* Voor [!DNL Search, Social, & Commerce] wordt deze functie ondersteund voor de meeste advertentienetwerken en campagneretypen. Zie &quot;[&#x200B; Gesteunde Inventaris &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)&quot;in de [!DNL Search, Social, & Commerce] Gids voor meer informatie.

## Verkeersmetriek van Adobe Advertising

Adobe Advertising-verkeersmaatstaven in [!DNL Analytics] beginnen gewoonlijk met &quot;Adobe Advertising&quot;, behalve &quot;[!UICONTROL AMO ID Instances]&quot;. Voor klanten op lange termijn die een aangepaste gebeurtenis (in plaats van een gereserveerde gebeurtenis) gebruikten om metriek voor kliks, kosten, en beelden oorspronkelijk tot stand te brengen, beginnen die metriek nog met &quot;AMO.&quot;

| Verkeersmeter | Beschrijving |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] of (sommige verouderde klanten) [!UICONTROL AMO Clicks] | Het aantal totale kliks van Adobe Advertising. |
| [!UICONTROL Adobe Advertising Cost] of (sommige verouderde klanten) [!UICONTROL AMO Cost] | De Adobe Advertising besteedt geld in de valuta van de rapportensuite. |
| [!UICONTROL Adobe Advertising Impressions] of (sommige verouderde klanten) [!UICONTROL AMO Impressions] | Het aantal Adobe Advertising-afbeeldingen. |
| [!UICONTROL Adobe Advertising Measurable Impressions] | Het aantal indrukkingen waarvoor de viewability instrumentatie met succes werd geïnitialiseerd. Deze waarde wordt berekend als (geïndexeerde indrukken - het aantal niet-meetbare indrukken). |
| [!UICONTROL Adobe Advertising Minutes Viewed] | Het aantal minuten dat een Adobe Advertising-video is bekeken. |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | Het aantal indrukkingen waarvan is vastgesteld dat ze niet kunnen worden weergegeven. Deze waarde wordt berekend als ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]). |
| [!UICONTROL Adobe Advertising Viewable Impressions] | Het aantal indrukkingen dat is gemeten om te kunnen worden weergegeven volgens de plaatsingsconfiguratie. |
| [!UICONTROL Adobe Advertising Views] | Het aantal weergaven op een advertentie. Een weergave wordt geteld wanneer de viewer de Adobe Advertising-video start. |
| [!UICONTROL Adobe Advertising Views 25% Complete] | Het aantal weergaven waarvoor ten minste 25% van een Adobe Advertising-video is bekeken. |
| [!UICONTROL Adobe Advertising Views 50% Complete] | Het aantal weergaven waarvoor ten minste 50% van een Adobe Advertising-video is bekeken. |
| [!UICONTROL Adobe Advertising Views 75% Complete] | Het aantal weergaven waarvoor ten minste 75% van een Adobe Advertising-video is bekeken. |
| [!UICONTROL Adobe Advertising Views 100% Complete] | Het aantal weergaven waarvoor 100% van een Adobe Advertising-video is bekeken. |
| [!UICONTROL AMO ID Instances] | Het aantal keren dat de [!UICONTROL AMO ID] is ingesteld. |

## Adobe Advertising-afmetingen

>[!NOTE]
>
>Alle Adobe Advertising-afmetingen in [!DNL Analytics] worden gevolgd door &quot;[!DNL (AMO ID)]&quot;.

| Dimension | Toepasselijke Adobe Advertising-gegevens | Beschrijving |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | Advertising DSP of de naam van de zoekmachine |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | De accountnaam. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | RTB ([!DNL DSP]) of de naam van het advertentienetwerk ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | De naam van de campagne. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | The package ([!DNL DSP]) or portfolio ([!DNL Search, Social, & Commerce]) name. |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] gegevens | De plaatsingsnaam. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] gegevens | De naam van de advertentiegroep. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] gegevens | Het trefwoord. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] gegevens | Het type zoekovereenkomst. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] gegevens | Het trefwoord en het overeenkomende type. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | Het advertentietype, zoals `text` , `video` , `display` of `native` . |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | Het advertentietype ([!DNL DSP]) of advertentietype ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | De beschrijving van de advertentie ([!DNL DSP]) of advertentie ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] gegevens | De URL die wordt weergegeven in de advertentie. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] gegevens | De doel-URL voor de advertentie. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | Hiermee wordt aangegeven of het item van de openingspagina een doorkijkeffect of een doorklikeffect heeft. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] gegevens | Het productdoel voor een advertentie voor een productaanbieding. |

## Nuttige aangepaste berekende maatstaven voor Adobe Advertising

U kunt de volgende maatstaven voor uw Adobe Advertising-gegevens maken.

* Klik op Landing Page Instance ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks] ): Dit is het percentage personen dat op de advertentie heeft geklikt en deze op de bestemmingspagina heeft geplaatst.
* Meetbare snelheid ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* Weergavesnelheid ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* Kosten per weergave ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views])
* Kosten per klik ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [&#x200B; Overzicht van  [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics]  Gegevens in Adobe Advertising &#x200B;](/help/integrations/analytics/analytics-data-in-advertising.md)
