---
title: FTP-toegang tot rapporten
description: Leer hoe u rapporten ontvangt op een alleen-lezen FTP-locatie.
exl-id: eca9f033-5b1b-4afa-926b-b4c31e2dede3
feature: Search Reports
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# FTP-toegang tot rapporten

U kunt optioneel rapporten ontvangen op een alleen-lezen FTP-locatie, waar u de bestanden kunt ophalen voor extra geautomatiseerde processen (bijvoorbeeld om de gegevens te parseren met een ander programma). Alle basisverslagen behalve [!UICONTROL Search Engine Account Report] en alle geavanceerde rapporten kunnen aan een plaats van FTP als gecomprimeerde TSV- dossiers (het gebrek) of Csv- dossiers, met een .ZIP dossieruitbreiding worden geleverd. Alle TSV- of CSV-bestandsheaders worden opgenomen en kunnen niet worden onderdrukt.

FTP-toegang tot rapporten vereist toegang tot een opgegeven FTP-account en u moet rapportsjablonen instellen met een specifieke naamgevingsconventie en een schema.

## Een FTP-account instellen voor toegang tot rapporten

* Neem contact op met het accountteam van de Adobe om een FTP-account in te stellen voor toegang tot rapporten.

  Het team voorziet u van uw gebruikersbenaming en wachtwoord.

## Rapportsjablonen instellen voor FTP-levering

Als u rapporten wilt genereren in uw aangewezen FTP-map, maakt u een [rapportsjabloon](templates/template-create.md) met de volgende naamconventies en het volgende schema.

>[!NOTE]
>
>Alle geavanceerde rapporten en alle basisverslagen behalve de [!UICONTROL Search Engine Account Report] kan worden geleverd naar een FTP-locatie.

1. In het rapportmalplaatje, omvat overal de volgende informatie in de malplaatjenaam:

   * `FTP` (in hoofdletters).

   * (Optioneel) Een van de drie systeemdatums met gebruik van de volgende hoofdlettergevoelige syntaxis, inclusief vierkante haken:

      * `[TODAY]` — De datum, het uur en de minuut waarop het rapport werd uitgevoerd, worden opgenomen. Omdat dit de nauwkeurige tijd omvat, kan het zelfde malplaatje veelvoudige tijden per dag worden in werking gesteld zonder het vorige rapport te beschrijven.

      * `[SDATE]` — Opnemen van de begindatum van het bereik van de rapportdatum.

      * `[EDATE]` — Opnemen van de einddatum van het bereik van de rapportdatum.

   * (Optioneel) `[CSV]` (in hoofdletters en tussen haakjes) om bestanden in CSV-indeling te maken in plaats van in de standaard-TSV-indeling.

   Voorbeeld: `[TODAY]-Portfolio-FTP-[SDATE]-[EDATE]-[CSV]` zou een bestand maken zoals 202305051656-Portfolio-FTP-20230428-20110504.csv.

1. Plan het rapport dat op een bepaald tijdstip moet worden uitgevoerd.

   De rapporten worden binnen een uur na voltooiing aan de FTP-account geleverd.

>[!NOTE]
>
>* Als u voltooide rapporten per e-mail wilt verzenden, voert u gewoon de adressen van alle e-mailontvangers in wanneer u het rapport of de sjabloon genereert.
>* Rapporten worden volgens de opgegeven schema&#39;s uitgevoerd en worden binnen een uur na voltooiing van de rapporten aan de FTP-account geleverd.

## Rapporten openen in een FTP-opslagplaats

Als u toegang wilt krijgen tot uw rapporten, maakt u verbinding met een van de volgende FTP-hosts via de aanmelding voor uw FTP-account (`amo<userID>rpt`, zoals amo1234rpt) en een wachtwoord of een persoonlijke verbindingssleutel als er een is ingesteld:

* Internationale klanten: `ftp3.adobe.net`
* Amerikaanse klanten: `ftp5.adobe.net`

>[!NOTE]
>
>De rapportopslagplaats is alleen-lezen en wordt elke 15 dagen gewist.


>[!MORELIKETHIS]
>
>* [Een rapportsjabloon maken](/help/search-social-commerce/reports/automation/templates/template-create.md)
