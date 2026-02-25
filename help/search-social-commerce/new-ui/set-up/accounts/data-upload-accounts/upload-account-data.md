---
title: Offline accountgegevens uploaden voor rapportage en simulaties
description: Leer hoe te om off-line rekeningsgegevens manueel te uploaden of aan een  [!DNL Amazon] [!DNL S3] emmer voor rapportering en simulatiesteun. Logbestanden volgen de voortgang van uploadtaken.
source-git-commit: bfa5403ff66bed73797fc4c7115b8c043856745d
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 1%

---

# Offline accountgegevens uploaden voor rapportage en simulaties

*Advertisers die voor de uploads van rekeningsgegevens* worden toegelaten

Upload inhoud van de campagne en offline kosten, klik, en omzettingsgegevens voor een rekening zonder API steun voor rapportering en prestatiessimulaties.

U kunt de voortgang van de uploadtaken volgen met de functie [!UICONTROL Upload Logs] :

* Een lijst weergeven met elk bestand dat voor de account is geüpload. De informatie over elke bestandsupporttaak omvat de bestandsnaam, het uploadkanaal (*[!UICONTROL Cloud Storage]* of *[!UICONTROL Drag & Drop]* ), de synchronisatiedatum en -status en de redenen voor onvolledige uploads.

* Download een bestand met de accountentiteiten en de bijbehorende gegevens die voor een taak zijn geüpload. De bestanden hebben de indeling CSV (comma-separated values, door komma&#39;s gescheiden waarden).

## Accountgegevens handmatig uploaden

U kunt een account vullen met inhoud en kosten voor de campagne, klikken en conversiegegevens door de gegevens handmatig te uploaden in een bestand.

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

1. Klik in het hoofdmenu op **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** .

1. Voer een van de volgende handelingen uit:

   * (Vanuit de [!UICONTROL Accounts] -weergave):

      1. Schakel het selectievakje naast de accountnaam in en klik op **[!UICONTROL Upload]** op de werkbalk voor bulkacties.

      1. Sleep een bestand naar het vak of klik op **[!UICONTROL Browse Files]** en kies een bestand van uw apparaat of netwerk.

      1. Klik op **[!UICONTROL Upload Files]**.

   * (Uit de accountinstellingen):

      1. Selecteer de account op een van de volgende manieren:

         * Plaats de cursor boven de accountnaam, klik op **..** en klik vervolgens op **[!UICONTROL Edit]** .

         * Schakel het selectievakje naast de accountnaam in en klik op **[!UICONTROL Edit]** op de werkbalk voor bulkacties.

      1. Klik op de tab **[!UICONTROL Upload File]** .

      1. Sleep een bestand naar het vak of klik op **[!UICONTROL Browse Files]** en kies een bestand van uw apparaat of netwerk.

      1. Klik op **[!UICONTROL Save]**.

&#x200B;# Accountgegevens uploaden naar een [!DNL Amazon] [!DNL S3] emmertje {#data-upload-s3}

U kunt een account vullen met inhoud en kosten voor de campagne, klikken en conversiegegevens door de gegevens te uploaden naar een door Zoeken, Sociaal en Commerce toegewezen map in een [!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3]) emmer.

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

>[!PREREQUISITES]
>
>* Neem contact op met uw Adobe-accountteam om het uploaden van accountgegevens voor uw advertentieaccount voor Zoeken, Sociaal en Commerce in te schakelen. Het team zal de verwezenlijking van een organisatie-specifieke omslag in een [!DNL S3] emmer vergemakkelijken, en zij zullen u op de hoogte brengen wanneer het wordt voltooid.<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
>* Haal het [!DNL S3] -pad voor cloudopslag, de toegangstoets-id en de sleutel voor geheime toegang voor uw account op. Dezelfde toegangssleutel-id en geheime toegangssleutel worden gebruikt voor alle <!-- naming convention?--> -accounts van de organisatie die gegevens uploaden.

1. Klik in het hoofdmenu op **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** .

1. Voer een van de volgende handelingen uit:

   * (Vanuit de [!UICONTROL Accounts] -weergave):

      1. Schakel het selectievakje naast de accountnaam in en klik op **[!UICONTROL Upload]** op de werkbalk voor bulkacties.

      1. Klik in het vak [!UICONTROL Cloud Storage Link] op **[!UICONTROL Go to the Link]** .

      1. Klik op **[!UICONTROL Show Access Key and Secret]**.

      1. Klik naast het veld [!UICONTROL Storage Link] op **[!UICONTROL Copy]** om de koppeling naar het klembord te kopiëren en sla de koppeling op een veilige plaats op.

      1. Kopieer en sla de waarden [!UICONTROL Access Key] en [!UICONTROL Secret Key] veilig op.

      1. Klik op **[!UICONTROL Done]**.

   * (Uit de accountinstellingen):

      1. Selecteer de account op een van de volgende manieren:

         * Plaats de cursor boven de accountnaam, klik op **..** en klik vervolgens op **[!UICONTROL Edit]** .

         * Schakel het selectievakje naast de accountnaam in en klik op **[!UICONTROL Edit]** op de werkbalk voor bulkacties.

      1. Klik op de tab **[!UICONTROL Upload File]** .

      1. Klik in het vak [!UICONTROL Cloud Storage Link] op **[!UICONTROL Go to the Link]** .

      1. Klik op **[!UICONTROL Show Access Key and Secret]**.

      1. Klik naast het veld [!UICONTROL Storage Link] op **[!UICONTROL Copy]** om de koppeling naar het klembord te kopiëren en sla de koppeling op een veilige plaats op.

      1. Kopieer en sla de waarden [!UICONTROL Access Key] en [!UICONTROL Secret Key] veilig op.

      1. Klik op **[!UICONTROL Done]**.

      1. Klik op **[!UICONTROL Save]**.

1. (Eenmaal per organisatie) Stel uw lokale AWS-omgeving in:

   1. Download en installeer [!DNL AWS Command Line Interface] (AWS CLI), van de volgende plaats: [&#x200B; https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html &#x200B;](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).

   1. Configureer uw AWS-gebruikersgegevens:

      1. Maak een plaintext bestand en noem dit bestand `~/.aws/credentials` (zonder bestandsextensie).

      1. Open het bestand in een teksteditor en voer de toegangstoets-id van de organisatie en de sleutel voor geheime toegang als volgt in:

         ```
         [default]
         aws_access_key_id = <Access key copied in Step 2>
         aws_secret_access_key = <Secret key copied in Step 2>
         ```

1. Download het rapport met accountgegevens van het advertentienetwerk en sla dit op.

1. Voer in AWS CLI de volgende opdracht uit om uw accountgegevens te uploaden naar de locatie in de [!DNL S3] -cloud.

   ```
   aws s3 cp <local-report-file-location <S3-cloud-location-associated-with-your-account>
   ```

   Voorbeeld: `aws s3 cp filename.txt s3://cloud-location/`

## Een logboek met geüploade bestanden met accountgegevens weergeven

1. Klik in het hoofdmenu op **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** .

1. Plaats de cursor boven de accountnaam, klik op **..** en klik vervolgens op **[!UICONTROL Upload Logs]** .

1. (Facultatief) om de gegevens voor een geupload dossier te downloaden, klik ![&#x200B; Download &#x200B;](/help/search-social-commerce/assets/download.png " in de ") kolom en download het dossier volgens de normale procedure van uw browser.[!UICONTROL Download]

## Vereiste gegevens

De gegevens moeten de gegevensvereisten voor het advertentienetwerk volgen. De gegevensgebieden voor elke entiteit kunnen door ad netwerk variëren.
