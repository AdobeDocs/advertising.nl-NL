---
title: Ad-specificaties
description: Algemene en uitgeverspecifieke referentiespecificaties.
feature: DSP Ads
exl-id: 133dfc0d-d839-4e06-a819-21e3e630830c
source-git-commit: a6f9bb2d714e7ddb22f74c9c614772eca30f9e40
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

---

# Specificaties voor ondersteunde advertentietypen

## Video-advertenties (Pre-Roll, CTV en Universal Video)

### Ondersteunde Screens

Advertenties worden standaard geleverd op desktopapparaten, mobiele apparaten en aangesloten tv-apparaten. Apparaatgerichtheid is beschikbaar om de levering aan te passen.

### Ondersteunde externe advertentieservers

U kunt tagbladen gebruiken vanuit [!DNL DCM] , [!DNL Flashtalking] , [!DNL Innovid] en [!DNL Sizmek] . Voor een volledige lijst van gesteunde verkopers, zie &quot;[ Verklaarde en Servende Partners ](certified-ad-servers.md).&quot;

### Vereisten voor High Definition Video Assets

**Type van VideoMarkering:** VPAID 2.0 JavaScript of VAST (CTV). Alle VPAID en eenheden moeten aan de [ VPAID 2.0 specificatie ](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) zoals die door het Interactieve Bureau van Advertising (IAB) wordt bepaald naleven.

**Videocodec:** MP4/H.264

**Resolutie:** 1280x720 voor 720p, 1920x1080 voor 1080p

**Bitsnelheid:** 1500-2500 kbps voor 720p, 2500-3500 kbps voor 1080p

**H.264 Profiel/Niveau:** Hoog profiel, niveau 3.1 voor 720p; Hoog profiel, niveau 4.0 voor 1080p

**VideoTarief dat van het Kader:** 29.970 fps (algemeen als 30 fps wordt bedoeld) voor NTSC landen, 25 fps voor PAL landen, 23.976 fps (algemeen die als 24 fps worden bedoeld) voor film-blik inhoud

**VideoRuimte van de Kleur:** 4 :2: 0 YUV subsampling van Chroma

**Video het Interllen:** Progressief aftasten, d.w.z., niet-doorweven. Geen beweging binnen het veld (overvloeiframes) of interliniëring.

**Leiders (Slaat):** niet toegelaten

**AudioCodec:** AAC-LC of HE-AACv1

**Audio Bitrate:** 128-192 kbps voor AAC-LC, 64-128 kbps voor HE-AACv1

**Audiokanaal:** 2 kanaals stereomix

**Audio het Tarief van de Steekproef:** 44.1 kHz of 48 kHz, zoals per bronmateriaal

**Audioniveaus:** 24 LKFS (+/- 2.0 dB) in de V.S. volgens ATSC A/85; 23 LUFS (+/- 1.0) in de EU volgens EBU R128

#### Aanvullende vereisten voor uitgevers voor aangesloten tv-advertenties

* **A+E Netwerk:** zie A+E 2} en specificaties van het Netwerk van A+E [](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf)

* **Ontdekking:** zie de 2} en specificaties van Ontdekking [.](/help/dsp/assets/discovery-networks-ad-specs.pdf)

