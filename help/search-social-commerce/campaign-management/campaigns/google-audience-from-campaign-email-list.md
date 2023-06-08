---
title: Een [!DNL Google Ads] klant stemt publiek van een Adobe Campaign e-maillijst overeen
description: Leer hoe u een [!DNL Google Ads] klanten komen overeen met publiek uit een bestaande Adobe Campaign-e-maillijst.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '672'
ht-degree: 0%

---

# Een [!DNL Google Ads] klant stemt publiek van een Adobe Campaign e-maillijst overeen

*[!DNL Google Ads]accounts die alleen in aanmerking komen voor overeenkomst met klanten*

U kunt een [!DNL Google Ads] klant stemt publiek van een e-maillijst in Adobe Campaign door een accountkoppeling en een workflow in te stellen in [!DNL Campaign].

Hiervoor hebt u toegang nodig tot uw [!DNL Campaign] -instantie en een XML-bestand met de vereiste workflow die uw Adobe-accountteam u zal geven. De instructies kunnen voor verschillende versies van [!DNL Campaign]. Indien nodig kan uw Adobe-accountteam u helpen bij het instellen van de workflow in [!DNL Campaign].

1. Verkrijg geloofsbrieven voor een Advertising Search, Social, &amp; Commerce-Geleverde rekening van SFTP.

1. In [!DNL Campaign], stelt u levering van de e-maillijst in voor Zoeken naar advertenties, sociale media en handel:

   1. Een [externe rekening](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html) om uw door Zoeken, Sociaal, &amp; Handel geleverde SFTP-account te koppelen:

      1. Ga in het linkermenu naar **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**.

      1. Klikken ![Account maken](/help/search-social-commerce/assets/campaign-create-account.png "Account maken").

      1. Voer een label in voor de account en selecteer **[!UICONTROL SFTP]** als het accounttype.

      1. Voer de URL en het poortnummer in voor de [!DNL Adobe] SFTP-server en de mapnaam, gebruikersnaam en wachtwoord van de adverteerder.

      1. Klik op **[!UICONTROL Save]**.
   1. In [!DNL Campaign Client]Installeer het gegevenspakket met de vereiste workflow voor het verzenden van e-mailgegevens:

      1. Ga in de menubalk naar **[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**.

      1. Selecteren **[!UICONTROL Install a package from a file]** en klik vervolgens op **[!UICONTROL Next]**.

      1. Het bestand met het gegevenspakket zoeken (`AMO_Workflow.xml`) op het apparaat of netwerk en klik vervolgens op **[!UICONTROL Next]**.

      1. Klikken **[!UICONTROL Start]** en wacht tot de workflow is geïnstalleerd.
   1. Bewerk de geïnstalleerde workflow om desgewenst de filters voor de gegevensquery te bewerken en de nieuwe publieksnaam en de externe SFTP-account te identificeren:

      1. Ga naar **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]** en open het pakket.

      1. (Optioneel) Bewerk een van de filters voor de gegevens:

         * In het werkschema, klik de vraagactiviteit (zoals ForkTransition 1) tweemaal.

         * Bewerk de filterexpressies.

         * Klik op **[!UICONTROL Finish]**.
      1. Geef het segment een naam:

         * Dubbelklik in de workflow op de activiteit **[!UICONTROL Data extraction (File)]**.

         * Aan de **[!UICONTROL Data extraction (File)]** tabblad, in het dialoogvenster **[!UICONTROL File name]** veld, voer de segmentnaam in met de extensie &quot;`.added`&quot; (zoals PaidSubscribers.added).

            De segmentnaam mag nog niet bestaan. De segmentnaam is hoofdlettergevoelig en moet bestaan uit ASCII-tekens, maar mag geen onderstrepingstekens bevatten (`_`).

            Nochtans, als u het segment aan een specifiek wilt toevoegen [!DNL Google Ad] de rekening, dan voeg de segmentnaam met een onderstrepingsteken en toe [!UICONTROL User SE Account ID] (zoek-, sociale en handels-id voor de [!DNL Google Ads] account, niet de account-id van het netwerk):

            `_<User SE Account ID>`

            Voorbeeld: Paid_Subscribers_1234.added

            >[!NOTE]
            >
            >Dit is een uitzondering op de regel die onderstrepingstekens in de bestandsnaam niet toestaat.

            Anders wordt het segment toegevoegd aan alle [!DNL Google Ads] accounts die door Search, Social &amp; Commerce worden gesynchroniseerd voor de adverteerder.

         * De optie behouden voor **[!UICONTROL Generate an outbound transition]** geselecteerd.

         * Klik op **[!UICONTROL Ok]**.
      1. Geef de externe account op waarnaar de gegevens worden verzonden:

         * Dubbelklik in de workflow op de activiteit **[!UICONTROL File Transfer]**.

         * Aan de **[!UICONTROL File Transfer]** tabblad, in het dialoogvenster **[!UICONTROL Remote server]** selecteert u de optie om **[!UICONTROL Use an external account]**.

         * In de **[!UICONTROL External account]** selecteert u het label voor de externe account die u hebt gemaakt in Stap 2.

         * In de **[!UICONTROL Server folder]** veld, selecteert u de waarde voor de [!UICONTROL Account] veld voor de externe rekening.

         * (Optioneel) Op de **[!UICONTROL Schedule]** een ander schema voor de bestandsoverdracht op.

            De workflow wordt standaard uitgevoerd om 00:00 (middernacht), zodat alle records worden verwerkt. Om latentie te minimaliseren, plant het werkschema om uiterlijk 18:00 in werking te stellen.

         * Klik op **[!UICONTROL Ok]**.





Zoek, Sociale, &amp; Handel controleert de folder om de 30 minuten (om NN:30 en NN:59 in de tijdzone van de adverteerder) en beweegt om het even welke dossiers het aan een andere plaats vindt, en leidt dan automatisch tot een publiek van de gegevens en duwt het aan Google om 22:00 (10 p.m.). U kunt elke 30 minuten zoeken naar updates (toevoegingen en aftrekken) in de e-maillijst en het publiek bijwerken op [!DNL Google Ads] dienovereenkomstig om 22.00 uur per dag.

>[!NOTE]
>
>* Als u tussen de verwerkingscycli meerdere versies van een bestand uploadt, wordt het meest recente bestand gebruikt.
>
>* Met Zoeken, Sociaal en Handel worden geen van de klantgegevens uit uw e-maillijsten opgeslagen die worden gebruikt om een [!DNL Google Ads] publiek.
>
>* [!DNL Google Ads] Het kan even duren voordat updates voor een publiek worden verwerkt.
>
>* Zie [[!DNL Google Ads] documentatie over de werking en de beperkingen van klantenovereenkomsten](https://support.google.com/displayvideo/answer/9539301).


>[!MORELIKETHIS]
>
>* [Informatie over publiek](audience-about.md)
>* [Maken [!DNL Google Ads] klant stemt doelgroep van [!DNL Adobe] publiek](google-audience-from-adobe-audience.md)
>* [Beheer klanten gelijke soorten publiek gebruikend de lijsten van klantengegevens](audience-from-customer-data-list.md)
>* [Dynamisch publiek voor opnieuw op de markt brengen beheren](audience-dynamic-remarketing-manage.md)

