---
title: Uploaden van doelstellingen naar en netwerken inschakelen
description: Leer hoe u doelstellingen voor uw hybride portfolio's kunt uploaden naar [!DNL Google Ads] en [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: aaad3eb6cd33f4342c46ffb244227a00fbcb4e44
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 0%

---

# Uploaden van doelstellingen naar en netwerken inschakelen

*Adverteerders met [!DNL Google Ads] en [!DNL Microsoft Advertising] alleen accounts*

*Adverteerders alleen ingeschakeld voor hybride optimalisatie*

Met Zoeken, Sociaal en Commerce kunt u de doelstellingen voor de portfolio&#39;s van een advertentieaccount uploaden naar [!DNL Google Ads] en [!DNL Microsoft Advertising] zodat kunt u ze gebruiken voor hybride optimalisatie. De geüploade doelstellingen zijn beschikbaar als conversieacties voor aangepaste conversiedoelstellingen op accountniveau en op campagnereniveau.

Als u deze optie inschakelt, wordt er automatisch een upload uitgevoerd naar doelstellingen in portfolio&#39;s die campagnes met slimme biedstrategieën bevatten. Met Zoeken, Sociaal en Commerce maakt u een conversie op het advertentienetwerk voor elke toepasselijke doelstelling. De omzetting vertegenwoordigt alle gewogen omzettingsmetriek in het doel op EF ID (klik identiteitskaart) niveau. Voor [!DNL Google Ads] klikt, EF identiteitskaart is [!DNL Google Ads] `gclid`; for [!DNL Microsoft Advertising] klikt, EF identiteitskaart is [!DNL Microsoft Advertising] `msclkid`. Vanwege deze klik-id kunnen conversiegegevens worden toegewezen aan het specifieke trefwoord en de kliktijd.

Elke geüploade conversie heeft een van de volgende namen:

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  waar `<network_ID>` is de numerieke id die Search, Social &amp; Commerce gebruikt voor het advertentienetwerk. `<objective_id>` de numerieke doelstelling-id is, en `<network_account_ID>` is de numerieke id voor de account of het beheerdersaccount van het advertentienetwerk.

* (Oude indeling die in de toekomst wordt vervangen) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  waar `<portfolio_id>` is de numerieke portefeuille-id en `<se_acctid/conversion_manager_se_acctid>` is de numerieke id voor de account of het beheerdersaccount van het advertentienetwerk.

  Uw accountteam van de Adobe werkt met u samen om uw bestaande namen van conversieacties binnen het advertentienetwerk te migreren voordat de oude indeling wordt vervangen. Tijdens de migratieperiode worden zowel de oude als de nieuwe uploads parallel uitgevoerd. Modellering en optimalisatie worden niet beïnvloed omdat de nieuwe omzettingsacties aanvankelijk met &quot;secundaire&quot; (niet geoptimaliseerde) status en met 90 dagen backfill gegevens verschijnen.

Uploads naar [!DNL Google Ads] komt dagelijks om 6.00 uur voor in de tijdzone van de adverteerder. Uploads naar [!DNL Microsoft Advertising] komt dagelijks om 9.00 uur voor in de tijdzone van de adverteerder.

>[!IMPORTANT]
>
>Conversies die worden bijgehouden door Google Ads en de tag Universal Event tracking (UET) van Microsoft Advertising worden niet opnieuw geüpload naar de advertentienetwerken. Als u hen binnen een doelstelling omvat, moet u hen aan de campagnedoelstellingen binnen de redacteur van het advertentienetwerk toevoegen.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Schakel het selectievakje in naast **[!UICONTROL Enable Objective Upload]**.

1. (Adverteerders met [!DNL Google Ads] accounts die zaken doen in de Europese Economische Ruimte (EER) of het Verenigd Koninkrijk (VK); facultatief) Als u toestemming van gebruikers in de EER en het VK hebt verzameld om hun gegevens voor reclamedoeleinden te uploaden, schakelt u het selectievakje naast **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klik op **[!UICONTROL Save]**.

1. (Als uw conversies worden bijgehouden op het niveau van een beheerdersaccount) [Referenties toevoegen voor uw beheerdersaccount](/help/search-social-commerce/admin/manager-accounts.md) om **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. Controleren of elke doelstelling — met naam `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — verschijnt binnen twee dagen op het advertentienetwerk.

   In de [!DNL Google Ads] editor, opzoeken [conversiehandelingen](https://support.google.com/google-ads/answer/11461796). In de [!DNL Microsoft Advertising] editor, opzoeken [conversiedoelstellingen](https://help.ads.microsoft.com/#apex/ads/en/56709).

   Werk indien nodig het datumbereik bij en voeg de uploaddatum toe.

## Hoe de gewogen doelstelling wordt berekend

Het gewogen doel dat tot het advertentienetwerk wordt overgegaan is de som alle metrische waarden die, met uitzondering van omzettingen worden verzameld die door [!DNL Google Ads] of door de [!DNL Microsoft Advertising] Label voor Universal Event tracking (UET). De waarde wordt berekend met de toewijzingsmethode die is ingesteld voor de account Zoeken, Sociaal en Commerce van de adverteerder.

Stel dat het doel van de doelstelling metrisch is met Cart Additions met een gewicht van 25 en dat uw maateenheden voor assistentie GL_Lead en Revenue met gewichten van 1 en Downloads met een gewicht van 0,5 zijn.

![Voorbeeld van een gewogen doelstelling](/help/search-social-commerce/assets/objective-example.png "Voorbeeld van een gewogen doelstelling")

Stel dat een trefwoord resulteert in de volgende handelingen voor het portfolio:

* 10 extra winkelwagentjes
* 500 dollar aan inkomsten
* 50 downloads
* 5 GGL_Lead

GGL_Lead wordt niet opgenomen in de berekening/upload omdat het een metrische waarde is die door Google Ads wordt bijgehouden. Daarom wordt de gewogen objectieve waarde berekend als ((10 x 25) + (500 x 1) + (50 x 0,5)) = 775.

>[!TIP]
>
>U kunt gegevens voor Adobe Advertising gewogen opbrengst binnen de rapporten van het advertentienetwerk bekijken. Als beste praktijk, vergelijk de gewogen opbrengst met [!DNL Google Ads] &quot;Alle conv. (door conv. time)&quot; metrisch of de [!DNL Microsoft Advertising] metrische &quot;All conv. opbrengst,&quot;gesegmenteerd aan metrisch O_ACS_OBJ*.<!--clarify -->

in de editor van het advertentienetwerk

## Problemen met ontbrekende doelstellingen oplossen

Indien het doel `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — voor een van uw portfolio&#39;s wordt niet weergegeven op het advertentienetwerk, controleert u het volgende:

* ([!DNL Google Ads]) Controleer of de conversies moeten worden geüpload naar het account- of beheerniveau. Als ze op managementniveau moeten worden geüpload:

   * Controleer of de referenties voor de [!DNL Google Ads] beheerdersaccount is beschikbaar op **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. Indien nodig [Voeg de geloofsbrieven voor de managerrekening toe](/help/search-social-commerce/admin/manager-accounts.md).

   * Controleer of de netwerkaccount voor advertenties al dezelfde metrische naam bevat. Als het, dan metrisch anders noemt zodat het correcte manager-vlakke bezit kan worden gecreeerd.

* Controleer of de optie &quot;hybride&quot; van de portefeuille is geselecteerd en of de doelstelling geldige opbrengsten heeft.

>[!MORELIKETHIS]
>
>* [Informatie over het beheren van conversiegegevens van adverteerders](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [Conversiemetriek uploaden naar [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
