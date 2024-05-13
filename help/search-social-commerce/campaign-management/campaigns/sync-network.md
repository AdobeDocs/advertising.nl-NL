---
title: Netwerkgegevens handmatig synchroniseren
description: Leer hoe u de synchronisatie van uw campagnestructuur en campagneentiteiten voor ondersteunde advertentienetwerken handmatig kunt activeren.
exl-id: 185c6a01-c2e8-4bbb-a9dd-0a8200eb4792
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Netwerkgegevens handmatig synchroniseren

*[!DNL Google Ads], [!DNL Microsoft Advertising] (voorheen) [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], [!DNL Yandex]en bestaande [!DNL Baidu] alleen accounts*

De synchronisatie is het proces waardoor Onderzoek, Sociaal, &amp; Commerce bijgewerkte informatie voor de verbonden advertentienetwerkrekeningen van elke adverteerder op verzamelt [ondersteunde advertentienetwerken](/help/search-social-commerce/introduction/supported-inventory.md). Deze gegevens omvatten de campagnestructuur en campagneentiteiten van de adverteerder, inclusief de meeste kenmerken die worden beheerd of gerapporteerd in Search, Social &amp; Commerce. Het omvat geen klikgegevens, noch biedingen en biedingsbepalingen ingegaan buiten Onderzoek, Sociale, &amp; Commerce, die afzonderlijk worden verzameld.

Zoeken, sociale media en Commerce synchroniseren (synchroniseren) automatisch met uw advertentienetwerkaccounts één keer per dag, en ook telkens wanneer een nieuwe campagne wordt gedetecteerd op een van uw advertentienetwerken. Bovendien verzendt het onmiddellijk alle veranderingen in campagnegegevens die van binnen Onderzoek, Sociale, &amp; Commerce aan het advertentienetwerk worden gemaakt.

U kunt handmatig verzoeken om synchronisatie van alle actieve en gepauzeerde campagnes in opgegeven accounts of in specifieke actieve en gepauzeerde campagnes. Deze taak verzamelt entiteiten op het advertentienetwerk die nieuw of veranderd zijn.

Voor campagnes met de &quot;[!UICONTROL Auto Upload]&quot;, genereert de synchronisatiebewerking ook trackingcodes die ontbreken of moeten worden gewijzigd in de trackingsjablonen of doel-URL&#39;s. De URL&#39;s worden gegenereerd volgens de parameters in de instellingen voor bijhouden van de accountinstellingen of campagne. Als er URL&#39;s voor het bijhouden van de relevante items bestaan, worden deze niet opnieuw gegenereerd, tenzij er nieuwe URL&#39;s nodig zijn (bijvoorbeeld als het trefwoordtype, de creatieve tekst of de parameters voor het bijhouden van de account zijn gewijzigd).

>[!NOTE]
>
>Altijd [een werkblad maken](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)U kunt desgewenst synchroniseren met het advertentienetwerk voordat het bulksblad wordt gemaakt.

1. Klik in het hoofdmenu op **[!UICONTROL Search]>[!UICONTROL Campaigns]**. Selecteer in het submenu een van de **[!UICONTROL Accounts]** om alle campagnes in specifieke rekeningen te synchroniseren of **[!UICONTROL Campaigns]** specifieke campagnes synchroniseren.

1. (Optioneel) Filter de lijst om specifieke accounts of campagnes op te nemen.

1. Schakel het selectievakje in naast elke account of campagne die u wilt synchroniseren. U kunt maximaal 50 campagnes tegelijk synchroniseren. Als u meer dan vijf accounts tegelijk synchroniseert, wordt de taak opgedeeld in batches van maximaal vijf accounts.

1. Klikken **![Meer](/help/search-social-commerce/assets/more.png "Meer")** in de werkbalk en selecteert u vervolgens **[!UICONTROL Sync]**.

U kunt de status van de synchronisatietaak volgen in het dialoogvenster [!UICONTROL Workspace] weergeven. Het kan een uur of langer duren voordat de taak wordt weergegeven.

>[!MORELIKETHIS]
>
>* [Een bulkbladbestand downloaden/maken](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
