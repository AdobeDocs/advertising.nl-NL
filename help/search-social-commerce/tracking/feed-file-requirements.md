---
title: Bestandsvereisten voor de conversie van feed-bestanden
description: Verwijs naar de vereisten voor conversievoederbestanden.
exl-id: 7d865802-0ab9-4965-9618-6bc0667f4939
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---

# Bestandsvereisten voor de conversie van feed-bestanden

Hieronder vindt u de vereisten voor de bestandsindeling, vereiste en optionele gegevensvelden, bestandsnaam en protocol voor bestandsoverdracht voor feed-bestanden.

## Bestandsindeling

Het gegevensbestand moet in vlakke tekst (TXT), komma-gescheiden waarden (CSV), of lusje-gescheiden waarden (TSV) formaat zijn. Het bestand kan bestaan uit een koptekstrij en gegevensrijen met waarden die worden gescheiden door tabs, komma&#39;s of een ander teken (maar geen spaties):

* **Koptekstrij:** (Optioneel) De eerste regel van het bestand is een koptekst die de vereiste veldnamen (of kolomnamen) in een bepaalde volgorde opgeeft, gescheiden door tabs of komma&#39;s. De vereiste kolomnamen omvatten de transactieeigenschappen die de Adobe Advertising als omzettingen volgt.

* **Gegevensrijen:** Elke volgende regel bevat gegevensvelden in dezelfde volgorde als de koptekst en gescheiden door tabs of komma&#39;s. Als de eerste record geen koptekst is, moet elke gegevensrij alle mogelijke velden in een opgegeven volgorde bevatten. De waarden van alle id&#39;s en transactieeigenschappen moeten alfanumeriek zijn.

  Wanneer meerdere klikken op een of meerdere advertenties tot één transactie leiden, moet u de klik-id en de volgende-id bepalen waaraan u de transactie wilt toewijzen. Omdat voor elke transactie een unieke id wordt gerapporteerd, kunt u afzonderlijke transacties bijwerken.

## Naamgevingsconventie voor bestanden

De bestandsnaam moet de datum bevatten en consistent zijn. Als u bijvoorbeeld de notatie YYYYMMDD.txt gebruikt, moet een bestand dat op 15 mei 2011 wordt verzonden de naam 20110515.txt hebben.

## Protocol voor bestandsoverdracht

Verzend het bestand via het SFTP-overdrachtsprotocol met poort 22. U moet uw openbare-sleutelgegevens opgeven.  Uw Adobe Account Team of het implementatieteam zal u de serverplaats samen met de geloofsbrieven verstrekken die voor uw systeem worden vereist om de dossiers over te brengen.

>[!TIP]
>
>Conversiegegevensfeeds worden meerdere keren per dag verwerkt. Upload de dagelijkse voer zo spoedig mogelijk na 23:00 lokale tijd om middernacht zodat de Adobe Advertising uw gegevens kan verwerken en het in de rapporteringsUI in de vroege ochtend ter beschikking stellen.

>[!MORELIKETHIS]
>
>* [Gegevensvereisten voor gegevensfeeds die gebruikmaken van EF-id&#39;s](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
>* [Gegevensvereisten voor gegevensfeeds met een transactie-id](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
