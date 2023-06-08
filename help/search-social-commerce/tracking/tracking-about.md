---
title: Over het volgen voor Zoeken, Sociale Zaken en Handel
description: Meer informatie over opties voor Zoeken, Sociale Zaken en Handel.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Over het volgen voor Zoeken, Sociale Zaken en Handel

Als je de prestaties van je advertenties wilt volgen, moet je op Zoeken, Sociale Zaken en Handel indruk maken, klikken, kosten en conversie (transactie) gegevens voor je advertenties. Zoekopdrachten, sociale zaken en handel maken gebruik van deze gegevens om modellen voor gegevensprognoses te maken die nodig zijn om uw advertentieportfolio&#39;s te optimaliseren.

## Kosten-, klik- en afbeeldingsgegevens

Met Zoeken, Sociaal zoeken en Handel kunt u direct uit de gegevens over afbeeldingen de indruk, klik en kosten ophalen [ondersteunde advertentienetwerken](/help/search-social-commerce/introduction/supported-inventory.md) elke dag. Daarnaast kunt u met Zoeken, Sociaal zoeken en Handel een unieke code voor het bijhouden van klikken toevoegen (inclusief een omleiding naar een trackingserver) in uw trackingsjablonen en doel-URL&#39;s om weergave-/inhoudsindrukkingen bij te houden, te klikken en kosten op te nemen en de gebeurtenissen later aan conversies te koppelen.

Als u campagnes wilt volgen op advertentienetwerken waarmee Onderzoek, Sociale, &amp; Handel geen gegevens synchroniseert, dan moet u gegevens voor die campagnes verstrekken door een dagelijks voederdossier met de indruk, de klik, en kostengegevens te verzenden.

### Labels voor bijhouden van klikken

Uw implementatieteam voor Zoeken, Sociale Zaken en Handel stelt kliktracking in door de tracingsjablonen en doel-URL&#39;s voor advertenties, trefwoorden, plaatsingen, productgroepen en sitelink-extensies bij te werken in uw gesynchroniseerde advertentiecampagnes, zodat deze een unieke id-tekenreeks voor bijhouden en een Adobe Advertising-omleiding bevatten. Ze voegen ook het bijhouden van de achtervoegsels voor de landpagina (laatste URL-achtervoegsels) toe aan uw [!DNL Google Ads] en [!DNL Microsoft Advertising] accounts en campagnes.

Met behulp van de volgende parameters kunnen Adobe-advertenties klikken bijhouden op een afzonderlijk trefwoordniveau (zoekcampagnes) of variatieniveau (zoekcampagnes met inhoud of doellocatie, weergavecampagnes en sociale campagnes). Telkens wanneer een gebruiker een weergave/inhoud bekijkt en of op een van uw advertenties klikt, verzendt het advertentienetwerk de gebeurtenis naar de Adobe Advertising pixelservers met behulp van een kliktrackingtag die aan het trefwoord of de advertentie is gekoppeld. Voor klikken:

* Voor advertenties in Google Ads en Microsoft op browsers die parallelle tracering ondersteunen, stuurt het advertentienetwerk de klik eerst naar uw website en vervolgens naar de Adobe Advertising-pixelservers, die vervolgens een cookie op de computer van de gebruiker plaatsen, als er nog geen cookie is.

* In alle andere gevallen verzendt het advertentienetwerk de klik rechtstreeks naar de Adobe Advertising pixelservers. De pixelserver plaatst een cookie op de computer van de gebruiker (als deze nog niet bestaat) en leidt de gebruiker vervolgens om naar de relevante URL op uw website. De algemene ervaring voor de eindgebruiker is hetzelfde als zonder omleiding.

Het cookie wordt ingesteld in het dialoogvenster [!DNL Adobe] domain (`everesttech.net`) als een eersteklas cookie. Na een omleiding bevindt de gebruiker zich in het domein van de adverteerder en wordt het cookie vervolgens behandeld als een cookie van een derde. Raadpleeg voor meer informatie over Adobe-advertentiecookies &quot;[Adobe Reclamecookies](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html).&quot;

## Conversiegegevens

Wanneer een klant op een advertentie klikt of een display of sociale advertentie weergeeft, moet Zoeken, Sociaal en Handel elke resulterende conversie opnieuw toewijzen aan de oorspronkelijke klik of weergave/sociale indruk.

De adverteerder speelt een rol bij het leveren van de conversiegegevens voor alle klikken en weergave-/sociale indrukkingen. Conversiegegevens kunnen informatie bevatten over elk type gebeurtenis dat zich op een website voordoet en dat kan worden gebruikt voor het optimaliseren van biedingen. U kunt conversiegegevens opgeven door conversietraccode te implementeren in de conversiepagina&#39;s van de adverteerder (zoals de pagina &quot;success&quot; die wordt weergegeven nadat een klant een transactie heeft voltooid) of door een dagelijks feed-bestand te verzenden met conversiegegevens die door een andere methode zijn vastgelegd.

### Tags voor conversie bijhouden

U kunt [conversietags van verschillende leveranciers](/help/search-social-commerce/tracking/conversion-tracking-about.md).

Wanneer u een conversietag voor Adobe-reclame gebruikt en een gebruiker een geslaagde transactie voltooit en op een pagina met succesmeldingen landt, controleert de Adobe Advertising pixelserver of het cookie op de computer van de gebruiker aanwezig is, die was ingesteld op het moment dat de klik werd omgeleid. Wanneer het een koekje vindt, wordt de informatie over de transactiegebeurtenis overgegaan gebruikend de ef_transid parameter, en de transactie wordt erkend als omzetting en aan de voorafgaande en klik of vertoningsindruk gecrediteerd.

Als de gebruiker op meerdere van uw advertenties heeft geklikt, krijgt de Adobe-advertentie een creditering van de transactie met de uiteindelijke advertentie of klikt (voor weergave- of videocampagnes) de uiteindelijke advertentie, tenzij u anders opgeeft. Uw [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j) bepaalt het aantal dagen nadat een betaalde klik of een vertoning/video indruk (respectievelijk) voorkomt waarin de gebeurtenis aan een omzetting kan worden toegeschreven.

Het Adobe Advertising Implementation-team werkt samen met de adverteerder om de indeling van de conversietags te bepalen die de adverteerder moet implementeren, de webpagina&#39;s te identificeren waarop elke conversietag moet worden ingevoegd en vervolgens de conversietags te leveren die moeten worden geïmplementeerd.
