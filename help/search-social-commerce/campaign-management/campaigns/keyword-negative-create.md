---
title: Negatieve trefwoorden maken
description: Leer hoe u negatieve trefwoorden maakt voor zoekcampagnes en advertentiegroepen.
exl-id: afe786bf-eda8-4590-b471-3fb696c420de
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Negatieve trefwoorden maken

*[!DNL Google Ads], [!DNL Microsoft Advertising] , [!DNL Yahoo! Japan Ads] en alleen bestaande [!DNL Baidu] accounts*

U kunt negatieve sleutelwoorden voor een onderzoek en een groep of een campagne tot stand brengen die het onderzoek of de vertoning of het inheemse netwerk richten. Negatieve trefwoorden activeren geen advertenties.

>[!NOTE]
>U kunt negatieve sleutelwoorden in [ ook creëren en uitgeven en groepsmontages ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) en [ campagnemontages ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

>[!TIP]
>Om vele negatieve sleutelwoorden in één keer tot stand te brengen, gebruik [ campagnebulksheets ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** . Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]** .

1. In de toolbar boven de gegevenslijst, creeert de klik ![&#128279;](/help/search-social-commerce/assets/add.png " "), en klikt dan **[!UICONTROL Campaign]** om campagne-vlakke negatieve sleutelwoorden tot stand te brengen of **[!UICONTROL Ad Group]** om negatieve sleutelwoorden op ad-niveau tot stand te brengen.

1. Selecteer het advertentienetwerk, de account, de campagne en (indien van toepassing) de advertentiegroep en klik op **[!UICONTROL Continue]** .

1. Voer de negatieve trefwoorden in. Gebruik de volgende syntaxis, zonder een minteken (`-`):

   * Negatieve brede overeenkomst: `keyword` (wordt niet ondersteund door [!DNL Microsoft Advertising])

   * Negatieve woordgroep komt overeen: `"keyword"`

   * Negatieve exacte overeenkomst: `[keyword]`

   Scheid meerdere waarden met komma&#39;s of voer deze op afzonderlijke regels in. U kunt maximaal 2000 negatieve trefwoorden in één bewerking invoeren of plakken. Zie ook de volgende vereisten en beperkingen:

   * Maximale tekenlengte: [!DNL Baidu]: 30 single-byte of 15 double-byte; [!DNL Microsoft Advertising]: 100 single-byte of 50 double-byte; [!DNL Google Ads] en [!DNL Yahoo! Japan Ads]: 80 single-byte of 40 double-byte.

   * [!DNL Baidu] staat slechts één gelijke type per sleutelwoord per ad groep toe. Advertentiegroep 1 kan bijvoorbeeld niet zowel `"keyword"` als `[keyword]` bevatten.

   * [!DNL Google Ads]: elk trefwoord mag uit maximaal 10 woorden bestaan en mag alleen letters, cijfers en de volgende speciale tekens bevatten: spatie `# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex]: elk trefwoord kan maximaal zeven woorden hebben, met uitzondering van stopwoorden. Elke [!DNL Yandex ad group] kan maximaal 200 trefwoorden bevatten.

1. Klik op **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [ Ongeveer sleutelwoorden ](keyword-about.md)
>* [ beheert biddable sleutelwoorden ](keyword-manage.md)
>* [ Verandering het statuut van sleutelwoorden en negatieve sleutelwoorden ](keyword-status-edit.md)
