---
title: Elementbestanden beheren
description: Leer hoe u het elementbestand voor een adverteerder kunt uploaden en beheren.
feature: Creative Dynamic Creatives
source-git-commit: 76e3ae8369fda1c4d95c06ecb085a8669dcf142b
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---

# Elementbestanden beheren

Dynamische HTML5-advertenties vereisen zowel een feed-bestand in de indeling Microsoft Excel-spreadsheet (XLSX) als de afbeeldingselementen waarnaar in het spreadsheet wordt verwezen (behalve Adobe Experience Manager-elementverwijzingen). Voor statische HTML5-advertenties is slechts één afbeeldingselement per advertentie vereist.

>[!NOTE]
>
> U kunt elk feed-bestand slechts voor één catalogus gebruiken.

## Bestandsvereisten

* Dynamische HTML5-advertenties:

   * Een feed-bestand in de indeling Microsoft Excel-werkblad (XLSX), met één koptekstrij en één gegevensrij voor elke advertentievariatie. Neem in elke rij een afbeeldingsnaam of een verwijzing naar een Adobe Experience Manager op.<!-- need spec of available column names that the user-created header names must map to; need to reference it in feed template topic too, so make it a separate file/appendix. -->

     Voor beelden zult u uploaden, verwijs het beeld gebruikend het formaat `images/image_name` (zoals `images/300x250_acme_logo.png`.) <!-- Verify.  Also need to include the spec for how to reference images in AEM -->

   * De gekoppelde afbeeldingselementen in JPEG-, JPG- of PNG-indeling.<!-- NOT GIF still? And is this true: The maximum file size is two (2) MB. --> zie [ gesteunde creatieve grootte ](/help/creative/creative-libraries/creative-sizes.md).

  U kunt één enkel XLSX- dossier, één enkel beelddossier, of één enkel dossier uploaden dat om het even welke combinatie XLSX en beelddossiers bevat.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Statische HTML5-advertenties:

   * Eén afbeeldingselement per advertentie in JPG-, JPEG- of PNG-indeling.

     U kunt één afbeelding of meerdere afbeeldingen uploaden in een ZIP-bestand.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

## Een elementbestand uploaden

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
>* [ Werkschema voor dynamische advertenties ](/help/creative/introduction/workflow-dynamic-ads.md)
>* [ beheer voedermalplaatjes ](/help/creative/feeds/feed-template-manage.md)
>* [ beheert catalogi ](/help/creative/feeds/catalog-manage.md)
>* [ beheer dynamische ad malplaatjes ](/help/creative/ad-templates/ad-template-manage.md)
>* [ voeg dynamische creatieve creatieve bibliotheek ](/help/creative/creative-libraries/creative-add-dynamic.md) toe
