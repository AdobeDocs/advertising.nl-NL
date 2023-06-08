---
title: Beheer klanten gelijke soorten publiek gebruikend de lijsten van klantengegevens
description: Leer maken en bewerken [!DNL Google Ads] en [!DNL Microsoft® Advertising] klant past publiek van uw lijsten van klantengegevens aan.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---

# Beheren [!DNL Google Ads] en [!DNL Microsoft® Advertising] klant past publiek aan gebruikend de lijsten van klantengegevens

U kunt [!DNL Google Ads] en [!DNL Microsoft® Advertising] klant past publiek van uw lijsten van klantengegevens aan. U kunt ook [!DNL Google Ads] of [!DNL Microsoft® Advertising] klant stemt publiek behalve [!DNL Google Ads] publiek dat is gemaakt op basis van een [!DNL Adobe] publiek.

## Creeer een publiek van de klantengelijke van een lijst van klantengegevens

*[!DNL Google Ads]en [!DNL Microsoft® Advertising] accounts die alleen in aanmerking komen voor overeenkomst met klanten*

U kunt een [!DNL Google Ads] of [!DNL Microsoft® Advertising] op gegevens-gebaseerde lijst van de klant van een gegevensdossier dat u van uw systeem van het beheer van de klantenverhouding (CRM) produceert.

Voor [!DNL Microsoft® Advertising] accounts, kan het bestand e-mailadressen bevatten. Voor [!DNL Google Ads] accounts, kan het bestand e-mailadressen, mailingadressen of telefoonnummers bevatten; gebruikers-id&#39;s; of mobiele apparaat-id&#39;s van uw CRM.

>[!NOTE]
>
>Met Zoeken, Sociaal en Handel worden geen klantgegevens opgeslagen die u uploadt of via de [!DNL Adobe] segmenten die worden gebruikt voor het maken of bewerken van een [!DNL Google Ads] of [!DNL Microsoft® Advertising] publiek.

