---
title: Gegevens over voorraadfeed doorgeven via sjablonen
description: Meer informatie over het doorgeven van gegevens uit uw voorraad via advertentiesjablonen om de accountstructuur te beheren en dynamische advertenties te leveren.
exl-id: 9660af19-a517-4593-9a99-da600a0285a5
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '876'
ht-degree: 0%

---

# Gegevens over voorraadfeed doorgeven via sjablonen

*[!DNL Google Ads], [!DNL Microsoft Advertising] , [!DNL Yahoo! Japan Ads] (alleen acties verwijderen) en [!DNL Yandex] alleen accounts*

Nadat u een ad netwerk-specifieke voedermalplaatje creeert en een voederdossier of een [!DNL Google] of [!DNL Microsoft] handels centrumrekening met het associeert, kunt u advertenties dynamisch tot stand brengen door de voedergegevens door het malplaatje volgens de [&#x200B; montages van voedergegevens &#x200B;](feed-settings-manage.md) te verspreiden. Tijdens propagatie, worden de kolomnamen in het malplaatje vervangen met gegevenswaarden in het voer, en de geproduceerde campagnes en hun componenten hebben de standaardmontages tenzij het malplaatje anders specificeert. Afhankelijk van de sjabloonopties maakt u met Zoeken, Sociaal en Commerce ofwel een nieuwe accountstructuur (campagnes, groepen en trefwoorden) voor de advertenties of wijst u de advertenties toe aan de bestaande accountstructuur.

Wanneer nieuwe feed-gegevens nieuwe gegevenswaarden voor een item bevatten of de sjabloon is gewijzigd, worden bestaande advertenties verwijderd en worden nieuwe advertenties gemaakt. Als de enige wijziging de aanwijzing van [!DNL Google Ads] Param 1 en Param 2 is, worden alleen die waarden bijgewerkt. Er worden nooit dubbele advertenties gemaakt (dezelfde pagina voor kopiëren en landen).

Wanneer u gegevens verspreidt, kunt u naar keuze voorproef de geproduceerde gegevens binnen een mening van de campagnehiërarchie, een bulksbladdossier voor overzicht produceren, of een bulksbladdossier voor directe post aan het ad netwerk produceren. Wanneer elke propagatieactie wordt voltooid, wordt een propagatiesamenvatting toegevoegd aan het lusje van Verspreidingen, die op het aantal van elk entiteittype wijzen dat werd of zou worden gecreeerd, gepauzeerd, of geschrapt gebaseerd op de propagatie. Als u de gegevens niet meteen plaatst, kunt u deze voorvertonen en later posten.

## Feed-bestanden doorgeven via het tabblad [!UICONTROL Templates]

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** , dat wordt geopend op de tab [!UICONTROL Templates] .

1. Schakel het selectievakje naast de sjablonen die u wilt verspreiden in.

1. Klik in de werkbalk op **[!UICONTROL Propagate]** en selecteer een van de volgende opties:

   * **[!UICONTROL Propagate Only]:** De doorgegeven gegevens weergeven op de tabbladen [!UICONTROL Campaigns] , [!UICONTROL Ad Groups] , [!UICONTROL Keywords] en [!UICONTROL Ads] . U kunt de gegevens voor elke component en de bijbehorende subcomponenten later nog steeds plaatsen vanaf het tabblad [!UICONTROL Templates] .

   * **[!UICONTROL Propagate and Preview]:** om een dossier tot stand te brengen bulksheet (genoemd &quot;`<feed file name>_<template name>`&quot;), dat in de [!UICONTROL Bulksheets] mening voor overzicht (maar niet op [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] lusjes) beschikbaar is. U kunt het bulksbladbestand later vanuit de [!UICONTROL Bulksheets] -weergave plaatsen.

     Als het resulterende bulksheet-bestand groter is dan 2 MB, heeft het bestand de ZIP-indeling. U hoeft het bestand niet uit te pakken om het te posten.

   * **[!UICONTROL Propagate and Post to SE]:** om een bulksheet dossier (genoemd &quot;`<feed file name>_<template name>`&quot;te creëren) dat onmiddellijk voor het posten aan het advertentienetwerk een rij wordt gevormd. Het bulksbladbestand is beschikbaar in de [!UICONTROL Bulksheets] -weergave, maar niet op de tabbladen [!UICONTROL Campaigns] , [!UICONTROL Ad Groups] , [!UICONTROL Keywords] en [!UICONTROL Ads] .

     Als het resulterende bulksheet-bestand groter is dan 2 MB, heeft het bestand de ZIP-indeling.

   De &quot;laatste prop. In de kolom Status wordt de taakstatus voor de toepasselijke sjablonen weergegeven.

   Wanneer elke propagatieactie wordt voltooid, wordt een propagatiesamenvatting toegevoegd aan het [!UICONTROL Propagations] lusje, die op het aantal van elk entiteittype wijst dat werd of zou worden gecreeerd, gepauzeerd, of geschrapt gebaseerd op de propagatie. De schatting omvat geen veranderingen die van binnen de eigen ad redacteur van het advertentienetwerk worden aangebracht.

## Feed-bestanden doorgeven vanuit de lijst [!UICONTROL Feeds]

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** .

1. Klik in de werkbalk boven de gegevenstabel op **[!UICONTROL Feeds]** .

1. Schakel het selectievakje naast het feed-bestand in.

1. Klik boven de gegevenstabel op **[!UICONTROL Propagate/Post Feed Data]** en selecteer een van de volgende opties:

   * **[!UICONTROL Propagate Only]:** De doorgegeven gegevens weergeven op de tabbladen [!UICONTROL Campaigns] , [!UICONTROL Ad Groups] , [!UICONTROL Keywords] en [!UICONTROL Ads] . U kunt de gegevens voor elke component en de bijbehorende subcomponenten later nog steeds plaatsen vanaf het tabblad [!UICONTROL Templates] .

   * **[!UICONTROL Propagate and Preview]:** om een dossier tot stand te brengen bulksheet (genoemd &quot;`<feed file name>_<template name>`&quot;), dat in de [!UICONTROL Bulksheets] mening voor overzicht (maar niet op [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] lusjes) beschikbaar is. U kunt het bulksbladbestand later vanuit de [!UICONTROL Bulksheets] -weergave plaatsen.

     Als het resulterende bulksheet-bestand groter is dan 2 MB, heeft het bestand de ZIP-indeling. U hoeft het bestand niet uit te pakken om het te posten.

   * **[!UICONTROL Propagate and Post to SE]:** om een bulksheet dossier (genoemd &quot;`<feed file name>_<template name>`&quot;te creëren) dat onmiddellijk voor het posten aan het advertentienetwerk een rij wordt gevormd. Het bulksbladbestand is beschikbaar in de [!UICONTROL Bulksheets] -weergave, maar niet op de tabbladen [!UICONTROL Campaigns] , [!UICONTROL Ad Groups] , [!UICONTROL Keywords] en [!UICONTROL Ads] .

     Als het resulterende bulksheet-bestand groter is dan 2 MB, heeft het bestand de ZIP-indeling.

1. Selecteer in het pop-upvenster het selectievakje naast elke sjabloon waardoorheen u gegevens uit het feed-bestand wilt doorgeven en klik op **[!UICONTROL Propagate Feed]** .

   Alle sjablonen die aan het bestand zijn gekoppeld, worden weergegeven.

Het tabblad [!UICONTROL Templates] wordt geopend en in de kolom &quot;[!UICONTROL Last Prop. Status]&quot; wordt de taakstatus voor de toepasselijke sjablonen weergegeven.

Wanneer elke propagatieactie wordt voltooid, wordt een propagatiesamenvatting toegevoegd aan het [!UICONTROL Propagations] lusje, die op het aantal van elk entiteittype wijst dat werd of zou worden gecreeerd, gepauzeerd, of geschrapt gebaseerd op de propagatie. De schatting omvat geen veranderingen die van binnen de eigen ad redacteur van het advertentienetwerk worden aangebracht.

## Een overzicht van de propagatie weergeven

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** .

1. Klik op de tab **[!UICONTROL Propagations]** .

1. Naast de malplaatjenaam, klik ![&#x200B; Mening/geef montagespictogram &#x200B;](/help/search-social-commerce/assets/settings.png " Mening/geef montagespictogram ") uit.

## Een propagatietaak stoppen

U kunt een propagatietaak voor de gegevens van de inventarisfeed stoppen terwijl de taak nog in de wachtrij staat.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** , dat wordt geopend op de tab [!UICONTROL Templates] .

1. Klik in de kolom &quot;[!UICONTROL Last Prop. Status]&quot; naast de sjabloonnaam op **[!UICONTROL Cancel]** .

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer inventarisvoer &#x200B;](inventory-feeds-about.md)
>* [&#x200B; beheer en malplaatjes voor inventarisvoer &#x200B;](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
>* [&#x200B; gegevens van de Mening die van voer &#x200B;](propagated-data-view.md) worden geproduceerd
>* [&#x200B; geeft gegevens uit die van voer &#x200B;](propagated-data-edit.md) worden geproduceerd uit
>* [&#x200B; Post campagnegegevens die van voer aan ad netwerken worden geproduceerd &#x200B;](propagated-data-post.md)
>* [&#x200B; Einde een het posten baan voor de gegevens van het inventarisvoer &#x200B;](stop-job.md)
>* [&#x200B; Statussen van gegevens die uit voer &#x200B;](propagated-data-status.md) worden geproduceerd
