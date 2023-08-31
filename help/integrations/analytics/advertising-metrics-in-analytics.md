---
title: Adoben Advertising in Analysis Workspace
description: Adoben Advertising in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: da69280679a4e0c5ce04f55ee94ce984745395ff
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Adoben Advertising in Analysis Workspace

*Adverteerders met alleen Adobe Advertising-Adobe Analytics-integratie*

>[!NOTE]
>
>* Adobe Advertising gaat verkeersmetriek en dimensies tot over [!DNL Analytics] dagelijks.
>* [!DNL Analytics] vangt Adobe Advertising klikdoorhalingen en mening-doorvoer in echt - tijd.
>* Voor [!DNL Search, Social, & Commerce], wordt deze functie ondersteund voor de meeste advertentienetwerken en campagneretypen. Zie &quot;[Ondersteunde voorraad](/help/search-social-commerce/introduction/supported-inventory.md)&quot; in de [!DNL Search, Social, & Commerce] Voor meer informatie.

## Verkeersmetriek van Adobe Advertising

Adobe Advertising verkeersmetriek in [!DNL Analytics] begint gewoonlijk met &quot;Adobe Advertising&quot;, behalve &quot;[!UICONTROL AMO ID Instances].&quot; Voor klanten op lange termijn die een aangepaste gebeurtenis (in plaats van een gereserveerde gebeurtenis) gebruikten om metriek voor kliks, kosten, en beelden oorspronkelijk tot stand te brengen, beginnen die metriek nog met &quot;AMO.&quot;

| Verkeersmeter | Beschrijving |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] of (sommige verouderde klanten) [!UICONTROL AMO Clicks] | Het aantal klikken van de totale Adobe Advertising. |
| [!UICONTROL Adobe Advertising Cost] of (sommige verouderde klanten) [!UICONTROL AMO Cost] | De Adobe Advertising besteedt in de valuta van de rapportenreeks. |
| [!UICONTROL Adobe Advertising Impressions] of (sommige verouderde klanten) [!UICONTROL AMO Impressions] | Het aantal Adobe Advertising-impressies. |
| [!UICONTROL Adobe Advertising Measurable Impressions] | Het aantal indrukkingen waarvoor de viewability instrumentatie met succes werd geïnitialiseerd. Deze waarde wordt berekend als (geïndexeerde indrukken - het aantal niet-meetbare indrukken). |
| [!UICONTROL Adobe Advertising Minutes Viewed] | Het aantal minuten dat een video van de Adobe Advertising is bekeken. |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | Het aantal indrukkingen waarvan is vastgesteld dat ze niet kunnen worden weergegeven. Deze waarde wordt berekend als ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]). |
| [!UICONTROL Adobe Advertising Viewable Impressions] | Het aantal indrukkingen dat is gemeten om te kunnen worden weergegeven volgens de plaatsingsconfiguratie. |
| [!UICONTROL Adobe Advertising Views] | Het aantal weergaven op een advertentie. Een weergave wordt geteld wanneer de viewer de Adobe Advertising-video start. |
| [!UICONTROL Adobe Advertising Views 25% Complete] | Het aantal weergaven waarvoor ten minste 25% van een Adobe Advertising video is bekeken. |
| [!UICONTROL Adobe Advertising Views 50% Complete] | Het aantal weergaven waarvoor ten minste 50% van een Adobe Advertising video is bekeken. |
| [!UICONTROL Adobe Advertising Views 75% Complete] | Het aantal weergaven waarvoor ten minste 75% van een Adobe Advertising video is bekeken. |
| [!UICONTROL Adobe Advertising Views 100% Complete] | Het aantal weergaven waarvoor 100% van een Adobe Advertising video is bekeken. |
| [!UICONTROL AMO ID Instances] | Het aantal keren dat de [!UICONTROL AMO ID] is ingesteld. |

## Dimensionen Adobe Advertising

>[!NOTE]
>
>Alle afmetingen van de Adobe Advertising in [!DNL Analytics] worden gevolgd door &quot;[!DNL (AMO ID)].&quot;

| Dimension | Toepasselijke Adobe Advertising | Beschrijving |
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

## Nuttige aangepaste berekende cijfers voor Adobe Advertising

U kunt de volgende meetgegevens voor de Adobe Advertising maken.

* Klikt op instantie van bestemmingspagina ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks]): Dit is het percentage mensen dat op de advertentie heeft geklikt en deze op de landingspagina heeft gezet.
* Meetbare snelheid ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* Weergavegraad van de depressie ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* Kosten per weergave ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views])
* Kosten per klik ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [Overzicht van [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Gegevens in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