* **Disney (incl. Hulu):** zie de 1} en specificaties van Disney [.](https://www.disneyadvertising.com/mediakit/#specifications)

* **Max HBO:** zie Max van HBO [ en specificaties ](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx).

* **NBCUniversal:**

   * [ Digitale Video ](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [ Livestream ](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [ Peacock ](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **Paramount:** zie de 2} en specificaties van het Hoofdbedrag [.](https://www.paramount.com/digital-ads)

## Advertenties weergeven

### Ondersteunde Screens

Advertenties worden standaard geleverd op desktopapparaten en mobiele apparaten. Apparaatgerichtheid is beschikbaar om de levering aan te passen.

### Ondersteunde bestandstypen

**Beeld:** GIF, JPG/JPEG, PNG

**HTML5:** de dossiertypes van het Beeld: GIF, JPG/JPEG, PNG, SVG

### Vereisten voor Image Assets

Universal Display wordt ondersteund.

**Aanbevolen ad grootte:** 120x60, 160x600, 180x150, 300x50, 300x100, 300x1050, 300x250, 300 x 600, 320 x 50, 320 x 480, 480 x 60, 640 x 480, 88 x 31, 728 x 90, 970 x 250, 970 x 90

**Gesteunde Servers van de Advertentie van de Derde:** u kan markeringsbladen van [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid], en [!DNL Sizmek] gebruiken. Voor een volledige lijst van gesteunde verkopers, zie &quot;[ Verklaarde en Servende Partners ](certified-ad-servers.md).&quot;

## Audiobanden

### Ondersteunde Screens

Desktop, mobiel, tablet, slimme luidsprekers en aangesloten tv

### Ondersteunde externe advertentieservers

U kunt tagbladen gebruiken vanuit [!DNL DCM] , [!DNL Flashtalking] , [!DNL Innovid] en [!DNL Sizmek] . Voor een volledige lijst van gesteunde verkopers, zie &quot;[ Verklaarde en Servende Partners ](certified-ad-servers.md).&quot;

### Vereisten voor audio Assets

**het type van Dossier:** MP3, OGG, AAC

**Leiders (leisteen):** niet toegelaten

**Maximale dossiergrootte:** 2MB

**Bitsnelheid:** 128

**Lengte van het Dossier:** 0-60s

#### Aanvullende vereisten voor uitgevers

* **[!DNL iHeartRadio]**
   * Lengte: 5, 15, 30 of 60 seconden
   * Bestandstype: MP3
   * Maximale bestandsgrootte: 320 kbps
   * Volume: 44,1 kHz

* **[!DNL Pandora]**
   * Lengte: 15 of 30 seconden
   * Bestandstype: MP4 (in-app), MP3 (desktop)
   * Maximale bestandsgrootte: 2,2 MB

* **[!DNL SoundCloud]**
   * Lengte: 6, 15 of 30 seconden
   * Bestandstype: MP3
   * Maximale bestandsgrootte: 5 MB

* **[!DNL Spotify]**
   * Lengte: tot 30 seconden
   * Bestandstype: OGG
   * Maximale bestandsgrootte: 500 MB
   * Volume: RMS genormaliseerd naar -14; dBFS piek genormaliseerd naar -0,2 dBFS

* **[!DNL TargetSpot]**
   * Lengte: 15, 30 of 60 seconden
   * Bestandstype: MP3

* **[!DNL TuneIn]**
   * Lengte: 10, 15 of 30 seconden
   * Bestandstype: MP3, OGG
   * Volume: 44,1 kHz

### Vereisten voor extra hulpmiddelen van de Banner (facultatief)

**Gesteunde grootte:** 300x250, 500x500, 640x640, 1024x1024

#### Aanvullende vereisten voor uitgevers

* **[!DNL iHeartRadio]:**
   * Bestandstype: JPEG, JPG, PNG, GIF, SWF, HTML
   * Maximale bestandsgrootte: 2,2 MB
   * Afmetingen: 300 x 250

* **[!DNL Pandora]:**
   * Bestandstype: JPEG, GIF
   * Maximale bestandsgrootte: grootte: 100 kB
   * Afmetingen: 300 x 250 (mobiel of bureaublad) of 500 x 500 (bureaublad)

* **[!DNL SoundCloud]:**
   * Bestandstype: statische JPG, PNG
   * Maximale bestandsgrootte: minder dan 400 kB
   * Afmetingen: 1024x1024

* **[!DNL Spotify]:**
   * Bestandstype: statische JPG, PNG
   * Maximale bestandsgrootte: 200 kB
   * Afmetingen: 300 x 250

* **[!DNL TuneIn]:**
   * Bestandstype: JPEG, JPG, PNG, GIF, HTML
   * Maximale bestandsgrootte: 2 MB
   * Afmetingen: 300 x 250

## Systeemeigen weergaveadvertenties

Elke advertentie kan een stilstaand beeld of een bewegende GIF (cinemagraph) bevatten.

### Ondersteunde Screens

Advertenties worden standaard geleverd op desktopapparaten en mobiele apparaten. Apparaatgerichtheid is beschikbaar om de levering aan te passen.

### Vereiste Assets voor alle native invoerindelingen

#### Afbeeldingselement

**Resolutie:** minimum 600x600px; geadviseerde minimum van 1200x627px

**het type van Dossier:** JPEG (beeld en of video en omslagbeeld), GIF (cinemograph)

**Grootte van het Dossier:** minder dan 1 MB (het Beeld zou vrij van tekst moeten zijn.)

#### Advertiserlogo

**Resolutie:** minimum 80x80px; geadviseerd minimum van 300x300px

**type van Dossier:** JPEG of PNG.

**Verhouding:** 1x1 verhouding

>[!NOTE]
>
>Afhankelijk van de afbeelding waarop de afbeelding wordt geplaatst, kunt u kiezen tussen lichte of donkere logo-elementen.

#### Tekst/kopie

**Titel:** Maximum 200 karakters; 25 geadviseerde karakters

**Bijschrift:** Maximum 200 karakters; 100 geadviseerde karakters

**gesponsord door:** Maximum 200 karakters; 30 geadviseerde karakters

**Call to action (MoPub slechts):** Maximum 15 karakters

>[!NOTE]
>
>De uiteindelijke indeling wordt tijdens runtime door de uitgever gedefinieerd. Als een advertentie het geadviseerde karakteraantal overschrijdt, kunnen sommige voorraadleveranciers niet de advertentie leveren, of de uitgever of SSP kunnen de tekst beknotten.

#### URL van bestemmingspagina

De doorklikURL met facultatieve kliksporen.

Vereisten voor kliktrackers:

* Pixels voor het bijhouden van afbeeldingen van derden: alleen 1x1-afbeeldings-URL-indeling

* Viewability JavaScript trackers: slechts gesteund voor IAS; 1x1 beelden in formaat JS.append slechts

* Klikvolgende pixels van derden: moet worden omgeleid naar de bestemmingspagina die is ingesloten in de URL (HTTP 302 omleiding)

* Het platform voor gegevensbeheer (DMP) klikt op trackers met 200 of meer reacties worden niet ondersteund.

>[!MORELIKETHIS]
>
>* [ Ongeveer Advertentiebeheer ](ad-about.md)
>* [ creeer Één enkele Advertentie ](ad-create.md)
>* [ creeer Veelvoudige Derde Advertenties ](ad-create-multiple.md)
>* [ geef een Advertentie uit ](ad-edit.md)
