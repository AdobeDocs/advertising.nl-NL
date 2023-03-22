---
title: Adobe Advertising Metrics in Analysis Workspace
description: Adobe Advertising Metrics in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: 5dd3772de945660e76321dac935de5ebcab5979a
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Adobe Advertising Metrics in Analysis Workspace

*Adverteerders met een Adobe Advertising-Adobe Analytics Integration Only*

>[!NOTE]
>
>* Adobe Adverteren geeft verkeersmaatstaven en -afmetingen door aan [!DNL Analytics] dagelijks.
>* [!DNL Analytics] Hiermee legt u doorklikbewerkingen voor Adobe-advertenties en doorzoekingen in real-time vast.
   > Voor [!DNL Search, Social, & Commerce], wordt deze functie ondersteund voor de meeste advertentienetwerken en campagneretypen. Zie &quot;Ondersteunde voorraad&quot; in het dialoogvenster [!DNL Search, Social, & Commerce] Voor meer informatie.<!-- add link when that's published in ExL -->


## Verkeersmetriek van Adobe-reclame

>[!NOTE]
>
>Alle Adobe Advertising Traffic Metrics in [!DNL Analytics] beginnen met &quot;AMO.&quot;

| Verkeersmetrisch | Beschrijving |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Het aantal Adobe-advertenties. |
| [!UICONTROL AMO Clicks] | Het aantal geklikte Adobe-advertenties. |
| [!UICONTROL AMO Cost] | De Adobe-advertentie wordt uitgegeven in de valuta van de rapportsuite. |
| [!UICONTROL AMO ID Instance] | Het aantal keren dat de Adobe-advertentie-id is ingesteld. |
| [!UICONTROL AMO Minutes Viewed] | Het aantal minuten dat een Adobe-advertentievideo is weergegeven. |
| [!UICONTROL AMO Views] | Het aantal weergaven op een advertentie. Een weergave wordt geteld wanneer de viewer de Adobe-advertentievideo start. |
| [!UICONTROL AMO Views 25% Complete] | Het aantal weergaven waarvoor ten minste 25% van een Adobe-advertentievideo werd bekeken. |
| [!UICONTROL AMO Views 50% Complete] | Het aantal weergaven waarvoor ten minste 50% van een Adobe-advertentievideo is bekeken. |
| [!UICONTROL AMO Views 75% Complete] | Het aantal weergaven waarvoor ten minste 75% van een Adobe-advertentievideo werd bekeken. |
| [!UICONTROL AMO Views 100% Complete] | Het aantal weergaven waarvoor 100% van een Adobe-advertentievideo werd bekeken. |
| [!UICONTROL AMO Viewable Impressions] | Het aantal indrukkingen dat is gemeten om te kunnen worden weergegeven volgens de plaatsingsconfiguratie. |
| [!UICONTROL AMO Not Viewable Impressions] | Het aantal indrukkingen waarvan is vastgesteld dat ze niet kunnen worden weergegeven. Deze waarde wordt berekend als ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable]). |
| [!UICONTROL AMO Measurable Impressions] | Het aantal indrukkingen waarvoor de viewability instrumentatie met succes werd geïnitialiseerd. Deze waarde wordt berekend als (geïndexeerde indrukken - het aantal niet-meetbare indrukken). |

## Adobe Advertentie-Dimension

>[!NOTE]
>
>Alle Adobe-advertentiedimensies in [!DNL Analytics] worden gevolgd door &quot;(AMO-id)&quot;.

| Dimension | Toepasselijke Adobe-advertentiegegevens | Beschrijving |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | Reclame-DSP of naam van de zoekmachine |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | De accountnaam. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | RTB ([!DNL DSP]) of de naam van het advertentienetwerk ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | De naam van de campagne. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | Het pakket ([!DNL DSP]) of portfolio ([!DNL Search, Social, & Commerce]) name. |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | De plaatsingsnaam. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] data | De naam van de advertentiegroep. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] data | Het trefwoord. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | Het type zoekovereenkomst. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] data | Het trefwoord en het overeenkomende type. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | Het advertentietype, zoals `text`, `video`, `display`, of `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | Het advertentietype ([!DNL DSP]) of een advertentitel ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | De advertentiebeschrijving ([!DNL DSP]) of ad body ([!DNL Search, Social, & Commerce]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | De URL die wordt weergegeven in de advertentie. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] data | De doel-URL voor de advertentie. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] en [!DNL Search, Social, & Commerce] data | Hiermee wordt aangegeven of het item van de openingspagina een doorkijkeffect of een doorklikeffect heeft. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] data | Het productdoel voor een advertentie voor een productaanbieding. |

## Nuttige aangepaste berekende cijfers voor Adobe-advertenties

Overweeg de volgende meetgegevens voor uw Adobe-advertentiegegevens te maken.

* Klikt op instantie Landing Page ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]): Dit is het percentage mensen dat op de advertentie klikte en deze naar de landingspagina maakte.
* Meetbare snelheid ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Weergavegraad van de depressie ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Kosten per weergave ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Kosten per klik ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

>[!MORELIKETHIS]
>
>* [Overzicht van [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Gegevens in Adobe-reclame](/help/integrations/analytics/analytics-data-in-advertising.md)

