---
title: Ondersteuning voor het activeren van Universal ID's
description: Leer over steun om uw universele segmenten van identiteitskaart in te voeren, douanesegmenten tot stand te brengen om universele IDs te volgen, en andere gebruikersidentificatoren in uw eerste-partijsegmenten in universele IDs voor het kokieloze richten om te zetten.
feature: DSP Audiences
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 0%

---

# Ondersteuning voor het activeren van Universal ID&#39;s

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Beta, functie*

DSP ondersteunt universele id&#39;s op basis van personen voor koelapparaten, enkelvoudige apparaten (niet voor alle apparaten) die zich richten op digitale indelingen die worden ondersteund door DSP.

* U kunt uw geverifieerde [[!DNL LiveRamp] [!DNL RampIDs]] rechtstreeks DSP met de [!DNL LiveRamp] [!DNL Connect] dashboard. Zie &quot;[Geverifieerde segmenten handmatig importeren uit [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md).&quot;

* DSP kan uw eerste-partijsegmenten die uit gehakte e-mailidentiteitskaart worden samengesteld binnen uw platform van klantengegevens (CDP) opnemen en hen omzetten in [!DNL LiveRamp] [!DNL RampIDs] en [!DNL Unified ID 2.0 (UID2.0)] ID&#39;s. Voor meer informatie over de ondersteunde platforms voor klantgegevens, de beschikbare functies voor elk ondersteund universeel id-type en de bijbehorende workflows raadpleegt u &quot;[Ongeveer de Bronnen van het Publiek van de Eerste Partij](/help/dsp/audiences/sources/source-about.md).&quot;

* U kunt aangepaste segmenten maken die gebruikers bijhouden die zijn gekoppeld aan universele id&#39;s van ID5 en die worden blootgesteld aan advertenties van mobiele en desktopapparaten en die specifieke webpagina&#39;s bezoeken. ID5 gebruikt een probabilistisch model om een identiteitskaart toe te wijzen die uit diverse gebruikerssignalen en browser signalen wordt afgeleid. Zie voor instructies &quot;[Een aangepast segment maken en implementeren](/help/dsp/audiences/custom-segment-create.md).&quot;

* Segmenten van derden [!DNL Eyeota] en sommige andere leveranciers kunnen automatisch ID5-id&#39;s bevatten, naast gebruikers die worden bijgehouden door cookies of apparaat-id&#39;s. De segmentdetails omvatten de grootte voor elk type. De gebruikelijke gebruiksvergoeding voor elk segment, die naast de segmentnaam wordt vermeld, is van toepassing; er worden geen extra kosten in rekening gebracht voor de ID5-id&#39;s.

<!-- Make above statement more generic when other ID types are available 

* Some third-party segment vendors have started including universal IDs in their segments, and you can use them in saved audiences and as placement targets without any extra steps or extra fees.
-->

## Rapportage per type Universal ID

* **Aangepaste rapporten:** Kostprijs-, indruk-, klik-, conversie- en frequentiegegevens per universeel id-type zijn beschikbaar in aangepaste rapporten.

* **[!DNL Analytics]rapporten:** Adverteerders met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) die alle vereiste stappen hebben geïmplementeerd, kunnen doorkijkconversies via Universal ID-type bekijken in [!DNL Analytics].

* **Segmentdetails:** Voor alle segmenttypes, omvatten de segmentdetails de publieksgrootte door universeel type van identiteitskaart en door het apparatentype dat door koekjes of apparaat IDs wordt gevolgd.

## Hoe te om een Universeel Publiek van identiteitskaart in Uw Plaatsen te richten

>[!NOTE]
>
>U kunt de beoogde id-typen niet wijzigen in een live plaatsing. Indien nodig kunt u een live plaatsing dupliceren en de beoogde id-typen wijzigen in de nieuwe plaatsing.

Ga als volgt te werk in een nieuwe, geplande of gepauzeerde plaatsing:

