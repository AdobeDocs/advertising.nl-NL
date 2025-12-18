---
title: Waarschuwingen weergeven
description: Leer hoe u waarschuwingen en aanbevolen resoluties voor uw campagnes en campagnecomponenten kunt weergeven.
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
exl-id: 667bf1c3-3bad-4a1a-b907-0c9bfe5362a9
source-git-commit: 9ab8d3345659f48d1d131c3c6c1e1b87f0b0a0e6
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# Waarschuwingen weergeven

DSP helpt u te identificeren wanneer een van uw campagnes of campagnecomponenten problemen heeft. DSP maakt voor elk probleem een waarschuwing met een tijdstempel en de aanbevolen actie om het probleem op te lossen. De redenen voor alarm omvatten configuratiekwesties (bijvoorbeeld, wanneer geen advertenties aan een plaatsing worden vastgemaakt of wanneer een overeenkomst verkeerd wordt geplaatst), afwijzing, en de kwesties van de campagnegezondheid (zoals slechte levering of prestaties). De alarm zijn beschikbaar op de campagne, het pakket, de plaatsing, en overeenkomstenniveaus.

Waarschuwingen zijn beschikbaar op de volgende locaties:

* Een [!UICONTROL Pulse Panel] -pictogram in de weergaven [!UICONTROL Campaigns] , [!UICONTROL Packages] en Pakketdetails [!UICONTROL Placements] en [!UICONTROL Ads] geeft aan of er waarschuwingen beschikbaar zijn voor de items in die weergave. Wanneer het pictogram een blauwe punt heeft (![ pictogram van het Comité van de Puls wanneer het alarm ](/help/dsp/assets/alerts-panel.png " pictogram van het Comité van de Puls beschikbaar is wanneer het alarm ") beschikbaar is), zijn het alarm beschikbaar. Wanneer geen punt zichtbaar is (![Pictogram van deelvenster Start wanneer er geen waarschuwingen beschikbaar zijn](/help/dsp/assets/alerts-panel-empty.png "Pictogram van deelvenster Start wanneer er geen waarschuwingen beschikbaar zijn")), zijn geen alarm beschikbaar.

* De gegevenstabellen in de zelfde meningen omvatten &quot;[!UICONTROL Alerts]&quot;kolom die erop wijst wanneer het punt — of zijn componenten — een kwestie heeft. De alarm indicatoren omvatten &quot;Kritieke&quot;(![ Kritieke ](/help/dsp/assets/indicator-critical.png " Kritieke ")), &quot;Waarschuwing&quot; (![Waarschuwing](/help/dsp/assets/indicator-warning.png "Waarschuwing")), en &quot;Informatie&quot; (![ Informatie ](/help/dsp/assets/indicator-information.png " Informatie ")).

U kunt de relevante campagnebeheerweergave openen voor elke waarschuwing, zodat u de instellingen naar wens kunt bewerken om het probleem op te lossen.

U kunt ook een afzonderlijke waarschuwing negeren, die deze uit het deelvenster [!UICONTROL Pulse] verwijdert.

Waarschuwings- en waarschuwingsindicatoren verdwijnen automatisch wanneer de onderliggende problemen worden opgelost.

## Waarschuwingen weergeven in het dialoogvenster [!UICONTROL Pulse Panel]

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]** .

1. Voer een van de volgende handelingen uit:

   * (Voor alle alarm van toepassing op de mening) rechts van de toolbar in om het even welke mening van het campagnebeheer, klik {het pictogram van het Comité van de Pulse van 0} wanneer het alarm ![ het pictogram van het Comité van de Pulse beschikbaar is wanneer het alarm ](/help/dsp/assets/alerts-panel.png " beschikbaar is.")

   * (Voor alle alarm voor een specifieke campagne) klik de waakzame indicator voor een campagnerij, en klik dan **[!UICONTROL View in Pulse panel]**.

   * (Voor alle waarschuwingen voor een specifiek pakket, een specifieke plaatsing of een specifieke advertentie) Ga als volgt te werk:

      1. Klik op de naam van de campagne.

      1. Klik in het submenu op **[!UICONTROL Packages]** , **[!UICONTROL Placements]** of **[!UICONTROL Ads]** om de desbetreffende weergave van de campagnecomponent te openen.

      1. Klik op de waarschuwingsindicator voor een pakket, plaatsing of advertentierij en klik vervolgens op **[!UICONTROL View in Pulse Panel]** .

   Alle waarschuwingen met betrekking tot de campagne en de onderdelen ervan, inclusief gerichte aanbiedingen, worden vermeld. Standaard worden essentiële waarschuwingen als eerste vermeld.

1. (Adverteerders met Advertising Creative; optioneel) Klik op het tabblad **[!UICONTROL Creative]** om waarschuwingen voor plaatsen met ervaringen met Advertising Creative weer te geven.

1. (Facultatief) om het alarm volgens hun eerste datum van opsporing te groeperen, of het alarm door waakzame status, componentenstatus, componententype, of met een specifieke campagnenaam te filtreren, klik ![ knoop van de Filter ](/help/dsp/assets/filter.png) in het hogere recht van het paneel, selecteer de filteropties, en klik dan **[!UICONTROL Apply]**.

1. Om een lijst van alle beïnvloede campagnecomponenten voor een specifiek waakzaam type te bekijken, klik de waakzame naam, zoals &quot;[!UICONTROL Package: No Active Placement (*N*) ]&quot;. Klik op [!UICONTROL EXPAND ALL] of klik op de naam van de component om de details van elke desbetreffende component, inclusief de aanbevolen handeling, weer te geven. Om de relevante mening van het campagnebeheer voor om het even welke beïnvloede component te openen zodat kunt u de geadviseerde veranderingen aanbrengen, de curseur over de componentennaam houden en ![ klikken gaat ](/help/dsp/assets/go-to-view.png " aan mening ").

1. (Facultatief) om een alarm te negeren (te verbergen), de curseur over de componentennaam te houden en ![ te klikken negeert ](/help/dsp/assets/alert-ignore.png " "), en dan **[!UICONTROL Ignore alert till next check]**, **[!UICONTROL Ignore alert for 3 days]**, of **[!UICONTROL Ignore indefinitely]** te klikken.

U hebt een paar seconden nadat u een waarschuwing hebt genegeerd om de handeling ongedaan te maken. Nadat het optiemelding is gesloten, kunt u de handeling niet annuleren.

1. (Facultatief) om genegeerde alarm terug te winnen, filter de alarm om [!UICONTROL Alert Status] van &quot;[!UICONTROL All]&quot;of &quot;[!UICONTROL Ignored] te tonen.&quot; Om een alarm ongedaan te maken, houd de curseur over de componentennaam en klik ![ niet-negeert ](/help/dsp/assets/alert-un-ignore.png " ").

## Sluit het dialoogvenster [!UICONTROL Pulse Panel]

* Aan het recht van de toolbar, klik ![ pictogram van het Comité van de Puls wanneer het alarm ](/help/dsp/assets/alerts-panel.png " pictogram van het Comité van de Puls beschikbaar is wanneer het alarm ") of ![Pictogram van deelvenster Start wanneer er geen waarschuwingen beschikbaar zijn](/help/dsp/assets/alerts-panel-empty.png "Pictogram van deelvenster Start wanneer er geen waarschuwingen beschikbaar zijn") beschikbaar is.

>[!MORELIKETHIS]
>
>* [ Types van Rapporten van Prestaties in de Meningen van het Beheer van de Campagne ](campaign-reports-about.md)
