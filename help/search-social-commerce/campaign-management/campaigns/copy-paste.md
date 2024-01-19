---
title: Campagne-gegevens bulksgewijs maken en bewerken met kopiëren en plakken
description: Leer hoe u campagnegegevens bulksgewijs kunt beheren met de functie Kopiëren en plakken.
exl-id: 2ae1b02f-46ac-4ea8-aa9f-9e26ccaf63d0
feature: Search Campaign Management
source-git-commit: c2a1ce841a9dc99c57239f817dbd2065b91cdfb9
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Campagne-gegevens bulksgewijs maken en bewerken met kopiëren en plakken

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex]en bestaande [!DNL Baidu] alleen accounts*

*[!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] views*

U kunt maximaal 10.000 rijen kopiëren uit de [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] weergaven, en deze plakken in [!DNL Microsoft Excel] of een andere editor om niet-id-velden te bewerken. U kunt vervolgens de [!DNL Excel] Hiermee kunt u de wijzigingen aanbrengen en deze als tabgescheiden gegevens weer in de weergave plakken. De functie gebruikt het klembord van uw computer.

Met deze functie kunt u bestaande campagneobjecten (met id-velden) bewerken en nieuwe campagneobjecten zonder id-velden maken.

## Gegevensrijen kopiëren

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klik in de submenu&#39;s op **[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**.

1. Schakel het selectievakje in naast elke rij die u wilt kopiëren.

   U kunt maximaal 10.000 rijen kopiëren.

1. Klik op de werkbalk boven de tabel met gegevens op ![Meer](/help/search-social-commerce/assets/more.png "Meer")en klik vervolgens op **[!UICONTROL Copy]**.

   U kunt ook de &quot;copy&quot;-toetsenbordopdracht van uw besturingssysteem gebruiken, zoals **[!DNL Ctrl+C]** for [!DNL Microsoft Windows] of **[!DNL Command-C]** for [!DNL Apple Mac].

1. In de [!UICONTROL Copy to Clipboard] dialoogvenster, klikt u op **[!UICONTROL Continue]**. Wanneer de gegevens klaar zijn om te worden gekopieerd, klikt u op **[!UICONTROL Copy]**.

1. De rijen plakken in [!DNL Excel] of een andere editor.

## Gegevensrijen bewerken en maken

1. Bewerk de gegevens volgens de volgende vereisten:

   * De geplakte gegevens moeten een koptekstrij en de vereiste campagneobjectwaarden bevatten; zie de vereiste bulksbladkolommen voor [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Adds](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo! Netwerk weergeven](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md), [Yahoo! Japan](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md), en [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md). De kolomvolgorde is niet van belang.

      * Voor bestaande objecten die u wilt bewerken, moet u alle relevante ID-kolommen, entiteitsnamen en het kenmerk dat u wilt bewerken opnemen. Bewerk de numerieke id van het object niet.

      * Voor nieuwe campagneobjecten neemt u alle relevante entiteitsnamen en -kenmerken op, maar niet de object-id&#39;s (die automatisch worden gegenereerd). Als u bijvoorbeeld een nieuwe advertentie maakt, laat u de knop [!UICONTROL Ad ID] veld leeg. Het ad-netwerk maakt automatisch een id wanneer u het object plaatst.

   * De waarde in een niet-verplichte kolom mag null (leeg) zijn, maar elke rij moet hetzelfde aantal waarden met tabs als scheidingsteken hebben.

1. Sla de gegevens op als door tabs gescheiden waarden.

## Gegevensrijen plakken in de weergaven van het campagnebeheer

>[!NOTE]
>
>Als de geplakte rijen gegevens bevatten die identiek zijn aan die in de bestaande entiteiten of die een bestaande entiteit dupliceren, worden de dubbele gegevens genegeerd.

1. In [!DNL Excel] of een andere editor, kopieert u de relevante rijen met tabs als scheidingsteken.

1. Klik in het hoofdmenu Zoeken, Sociaal en Handel op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. De weergave openen waarin gegevens moeten worden geplakt (**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**).

1. Klik op de werkbalk boven de tabel met gegevens op ![Meer](/help/search-social-commerce/assets/more.png "Meer")en klik vervolgens op **[!UICONTROL Paste]**.

   U kunt ook de toetsenbordopdracht &quot;plakken&quot; van het besturingssysteem gebruiken, zoals **[!DNL Ctrl+V]** for [!DNL Microsoft Windows] of **[!DNL Command-V]** for [!DNL Apple Mac].

1. Plak de gegevens in het invoervak en klik vervolgens op **[!UICONTROL Process]**.

1. (Optioneel) Voer aanvullende gegevens in:

   * (Als **[!UICONTROL Additional Details]** is gecomprimeerd) Klik op ![Openen](/help/search-social-commerce/assets/chevron-up.png "Openen") om de details uit te breiden.

   * Voer een optionele **[!UICONTROL Job Name]** en/of facultatief **[!UICONTROL Job Description]**.

1. Klik op **[!UICONTROL Post Now]**.


>[!MORELIKETHIS]
>
>* [Campagnegegevens beheren met behulp van bulksbladen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [Instellingen rechtstreeks in een rij bewerken](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [Campagnes beheren](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [Adroepen beheren](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [Trefwoorden beheren](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [Advertenties beheren](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
