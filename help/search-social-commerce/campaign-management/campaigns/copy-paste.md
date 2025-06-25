---
title: Campagne-gegevens bulksgewijs maken en bewerken met kopiëren en plakken
description: Leer hoe u campagnegegevens bulksgewijs kunt beheren met de functie Kopiëren en plakken.
exl-id: 2ae1b02f-46ac-4ea8-aa9f-9e26ccaf63d0
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Campagne-gegevens bulksgewijs maken en bewerken met kopiëren en plakken

*[!DNL Google Ads], [!DNL Microsoft Advertising] , [!DNL Yahoo! Japan Ads] , [!DNL Yandex] en alleen bestaande [!DNL Baidu] accounts*

*[!UICONTROL Campaigns], [!UICONTROL Ad Groups] , [!UICONTROL Keywords] en [!UICONTROL Ads] views*

U kunt maximaal 10.000 rijen uit de weergaven [!UICONTROL Campaigns] , [!UICONTROL Ad Groups] , [!UICONTROL Keywords] en [!UICONTROL Ads] kopiëren en deze in [!DNL Microsoft Excel] of een andere editor plakken om niet-id-velden te bewerken. Vervolgens kunt u de [!DNL Excel] -rijen kopiëren en deze als tabgescheiden gegevens weer in de weergave plakken om de wijzigingen aan te brengen. De functie gebruikt het klembord van uw computer.

Met deze functie kunt u bestaande campagneobjecten (met id-velden) bewerken en nieuwe campagneobjecten zonder id-velden maken.

## Gegevensrijen kopiëren

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** . Klik in de submenu&#39;s op **[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads] \]**.

1. Schakel het selectievakje in naast elke rij die u wilt kopiëren.

   U kunt maximaal 10.000 rijen kopiëren.

1. In de toolbar boven de gegevenslijst, klik ![ Meer ](/help/search-social-commerce/assets/more.png " "), en klik dan **[!UICONTROL Copy]**.

   U kunt ook de toetsenbordopdracht &#39;copy&#39; van uw besturingssysteem gebruiken, zoals **[!DNL Ctrl+C]** for [!DNL Microsoft Windows] of **[!DNL Command-C]** for [!DNL Apple Mac] .

1. Klik in het dialoogvenster [!UICONTROL Copy to Clipboard] op **[!UICONTROL Continue]** . Klik op **[!UICONTROL Copy]** wanneer de gegevens gereed zijn om te kopiëren.

1. Plak de rijen in [!DNL Excel] of een andere editor.

## Gegevensrijen bewerken en maken

1. Bewerk de gegevens volgens de volgende vereisten:

   * De geplakte gegevens moeten een koptekstrij en de noodzakelijke campagneobjecten waarden omvatten; zie de vereiste bulksemolommen voor [ Baidu ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [ Google Adds ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [ Microsoft Advertising ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [ Navigator ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [ Yahoo! Het Netwerk van de vertoning ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md), [ Yahoo! Japan ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md), en [ Yandex ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md). De kolomvolgorde is niet van belang.

      * Voor bestaande objecten die u wilt bewerken, moet u alle relevante ID-kolommen, entiteitsnamen en het kenmerk dat u wilt bewerken opnemen. Bewerk de numerieke id van het object niet.

      * Voor nieuwe campagneobjecten neemt u alle relevante entiteitsnamen en -kenmerken op, maar niet de object-id&#39;s (die automatisch worden gegenereerd). Als u bijvoorbeeld een nieuwe advertentie maakt, laat u het veld [!UICONTROL Ad ID] leeg. Het ad-netwerk maakt automatisch een id wanneer u het object plaatst.

   * De waarde in een niet-verplichte kolom mag null (leeg) zijn, maar elke rij moet hetzelfde aantal waarden met tabs als scheidingsteken hebben.

1. Sla de gegevens op als door tabs gescheiden waarden.

## Gegevensrijen plakken in de weergaven van het campagnebeheer

>[!NOTE]
>
>Als de geplakte rijen gegevens bevatten die identiek zijn aan die in de bestaande entiteiten of die een bestaande entiteit dupliceren, worden de dubbele gegevens genegeerd.

1. Kopieer in [!DNL Excel] of een andere editor de relevante rijen met tabs als scheidingsteken.

1. Klik in het hoofdmenu Zoeken, Sociaal en Commerce op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** . De weergave openen waarin gegevens moeten worden geplakt (**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \|) [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads] \]**).

1. In de toolbar boven de gegevenslijst, klik ![ Meer ](/help/search-social-commerce/assets/more.png " "), en klik dan **[!UICONTROL Paste]**.

   U kunt ook de toetsenbordopdracht &quot;plakken&quot; van uw besturingssysteem gebruiken, zoals **[!DNL Ctrl+V]** for [!DNL Microsoft Windows] of **[!DNL Command-V]** for [!DNL Apple Mac] .

1. Plak de gegevens in het invoervak en klik op **[!UICONTROL Process]** .

1. (Optioneel) Voer aanvullende gegevens in:

   * (Als **[!UICONTROL Additional Details]** wordt samengeperst) klik ![ Open ](/help/search-social-commerce/assets/chevron-up.png " Open ") om de details uit te breiden.

   * Voer een optionele **[!UICONTROL Job Name]** en/of optionele **[!UICONTROL Job Description]** in.

1. Klik op **[!UICONTROL Post Now]**.


>[!MORELIKETHIS]
>
>* [ Ongeveer het beheren van campagnegegevens gebruikend bulksbladen ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [ geef montages direct binnen een rij ](/help/search-social-commerce/common-tasks/settings-edit-within-row.md) uit
>* [ beheert campagnes ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [ beheer en groepen ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [ beheert sleutelwoorden ](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [ beheert advertenties ](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
