---
title: Een aangepast segment maken en implementeren
description: Leer hoe u een aangepast segment kunt maken en implementeren om gebruikers te volgen die worden blootgesteld aan advertenties of gebruikers die uw webpagina's bezoeken.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 3774da55139fd9f70162c931dd7708e8e258ad83
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 0%

---

# Een aangepast segment maken en implementeren

U kunt uw eigen gegevens van het eerste publiek verzamelen door een douane DSP segment te creëren en uit te voeren. U kunt het segment gebruiken om a) gebruikers te volgen die aan advertenties van Desktop en mobiele apparaten worden blootgesteld en b) gebruikers die specifieke webpagina&#39;s bezoeken. U kunt gebruikers in het segment later opnieuw richten met extra advertenties of gebruikers in het segment verhinderen extra advertenties te ontvangen.

>[!NOTE]
>
>Om gebruikers IDs van consument te volgen opt-out-of-verkoop verzoeken op uw website, per de Wet van de Privacy van de consument van Californië (CCPA), creeer a [ opt-out-of-verkoop segment CCPA ](ccpa-opt-out-segment-create.md).

## Vereisten voor segmenten om ID5-id&#39;s bij te houden

*eigenschap van Beta*

* Voordat u een segment genereert om gebruikers bij te houden die aan id5-id&#39;s zijn gekoppeld, ondertekent u een overeenkomst met [!DNL ID5] en haalt u de partner-id van uw organisatie op. Neem voor instructies contact op met het accountteam van de Adobe.

* Voor metingen in Adobe Analytics moet u:

   1. Voltooi alle [ eerste vereisten voor het uitvoeren van  [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md), en zorg ervoor dat [ identiteitskaart van AMO en identiteitskaart van EF ](/help/integrations/analytics/ids.md) in uw het volgen URLs wordt bevolkt.

   1. Voeg de volgende parameter aan uw webpagina&#39;s vóór of binnen de [ code van JavaScript toe die voor  [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md) wordt vereist — overal alvorens de laatste gebeurtenisdienst wordt geïnitialiseerd.

      ```window.id5PartnerId=Your_ID5_PartnerID;```

      Voorbeeld:

      ```
      <script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
      <script>
        window.id5PartnerId=Your_ID5_PartnerID;
             if("undefined" != typeof AdCloudEvent)
                 AdCloudEvent('IMS ORG Id','rsid');
      </script>
      ```

      Zie &quot;[ Formaat van de conversie het volgen van de markeringen van JavaScript versie 3 ](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)&quot;en &quot;[ Formaat van de omzetting van JavaScript volgende etikettenversie 2 ](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)&quot;voor het volledige markeringsformaat.

   1. Gebruik om het even welk browser het zuiveren hulpmiddel om te verifiëren dat elke vraag aan het domein `lasteventf-tm.everesttech.net` in werking wordt gesteld en de parameter `_les_id5` met gecodeerde ID5 als waarde bevat.

## Een aangepast segment maken en implementeren

1. Maak het segment:

   1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL Segments]** .

   1. Klik boven de gegevenstabel op **[!UICONTROL Create]** .

   1. Voer een uniek **[!UICONTROL Segment Name]** in.

   1. Selecteer *[!UICONTROL Custom]* voor **[!UICONTROL Segment Type]** .

   1. Voer de waarde **[!UICONTROL Lookback Window]** in. Dit is het aantal dagen dat de cookie van een gebruiker in het segment blijft staan.

      Het standaardvenster is 45 dagen. Voer een waarde tussen 1 en 365 in.

   1. Klik op **[!UICONTROL Advanced]** om de geavanceerde instellingen uit te vouwen en selecteer vervolgens de typen gebruikers-id&#39;s die de segmenttag bijhoudt:

      * *[!UICONTROL Cookies]:* (Het gebrek) de segmentmarkering houdt koekjes bij.

      * [!UICONTROL Universal IDs (Beta)]:

         * *[!UICONTROL ID5]:* De segmenttag traceert [!DNL ID5] id&#39;s. Er worden geen kosten in rekening gebracht voor afbeeldingen die aan universele id&#39;s worden geleverd.

        **[!UICONTROL Terms of Service]:** De serviceovereenkomst voor het gebruik van universele id&#39;s. Je of een andere gebruiker in de DSP account moet de voorwaarden één keer accepteren voordat je universele id&#39;s voor een nieuw type id kunt gebruiken. Voor klanten met beheerde de dienstcontracten, zal uw Team van de Rekening van de Adobe uw toestemming krijgen en zal de termijnen namens uw organisatie goedkeuren. Om de termijnen te lezen, klik **>**. Schuif naar de onderkant van de voorwaarden en klik op **[!UICONTROL Accept]** om de voorwaarden te accepteren.

   1. Klik op **[!UICONTROL Save]**.

