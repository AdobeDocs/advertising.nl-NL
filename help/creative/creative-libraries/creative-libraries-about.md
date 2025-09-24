---
title: Over uw creatieve bibliotheken
description: Meer informatie over het beheren van de creatieve projecten voor uw advertentiervaringen.
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: ce716c8dca8410a121858944f0c044423d9dff78
workflow-type: tm+mt
source-wordcount: '1386'
ht-degree: 0%

---

# Over uw creatieve bibliotheken

Met uw creatieve bibliotheken kunt u de creatieve projecten beheren die u in uw advertentiervaringen zult gebruiken. U kunt veelvoudige bibliotheken, elk met een reeks creatieve en *creatieve bundels* tot stand brengen, die groepen creatieve producten zijn die u aan een ervaring als één eenheid kunt toevoegen.

Uw bibliotheken kunnen het volgende bevatten:

* **Individuele creatieven:** u kunt individuele creatieve personen direct binnen en ervaringen omvatten die geen bepaalde gebruikersdoelstellingen hebben. U kunt uw creatieven ook gebruiken om bundels tot stand te brengen, die u in gerichte [ en ervaringen ](/help/creative/experiences/experience-about.md) kunt omvatten.

   * **Standaard creatieven:** u kunt creatieve elementen in [ diverse formaten ](#creative-creative-formats) uploaden en beheren. Voor elke creatieve advertentie geeft u de standaardtaal op voor elke advertentie waarmee u de creatieve pagina en de standaard openingspagina koppelt die wordt geopend wanneer een gebruiker op een advertentie klikt die de creatieve pagina bevat. U kunt desgewenst labels opgeven die u als filters wilt gebruiken in verschillende weergaven binnen [!DNL Creative] en als kolomwaarden in [!UICONTROL Custom Creative Report] wanneer u de [!UICONTROL Creative Label] -dimensie gebruikt.

   * **Dynamische creatieven:** u kunt dynamisch geproduceerde creatieve elementen tot stand brengen door dynamische variabelen in een advertentiemalplaatje aan waarden in een voederdossier in kaart te brengen. Alle gebruikers kunnen bestaande dynamische advertenties voorvertonen, dupliceren en verwijderen.

* **Creatieve bundels:** Groepeer creatieve elementen in bundels over veelvoudige ervaringen met bepaalde gebruikersdoelstellingen te gebruiken. U kunt *standaardvertoningsbundels* tot stand brengen die uit standaardvertoningsadvertenties bestaan, *standaardvideobundels* die uit standaardvideoadvertenties bestaan, en *dynamische vertoningsbundels* die uit dynamisch geproduceerde vertoningsadvertenties bestaan.

## Ondersteunde Creative-indelingen {#creative-creative-formats}

### Formaten voor standaardcreatieve producten

U kunt de volgende creatieve types in de [ gesteunde creatieve grootte toevoegen en beheren ](creative-sizes.md).

>[!IMPORTANT]
>
>* Zelfs als u HTML5, Flexible HTML5 of creatieve producten van derden wilt gebruiken voor uw standaardweergave en -ervaring, moet u ook creatieve afbeeldingen toevoegen voor elke creatieve grootte die u gebruikt.
>* Voor elke standaardweergave is een standaardafbeelding vereist die creatief is voor elke creatieve grootte die aan de ervaring is toegewezen. De standaardafbeeldingscreatieven worden gebruikt wanneer een browser niet geschikt is voor JavaScript of wanneer de advertentieserver de advertentie niet kan personaliseren vanwege vertragingen.
>* Elke standaard videoervaring vereist standaardvideo creatief voor elke creatieve duur die aan de ervaring wordt toegewezen.<!-- when is it used? -->

#### Flexibele HTML5

Flexibele HTML5-creatieven zijn HTML5-creatieven met al hun afbeeldingen en andere kenmerken als standaard HTML-tags, die u rechtstreeks in [!DNL Creative] kunt bewerken, in een creatieve bibliotheek of in een individuele ervaring (waardoor een variatie van de originele creatieve elementen ontstaat). In DSP zijn flexibele HTML5-creatieven bedoeld voor één specifieke advertentiegrootte (in pixels). U kunt desgewenst de standaardwaarden wijzigen van de kenmerken die zijn opgegeven in een flexibele creatieve HTML5. Later kunt u aangepaste waarden opgeven voor de kenmerken binnen een bepaalde ervaring. Hierdoor wordt een variatie van de bovenliggende creatieve elementen gemaakt.

U kunt flexibele HTML5-creatieven uploaden als ZIP-bestanden of een van de sjablonen gebruiken die beschikbaar zijn voor uw account als startpunt. Zie de [ specificaties voor flexibele HTML5 creatieven ](html5-creative-specification.md).

#### HTML5-creatieven

U kunt eenvoudige of statische HTML5-creatieven uploaden, met alle kenmerken en afbeeldingen opgegeven als ZIP-bestanden. U kunt geen kenmerken bewerken of afbeeldingen toevoegen. U kunt in plaats daarvan een nieuw ZIP-bestand uploaden om een nieuwe creatieve functie toe te voegen. Zie de [ specificaties voor eenvoudige en statische HTML5 creatieven ](html5-creative-specification.md).

#### Afbeeldingscreatieven

U kunt creatieve afbeeldingen opnemen in de indeling GIF, JPEG, JPG of PNG. U kunt goedgekeurde afbeeldingen uploaden vanaf uw Adobe Experience Manager-accounts of vanaf uw apparaat of netwerk.

Voor elke standaardweergave en -ervaring is een standaardafbeelding vereist die creatief is voor elke creatieve grootte die aan de ervaring is toegewezen.

#### Kinderen van derden

Voer JavaScript-trackingtags in voor creatieve producten die worden gehost op externe advertentieservers. Het script varieert per advertentieserver. Hieronder ziet u een voorbeeld:

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

#### Videocreatieven {#creative-video-specs}

U kunt eersteklas videoclips voor het web, mobiele apparaten of aangesloten tv uploaden vanaf uw apparaat of netwerk. Voor elke standaardvideo en -ervaring is een creatieve standaardvideo vereist voor elke creatieve duur die aan de ervaring wordt toegewezen. Alle videocamera&#39;s worden automatisch door DSP getranscodeerd als VAST 2.0-tags, zodat u deze kunt voorvertonen. In [!UICONTROL Tag Manager], kunt u naar keuze [ DSP-Specifieke transcodering ](/help/creative/experiences/experience-tag-video-transcoding.md) op om het even welke video en ervaringstag toepassen.

Bekijk de volgende creatieve videovereisten. **Nota:** als u videoervaringen aan Advertising DSP zult uploaden, dan zie ook DSP [ Vereisten voor Video Assets van High-Definition ](https://experienceleague.adobe.com/en/docs/advertising/dsp/campaign-management/ads/ad-specs#requirements-for-high-definition-video-assets), die meer beperkt kunnen zijn.

**Type van Dossier:** .mov, .mp4, .webm

**Grootte van het Dossier:** Maximum van 512 MB

**Videoverhouding:** 16 :9, 4 :3

**VideoResolutie:** 640x360 voor 360p, 1280x720 voor 720p, 1920x1080 voor 1080p

**Videolengte:** Maximum van 90 seconden

**Bitsnelheid:** 600-1200 kbps voor 360p, 1500-2500 kbps voor 720p, 3000-5000+ kbps voor 1080p

**het tarief van het Videoframe:** 23.98 FPS. Aanvullende framesnelheden kunnen worden geaccepteerd op basis van regionale of uitgeververeisten

**Videocodec:** H.264 (industriestandaard), AV1, H.265

**AudioFormaat:** ACC (industriestandaard/MP4), Opus (WebM/AV1)

**AudioBitsnelheid:** 16-512 kbps

**Audio Steekproeftarief:** 44100-48000 Herz

**Audiotarief:** 44.1kHz of 48 kHz

**Audio andere:** het geuploade dossier moet niet-doorweven zijn, gemengd, en een audiospoor bevatten. Er is mogelijk geen geluid, maar een audiotrack moet in het videobestand worden opgenomen.

### Indeling voor dynamische advertenties

U kunt creatieve elementen dynamisch genereren in statische HTML5- en dynamische HTML5-indeling door dynamische variabelen in een advertentiesjabloon toe te wijzen aan waarden in een feed-bestand. Dynamische creatieve producten kunnen creatieve producten bevatten die zijn gemigreerd uit uw oudere Adobe Advertising Dynamic Creative Optimization (DCO)-ervaringen.

## De weergaven [!UICONTROL Creative Libraries]

Zie &quot;[ uw gegevensmeningen ](/help/creative/introduction/customize-data-views.md)&quot;voor meer informatie aanpassen over het aanpassen van elke mening.

### De hoofdweergave van [!UICONTROL Creative Libraries]

In de hoofdweergave van [!UICONTROL Creative Libraries] worden al uw creatieve bibliotheken weergegeven. De gegevens voor elke bibliotheek bevatten het aantal ervaringen waaraan de bibliotheekbundels zijn toegewezen, het aantal bundels, het aantal creatieve formaten, het aantal creatieve formaten, het aantal standaardtaaldoelen, de aanmaakdatum en de laatste wijzigingsdatum voor elk element van de bibliotheek. De tabelmodus bevat ook een kolom voor de adverteerder.

In de kaartmodus kunt u met de knoppen &lt; en > door de afbeeldingen in een bibliotheek schuiven met meerdere creatieven.

#### Beschikbare acties

* [Een nieuwe bibliotheek maken](/help/creative/creative-libraries/creative-library-manage.md#create-a-creative-library)

* Voor elke creatieve bibliotheek:

   * [Een bibliotheeknaam bewerken](/help/creative/creative-libraries/creative-library-manage.md#edit-the-name-of-a-creative-library)

   * [Een bibliotheek openen om de creatieve en bundels weer te geven die aan de bibliotheek zijn toegewezen](/help/creative/creative-libraries/creative-library-manage.md#open-a-creative-library)

   * [Bibliotheken verwijderen](/help/creative/creative-libraries/creative-library-manage.md#delete-creative-libraries)

### De weergaven [!UICONTROL Creative Libraries] > [!UICONTROL Creatives]

#### [!UICONTROL Standard Ads]

Op het tabblad [!UICONTROL Standard Ads] worden alle standaardcreatieve elementen weergegeven die u hebt gemaakt. De gegevens voor elke creatieve waarde zijn onder andere de creatieve grootte, het creatieve type en de aanmaakdatum. De tabelmodus bevat ook kolommen voor de standaardtaal en de standaardlandingspagina.

##### Beschikbare acties

* [Standaardcreatieve elementen toevoegen aan een bibliotheek](creative-add-standard.md)

* [Een standaard creatieve bewerking](creative-edit-standard.md)

* [Een standaard creatieve voorvertoning weergeven](creative-preview.md)

* [Standaardcreatieve elementen toevoegen aan standaardweergavesystemen en standaardcreatieven verwijderen uit een standaardweergaveset](creative-attach-detach-bundles.md)

* [Videoontwerpers toevoegen aan standaardvideobundels en creatieve videobeelden verwijderen uit een standaardvideobundel](creative-attach-detach-bundles.md)

* [Standaard creatieve producten dupliceren](creative-duplicate.md)

* [Standaardcreatieven downloaden](creative-download.md)

* [Standaardcreatieve producten verwijderen](creative-delete.md)

#### [!UICONTROL Dynamic Ads]

Het [!UICONTROL Dynamic Ads] lusje toont alle dynamische creatieve creatieve creatieve die dynamisch voor uw creatieve catalogi, behalve om het even welke dynamische creatieve creatieve creatieve die u [ manueel schrapte ](creative-delete.md) van het [!UICONTROL Dynamic Ads] lusje werden gecreeerd. Als u [ manueel gedupliceerde ](creative-duplicate.md) om het even welke dynamische creatieve personen <!-- I don't think existing ads are deletd via feeds, so this probably isn't true: since a catalog was last processed -->, dan omvat de lijst van creatieve personen voor die catalogus ook de dubbele creatieve elementen.

De gegevens voor elke creatieve functie omvatten het creatieve type, de creatieve grootte, het aantal catalogi waartoe de creatieve functie behoort, en de aanmaakdatum. De tabelmodus bevat ook kolommen voor de advertentiesjabloon waarmee de creatieve items zijn gegenereerd en het aantal aanbiedingen.

>[!NOTE]
>
>Telkens als een catalogus wordt verwerkt, worden de gegevens verfrist voor de bestaande dynamische creatieve elementen voor die catalogus.<!-- Verify this!!! And is there anything more to say w/regard to  -->

##### Beschikbare acties

* [Dynamische creatieve elementen toevoegen aan een bibliotheek](creative-add-dynamic.md)

* [Een dynamisch creatief bewerken](creative-edit-dynamic.md)

* [Dynamische creatieve voorvertoningen voorvertonen](creative-preview.md)

* [Dynamische creatieve elementen toevoegen aan dynamische weergavesystemen en dynamische creatieve elementen verwijderen uit een dynamische weergaveset](creative-attach-detach-bundles.md)

* [Dynamische creatieve elementen dupliceren](creative-duplicate.md)

* [Dynamische creatieve elementen verwijderen](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### De weergave [!UICONTROL Creative Libraries] > [!UICONTROL Bundles]

In de weergave [!UICONTROL Bundles] worden al uw standaard- en dynamische bundelcontainers weergegeven. U kunt de creatieve namen, creatieve grootten, en talen voor de creatieve creatieven zien inbegrepen in elke bundel. In de kaartmodus kunt u met de knoppen &lt; en > door de afbeeldingen bladeren in een bundel met meerdere creatieven.

#### Beschikbare acties

* Standaardweergave, standaardvideo en dynamische weergavesystemen toevoegen aan een bibliotheek

* Creatieve elementen in een bundel weergeven en voorvertonen

* Een bundelnaam bewerken

* Standaardweergavefinanciers toevoegen aan standaardweergavesystemen en standaardweergavefinanciers verwijderen uit een standaardweergavesuite

* Standaardvideocamera&#39;s toevoegen aan standaardvideobundels en standaardvideocamera&#39;s verwijderen uit een standaardvideobundel

* Bundels dupliceren

* Bundels verwijderen

>[!MORELIKETHIS]
>
>* [ beheer creatieve bibliotheken ](/help/creative/creative-libraries/creative-library-manage.md)
>* [ voeg standaardcreatieve creatieve bibliotheek ](creative-add-standard.md) toe
>* [ beheer creatieve bundels ](bundle-manage.md)
>* [ pas uw gegevensmeningen ](/help/creative/introduction/customize-data-views.md) aan
