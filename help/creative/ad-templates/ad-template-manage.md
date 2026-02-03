---
title: Dynamische advertentiesjablonen beheren
description: Leer hoe u dynamische advertentiesjablonen beheert en er advertenties van maakt.
feature: Creative Templates
source-git-commit: 9c7f3d2aec0952b38d2fd3097d0b3499d33bf3b8
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# Dynamische advertentiesjablonen beheren

Maak een aparte advertentiesjabloon voor elke combinatie van advertentietype (statische HTML5 of dynamische HTML5) en advertentiegrootte door een gecomprimeerd HTML5-bestand met de gewenste advertentievorm te uploaden. Voor dynamische HTML5-advertenties uploadt u ook een bestand met de advertentiekenmerken <!-- more clarification? --> .

<!-- add this where/how?: You can use the same feed template for multiple ad templates. -->

<!-- EXPLAIN MORE:  Is this like repropagating a feed file through a template, or can you just change some things? Is generating an ad template a one-time thing, using the existing feed file, but you might later update the file and re-propagation doesn't happen automatically? Clarify the use cases for each.-->

## Een dynamische advertentiesjabloon maken

>[!NOTE]
>
>U kunt een dynamisch advertentiemalplaatje ook uploaden wanneer u [ dynamische creatieve creatieven aan een creatieve bibliotheek ](/help/creative/creative-libraries/creative-add-dynamic.md) toevoegt. Alle advertentiesjablonen die u daar maakt, worden beschikbaar in de weergave [!UICONTROL Ad Templates] voor toekomstig gebruik.

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]** .

1. Klik rechtsboven op **[!UICONTROL Create Ad Template]**

1. Specificeer [ en malplaatjemontages ](#ad-template-settings)

1. Klik op **[!UICONTROL Create]**.

## Een dynamische advertentiesjabloon bewerken

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]** .

1. Plaats de cursor op de rij voor de advertentiesjabloon en klik op **[!UICONTROL Edit]** .

1. Bewerk de [ montages van het advertentiesjabloon ](#ad-template-settings).

1. Klik op **[!UICONTROL Save]**.

## Een dynamische advertentiesjabloon downloaden

<!-- Explain more about what this contains and the format:  Downloaded ad templates are compressed (zipped) files that include XXX as TDF files and the uploaded HTML5 (and attributes?) data. You can open the TDF file in a text editor. -->

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]** .

1. Plaats de cursor op de rij voor de advertentiesjabloon en klik op **[!UICONTROL Download]** .

   Het bestand wordt gedownload volgens de normale procedure van uw browser.

## Een dynamische advertentiesjabloon verwijderen

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]** .

1. Plaats de cursor op de rij voor de advertentiesjabloon en klik op **[!UICONTROL Delete]** .

1. Klik in het bevestigingsbericht op **[!UICONTROL Delete]** . <!-- Confirm -->

## Dynamische advertenties maken van een advertentiesjabloon

>[!NOTE]
>
>U kunt dynamische creatieve creatieven aan een creatieve bibliotheek [ van binnen een creatieve bibliotheek ook toevoegen.](/help/creative/creative-libraries/creative-add-dynamic.md)

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]** .

1. Plaats de cursor op de rij voor de advertentiesjabloon en klik op **[!UICONTROL Create Dynamic Ad]** .

   In het [!UICONTROL New Dynamic Ad] -scherm worden de velden [!UICONTROL Ad Template Size] , [!UICONTROL Ad Template Type] en [!UICONTROL Ad Template] automatisch geselecteerd en hebben deze het kenmerk Alleen-lezen.

1. Specificeer de dynamische ad montages om [ de dynamische advertenties ](/help/creative/creative-libraries/creative-add-dynamic.md) tot stand te brengen.

## Sjablooninstellingen toevoegen {#ad-template-settings}

### Sjabloondetails toevoegen

**[!UICONTROL Advertiser]**: (Alleen-lezen voor bestaande sjablonen) De adverteerder waarvoor advertenties worden gegenereerd.

**[!UICONTROL Ad Template Name]**: Een unieke naam voor een advertentiesjabloon voor de adverteerder.

**[!UICONTROL Ad Template Type]**: (Read-only voor bestaande malplaatjes) het formaat van het advertentiemalplaatje: *Statische HTML5* of *Dynamische HTML5*.

**[!UICONTROL Ad Template Size]**: (Alleen-lezen voor bestaande sjablonen) De afmetingen van de advertenties die door de sjabloon zijn gemaakt.

**[!UICONTROL Description]**: (Optioneel) Informatie die nuttig is voor iedereen die de advertentiesjabloon gebruikt.

<!-- I don't see this on 9/24:

### (Static HTML5 ad templates) Click Tags

**\[Click Tag Parameter\]**: The click tag parameters to allow click-tracking redirects from ads created using the ad template. To add a parameter, click **[!UICONTROL + Add More]** and enter an additional parameter. You can include up to five parameters.

-->

### HTML5 zip

Een gecomprimeerd HTML5-bestand met de gewenste advertentievorm. Als u al een bestand hebt geüpload, wordt de bestandsnaam weergegeven.

Zie [ HTML5 creatieve specificatie ](/help/creative/creative-libraries/html5-creative-specification.md).

Een bestand uploaden:

1. Klik op **[!UICONTROL Upload HTML5 zip]**.

1. Zoek het bestand op uw apparaat of netwerk.

### (Dynamisch HTML5-advertentiesjablonen) Attributenbestand

<!-- EXPLAIN -->Een bestand dat kenmerken bevat voor de advertentiesjabloon. Als u al een bestand hebt geüpload, wordt de bestandsnaam weergegeven.

<!-- Add specs for this file type -->

Een bestand uploaden:

1. Klik op **[!UICONTROL Upload Attributes File]**.

1. Zoek het bestand op uw apparaat of netwerk.

>[!MORELIKETHIS]
>
>* [ Werkstromen voor dynamische advertenties ](/help/creative/introduction/workflow-dynamic-ads.md)
>* [ beheert activa dossiers ](/help/creative/feeds/asset-manage.md)
>* [ beheer voedermalplaatjes ](/help/creative/feeds/feed-template-manage.md)
>* [ beheert catalogi ](/help/creative/feeds/catalog-manage.md)
>* [ voeg dynamische creatieve creatieve bibliotheek ](/help/creative/creative-libraries/creative-add-dynamic.md) toe

