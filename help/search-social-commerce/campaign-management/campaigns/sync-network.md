---
title: Netwerkgegevens handmatig synchroniseren
description: Leer hoe u de synchronisatie van uw campagnestructuur en campagneentiteiten voor ondersteunde advertentienetwerken handmatig kunt activeren.
exl-id: da437f37-800a-4c56-b5c1-7c985ddd45c8
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Netwerkgegevens handmatig synchroniseren

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft® Advertising] (voorheen) [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], en [!DNL Yandex] alleen accounts*

De synchronisatie is het proces waardoor Onderzoek, Sociale, &amp; Handel bijgewerkte informatie voor de advertentienetwerkrekeningen van elke adverteerder over verzamelt [ondersteunde advertentienetwerken](/help/search-social-commerce/introduction/supported-inventory.md). Deze gegevens omvatten de campagnestructuur en de campagneentiteiten van de adverteerder, met inbegrip van de meeste attributen die in Onderzoek, Sociale, &amp; Handel worden beheerd of gerapporteerd. Het omvat geen klikgegevens, noch biedingen en biedingsbepalingen ingegaan buiten Onderzoek, Sociale, &amp; Handel, die afzonderlijk worden verzameld.

Zoek, Sociale, &amp; Handel synchroniseert (synchroniseert) automatisch met uw rekeningen van het advertentienetwerk eens per dag, en ook wanneer het een nieuwe campagne op één van uw advertentienetwerken ontdekt. Bovendien verzendt het onmiddellijk alle veranderingen in campagnegegevens die van binnen Onderzoek, Sociale, &amp; Handel aan het advertentienetwerk worden gemaakt.

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
