---
title: Elementbestanden beheren
description: Leer hoe u het elementbestand voor een adverteerder kunt uploaden en beheren.
feature: Creative Dynamic Creatives
source-git-commit: 0d7a7ab23173a061961c4b5c66ace5b69a746e86
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Elementbestanden beheren

Dynamische HTML5-advertenties vereisen zowel een feed-bestand in de indeling Microsoft Excel-spreadsheet (XLSX) als de afbeeldingselementen waarnaar in het spreadsheet wordt verwezen (behalve Adobe Experience Manager-elementverwijzingen). Voor statische HTML5-advertenties is slechts één afbeeldingselement per advertentie vereist.


>[!NOTE]
>
> U kunt elk feed-bestand slechts voor één catalogus gebruiken.

## Bestandsvereisten

* Dynamische HTML5-advertenties:

   * Een feed-bestand in de indeling CSV, TSV of Microsoft Excel-spreadsheet (XLSX), met één koptekstrij en één gegevensrij voor elke advertentievariatie. Neem in elke rij een afbeeldingsnaam op in de indeling `images/image_name` (bijvoorbeeld `images/300x250_acme_logo.png` ).

     De adverteerder-specifieke gebiedsnamen moeten aan de [ beschikbare gebieden voor dynamische ad voederdossiers ](/help/creative/appendix-available-feed-fields.md) in kaart brengen.

   * De bijbehorende afbeeldingselementen in de indeling GIF, JPEG, JPG of PNG.<!-- Is this true: The maximum file size is two (2) MB. --> zie [ gesteunde creatieve grootte ](/help/creative/creative-libraries/creative-sizes.md).

   * (Optioneel) Video-elementen in MP4- of WEBM-indeling

  U kunt één enkel XLSX dossier, één enkel beeld of videodossier, of één enkel dossier uploaden van het PIT dat om het even welke combinatie XLSX, beeld, en videodossiers bevat.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Statische HTML5-advertenties:

   * Eén afbeeldingselement per advertentie in GIF-, JPG-, JPEG- of PNG-indeling.

     U kunt één afbeelding of meerdere afbeeldingen uploaden in een ZIP-bestand.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

## Een elementbestand uploaden

>[!NOTE]
>
>In plaats van het uploaden van activadossiers, kunt u een catalogus ook direct uploaden wanneer u [ dynamische creatieve creatieve bibliotheek ](/help/creative/creative-libraries/creative-add-dynamic.md) toevoegt. Alle catalogi die u daar maakt, worden beschikbaar in de [!UICONTROL Catalogs] -weergave voor toekomstig gebruik.

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** .

1. Klik op de tab **[!UICONTROL Assets]** .

1. Klik in de rechterbovenhoek op **[!UICONTROL Create]** > **[!UICONTROL Asset]** .

1. Het elementbestand configureren:

   1. Selecteer de adverteerder die toegang heeft tot het elementbestand.

   1. Geef het elementbestand op een van de volgende manieren op:

      * Sleep een bestand naar het apparaat of het netwerk en zet het neer in het vak.

      * Klik op **[!UICONTROL Select a file]** om het bestand op uw apparaat of netwerk te zoeken.

   1. Klik op **[!UICONTROL Upload]**.

Alle ZIP-bestanden worden automatisch gedecomprimeerd. Wanneer u een spreadsheetbestand uploadt, wordt het bestand weergegeven op het subtabblad [!UICONTROL Feeds] . Wanneer u een afbeeldingsbestand uploadt, wordt het afbeeldingsbestand weergegeven op het subtabblad [!UICONTROL Images] .

## Een elementbestand downloaden

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** .

1. Klik op de tab **[!UICONTROL Assets]** .

1. Plaats de cursor op de elementenrij en klik op **[!UICONTROL Download]** .

   Het bestand wordt gedownload volgens de normale procedure van uw browser.

## Een elementbestand verwijderen

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** .

1. Klik op de tab **[!UICONTROL Assets]** .

1. Plaats de cursor op de elementenrij en klik op **[!UICONTROL Delete]** .

>[!MORELIKETHIS]
>
>* [ Beschikbare gebieden voor dynamische en voederdossiers ](/help/creative/appendix-available-feed-fields.md)
>* [ Werkstromen voor dynamische advertenties ](/help/creative/introduction/workflow-dynamic-ads.md)
>* [ beheer voedermalplaatjes ](/help/creative/feeds/feed-template-manage.md)
>* [ beheert catalogi ](/help/creative/feeds/catalog-manage.md)
>* [ beheer dynamische ad malplaatjes ](/help/creative/ad-templates/ad-template-manage.md)
>* [ voeg dynamische creatieve creatieve bibliotheek ](/help/creative/creative-libraries/creative-add-dynamic.md) toe
