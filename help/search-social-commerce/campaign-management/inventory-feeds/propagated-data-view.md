---
title: Gegevens weergeven die zijn gegenereerd uit feeds
description: Leer hoe u gegevens kunt bekijken die zijn gegenereerd uit de invoer van inventarisgegevens.
exl-id: ee48f0f1-65fb-4d27-8f59-0108835d70e5
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Gegevens weergeven die zijn gegenereerd uit feeds

*[!DNL Google Ads], [!DNL Microsoft Advertising] , [!DNL Yahoo! Japan Ads] (alleen acties verwijderen) en [!DNL Yandex] alleen accounts*

Wanneer u voedergegevens verspreidt zonder het tegelijkertijd aan het advertentienetwerk te posten, kunt u voorproef de gegevens op één van de volgende manieren. U kunt later [&#x200B; gegevens &#x200B;](propagated-data-post.md) van één van beide plaats aan de relevante advertentienetwerken naar keuze posten.

* Als u de optie aan &quot;[!UICONTROL Propagate and Preview] gebruikte,&quot;dan bekijk het geproduceerde bulksblad (genoemd &quot;`<feed file name>_<template name>`&quot;) van de [!UICONTROL Bulksheets] mening. Er worden geen gegevens opgenomen op de tabbladen [!UICONTROL Campaigns] , [!UICONTROL Ad Groups] , [!UICONTROL Keywords] en [!UICONTROL Ads] . Deze optie staat u toe om [&#x200B; de het landen pagina&#39;s &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) te bevestigen verbonden aan de advertenties en de sleutelwoorden alvorens u de gegevens post.

* Als u de optie hebt gebruikt voor &quot;[!UICONTROL Propagate only]&quot;, bekijkt u de gegenereerde gegevens in een hiërarchische weergave van de tabbladen [!UICONTROL Campaigns] , [!UICONTROL Ad Groups] , [!UICONTROL Keywords] en [!UICONTROL Ads] .

  In de weergaven van de campagnehiërarchie worden alleen de gegevens weergegeven die zijn gegenereerd uit het feed-bestand, niet de bestaande accountcomponenten. Nadat gegevens voor een component en al zijn subcomponents aan het advertentienetwerk worden gepost, is het niet meer vermeld in de mening van de campagnehiërarchie.

   1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** , dat wordt geopend op de tab [!UICONTROL Templates] .

   1. (Optioneel) Alleen campagnecomponenten weergeven die voor een specifieke sjabloon zijn gemaakt:

      1. Klik op de sjabloonnaam.

      1. Vouw in het menu [!UICONTROL Accounts] in het navigatievenster aan de linkerkant het netwerkknooppunt voor de advertentie en het knooppunt voor de netwerkaccount voor de advertentie uit en schakel vervolgens het selectievakje naast de sjabloonnaam in.

   1. Klik op het tabblad **[!UICONTROL Campaigns]** , **[!UICONTROL Ad Groups]** , **[!UICONTROL Keywords]** of **[!UICONTROL Ads]** , afhankelijk van de componenten die u wilt weergeven.

      >[!NOTE]
      >
      >* Tenzij u gegevens voor een specifieke sjabloon bekijkt, worden op de tabbladen [!UICONTROL Ad Groups] , [!UICONTROL Keywords] en [!UICONTROL Ads] alle groepen en advertenties vermeld die zijn gemaakt met alle sjablonen en feedbestanden. Productgroepen die worden gebruikt voor [!DNL Google Ads] winkeladvertenties, worden weergegeven op het tabblad [!UICONTROL Keywords] .
      >* Als u alleen de subcomponenten van een specifieke campagne wilt weergeven, begint u met het weergeven van het tabblad [!UICONTROL Campaigns] . Als u alleen de subcomponenten van een specifieke advertentiegroep wilt weergeven, begint u met het weergeven van de tab [!UICONTROL Ad Groups] .

   1. (Optioneel) Voer een van de volgende twee handelingen uit om meer informatie weer te geven:

      * Om de montages voor om het even welke campagne, en groep, sleutelwoord, of advertentie te bekijken, klik [&#x200B; Mening/geef montagespictogram &#x200B;](/help/search-social-commerce/assets/settings.png "Pictogram Instellingen weergeven/bewerken") naast de naam uit.

      * Ga als volgt te werk om de subcomponenten van een campagne of advertentiegroep weer te geven:

         * Als u alle advertentiegroepen in een campagne wilt weergeven, klikt u op de naam van de campagne.

         * Als u alle trefwoorden of productdoelen in een advertentiegroep wilt weergeven, klikt u op de naam van de advertentiegroep.

         * Als u alle advertenties in een advertentiegroep wilt weergeven, klikt u op de naam van de advertentiegroep en vervolgens op de tab [!UICONTROL Ads] .

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer inventarisvoer &#x200B;](inventory-feeds-about.md)
>* [&#x200B; geeft gegevens uit die van voer &#x200B;](propagated-data-edit.md) worden geproduceerd uit
>* [&#x200B; Post campagnegegevens die van voer aan ad netwerken worden geproduceerd &#x200B;](propagated-data-post.md)
>* [&#x200B; Einde een het posten baan voor de gegevens van het inventarisvoer &#x200B;](stop-job.md)
>* [&#x200B; Statussen van gegevens die uit voer &#x200B;](propagated-data-status.md) worden geproduceerd
