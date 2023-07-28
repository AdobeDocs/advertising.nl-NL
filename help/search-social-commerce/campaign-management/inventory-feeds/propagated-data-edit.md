---
title: Uit feeds gegenereerde gegevens bewerken
description: Leer hoe u gegevens kunt bewerken die zijn gegenereerd uit de invoer van inventarisgegevens.
exl-id: 5f866557-e44b-4fd9-9683-f7fbaf6d308b
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Uit feeds gegenereerde gegevens bewerken

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (alleen handelingen verwijderen), en [!DNL Yandex] alleen accounts*

Wanneer u voedergegevens verspreidt zonder het gelijktijdig te posten aan het advertentienetwerk, kunt u de gegevens op één van beide volgende manieren uitgeven. U kunt later desgewenst [postgegevens](propagated-data-post.md) van beide locaties naar de relevante advertentienetwerken:

* Als u de optie &quot;[!UICONTROL Propagate and Preview],&quot; kunt u het gegenereerde bestand met de opsommingstekens bewerken (met de naam &quot;`<feed file name>_<template name>`&quot;) door deze te downloaden van de [!UICONTROL Bulksheets] weergeven, het bestand bewerken en opnieuw uploaden. Er zijn geen gegevens opgenomen op het tabblad [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] tabs.

* Als u de optie &quot;[!UICONTROL Propagate only],&quot; kunt u de gegenereerde gegevens voor componenten bewerken met de [[!UICONTROL New] status](propagated-data-status.md) binnen een campagnehiërarchieweergave vanuit de [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] tabs.

  In de weergaven van de campagnehiërarchie worden alleen de gegevens weergegeven die zijn gegenereerd uit het feed-bestand, niet de bestaande accountcomponenten. Nadat gegevens voor een component en al zijn subcomponents aan het advertentienetwerk worden gepost, is het niet meer vermeld in de campagnehiërarchie.

   1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, die voor de [!UICONTROL Templates] tab.

   1. (Optioneel) Alleen campagnecomponenten weergeven die voor een specifieke sjabloon zijn gemaakt:

      1. Klik op de sjabloonnaam.

      1. In de [!UICONTROL Accounts] in het linkernavigatievenster, breid de knoop van het advertentienetwerk en de knoop van de advertentienetwerkrekening uit, en selecteer dan de controledoos naast de malplaatjenaam.

   1. Klik op de knop **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]**, of **[!UICONTROL Ads]** , afhankelijk van de componenten die u wilt weergeven.

      >[!NOTE]
      >
      >* Tenzij u gegevens voor een specifieke sjabloon bekijkt, wordt de [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] op de tabbladen staan alle groepen en trefwoorden en advertenties die zijn gemaakt op basis van alle sjablonen en feedbestanden. Productgroepen gebruikt voor [!DNL Google Ads] winkeladvertenties worden vermeld op de [!UICONTROL Keywords] tab.
      >* Als u alleen de subcomponenten van een specifieke campagne wilt weergeven, begint u met het weergeven van de [!UICONTROL Campaigns] tab. Als u alleen de subcomponenten van een specifieke advertentiegroep wilt weergeven, begint u met het weergeven van de [!UICONTROL Ad Groups] tab.

   1. (Optioneel; alleen voor het bewerken van advertentiegroepen, trefwoorden of advertenties) Filter de lijst zodat deze alleen de subcomponenten van een specifieke campagne of advertentiegroep bevat:

      * Als u alle advertentiegroepen in een campagne wilt weergeven, klikt u op de naam van de campagne.

      * Als u alle trefwoorden in een advertentiegroep wilt weergeven, klikt u op de naam van de advertentiegroep.

      * Als u alles wilt weergeven zoals in een advertentiegroep, klikt u op de naam van de advertentiegroep en vervolgens op de knop [!UICONTROL Ads] tab.

   1. Klikken [Pictogram Instellingen weergeven/bewerken](/help/search-social-commerce/assets/settings.png "Pictogram Instellingen weergeven/bewerken") naast de naam van de campagne, advertentiegroep, trefwoord of advertentie.

   1. Bewerk de instellingen en klik op **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Informatie over voorraadfeeds](inventory-feeds-about.md)
>* [Gegevens weergeven die zijn gegenereerd uit feeds](propagated-data-view.md)
>* [Gegevens van de post campagne die van voer aan advertentienetwerken worden geproduceerd](propagated-data-post.md)
>* [Een publicatietaak voor de gegevens van de inventarisfeed stoppen](stop-job.md)
>* [Statussen van gegevens die zijn gegenereerd uit feeds](propagated-data-status.md)
