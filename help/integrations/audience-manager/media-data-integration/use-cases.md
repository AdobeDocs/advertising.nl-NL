---
title: Gevallen gebruiken
description: Meer informatie over gebruiksgevallen voor het delen van Advertising DSP-mediagegevens met Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# Gebruik gevallen voor het vastleggen van gegevens over mediablootstelling in Adobe Audience Manager

*Advertisers met slechts Advertising DSP*

*Advertisers met slechts een integratie Adobe Advertising-Adobe Audience Manager*

Hieronder vindt u een aantal manieren waarop u kunt profiteren van het vastleggen van belichtingsgegevens voor Advertising DSP-media <!-- ad impression data? --> in Audience Manager.

## Recente- en frequentiebeheer

Door impliciete gegevens vast te leggen in Audience Manager kunt u uw frequentiebeheer verbeteren door segmenten van gebruikers te maken die zijn blootgesteld aan een bepaalde advertentie of campagne. U kunt deze segmenten gebruiken voor het opgeven van doelen als u de frequentie wilt verhogen of voor het onderdrukken van advertenties als u de frequentie wilt beperken.

Ook, met Audience Manager [!DNL Segment Builder], kunt u [ recency en frequentiecontroles ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) op om het even welke [ regel-gebaseerde tretten ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) toepassen die actionable signalen bevatten. Zo kunt u bijvoorbeeld het aantal keren beperken dat een gebruiker een bepaalde creatieve vertoning weergeeft in een mediacampagne. Lees &quot;[ Onmiddellijke Onderdrukking van het dwars-Apparaat ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)&quot;om te leren hoe te om dit te doen.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Sequentiële berichten

Door het vangen van beeldgegevens, kunt u een segment van gebruikers tot stand brengen die aan een campagne of een advertentie zijn blootgesteld en dit segment voor opeenvolgend overseinen of onderdrukking gebruiken. U kunt bijvoorbeeld gebruikers die creatieve `123` tekeningen hebben gemaakt maar niet hebben geklikt of omgezet, opnieuw als doel instellen door ze creatief weer te geven `456` .

Om dit voorbeeld in Audience Manager uit te voeren, zou u deze stappen volgen:<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Maak een eigenschap om gebruikers vast te leggen die de creatieve foto&#39;s hebben gezien.

   Als u bijvoorbeeld de eigenschap `Creative Trait 123` een naam wilt geven, gebruikt u de volgende regel:

   ```
   d_creative == 123 AND d_event == imp
   ```

1. Maak een eigenschap om gebruikers vast te leggen die klikken of converteren.

   Als u deze eigenschap bijvoorbeeld wilt benoemen `Click and Converter` , gebruikt u de volgende regel:

   ```
   d_event == click OR d_event=conv
   ```

1. Maak een segment met de naam `Retarget Users` om te vullen met gebruikers die creatief `123` hebben gezien, maar niet hebben geklikt of geconverteerd. Gebruik de volgende gedragslijn:

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. Wijs het segment `Retarget Users` toe aan een doel en wijs gebruikers in de bestemming met creatief `456` aan.

## [!DNL Adobe Audience Analytics] en gegevens over campagnebelichting

Zodra de campagneindruk en de klikgegevens binnen Audience Manager beschikbaar zijn, kunt u eigenschappen en segmenten van gebruikers tot stand brengen die aan, of interactie met, een bepaalde campagne of een tactiek werden blootgesteld. Met een [[!DNL Audience Analytics]  integratie ](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html), kunnen uw segmenten van Audience Manager met [!DNL Analytics] voor verdere analyse worden gesynchroniseerd. Mogelijke gevallen van gebruik zijn onder meer:

* **analyse van de Interactie tussen DSP en [!DNL Advertising Search, Social, & Commerce] advertenties:** de standaard [[!DNL Analytics for Advertising]  integratie ](/help/integrations/analytics/overview.md) verstrekt geen inzichten in de interactie tussen DSP en [!DNL Search, Social, & Commerce] omdat beide kanalen AMO IDs gebruiken die AMO ID attributieregels volgen, waarvoor een onderzoek klikt een vertoning mening-door met voeten treedt. Als u een DSP-belichtingssegment maakt in Audience Manager, kunt u met [!DNL Audience Analytics] de interactie tussen DSP en [!DNL Search, Social, & Commerce] advertenties in [!DNL Analytics] analyseren.

* **analyse van de Frequentie:** u kunt segmenten in Audience Manager tot stand brengen die op hoeveel tijden een gebruiker aan een bepaalde advertentie of een campagne werd blootgesteld. Vervolgens kunt u de verschillende belichtingssegmenten in Analytics analyseren om te zien hoe het gedrag van de gebruiker verandert afhankelijk van het aantal DSP-blootstellingen.

## [!DNL Audience Optimization Reports]

U kunt hefboomwerking [ Audience Manager  [!DNL Audience Optimization Reports] ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) gebruiken om potentiële prestatiemogelijkheden voor segmenten over uw campagnes te identificeren. Deze rapporten combineren campagneindruk, klik, en omzettingsgegevens met segmentmetriek om segment-centric optimalisaties en een efficiënte kanaalmengeling te informeren.

### Typen relevante Audience Optimization-rapporten

| Rapport | Beschrijving |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Rapport ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | Vergelijkt in kaart gebrachte en unmapped segmenten door beelden en omzettingspercentages. |
| [[!UICONTROL Trend Analysis and Volume Analysis] Rapporten]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Retourneer gegevens over afbeeldingen, doorkliksnelheden en conversies voor een groot aantal verschillende advertentiemetingen. |
| [[!UICONTROL Optimal Frequency] Rapport ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | Helpt u de optimale balans tussen het aantal gediende indrukkingen en omzettingen te ontdekken. Zo kunt u het aantal afbeeldingen dat wordt weergegeven aanpassen voordat u dalende resultaten ziet. |
| [[!UICONTROL Unique User Reach] Rapport ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | Een bubbelgrafiek, waarin elke bel in direct verhouding aan het aantal unieke gebruikers voor uw geselecteerde afmeting wordt gerangschikt. |

### Overwegingen

* Als [!DNL Audience Optimization Reports] -gebruikers toegangsbeheer op basis van rollen (RBAC) hebben, moet [!DNL Adobe Customer Care] een toewijzing configureren tussen de Advertiser-id en de Audience Manager-code voor gegevensbronintegratie van de organisatie. Beheerders kunnen vervolgens RBAC-rechten aan verschillende gebruikers verstrekken.

* Voor conversierapportage in [!DNL Audience Optimization Reports] moet de eindgebruiker iets instellen. Gebruikers moeten metagegevensbestanden invullen.

* [!DNL Audience Optimization Reports] biedt geen ondersteuning voor wijzigingen in campagnemetagegevens (zoals naam van de campagne of naam van de plaatsing).

* Klik op zoekadvertenties worden alleen in [!DNL Audience Optimization Reports] opgenomen als deze gecorreleerd zijn met afbeeldingen. Met andere woorden, zoekklikken worden na indrukken beschouwd als omzettingen. Als gevolg hiervan worden veel zoekklikken mogelijk niet opgenomen in [!DNL Audience Optimization Reports] .

>[!MORELIKETHIS]
>
>* [ Overzicht van het verzenden van de media van DSP blootstellingsgegevens naar Adobe Audience Manager ](overview.md)
>* [ verzamel klik en indruk gegevens van de campagnes van Advertising DSP ](collect.md)
