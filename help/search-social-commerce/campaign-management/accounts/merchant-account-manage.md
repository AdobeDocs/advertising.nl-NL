---
title: Zakelijke accounts beheren
description: Leer hoe u accountgegevens voor een bedrijfscentrum instelt en beheert.
exl-id: 7d940e45-ea49-470b-98d0-0196593228cb
feature: Search Campaign Management
source-git-commit: cb65108fcc60c11b901e3b43c292ad5a94192b9f
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# Zakelijke accounts beheren

*de rekeningsmanager van het Agentschap, de rekeningsmanager van Adobe, en slechts de rollen van de beheerdergebruiker*

Met Zoeken, Sociaal en Commerce kunt u elke dag productgegevens downloaden en weergeven voor Google Merchant Center- of Microsoft Merchant Center-accounts van adverteerders. Bovendien kan het Onderzoek, Sociaal, &amp; Commerce en verwezenlijking automatiseren die op de inhoud van de handelaarrekening wordt gebaseerd.Om direct met productgegevens in Onderzoek, Sociale, &amp; Commerce te werken, moet u een overeenkomstig rekeningsverslag tot stand brengen dat de geloofsbrieven van de rekeningstoegang en met toegang *bevat toegelaten*.

>[!NOTE]
>
>U kunt een zakelijke accountrecord niet verwijderen. U kunt toegang tot een rekening onbruikbaar maken door het accounttype te veranderen in *gehandicapt*.

## Detailgegevens van zakelijke accounts maken {#create-merchant-account}

*de rekeningsmanager van het Agentschap, de rekeningsmanager van Adobe, en slechts de rollen van de beheerdergebruiker*

Om productgegevens te bekijken en het volgen malplaatjes voor een handelaarrekening te produceren, en advertenties tot stand te brengen die op de gegevens worden gebaseerd, moet u een overeenkomstig rekeningsverslag tot stand brengen dat de geloofsbrieven van de rekeningstoegang en met toegang tot de toegelaten rekening ** bevat.

>[!NOTE]
>
>Ga naar de website van het netwerk als u een werkelijke account op het zakelijke netwerk wilt maken.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** , dat wordt geopend op het tabblad [!UICONTROL Accounts] .

1. Klik in de werkbalk boven de gegevenstabel op **[!UICONTROL Create Account]** .

