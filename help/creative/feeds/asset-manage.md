---
title: Elementbestanden beheren
description: Leer hoe u het elementbestand voor een adverteerder kunt uploaden en beheren.
feature: Creative Dynamic Creatives
exl-id: 2fe2d778-8456-490a-bf44-234dbc08649f
source-git-commit: ad7d2b02103b5a45dadcd51b60621c31e9db0d29
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---

# Elementbestanden beheren

* Dynamische HTML5-advertenties vereisen een feed-bestand in de indeling Microsoft Excel-spreadsheet (XLSX) en de eigenlijke afbeeldingselementen waarnaar in het spreadsheet wordt verwezen.

* Voor statische HTML5-advertenties is slechts één afbeeldingselement per advertentie vereist.

* Voor videoladingen is een feed-bestand vereist in de indeling Microsoft Excel-spreadsheet (XLSX) en de werkelijke video-elementen waarnaar in het spreadsheet wordt verwezen.

>[!NOTE]
>
> U kunt elk feed-bestand slechts voor één catalogus gebruiken.

## Bestandsvereisten

* Dynamische HTML5-advertenties:

   * Een feed-bestand in de indeling CSV, TSV of Microsoft Excel-spreadsheet (XLSX), met één koptekstrij en één gegevensrij voor elke advertentievariatie. Neem in elke rij een afbeeldingsnaam op in de indeling `images/image_name` (bijvoorbeeld `images/300x250_acme_logo.png` ).

     De adverteerder-specifieke gebiedsnamen moeten aan de [&#x200B; beschikbare gebieden voor dynamische ad voederdossiers &#x200B;](/help/creative/appendix-available-feed-fields.md) in kaart brengen.

   * De bijbehorende afbeeldingselementen in de indeling GIF, JPEG, JPG of PNG.<!-- Is this true: The maximum file size is two (2) MB. --> zie [&#x200B; gesteunde creatieve grootte &#x200B;](/help/creative/creative-libraries/creative-sizes.md).

  U kunt één enkel XLSX- dossier, één enkel beelddossier, of één enkel dossier uploaden dat om het even welke combinatie XLSX en beelddossiers bevat.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Statische HTML5-advertenties:

   * Eén afbeeldingselement per advertentie in GIF-, JPG-, JPEG- of PNG-indeling.

     U kunt één afbeelding of meerdere afbeeldingen uploaden in een ZIP-bestand.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

* Dynamische videobaden:

   * Een feed-bestand in de indeling CSV, TSV of Microsoft Excel-spreadsheet (XLSX), met één koptekstrij en één gegevensrij voor elke advertentievariatie. Neem in elke rij een videonaam op in de indeling `videos/image_name` (bijvoorbeeld `videos/300x250_acme_logo.png` ). Het ZIP-bestand kan maximaal 512 MB en maximaal 500 rijen bevatten.

     De adverteerder-specifieke gebiedsnamen moeten aan de [&#x200B; beschikbare gebieden voor dynamische ad voederdossiers &#x200B;](/help/creative/appendix-available-feed-fields.md) in kaart brengen.

     Voor alle rekeningen met dynamische video&#39;s, moet de beste praktijk [&#x200B; een catalogus &#x200B;](catalog-manage.md) tot stand brengen gebruikend het activadossier samen met een exemplaar van het [&#x200B; universele voedermalplaatje [!UICONTROL Adobe Creative Template]](feed-template-manage.md), waarin u elk gebied in het activadossier aan een gebied op de achtergrond van Advertising Creative in kaart brengt.

   * De gekoppelde video-elementen in MP4-, MOV- of WEBM-indeling. Tot de ondersteunde advertentiesjablonen behoren startkaart, eindkaart, overlay bovenaan, bedekking onderaan of L-vormig. De duur van elke video moet tussen 1 en 90 seconden liggen. Zie [&#x200B; gesteunde creatieve grootte &#x200B;](/help/creative/creative-libraries/creative-sizes.md).

  U kunt één enkel XLSX- dossier, één enkel beelddossier, of één enkel dossier uploaden dat om het even welke combinatie XLSX en videodossiers bevat.<!-- Check w/eng re any limitations or best practices WRT number of files and filesize allowed -->

## Een elementbestand uploaden

>[!NOTE]
>
>In plaats van het uploaden van activadossiers, kunt u een catalogus ook direct uploaden wanneer u [&#x200B; dynamische creatieve creatieve bibliotheek &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md) toevoegt. Alle catalogi die u daar maakt, worden beschikbaar in de [!UICONTROL Catalogs] -weergave voor toekomstig gebruik.

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
>* [&#x200B; Beschikbare gebieden voor dynamische en voederdossiers &#x200B;](/help/creative/appendix-available-feed-fields.md)
>* [&#x200B; Werkstromen voor dynamische advertenties &#x200B;](/help/creative/introduction/workflow-dynamic-ads.md)
>* [&#x200B; beheer voedermalplaatjes &#x200B;](/help/creative/feeds/feed-template-manage.md)
>* [&#x200B; beheert catalogi &#x200B;](/help/creative/feeds/catalog-manage.md)
>* [&#x200B; beheer dynamische ad malplaatjes &#x200B;](/help/creative/ad-templates/ad-template-manage.md)
>* [&#x200B; voeg dynamische creatieve creatieve bibliotheek &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md) toe