* In de [!UICONTROL Geo-Targeting] in de sectie, de geografische gebieden specificeren waarop de actie betrekking heeft. Elke partner van universele id staat gebruiker toe slechts gericht op specifieke geografische gebieden en slechts zijn de in aanmerking komende types van identiteitskaart beschikbaar in [!UICONTROL Targeting] instellingen.

* In de [!UICONTROL Audience Targeting] Ga als volgt te werk:

   * In de [!UICONTROL Included Audiences] Selecteer het segment waarvoor gebruikersgegevens zijn omgezet in universele id&#39;s.

     U kunt desgewenst aanvullende segmenten opnemen.

   * In de [!UICONTROL Targeting] Selecteer het universele-id-type waarop u wilt wijzen.

     De instelling bevat de opties &quot;[!UICONTROL Legacy IDs]&quot; en &quot;[!UICONTROL Universal ID], die de subopties kunnen omvatten &quot;[!UICONTROL ID5],&quot; &quot;[!UICONTROL RampID],&quot; en &quot;[!UICONTROL Unified ID2.0].&quot; De werkelijke subopties worden bepaald door de geselecteerde geografische doelstellingen.

     U kunt beide &quot;[!UICONTROL Legacy IDs]&quot; en &quot;[!UICONTROL Universal ID],&quot; maar u kunt slechts één type universele id selecteren per plaatsing. Wanneer je zowel oude als universele id&#39;s selecteert, krijgt universele id&#39;s de voorkeur voor biedingen.

Zie &quot;[Plaatsingsinstellingen](/help/dsp/campaign-management/placements/placement-settings.md).&quot;

## Aanbevolen procedures voor het testen en valideren van gegevens

Gebruik de volgende aanbevolen procedures voor [!DNL RampID]Op -gebaseerde segmenten en op ID5 gebaseerde segmenten, waarvoor Adobe Analytics-metingen beschikbaar zijn.

