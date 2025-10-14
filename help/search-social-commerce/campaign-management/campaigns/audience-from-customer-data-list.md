---
title: Beheer klanten gelijke soorten publiek gebruikend de lijsten van klantengegevens
description: Leer om  [!DNL Google Ads]  tot stand te brengen en uit te geven en  [!DNL Microsoft Advertising]  klantengelijke publiek van uw lijsten van klantengegevens.
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Beheer [!DNL Google Ads] en [!DNL Microsoft Advertising] klanten gelijke soorten publiek gebruikend de lijsten van klantengegevens

U kunt [!DNL Google Ads] - en [!DNL Microsoft Advertising] -klantovereenkomsten maken op basis van de gegevenslijsten van uw klant. U kunt ook alle [!DNL Google Ads] - of [!DNL Microsoft Advertising] klantspecifieke doelgroepen bijwerken, behalve [!DNL Google Ads] publiek dat is gemaakt vanuit een [!DNL Adobe] -publiek.

## Creeer een publiek van de klantengelijke van een lijst van klantengegevens

*[!DNL Google Ads]en [!DNL Microsoft Advertising] accounts die alleen in aanmerking komen voor overeenkomst met klanten*

U kunt een [!DNL Google Ads] of [!DNL Microsoft Advertising] op gegevens gebaseerde lijst van klanten van een gegevensdossier tot stand brengen dat u van uw systeem van het Beheer van de klantenverhouding (CRM) produceert.

Voor [!DNL Microsoft Advertising] -accounts kan het bestand e-mailadressen bevatten. Voor [!DNL Google Ads] -accounts kan het bestand e-mailadressen, e-mailadressen of telefoonnummers, gebruikers-id&#39;s of mobiele apparaat-id&#39;s van uw CRM bevatten.

>[!NOTE]
>
>In Zoeken, Sociaal en Commerce worden geen klantgegevens opgeslagen die u uploadt, noch gegevens uit de [!DNL Adobe] -segmenten die worden gebruikt om een [!DNL Google Ads] - of [!DNL Microsoft Advertising] -publiek te maken of te bewerken.

