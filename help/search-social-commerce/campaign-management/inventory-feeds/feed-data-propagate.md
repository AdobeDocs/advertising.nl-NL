---
title: Gegevens over voorraadfeed doorgeven via sjablonen
description: Meer informatie over het doorgeven van gegevens uit uw voorraad via advertentiesjablonen om de accountstructuur te beheren en dynamische advertenties te leveren.
exl-id: 9660af19-a517-4593-9a99-da600a0285a5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---

# Gegevens over voorraadfeed doorgeven via sjablonen

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (alleen handelingen verwijderen), en [!DNL Yandex] alleen accounts*

Nadat u een ad-netwerkspecifieke voedermalplaatje creeert en een voederdossier of een [!DNL Google] of [!DNL Microsoft] handelaarscentrum-account met dit account, kunt u dynamisch advertenties maken door de voedergegevens via de sjabloon door te geven volgens de [gegevensinstellingen van feed](feed-settings-manage.md). Tijdens propagatie, worden de kolomnamen in het malplaatje vervangen met gegevenswaarden in het voer, en de geproduceerde campagnes en hun componenten hebben de standaardmontages tenzij het malplaatje anders specificeert. Afhankelijk van de sjabloonopties maakt u met Zoeken, Sociaal en Commerce ofwel een nieuwe accountstructuur (campagnes, groepen en trefwoorden) voor de advertenties of wijst u de advertenties toe aan de bestaande accountstructuur.

Wanneer nieuwe feed-gegevens nieuwe gegevenswaarden voor een item bevatten of de sjabloon is gewijzigd, worden bestaande advertenties verwijderd en worden nieuwe advertenties gemaakt. Als de enige wijziging de aanwijzing van [!DNL Google Ads] Param 1 en Param 2, dan slechts worden die waarden bijgewerkt. Er worden nooit dubbele advertenties gemaakt (dezelfde pagina voor kopiëren en landen).

Wanneer u gegevens verspreidt, kunt u naar keuze voorproef de geproduceerde gegevens binnen een mening van de campagnehiërarchie, een bulksbladdossier voor overzicht produceren, of een bulksbladdossier voor directe post aan het ad netwerk produceren. Wanneer elke propagatieactie wordt voltooid, wordt een propagatiesamenvatting toegevoegd aan het lusje van Verspreidingen, die op het aantal van elk entiteittype wijzen dat werd of zou worden gecreeerd, gepauzeerd, of geschrapt gebaseerd op de propagatie. Als u de gegevens niet meteen plaatst, kunt u deze voorvertonen en later posten.

## Feed-bestanden doorgeven vanuit de [!UICONTROL Templates] tab

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, die voor de [!UICONTROL Templates] tab.

1. Schakel het selectievakje naast de sjablonen die u wilt verspreiden in.

1. Klik op de werkbalk op **[!UICONTROL Propagate]** en selecteer vervolgens een van de volgende opties:

   * **[!UICONTROL Propagate Only]:** De doorgegeven gegevens weergeven op het tabblad [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] tabs. U kunt de gegevens voor om het even welke component en zijn subcomponenten later nog posten van [!UICONTROL Templates] tab.

   * **[!UICONTROL Propagate and Preview]:** Een bestand met een opsommingsteken maken (met de naam &quot;`<feed file name>_<template name>`&quot;), die beschikbaar is in de [!UICONTROL Bulksheets] mening voor overzicht (maar niet op [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] tabs). U kunt het bestand met de opsommingstekens later plaatsen vanuit het dialoogvenster [!UICONTROL Bulksheets] weergeven.

     Als het resulterende bulksheet-bestand groter is dan 2 MB, heeft het bestand de ZIP-indeling. U hoeft het bestand niet uit te pakken om het te posten.

   * **[!UICONTROL Propagate and Post to SE]:** Een bestand met een opsommingsteken maken (met de naam &quot;`<feed file name>_<template name>`&quot;) die onmiddellijk voor het posten aan het advertentienetwerk een rij wordt gevormd. Het bestand met de opsommingstekens is beschikbaar in het dialoogvenster [!UICONTROL Bulksheets] wordt weergegeven, maar is niet beschikbaar op [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] tabs.

     Als het resulterende bulksheet-bestand groter is dan 2 MB, heeft het bestand de ZIP-indeling.

   De &quot;laatste prop. In de kolom Status wordt de taakstatus voor de toepasselijke sjablonen weergegeven.

   Wanneer elke propagatieactie wordt voltooid, wordt een propagatiesamenvatting toegevoegd aan [!UICONTROL Propagations] tab, die het aantal van elk entiteittype aangeeft dat is gemaakt, gepauzeerd of verwijderd op basis van de propagatie. De schatting omvat geen veranderingen die van binnen de eigen ad redacteur van het advertentienetwerk worden aangebracht.

