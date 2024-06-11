---
title: Ondersteuning voor het activeren van Universal ID's
description: Leer over steun om uw universele segmenten van identiteitskaart in te voeren, douanesegmenten tot stand te brengen om universele IDs te volgen, en andere gebruikersidentificatoren in uw eerste-partijsegmenten in universele IDs voor het kokieloze richten om te zetten.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: 4b8dc6e691516d87e391802b54664b96ad603b75
workflow-type: tm+mt
source-wordcount: '1377'
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

## Rapportage per type Universal ID

* **Aangepaste rapporten:** Kostprijs-, indruk-, klik-, conversie- en frequentiegegevens per universeel id-type zijn beschikbaar in aangepaste rapporten.

* **[!DNL Analytics]rapporten:** Adverteerders met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) die alle vereiste stappen hebben geïmplementeerd, kunnen doorkijkconversies via Universal ID-type bekijken in [!DNL Analytics].

  >[!IMPORTANT]
  >
  >Voor een juiste conversie-toewijzing moet u ervoor zorgen dat de URL&#39;s waarop u klikt voor uw advertenties zowel de [EF-id en AMO-id](/help/integrations/analytics/ids.md).

* **Segmentdetails:** Voor alle segmenttypes, omvatten de segmentdetails de publieksgrootte door universeel type van identiteitskaart en door het apparatentype dat door koekjes of apparaat IDs wordt gevolgd.

## Hoe te om een Universeel Publiek van identiteitskaart in Uw Plaatsen te richten

>[!NOTE]
>
>U kunt de beoogde id-typen niet wijzigen in een live plaatsing. Indien nodig kunt u een live plaatsing dupliceren en de beoogde id-typen wijzigen in de nieuwe plaatsing.

Ga als volgt te werk in een nieuwe, geplande of gepauzeerde plaatsing:

1. In de [!UICONTROL Geo-Targeting] in de sectie, de geografische gebieden specificeren waarop de actie betrekking heeft. Elke partner van universele id staat gebruiker toe slechts gericht op specifieke geografische gebieden en slechts zijn de in aanmerking komende types van identiteitskaart beschikbaar in [!UICONTROL Targeting] instellingen.

1. In de [!UICONTROL Audience Targeting] Ga als volgt te werk:

   1. In de [!UICONTROL Included Audiences] Selecteer het segment waarvoor gebruikersgegevens zijn omgezet in universele id&#39;s.

      U kunt desgewenst aanvullende segmenten opnemen.

   1. In de [!UICONTROL Targeting] instellingen:

      1. Selecteer het universele-id-type waarop u wilt wijzen.

         De instelling bevat de opties &quot;[!UICONTROL Legacy IDs]&quot; en &quot;[!UICONTROL Universal ID], die de subopties kunnen omvatten &quot;[!UICONTROL ID5],&quot; &quot;[!UICONTROL RampID],&quot; en &quot;[!UICONTROL Unified ID2.0].&quot; De geselecteerde geografische doelstellingen bepalen de beschikbare subopties.

         U kunt beide &quot;[!UICONTROL Legacy IDs]&quot; en &quot;[!UICONTROL Universal ID],&quot; maar u kunt slechts één type universele id selecteren per plaatsing. Wanneer je zowel oude als universele id&#39;s selecteert, krijgt universele id&#39;s de voorkeur voor biedingen.

      1. (Indien nodig) Accepteer de serviceovereenkomst voor het gebruik van universele id&#39;s.

         Voordat u gegevens kunt converteren naar een nieuw type id, moet een gebruiker in de DSP account de serviceovereenkomst accepteren. De voorwaarden moeten slechts eenmaal per ID-type per account worden geaccepteerd.

Zie &quot;[Plaatsingsinstellingen](/help/dsp/campaign-management/placements/placement-settings.md).&quot;

## Aanbevolen procedures voor het testen en valideren van gegevens

Gebruik de volgende aanbevolen procedures voor [!DNL RampID]Op -gebaseerde segmenten en op ID5 gebaseerde segmenten, waarvoor Adobe Analytics-metingen beschikbaar zijn.

