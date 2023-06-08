---
title: Werkbladgegevens voor [!DNL Yahoo! Display Network] rekeningen
description: Verwijs naar de kopbalgebieden en gegevensgebieden in gedownloade bulksbladen voor [!DNL Yahoo! Display Network] rekeningen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Bijlage - Werkbladgegevens voor [!DNL Yahoo! Display Network] rekeningen

<!-- 
[Re-add "Required" to title, file name, and TOC if you add the ability to create/edit campaigns using YDN bulksheets. Then will also need to add more text below, like for the other SEs.]
-->

U kunt gegevens downloaden voor [!DNL Yahoo! Display Network] accounts in bulk, maar kunnen geen bulksbladen uploaden of posten naar het advertentienetwerk.

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

The following example shows data in comma-delimited values. If you're using tab-separated values, then the data looks different.

Platform,Acct Name,Campaign Name,Ad Group Name,Ad Name, Ad Title,Description Line 1,Description Line 2,Base URL/Final URL,Destination URL,[Advertiser-specific Label Classification],Bid Rules,Constraints,Campaign Status,Ad Group Status,Ad Status,Campaign ID,Ad Group ID,Ad ID,AMO ID,EF Error Message

-->

## Beschikbare gegevensvelden

| Veld | Campagne | Advertentiegroep | Advertentie | Beschrijving |
|----|----|----|----|----|
| [!UICONTROL Platform] | n.v.t. | n.v.t. | n.v.t. | (Opgenomen in gegenereerde bulksbladen ter informatie) Het advertentieplatform. |
| [!UICONTROL Acct  Name] | Indien inbegrepen | Indien inbegrepen | Indien inbegrepen | De unieke naam die een advertentienetwerkaccount identificeert. |
| [!UICONTROL Campaign Name] | Indien inbegrepen | Indien inbegrepen | Indien inbegrepen | De unieke naam die een campagne voor een account identificeert. |
| [!UICONTROL Ad Group Name] | n.v.t. | Indien inbegrepen | Indien inbegrepen | De unieke naam die een advertentiegroep identificeert. |
| [!UICONTROL Ad Name] | n.v.t. | n.v.t. | Indien inbegrepen | De unieke naam die de advertentie in een advertentiegroep identificeert. De maximumlengte is 50 tekens. |
| [!UICONTROL Ad Title] | n.v.t. | n.v.t. | Indien inbegrepen | De kop van een advertentie. |
| [!UICONTROL Description Line 1] | n.v.t. | n.v.t. | Indien inbegrepen | De eerste regel van de tekst van een advertentie. |
| [!UICONTROL Description Line 2] | n.v.t. | n.v.t. | Indien inbegrepen | De tweede regel van de tekst van een advertentie. |
| [!UICONTROL Base URL/Final URL] | n.v.t. | n.v.t. | Indien inbegrepen | De bestemmingspagina URL waaraan de eind - gebruikers worden genomen wanneer zij uw advertentie klikken, met inbegrip van om het even welke toevoegingsparameters die voor de campagne of de rekening worden gevormd. Basis/definitieve URLs op het sleutelwoordniveau treedt URLs op het advertentieniveau en hoger met voeten. |
| [!UICONTROL Destination URL] | n.v.t. | n.v.t. | n.v.t. | (Ter informatie opgenomen in gegenereerde bulksbladen; niet gepost aan het advertentienetwerk) Voor accounts met doel-URL&#39;s is deze waarde de URL die een advertentie koppelt aan een basis-URL/bestemmingspagina op de website van de adverteerder (soms via een andere site die de klik bijhoudt en de gebruiker vervolgens doorstuurt naar de bestemmingspagina). Het omvat om het even welke toevoegingsparameters die voor de Onderzoek, Sociale, &amp; de campagne of de rekening van de Handel worden gevormd. Als u URL&#39;s voor bijhouden hebt gegenereerd, is deze waarde gebaseerd op de volgende parameters in uw accountinstellingen en campagnemontages. Als u netwerkspecifieke parameters toevoegde, dan kunnen zij met de gelijkwaardige parameters voor Onderzoek, Sociale, &amp; Handel worden vervangen. |
| \[Advertiserspecifieke labelclassificatie\] | Indien inbegrepen | Indien inbegrepen | Indien inbegrepen | (Benoemd voor een advertentiespecifieke labelclassificatie, zoals &quot;Kleur&quot; voor een labelclassificatie genaamd Kleur) Een waarde voor de opgegeven classificatie die aan de entiteit is gekoppeld. |
| [!UICONTROL Constraints] | Indien inbegrepen | Indien inbegrepen | n.v.t. | Een beperking die aan de entiteit is toegewezen. |
| [!UICONTROL Campaign Status] | Indien inbegrepen | n.v.t. | n.v.t. | De weergavestatus van de campagne: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, of <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | n.v.t. | Indien inbegrepen | n.v.t. | De weergavestatus van de advertentiegroep: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, of <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Keyword Status] | n.v.t. | n.v.t. | Indien inbegrepen | De weergavestatus van het trefwoord: <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, of <i>[!UICONTROL Deleted]</i> (alleen bestaande trefwoorden). |
| [!UICONTROL Campaign ID] | Indien inbegrepen | Indien inbegrepen | Indien inbegrepen | De unieke id die een bestaande campagne identificeert. |
| [!UICONTROL Ad Group ID] | n.v.t. | Indien inbegrepen | Indien inbegrepen | De unieke id die een bestaande advertentiegroep identificeert. |
| [!UICONTROL Keyword ID] | n.v.t. | n.v.t. | Indien inbegrepen | De unieke id die een bestaand trefwoord identificeert. |
| [!UICONTROL AMO ID] | n.v.t. | n.v.t. | n.v.t. | (In gegenereerde bulksbladen) Een unieke id die door Adobe wordt gegenereerd voor een gesynchroniseerde entiteit. |
| [!UICONTROL EF Error Message] | n.v.t. | n.v.t. | n.v.t. | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van foutberichten van Zoeken, Sociale Zaken en Handel met betrekking tot gegevens in de rij. foutberichten worden opgenomen in EF-foutbestanden. |

<table style="table-layout:auto">

>[!MORELIKETHIS]
>
>* [Een bulkbladbestand downloaden/maken](../bulksheet-download.md)

