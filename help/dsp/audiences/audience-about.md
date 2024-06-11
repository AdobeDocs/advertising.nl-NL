---
title: Over het beheer van het publiek in DSP
description: Meer informatie over de functies voor publieksbeheer.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: ac3ceaf0e1d9f1708896d17ab413d23f366c4b36
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 0%

---

# Over het beheer van het publiek in DSP

In DSP kunt u publiekssegmenten en publiekssets maken en beheren, die u kunt gebruiken als doelen voor uw plaatsingen:

* Verzamel uw eigen gegevens van het eerste publiek door DSP segmenten te creëren en uit te voeren. U kunt gebruikers in het segment later opnieuw toewijzen met advertenties of u kunt voorkomen dat gebruikers in het segment advertenties ontvangen. U kunt de volgende typen segmenten maken:

   * [Aangepaste segmenten](/help/dsp/audiences/custom-segment-create.md) om a) gebruikers bij te houden die zijn blootgesteld aan advertenties van mobiele en desktopapparaten en b) gebruikers die specifieke webpagina&#39;s bezoeken. De tag tracking kan gebruikers bijhouden die zijn gebaseerd op cookies of gebruikers die zijn gekoppeld aan universele id&#39;s van ID5.

   * [CCPA opt-out of-of-sale segmenten](/help/dsp/audiences/ccpa-opt-out-segment-create.md) om de gebruikers-id&#39;s op uw website te traceren van de door de consument ingediende opt-out-of-sale aanvragen, overeenkomstig de California Consumer Privacy Act (CCPA). U kunt maandelijkse rapporten van de gebruikers-id&#39;s ophalen uit aanvragen om niet te verkopen.

     Voor meer informatie over de steun van de Adobe Advertising voor CCPA opt-out van verkoop verzoeken, zie [Adobe Advertising Support for the California Consumer Privacy Act: Consumer Opt-out Support](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* (Functie Bèta) [Lege id&#39;s ophalen en gebruiken voor kiezen zonder kokieten](/help/dsp/audiences/universal-ids.md):

   * De geverifieerde gegevens handmatig verzenden [!DNL LiveRamp] [!DNL RampID] segmenten rechtstreeks naar DSP.

   * Sta DSP toe om eerste-partijsegmenten van uw platform van klantengegevens in te voeren en hen te vertalen aan gesteunde universele types van identiteitskaart.

   * Neem zonder extra stappen ook segmenten van derden op die universele id&#39;s in uw plaatsingsdoelen bevatten.

* Een publieksbibliotheek maken van [herbruikbaar publiek](/help/dsp/audiences/reusable-audience-create.md). Opgeslagen doelgroepen bestaan uit een van uw beschikbare doelsegmenten en een van uw andere opgeslagen doelgroepen. Wijzigingen die u aanbrengt in een opgeslagen publiek, worden automatisch toegepast op alle plaatsen die het publiek als doel hebben of uitsluiten en op alle andere soorten publiek die het opgeslagen publiek bevatten.

  Opgeslagen publiek stelt mediaplanners in staat om het publiek zo nodig te groeperen door meerdere segmenten met behulp van complexe Booleaanse logica in te sluiten en uit te sluiten. De grootte van elk individueel segment en de totale publieksgrootte worden vermeld aangezien u een publiek bouwt. De managers van de campagne kunnen één of meerdere bewaarde publiek dan eenvoudig selecteren als plaatsingsdoelstellingen eerder dan manueel publieksdoelstellingen voor elke plaatsing vormen.

Er zijn ook extra publiekstypen beschikbaar voor plaatsing als doel.

## Eerste partij en gegevenssegmenten van derden importeren

U hebt vele opties om de segmenten van de eerste partij en van de derdegegevens in DSP in te voeren, gebruikend de DSP gebruikersinterface en/of door de diensten van de douaneinvoer.

* DSP kan je Adobe Audience Manager en andere [!DNL Adobe] doelgroepen. Voor voorwaarden en instructies raadpleegt u &quot;[Adobe Audience Manager-segmenten importeren voor advertentiedoeleinden](/help/integrations/audience-manager/import-audiences.md).

* DSP kan de segmenten van de eerste-partijgegevens van gesteunde platforms van klantengegevens aan segmenten met universele identiteitskaart omzetten gebruikend [Bronfunctie](/help/dsp/audiences/sources/source-about.md). U kunt [uw geverifieerde gegevens handmatig verzenden [!DNL LiveRamp] [!DNL RampID] segmenten rechtstreeks naar DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* DSP kunnen uw andere eerste-partijgegevenssegmenten direct van uw platform van het gegevensbeheer (DMP) invoeren en hen verstrekken aan om het even welke reeks adverteerders, zoals nodig.

* DSP kunnen aangepaste segmenten van derden importeren, waaronder complexe combinaties van segmenten van derden. U kunt de segmenten desgewenst aan elke set adverteerders aanbieden.

Neem contact op met het accountteam van de Adobe voor meer informatie.

## publiek beschikbaar als plaatsingsdoelen

U kunt uw plaatsingen aan alle volgende soorten publiek richten.

* Alle door de gebruiker gemaakte publiekssets die in DSP zijn opgeslagen.

* Alle door de gebruiker gemaakte publiekssegmenten die in DSP zijn gemaakt:

   * Aangepaste segmenten voor gebruikers die specifieke webpagina&#39;s hebben bezocht en gebruikers die zijn blootgesteld aan indrukken van specifieke advertenties.

     Er worden geen kosten in rekening gebracht voor afbeeldingen die aan universele id&#39;s worden geleverd.

   * CCPA opt-out-of-sale publiekssegmenten voor gebruikers die opt-out-of-sale verzoeken op uw website, volgens de California Consumer Privacy Act (CCPA) hebben ingediend.

* Alle geïmporteerde gegevenssegmenten van de eerste partij, inclusief segmenten die naar universele id&#39;s zijn vertaald.

  Er worden extra kosten in rekening gebracht voor afdrukken die aan universele id&#39;s worden geleverd. Zie &quot;[Ongeveer de Bronnen van het Publiek van de Eerste Partij](/help/dsp/audiences/sources/source-about.md)&quot; voor tarieven.

* Alle geïmporteerde gegevenssegmenten van derden.

* (Plaatsen die zich richten op de V.S. slechts) [Alle gegevenssegmenten van derden die beschikbaar zijn voor DSP klanten van meer dan 30 providers](/help/dsp/audiences/third-party-data-providers.md), inclusief [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast]en nog veel meer.

  U kunt zich richten op specifieke segmenten, die gebruikers richten die op publieksgegevens (bijvoorbeeld, gebruikers met specifieke demografie, belangen of intents, en/of gedragsprofielen) worden gebaseerd. U kunt bladeren door gegevensleverancier en categorie, naar segmenten door naam of segmentidentiteitskaart zoeken, of de resultaten door gegevensleverancier, totale segmentgrootte, Webbrowser telling, of apparatentelling filtreren.

  Voor segmenten van derden worden extra kosten aangerekend, die naast elke segmentnaam worden vermeld.

* (Adverteerders met Adobe Experience Platform en [!DNL Real-Time CDP], Adobe Audience Manager of Adobe Analytics die alleen conversietags voor Adobe Advertising JavaScript gebruiken) Alle beschikbare doelsegmenten van het type first-, second of third-party die zijn gemaakt in [!DNL Real-Time CDP], gemaakt in Audience Manager of gepubliceerd naar Adobe Experience Cloud vanuit Audience Manager of [!DNL Analytics].

  Prijzen voor het gebruik van de segmenten worden vooraf onderhandeld en zijn niet zichtbaar in DSP.

  Segmenten van [!DNL Analytics] zijn ongeveer een uur beschikbaar nadat u deze als publiek voor Experiencen Cloud hebt gemaakt of gepubliceerd. Segmenten die rechtstreeks afkomstig zijn van Audience Manager of [!DNL Real-Time CDP] zijn beschikbaar binnen 24 uur nadat u deze deelt.

  >[!NOTE]
  >
  >Zie de documentatie voor [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analyse](https://experienceleague.adobe.com/docs/analytics.html), en [de [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) voor informatie over vestiging en het verzamelen van gegevens voor segmenten in die oplossingen.

## Gegevens over doelgrootte

In Soorten publiek > Alle Soorten publiek en in de sectie Doelgroep van het publiek van plaatsingsmontages, kunt u elke segmentlijst door formaatwaaier, met inbegrip van de totale waaier en afzonderlijke waaiers voor specifieke apparatentypes of universele types van identiteitskaart filtreren.

![filteren op doelgrootte](/help/dsp/assets/audience-size-filter.png)

U kunt ook gedetailleerde gegevens over de publieksgrootte zien:

* De totale en actieve gededupliceerde publieksgrootte voor alle geselecteerde segmenten en opgeslagen doelgroepen wordt weergegeven en u kunt details per apparaattype (browser, mobiel of aangesloten tv) weergeven.

  ![de gecombineerde publieksgrootte](/help/dsp/assets/audience-size.png)

* Voor individuele segmenten, worden de totale publieksgrootte en CPM (indien van toepassing) getoond naast de segmentnaam.

  ![de individuele segmentgrootte](/help/dsp/assets/audience-size-segment.png)

* U kunt meer details over een afzonderlijk segment of een opgeslagen publiek weergeven, zoals de grootte per browser, mobiel, aangesloten tv en partner voor het universele-id-type. Voor opgeslagen publiek is de totale grootte het gedupliceerde totaal.

  ![het afzonderlijke segment of de opgeslagen publieksdetails](/help/dsp/assets/audience-size-segment-details.png)

## De weergave Soorten publiek

### De weergave Alle soorten publiek

In de [!UICONTROL All Audiences] In de Audience Library kunt u herbruikbare soorten publiek opslaan en beheren, waaronder groepen publiekssegmenten en zelfs andere opgeslagen soorten publiek. U kunt doelgroepen gebruiken als doelen voor meerdere plaatsen. Het aantal plaatsen waarin elk publiek wordt gebruikt wordt vermeld naast de plaatsingsnaam.

U kunt een publiek bewerken, klonen, verwijderen, exporteren of delen.

### De weergave Segmenten

In de [!UICONTROL Segments] alle gebruikers kunnen extra aangepaste segmenten maken.

De [!UICONTROL Segments] in de weergave worden ook de volgende segmenttypen weergegeven:

* Alle door de gebruiker gemaakte aangepaste segmenten zijn beschikbaar voor de gebruiker.

  U kunt de volgende markeringen voor om het even welke douanesegmenten bekijken u creeerde, en die segmenten met andere gebruikers delen. U kunt ook de aangepaste segmenten die u hebt gemaakt bewerken of verwijderen.

  U kunt geen aangepaste segmenten bewerken of delen die andere gebruikers met u hebben gedeeld.

* Alle eerste-partijsegmenten die worden ingevoerd zoals-is die aan de gebruiker beschikbaar zijn.

  U kunt geen eerste-partijsegmenten uitgeven of delen die met u werden gedeeld. Neem contact op met het accountteam van de Adobe als u de eerste-partijsegmenten met extra gebruikers moet delen.

* Alle aangepaste segmenten van derden zijn beschikbaar voor de gebruiker.

  U kunt segmenten van derden die met u zijn gedeeld, niet bewerken of delen. Neem contact op met het accountteam van de Adobe als u segmenten van derden met extra gebruikers wilt delen.

### De Bronweergave

In de [!UICONTROL Sources] bekijken, kunt u bronnen voor eerste-partijsegmenten in gesteunde platforms van klantengegevens vormen die u in segmenten wilt omzetten die gespecificeerde universele types van identiteitskaart bevatten. De bronmontages omvatten een auto-geproduceerde bronsleutel, die u aan uw platform van klantengegevens zult verstrekken om de verbinding te vestigen.

Voor meer informatie over de gesteunde platforms van klantengegevens, de gesteunde universele types van identiteitskaart en de werkschema&#39;s aan opstellingsverbindingen aan elk platform van de klantengegevens, zie &quot;[Bronnen](/help/dsp/audiences/sources/source-about.md).&quot;

De vertaalde segmenten zijn beschikbaar om in herbruikbaar publiek en in plaatsingsmontages voor het kiezen zonder koken te omvatten.

>[!MORELIKETHIS]
>
>* [Ondersteuning voor het activeren van Universal ID&#39;s](/help/dsp/audiences/universal-ids.md)
>* [Een herbruikbaar publiek maken](reusable-audience-create.md)
>* [Een aangepast segment maken en implementeren](custom-segment-create.md)
>* [Een [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Ongeveer de Bronnen van het Publiek van de Eerste Partij](/help/dsp/audiences/sources/source-about.md)
>* [Bronnen voor publiek beheren om Universal ID-publiek te activeren](/help/dsp/audiences/sources/source-manage.md)
>* [Geverifieerde segmenten handmatig importeren uit [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Beschikbare gegevensleveranciers van derden](third-party-data-providers.md)
>* [Plaatsingsinstellingen](/help/dsp/campaign-management/placements/placement-settings.md)