* Ongeveer 24 uur nadat u een segment activeert, controleer het omgezette aantal identiteitskaart voor het segment binnen [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Neem contact op met het accountteam van de Adobe als het aantal id&#39;s onverwacht is.

  Zie &quot;[Oorzaken voor gegevensvariaties tussen e-mailadressen en universele id&#39;s](#universal-ids-data-variances)&quot; voor meer informatie over hoe de segmenttellingen kunnen variëren.

* Wijzig de bestaande pakketten en plaatsen niet. Nochtans, als u geen stijgende begroting hebt om universele IDs te testen, dan verminder de originele begrotingen om de tests te financieren.

* Kopieer de originele pakketten en plaatsingen, pas de budgetten aan op basis van de grootte van de test, wijzig het publiek dat u wilt gebruiken [!DNL RampID]-based segmenten (voor voor authentiek verklaarde gebruikers) of op ID5-Gebaseerde segmenten (voor niet voor authentiek verklaarde gebruikers), en verifieer dat de nieuwe pakketten en de plaatsen hun volledige begrotingen uitgeven.

   * Als u de prestaties van universele id-gebaseerde segmenten wilt vergelijken met de prestaties van plaatsingen voor andere publiek-id&#39;s, zoals cookies of mobiele advertentie-id&#39;s, maakt u een campagne met een aparte universele id-gebaseerde plaatsing en een oudere ID-gebaseerde plaatsing.

     Voor een volledige het opnieuw richten test, doel zowel RampIDs voor voor authentiek verklaarde gebruikers als ID5s voor niet voor authentiek verklaarde gebruikers.

     De beste prestaties leveren zou niet de primaire vergelijking moeten zijn. Bepaal in plaats daarvan welke id&#39;s goed schalen, wat uw optimalisatie en begrotingstoewijzingen later kan beïnvloeden. Het langetermijndoel is het compenseren van verloren indrukken en plaatsverkeer wanneer de koekjes verouderd zijn.

   * Als u het totale bereik van de browser wilt vergelijken, richt u op universele ID gebaseerde segmenten en verouderde ID-gebaseerde segmenten in dezelfde plaatsing. Gebruik de zelfde campagnemontages zoals het vorige gebruiksgeval, behalve dat te hoeven u niet om het campagnebudget te verdelen.

     Biedvoorkeur wordt gegeven aan universele id&#39;s, maar oudere id&#39;s ontvangen biedingen als universele id&#39;s niet beschikbaar zijn. Vergelijk bereik in verschillende browsers (inclusief Chrome, Safari en Mozilla).

     >[!NOTE]
     >
     >De frequentietoewijzing is van toepassing op een individuele identiteitskaart. Wanneer een gebruiker veelvoudige types van identiteitskaart heeft, zou u die gebruiker kunnen bereiken meer dan u verwacht.

* Herinner dat het bereik voor voor authentiek verklaarde publiekssegmenten natuurlijk kleiner is dan het bereik voor op koekjes-gebaseerde segmenten, en dat het gebruiken van extra het richten opties uw bereik verder vermindert. Wees voorzichtig met het gebruik van korrelige doelen, vooral door meerdere doelen te verbinden met AND-instructies.

## Oorzaken voor gegevensvariaties tussen e-mailadressen en universele id&#39;s {#universal-ids-data-variances}

* Vertaalde e-mailadressen zijn vertaald naar id5:

  Het probabilistische model heeft een foutenvariantie van +/- 5%. Dit betekent dat het aantal kijkers met 5% kan worden overschat of onderschat.

* Vertaalde e-mailadressen naar [!DNL RampIDs]:

   * Wanneer meerdere profielen dezelfde e-mailid gebruiken, kan het aantal DSP segmenten lager zijn dan het aantal profielen in het gegevensplatform van uw klant. In Adobe Photoshop kunt u bijvoorbeeld een bedrijfsaccount en een persoonlijke account maken met één e-mailadres. Maar als beide profielen tot hetzelfde segment behoren, worden de profielen toegewezen aan één e-mailid en aan één overeenkomstige e-mailid [!DNL RampID].

   * A [!DNL RampID] kan worden geüpgraded naar een nieuwe waarde. Indien [!DNL LiveRamp] herkent geen e-mailid of kan deze niet toewijzen aan een bestaande id [!DNL RampID] in zijn gegevensbestand, dan wijst het een nieuw toe [!DNL RampID] naar de e-mailadres. In de toekomst, wanneer zij e-mailidentiteitskaart aan een andere kunnen toewijzen [!DNL RampID] of meer informatie over dezelfde e-mailadres verzamelen, upgraden ze de [!DNL RampID] naar een nieuwe waarde. [!DNL LiveRamp] verwijst naar deze actie als een upgrade van een &quot;afgeleid&quot; product [!DNL RampID] aan een &quot;onderhouden&quot; [!DNL RampID]. DSP krijgt echter geen toewijzingen tussen afgeleid en onderhouden [!DNL RampIDs] en kan daarom niet de vorige versie van RampID uit het DSP segment verwijderen. In dit geval kan het aantal segmenten groter zijn dan het aantal profielen.

     Voorbeeld: een gebruiker meldt zich aan bij de [!DNL Adobe] website en bezoekt de Photoshop-pagina. Indien [!DNL LiveRamp] heeft geen bestaande informatie over de e-mailid en wijst deze vervolgens een afgeleid e-mailadres toe [!DNL RampID], D123. Vijftien dagen later bezoekt de gebruiker dezelfde pagina, maar [!DNL LiveRamp] heeft de [!DNL RampID] gedurende die 15 dagen en heeft de [!DNL RampID] naar M123. Hoewel het segment &quot;Photoshop Enthusiast&quot; van het klantgegevensplatform slechts één e-mailadres voor de gebruiker heeft, heeft het DSP segment twee RampID&#39;s: D123 en M123.

## Problemen oplossen

Als u het aantal gebruikers niet ziet, of uw publieksgrootte is laag, dan controleer het volgende:

* Als u [!DNL Flashtalking] of [!DNL Google Campaign Manager 360] voegt u toe, controleert u vervolgens of de URL&#39;s waarop de advertenties klikken, de juiste macro&#39;s bevatten. Zie de macro&#39;s voor [[!DNL Flashtalking] advertenties](/help/integrations/analytics/macros-flashtalking.md) en [[!DNL Google Campaign Manager 360] advertenties](/help/integrations/analytics/macros-google-campaign-manager.md).

* Zorg ervoor dat de juiste, universele id partnerspecifieke code op uw website wordt geïmplementeerd om gebeurtenissen en advertentieblootstellingen op locatie te laten overeenkomen. Werk met uw [!DNL LiveRamp] of [!DNL ID5] indien nodig.

* (Voor [!DNL RampIDs] en [!DNL UID 2.0] Id&#39;s) Controleer of uw [DSP gegevensbron is correct geconfigureerd](/help/dsp/audiences/sources/source-manage.md#source-settings)en dat de tellingen van de gebruiker worden gevuld voor de gegenereerde publiekssegmenten.

* Als uw bereik kleiner is dan u verwacht, controleert u of de logica van het publiekssegment niet te korrelig is.

Neem contact op met het accountteam van de Adobe als u het probleem niet kunt oplossen.

>[!MORELIKETHIS]
>
>* [Ongeveer de Bronnen van het Publiek van de Eerste Partij](/help/dsp/audiences/sources/source-about.md)
>* [Bronnen voor publiek beheren om Universal ID-publiek te activeren](/help/dsp/audiences/sources/source-manage.md)
>* [Een aangepast segment maken en implementeren](/help/dsp/audiences/custom-segment-create.md)
>* [Geverifieerde segmenten handmatig importeren uit [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
>* [Plaatsingsinstellingen](/help/dsp/campaign-management/placements/placement-settings.md)
