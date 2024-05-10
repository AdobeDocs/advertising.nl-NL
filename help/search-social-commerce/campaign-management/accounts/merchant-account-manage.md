---
title: Zakelijke accounts beheren
description: Leer hoe u accountgegevens voor een bedrijfscentrum instelt en beheert.
exl-id: 7d940e45-ea49-470b-98d0-0196593228cb
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# Zakelijke accounts beheren

*Accountmanager, accountmanager en alleen gebruikersrollen voor beheerders van Adoben*

Met Zoeken, Sociaal en Commerce kunt u elke dag productgegevens downloaden en weergeven voor Google Merchant Center- of Microsoft Merchant Center-accounts van adverteerders. Bovendien kunnen met Zoeken, Sociaal en Commerce advertenties worden geautomatiseerd op basis van de inhoud van het zakelijke account. Als u rechtstreeks wilt werken met productgegevens in Zoeken, Sociaal en Commerce, moet u een corresponderend accountrecord maken met de toegangsreferenties van uw account en met toegang *enabled*.

>[!NOTE]
>
>U kunt een zakelijke accountrecord niet verwijderen. U kunt de toegang tot een account uitschakelen door het accounttype te wijzigen in *uitgeschakeld*.

## Detailgegevens van zakelijke accounts maken {#create-merchant-account}

*Accountmanager, accountmanager en alleen gebruikersrollen voor beheerders van Adoben*

Als u productgegevens wilt weergeven en trackingsjablonen wilt genereren voor een zakelijke account, en advertenties wilt maken op basis van de gegevens, moet u een corresponderend accountrecord maken met de toegangsgegevens van de account en met toegang tot de account *enabled*.

>[!NOTE]
>
>Ga naar de website van het netwerk als u een werkelijke account op het zakelijke netwerk wilt maken.

1. Klik in het hoofdmenu op **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]**, die voor de [!UICONTROL Accounts] tab.

1. Klik op de werkbalk boven de tabel met gegevens op **[!UICONTROL Create Account]**.