1. Kopieer en implementeer tags om het segment bij te houden, indien nodig:

   1. Ga terug naar **[!UICONTROL Audiences]** > **[!UICONTROL Segments]** .

   1. Plaats de cursor op de segmentrij en klik op **[!UICONTROL Get Pixel]** .

      * Ga als volgt te werk om bezoekers van het bureaublad en mobiele apparaten bij te houden op een webpagina:

         1. Kopieer de volgende markering van de paginamening, die &quot; [!UICONTROL Desktop or mobile websites]&quot; wordt geëtiketteerd.

         1. (Tags voor segmenten die [!DNL ID5] id&#39;s bijhouden) Vervang `ID5_PARTNER_ID` in de gekopieerde tag door de partner-id die [!DNL ID5] aan uw organisatie is toegewezen.

            Als de ID5-partner bijvoorbeeld `abcde` is en de gegenereerde segmenttag bestaat uit

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            Vervang `ID5_PARTNER_ID` vervolgens door `abcde` in de tag voor het volgende:

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            Uw organisatie heeft de partner-id ontvangen toen deze een overeenkomst met [!DNL ID5] ondertekende. Neem contact op met het accountteam van de Adobe als u uw partner-id niet kent.

            Deze stap is niet nodig voor tags om [!DNL ID5] -id&#39;s bij te houden voor gebruikers die worden blootgesteld aan een advertentie-eenheid op desktops of mobiele apparaten.

         1. Geef de tag door aan de adverteerder of websitecontactpersoon voor implementatie.

            De IT-afdeling of andere groep van de adverteerder moet mogelijk de implementatie van de tag plannen of hierover worden geïnformeerd.

      * Om gebruikers te volgen die aan een advertentie-eenheid op Desktop of mobiele apparaten worden blootgesteld:

         1. Kopieer de volgende code van de indruk, die &quot; [!UICONTROL Desktop or mobile ads]&quot; wordt geëtiketteerd.

         1. Voeg de tag toe aan de tab [!UICONTROL Pixel] voor elke relevante advertentie of aan de sectie [!UICONTROL Event Pixels] van de instellingen [[!UICONTROL Tracking] voor elke relevante plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking) .

Zodra een volgende markering wordt uitgevoerd, kunt u het segment in de publieksdoelstellingen of uitsluitingen voor om het even welke plaatsing gebruiken.

>[!TIP]
>
>Houd de segmentgrootte bij terwijl gebruikers worden bijgehouden.

>[!MORELIKETHIS]
>
>* [ Ongeveer het Beheer van het Publiek ](audience-about.md)
>* [ geef de Informatie van het Segment ](segment-edit.md) uit
>* [ Schrap een Segment ](segment-delete.md)
>* [ Mening Volgend Pixels voor een Segment ](segment-view-pixels.md)
>* [ Aandeel of Einde delend een Segment ](segment-share.md)
>* [ creeer en voer a [!UICONTROL CCPA Opt-Out-of-Sale] Segment ](ccpa-opt-out-segment-create.md) uit
>* [ creeer een Herbruikbaar publiek ](reusable-audience-create.md)
>* [ Beschikbare Leveranciers van Gegevens van derden ](third-party-data-providers.md)
>* [ Montages van de Plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md)
