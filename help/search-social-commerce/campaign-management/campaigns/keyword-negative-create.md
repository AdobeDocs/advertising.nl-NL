---
title: Negatieve trefwoorden maken
description: Leer hoe u negatieve trefwoorden maakt voor zoekcampagnes en advertentiegroepen.
exl-id: afe786bf-eda8-4590-b471-3fb696c420de
feature: Search Campaign Management
source-git-commit: c2a1ce841a9dc99c57239f817dbd2065b91cdfb9
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Negatieve trefwoorden maken

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads]en bestaande [!DNL Baidu] alleen accounts*

U kunt negatieve sleutelwoorden voor een onderzoek en een groep of een campagne tot stand brengen die het onderzoek of de vertoning of het inheemse netwerk richten. Negatieve trefwoorden activeren geen advertenties.

>[!NOTE]
>U kunt ook negatieve trefwoorden maken en bewerken in het dialoogvenster [groepsinstellingen toevoegen](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) en [campagne-instellingen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

>[!TIP]
>Als u veel negatieve trefwoorden tegelijk wilt maken, gebruikt u [brochures](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]**.

1. Klik op de werkbalk boven de tabel met gegevens op ![Maken](/help/search-social-commerce/assets/add.png "Maken")en klik vervolgens op **[!UICONTROL Campaign]** om negatieve trefwoorden op campagnereniveau te maken of **[!UICONTROL Ad Group]** om negatieve trefwoorden op groepsniveau te maken.

1. Selecteer het advertentienetwerk, de account, de campagne en (indien van toepassing) de advertentiegroep en klik op **[!UICONTROL Continue]**.

1. Voer de negatieve trefwoorden in. Gebruik de volgende syntaxis, zonder een minteken (`-`):

   * Negatieve brede overeenkomst: `keyword` (wordt niet ondersteund door [!DNL Microsoft® Advertising])

   * Negatieve woordovereenkomst: `"keyword"`

   * Negatieve exacte overeenkomst: `[keyword]`

   Scheid meerdere waarden met komma&#39;s of voer deze op afzonderlijke regels in. U kunt maximaal 2000 negatieve trefwoorden in één bewerking invoeren of plakken. Zie ook de volgende vereisten en beperkingen:

   * Maximale tekenlengte: [!DNL Baidu]: 30 single-byte of 15 double-byte; [!DNL Microsoft® Advertising]: 100 single-byte of 50 double-byte; [!DNL Google Ads] en [!DNL Yahoo! Japan Ads]: 80 single-byte of 40 double-byte.

   * [!DNL Baidu] staat slechts één gelijke type per sleutelwoord per advertentiegroep toe. Groep 1 toevoegen kan bijvoorbeeld niet beide opnemen `"keyword"` en `[keyword]`.

   * [!DNL Google Ads]: Elk trefwoord mag uit maximaal 10 woorden bestaan en mag alleen letters, cijfers en de volgende speciale tekens bevatten: spatie `# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex]: Elk trefwoord mag maximaal zeven woorden bevatten, met uitzondering van stopwoorden. Elk [!DNL Yandex ad group] Kan maximaal 200 trefwoorden bevatten.

1. Klik op **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Trefwoorden](keyword-about.md)
>* [Biedeerbare trefwoorden beheren](keyword-manage.md)
>* [De status van trefwoorden en negatieve trefwoorden wijzigen](keyword-status-edit.md)