1. Genereer een bestand met de klantgegevens in de vereiste indeling.

   Voor- en achternamen, e-mailadressen en telefoonnummers moet het SHA-256-algoritme worden gebruikt. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> voor [!DNL Google Ads] publiek, zie de [!DNL Google Ads] documentatie over &quot;[&#x200B; Formatterende richtlijnen voor het uploaden van gehakte gegevens &#x200B;](https://support.google.com/google-ads/answer/7476159)&quot;voor een lijst van toegestane gebieden en vereisten van de contactinformatie. Voor [!DNL Microsoft Advertising] publiek, zie de [!DNL Microsoft Advertising] documentatie over [&#x200B; voorbereidend de lijsten van de klantengelijke &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/56921). U kunt desgewenst een [!DNL Microsoft Excel] -sjabloon downloaden voor contactgegevens.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** . Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]** .

1. In de toolbar boven de gegevenslijst, leidt de klik ![&#x200B; &#x200B;](/help/search-social-commerce/assets/add.png " tot ").

1. Selecteer het advertentienetwerk en de accountnaam en klik op **[!UICONTROL Continue]** .

1. Geef de publieksinformatie op:

   1. Selecteer **[!UICONTROL Customer List]** in het menu [!UICONTROL Data Source] .

   1. Voer de **[!UICONTROL Audience Name]** in.

   1. Upload het bestand:

      1. Selecteer [!UICONTROL Data Upload Type]: *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]* of *[!UICONTROL Mobile Device IDs]* .

         De optie van identiteitskaarts van de Gebruiker is beschikbaar slechts aan [!DNL Google Ads] adverteerders in de V.S. die binnen voor [&#x200B; gebruikersID segmenten &#x200B;](https://support.google.com/google-ads/answer/9199250) worden gekozen

      1. (Alleen lijsten met mobiele apparaten) Selecteer **[!UICONTROL OS Type]** (*[!UICONTROL Android™]* of *[!UICONTROL iOS]*) en voer de **[!UICONTROL App ID]** in.

         De toepassings-id is een unieke id die het mobiele besturingssysteem gebruikt om uw toepassing toe te staan verbinding te maken met de Google Play of Apple App Store:

         * ([!DNL Android™] apps) De [!DNL Android™] pakketnaam in [!DNL Google Play] , geïdentificeerd door &quot;`id=<package_name>`&quot;.

           In `https://play.google.com/store/apps/details?id=com.example.game` is de pakketnaam bijvoorbeeld com.example.game.

         * ([!DNL iOS] apps) De toepassings-id binnen [!DNL iTunes App Store], geïdentificeerd door &quot;`<idNNNNNNNNN>`&quot; aan het einde van de URL. Het is ook beschikbaar in [!DNL iOS Developer Console].

           In `https://itunes.apple.com/us/app/id284882215` is de id bijvoorbeeld id284882215.

         Uw ontwikkelingsteam heeft toegang tot [!UICONTROL App ID] voor het relevante platform.

      1. Klik in het veld [!UICONTROL Select File] op **[!UICONTROL Choose File]** en selecteer het bestand in uw netwerk of apparaat.

      1. Schakel het selectievakje in om aan te geven dat u akkoord gaat met de voorwaarden van het [!DNL Adobe] -beleid en het privacybeleid van het netwerk.

      1. (Adverteerders die [!DNL Google Ads] publiek maken dat zaken doet in de Europese Economische Ruimte (EER) of het Verenigd Koninkrijk (VK); facultatief) Als u toestemming van gebruikers in de EER en het VK hebt verzameld om hun gegevens voor reclamedoeleinden te uploaden, schakelt u het selectievakje naast **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]** in

      [!DNL Google Ads] negeert gegevens voor gebruikers in de EER en het Verenigd Koninkrijk met een niet-gespecificeerde toestemmingsstatus. Dit kan leiden tot verschillen in gegevens en prestatieproblemen.

      1. Klik op **[!UICONTROL Upload File]**.

   1. Geef het aantal **[!UICONTROL Membership Days]** op. Dit is het aantal dagen dat de cookie van een gebruiker in het publiek blijft.

   Gebruik de tijdsduur waarvan u verwacht dat uw advertentie relevant is voor de gebruiker. Lijsten van klanten verlopen alleen als u een waarde invoert.

1. Klik op **[!UICONTROL Post]**.

>[!NOTE]
>
>* Het ad-netwerk kan 24 uur duren voordat het bestand is verwerkt.
>* Zie [[!DNL Google Ads]  documentatie op hoe de klantengelijken werken en beperkingen &#x200B;](https://support.google.com/displayvideo/answer/9539301) aanpassen.

## Een publiek van de Aanpassing van de Klant uitgeven die een Lijst van de Gegevens van de Klant gebruikt

U kunt alle [!DNL Google Ads] - of [!DNL Microsoft Advertising] klantspecifieke doelgroepen bijwerken, behalve [!DNL Google Ads] publiek dat is gemaakt vanuit een [!DNL Adobe] -publiek. U kunt gegevens uploaden om toe te voegen, te schrappen, of alle bestaande gegevens voor het publiek te vervangen.

De gegevens moeten van hetzelfde type zijn als de oorspronkelijke lijst met klanten (e-mailadressen, e-mailadressen, telefoonnummers, gebruikers-id&#39;s of mobiele apparaat-id&#39;s voor een specifieke toepassing op een specifiek mobiel besturingssysteem).

1. Genereer een bestand met de klantgegevens in de vereiste indeling voor het bestaande gegevenstype.

Voor- en achternamen, e-mailadressen en telefoonnummers moet het SHA-256-algoritme worden gebruikt. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> voor [!DNL Google Ads] publiek, zie de [!DNL Google Ads] documentatie over &quot;[&#x200B; Formatterende richtlijnen voor het uploaden van gehakte gegevens &#x200B;](https://support.google.com/google-ads/answer/7476159)&quot;voor een lijst van toegestane gebieden en vereisten van de contactinformatie. Voor [!DNL Microsoft Advertising] publiek, zie de [!DNL Microsoft Advertising] documentatie over [ het voorbereiden van de lijsten van de klantengelijke ] (https://help.ads.microsoft.com/#apex/ads/en/56921. U kunt desgewenst een [!DNL Microsoft Excel] -sjabloon downloaden voor contactgegevens.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** . Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]** .

1. Schakel het selectievakje naast het publiek dat u wilt bewerken in.

1. In de toolbar boven de gegevenslijst, geeft de klik ![&#x200B; &#x200B;](/help/search-social-commerce/assets/edit.png) uit.

1. Selecteer de actie: *[!UICONTROL Add]* (om de geüploade gegevens toe te voegen aan de bestaande gegevens, tenzij deze al bestaan), *[!UICONTROL Delete]* (om de geüploade gegevens te verwijderen uit de bestaande gegevens, als deze al bestaan) of *[!UICONTROL Replace]* (om alle bestaande gegevens te verwijderen en te vervangen door de geüploade gegevens).

1. Upload het bestand:

   1. Klik in het veld [!UICONTROL Select File] op **[!UICONTROL Choose File]** en selecteer het bestand in uw netwerk of apparaat.

   1. Schakel het selectievakje in om aan te geven dat u akkoord gaat met de voorwaarden van het [!DNL Adobe] -beleid en het privacybeleid van het netwerk.

   1. Klik op **[!UICONTROL Upload File]**.

1. Klik op **[!UICONTROL Post]**.

>[!NOTE]
>
>Het advertentienetwerk kan enige tijd duren om updates aan een publiek te verwerken.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer publiek &#x200B;](audience-about.md)
>* [&#x200B; creeer  [!DNL Google Ads]  publiek van de klantenovereenkomst van  [!DNL Adobe]  publiek &#x200B;](google-audience-from-adobe-audience.md)
>* [&#x200B; creeer a [!DNL Google Ads]  publiek van de klantengelijke van een e-maillijst van Adobe Campaign &#x200B;](google-audience-from-campaign-email-list.md)
>* [&#x200B; beheer dynamische remarketing publiek &#x200B;](audience-dynamic-remarketing-manage.md)
