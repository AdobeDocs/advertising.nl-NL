---
title: Een plaatsing maken
description: Leer hoe u een plaatsing maakt.
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
source-git-commit: 0afe1d9985c1451c28943aaa17c7d6f8a73a95ef
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 0%

---

# Een plaatsing maken

>[!TIP]
>
>Plaatsen maken op basis van specifieke campagnedoelen of rapportagebehoeften.

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Klik op de naam van de campagne waarin u de plaatsing wilt opnemen.

1. Klik boven de gegevenstabel op **[!UICONTROL Create]** . Klik in de sectie [!UICONTROL Placement Types] van het menu op het plaatsingstype.

   Het plaatsingstype bepaalt het advertentietype dat de plaatsing kan omvatten.

1. Ga de [ plaatsingsmontages ](placement-settings.md) in:

   1. Geef de [!UICONTROL Placement Basics] -instellingen op.

   1. Geef in de sectie [!UICONTROL Goals] de waarde [!UICONTROL Gross Budget] op en geef desgewenst aanvullende doelen voor plaatsing op.

      Sommige velden hebben standaardwaarden die u kunt overschrijven.

      Als het pakket waaraan de plaatsing wordt toegewezen pakketniveau het verpakken heeft, dan weerspiegelen uw doelstellingen en het verpakken montages de pakketmontages.

   1. (Optioneel) Verklein in de sectie [!UICONTROL Geo-Targeting] de locaties die zijn opgenomen of uitgesloten.

      Als u geen specifieke plaatsen identificeert, worden alle plaatsen gericht.

      >[!NOTE]
      >
      >De plaatsen van de Stad en DMA zijn niet beschikbaar voor Plaatsen Roku.

   1. Verklein in de sectie [!UICONTROL Inventory Targeting] de inventarisbronnen die u wilt opnemen of uitsluiten.

      Voor de meeste plaatsingstypen worden alle voorraadtypen en alle bronnen voor elk type standaard opgenomen. Voor [!DNL Roku] plaatsingen, moet u het inventaristype en de bronnen specificeren.

   1. (Optioneel) Verklein in de sectie [!UICONTROL Site Targeting] de sites waarop u wilt verwijzen en geef de sites op die u wilt uitsluiten.

   1. (Optioneel) In de sectie [!UICONTROL Audience Targeting] :

      1. Versmal het publiek. Dit omvat het selecteren van publiekssegmenten om binnen de plaatsing te richten.

         Voor [!DNL Roku] plaatsen, kunt u hefboomwerking {het unieke publiek van 1} DSP aanpassen met [ door één of meerdere publiekssegmenten te omvatten die tegen  [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) (opted-in) deterministische dataset kunnen worden aangepast.[!DNL Roku]

         De segmenten van eerste-partij RampID die niet aan een actieve, geplande, of gepauzeerde plaatsing in bijlage zijn worden gepauzeerd. Het segment wordt in de segmentlijst genoteerd als &quot;Automatisch gepauzeerd&quot;.

      1. (Voor campagnes met personen-vlakke dwars-apparaat het richten; facultatief) Wanneer de plaatsing één of meerdere specifieke doelgroepen richt, laat op mensen-gebaseerde cross-device het richten voor de plaatsing toe.

         Op mensen gebaseerde cross-device gerichte toepassingen worden alleen verschaft door [!DNL LiveRamp] met Amerikaanse gegevens. De service is beschikbaar voor alle adverteerders op $0,35 CPM voor indrukken die worden geleverd met de apparaatgrafiek van [!DNL LiveRamp] (dat wil zeggen voor apparaten die niet in de doelpubliekssegmenten worden gevonden).

   1. (Optioneel) Pas in de sectie [!DNL Brand Safety and Media Targeting] de merkveiligheidsbeperkingen toe op uw plaatsen.

   1. (Optioneel) Geef in de sectie [!DNL Tracking] gebeurtenispixels van derden of conversiepixels op voor advertenties in de plaatsing.

      >[!NOTE]
      >
      >([!DNL Roku] placements) Pixelleveranciers van derden die zijn goedgekeurd door [!DNL Roku] include [!DNL Acxiom] , [!DNL Comscore], [!DNL Data Plus Math] , [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] en [!DNL Research Now] .

1. Klik op **[!UICONTROL Create Placement]**.

1. (Optioneel) Advertenties aan de plaatsing koppelen:

   1. Klik op **[!UICONTROL Attach an ad]**.

   1. Voer een van de volgende handelingen uit:

      * Een nieuwe advertentie maken:

         1. Klik op **[!UICONTROL Create a New Ad].**

         1. Specificeer de advertentiemontages voor [ audioadvertenties ](/help/dsp/campaign-management/ads/ad-settings-audio.md), [ verbonden TV ](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [ vertoningsadvertenties ](/help/dsp/campaign-management/ads/ad-settings-display.md), [ mobiele advertenties ](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [ inheemse advertenties ](/help/dsp/campaign-management/ads/ad-settings-native.md), [ pre-rol advertenties ](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md), of [ universele videoadvertenties ](/help/dsp/campaign-management/ads/ad-settings-universal-video.md).

        >[!NOTE]
        >
        >Universal video placements can contain only Universal video ads.

         1. Klik op **[!UICONTROL Save & Submit for Review]**.

         1. (Optioneel) Klik voor elke aanvullende advertentie die u voor de plaatsing wilt maken op **[!UICONTROL Attach Another Ad]** en herhaal vervolgens stap 1-3.

         1. Als u geen bestaande advertenties wilt koppelen, klikt u op **[!UICONTROL I'm done for now]** .

      * Bestaande advertenties toevoegen aan de campagne:

      1. Klik op **[!UICONTROL Select an Ad]**.

      1. Voer een van de volgende handelingen uit:

         * Eén advertentie tegelijk toevoegen:

            1. Klik naast de naam van de advertentie op **[!UICONTROL Select].**

            1. (Optioneel) Klik voor elke aanvullende advertentie die u wilt bijvoegen op **[!UICONTROL Attach Another Ad]** en herhaal het proces.

         * U kunt maximaal 20 advertenties tegelijk toevoegen:

            1. Schakel het selectievakje boven de advertentielijst in.

            1. Schakel het selectievakje naast elke advertentie in die u wilt toevoegen.

            1. Klik op **[!UICONTROL Attach]**.

            1. Klik op **[!UICONTROL Select]** naast de naam van de advertentie.

      1. (Optioneel) De standaardvliegperiode en de ad-rotatie overschrijven voor specifieke advertenties in de plaatsing:

         1. Klik op **[!UICONTROL Custom Schedule Ads]**.

         1. Voer een van de volgende handelingen uit:

            * Als u een vlucht wilt toevoegen, klikt u op **[!UICONTROL Add Flight]** en geeft u vervolgens de begin- en einddatum op.

            * Als u een bestaande vlucht aan een advertentie wilt toevoegen, klikt u op **[!UICONTROL +]** in de rij met toevoegingen voor de vluchtkolom.

            * Als u een bestaande vlucht uit een advertentie wilt verwijderen, klikt u op **[!UICONTROL x]** in de rij met toevoegingen voor de vluchtkolom.

            * (Als meerdere advertenties dezelfde vlucht hebben) Als u de advertenties ongelijk wilt roteren, klikt u op **[!UICONTROL Even Rotation]** in de vluchtinformatie en voert u vervolgens het relatieve gewicht in waarmee u elke advertentie wilt roteren, als een percentage.

              Het totale gewicht moet 100 zijn.

         1. Klik in de rechterbovenhoek op **[!UICONTROL Continue]** .

         1. Controleer de vlieggegevens en klik op **[!UICONTROL Save & Finish]** .

>[!MORELIKETHIS]
>
>* [ Ongeveer het Beheer van de Plaatsing ](placement-about.md)
>* [ geeft Plaatsen ](placement-edit.md) uit
>* [ beheert Bodmultipliers voor Plaatsingen ](placement-manage-bid-multipliers.md)
>* [ geef de Advertentieschema&#39;s voor Plaatsen uit ](placement-edit-ad-schedule.md)
>* [ Pauze of activeer een Plaatsing ](placement-pause-activate.md)
>* [ Mening het Logboek van de Verandering voor een Plaatsing ](placement-change-log.md)
>* [ Montages van de Plaatsing ](placement-settings.md)
>* [ Mening het Voorspelde Rapport van de Plaatsing ](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [ Veelgestelde vragen over Universele Video ](/help/dsp/campaign-management/faq-universal-video.md)
>* [ Sneltoetsen ](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [ Prestaties van het oplossen van problemen ](/help/dsp/optimization/troubleshooting-performance.md)
>* [ Video: Hoe te om een StandaardPlaatsing van de Vertoning te creëren ](https://video.tv.adobe.com/v/340454)