* Ongeveer 24 uur nadat u een segment activeert, controleer het omgezette aantal identiteitskaart voor het segment binnen [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Neem contact op met het accountteam van de Adobe als het aantal id&#39;s onverwacht is.

  Zie &quot;[Oorzaken voor gegevensvariaties tussen e-mailadressen en universele id&#39;s](#universal-ids-data-variances)&quot; voor meer informatie over hoe de segmenttellingen kunnen variëren.

* Wijzig de bestaande pakketten en plaatsen niet. Nochtans, als u geen stijgende begroting hebt om universele IDs te testen, dan verminder de originele begrotingen om de tests te financieren.

* Kopieer de originele pakketten en plaatsingen, pas de budgetten aan op basis van de grootte van de test, wijzig het publiek dat u wilt gebruiken [!DNL RampID]-based segmenten (voor voor authentiek verklaarde gebruikers) of op ID5-Gebaseerde segmenten (voor niet voor authentiek verklaarde gebruikers), en verifieer dat de nieuwe pakketten en de plaatsen hun volledige begrotingen uitgeven.

   * Als u de prestaties van universele id-gebaseerde segmenten wilt vergelijken met de prestaties van plaatsingen voor andere publiek-id&#39;s, zoals cookies of mobiele advertentie-id&#39;s, maakt u een campagne met een aparte universele id-gebaseerde plaatsing en een oudere ID-gebaseerde plaatsing.

     De beste prestaties leveren zou niet de primaire vergelijking moeten zijn. Bepaal in plaats daarvan welke id&#39;s goed schalen, wat uw optimalisatie en begrotingstoewijzingen later kan beïnvloeden. Het langetermijndoel is het compenseren van verloren indrukken en plaatsverkeer wanneer de koekjes verouderd zijn.

   * Als u het totale bereik van de browser wilt vergelijken, richt u op universele ID gebaseerde segmenten en verouderde ID-gebaseerde segmenten in dezelfde plaatsing. Gebruik de zelfde campagnemontages zoals het vorige gebruiksgeval, behalve dat te hoeven u niet om het campagnebudget te verdelen.

     Biedvoorkeur wordt gegeven aan universele id&#39;s, maar oudere id&#39;s ontvangen biedingen als universele id&#39;s niet beschikbaar zijn. Vergelijk bereik in verschillende browsers (inclusief Chrome, Safari en Mozilla).

     >[!NOTE]
     >
     >De frequentietoewijzing is van toepassing op een individuele identiteitskaart. Wanneer een gebruiker veelvoudige types van identiteitskaart heeft, zou u die gebruiker kunnen bereiken meer dan u had verwacht.

* Herinner dat het bereik voor voor authentiek verklaarde publiekssegmenten natuurlijk kleiner is dan het bereik voor op koekjes-gebaseerde segmenten, en dat het gebruiken van extra het richten opties uw bereik verder vermindert. Wees voorzichtig met het gebruik van korrelige doelen, vooral door meerdere doelen te verbinden met AND-instructies.

## Oorzaken voor gegevensvariaties tussen e-mailadressen en universele id&#39;s {#universal-ids-data-variances}

Er zijn twee redenen voor variatie voor gehashte e-mailadressen waarnaar wordt vertaald [!DNL RampIDs]:

* Wanneer meerdere profielen dezelfde e-mailid gebruiken, kan het aantal DSP segmenten lager zijn dan het aantal profielen in het gegevensplatform van uw klant. In Adobe Photoshop kunt u bijvoorbeeld een bedrijfsaccount en een persoonlijke account maken met één e-mailadres. Maar als beide profielen tot hetzelfde segment behoren, worden de profielen toegewezen aan één e-mailid en aan één overeenkomstige e-mailid [!DNL RampID].

* A [!DNL RampID] kan worden geüpgraded naar een nieuwe waarde. Indien [!DNL LiveRamp] herkent geen e-mailid of kan deze niet toewijzen aan een bestaande id [!DNL RampID] in zijn gegevensbestand, dan wijst het een nieuw toe [!DNL RampID] naar de e-mailadres. In de toekomst, wanneer zij e-mailidentiteitskaart aan een andere kunnen toewijzen [!DNL RampID] of meer informatie over dezelfde e-mailadres verzamelen, upgraden ze de [!DNL RampID] naar een nieuwe waarde. [!DNL LiveRamp] verwijst naar deze actie als een upgrade van een &quot;afgeleid&quot; product [!DNL RampID] aan een &quot;onderhouden&quot; [!DNL RampID]. DSP krijgt echter geen toewijzingen tussen afgeleid en onderhouden [!DNL RampIDs] en kan daarom niet de vorige versie van RampID uit het DSP segment verwijderen. In dit geval kan het aantal segmenten groter zijn dan het aantal profielen.

  Voorbeeld: een gebruiker meldt zich aan bij de [!DNL Adobe] website en bezoek de Photoshop-pagina. Indien [!DNL LiveRamp] heeft geen bestaande informatie over de e-mailid en wijst deze vervolgens een afgeleid e-mailadres toe [!DNL RampID], D123. Vijftien dagen later bezoekt de gebruiker dezelfde pagina, maar [!DNL LiveRamp] heeft de [!DNL RampID] gedurende die 15 dagen en heeft de [!DNL RampID] naar M123. Hoewel het segment &quot;Photoshop Enthusiast&quot; van het klantgegevensplatform slechts één e-mailadres voor de gebruiker heeft, heeft het DSP segment twee RampID&#39;s: D123 en M123.

>[!MORELIKETHIS]
>
>* [Een doelbron maken om Universal ID-publiek te activeren](/help/dsp/audiences/sources/source-create.md)
>* [Gebruikersnamen converteren van [!DNL Adobe Real-Time CDP] naar universele id&#39;s](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Gebruikersnamen converteren van [!DNL Tealium] naar universele id&#39;s](/help/dsp/audiences/sources/source-tealium.md)
>* [Een aangepast segment maken en implementeren](/help/dsp/audiences/custom-segment-create.md)
>* [Geverifieerde segmenten handmatig importeren uit [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
>* [Plaatsingsinstellingen](/help/dsp/campaign-management/placements/placement-settings.md)