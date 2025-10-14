---
title: Gegevens van de post campagne die van voer aan advertentienetwerken worden geproduceerd
description: Leer hoe te om gegevens te posten die van de voer van inventarisgegevens aan advertentienetwerken worden geproduceerd.
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Gegevens van de post campagne die van voer aan advertentienetwerken worden geproduceerd

*[!DNL Google Ads], [!DNL Microsoft Advertising] , [!DNL Yahoo! Japan Ads] (alleen acties verwijderen) en [!DNL Yandex] alleen accounts*

U kunt campagnegegevens posten die van een voer worden geproduceerd aangezien u de gegevens door de bijbehorende malplaatjes of als afzonderlijk proces verspreidt. Nadat u gegevens hebt gepost, worden bestaande doorgegeven gegevens verwijderd uit de lijsten [!UICONTROL Campaigns] , [!UICONTROL Ad Groups] , [!UICONTROL Keywords] en [!UICONTROL Ads] .

Alle advertentiegroepen moeten aan campagnes worden toegewezen, alle trefwoorden en advertenties moeten worden toegewezen aan advertentiegroepen en alle vereiste informatie moet worden opgenomen zonder overschrijdingen van de lengte.

* Als u de optie aan &quot;[!UICONTROL Propagate and Preview] gebruikte,&quot;dan [&#x200B; post het geproduceerde bulksbladdossier &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (genoemd &quot;`<feed file name>_<template name>`&quot;) van de [!UICONTROL Bulksheets] mening.

  Als u niet eerder [&#x200B; uw het landen pagina&#39;s &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) bevestigde, dan kunt u dit doen alvorens u het dossier post.

* Als u de optie aan &quot;[!UICONTROL Propagate only] gebruikte,&quot;dan kunt u de geproduceerde gegevens voor componenten met [[!UICONTROL New] status &#x200B;](propagated-data-status.md) binnen een mening van de campagnehiërarchie van het [!UICONTROL Templates] lusje posten.

  >[!NOTE]
  >
  >Actieve of verwijderde componenten kunnen subcomponenten bevatten die nieuw zijn en de subcomponenten kunnen worden gepost als de gegevens geldig zijn.

  >[!TIP]
  >
  >Als u niet eerder uw het landen pagina&#39;s bevond en dit wilt doen, dan [&#x200B; verspreidt gegevens en voorproef het &#x200B;](feed-data-propagate.md) van de [!UICONTROL Bulksheets] mening in plaats van het te posten aan het advertentienetwerk. U kunt dan [&#x200B; URLs &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) bevestigen alvorens het dossier aan het advertentienetwerk manueel te posten.

   1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** , dat wordt geopend op de tab [!UICONTROL Templates] .

   1. Schakel het selectievakje naast de sjabloon in.

   1. Klik in de werkbalk op **[!UICONTROL Post]** .

   1. Voer in de postingsinstellingen gegevens in de velden in of selecteer deze en klik op **[!UICONTROL Post]** .

      * **[!UICONTROL Selection]:** Welke accountcomponenten worden gepost.

      * **[!UICONTROL Scheduling]:** Wanneer het bestand wordt geplaatst:

         * *[!UICONTROL Post to search engine now]* (standaard): hiermee maakt u een bulkbladbestand op basis van de doorgegeven voedergegevens en wordt het bestand direct gepost.

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* hiermee maakt u een bestand met een opsommingsteken en plaatst u het later. Geef het volgende op:

            * **[!UICONTROL Start Time]:** Een datum en tijd in de toekomst waarop het bulksbladbestand naar het advertentienetwerk moet worden gepost. Standaard wordt het bestand de volgende dag om 00:00 (12:00) verzonden. **Nota:** voor grote dossiers die langere verwerking vereisen, zijn de geposte gegevens niet onmiddellijk beschikbaar binnen de meningen van het campagnebeheer of binnen de manager van de advertentie van het netwerk.

            * **[!UICONTROL End Time]:** Een toekomstige datum en tijd waarbij de geposte advertenties kunnen worden gepauzeerd of worden geschrapt gebaseerd op [&#x200B; het plaatsen van voedergegevens &#x200B;](feed-settings-manage.md#feed-data-settings) voor &quot;[!UICONTROL When the Scheduled End Date is reached].&quot; Standaard is de eindtijd 30 dagen na vandaag om 00:00 (12:00 uur). Selecteer **[!UICONTROL None]** om de gegevens actief te houden voor onbepaalde tijd (of tot u nieuwe gegevens voor het malplaatje) verspreidt, of een datum en een tijd te specificeren.

              Om een datum te specificeren, gebruik het formaat DD/MM/JJJJ of D/M/JJJJ of klik ![&#128279;](/help/search-social-commerce/assets/calendar.png " Kalender ") om de kalender te openen en [&#x200B; een datum &#x200B;](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md) te selecteren.  Als u een tijd wilt wijzigen, voert u de tijd in in de 24-uursnotatie HH/MM of H/M of selecteert u een tijd (met intervallen van 30 minuten) in de lijst.

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** hiermee maakt u een bulkbladbestand dat beschikbaar is in de weergave [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Bulksheets] . U kunt het bestand desgewenst van daaruit posten.

           Als het resulterende bulksheet-bestand groter is dan 2 MB, heeft het bestand de ZIP-indeling. U hoeft het bestand niet uit te pakken om het te posten.

      * **[!UICONTROL Generate Tracking URLs]:** Of URL&#39;s voor bijhouden van trefwoorden en variaties in het bulksbladbestand moeten worden opgenomen: *[!UICONTROL Yes]* (de standaardinstelling) of *[!UICONTROL No]* .

        Als u *[!UICONTROL Yes]* selecteert, dan wordt URLs geproduceerd van basis URLs voor de sleutelwoorden en advertenties volgens de [!UICONTROL Tracking Methods] parameters in de [&#x200B; rekeningsmontages &#x200B;](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) of, als u gegevens aan bestaande campagnes in kaart brengt, aan de [!UICONTROL Tracking Methods] parameters in de bestaande [&#x200B; campagnecontages &#x200B;](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

        Als URL&#39;s bijhouden voor de relevante items bestaat, worden deze alleen opnieuw gegenereerd als er nieuwe URL&#39;s nodig zijn (bijvoorbeeld als het trefwoordtype overeenkomen, de creatieve tekst of de trackingparameters van de account zijn gewijzigd).

      * **[!UICONTROL Bulksheet Name]:** De naam van het bulksbladdossier om van de propagated voedergegevens tot stand te brengen. Standaard krijgt het bestand de naam `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt` . U kunt de naam van het bestand desgewenst wijzigen, maar het bestand moet eindigen met een van de volgende bestandsextensies: `.tsv` (voor waarden met tabs als scheidingsteken), `.txt` (voor ASCII-tekst), `.csv` (voor waarden met komma&#39;s als scheidingsteken) of `.zip` (voor een gecomprimeerd TSV-bestand). Voor gegevens die internationale karakters omvatten, gebruik TSV of formaat TXT.

        Het geposte bestand is 30 dagen beschikbaar in de weergave [!UICONTROL Bulksheets] , of u het nu op het advertentienetwerk plaatst of niet.

De kolom &quot;[!UICONTROL Last Prop. Status]&quot;toont de baanstatus voor de toepasselijke malplaatjes.

Wanneer het bulksblad wordt gecreeerd, is het vermeld in de [!UICONTROL Bulksheets] mening. Wanneer het bestand wordt gepost, wordt een e-mailbericht verzonden met een koppeling naar het bestand. Als alle of sommige gegevens echter niet kunnen worden gepost, wordt een foutbestand weergegeven in de weergave [!UICONTROL Bulksheets] en wordt een e-mailmelding verzonden met een koppeling naar het foutbestand.

>[!NOTE]
>
>* Ongeacht de optie voor het plannen die u hebt geselecteerd, worden de opgegeven gegevens verwijderd uit de lijsten [!UICONTROL Campaigns] , [!UICONTROL Ad Groups] , [!UICONTROL Keywords] en [!UICONTROL Ads] .
>* Het duurt langer om grote hoeveelheden gegevens te verwerken. U kunt de voortgang van het bestand tijdens het proces volgen.
>* Alle geposte gegevens zijn onderworpen aan het redactionele proces van het netwerk.
>* Alvorens een bulksbladdossier wordt gepost, kunt u [&#x200B; het posten &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md) annuleren.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer inventarisvoer &#x200B;](inventory-feeds-about.md)
>* [&#x200B; gegevens van de Mening die van voer &#x200B;](propagated-data-view.md) worden geproduceerd
>* [&#x200B; geeft gegevens uit die van voer &#x200B;](propagated-data-edit.md) worden geproduceerd uit
>* [&#x200B; Einde een het posten baan voor de gegevens van het inventarisvoer &#x200B;](stop-job.md)
>* [&#x200B; Statussen van gegevens die uit voer &#x200B;](propagated-data-status.md) worden geproduceerd
