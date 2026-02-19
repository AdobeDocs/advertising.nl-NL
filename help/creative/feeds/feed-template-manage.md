---
title: Feed-sjablonen beheren
description: Leer hoe u voedersjablonen beheert.
feature: Creative Dynamic Creatives
exl-id: 63f8af87-639c-45c8-b17f-99ce19594d35
source-git-commit: ad7d2b02103b5a45dadcd51b60621c31e9db0d29
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# Feed-sjablonen beheren

<!-- I have a "Retail" feed template that was created by rkarthik@adobe. Ask product if this is available to all clients or just internal.  -->

<!-- We have a finite set of supported fields on the backend. I need to include that info in an appendix. -->

Met Feed-sjablonen kunt u velden in uw feed-bestanden/catalogi toewijzen met velden op de Advertising Creative-achtergrond. Dynamische HTML5- en videoadvertenties, maar geen statische HTML5-advertenties, vereisen een feed-sjabloon om dynamische advertenties te maken. U kunt desgewenst universele voedersjablonen downloaden en vullen ([!UICONTROL Retail] voor kleinhandelscampagnes en [!UICONTROL Adobe Creative Template] voor elk type campagne).

U kunt een voedermalplaatje met veelvoudige advertentiesjablonen gebruiken.

>[!TIP]
>
>Voor alle rekeningen met dynamische video&#39;s, is de beste praktijken [ het universele voedermalplaatje [!UICONTROL Adobe Creative Template]](feed-template-manage.md) te downloaden, elk gebied in het activadossier aan een gebied op de Advertising Creative achterkant in kaart te brengen, en dan het voedermalplaatje anders te noemen en te uploaden. Gebruik het nieuwe voedermalplaatje, samen met het activadossier, om een catalogus [ tot stand te brengen. ](catalog-manage.md)

## Een voedersjabloon maken

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** .

1. Klik op de tab **[!UICONTROL Templates]** .

1. Klik in de rechterbovenhoek op **[!UICONTROL Create]** > **[!UICONTROL Template]** .

1. Specificeer de [ montages van het voedermalplaatje ](#feed-template-settings).

1. Klik op **[!UICONTROL Save]**.

## Een voedersjabloon bewerken

**Nota:** u kunt slechts voedermalplaatjes uitgeven die u creeerde.

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** .

1. Klik op de tab **[!UICONTROL Templates]** .

1. Plaats de cursor op de sjabloonrij en klik op **[!UICONTROL Duplicate]** .

1. Bewerk de [ montages van het voedermalplaatje ](#feed-template-settings) zoals nodig.

1. Klik op **[!UICONTROL Save]**.

## Een voedersjabloon weergeven

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** .

1. Klik op de tab **[!UICONTROL Templates]** .

1. Plaats de cursor op de sjabloonrij en klik op **[!UICONTROL View]** .

## Een voedersjabloon dupliceren

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** .

1. Klik op de tab **[!UICONTROL Templates]** .

1. Plaats de cursor op de sjabloonrij en klik op **[!UICONTROL Duplicate]** .

1. Voer in het scherm [!UICONTROL Duplicate Template] een unieke **[!UICONTROL Template Name]** in. Als u een sjabloon dupliceert die door iemand anders is gemaakt, selecteert u de **[!UICONTROL Advertiser]** . Naar keuze geef andere [ montages van het voedermalplaatje ](#feed-template-settings) uit zoals nodig.

1. Klik op **[!UICONTROL Save]**.

## Een feed-sjabloon downloaden

Gedownloade feed-sjablonen hebben de indeling XLSX (zipped Microsoft Excel spreadsheet).

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Feeds]** .

1. Klik op de tab **[!UICONTROL Templates]** .

1. Plaats de cursor op de sjabloonrij en klik op **[!UICONTROL Download]** .

   Het bestand wordt gedownload volgens de normale procedure van uw browser.

## Sjablooninstellingen voor feed {#feed-template-settings}

### [!UICONTROL General] instellingen

**[!UICONTROL Template Name]:** Een unieke sjabloonnaam voor de opgegeven adverteerder.

**[!UICONTROL Advertiser]:** De adverteerder die de sjabloon kan gebruiken.

**[!UICONTROL Description]:** (Facultatieve) Informatie die aan iedereen nuttig is die het voedermalplaatje gebruikt.

### [!UICONTROL Field Mapping] instellingen

Wijs elk veld in het feed-bestand toe aan een veld op de Advertising Creative-achtergrond. Zie &quot;[ Beschikbare gebieden voor dynamische en voederdossiers ](/help/creative/appendix-available-feed-fields.md)&quot;voor een lijst van de achterste gebieden en hun vereiste attributen.<!-- Check w/product: What is displayed where in the UI/reports and published ads? -->

Minstens één gebied van het inputdossier moet als &quot;[!UICONTROL Is Unique] worden gemerkt.&quot; Als u een veldtoewijzing wilt toevoegen, klikt u op **[!UICONTROL +]** . Als u de laatste veldtoewijzing wilt verwijderen, klikt u op **[!UICONTROL +]** .

**[!UICONTROL Field Name]:** Het gebied in het voederdossier.

**[!UICONTROL Description]:** (Facultatieve) Informatie die voor iedereen nuttig is die het voedermalplaatje gebruikt.

**[!UICONTROL Is Unique]:** Geeft aan dat het veld een unieke id (sleutel) is. Ten minste één veld per voedersjabloon moet uniek zijn. Om deze optie te selecteren, klik de knoop om het naar het recht te bewegen.<!-- **Note: The unique identifier is different from the feed "trigger" in experience settings. -->

**[!UICONTROL Backend Field]:** het [ gebied op de achtergrond van Advertising Creative ](/help/creative/appendix-available-feed-fields.md) dat aan gespecificeerd [!UICONTROL Field Name] in het voederdossier in kaart brengt.

>[!MORELIKETHIS]
>
>* [ Werkstromen voor dynamische advertenties ](/help/creative/introduction/workflow-dynamic-ads.md)
>* [ beheert activa dossiers ](/help/creative/feeds/asset-manage.md)
>* [ beheert catalogi ](/help/creative/feeds/catalog-manage.md)
>* [ Spoor het statuut van catalogusverwerkingstaken ](/help/creative/feeds/job-status-track.md)
>* [ beheer dynamische ad malplaatjes ](/help/creative/ad-templates/ad-template-manage.md)
>* [ voeg dynamische creatieve creatieve bibliotheek ](/help/creative/creative-libraries/creative-add-dynamic.md) toe
