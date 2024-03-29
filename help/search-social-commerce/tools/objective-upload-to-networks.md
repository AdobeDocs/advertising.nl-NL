---
title: Uploaden van doelstellingen naar en netwerken inschakelen
description: Leer hoe u doelstellingen voor uw hybride portfolio's kunt uploaden naar [!DNL Google Ads] en [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: e8eabf7e4aa7c9201cd8198aae32d325b2858f2b
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Uploaden van doelstellingen naar en netwerken inschakelen

*Adverteerders met [!DNL Google Ads] en [!DNL Microsoft® Advertising] alleen accounts*

*Adverteerders alleen ingeschakeld voor hybride optimalisatie*

Als uw adverteerderaccount is geconfigureerd voor hybride optimalisatie, kan Adobe Advertising optioneel de doelstellingen voor de portfolio&#39;s van de account uploaden naar [!DNL Google Ads] en [!DNL Microsoft® Advertising] als omzettingen zodat kunt u hen voor hybride optimalisering gebruiken.

Als u deze optie inschakelt, wordt automatisch een upload gestart voor portfolio&#39;s die campagnes met slimme biedstrategieën bevatten. Met Zoeken, Sociaal en Handel wordt een conversie op het advertentienetwerk gemaakt voor elke toepasselijke combinatie van portfolio en doel. Elke conversie heeft de naam `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`, waarbij `<portfolio_id>` is de numerieke portefeuille-id en `<se_acctid/conversion_manager_se_acctid>` is de numerieke id voor de account of het beheerdersaccount van het advertentienetwerk. De conversie vertegenwoordigt alle gewogen conversiemetriek in het doel.

Uploads naar [!DNL Google Ads] komt dagelijks om 6.00 uur voor in de tijdzone van de adverteerder. Uploads naar [!DNL Microsoft® Advertising] komt dagelijks om 9.00 uur voor in de tijdzone van de adverteerder.

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Schakel het selectievakje in naast **[!UICONTROL Enable Objective Upload]**.

   Deze optie is alleen beschikbaar als uw adverteerderaccount is geconfigureerd voor gebruik van hybride optimalisatie. Neem contact op met het accountteam van de Adobe om hybride optimalisatie in te schakelen.

1. (Adverteerders met [!DNL Google Ads] accounts die zaken doen in de Europese Economische Ruimte (EER) of het Verenigd Koninkrijk (VK); facultatief) Als u toestemming van gebruikers in de EER en het VK hebt verzameld om hun gegevens voor reclamedoeleinden te uploaden, schakelt u het selectievakje naast **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klik op **[!UICONTROL Save]**.

1. (Als uw conversies worden bijgehouden op het niveau van een beheerdersaccount) [Referenties toevoegen voor uw beheerdersaccount](/help/search-social-commerce/admin/manager-accounts.md) om **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Informatie over het beheren van conversiegegevens van adverteerders](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Conversiemetriek uploaden naar [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
