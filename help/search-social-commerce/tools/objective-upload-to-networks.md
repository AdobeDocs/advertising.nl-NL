---
title: Uploaden van doelstellingen naar advertentienetwerken inschakelen
description: Leer hoe je doelstellingen voor je hybride portfolio kunt uploaden naar [!DNL Google Ads] en [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 803f1ad2ad5be005b7dab467efbeb1c4ceaa7559
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# Uploaden van doelstellingen naar advertentienetwerken inschakelen

*Alleen adverteerders bij [!DNL Google Ads] en [!DNL Microsoft Advertising] accounts*

*Alleen adverteerders ingeschakeld voor hybride optimalisatie*

Zoeken, Social en Commerce kunnen de doelstellingen van de portfolio&#39;s van een adverteerderaccount uploaden naar [!DNL Google Ads] en [!DNL Microsoft Advertising] zodat je deze kunt gebruiken voor hybride optimalisatie. Uw geüploade doelstellingen zijn beschikbaar als conversieacties voor aangepaste conversiedoelen op account- en campagneniveau.

Als u deze optie inschakelt, wordt automatisch een upload geactiveerd voor doelstellingen in portfolio&#39;s die campagnes met slimme biedstrategieën bevatten. Search, Social en Commerce maakt een conversie op het advertentienetwerk voor elke toepasselijke doelstelling. De conversie vertegenwoordigt alle gewogen conversiestatistieken in de doelstelling. Elke conversie heeft een van de volgende namen:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  waarbij `<network_ID>` is de numerieke id die Search, Social en Commerce voor het advertentienetwerk gebruikt, `<objective_id>` de numerieke doel-id is en `<network_account_ID>` de numerieke id voor het advertentienetwerkaccount of het manageraccount.

* (Oude indeling die in de toekomst wordt vervangen) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  waar `<portfolio_id>` is de numerieke portefeuille-id en `<se_acctid/conversion_manager_se_acctid>` is de numerieke id voor het account of het beheeraccount van het advertentienetwerk.

  Uw Adobe-accountteam zal met u samenwerken om uw bestaande namen voor conversieacties binnen het advertentienetwerk te migreren voordat de oude indeling wordt verouderd. Tijdens de migratieperiode worden zowel de oude als de nieuwe uploads parallel uitgevoerd. Modellering en optimalisatie worden niet beïnvloed omdat de nieuwe omzettingsacties aanvankelijk met &quot;secundaire&quot; (niet geoptimaliseerde) status en met 90 dagen backfill gegevens verschijnen.

Uploads worden dagelijks om [!DNL Google Ads] 06:00 uur uitgevoerd in de tijdzone van de adverteerder. Uploads worden [!DNL Microsoft Advertising] dagelijks om 09:00 uur uitgevoerd in de tijdzone van de adverteerder.

>[!IMPORTANT]
>
>Conversies die worden bijgehouden door Google Ads en de UET-tag (Universal Event Tracking) van Microsoft Advertising, worden niet opnieuw geüpload naar de advertentienetwerken. Als u ze in een doelstelling opneemt, voegt u ze in de editor van het advertentienetwerk toe aan de campagnedoelen.

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Schakel het selectievakje naast **[!UICONTROL Enable Objective Upload]**.

1. (Adverteerders met [!DNL Google Ads] accounts die zaken doen in de Europese Economische Ruimte (EER) of het Verenigd Koninkrijk (VK); optioneel) Als je toestemming hebt verkregen van gebruikers van de EER of het Verenigd Koninkrijk om hun gegevens te uploaden voor advertentiedoeleinden, schakel dan het selectievakje naast **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klik op **[!UICONTROL Save]**.

1. (Als uw conversies worden bijgehouden op beheerdersaccountniveau) [Referenties toevoegen voor uw beheerdersaccount](/help/search-social-commerce/admin/manager-accounts.md) om **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Controleren of elke doelstelling — `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — verschijnt binnen twee dagen op het advertentienetwerk.

   In het dialoogvenster [!DNL Google Ads] editor, zoek uw [conversieacties](https://support.google.com/google-ads/answer/11461796). In het dialoogvenster [!DNL Microsoft Advertising] editor, zoek uw [conversiedoelen](https://help.ads.microsoft.com/#apex/ads/en/56709).

   Werk zo nodig het datumbereik bij en voeg de uploaddatum toe.

## Problemen met ontbrekende doelen oplossen

Als de doelstelling (genaamd `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` ) voor een van je portfolio&#39;s niet in het advertentienetwerk wordt weergegeven, controleer je het volgende:

* ([!DNL Google Ads]) Controleer of de conversies moeten worden geüpload naar account- of managerniveau. Als ze moeten worden geüpload op managerniveau:

   * Controleer of de aanmeldingsgegevens voor het [!DNL Google Ads] manageraccount zijn opgegeven op **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. Voeg zo [nodig de aanmeldingsgegevens voor het manageraccount](/help/search-social-commerce/admin/manager-accounts.md) toe.

   * Controleer of het advertentienetwerkaccount al dezelfde metrische naam heeft. Als dat het geval is, wijzigt u de naam van de metrische waarde, zodat de juiste eigenschap op managerniveau kan worden gemaakt.

* Controleer of de optie &quot;hybride&quot; van de portfolio is geselecteerd en of het doel geldige omzet heeft.

>[!MORELIKETHIS]
>
>* [Informatie over het beheren van conversiemetrieken van adverteerders](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Conversiemetrieken uploaden naar [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
