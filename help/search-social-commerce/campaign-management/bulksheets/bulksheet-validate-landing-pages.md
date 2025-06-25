---
title: Openingspagina's in bulkbladbestanden valideren
description: Leer hoe u de doel-URL's valideert in een bulksheet-bestand voor één account.
exl-id: 191cb1bc-54a9-4c6c-a29c-f3cbae08e0d8
feature: Search Bulksheets
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Openingspagina&#39;s in bulkbladbestanden valideren

*Rekeningen met slechts doel URLs*

U kunt de openingspagina&#39;s in alle doel-URL&#39;s valideren in een bulksheet-bestand voor één account. U kunt om het even welke uitdrukkingen en URLs specificeren die op een ongeldige pagina wijzen en naar keuze het landen van de pagina omleiden als fouten melden. Zoek-, sociale en Commerce-controles op de opgegeven voorwaarden en op ontbrekende bestemmingspagina&#39;s (die resulteren in HTTP 404- of &quot;Niet gevonden&quot;-fouten).

Als er fouten worden gevonden, maken Zoeken, Sociaal en Commerce een foutbestand voor het bulksheet dat alle rijen bevat in het oorspronkelijke bulksheet en foutberichten voor alle rijen met een ongeldige bestemmingspagina. De fouten worden vermeld in de kolom [!UICONTROL EF Errors] . De bestandsnaamconventie is `<bulksheet name>__lpv_errors.<extension used for the bulksheet>` .

U kunt het bestand later downloaden, de fouten corrigeren en het gecorrigeerde bestand uploaden en het gecorrigeerde bestand vervolgens naar de netwerkaccount van de advertentie posten.

>[!NOTE]
>
>* Deze functie valideert geen waarden in de kolom Basis-URL/Definitieve URL.
>* U kunt bladbestanden met opsommingstekens plaatsen terwijl deze worden gevalideerd, of zelfs als er fouten worden gevonden.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]** .

1. Schakel het selectievakje in naast elk bestand dat u wilt valideren.

1. Klik in de werkbalk boven de gegevenstabel op **[!UICONTROL Validate URLs]** .

1. Voer in het dialoogvenster informatie in de velden in en klik op **[!UICONTROL Apply]** :

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]:** Tekst in de tekst van een openingspagina die aangeeft dat de pagina ongeldig is. Als u meerdere waarden wilt opgeven, voert u deze op aparte regels in.

   **[!UICONTROL Enter invalid landing pages(one per line):]** De URL&#39;s van pagina&#39;s die ongeldig zijn als bestemmingspagina&#39;s. Als u meerdere waarden wilt opgeven, voert u deze op aparte regels in.

   **[!UICONTROL User Agent:]** Hoe de validatieagent voor de bestemmingspagina wordt geïdentificeerd aan de webserver waarop de bestemmingspagina zich bevindt. Het gebrek is gebrek, dat meningen door de agent aan een anonieme [!DNL Mozilla Firefox] gebruiker kenmerkt. Als de webserver aanvragen van anonieme [!DNL Mozilla Firefox] gebruikers blokkeert, voert u de naam van een andere agent in. Typ bijvoorbeeld bij [!DNL Googlebot] `Googlebot/2.1;+http://www.google.com/bot.html` .

   **[!UICONTROL Report redirects as errors]:** wanneer een landingspagina naar een andere pagina wordt omgeleid (bijvoorbeeld als de landingspagina ontbreekt en de site een vervangende pagina weergeeft), geeft de [!UICONTROL ER Errors] -kolom in het foutbestand van de bestemmingspagina de URL aan waarnaar de landingspagina wordt omgeleid.

Wanneer de taak begint, wordt een nieuwe rij toegevoegd aan [!UICONTROL Bulksheets view]. Wanneer het bestand is gemaakt, wordt een e-mailbericht verzonden met een koppeling naar het bestand. Afhankelijk van de hoeveelheid gecompileerde gegevens kan het e-mailbericht enkele minuten of langer duren. U kunt het bestand downloaden om het te bewerken en vervolgens opnieuw uploaden om het te posten, of u kunt het bestand ongewijzigd plaatsen. Als het genereren van het bestand echter mislukt, wordt een foutbestand weergegeven op de pagina [!UICONTROL Bulksheet Management] en wordt een e-mailmelding verzonden met een koppeling naar het foutbestand.

>[!NOTE]
>
>* Het duurt langer om grote bestanden te valideren.
>* Bulksheet-bestanden voor meerdere campagnes kunnen maximaal 500.000 gegevensrijen bevatten. Als u gegevens voor meerdere campagnes genereert en de gecombineerde gegevens uit meer dan 500.000 rijen bestaan, worden de gegevens op campagne gesplitst in twee of meer bestanden met de naam `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv` enzovoort.

>[!MORELIKETHIS]
>
>* [ Ongeveer het beheren van campagnegegevens gebruikend bulksbladen ](bulksheet-about.md)
>* [ Schrap geüploade bulksbladen en foutendossiers ](bulksheet-delete.md)
>* [ Post bulksbladen of gecorrigeerde foutendossiers ](bulksheet-post.md)
>* [ Einde een bulksbladbaan lopend ](bulksheet-stop-job.md)
>* [ upload een bulksheet of verbeterd foutendossier ](bulksheet-upload.md)
>* [ de Uitvoer een geproduceerd of geupload bulksbladdossier ](bulksheet-export.md)
