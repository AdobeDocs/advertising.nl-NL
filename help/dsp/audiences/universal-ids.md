---
title: Ondersteuning voor het activeren van Universal ID's
description: Leer over steun om uw universele segmenten van identiteitskaart in te voeren, douanesegmenten tot stand te brengen om universele IDs te volgen, en andere gebruikersidentificatoren in uw eerste-partijsegmenten in universele IDs voor het kokieloze richten om te zetten.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: 202f4ae8e6633672b7af12937f0b35da5052f7fc
workflow-type: tm+mt
source-wordcount: '1500'
ht-degree: 0%

---

# Ondersteuning voor het activeren van Universal ID&#39;s

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*eigenschap van Beta*

DSP ondersteunt universele id&#39;s op basis van personen voor koelapparaten, enkelvoudige apparaten (niet voor alle apparaten) die zich richten op digitale indelingen die worden ondersteund door DSP.

* U kunt uw geverifieerde [[!DNL LiveRamp] [!DNL RampIDs]] handmatig rechtstreeks naar DSP verzenden via het [!DNL LiveRamp] [!DNL Connect] -dashboard. Zie &quot;[ manueel de Invoer Authenticated Segmenten van  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md).&quot;

* DSP kan uw eerste-partijsegmenten die uit gehakt e-mailIDs worden samengesteld binnen uw platform van het klantengegeven (CDP) en hen omzetten in [!DNL LiveRamp] [!DNL RampIDs] en [!DNL Unified ID 2.0 (UID2.0)] IDs. Voor meer informatie over de gesteunde platforms van klantengegevens, zien de beschikbare eigenschappen voor elk gesteund universeel type van identiteitskaart, en de verwante werkschema&#39;s, &quot;[ Ongeveer de Bronnen van het Publiek van de Eerste Partij ](/help/dsp/audiences/sources/source-about.md).&quot;

* U kunt aangepaste segmenten maken die gebruikers bijhouden die zijn gekoppeld aan universele id&#39;s van ID5 en die worden blootgesteld aan advertenties van mobiele en desktopapparaten en die specifieke webpagina&#39;s bezoeken. ID5 gebruikt een probabilistisch model om een identiteitskaart toe te wijzen die uit diverse gebruikerssignalen en browser signalen wordt afgeleid. Voor instructies, zie &quot;[ creëren en een Segment van de Douane uitvoeren ](/help/dsp/audiences/custom-segment-create.md).&quot;

* Secties van derden van sommige leveranciers kunnen automatisch universele id&#39;s bevatten naast gebruikers die worden bijgehouden door cookies of apparaat-id&#39;s. Segmenten van [!DNL Eyeota] kunnen bijvoorbeeld automatisch ID5-id&#39;s bevatten en segmenten van [!DNL Lotame] kunnen UID2.0-id&#39;s bevatten. De segmentdetails omvatten de grootte voor elk type. De gebruikelijke gebruiksvergoeding voor elk segment, die naast de segmentnaam wordt vermeld, is van toepassing; er worden geen extra kosten in rekening gebracht voor de ID5-id&#39;s.

## Rapportage per type Universal ID

* **de rapporten van de Douane:** De kosten, de indruk, de klik, de omzetting, en de frequentiegegevens door het universele type van identiteitskaart zijn beschikbaar in douanerapporten.

* **[!DNL Analytics]rapporten:** Adverteerders met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) die alle vereiste stappen hebben geïmplementeerd, kunnen doorkijkconversies via Universal ID bekijken in [!DNL Analytics] .

  >[!IMPORTANT]
  >
  >Voor juiste omzettingsattributie, zorg ervoor dat klikthrough URLs voor uw advertenties zowel [ EF identiteitskaart als AMO identiteitskaart ](/help/integrations/analytics/ids.md) omvatten.

* **de details van het Segment:** voor alle segmenttypes, omvatten de segmentdetails de publieksgrootte door universeel type van identiteitskaart en door het apparatentype dat door koekjes of apparaat IDs wordt gevolgd.

