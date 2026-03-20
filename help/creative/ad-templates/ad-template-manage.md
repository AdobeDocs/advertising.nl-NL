---
title: Dynamische advertentiesjablonen beheren
description: Leer hoe u dynamische advertentiesjablonen beheert en er advertenties van maakt.
feature: Creative Templates
exl-id: 248f1467-ebd3-47f2-a24c-043bbfadcc6e
source-git-commit: 7945887cf34c5ff390a35f1b9a6ede2888254c65
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---

# Dynamische advertentiesjablonen beheren

Maak een aparte advertentiesjabloon voor elke combinatie van advertentietype (statische HTML5 of dynamische HTML5) en advertentiegrootte door een gecomprimeerd HTML5-bestand met de gewenste advertentievorm te uploaden. Voor dynamische HTML5-advertenties uploadt u ook een bestand met de advertentiekenmerken <!-- more clarification? --> .

<!-- add this where/how?: You can use the same feed template for multiple ad templates. -->

<!-- EXPLAIN MORE:  Is this like repropagating a feed file through a template, or can you just change some things? Is generating an ad template a one-time thing, using the existing feed file, but you might later update the file and re-propagation doesn't happen automatically? Clarify the use cases for each.-->

## Een dynamische advertentiesjabloon maken

>[!NOTE]
>
>U kunt een dynamisch advertentiemalplaatje ook uploaden wanneer u [&#x200B; dynamische creatieve creatieven aan een creatieve bibliotheek &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md) toevoegt. Alle advertentiesjablonen die u daar maakt, worden beschikbaar in de weergave [!UICONTROL Ad Templates] voor toekomstig gebruik.

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]** .

1. Klik rechtsboven op **[!UICONTROL Create Ad Template]**

1. Specificeer [&#x200B; en malplaatjemontages &#x200B;](#ad-template-settings)

1. Klik op **[!UICONTROL Create]**.

## Een dynamische advertentiesjabloon bewerken

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]** .

1. Plaats de cursor op de rij voor de advertentiesjabloon en klik op **[!UICONTROL Edit]** .

1. Bewerk de [&#x200B; montages van het advertentiesjabloon &#x200B;](#ad-template-settings).

1. Klik op **[!UICONTROL Save]**.

## Een dynamische advertentiesjabloon downloaden

<!-- Explain more about what this contains and the format:  Downloaded ad templates are compressed (zipped) files that include XXX as TDF files and the uploaded HTML5 (and attributes?) data. You can open the TDF file in a text editor. -->

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]** .

1. Plaats de cursor op de rij voor de advertentiesjabloon en klik op **[!UICONTROL Download]** .

   Het bestand wordt gedownload volgens de normale procedure van uw browser.

## Een dynamische advertentiesjabloon verwijderen

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]** .

1. Plaats de cursor op de rij voor de advertentiesjabloon en klik op **[!UICONTROL Delete]** .

1. Klik in het bevestigingsbericht op **[!UICONTROL Delete]** .

## Dynamische advertenties maken van een advertentiesjabloon

>[!NOTE]
>
>U kunt dynamische creatieve creatieven aan een creatieve bibliotheek [&#x200B; van binnen een creatieve bibliotheek ook toevoegen.](/help/creative/creative-libraries/creative-add-dynamic.md)

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]** .

1. Plaats de cursor op de rij voor de advertentiesjabloon en klik op **[!UICONTROL Create Dynamic Ad]** .

   In het [!UICONTROL New Dynamic Ad] -scherm worden de velden [!UICONTROL Ad Template Size] , [!UICONTROL Ad Template Type] en [!UICONTROL Ad Template] automatisch geselecteerd en hebben deze het kenmerk Alleen-lezen.

1. Specificeer de dynamische ad montages om [&#x200B; de dynamische advertenties &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md) tot stand te brengen.

## Sjablooninstellingen toevoegen {#ad-template-settings}

### Sjabloondetails toevoegen

**[!UICONTROL Advertiser]**: (Alleen-lezen voor bestaande sjablonen) De adverteerder waarvoor advertenties worden gegenereerd.

**[!UICONTROL Ad Template Name]**: Een unieke naam voor een advertentiesjabloon voor de adverteerder.

**[!UICONTROL Ad Template Type]**: (Read-only voor bestaande malplaatjes) het formaat van het advertentiemalplaatje: *Statische HTML5* of *Dynamische HTML5*.

**[!UICONTROL Ad Template Size]**: (Alleen-lezen voor bestaande sjablonen) De afmetingen van de advertenties die door de sjabloon zijn gemaakt.

**[!UICONTROL Description]**: (Optioneel) Informatie die nuttig is voor iedereen die de advertentiesjabloon gebruikt.

### (Statische HTML5-advertentiesjablonen) Klik op Codes

**\ [klik de Parameter van de Markering \]**: De parameters van de klikmarkering om klik-volgende omleidingen van advertenties toe te staan die gebruikend het advertentiemalplaatje worden gecreeerd. Als u een parameter wilt toevoegen, klikt u op **[!UICONTROL + Add More]** en voert u een extra parameter in. U kunt maximaal vijf parameters opnemen.

### HTML5 zip

Een gecomprimeerd HTML5-bestand met de gewenste advertentievorm. Als u al een bestand hebt geüpload, wordt de bestandsnaam weergegeven.

Zie [&#x200B; HTML5 creatieve specificatie &#x200B;](/help/creative/creative-libraries/html5-creative-specification.md).

Een bestand uploaden:

1. Klik op **[!UICONTROL Upload HTML5 zip]**.

1. Zoek het bestand op uw apparaat of netwerk.

### (Dynamisch HTML5-advertentiesjablonen) Attributenbestand

<!-- EXPLAIN and ad specs below for this file type -->Een bestand dat kenmerken bevat voor de advertentiesjabloon. Als u al een bestand hebt geüpload, wordt de bestandsnaam weergegeven.

Een bestand uploaden:

1. Klik op **[!UICONTROL Upload Attributes File]**.

1. Zoek het bestand op uw apparaat of netwerk.

>[!MORELIKETHIS]
>
>* [&#x200B; Werkstromen voor dynamische advertenties &#x200B;](/help/creative/introduction/workflow-dynamic-ads.md)
>* [&#x200B; beheert activa dossiers &#x200B;](/help/creative/feeds/asset-manage.md)
>* [&#x200B; beheer voedermalplaatjes &#x200B;](/help/creative/feeds/feed-template-manage.md)
>* [&#x200B; beheert catalogi &#x200B;](/help/creative/feeds/catalog-manage.md)
>* [&#x200B; voeg dynamische creatieve creatieve bibliotheek &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md) toe
