---
title: Een aangepast segment maken en implementeren
description: Leer hoe u een aangepast segment kunt maken en implementeren om gebruikers te volgen die worden blootgesteld aan advertenties of gebruikers die uw webpagina's bezoeken.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Een aangepast segment maken en implementeren

U kunt uw eigen gegevens van het eerste publiek verzamelen door een douane DSP segment te creëren en uit te voeren. U kunt het segment gebruiken om a) gebruikers te volgen die aan advertenties van Desktop en mobiele apparaten worden blootgesteld en b) gebruikers die specifieke webpagina&#39;s bezoeken. U kunt gebruikers in het segment later opnieuw richten met extra advertenties of gebruikers in het segment verhinderen extra advertenties te ontvangen.

>[!NOTE]
>
>Als u gebruikers-id&#39;s wilt bijhouden van een aanvraag voor een opt-out-of-verkoop voor een consument op uw website, maakt u op basis van de California Consumer Privacy Act (CCPA) een [CCPA opt-out of-of-sales segment](ccpa-opt-out-segment-create.md).

## Vereisten voor segmenten om ID5-id&#39;s bij te houden

*Beta, functie*

* Voordat u een segment genereert om gebruikers bij te houden die aan id5-id&#39;s zijn gekoppeld, moet u een overeenkomst ondertekenen met [!DNL ID5] en ontvang de partner-id van uw organisatie. Neem voor instructies contact op met het accountteam van de Adobe.

* Voor metingen in Adobe Analytics moet u:

   1. Alles voltooien [voorwaarden voor de uitvoering [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) en de [AMO-id en EF-id in URL&#39;s voor bijhouden](/help/integrations/analytics/ids.md).

   1. Voeg de volgende parameter toe aan uw webpagina&#39;s voor of binnen de [JavaScript-code vereist voor [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md) — ergens voordat de laatste gebeurtenisservice wordt geïnitialiseerd.

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

## Een aangepast segment maken en implementeren

1. Maak het segment:

   1. Klik in het hoofdmenu op **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Klik boven de gegevenstabel op **[!UICONTROL Create]**.

   1. Voer een unieke waarde in **[!UICONTROL Segment Name]**.

   1. Voor de **[!UICONTROL Segment Type]**, selecteert u *[!UICONTROL Custom]*.

   1. Voer de **[!UICONTROL Lookback Window]** Dit is het aantal dagen dat een cookie van een gebruiker in het segment blijft staan.

      Het standaardvenster is 45 dagen. Voer een waarde tussen 1 en 365 in.

   1. Klikken **[!UICONTROL Advanced]** om de geavanceerde montages uit te breiden, en dan de types van gebruikers herkenningstekens te selecteren die de segmentmarkering volgt:

      * *[!UICONTROL Cookies]:* (De standaardinstelling) De segmenttag houdt cookies bij.

      * [!UICONTROL Universal IDs (Beta)]:

         * *[!UICONTROL ID5]:* De segmenttagtracks [!DNL ID5] ID&#39;s. Er worden geen kosten in rekening gebracht voor afbeeldingen die aan universele id&#39;s worden geleverd.

        **[!UICONTROL Terms of Service]:** De serviceovereenkomst voor het gebruik van universele id&#39;s. Je of een andere gebruiker in de DSP account moet de voorwaarden één keer accepteren voordat je universele id&#39;s voor een nieuw type id kunt gebruiken. Voor klanten met beheerde de dienstcontracten, zal uw Team van de Rekening van de Adobe uw toestemming krijgen en zal de termijnen namens uw organisatie goedkeuren. Als u de voorwaarden wilt lezen, klikt u op **>**. Als u de voorwaarden wilt accepteren, schuift u naar de onderkant van de voorwaarden en klikt u op **[!UICONTROL Accept]**.

   1. Klik op **[!UICONTROL Save]**.

1. Kopieer en implementeer tags om het segment bij te houden, indien nodig:

   1. Terug naar **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Plaats de cursor op de segmentrij en klik op **[!UICONTROL Get Pixel]**.

      * Ga als volgt te werk om bezoekers van het bureaublad en mobiele apparaten bij te houden op een webpagina:

         1. Kopieer de tag voor het bijhouden van de paginaweergave, die is gelabeld als &quot;[!UICONTROL Desktop or mobile websites].&quot;

         1. Geef de tag door aan de adverteerder of websitecontactpersoon voor implementatie.

            De IT-afdeling of andere groep van de adverteerder moet mogelijk de implementatie van de tag plannen of hierover worden geïnformeerd.

      * Om gebruikers te volgen die aan een advertentie-eenheid op Desktop of mobiele apparaten worden blootgesteld:

         1. Kopieer de code voor het bijhouden van de indruk met het label &quot;[!UICONTROL Desktop or mobile ads].&quot;

   1. (Tags voor segmenten die worden bijgehouden [!DNL ID5] ID&#39;s voor desktopbezoekers en mobiele bezoekers van een webpagina) Vervang in de gekopieerde tag `ID5_PARTNER_ID` met partneridentiteitskaart dat [!DNL ID5] toegewezen aan uw organisatie.

   Bijvoorbeeld, als uw ID5 partner identiteitskaart is `abcde` en de gegenereerde segmenttag is

   ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

   vervolgens vervangen `ID5_PARTNER_ID` with `abcde` binnen de tag om het volgende op te halen:

   ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

   Uw organisatie ontving partneridentiteitskaart toen het een overeenkomst met ondertekende [!DNL ID5]. Neem contact op met het accountteam van de Adobe als u uw partner-id niet kent.

   Deze stap is niet nodig voor codes om te volgen [!DNL ID5] Id&#39;s voor gebruikers die worden blootgesteld aan een advertentie-eenheid op mobiele of desktopapparaten.

1. Voeg de tag toe aan de [!UICONTROL Pixel] tabblad voor elke relevante advertentie of voor de [!UICONTROL Event Pixels] van de [[!UICONTROL Tracking] instellingen voor elke relevante plaatsing](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

Zodra een volgende markering wordt uitgevoerd, kunt u het segment in de publieksdoelstellingen of uitsluitingen voor om het even welke plaatsing gebruiken.

>[!TIP]
>
>Houd de segmentgrootte bij terwijl gebruikers worden bijgehouden.

>[!MORELIKETHIS]
>
>* [Informatie over Audience Management](audience-about.md)
>* [Segmentinformatie bewerken](segment-edit.md)
>* [Een segment verwijderen](segment-delete.md)
>* [Trackingpixels voor een segment weergeven](segment-view-pixels.md)
>* [Een segment delen of delen stoppen](segment-share.md)
>* [Een [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Een herbruikbaar publiek maken](reusable-audience-create.md)
>* [Beschikbare gegevensleveranciers van derden](third-party-data-providers.md)
>* [Plaatsingsinstellingen](/help/dsp/campaign-management/placements/placement-settings.md)