## Hoe te om een Universeel Publiek van identiteitskaart in Uw Plaatsen te richten

>[!NOTE]
>
>U kunt de beoogde id-typen niet wijzigen in een live plaatsing. Indien nodig kunt u een live plaatsing dupliceren en de beoogde id-typen wijzigen in de nieuwe plaatsing.

Ga als volgt te werk in een nieuwe, geplande of gepauzeerde plaatsing:

1. Geef in de sectie [!UICONTROL Geo-Targeting] de geografische gebieden op die u wilt gebruiken. Elke partner met een universele id staat toe dat gebruikers zich alleen richten op specifieke geografische gebieden en dat alleen in aanmerking komende id-typen beschikbaar zijn in de [!UICONTROL Targeting] -instellingen.

1. Ga als volgt te werk in de sectie [!UICONTROL Audience Targeting] :

   1. Selecteer in de instelling [!UICONTROL Included Audiences] het segment waarvoor gebruikersgegevens zijn omgezet in universele id&#39;s.

      U kunt desgewenst aanvullende segmenten opnemen.

   1. In de [!UICONTROL Targeting] -instellingen:

      1. Selecteer het universele-id-type waarop u wilt wijzen.

         Het plaatsen omvat de opties &quot;[!UICONTROL Legacy IDs]&quot; en &quot;[!UICONTROL Universal ID],&quot;die subopties &quot;[!UICONTROL ID5],&quot; [!UICONTROL RampID],&quot;en &quot;[!UICONTROL Unified ID2.0]&quot;kunnen omvatten. De geselecteerde geografische doelstellingen bepalen de beschikbare subopties.

         U kunt zowel &quot;[!UICONTROL Legacy IDs]&quot;als &quot;[!UICONTROL Universal ID] selecteren,&quot;maar u kunt slechts één type van universele identiteitskaart per plaatsing selecteren. Wanneer je zowel oude als universele id&#39;s selecteert, krijgt universele id&#39;s de voorkeur voor biedingen.

      1. (Indien nodig) Accepteer de serviceovereenkomst voor het gebruik van universele id&#39;s.

         Voordat u gegevens kunt converteren naar een nieuw type id, moet een gebruiker in de DSP account de serviceovereenkomst accepteren. De voorwaarden moeten slechts eenmaal per ID-type per account worden geaccepteerd.

Zie &quot;[ Montages van de Plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md).&quot;

## Aanbevolen procedures voor het testen en valideren van gegevens

Gebruik de volgende aanbevolen procedures voor op [!DNL RampID] gebaseerde segmenten en op ID5 gebaseerde segmenten, waarvoor Adobe Analytics-metingen beschikbaar zijn.

