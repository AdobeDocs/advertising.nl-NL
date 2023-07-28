---
title: Over het volgen voor Zoeken, Sociale Zaken en Handel
description: Meer informatie over opties voor Zoeken, Sociale Zaken en Handel.
exl-id: 0a26f67c-8b3b-4fa1-ac24-a8461624cfc5
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
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

Uw implementatieteam voor Zoeken, Sociale Zaken en Handel stelt klikvolgen in door de volgende sjablonen en doel-URL&#39;s voor advertenties, trefwoorden, plaatsingen, productgroepen en sitelink-extensies bij te werken in uw gesynchroniseerde advertentiecampagnes, zodat deze een unieke id-tekenreeks voor het bijhouden en een omleiding van de Adobe Advertising bevatten. Ze voegen ook het bijhouden van de achtervoegsels voor de landpagina (laatste URL-achtervoegsels) toe aan uw [!DNL Google Ads] en [!DNL Microsoft Advertising] accounts en campagnes.

Met de volgende parameters kan de Adobe Advertising klikken bijhouden op een afzonderlijk trefwoordniveau (zoekcampagnes) of op variatieniveau (zoekcampagnes met inhoud of doellocatie, weergavecampagnes en sociale campagnes). Telkens wanneer een gebruiker een weergave/inhoud bekijkt en of op een van uw advertenties klikt, verzendt het advertentienetwerk de gebeurtenis naar de pixelservers van de Adobe Advertising met behulp van een kliktrackingtag die aan het trefwoord of de advertentie is gekoppeld. Voor klikken:

* Voor advertenties van Google Ads en Microsoft op browsers die parallelle tracering steunen, verzendt het advertentienetwerk de klik eerst naar uw website en dan naar de Adobe Advertising pixelservers, die dan een koekje op de computer van de gebruiker plaatsen, als men niet reeds bestaat.

* In alle andere gevallen verzendt het advertentienetwerk de klik rechtstreeks naar de pixelservers van de Adobe Advertising. De pixelserver plaatst een cookie op de computer van de gebruiker (als deze nog niet bestaat) en leidt de gebruiker vervolgens om naar de relevante URL op uw website. De algemene ervaring voor de eindgebruiker is hetzelfde als zonder omleiding.

Het cookie wordt ingesteld in het dialoogvenster [!DNL Adobe] domain (`everesttech.net`) als een eersteklas cookie. Na een omleiding bevindt de gebruiker zich in het domein van de adverteerder en wordt het cookie vervolgens behandeld als een cookie van een derde. Voor meer informatie over Adobe Advertising koekjes, zie &quot;[Cookies Adoben Advertising](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html).&quot;

## Conversiegegevens

Wanneer een klant op een advertentie klikt of een display of sociale advertentie weergeeft, moet Zoeken, Sociaal en Handel elke resulterende conversie opnieuw toewijzen aan de oorspronkelijke klik of weergave/sociale indruk.

De adverteerder speelt een rol bij het leveren van de conversiegegevens voor alle klikken en weergave-/sociale indrukkingen. Conversiegegevens kunnen informatie bevatten over elk type gebeurtenis dat zich op een website voordoet en dat kan worden gebruikt voor het optimaliseren van biedingen. U kunt conversiegegevens opgeven door conversietraccode te implementeren in de conversiepagina&#39;s van de adverteerder (zoals de pagina &quot;success&quot; die wordt weergegeven nadat een klant een transactie heeft voltooid) of door een dagelijks feed-bestand te verzenden met conversiegegevens die door een andere methode zijn vastgelegd.

### Tags voor conversie bijhouden

U kunt [conversietags van verschillende leveranciers](/help/search-social-commerce/tracking/conversion-tracking-about.md).

Wanneer u een conversietag van de Adobe Advertising gebruikt en een gebruiker een succesvolle transactie voltooit en op een &quot;succes&quot;pagina landt, controleert de de pixelserver van de Adobe Advertising op het bestaan van het koekje op de computer van de gebruiker, die op het tijdstip van de klik redirect werd geplaatst. Wanneer het een koekje vindt, wordt de informatie over de transactiegebeurtenis overgegaan gebruikend de ef_transid parameter, en de transactie wordt erkend als omzetting en aan de voorafgaande en klik of vertoningsindruk gecrediteerd.

Als de gebruiker op meer dan een advertentie heeft geklikt, geeft de Adobe Advertising de transactie door aan de eindgebruiker en klikt (voor weergave- of videocampagnes) de laatste advertentie, tenzij u een andere advertentie opgeeft. Uw [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j) bepaalt het aantal dagen nadat een betaalde klik of een vertoning/video indruk (respectievelijk) voorkomt waarin de gebeurtenis aan een omzetting kan worden toegeschreven.

Het Adobe Advertising-implementatieteam werkt samen met de adverteerder om de indeling van de conversietags te bepalen die de adverteerder moet implementeren, de webpagina&#39;s te identificeren waarop elke conversietag moet worden ingevoegd en vervolgens de conversietags te leveren die moeten worden geïmplementeerd.