## Feed-bestanden doorgeven vanuit de [!UICONTROL Feeds] list

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klik op de werkbalk boven de tabel met gegevens op **[!UICONTROL Feeds]**.

1. Schakel het selectievakje naast het feed-bestand in.

1. Klik boven de gegevenstabel op **[!UICONTROL Propagate/Post Feed Data]** en selecteer vervolgens een van de volgende opties:

   * **[!UICONTROL Propagate Only]:** De doorgegeven gegevens weergeven op het tabblad [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] tabs. U kunt de gegevens voor om het even welke component en zijn subcomponenten later nog posten van [!UICONTROL Templates] tab.

   * **[!UICONTROL Propagate and Preview]:** Een bestand met een opsommingsteken maken (met de naam &quot;`<feed file name>_<template name>`&quot;), die beschikbaar is in de [!UICONTROL Bulksheets] mening voor overzicht (maar niet op [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] tabs). U kunt het bestand met de opsommingstekens later plaatsen vanuit het dialoogvenster [!UICONTROL Bulksheets] weergeven.

     Als het resulterende bulksheet-bestand groter is dan 2 MB, heeft het bestand de ZIP-indeling. U hoeft het bestand niet uit te pakken om het te posten.

   * **[!UICONTROL Propagate and Post to SE]:** Een bestand met een opsommingsteken maken (met de naam &quot;`<feed file name>_<template name>`&quot;) die onmiddellijk voor het posten aan het advertentienetwerk een rij wordt gevormd. Het bestand met de opsommingstekens is beschikbaar in het dialoogvenster [!UICONTROL Bulksheets] wordt weergegeven, maar is niet beschikbaar op [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] tabs.

     Als het resulterende bulksheet-bestand groter is dan 2 MB, heeft het bestand de ZIP-indeling.

1. Selecteer in het pop-upvenster het selectievakje naast elke sjabloon waardoor u gegevens uit het feed-bestand wilt doorgeven en klik vervolgens op **[!UICONTROL Propagate Feed]**.

   Alle sjablonen die aan het bestand zijn gekoppeld, worden weergegeven.

De [!UICONTROL Templates] wordt geopend en &quot;[!UICONTROL Last Prop. Status]&quot; de kolom toont de baanstatus voor de toepasselijke malplaatjes.

Wanneer elke propagatieactie wordt voltooid, wordt een propagatiesamenvatting toegevoegd aan [!UICONTROL Propagations] tab, die het aantal van elk entiteittype aangeeft dat is gemaakt, gepauzeerd of verwijderd op basis van de propagatie. De schatting omvat geen veranderingen die van binnen de eigen ad redacteur van het advertentienetwerk worden aangebracht.

## Een overzicht van de propagatie weergeven

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klik op de knop **[!UICONTROL Propagations]** tab.

1. Klik naast de sjabloonnaam op ![Pictogram Instellingen weergeven/bewerken](/help/search-social-commerce/assets/settings.png "Pictogram Instellingen weergeven/bewerken") .

## Een propagatietaak stoppen

U kunt een propagatietaak voor de gegevens van de inventarisfeed stoppen terwijl de taak nog in de wachtrij staat.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, die voor de [!UICONTROL Templates] tab.

1. In het veld &quot;[!UICONTROL Last Prop. Status]&quot; naast de sjabloonnaam klikt u op **[!UICONTROL Cancel]**.

>[!MORELIKETHIS]
>
>* [Informatie over voorraadfeeds](inventory-feeds-about.md)
>* [Advertentiesjablonen beheren voor voorraadfeeds](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [Gegevens weergeven die zijn gegenereerd uit feeds](propagated-data-view.md)
>* [Uit feeds gegenereerde gegevens bewerken](propagated-data-edit.md)
>* [Gegevens van de post campagne die van voer aan advertentienetwerken worden geproduceerd](propagated-data-post.md)
>* [Een publicatietaak voor de gegevens van de inventarisfeed stoppen](stop-job.md)
>* [Statussen van gegevens die zijn gegenereerd uit feeds](propagated-data-status.md)
