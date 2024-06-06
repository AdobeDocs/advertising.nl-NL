---
title: Referenties beheren voor accounts van ad-netwerkbeheerders
description: Leer hoe u uw aanmeldingsgegevens kunt opgeven [!DNL Google Ads] beheeraccounts.
exl-id: 95866a2e-4695-4b1d-ac23-844d3b9a0a74
feature: Search Admin
source-git-commit: 4cf04fc7ea22e50b5f56cd278ad9a1aac724edf7
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 1%

---

# Referenties beheren voor accounts van ad-netwerkbeheerders

*[!DNL Google Ads]alleen accounts*

Geef de referenties op voor uw [!DNL Google Ads] Beheerdersaccounts waarnaar u conversies via verschillende accounts wilt uploaden via Zoeken, Sociaal en Commerce. Gebruik deze functie als u een upload wilt uitvoeren [!DNL Adobe]-tracked, cross-account conversie metrics naar a [!DNL Google Ads] de rekening van de manager of b) uploadt portefeuilledoelstellingen die dwars-rekeningsomzettingen in [!DNL Google Ads] voor hybride optimalisatie.

<!-- [Maybe later: and c) sync conversion value rules for accounts that use cross-account conversion tracking with Google Ads.] -->

U kunt geloofsbrieven voor nieuwe verslagen van de managerrekening toevoegen, of een bestaande managerrekening opnieuw voor authentiek verklaren.

Nadat u referenties voor een beheerdersaccount hebt toegevoegd, wordt de id van de gekoppelde beheeraccount als alleen-lezen weergegeven in de accountinstellingen. Daarnaast is een optionele &quot;[!UICONTROL Manager Account for Cross-Account Conversions]&quot; in de [!UICONTROL Campaigns] > [!UICONTROL Accounts] de mening toont managerrekening ID voor elke kindrekening en wijst op een fout wanneer de managerrekening niet voor authentiek wordt verklaard. [!UICONTROL Notification Center] bevat meldingen wanneer de referenties van een beheerdersaccount ontbreken ([de [!UICONTROL Manager Account Missing Error]](/help/search-social-commerce/notifications/notification-about.md)) of wanneer een beheerdersaccountverificatietoken verloopt ([de [!UICONTROL Manager Account Auth Error]](/help/search-social-commerce/notifications/notification-about.md)).

## Om geloofsbrieven voor een nieuwe managerrekening toe te voegen

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Selecteren **[!UICONTROL Create new manager account]**.

1. Geef aanmeldingsgegevens voor de beheerdersaccount op.

   De **[!UICONTROL Manager Account ID]** en **[!UICONTROL Login Email]** zijn vereist. Met Zoeken, Sociaal en Commerce wordt het accounttoken automatisch vastgelegd en opgeslagen voor verificatie.

   U kunt desgewenst een **[!UICONTROL MCC Account Name]** voor identificatie binnen Search, Social &amp; Commerce en de account **[!UICONTROL Password]**. Voer het wachtwoord in wanneer u het wilt versleutelen en sla het op zodat de accountmanager de tokens naar behoefte kan vernieuwen.

1. Klik op **[!UICONTROL Authenticate]**.

1. Klik op **[!UICONTROL Save]**.

## Een bestaande beheerdersaccount opnieuw verifiëren

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Selecteren **[!UICONTROL Reauthenticate existing manager account]**.

1. Selecteer de beheerdersaccount.

1. Geef aanmeldingsgegevens voor de beheerdersaccount op.

   De **[!UICONTROL Manager Account ID]** en **Aanmeldingsbericht** zijn vereist. Met Zoeken, Sociaal en Commerce wordt het accounttoken automatisch vastgelegd en opgeslagen voor verificatie.

   U kunt desgewenst een **[!UICONTROL MCC Account Name]** voor identificatie binnen Search, Social &amp; Commerce en de account **[!UICONTROL Password]**. Voer het wachtwoord in wanneer u het wilt versleutelen en sla het op zodat de accountmanager de tokens naar behoefte kan vernieuwen.

1. Klik op **[!UICONTROL Authenticate]**.

1. Klik op **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Uploaden van doelstellingen naar en netwerken inschakelen](/help/search-social-commerce/tools/objective-upload-to-networks.md)
>* [Conversiemetriek uploaden naar [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
>* [Uw meldingsinstellingen bewerken](/help/search-social-commerce/notifications/notification-edit.md)
