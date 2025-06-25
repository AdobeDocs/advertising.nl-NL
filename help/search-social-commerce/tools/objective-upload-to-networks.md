---
title: Uploaden van doelstellingen naar en netwerken inschakelen
description: Leer hoe te om doelstellingen voor uw hybride portefeuilles aan  [!DNL Google Ads]  en  [!DNL Microsoft Advertising] te uploaden.
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Uploaden van doelstellingen naar en netwerken inschakelen

*Advertisers met [!DNL Google Ads] en [!DNL Microsoft Advertising] slechts rekeningen*

*Advertisers die voor hybride slechts optimalisering worden toegelaten*

Met Zoeken, Sociaal en Commerce kunt u de doelstellingen voor de portfolio&#39;s van een advertentieaccount uploaden naar [!DNL Google Ads] en [!DNL Microsoft Advertising] , zodat u deze kunt gebruiken voor hybride optimalisatie. De geüploade doelstellingen zijn beschikbaar als conversieacties voor aangepaste conversiedoelstellingen op accountniveau en op campagnereniveau.

Als u deze optie inschakelt, wordt er automatisch een upload uitgevoerd naar doelstellingen in portfolio&#39;s die campagnes met slimme biedstrategieën bevatten. Met Zoeken, Sociaal en Commerce maakt u een conversie op het advertentienetwerk voor elke toepasselijke doelstelling. De omzetting vertegenwoordigt alle gewogen omzettingsmetriek in het doel op EF ID (klik identiteitskaart) niveau. Voor [!DNL Google Ads] klikken is de EF-id de [!DNL Google Ads] `gclid` ; voor [!DNL Microsoft Advertising] klikken is de EF-id de [!DNL Microsoft Advertising] `msclkid` . Vanwege deze klik-id kunnen conversiegegevens worden toegewezen aan het specifieke trefwoord en de kliktijd.

Elke geüploade conversie heeft de volgende naam:

`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

waarbij `<network_ID>` de numerieke id is die door Search, Social en Commerce wordt gebruikt voor het advertentienetwerk, is `<objective_id>` de numerieke objectieve id en is `<network_account_ID>` de numerieke id voor de account of het beheerdersaccount van het advertentienetwerk.

Uploads naar [!DNL Google Ads] vinden dagelijks plaats om 6:00 uur in de tijdzone van de adverteerder. Uploads naar [!DNL Microsoft Advertising] vinden dagelijks plaats om 9:00 uur in de tijdzone van de adverteerder.

>[!IMPORTANT]
>
>Conversies die worden bijgehouden door Google Ads en de tag Universal Event tracking (UET) van Microsoft Advertising worden niet opnieuw geüpload naar de advertentienetwerken. Als u hen binnen een doelstelling omvat, moet u hen aan de campagnedoelstellingen binnen de redacteur van het advertentienetwerk toevoegen.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]** .

1. Schakel het selectievakje naast **[!UICONTROL Enable Objective Upload]** in.

1. (Adverteerders met [!DNL Google Ads] -accounts die zaken doen in de Europese Economische Ruimte (EER) of het Verenigd Koninkrijk (VK); optioneel) Als u toestemming van gebruikers in de EER en het VK hebt verzameld om hun gegevens te uploaden voor reclamedoeleinden, schakelt u het selectievakje in naast **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Klik op **[!UICONTROL Save]**.

1. (Als uw omzettingen op het niveau van de managerrekening worden gevolgd) [ voeg geloofsbrieven voor uw managerrekening ](/help/search-social-commerce/admin/manager-accounts.md) bij **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]** toe.

1. Controleer of elk doel — genaamd `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — binnen twee dagen op het advertentienetwerk wordt weergegeven.

   In de [!DNL Google Ads] redacteur, kijk omhoog uw [ omzettingsacties ](https://support.google.com/google-ads/answer/11461796). In de [!DNL Microsoft Advertising] redacteur, kijk omhoog uw [ omzettingsdoelstellingen ](https://help.ads.microsoft.com/#apex/ads/en/56709).

   Werk indien nodig het datumbereik bij en voeg de uploaddatum toe.

## Hoe de gewogen doelstelling wordt berekend

Het gewogen doel dat aan het advertentienetwerk wordt overgegaan is de som alle metrische waarden verzamelde, met uitzondering van omzettingen die door [!DNL Google Ads] of door de [!DNL Microsoft Advertising] Universal Event tracking (UET) markering worden gevolgd. De waarde wordt berekend met de toewijzingsmethode die is ingesteld voor de account Zoeken, Sociaal en Commerce van de adverteerder.

Stel dat het doel van de doelstelling metrisch is met Cart Additions met een gewicht van 25 en dat uw maateenheden voor assistentie GL_Lead en Revenue met gewichten van 1 en Downloads met een gewicht van 0,5 zijn.

![ Voorbeeld van een gewogen doelstelling ](/help/search-social-commerce/assets/objective-example.png " Voorbeeld van een gewogen doelstelling ")

Stel dat een trefwoord resulteert in de volgende handelingen voor het portfolio:

* 10 extra winkelwagentjes
* 500 dollar aan inkomsten
* 50 downloads
* 5 GGL_Lead

GGL_Lead wordt niet opgenomen in de berekening/upload omdat het een metrische waarde is die door Google Ads wordt bijgehouden. Daarom wordt de gewogen objectieve waarde berekend als ((10 x 25) + (500 x 1) + (50 x 0,5)) = 775.

>[!TIP]
>
>U kunt gegevens voor Adobe Advertising gewogen opbrengsten binnen de rapporten van het advertentienetwerk bekijken. U kunt het beste de gewogen omzet vergelijken met de [!DNL Google Ads] &quot;All conv. (door conv. time)&quot; of de metrische waarde [!DNL Microsoft Advertising] &quot;All conv. opbrengst,&quot;gesegmenteerd aan metrisch O_ACS_OBJ*.<!--clarify -->

## Problemen met ontbrekende doelstellingen oplossen

Als het doel — genaamd `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — voor een van uw portfolio&#39;s niet op het advertentienetwerk wordt weergegeven, controleert u het volgende:

* ([!DNL Google Ads]) Controleer of de conversies moeten worden geüpload naar het account- of beheerniveau. Als ze op managementniveau moeten worden geüpload:

   * Controleer of de referenties voor de [!DNL Google Ads] manager-account zijn opgegeven op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]** . Indien noodzakelijk, [ voeg de geloofsbrieven voor de managerrekening ](/help/search-social-commerce/admin/manager-accounts.md) toe.

   * Controleer of de netwerkaccount voor advertenties al dezelfde metrische naam bevat. Als het, dan metrisch anders noemt zodat het correcte manager-vlakke bezit kan worden gecreeerd.

* Controleer of de optie &quot;hybride&quot; van de portefeuille is geselecteerd en of de doelstelling geldige opbrengsten heeft.

>[!MORELIKETHIS]
>
>* [ Ongeveer het leiden van de omzettingsmetriek van een adverteerder ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [ uploadt Onderzoek, Sociale, &amp; Commerce-Gecontroleerde omzettingsmetriek aan  [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
