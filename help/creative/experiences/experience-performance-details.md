---
title: Prestatierapporten op ervaringsniveau
description: Leer hoe u prestatierapporten op ervaringsniveau kunt weergeven.
feature: Creative Experiences
exl-id: 5e7c4c9d-b992-460a-9765-4276027f9a61
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---

# Prestatierapporten op ervaringsniveau

*Gesloten bèta*

U kunt gedetailleerde prestatiegegevens voor elke ervaring bekijken.

## Gegevens in prestatierapporten op ervaringsniveau

De rapportweergave bevat de volgende gegevens:

* **Overzicht** tabel: Een prestatiesoverzicht voor de volledige ervaring, die omvat:

   * **Algemene Prestaties** sectie:

   * **Algemene Prestaties**: De totale indrukkingen; klikt; klik-door tarief (CTR); en mening-door omzettingen en klik-door omzettingen voor één enkele metrische omzetting. <!-- Just one, or can you select multiple? And I don't see this as of 2/8:  You can optionally combine two metrics at a time into a single chart. -->

     <!--
     ![Overall performance](/help/creative/assets/experience-report-overall-performance.png "Overall performance"){width="100" zoomable="yes"}
          -->

   * **Gebrek Tarief**: (Ervaringen met beslissingsboom richtend slechts) het aantal indrukkingen die uit gerichte creatieven, generische creatieven zonder een doel of gericht aan &quot;Alle Else&quot;voortvloeien, en het gebrek creatief voor de ervaring.

     <!--
     ![Default rate](/help/creative/assets/experience-report-default-rate.png "Default rate"){width="100" zoomable="yes"} 
     -->

   * **sectie van de Onderbreking van 0} Prestaties {:**

      * **Regionale prestaties:*: individuele meetgegevens per geografische locatie.

        <!-- You can optionally do the following:
    
      * Click a metric name (such as [!UICONTROL Impressions]) to view that metric.

      * Select the region in the **[!UICONTROL Region]** menu.
      
      -->

        <!--   
      ![Regional performance](/help/creative/assets/experience-report-regional-performance.png "Regional performance"){width="100" zoomable="yes"}
      -->

      * **Prestaties van het Apparaat:** Individuele metriek door apparatentype, werkend systeem, en browser. Klik optioneel op de waarde voor een apparaatcategorie om een lijst weer te geven met de bovenste creatieve functies van <!-- NN --> die aan deze criteria voldoen.

        <!--    
      ![Device performance](/help/creative/assets/experience-report-device-performance.png "Device performance"){width="100" zoomable="yes"}
      -->

* **Creatieve Prestaties** tab*: Een prestatiesoverzicht door creatieve en bundel of ad markering, die omvatten:

   * **Creatieven** sub-tab: Het totale aantal beelden, klikt, en CTR voor elk creatief in de ervaring.<!-- No breakdown yet for the individual ad elements and/or the served ads. -->

     <!--

     * *Experiences with decision tree targeting:* The total number of impressions, clicks, and CTR for each creative. You can optionally do the following:
     
       * To break out the performance for each ad target, enable **[!UICONTROL Split targeting]**.

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report. [Find out about this:  ..., and total conversions for specified conversion metricsYour conversion metrics are combined into one Conversions column set unless you have made individual metric column sets available within Advertising Cloud Search.]

     * *Experiences without decision tree targeting:* The total number of impressions, clicks, and click-through rate (CTR) for each creative. You can optionally do the following:

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     -->

   * **bundels/tags** sub-tab: Het totale aantal beelden, klikken, en CTR voor individuele bundels (ervaringen met beslissingsboom richtend) of ad markeringen (ervaringen zonder beslissingsboom richtend) in de ervaring.

     <!--
   
     * *Experiences with decision tree targeting:* The total number of impressions, clicks, and CTR for each bundle. You can optionally do the following:
     
       * To break out the performance for each ad target, enable **[!UICONTROL Split targeting]**.

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions  and click-through conversions (using on the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     * *Experiences without decision tree targeting:* The total number of impressions, clicks, and click-through rate (CTR) for each ad tag. You can optionally do the following:

       * To switch between the grid view and a trend chart, which includes the addition of view-through conversions and click-through conversions (using the conversions specified in the top toolbar), click ![Chart](/help/creative/assets/chart-view-button.png "Chart") and ![Grid](/help/creative/assets/table-view-button.png "Grid") above the report.

     -->

## Prestatierapporten weergeven voor een ervaring

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Experiences]** .

1. (Facultatief) [ pas de mening ](/help/creative/introduction/customize-data-views.md) aan om specifieke ervaringen te omvatten.

1. Selecteer de ervaring:

   * Klik in de kaartweergave op **[!UICONTROL ...]** naast de naam van de ervaring en klik vervolgens op **[!UICONTROL Reports]** .

   * Houd in de tabelweergave de cursor boven de rij en klik op **[!UICONTROL Reports]** .

   Het tabblad [!UICONTROL Overview] wordt geopend.

1. (Optioneel) Geef op de werkbalk rechtsboven het datumbereik, de toewijzingsregel voor conversie en conversies op die in alle prestatierapporten worden gerapporteerd:

   * (Optioneel) Als u het datumbereik voor de prestatiegegevens wilt wijzigen, kiest u een optie in het datummenu:

      * Om een vooraf ingestelde periode te specificeren, selecteer het rapport: (*[!UICONTROL Last Month-to-date],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Last 7 days],* *[!UICONTROL Last 30 days],* *[!UICONTROL Today],* of *[!UICONTROL Yesterday]*.

      * Om een waaier van de douanedatum te specificeren, specificeer de begindatum en einddatum <!-- in the format MM/DD/YYYY or M/D/YYYY,--> of klik ![ kalenderpictogram ](/help/search-social-commerce/assets/calendar.png) naast een gebied en selecteer een datum.

   * (Facultatief) om de regel te veranderen die wordt gebruikt om omzettingsgegevens in een reeks gebeurtenissen te kenmerken die tot een omzetting leiden, ![ Montages ](/help/creative/assets/settings.png) klikken en **[!UICONTROL Attribution Rule]** veranderen.

   * (Facultatief) om de gemelde omzettingen te veranderen, klik ![ Montages ](/help/creative/assets/settings.png) en selecteer de omzettingsnamen in het **[!UICONTROL Conversions]** menu.&lt;!— Alleen één of meerdere? Controleren hoe deze worden weergegeven — Ik moet een adverteerder zien die al meerdere omzettingen heeft uitgevoerd —>

     De beschikbare conversiekolommen bevatten de conversies die beschikbaar zijn in Advertising Search, Social en Commerce, of u nu een klant voor Zoeken, Sociaal en Commerce bent of niet. Dit kan omzetting en de metriek van de plaatsovereenkomst omvatten die van Adobe Analytics wordt gesynchroniseerd wanneer adverteerder [  [!DNL Adobe Analytics for Advertising]  integratie ](/help/integrations/analytics/overview.md) heeft. <!--Analytics calculated metrics and advanced calculated metrics aren't available.--> voor meer informatie over het omvatten van verzamelde omzettingen in rapporten, zie het Onderzoek, Sociale, &amp; het onderwerp van de Gids van Commerce &quot;[ Ongeveer het leiden van de omzettingsmetriek van een adverteerder ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md).&quot;

1. (Op het tabblad [!UICONTROL Overview] ):

   * (Optioneel) Houd de cursor in de sectie [!UICONTROL Overall Regional Performance] boven een punt in het diagram om gegevens voor dat punt weer te geven.

   * (Optioneel) Voer in de sectie [!UICONTROL Regional Performance] een van de volgende handelingen uit:

      * Klik op een metrische naam (bijvoorbeeld [!UICONTROL Impressions] ) om die metrische naam weer te geven.

      * Selecteer het gebied in het menu [!UICONTROL Region] .

      * Houd de cursor boven een land of staat om gegevens voor dat gebied weer te geven.

   * (Optioneel) Voer in de sectie [!UICONTROL Device Performance] een van de volgende handelingen uit:

      * Houd de curseur over waarde voor om het even welke apparatencategorie om gegevens voor die criteria te zien.

      * Klik op de waarde voor een apparaatcategorie om een lijst weer te geven met de bovenste creatieve functies van <!-- NN--> die aan deze criteria voldoen.

1. (Optioneel) Als u gegevens op creatieve basis en op bundel- of advertentietag wilt weergeven, klikt u op de tab **[!UICONTROL Creative Performance]** .

   * Op de subtab [!UICONTROL Creatives] kunt u het volgende doen:

      * (Facultatief) om tussen grafiekmening en netmening te schakelen, klik ](/help/creative/assets/chart-view-button.png " Grafiek ") en ![Raster](/help/creative/assets/table-view-button.png "Raster"), respectievelijk.![

      * (Optioneel) Houd de cursor in de grafiekweergave boven een punt in het diagram om gegevens voor dat punt weer te geven.

      * (Ervaringen met alleen beslissingsboomstructuurdoelframes; optioneel) Schakel **[!UICONTROL Split targeting]** in om de prestaties voor elk toegepast ad-hocdoel te verdelen.

1. Als u gegevens wilt weergeven op bundel (ervaring met doelstructuurbeleid) of op ad-tag (ervaring zonder doelstructuurtoewijzing), klikt u op het subtabblad **[!UICONTROL Bundles]** . U kunt een van de volgende handelingen uitvoeren:

   * (Facultatief) om tussen grafiekmening en netmening te schakelen, klik ](/help/creative/assets/chart-view-button.png " Grafiek ") en ![Raster](/help/creative/assets/table-view-button.png "Raster"), respectievelijk.![

   * (Optioneel) Houd de cursor in de grafiekweergave boven een punt in het diagram om gegevens voor dat punt weer te geven.

   * (Ervaringen met alleen beslissingsboomstructuurdoelframes; optioneel) Schakel **[!UICONTROL Split targeting]** in om de prestaties voor elk toegepast ad-hocdoel te verdelen.

1. (Facultatief) om de gegevens in a [!DNL Microsoft Excel] dossier in spreadsheet (XLSX) formaat te downloaden, klik ![ Download ](/help/creative/assets/download.png " Download ") in de toolbar.

   Het bestand wordt gedownload volgens de normale procedure van uw browser.

>[!MORELIKETHIS]
>
>* [ Aangepast Creatief Rapport ](/help/creative/report-custom-creative.md)
