---
title: Uploaden van doelstellingen naar en netwerken inschakelen
description: Leer hoe u doelstellingen voor uw hybride portfolio's kunt uploaden naar [!DNL Google Ads] en [!DNL Microsoft® Advertising].
exl-id: 75a1a804-ad6a-4dbc-9cde-30fe54476162
feature: Search Tools
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# Uploaden van doelstellingen naar en netwerken inschakelen

*Adverteerders met [!DNL Google Ads] en [!DNL Microsoft® Advertising] alleen accounts*

*Adverteerders alleen ingeschakeld voor hybride optimalisatie*

Als uw adverteerderaccount is geconfigureerd voor hybride optimalisatie, kan Adobe Advertising optioneel de doelstellingen voor de portfolio&#39;s van de account uploaden naar [!DNL Google Ads] en [!DNL Microsoft® Advertising] als omzettingen zodat kunt u hen voor hybride optimalisering gebruiken.

Als u deze optie inschakelt, wordt automatisch een upload gestart voor portfolio&#39;s die campagnes met slimme biedstrategieën bevatten. Met Zoeken, Sociaal en Handel wordt een conversie op het advertentienetwerk gemaakt voor elke toepasselijke combinatie van portfolio en doel. Elke conversie heeft de naam `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`, waarbij `<portfolio_id>` is de numerieke portefeuille-id en `<se_acctid/conversion_manager_se_acctid>` is de numerieke id voor de account of het beheerdersaccount van het advertentienetwerk. De conversie vertegenwoordigt alle gewogen transactieeigenschappen in de doelstelling.

Uploads naar [!DNL Google Ads] komt dagelijks om 6.00 uur voor in de tijdzone van de adverteerder. Uploads naar [!DNL Microsoft® Advertising] komt dagelijks om 9.00 uur voor in de tijdzone van de adverteerder.

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Schakel het selectievakje in naast **[!UICONTROL Enable Objective Upload]**.

   Deze optie is alleen beschikbaar als uw adverteerderaccount is geconfigureerd voor gebruik van hybride optimalisatie. Neem contact op met uw Adobe-accountteam om hybride optimalisatie in te schakelen.

1. Klik op **[!UICONTROL Save]**.

1. (Als uw conversies worden bijgehouden op het niveau van een beheerdersaccount) [Referenties toevoegen voor uw beheerdersaccount](/help/search-social-commerce/admin/manager-accounts.md) om **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Informatie over het beheren van de transactieeigenschappen van een adverteerder](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md)
>* [Conversiemetriek uploaden naar [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
