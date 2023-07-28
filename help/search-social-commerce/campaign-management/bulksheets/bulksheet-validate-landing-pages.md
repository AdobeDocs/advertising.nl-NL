---
title: Openingspagina's in bulkbladbestanden valideren
description: Leer hoe u de doel-URL's valideert in een bulksheet-bestand voor één account.
exl-id: cf703687-1151-46f6-9540-12a83d41dfc8
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Openingspagina&#39;s in bulkbladbestanden valideren

*Accounts met alleen doel-URL&#39;s*

U kunt de openingspagina&#39;s in alle doel-URL&#39;s valideren in een bulksheet-bestand voor één account. U kunt om het even welke uitdrukkingen en URLs specificeren die op een ongeldige pagina wijzen en naar keuze het landen van de pagina omleiden als fouten melden. Zoek-, sociale en handelscontroles op de opgegeven voorwaarden en op ontbrekende bestemmingspagina&#39;s (die resulteren in HTTP 404- of &quot;Niet gevonden&quot;-fouten).

Als er fouten worden gevonden, maakt u met Zoeken, Sociaal en Handel een foutbestand met een opsommingsteken dat alle rijen in het oorspronkelijke bulksblad bevat en foutberichten voor alle rijen met een ongeldige bestemmingspagina. De fouten worden vermeld in het [!UICONTROL EF Errors] kolom. De bestandsnaamregel is `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

U kunt het bestand later downloaden, de fouten corrigeren en het gecorrigeerde bestand uploaden en het gecorrigeerde bestand vervolgens naar de netwerkaccount van de advertentie posten.

>[!NOTE]
>
>* Deze functie valideert geen waarden in de kolom Basis-URL/Definitieve URL.
>* U kunt bladbestanden met opsommingstekens plaatsen terwijl deze worden gevalideerd, of zelfs als er fouten worden gevonden.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Schakel het selectievakje in naast elk bestand dat u wilt valideren.

1. Klik op de werkbalk boven de tabel met gegevens op **[!UICONTROL Validate URLs]**.

1. Voer in het dialoogvenster informatie in de velden in en klik vervolgens op **[!UICONTROL Apply]**:

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]:** Tekst in de hoofdtekst van een openingspagina die aangeeft dat de pagina ongeldig is. Als u meerdere waarden wilt opgeven, voert u deze op aparte regels in.

   **[!UICONTROL Enter invalid landing pages(one per line):]** De URL&#39;s van pagina&#39;s die ongeldig zijn als bestemmingspagina&#39;s. Als u meerdere waarden wilt opgeven, voert u deze op aparte regels in.

   **[!UICONTROL User Agent:]** Hoe de validatieagent van de landingspagina wordt geïdentificeerd aan de webserver waarop de landingspagina zich bevindt. Het gebrek is gebrek, dat meningen door de agent aan anonieme attributen kenmerkt [!DNL Mozilla Firefox] gebruiker. Als de webserver aanvragen van anonieme [!DNL Mozilla Firefox] gebruikers, dan ga de naam van een verschillende agent in. Bijvoorbeeld: [!DNL Googlebot], enter `Googlebot/2.1;+http://www.google.com/bot.html`.

   **[!UICONTROL Report redirects as errors]:** Wanneer een bestemmingspagina naar een andere pagina wordt omgeleid (bijvoorbeeld als de landingspagina ontbreekt en de site een vervangende pagina weergeeft), wordt de [!UICONTROL ER Errors] in het foutbestand van de bestemmingspagina wordt de URL aangegeven waarnaar de bestemmingspagina wordt omgeleid.

Wanneer de taak begint, wordt een nieuwe rij toegevoegd aan [!UICONTROL Bulksheets view]. Wanneer het bestand is gemaakt, wordt een e-mailbericht verzonden met een koppeling naar het bestand. Afhankelijk van de hoeveelheid gecompileerde gegevens kan het e-mailbericht enkele minuten of langer duren. U kunt het bestand downloaden om het te bewerken en vervolgens opnieuw uploaden om het te posten, of u kunt het bestand ongewijzigd plaatsen. Als het genereren van het bestand echter mislukt, wordt een foutbestand weergegeven in het dialoogvenster [!UICONTROL Bulksheet Management] en er wordt een e-mailmelding verzonden met een koppeling naar het foutbestand.

>[!NOTE]
>
>* Het duurt langer om grote bestanden te valideren.
>* Bulksheet-bestanden voor meerdere campagnes kunnen maximaal 500.000 gegevensrijen bevatten. Als u gegevens voor veelvoudige campagnes produceert en de gecombineerde gegevens uit meer dan 500.000 rijen bestaan, dan worden de gegevens verdeeld door campagne in twee of meer dossiers genoemd `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`, enzovoort.

>[!MORELIKETHIS]
>
>* [Campagnegegevens beheren met behulp van bulksbladen](bulksheet-about.md)
>* [Geüploade bulksbladen en foutbestanden verwijderen](bulksheet-delete.md)
>* [Kolommen of gecorrigeerde foutbestanden plaatsen](bulksheet-post.md)
>* [Een bulkbladtaak onderbreken](bulksheet-stop-job.md)
>* [Upload een bulksheet of een gecorrigeerd foutbestand](bulksheet-upload.md)
>* [Een gegenereerd of geüpload bulksbladbestand exporteren](bulksheet-export.md)