1. Geef de [zakelijke accountinstellingen](#merchant-account-settings):

   1. In de [!UICONTROL Product Source] selecteert u het winkelcentrum.

   <!--

   1. ([!DNL Meta Ads] accounts only) Log in to the [!DNL Meta Ads] account.

   And are there additional steps just for Meta? If so, create a separate procedure for it.
   
   -->

   1. (Vereist voor [!DNL Google Ads] accounts; optioneel voor [!DNL Microsoft Advertising] accounts) Zoekopdrachten, sociale gegevens en Commerce toegang geven tot het account via de [[!DNL OAuth] machtigingsprotocol](https://oauth.net/2/):

      1. ([!DNL Microsoft Advertising] alleen accounts) Selecteren **[!UICONTROL oAuth]**.

      1. Klik op **[!UICONTROL Enable Connection]**.

      1. (Als u niet bent aangemeld bij de account van de adverteerder) Meld u aan bij de account van de adverteerder. De beste manier is om de geloofsbrieven voor inhoud API toegang tot het bedrijfscentrum account te gebruiken.

      1. Klik in het scherm Verzoek om toegang/toestemming op de knop om de machtiging te bevestigen.

      1. Kopieer de verificatietekenreeks in het pop-upvenster dat wordt geopend, en plak de tekenreeks in de **[!UICONTROL oAuth Token]** veld.

      1. Geef de overige accountinstellingen op.

1. Klik op **[!UICONTROL Save]**.

   Kenmerkgegevens voor alle producten in de account zijn beschikbaar in Zoeken, Sociaal en Commerce na het volgende dagelijkse synchronisatieproces (ongeveer 6:00 in de lokale tijdzone van de gebruiker). Vervolgens kunt u de productgegevens gebruiken om het maken en maken te automatiseren met behulp van voorraadfeeds.

## Details handelsaccount bewerken {#edit-merchant-account}

*Accountmanager, accountmanager en alleen gebruikersrollen voor beheerders van Adoben*

Als de accountgegevens veranderen of als u niet langer gegevens voor een zakelijke account wilt ophalen en gebruiken, bewerkt u de accountgegevens.

>[!NOTE]
>
>Ga naar de website van het netwerk als u een feitelijke account op het zakelijke netwerk wilt bewerken.

1. Klik in het hoofdmenu op **[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]**, die voor de [!UICONTROL Accounts] tab.

1. Klik naast de accountnaam op ![Instellingen weergeven/bewerken](/help/search-social-commerce/assets/settings.png "Instellingen weergeven/bewerken").

1. Bewerk de [zakelijke accountinstellingen](#merchant-account-settings).

1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
>Zoeken, Sociaal en Commerce moeten de nieuwe accountgegevens synchroniseren met die op het bedrijfsnetwerk. Dit gebeurt automatisch één keer per dag bij ongeveer 06:00 in de lokale tijdzone van de gebruiker.

## Toegang tot een zakelijke account uitschakelen {#disable-merchant-account}

*Accountmanager, accountmanager en alleen gebruikersrollen voor beheerders van Adoben*

Wanneer u een zakelijke account uitschakelt, worden via Zoeken, Sociaal zoeken en Commerce niet aangemeld bij de account en worden de bijgewerkte productgegevens daarom niet opgehaald. De gegevens die zijn verzameld terwijl de account was ingeschakeld, worden nog opgeslagen en bestaande advertenties die zijn gemaakt met productgegevens, worden niet bijgewerkt, gepauzeerd of verwijderd volgens de instellingen van de voedersjabloon en de voedergegevens.

1. Klik in het hoofdmenu op **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** , die voor de [!UICONTROL Accounts] tab.

1. Klik naast de accountnaam op ![Instellingen weergeven/bewerken](/help/search-social-commerce/assets/settings.png "Instellingen weergeven/bewerken").

1. Wijzig de [!UICONTROL EF Account Type] tot **[!UICONTROL Disabled]**.

1. Klik op **[!UICONTROL Save]**.

## Instellingen Merchant-account {#merchant-account-settings}

>[!NOTE]
>
>Alleen accountmanager van een agentschap [!DNL Adobe] accountmanager en beheerder gebruikersrollen kunnen bedrijfs accountinstellingen configureren.

**[!UICONTROL Product Source]:** Het commerciële netwerk. U kunt de waarde van een bestaand account niet wijzigen.

**[!UICONTROL OAuth Token]:** ([!DNL Google Merchant Center] alleen accounts) De token van de account voor het autoriseren van aanmeldingen met de [[!DNL OAuth] machtigingsprotocol](https://oauth.net/2/).

**[!UICONTROL Auth Type]:** ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] alleen) Of u aanmeldingsgegevens voor de account wilt toestaan met:

* *[!UICONTROL Client login]:* De aanmeldingsgegevens van de client gebruiken.

* *[!UICONTROL oAuth]* (de standaardinstelling): De [[!DNL OAuth] machtigingsprotocol](https://oauth.net/2/).

**[!UICONTROL Access Key]:** ([!DNL Microsoft Merchant Center] alleen) De toegangstoets voor de ontwikkelaarsaccount die moet worden gebruikt.

**[!UICONTROL Account Name]:** De naam die voor het account wordt weergegeven in Zoeken, Sociaal en Commerce.

**[!UICONTROL Login]:** De aanmeldingsnaam of id voor het account.

**[!UICONTROL Password]:** Het wachtwoord voor de account.

**[!UICONTROL Confirm Password]:** Het wachtwoord voor de account.

**[!UICONTROL EF Account Type]:** Of Search, Social &amp; Commerce toegang heeft tot de account:

* *[!UICONTROL Enabled]* (standaard): met Zoeken, Sociaal en Commerce kunt u zich aanmelden bij de account om de productgegevens op te halen.

* *[!UICONTROL Disabled]:* Search, Social &amp; Commerce meldt zich niet aan bij de account en haalt daarom geen bijgewerkte productgegevens op. De gegevens die zijn verzameld terwijl de account was ingeschakeld, worden nog opgeslagen en bestaande advertenties die zijn gemaakt met productgegevens, worden niet bijgewerkt, gepauzeerd of verwijderd volgens de instellingen van de voedersjabloon en de voedergegevens.

**[!UICONTROL Account ID]:** De zakelijke account-id. Als u slechts één account met de opgegeven aanmeldingsgegevens hebt, is deze waarde optioneel.

**[!UICONTROL Time Zone]:** De tijdzone van de adverteerder. Gebruik dezelfde tijdzone die is geconfigureerd voor de accountgegevens van de adverteerder voor zoeken, sociaal en Commerce (die wordt ingesteld wanneer het account wordt gemaakt). U kunt de waarde van een bestaand account niet wijzigen.

>[!MORELIKETHIS]
>
>* [Informatie over netwerkaccounts](ad-network-account-about.md)
>* [Netwerkaccounts beheren](ad-network-account-manage.md)
