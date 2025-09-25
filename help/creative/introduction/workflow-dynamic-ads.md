---
title: Workflows voor dynamische advertenties
description: Leer meer over de workflows voor het beheer van dynamische advertenties.
feature: Creative Dynamic Creatives
source-git-commit: 6f2f6580e8d4fc11f52a97b086ce453e423ab4e6
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Workflows voor dynamische advertenties

*Gebruikers met toestemmingen om dynamische advertenties tot stand te brengen*

U kunt dynamische advertenties op twee manieren instellen:

* Workflow 1: Upload een advertentiesjabloon en voeg een variatiecatalogus rechtstreeks toe binnen de dynamische ad-instellingen wanneer u dynamische advertenties toevoegt aan een creatieve bibliotheek. U kunt een bestaande voedermalplaatje downloaden om de catalogus tot stand te brengen.

  Gebruik deze workflow wanneer dezelfde persoon alle informatie kan opgeven (behalve de voedersjabloon) om de advertenties te maken. De geüploade bestanden blijven beschikbaar voor toekomstig gebruik.

* Workflow 2: stel een advertentiesjabloon in en voeg variatiecatalogi toe in afzonderlijke weergaven, en voeg vervolgens afzonderlijk dynamische advertenties toe aan een creatief bedrijf met behulp van de reeds beschikbare advertentiesjabloon en catalogi.

  Gebruik deze workflow wanneer verschillende personen verschillende taken uitvoeren of wanneer u slechts één taak tegelijk wilt uitvoeren.

## Workflow 1

>[!PREREQUISITES]
>
>* Advertentiesjablonen in HTML5-indeling
>* Productcatalogi in de indeling CSV, TSV of Microsoft Excel-werkblad (XLSX)

1. [ creeer dynamische creatieve creatieve ](/help/creative/creative-libraries/creative-add-dynamic.md) voor een creatieve bibliotheek. Upload voor dynamische HTML5-advertenties een advertentiesjabloon en catalogi.

1. Gebruik de dynamische creatieve elementen voor advertenties:

   1. [ creeer dynamische ad bundels ](/help/creative/creative-libraries/bundle-manage.md) die u allen aan een advertentie kunt in één keer vastmaken.

   1. Creeer dynamische en ervaringen [ met het richten van zich ](/help/creative/experiences/experience-create-targeting.md) of [ zonder ](/help/creative/experiences/experience-create-no-targeting.md) te richten en [ wijs de creatieve bundels aan de ervaringen ](/help/creative/experiences/experience-assign-creative-bundles.md) toe.

   1. [ produceer en voer de markeringen van de advertentiervaring uit ](/help/creative/experiences/experience-tag-export.md) om hen als advertenties in uw DSP in werking te stellen.

      Als u een advertentie wilt gebruiken als advertentie in Adobe Advertising DSP, uploadt u de advertentietag naar een Advertising DSP-campagne. Als u een advertentie wilt gebruiken als advertentie in een andere DSP, implementeert u de advertentietag in die DSP.

## Workflow 2

1. [ creeer een advertentiesjabloon ](/help/creative/ad-templates/ad-template-manage.md) voor uw dynamische advertenties die op de beschikbare activa worden gebaseerd.

1. Stel uw advertentie-elementen in:

   * (Voor enige statische advertenties HTML5) verzamel en [ upload de beeldactiva ](/help/creative/feeds/asset-manage.md) voor uw advertenties.

   * (Voor dynamische HTML5-advertenties) Maak catalogi van uw advertentie-elementen:

      1. Maak een feed-bestand in de indeling Microsoft Excel-werkblad (XLSX) met één rij voor elke advertentievariatie. Neem in elke rij een afbeeldingsnaam of een verwijzing naar een Adobe Experience Manager op. Verzamel de bijbehorende afbeeldingselementen afzonderlijk.

      1. [ uploadt het voederdossier en beeldactiva ](/help/creative/feeds/asset-manage.md).

      1. [ creeer een voedermalplaatje ](/help/creative/feeds/feed-template-manage.md) om de gebieden in uw voederdossier (spreadsheet) aan gebieden in de achtergrond van Advertising Creative in kaart te brengen.

      1. [ creeer een catalogus ](/help/creative/feeds/catalog-manage.md#feed-catalog-create) van een gespecificeerd voederdossier en een gespecificeerd voedermalplaatje, en dan [ proces de catalogus ](/help/creative/feeds/catalog-manage.md#feed-catalog-process) om de ad variaties te zien die van het kunnen worden gecreeerd.

         U kunt elk feed-bestand slechts voor één catalogus gebruiken.

         U kunt [ het statuut van de banen van de catalogusverwerking ](/help/creative/feeds/job-status-track.md) op [!UICONTROL Creative] volgen > [!UICONTROL Feeds] > [!UICONTROL Job Status] tabel.

1. [ creeer dynamische creatieve creatieve ](/help/creative/creative-libraries/creative-add-dynamic.md) voor een creatieve bibliotheek. Gebruik voor dynamische HTML5-advertenties een opgegeven advertentiesjabloon en opgegeven catalogi.

1. Gebruik de dynamische creatieve elementen voor advertenties:

   1. [ creeer dynamische ad bundels ](/help/creative/creative-libraries/bundle-manage.md) die u allen aan een advertentie kunt in één keer vastmaken.

   1. Creeer dynamische en ervaringen [ met het richten van zich ](/help/creative/experiences/experience-create-targeting.md) of [ zonder ](/help/creative/experiences/experience-create-no-targeting.md) te richten en [ wijs de creatieve bundels aan de ervaringen ](/help/creative/experiences/experience-assign-creative-bundles.md) toe.

   1. [ produceer en voer de markeringen van de advertentiervaring uit ](/help/creative/experiences/experience-tag-export.md) om hen als advertenties in uw DSP in werking te stellen.

      Als u een advertentie wilt gebruiken als advertentie in Adobe Advertising DSP, uploadt u de advertentietag naar een Advertising DSP-campagne. Als u een advertentie wilt gebruiken als advertentie in een andere DSP, implementeert u de advertentietag in die DSP.
