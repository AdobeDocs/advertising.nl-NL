---
title: Uit feeds gegenereerde gegevens bewerken
description: Leer hoe u gegevens kunt bewerken die zijn gegenereerd uit de invoer van inventarisgegevens.
exl-id: d43b593d-758d-4561-9cda-33b235099cc6
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Uit feeds gegenereerde gegevens bewerken

*[!DNL Google Ads], [!DNL Microsoft Advertising] , [!DNL Yahoo! Japan Ads] (alleen acties verwijderen) en [!DNL Yandex] alleen accounts*

Wanneer u voedergegevens verspreidt zonder het gelijktijdig te posten aan het advertentienetwerk, kunt u de gegevens op één van beide volgende manieren uitgeven. U kunt later [&#x200B; gegevens &#x200B;](propagated-data-post.md) van één van beide plaats aan de relevante advertentienetwerken naar keuze posten:

* Als u de optie aan &quot;[!UICONTROL Propagate and Preview] gebruikte,&quot;dan kunt u het geproduceerde dossier van het bulkblad (genoemd &quot;`<feed file name>_<template name>`&quot;) uitgeven door het van de [!UICONTROL Bulksheets] mening te downloaden, het dossier uit te geven, en het opnieuw te uploaden. Er worden geen gegevens opgenomen op de tabbladen [!UICONTROL Campaigns] , [!UICONTROL Ad Groups] , [!UICONTROL Keywords] en [!UICONTROL Ads] .

* Als u de optie aan &quot;[!UICONTROL Propagate only] gebruikte,&quot;dan kunt u de geproduceerde gegevens voor componenten met [[!UICONTROL New] status &#x200B;](propagated-data-status.md) binnen een mening van de campagnehiërarchie van de [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] lusjes uitgeven.

  In de weergaven van de campagnehiërarchie worden alleen de gegevens weergegeven die zijn gegenereerd uit het feed-bestand, niet de bestaande accountcomponenten. Nadat gegevens voor een component en al zijn subcomponents aan het advertentienetwerk worden gepost, is het niet meer vermeld in de campagnehiërarchie.

   1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** , dat wordt geopend op de tab [!UICONTROL Templates] .

   1. (Optioneel) Alleen campagnecomponenten weergeven die voor een specifieke sjabloon zijn gemaakt:

      1. Klik op de sjabloonnaam.

      1. Vouw in het menu [!UICONTROL Accounts] in het navigatievenster aan de linkerkant het netwerkknooppunt voor de advertentie en het knooppunt voor de netwerkaccount voor de advertentie uit en schakel vervolgens het selectievakje naast de sjabloonnaam in.

   1. Klik op het tabblad **[!UICONTROL Campaigns]** , **[!UICONTROL Ad Groups]** , **[!UICONTROL Keywords]** of **[!UICONTROL Ads]** , afhankelijk van de componenten die u wilt weergeven.

      >[!NOTE]
      >
      >* Tenzij u gegevens voor een specifieke sjabloon bekijkt, worden op de tabbladen [!UICONTROL Ad Groups] , [!UICONTROL Keywords] en [!UICONTROL Ads] alle groepen en advertenties vermeld die zijn gemaakt met alle sjablonen en feedbestanden. Productgroepen die worden gebruikt voor [!DNL Google Ads] winkeladvertenties, worden weergegeven op het tabblad [!UICONTROL Keywords] .
      >* Als u alleen de subcomponenten van een specifieke campagne wilt weergeven, begint u met het weergeven van het tabblad [!UICONTROL Campaigns] . Als u alleen de subcomponenten van een specifieke advertentiegroep wilt weergeven, begint u met het weergeven van de tab [!UICONTROL Ad Groups] .

   1. (Optioneel; alleen voor het bewerken van advertentiegroepen, trefwoorden of advertenties) Filter de lijst zodat deze alleen de subcomponenten van een specifieke campagne of advertentiegroep bevat:

      * Als u alle advertentiegroepen in een campagne wilt weergeven, klikt u op de naam van de campagne.

      * Als u alle trefwoorden in een advertentiegroep wilt weergeven, klikt u op de naam van de advertentiegroep.

      * Als u alles wilt weergeven zoals in een advertentiegroep, klikt u op de naam van de advertentiegroep en vervolgens op de tab [!UICONTROL Ads] .

   1. Klik [&#x200B; Mening/geef montagespictogram &#x200B;](/help/search-social-commerce/assets/settings.png "Pictogram Instellingen weergeven/bewerken") naast de campagne, ad groep, sleutelwoord, of advertentienaam uit.

   1. Bewerk de instellingen en klik op **[!UICONTROL Save]** .

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer inventarisvoer &#x200B;](inventory-feeds-about.md)
>* [&#x200B; gegevens van de Mening die van voer &#x200B;](propagated-data-view.md) worden geproduceerd
>* [&#x200B; Post campagnegegevens die van voer aan ad netwerken worden geproduceerd &#x200B;](propagated-data-post.md)
>* [&#x200B; Einde een het posten baan voor de gegevens van het inventarisvoer &#x200B;](stop-job.md)
>* [&#x200B; Statussen van gegevens die uit voer &#x200B;](propagated-data-status.md) worden geproduceerd
