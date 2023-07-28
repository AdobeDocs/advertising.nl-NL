---
title: Ondersteunde bestandsindelingen voor bulksbladen
description: Verwijs naar de algemene dossiervereisten voor bulksbladen.
exl-id: b14aaf11-e2e9-4f7c-b6bc-831f668b93a6
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# Ondersteunde bestandsindelingen voor bulksbladen

## Bestandsindelingen

U kunt bulksbladbestanden voor ondersteunde advertentienetwerken in de volgende indelingen downloaden, uploaden en posten:

* CSV (door komma&#39;s gescheiden waarden)
* TSV (door tabs gescheiden waarden)
* TXT (Unicode-tekst), gescheiden door komma&#39;s of tabs
* ZIP (gecomprimeerd) met één bestand in CSV-indeling, TSV-indeling of TXT-indeling dat is gescheiden door komma&#39;s of tabs

Wanneer u een werkblad maakt/downloadt, wordt dit gemaakt in de opgegeven bestandsindeling met alle relevante gegevens in het bestand. Gebruik de volgende informatie om gegevens in het bestand te bewerken of om handmatig uw eigen werkblad te maken.

## Basisinhoud van een bulksblad

De eerste record (regel) van een bulksheet-bestand bevat een set specifieke kolomnamen, gezamenlijk bekend als een <i>header</i>. De kolomnamen in de koptekst hebben een opgegeven volgorde en komen overeen met elk van de velden in de volgende gegevensrecords. De kolomnamen die in de kopbal worden vereist variëren door ad netwerk.

Elke volgende record (regel) bevat gegevens, met velden met waarden (of geen waarden) voor elke kolom in de koptekst.

## Maximale bestandsgrootte

Bulksheet-bestanden kunnen maximaal 2,5 GB zijn (ongeveer 2,5 miljoen rijen).

>[!NOTE]
>
>Wanneer u een bulksheet voor veelvoudige campagnes produceert en de gecombineerde gegevens uit meer dan 500.000 rijen bestaan, worden de gegevens verdeeld door campagne in twee of meer dossiers, genoemd `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`, enzovoort.

## Opmaakvereisten voor verschillende bestandstypen

Voor gegevensvelden die worden gescheiden door tabs en komma&#39;s is een andere opmaak vereist.

### TSV-bestanden en TXT-bestanden gescheiden met tabs

Gegevensvelden in TSV-bestanden en TXT-bestanden die zijn gescheiden met tabs, moeten als volgt worden opgemaakt:

* De velden in elke record worden gescheiden door tabtekens. Als u een waarde voor een veld wilt weglaten, gebruikt u alleen het tabteken.

  Voorbeeld: `Cruises<TAB>5000<TAB>Caribbean<TAB><TAB><TAB>`

* Velden mogen geen ingesloten tabtekens bevatten.

### CSV-bestanden en TXT-bestanden met komma&#39;s als scheidingsteken

Gegevensvelden in CSV-bestanden en TXT-bestanden met komma&#39;s als scheidingsteken moeten als volgt worden opgemaakt:

* De velden in een record worden gescheiden door komma&#39;s. Als u een waarde voor een veld wilt weglaten, gebruikt u alleen de komma.

  Voorbeeld: `Cruises,5000,Caribbean,,,`

* Willekeurig veld kan eventueel worden ingesloten door dubbele aanhalingstekens (`""`).

  Voorbeeld:  `"Cruises","5000","Caribbean",`

* Velden met ingesloten komma&#39;s moeten tussen dubbele aanhalingstekens staan (`""`).

  Voorbeeld: `Cruises,5000,Caribbean,"Luxurious, spacious cabins",`

* Velden met ingesloten dubbele aanhalingstekens moeten tussen dubbele aanhalingstekens staan (`""`).

  Voorbeeld: `Cruises,5000,Caribbean,"Customers say ""We wish we could stay forever."",`

* Velden met voorafgaande of navolgende spaties moeten tussen dubbele aanhalingstekens (`""`).

  Voorbeeld: `Cruises,5000,Caribbean,"  Come see what we mean.  ",`

>[!MORELIKETHIS]
>
>* [Campagnegegevens beheren met behulp van bulksbladen](../bulksheet-about.md)
>* [Bewerkingen die u kunt uitvoeren in bulksbladen](bulksheet-operations.md)
>* [Bijlage - Fouten in bladbladen](../bulksheet-errors.md)
>* [Een bulkbladbestand downloaden/maken](../bulksheet-download.md)
