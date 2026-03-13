---
title: Over Audience Management in Advertising DSP
description: Meer informatie over de functies voor publieksbeheer.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: ddd55586ed895962b8f6da0390a3d76fe43ca1ca
workflow-type: tm+mt
source-wordcount: '1322'
ht-degree: 0%

---

# Over Audience Management in Advertising DSP

In DSP kunt u publiekssegmenten en publiekssets maken en beheren, die u kunt gebruiken als doelen voor uw plaatsingen:

* Verzamel uw eigen gegevens over het eerste publiek door DSP-segmenten te maken en te implementeren. U kunt gebruikers in het segment later opnieuw toewijzen met advertenties of u kunt voorkomen dat gebruikers in het segment advertenties ontvangen. U kunt de volgende typen segmenten maken:

   * [ de segmenten van de Douane ](/help/dsp/audiences/custom-segment-create.md) om a) gebruikers te volgen die aan advertenties van Desktop en mobiele apparaten en b) gebruikers worden blootgesteld die specifieke webpagina&#39;s bezoeken. De tag tracking kan gebruikers bijhouden die zijn gebaseerd op cookies of gebruikers die zijn gekoppeld aan universele id&#39;s van ID5.

   * [ CCPA opt-out-of-sale segmenten ](/help/dsp/audiences/ccpa-opt-out-segment-create.md) om gebruikers IDs van consument opt-out-of-verkoop verzoeken op uw website, per de Wet van de Privacy van de consument van Californië (CCPA) te volgen. U kunt maandelijkse rapporten van de gebruikers-id&#39;s ophalen van afmeldingsverzoeken.

     Voor meer informatie over de steun van de Adobe Advertising voor CCPA opt-out-of-sale verzoeken, zie [ Steun van de Adobe Advertising voor de Californische Wet van de Privacy van de Consumentenconsument: De Opt-out Steun van de consument ](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* (De eigenschap van Beta) [ verkrijg en gebruik universele IDs voor cookieless het richten ](/help/dsp/audiences/universal-ids.md):

   * Verzend uw geverifieerde [!DNL LiveRamp] [!DNL RampID] -segmenten handmatig rechtstreeks naar DSP.

   * Laat DSP eerstehands segmenten uit je klantdataplatform importeren en vertalen naar ondersteunde universele ID-typen.

   * Neem zonder extra stappen ook segmenten van derden op die universele id&#39;s in uw plaatsingsdoelen bevatten.

* Creeer een publieksbibliotheek van [ herbruikbare publiek ](/help/dsp/audiences/reusable-audience-create.md). Opgeslagen doelgroepen bestaan uit een van uw beschikbare doelsegmenten en een van uw andere opgeslagen doelgroepen. Wijzigingen die u aanbrengt in een opgeslagen publiek, worden automatisch toegepast op alle plaatsen die het publiek als doel hebben of uitsluiten en op alle andere soorten publiek die het opgeslagen publiek bevatten.

  Opgeslagen publiek stelt mediaplanners in staat om het publiek zo nodig te groeperen door meerdere segmenten met behulp van complexe Booleaanse logica in te sluiten en uit te sluiten. De (doelbare) grootte van elk individueel segment en de algemene actieve publieksgrootte worden vermeld aangezien u een publiek bouwt. De managers van de campagne kunnen één of meerdere bewaarde publiek dan eenvoudig selecteren als plaatsingsdoelstellingen eerder dan manueel publieksdoelstellingen voor elke plaatsing vormen.

Er zijn ook extra publiekstypen beschikbaar voor plaatsing als doel.

## Gegevenssegmenten uit de eerste en derde hand importeren

U hebt veel opties om datasegmenten uit de eerste en derde hand in DSP te importeren, via de DSP gebruikersinterface en/of via aangepaste importservices.

* DSP kunnen je Adobe Audience Manager en andere [!DNL Adobe] doelgroepen aantrekken voor targeting. Voor eerste vereisten en instructies, zie &quot;[ de Segmenten van Adobe Audience Manager van de Invoer voor Ad Targeting ](/help/integrations/audience-manager/import-audiences.md).

* DSP kan de segmenten van eerstehands gegevens van gesteunde platforms van klantengegevens aan segmenten met universele IDs vertalen gebruikend de [ eigenschap van Bronnen ](/help/dsp/audiences/sources/source-about.md). U kunt [ uw geverifieerde  [!DNL LiveRamp] [!DNL RampID] segmenten ook manueel verzenden direct aan DSP ](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* DSP kan uw andere gegevenssegmenten van de eerste partij rechtstreeks vanuit uw gegevenbeheerplatform (DMP) importeren en deze naar alle mogelijke adverteerders doorgeven.

* DSP kan aangepaste segmenten van derden importeren, waaronder complexe combinaties van segmenten van derden. U kunt de segmenten desgewenst aan elke set adverteerders aanbieden.

Neem contact op met uw Adobe-accountteam voor meer informatie.

## publiek beschikbaar als plaatsingsdoelen

U kunt uw plaatsingen aan alle volgende soorten publiek richten.

* Alle door de gebruiker gemaakte publiekssets die in DSP zijn opgeslagen.

* Alle door de gebruiker gemaakte publiekssegmenten die in DSP zijn gemaakt:

   * Aangepaste segmenten voor gebruikers die specifieke webpagina&#39;s hebben bezocht en gebruikers die zijn blootgesteld aan indrukken van specifieke advertenties.

     Er worden geen kosten in rekening gebracht voor afbeeldingen die aan universele id&#39;s worden geleverd.

   * CCPA opt-out-of-sale publiekssegmenten voor gebruikers die opt-out-of-sale verzoeken op uw website, volgens de California Consumer Privacy Act (CCPA) hebben ingediend.

* Alle geïmporteerde gegevenssegmenten van de eerste partij, inclusief segmenten die naar universele id&#39;s zijn vertaald.

  Er worden extra kosten in rekening gebracht voor afdrukken die aan universele id&#39;s worden geleverd. Zie &quot;[ Ongeveer de Bronnen van het Publiek van de Eerste Partij ](/help/dsp/audiences/sources/source-about.md)&quot;voor tarieven.

* Alle geïmporteerde gegevenssegmenten van derden.

* (Plaatsen richtend de V.S. slechts) [ Alle derdegegevenssegmenten beschikbaar aan de klanten van DSP van meer dan 30 leveranciers ](/help/dsp/audiences/third-party-data-providers.md), met inbegrip van [!DNL eXelate], ([!DNL Eyeota]), ([!DNL LiveRamp]), [!DNL Lotame], [!DNL Neustar], en vele meer.

  U kunt zich richten op specifieke segmenten, die gebruikers richten die op publieksgegevens (bijvoorbeeld, gebruikers met specifieke demografie, belangen of intents, en/of gedragsprofielen) worden gebaseerd. U kunt bladeren door gegevensleverancier en categorie, naar segmenten door naam of segmentidentiteitskaart zoeken, of de resultaten door gegevensleverancier, actieve segmentgrootte, Webbrowser telling, of apparatentelling filtreren.

  Voor segmenten van derden worden extra kosten aangerekend, die naast elke segmentnaam worden vermeld.

* (Advertisers met Adobe Experience Platform en [!DNL Real-Time CDP] , Adobe Audience Manager of Adobe Analytics die alleen conversietags voor Adobe Advertising JavaScript gebruiken) Al uw beschikbare doelsegmenten van het type first-, second of third-party die in [!DNL Real-Time CDP] zijn gemaakt, in Audience Manager zijn gemaakt of vanuit Audience Manager of [!DNL Analytics] zijn gepubliceerd naar Adobe Experience Cloud.

  Prijzen voor het gebruik van de segmenten worden vooraf bepaald en zijn niet zichtbaar in DSP.

  Segmenten uit [!DNL Analytics] zijn ongeveer een uur beschikbaar nadat u ze hebt gemaakt of gepubliceerd als Experience Cloud-publiek. Segmenten die rechtstreeks afkomstig zijn uit Audience Manager of [!DNL Real-Time CDP] zijn binnen 24 uur beschikbaar nadat u ze hebt gedeeld.

  >[!NOTE]
  >
  >Zie de documentatie voor [ Audience Manager ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [ Analytics ](https://experienceleague.adobe.com/docs/analytics.html), en [  [!DNL Real-Time CDP] ](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) voor informatie over vestiging en het verzamelen van gegevens voor segmenten in die oplossingen.

## Gegevens over doelgrootte

In Soorten publiek > Alle Soorten publiek en in de sectie Doelgroep van het publiek van plaatsingsmontages, kunt u elke segmentlijst door formaatwaaier, met inbegrip van afzonderlijke waaiers voor specifieke apparatentypen of universele types van identiteitskaart filtreren.

![ filter door publieksgrootte ](/help/dsp/assets/audience-size-filter.png)

U kunt ook gedetailleerde gegevens over de publieksgrootte zien:

* De actieve, gededupliceerde publieksgrootte voor alle geselecteerde segmenten en het opgeslagen publiek wordt weergegeven en u kunt details bekijken op apparaattype (browser, mobiel of aangesloten tv).

  ![ de gecombineerde publieksgrootte ](/help/dsp/assets/audience-size.png)

* Voor afzonderlijke segmenten worden de actieve publieksgrootte en CPM (indien van toepassing) naast de segmentnaam weergegeven.

  ![ de individuele segmentgrootte ](/help/dsp/assets/audience-size-segment.png)

* U kunt meer details over een afzonderlijk segment of een opgeslagen publiek weergeven, zoals de grootte per browser, mobiel, aangesloten tv en partner voor het universele-id-type. Voor opgeslagen publiek is de totale actieve publieksgrootte het gedupliceerde totaal.

  ![ het individuele segment of de bewaarde publieksdetails ](/help/dsp/assets/audience-size-segment-details.png)

## De weergave Soorten publiek

### De weergave Alle soorten publiek

In de weergave [!UICONTROL All Audiences] of Audience Library kunt u herbruikbare soorten publiek opslaan en beheren, waaronder groepen publiekssegmenten en zelfs andere opgeslagen soorten publiek. U kunt doelgroepen gebruiken als doelen voor meerdere plaatsen. Het aantal plaatsen waarin elk publiek wordt gebruikt wordt vermeld naast de plaatsingsnaam.

U kunt een publiek bewerken, klonen, verwijderen, exporteren of delen.

### De weergave Segmenten

In de [!UICONTROL Segments] -weergave kunnen alle gebruikers extra aangepaste segmenten maken.

In de weergave [!UICONTROL Segments] worden ook de volgende segmenttypen weergegeven:

* Alle door de gebruiker gemaakte aangepaste segmenten zijn beschikbaar voor de gebruiker.

  U kunt de volgende markeringen voor om het even welke douanesegmenten bekijken u creeerde, en die segmenten met andere gebruikers delen. U kunt ook de aangepaste segmenten die u hebt gemaakt bewerken of verwijderen.

  U kunt geen aangepaste segmenten bewerken of delen die andere gebruikers met u hebben gedeeld.

* Alle eerste-partijsegmenten die worden ingevoerd zoals-is die aan de gebruiker beschikbaar zijn.

  U kunt segmenten uit de eerste hand die met u zijn gedeeld, niet bewerken of delen. Neem contact op met het accountteam van uw Adobe als u eerstehands segmenten met extra gebruikers wilt delen.

* Alle aangepaste segmenten van derden beschikbaar voor de gebruiker.

  U kunt segmenten van derden die met u zijn gedeeld, niet bewerken of delen. Neem contact op met het accountteam van uw Adobe als u segmenten van derden met extra gebruikers wilt delen.

### De Bronweergave

In de [!UICONTROL Sources] mening, kunt u bronnen voor eerste-partijsegmenten in gesteunde platforms van klantengegevens vormen die u in segmenten wilt omzetten die gespecificeerde universele types van identiteitskaart bevatten. De bronmontages omvatten een auto-geproduceerde bronsleutel, die u aan uw platform van klantengegevens zult verstrekken om de verbinding te vestigen.

Voor meer informatie over de gesteunde platforms van klantengegevens, gesteunde universele types van identiteitskaart, en de werkschema&#39;s aan opstellingsverbindingen aan elk platform van klantengegevens, zie &quot;[ Ongeveer Bronnen ](/help/dsp/audiences/sources/source-about.md).&quot;

De vertaalde segmenten zijn beschikbaar om in herbruikbaar publiek en in plaatsingsmontages voor het kiezen zonder koken te omvatten.

>[!MORELIKETHIS]
>
>* [ Steun voor het Activeren van Universal IDs ](/help/dsp/audiences/universal-ids.md)
>* [ creeer een Herbruikbaar publiek ](reusable-audience-create.md)
>* [ creeer en voer een Segment van de Douane uit ](custom-segment-create.md)
>* [ creeer en voer a [!UICONTROL CCPA Opt-Out-of-Sale] Segment ](ccpa-opt-out-segment-create.md) uit
>* [ Ongeveer de Bronnen van het Publiek van de Eerste Partij ](/help/dsp/audiences/sources/source-about.md)
>* [ beheer de Bronnen van het publiek om Universele identiteitskaart Doelgroepen te activeren ](/help/dsp/audiences/sources/source-manage.md)
>* [ manueel de Invoer Voor authentiek verklaarde Segmenten van  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [ Beschikbare Leveranciers van Gegevens van derden ](third-party-data-providers.md)
>* [ Montages van de Plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md)
