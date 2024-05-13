---
title: Gegevens weergeven die zijn gegenereerd uit feeds
description: Leer hoe u gegevens kunt bekijken die zijn gegenereerd uit de invoer van inventarisgegevens.
exl-id: ee48f0f1-65fb-4d27-8f59-0108835d70e5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Gegevens weergeven die zijn gegenereerd uit feeds

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (alleen handelingen verwijderen), en [!DNL Yandex] alleen accounts*

Wanneer u voedergegevens verspreidt zonder het tegelijkertijd aan het advertentienetwerk te posten, kunt u voorproef de gegevens op één van de volgende manieren. U kunt later desgewenst [postgegevens](propagated-data-post.md) van beide locaties naar de relevante advertentienetwerken.

* Als u de optie &quot;[!UICONTROL Propagate and Preview],&quot; bekijkt u het gegenereerde bulksblad (met de naam &quot;`<feed file name>_<template name>`&quot;) van de [!UICONTROL Bulksheets] weergeven. Er zijn geen gegevens opgenomen op het tabblad [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] tabs. Met deze optie kunt u [De openingspagina&#39;s valideren](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) gekoppeld aan de advertenties en trefwoorden voordat u de gegevens plaatst.

* Als u de optie &quot;[!UICONTROL Propagate only],&quot;bekijk dan de geproduceerde gegevens binnen een mening van de campagnehiërarchie van [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] tabs.

  In de weergaven van de campagnehiërarchie worden alleen de gegevens weergegeven die zijn gegenereerd uit het feed-bestand, niet de bestaande accountcomponenten. Nadat gegevens voor een component en al zijn subcomponents aan het advertentienetwerk worden gepost, is het niet meer vermeld in de mening van de campagnehiërarchie.

   1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, die voor de [!UICONTROL Templates] tab.

   1. (Optioneel) Alleen campagnecomponenten weergeven die voor een specifieke sjabloon zijn gemaakt:

      1. Klik op de sjabloonnaam.

      1. In de [!UICONTROL Accounts] in het linkernavigatievenster, breid de knoop van het advertentienetwerk en de knoop van de advertentienetwerkrekening uit, en selecteer dan de controledoos naast de malplaatjenaam.

   1. Klik op de knop **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]**, of **[!UICONTROL Ads]** , afhankelijk van de componenten die u wilt weergeven.

      >[!NOTE]
      >
      >* Tenzij u gegevens voor een specifieke sjabloon bekijkt, wordt de [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] op de tabbladen staan alle groepen en trefwoorden en advertenties die zijn gemaakt op basis van alle sjablonen en feedbestanden. Productgroepen gebruikt voor [!DNL Google Ads] winkeladvertenties worden vermeld op de [!UICONTROL Keywords] tab.
      >* Als u alleen de subcomponenten van een specifieke campagne wilt weergeven, begint u met het weergeven van de [!UICONTROL Campaigns] tab. Als u alleen de subcomponenten van een specifieke advertentiegroep wilt weergeven, begint u met het weergeven van de [!UICONTROL Ad Groups] tab.

   1. (Optioneel) Voer een van de volgende twee handelingen uit om meer informatie weer te geven:

      * Als u de instellingen voor een campagne, groep, trefwoord of advertentie wilt weergeven, klikt u op [Pictogram Instellingen weergeven/bewerken](/help/search-social-commerce/assets/settings.png "Pictogram Instellingen weergeven/bewerken") naast de naam.

      * Ga als volgt te werk om de subcomponenten van een campagne of advertentiegroep weer te geven:

         * Als u alle advertentiegroepen in een campagne wilt weergeven, klikt u op de naam van de campagne.

         * Als u alle trefwoorden of productdoelen in een advertentiegroep wilt weergeven, klikt u op de naam van de advertentiegroep.

         * Als u alle advertenties in een advertentiegroep wilt weergeven, klikt u op de naam van de advertentiegroep en vervolgens op de knop [!UICONTROL Ads] tab.

>[!MORELIKETHIS]
>
>* [Informatie over voorraadfeeds](inventory-feeds-about.md)
>* [Uit feeds gegenereerde gegevens bewerken](propagated-data-edit.md)
>* [Gegevens van de post campagne die van voer aan advertentienetwerken worden geproduceerd](propagated-data-post.md)
>* [Een publicatietaak voor de gegevens van de inventarisfeed stoppen](stop-job.md)
>* [Statussen van gegevens die zijn gegenereerd uit feeds](propagated-data-status.md)