* Ongeveer 24 uur nadat u een segment activeert, controleer het omgezette aantal identiteitskaart voor het segment binnen [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Neem contact op met het accountteam van de Adobe als het aantal id&#39;s onverwacht is.

  Zie &quot;[ de Variaties van Gegevens tussen E-mail IDs en Universele IDs ](#universal-ids-data-variances)&quot;voor meer informatie over hoe de segmenttellingen kunnen variëren.

* Wijzig de bestaande pakketten en plaatsen niet. Nochtans, als u geen stijgende begroting hebt om universele IDs te testen, dan verminder de originele begrotingen om de tests te financieren.

* Kopieer uw originele pakketten en plaatsingen, pas de begrotingen aan die op de grootte van de test worden gebaseerd, verander het publiek om [!DNL RampID] - gebaseerde segmenten (voor voor authentiek verklaarde gebruikers) of op ID5-Gebaseerde segmenten (voor niet voor authentiek verklaarde gebruikers) te gebruiken, en verifieer dat de nieuwe pakketten en de plaatsen hun volledige begrotingen uitgeven.

   * Als u de prestaties van universele id-gebaseerde segmenten wilt vergelijken met de prestaties van plaatsingen voor andere publiek-id&#39;s, zoals cookies of mobiele advertentie-id&#39;s, maakt u een campagne met een aparte universele id-gebaseerde plaatsing en een oudere ID-gebaseerde plaatsing.

     Voor een volledige het opnieuw richten test, doel zowel RampIDs voor voor authentiek verklaarde gebruikers als ID5s voor niet voor authentiek verklaarde gebruikers.

     De beste prestaties leveren zou niet de primaire vergelijking moeten zijn. Bepaal in plaats daarvan welke id&#39;s goed schalen, wat uw optimalisatie en begrotingstoewijzingen later kan beïnvloeden. Het langetermijndoel is het compenseren van verloren indrukken en plaatsverkeer wanneer de koekjes verouderd zijn.

   * Als u het totale bereik van de browser wilt vergelijken, richt u op universele ID gebaseerde segmenten en verouderde ID-gebaseerde segmenten in dezelfde plaatsing. Gebruik de zelfde campagnemontages zoals het vorige gebruiksgeval, behalve dat te hoeven u niet om het campagnebudget te verdelen.

     Biedvoorkeur wordt gegeven aan universele id&#39;s, maar oudere id&#39;s ontvangen biedingen als universele id&#39;s niet beschikbaar zijn. Vergelijk bereik in verschillende browsers (waaronder Chrome, Safari en Mozilla).

     >[!NOTE]
     >
     >De frequentietoewijzing is van toepassing op een individuele identiteitskaart. Wanneer een gebruiker veelvoudige types van identiteitskaart heeft, zou u die gebruiker kunnen bereiken meer dan u verwacht.

* Herinner dat het bereik voor voor authentiek verklaarde publiekssegmenten natuurlijk kleiner is dan het bereik voor op koekjes-gebaseerde segmenten, en dat het gebruiken van extra het richten opties uw bereik verder vermindert. Wees voorzichtig met het gebruik van korrelige doelen, vooral door meerdere doelen te verbinden met AND-instructies.

## Gegevensvariaties tussen e-mailadressen en universele id&#39;s {#universal-ids-data-variances}

### Aanvaardbare variantieniveaus

De vertaalsnelheid van gehashte e-mailadressen naar universele id&#39;s moet groter zijn dan 90%; de vertaalsnelheid voor [!DNL RampIDs] moet met name 95% zijn als alle gehashte e-mailadressen uniek zijn. Als u bijvoorbeeld 100 gehashte e-mailadressen verzendt van het gegevensplatform van uw klant, moeten deze worden vertaald naar minimaal 95 [!DNL RampIDs] of meer dan 90 andere typen universele id&#39;s. Een lager vertaaltarief kan op een uitgifte wijzen. Zie &quot;[ OORZAKEN van variantie ] (#Universal-ids-data-variances-veroorzaakt&quot;voor mogelijke verklaringen.

Neem voor [!DNL RampIDs] contact op met het accountteam van de Adobe voor verder onderzoek als de vertaalkosten lager zijn dan 70%.

### Oorzaken van variantie {#universal-ids-data-variances-causes}

* Alle segmenten:

  Het segment-aan-apparaat aantal gebruikt een probabilistisch model, dat een foutenvariantie van +/- 5% heeft. Dit betekent dat het aantal kijkers met 5% kan worden overschat of onderschat.

* Vertaalde e-mailadressen naar [!DNL RampIDs]:

   * Wanneer meerdere profielen dezelfde e-mailid gebruiken, kan het aantal DSP segmenten lager zijn dan het aantal profielen in het gegevensplatform van uw klant. In Adobe Photoshop kunt u bijvoorbeeld een bedrijfsaccount en een persoonlijke account maken met één e-mailadres. Maar als beide profielen bij dezelfde persoon horen, worden de profielen toegewezen aan één e-mailid en dienovereenkomstig aan één [!DNL RampID] .

   * Een [!DNL RampID] kan worden bijgewerkt naar een nieuwe waarde. Als [!DNL LiveRamp] een e-mailid niet herkent of deze niet kan toewijzen aan een bestaande [!DNL RampID] in de database, wordt een nieuwe [!DNL RampID] toegewezen aan de e-mailid. Als ze de e-mailid later kunnen toewijzen aan een andere [!DNL RampID] of meer informatie over dezelfde e-mailid kunnen verzamelen, werken ze de [!DNL RampID] bij naar een nieuwe waarde. [!DNL LiveRamp] verwijst naar deze handeling als een upgrade van een &#39;afgeleide&#39; [!DNL RampID] naar een &#39;onderhouden&#39; [!DNL RampID] . Nochtans, krijgt DSP geen afbeeldingen tussen afgeleid en gehandhaafd [!DNL RampIDs] en kan daarom niet de vorige versie van RampID uit het DSP segment verwijderen. In dit geval kan het aantal segmenten groter zijn dan het aantal profielen.

     Voorbeeld: een gebruiker meldt zich aan bij de [!DNL Adobe] -website en bezoekt de Photoshop-pagina. Als [!DNL LiveRamp] geen bestaande informatie over de e-mailid heeft, wijzen ze deze als afgeleid toe [!DNL RampID] , bijvoorbeeld D123. Vijftien dagen later bezoekt de gebruiker dezelfde pagina, maar [!DNL LiveRamp] heeft de [!DNL RampID] gedurende die 15 dagen bijgewerkt en de [!DNL RampID] opnieuw toegewezen aan M123. Hoewel het segment &quot;Photoshop Enthusiast&quot; van het klantgegevensplatform slechts één e-mailadres voor de gebruiker heeft, heeft het DSP segment twee RampID&#39;s: D123 en M123.

## Problemen oplossen

Als u het aantal gebruikers niet ziet, of als uw publieksgrootte laag is, dan controleer het volgende:

* Als u [!DNL Flashtalking] - of [!DNL Google Campaign Manager 360] -advertenties gebruikt, moet u ervoor zorgen dat de juiste macro&#39;s worden toegevoegd wanneer u op URL&#39;s van uw advertenties klikt. Zie de macro&#39;s voor [[!DNL Flashtalking]  advertenties ](/help/integrations/analytics/macros-flashtalking.md) en [[!DNL Google Campaign Manager 360]  advertenties ](/help/integrations/analytics/macros-google-campaign-manager.md).

* Zorg ervoor dat de juiste, universele id partnerspecifieke code op uw website wordt geïmplementeerd om gebeurtenissen en advertentieblootstellingen op locatie te laten overeenkomen. Werk zo nodig samen met uw [!DNL LiveRamp] - of [!DNL ID5] -vertegenwoordiger.

* (Voor [!DNL RampIDs] en [!DNL UID 2.0] IDs) zorg ervoor dat uw [ DSP gegevensbron correct ](/help/dsp/audiences/sources/source-manage.md#source-settings) wordt gevormd, en dat de gebruikertellingen voor de geproduceerde publiekssegmenten bevolkt zijn.

* Als uw bereik kleiner is dan u verwacht, controleert u of de logica van het publiekssegment niet te korrelig is.

* Zorg ervoor dat uw campagne, pakket, en plaatsingsmontages correct zijn.<!-- wording-->

Neem contact op met het accountteam van de Adobe als u het probleem niet kunt oplossen.

>[!MORELIKETHIS]
>
>* [ Ongeveer de Bronnen van het Publiek van de Eerste Partij ](/help/dsp/audiences/sources/source-about.md)
>* [ beheert de Bronnen van het Publiek om Universele Soorten van identiteitskaart ](/help/dsp/audiences/sources/source-manage.md) te activeren
>* [ creeer en voer een Segment van de Douane uit ](/help/dsp/audiences/custom-segment-create.md)
>* [ manueel de Invoer Authenticated Segmenten van  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [ Ongeveer het Beheer van het Publiek ](/help/dsp/audiences/audience-about.md)
>* [ Montages van de Plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md)
