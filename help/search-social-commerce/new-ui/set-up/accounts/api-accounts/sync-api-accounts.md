---
title: (Nieuwe interface) Gegevens handmatig synchroniseren en netwerkgegevens
description: Leer hoe u de synchronisatie van uw campagnestructuur en campagneentiteiten voor ondersteunde advertentienetwerken vanuit de nieuwe interface handmatig kunt activeren.
feature: Search Campaign Management
source-git-commit: 5e384445a35f81275eefeac660b31c1acdc785f3
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# (Nieuwe interface) Gegevens en netwerken handmatig synchroniseren via API-verbinding

<!-- EDIT ALL -- FROM LEGACY UI -->

*[!DNL Google Ads], [!DNL Microsoft Advertising] (voorheen [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads] , [!DNL Yandex] en alleen bestaande [!DNL Baidu] accounts*

De synchronisatie is het proces waardoor Onderzoek, Sociaal, &amp; Commerce bijgewerkte informatie voor de verbonden advertentienetwerkrekeningen van elke adverteerder op [&#x200B; gesteunde advertentienetwerken &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md) verzamelt. Deze gegevens omvatten de campagnestructuur en campagneentiteiten van de adverteerder, inclusief de meeste kenmerken die worden beheerd of gerapporteerd in Search, Social &amp; Commerce. Het omvat geen klikgegevens, noch biedingen en biedingsbepalingen ingegaan buiten Onderzoek, Sociale, &amp; Commerce, die afzonderlijk worden verzameld.

Zoeken, sociale media en Commerce synchroniseren (synchroniseren) automatisch met uw advertentienetwerkaccounts één keer per dag, en ook telkens wanneer een nieuwe campagne wordt gedetecteerd op een van uw advertentienetwerken. Bovendien verzendt het onmiddellijk alle veranderingen in campagnegegevens die van binnen Onderzoek, Sociale, &amp; Commerce aan het advertentienetwerk worden gemaakt.

U kunt synchronisatie van alle actieve en gepauzeerde campagnes in gespecificeerde rekeningen manueel verzoeken <!--Not available as of 2/23:  or in specific active and paused campaigns -->. Deze taak verzamelt entiteiten op het advertentienetwerk die nieuw of veranderd zijn.

Voor campagnes met &quot;[!UICONTROL Auto Update]&quot;optie, produceert de synchronisatieverrichting ook en post volgende codes die ontbreken of in het volgen malplaatjes of bestemmingsURLs moeten worden veranderd. De URL&#39;s worden gegenereerd volgens de parameters in de instellingen voor bijhouden van de accountinstellingen of campagne. Als er URL&#39;s voor het bijhouden van de relevante items bestaan, worden deze niet opnieuw gegenereerd, tenzij er nieuwe URL&#39;s nodig zijn (bijvoorbeeld als het trefwoordtype, de creatieve tekst of de parameters voor het bijhouden van de account zijn gewijzigd).

>[!NOTE]
>
>Telkens u [&#x200B; creeert een bulksheet &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md), kunt u naar keuze synchronisatie met het advertentienetwerk alvorens bulksheet wordt gecreeerd.

## Campagnes synchroniseren in een advertentienetwerkaccount

1. Klik in het hoofdmenu op **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** .

1. Schakel het selectievakje naast de accountnaam in.

   <!-- As of 2/23, you can sync only one acct at a time:  Select the check box next to each account or campaign that you want to sync. You can sync up to 50 campaigns at a time. If you sync more than five accounts at a time, the job is broken into batches of up to five accounts each. -->

1. Klik op de werkbalk voor bulkacties op **[!UICONTROL ... More Actions]** > **[!UICONTROL Sync]** .

   * Plaats de cursor boven de accountnaam, klik op **..** en klik vervolgens op **[!UICONTROL Edit]** .

U kunt de status van de synchronisatietaak volgen in de weergave [!UICONTROL Workspace] . De baan kan
een uur of meer om weer te geven.

>[!MORELIKETHIS]
>
>* [&#x200B; Download/creeer een bulksheet- dossier &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