1. Genereer een bestand met de klantgegevens in de vereiste indeling.

   Voor- en achternamen, e-mailadressen en telefoonnummers moet het SHA-256-algoritme worden gebruikt. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Voor [!DNL Google Ads] publiek, zie [!DNL Google Ads] documentatie over &quot;[Richtlijnen voor het uploaden van onderbroken gegevens opmaken](https://support.google.com/google-ads/answer/7476159)&quot; voor een lijst van toegestane contactinformatievelden en -vereisten. Voor [!DNL Microsoft® Advertising] publiek, zie [!DNL Microsoft® Advertising] documentatie over [opstellen van lijsten met overeenkomsten voor klanten](https://help.ads.microsoft.com/#apex/ads/en/56921. U kunt desgewenst een [!DNL Microsoft® Excel] sjabloon voor contactgegevens.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Klik op de werkbalk boven de tabel met gegevens op ![Maken](/help/search-social-commerce/assets/add.png "Maken").

1. Selecteer het advertentienetwerk en de accountnaam en klik vervolgens op **[!UICONTROL Continue]**.

1. Geef de publieksinformatie op:

   1. In de [!UICONTROL Data Source] menu, selecteert u **[!UICONTROL Customer List]**.

   1. Voer de **[!UICONTROL Audience Name]**.

   1. Upload het bestand:

      1. Selecteer [!UICONTROL Data Upload Type]: *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]*, of *[!UICONTROL Mobile Device IDs]*.

         De optie Gebruikersnamen is alleen beschikbaar voor [!DNL Google Ads] adverteerders in de VS die ervoor kiezen [gebruikers-id-segmenten](https://support.google.com/google-ads/answer/9199250)

      1. (Alleen lijsten met mobiele apparaten) Selecteer de optie **[!UICONTROL OS Type]** (*[!UICONTROL Android™]* of *[!UICONTROL iOS]*) en voert u de **[!UICONTROL App ID]**.

         De toepassings-id is een unieke id die het mobiele besturingssysteem gebruikt om uw toepassing toe te staan verbinding te maken met de Google Play of Apple App Store:

         * ([!DNL Android™] apps) De [!DNL Android™] pakketnaam binnen [!DNL Google Play], geïdentificeerd door &quot;`id=<package_name>`.&quot;

            In https://play.google.com/store/apps/details?id=com.example.game is de pakketnaam bijvoorbeeld com.example.game.

         * ([!DNL iOS] apps) De toepassings-id binnen de [!DNL iTunes App Store], geïdentificeerd door &quot;`<idNNNNNNNNN>`&quot; aan het einde van de URL. Het is ook beschikbaar in de [!DNL iOS Developer Console].

            In https://itunes.apple.com/us/app/id284882215 is de id bijvoorbeeld id284882215.
         Uw ontwikkelingsteam heeft toegang tot [!UICONTROL App ID] voor het desbetreffende platform.

      1. In de [!UICONTROL Select File] veld, klikken **[!UICONTROL Choose File]** en selecteer het bestand op uw netwerk of apparaat.

      1. Schakel het selectievakje in om aan te geven dat u akkoord gaat met de voorwaarden van het dialoogvenster [!DNL Adobe] en voegt beleid van de netwerkprivacy toe.

      1. Klik op **[!UICONTROL Upload File]**.
   1. Geef het aantal **[!UICONTROL Membership Days]**, dit is het aantal dagen dat de cookie van een gebruiker in het publiek blijft.

   Gebruik de tijdsduur waarvan u verwacht dat uw advertentie relevant is voor de gebruiker. Lijsten van klanten verlopen alleen als u een waarde invoert.

1. Klik op **[!UICONTROL Post]**.

>[!NOTE]
>
>* Het ad-netwerk kan 24 uur duren voordat het bestand is verwerkt.
>* Zie [[!DNL Google Ads] documentatie over de werking en de beperkingen van klantenovereenkomsten](https://support.google.com/displayvideo/answer/9539301).


## Een publiek van de Aanpassing van de Klant uitgeven die een Lijst van de Gegevens van de Klant gebruikt

U kunt elke [!DNL Google Ads] of [!DNL Microsoft® Advertising] klant stemt publiek behalve [!DNL Google Ads] publiek dat is gemaakt op basis van een [!DNL Adobe] publiek. U kunt gegevens uploaden om toe te voegen, te schrappen, of alle bestaande gegevens voor het publiek te vervangen.

De gegevens moeten van hetzelfde type zijn als de oorspronkelijke lijst met klanten (e-mailadressen, e-mailadressen, telefoonnummers, gebruikers-id&#39;s of mobiele apparaat-id&#39;s voor een specifieke toepassing op een specifiek mobiel besturingssysteem).

1. Genereer een bestand met de klantgegevens in de vereiste indeling voor het bestaande gegevenstype.

Voor- en achternamen, e-mailadressen en telefoonnummers moet het SHA-256-algoritme worden gebruikt. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Voor [!DNL Google Ads] publiek, zie [!DNL Google Ads] documentatie over &quot;[Richtlijnen voor het uploaden van onderbroken gegevens opmaken](https://support.google.com/google-ads/answer/7476159)&quot; voor een lijst van toegestane contactinformatievelden en -vereisten. Voor [!DNL Microsoft® Advertising] publiek, zie [!DNL Microsoft® Advertising] documentatie over [opstellen van lijsten met overeenkomsten voor klanten](https://help.ads.microsoft.com/#apex/ads/en/56921. U kunt desgewenst een [!DNL Microsoft® Excel] sjabloon voor contactgegevens.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Schakel het selectievakje naast het publiek dat u wilt bewerken in.

1. Klik op de werkbalk boven de tabel met gegevens op ![Bewerken](/help/search-social-commerce/assets/edit.png).

1. Selecteer de actie: *[!UICONTROL Add]* (om de geüploade gegevens aan de bestaande gegevens toe te voegen, tenzij deze al bestaan), *[!UICONTROL Delete]* (om de geüploade gegevens uit de bestaande gegevens te verwijderen, indien deze al bestaan), of *[!UICONTROL Replace]* (om alle bestaande gegevens te verwijderen en te vervangen door de geüploade gegevens).

1. Upload het bestand:

   1. In de [!UICONTROL Select File] veld, klikken **[!UICONTROL Choose File]** en selecteer het bestand op uw netwerk of apparaat.

   1. Schakel het selectievakje in om aan te geven dat u akkoord gaat met de voorwaarden van het dialoogvenster [!DNL Adobe] en voegt beleid van de netwerkprivacy toe.

   1. Klik op **[!UICONTROL Upload File]**.

1. Klik op **[!UICONTROL Post]**.

>[!NOTE]
>
>Het advertentienetwerk kan enige tijd duren om updates aan een publiek te verwerken.

>[!MORELIKETHIS]
>
>* [Informatie over publiek](audience-about.md)
>* [Maken [!DNL Google Ads] klant stemt doelgroep van [!DNL Adobe] publiek](google-audience-from-adobe-audience.md)
>* [Een [!DNL Google Ads] klant stemt publiek van een Adobe Campaign e-maillijst overeen](google-audience-from-campaign-email-list.md)
>* [Dynamisch publiek voor opnieuw op de markt brengen beheren](audience-dynamic-remarketing-manage.md)

