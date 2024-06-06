---
title: Gegevens van de post campagne die van voer aan advertentienetwerken worden geproduceerd
description: Leer hoe te om gegevens te posten die van de voer van inventarisgegevens aan advertentienetwerken worden geproduceerd.
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: 2cf15dbab3dc00ec88a41e4f7d8b5b3646b843e8
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Gegevens van de post campagne die van voer aan advertentienetwerken worden geproduceerd

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (alleen handelingen verwijderen), en [!DNL Yandex] alleen accounts*

U kunt campagnegegevens posten die van een voer worden geproduceerd aangezien u de gegevens door de bijbehorende malplaatjes of als afzonderlijk proces verspreidt. Wanneer u gegevens hebt gepost, worden alle bestaande doorgegeven gegevens verwijderd uit de [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] lijsten.

Alle advertentiegroepen moeten aan campagnes worden toegewezen, alle trefwoorden en advertenties moeten worden toegewezen aan advertentiegroepen en alle vereiste informatie moet worden opgenomen zonder overschrijdingen van de lengte.

* Als u de optie &quot;[!UICONTROL Propagate and Preview],&quot; dan [het gegenereerde bulkbladbestand plaatsen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (met de naam &quot;`<feed file name>_<template name>`&quot;) van de [!UICONTROL Bulksheets] weergeven.

  Als u dat niet eerder hebt gedaan [uw openingspagina&#39;s valideren](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md), kunt u dit doen voordat u het bestand plaatst.

* Als u de optie &quot;[!UICONTROL Propagate only],&quot; kunt u de gegenereerde gegevens voor componenten met de [[!UICONTROL New] status](propagated-data-status.md) binnen een campagnehiërarchieweergave vanuit de [!UICONTROL Templates] tab.

  >[!NOTE]
  >
  >Actieve of verwijderde componenten kunnen subcomponenten bevatten die nieuw zijn en de subcomponenten kunnen worden gepost als de gegevens geldig zijn.

  >[!TIP]
  >
  >Als u de bestemmingspagina&#39;s niet eerder hebt gevalideerd en dat wilt doen, dan [gegevens doorgeven en hiervan een voorvertoning weergeven](feed-data-propagate.md) van de [!UICONTROL Bulksheets] in plaats van deze naar het advertentienetwerk te posten. U kunt vervolgens [de URL&#39;s valideren](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) voordat u het bestand handmatig naar het advertentienetwerk publiceert.

   1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, die voor de [!UICONTROL Templates] tab.

   1. Schakel het selectievakje naast de sjabloon in.

   1. Klik op de werkbalk op **[!UICONTROL Post]**.

   1. Typ of selecteer in de postingsinstellingen gegevens in de velden en klik vervolgens op **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** Welke accountcomponenten worden gepost.

      * **[!UICONTROL Scheduling]:** Wanneer het bestand wordt geplaatst:

         * *[!UICONTROL Post to search engine now]* (standaard): hiermee maakt u een bulkbladbestand op basis van de doorgegeven voedergegevens en plaatst u dit bestand direct.

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* Hiermee maakt u een bestand met een werkblad en plaatst u het later. Geef het volgende op:

            * **[!UICONTROL Start Time]:** Een datum en tijd in de toekomst waarop het bulksbladbestand naar het advertentienetwerk moet worden gepost. Standaard wordt het bestand de volgende dag om 00:00 (12:00) verzonden. **Opmerking:** Voor grote dossiers die langere verwerking vereisen, zijn de geposte gegevens niet beschikbaar onmiddellijk binnen de meningen van het campagnebeheer of binnen de manager van de advertentie van het netwerk.

            * **[!UICONTROL End Time]:** Een datum en tijdstip in de toekomst waarop de geposte advertenties kunnen worden gepauzeerd of verwijderd op basis van de [gegevensinstelling feed](feed-settings-manage.md#feed-data-settings) for &quot;[!UICONTROL When the Scheduled End Date is reached].&quot; Standaard is de eindtijd 30 dagen na vandaag om 00:00 (12:00 uur). Selecteren **[!UICONTROL None]** om de gegevens voor onbepaalde tijd actief te houden (of tot u nieuwe gegevens voor het malplaatje) verspreidt, of een datum en een tijd te specificeren.

              Als u een datum wilt opgeven, gebruikt u de notatie DD/MM/JJJJ of D/M/JJJJ of klikt u op ![Kalender](/help/search-social-commerce/assets/calendar.png "Kalender") de kalender te openen en [selecteer een datum](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Als u een tijd wilt wijzigen, voert u de tijd in in de 24-uursnotatie HH/MM of H/M of selecteert u een tijd (met intervallen van 30 minuten) in de lijst.

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** Hiermee maakt u een bulkbladbestand dat beschikbaar is in het dialoogvenster [!UICONTROL Search] > [!UICONTROL Bulksheets] weergeven. U kunt het bestand desgewenst van daaruit posten.

           Als het resulterende bulksheet-bestand groter is dan 2 MB, heeft het bestand de ZIP-indeling. U hoeft het bestand niet uit te pakken om het te posten.

      * **[!UICONTROL Generate Tracking URLs]:** Of URL&#39;s voor bijhouden van trefwoorden en variaties in het bulksheet-bestand moeten worden opgenomen: *[!UICONTROL Yes]* (de standaardwaarde) of *[!UICONTROL No]*.

        Als u *[!UICONTROL Yes]*, worden de URL&#39;s gegenereerd op basis van de basis-URL&#39;s voor de trefwoorden en advertenties volgens de [!UICONTROL Tracking Methods] in de [accountinstellingen](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) of, als u gegevens toewijst aan bestaande campagnes, aan [!UICONTROL Tracking Methods] in de bestaande [campagne-instellingen](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

        Als URL&#39;s bijhouden voor de relevante items bestaat, worden deze alleen opnieuw gegenereerd als er nieuwe URL&#39;s nodig zijn (bijvoorbeeld als het trefwoordtype overeenkomen, de creatieve tekst of de trackingparameters van de account zijn gewijzigd).

      * **[!UICONTROL Bulksheet Name]:** De naam van het bulksbladbestand dat moet worden gemaakt op basis van de doorgegeven doorvoergegevens. Standaard krijgt het bestand de naam `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. U kunt de naam van het bestand wijzigen, maar het bestand moet eindigen met een van de volgende bestandsextensies: `.tsv` (voor tabgescheiden waarden), `.txt` (voor ASCII-tekst), `.csv` (voor door komma&#39;s gescheiden waarden), of `.zip` (voor een gecomprimeerd TSV-bestand). Voor gegevens die internationale karakters omvatten, gebruik TSV of formaat TXT.

        Het geposte bestand is beschikbaar in het dialoogvenster [!UICONTROL Bulksheets] mening gedurende 30 dagen, of u het aan het advertentienetwerk post.

De &quot;[!UICONTROL Last Prop. Status]&quot; de kolom toont de baanstatus voor de toepasselijke malplaatjes.

Wanneer het bulksblad wordt gecreeerd, is het vermeld in [!UICONTROL Bulksheets] weergeven. Wanneer het bestand wordt gepost, wordt een e-mailbericht verzonden met een koppeling naar het bestand. Als alle of sommige gegevens echter niet kunnen worden gepost, wordt een foutbestand weergegeven in het dialoogvenster [!UICONTROL Bulksheets] en er wordt een e-mailmelding verzonden met een koppeling naar het foutbestand.

>[!NOTE]
>
>* Ongeacht de optie die u hebt geselecteerd voor planning, worden de opgegeven gegevens verwijderd uit het dialoogvenster [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] lijsten.
>* Het duurt langer om grote hoeveelheden gegevens te verwerken. U kunt de voortgang van het bestand tijdens het proces volgen.
>* Alle geposte gegevens zijn onderworpen aan het redactionele proces van het netwerk.
>* Voordat een bulksbladbestand wordt geplaatst, kunt u [posten annuleren](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [Informatie over voorraadfeeds](inventory-feeds-about.md)
>* [Gegevens weergeven die zijn gegenereerd uit feeds](propagated-data-view.md)
>* [Uit feeds gegenereerde gegevens bewerken](propagated-data-edit.md)
>* [Een publicatietaak voor de gegevens van de inventarisfeed stoppen](stop-job.md)
>* [Statussen van gegevens die zijn gegenereerd uit feeds](propagated-data-status.md)