1. Specificeer de [&#x200B; handelende rekeningsmontages &#x200B;](#merchant-account-settings):

   1. Selecteer in het menu [!UICONTROL Product Source] het middelpunt van de koopman.

   <!--

   1. ([!DNL Meta Ads] accounts only) Log in to the [!DNL Meta Ads] account.

   And are there additional steps just for Meta? If so, create a separate procedure for it.
   
   -->

   1. (Vereist voor [!DNL Google Ads] rekeningen; facultatief voor [!DNL Microsoft Advertising] rekeningen) sta Onderzoek, Sociale, &amp; Commerce toe om tot de rekening toegang te hebben gebruikend het [[!DNL OAuth]  vergunningsprotocol &#x200B;](https://oauth.net/2/):

      1. ([!DNL Microsoft Advertising] alleen accounts) Selecteer **[!UICONTROL oAuth]** .

      1. Klik op **[!UICONTROL Enable Connection]**.

      1. (Als u niet bent aangemeld bij de account van de adverteerder) Meld u aan bij de account van de adverteerder. De beste manier is om de geloofsbrieven voor inhoud API toegang tot het bedrijfscentrum account te gebruiken.

      1. Klik in het scherm Verzoek om toegang/toestemming op de knop om de machtiging te bevestigen.

      1. Kopieer de verificatietekenreeks in het pop-upvenster dat wordt geopend en plak de tekenreeks in het veld **[!UICONTROL oAuth Token]** .

      1. Geef de overige accountinstellingen op.

1. Klik op **[!UICONTROL Save]**.

   Kenmerkgegevens voor alle producten in de account zijn beschikbaar in Zoeken, Sociaal en Commerce na het volgende dagelijkse synchronisatieproces (ongeveer 6:00 in de lokale tijdzone van de gebruiker). Vervolgens kunt u de productgegevens gebruiken om het maken en maken te automatiseren met behulp van voorraadfeeds.

## Details handelsaccount bewerken {#edit-merchant-account}

*de rekeningsmanager van het Agentschap, de rekeningsmanager van Adobe, en slechts de rollen van de beheerdergebruiker*

Als de accountgegevens veranderen of als u niet langer gegevens voor een zakelijke account wilt ophalen en gebruiken, bewerkt u de accountgegevens.

>[!NOTE]
>
>Ga naar de website van het netwerk als u een feitelijke account op het zakelijke netwerk wilt bewerken.

1. Klik in het hoofdmenu op **[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]** , dat wordt geopend op het tabblad [!UICONTROL Accounts] .

1. Naast de rekeningsnaam, klik ![&#x200B; Mening/geef montages &#x200B;](/help/search-social-commerce/assets/settings.png " Mening uit/geef montages ").

1. Bewerk de [&#x200B; handelende rekeningsmontages &#x200B;](#merchant-account-settings).

1. Klik op **[!UICONTROL Save]**.

>[!NOTE]
>
>Zoeken, Sociaal en Commerce moeten de nieuwe accountgegevens synchroniseren met die op het bedrijfsnetwerk. Dit gebeurt automatisch één keer per dag bij ongeveer 06:00 in de lokale tijdzone van de gebruiker.

## Toegang tot een zakelijke account uitschakelen {#disable-merchant-account}

*de rekeningsmanager van het Agentschap, de rekeningsmanager van Adobe, en slechts de rollen van de beheerdergebruiker*

Wanneer u een zakelijke account uitschakelt, worden via Zoeken, Sociaal zoeken en Commerce niet aangemeld bij de account en worden de bijgewerkte productgegevens daarom niet opgehaald. De gegevens die zijn verzameld terwijl de account was ingeschakeld, worden nog opgeslagen en bestaande advertenties die zijn gemaakt met productgegevens, worden niet bijgewerkt, gepauzeerd of verwijderd volgens de instellingen van de voedersjabloon en de voedergegevens.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** , dat wordt geopend op het tabblad [!UICONTROL Accounts] .

1. Naast de rekeningsnaam, klik ![&#x200B; Mening/geef montages &#x200B;](/help/search-social-commerce/assets/settings.png " Mening uit/geef montages ").

1. Wijzig [!UICONTROL EF Account Type] in **[!UICONTROL Disabled]** .

1. Klik op **[!UICONTROL Save]**.

## Instellingen Merchant-account {#merchant-account-settings}

>[!NOTE]
>
>Alleen accountbeheer, [!DNL Adobe] accountbeheer en beheerdersgebruikersrollen kunnen bedrijfs accountinstellingen configureren.

**[!UICONTROL Product Source]:** Het commerciële netwerk. U kunt de waarde van een bestaand account niet wijzigen.

**[!UICONTROL OAuth Token]:** ([!DNL Google Merchant Center] rekeningen slechts) het teken van de rekening om logins toe te staan gebruikend het [[!DNL OAuth]  vergunningsprotocol &#x200B;](https://oauth.net/2/).

**[!UICONTROL Auth Type]:** ([!DNL Microsoft Advertising]/ [!DNL Microsoft Merchant Center] slechts) of om logins aan de rekening toe te laten gebruikend:

* *[!UICONTROL Client login]:* om login van de cliënt te gebruiken.

* *[!UICONTROL oAuth]* (het gebrek): Om het [[!DNL OAuth]  vergunningsprotocol &#x200B;](https://oauth.net/2/) te gebruiken.

**[!UICONTROL Access Key]:** ([!DNL Microsoft Merchant Center] slechts) de toegangssleutel voor de ontwikkelaarrekening aan gebruik.

**[!UICONTROL Account Name]:** De naam die voor de account wordt weergegeven in Zoeken, Sociaal en Commerce.

**[!UICONTROL Login]:** De aanmeldnaam of -id voor de account.

**[!UICONTROL Password]:** Het wachtwoord voor de account.

**[!UICONTROL Confirm Password]:** Het wachtwoord voor de account.

**[!UICONTROL EF Account Type]:** Of Search, Social &amp; Commerce toegang heeft tot de account:

* *[!UICONTROL Enabled]* (standaard): met Zoeken, Sociaal en Commerce kunt u zich aanmelden bij de account om de productgegevens op te halen.

* *[!UICONTROL Disabled]:* Met Zoeken, Sociaal en Commerce kunt u zich niet aanmelden bij de account en worden de bijgewerkte productgegevens daarom niet opgehaald. De gegevens die zijn verzameld terwijl de account was ingeschakeld, worden nog opgeslagen en bestaande advertenties die zijn gemaakt met productgegevens, worden niet bijgewerkt, gepauzeerd of verwijderd volgens de instellingen van de voedersjabloon en de voedergegevens.

**[!UICONTROL Account ID]:** De zakelijke account-id. Als u slechts één account met de opgegeven aanmeldingsgegevens hebt, is deze waarde optioneel.

**[!UICONTROL Time Zone]:** De tijdzone van de adverteerder. Gebruik dezelfde tijdzone die is geconfigureerd voor de accountgegevens van de adverteerder voor zoeken, sociaal en Commerce (die wordt ingesteld wanneer het account wordt gemaakt). U kunt de waarde van een bestaand account niet wijzigen.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer ad netwerkrekeningen &#x200B;](ad-network-account-about.md)
>* [&#x200B; beheer en netwerkrekeningen &#x200B;](ad-network-account-manage.md)
