---
title: Waarschuwingen weergeven
description: Leer hoe u waarschuwingen en aanbevolen resoluties voor uw campagnes en campagnecomponenten kunt weergeven.
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
source-git-commit: 70592355207ba43341eb208750dcd3fc00db51c1
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---

# Waarschuwingen weergeven

*Beta, functie*

DSP helpt u te identificeren wanneer om het even welk van uw campagnes of campagnecomponenten kwesties hebben. DSP maakt voor elk probleem een waarschuwing met een tijdstempel en de aanbevolen actie om het probleem op te lossen. De redenen voor alarm omvatten configuratiekwesties (bijvoorbeeld, wanneer geen advertenties aan een plaatsing worden vastgemaakt of wanneer een overeenkomst verkeerd wordt geplaatst), afwijzing, en de kwesties van de campagnegezondheid (zoals slechte levering of prestaties). De alarm zijn beschikbaar op de campagne, het pakket, de plaatsing, en overeenkomstenniveaus.

Waarschuwingen zijn beschikbaar op de volgende locaties:

* A [!UICONTROL Pulse Panel] in het deelvenster [!UICONTROL Campaigns], [!UICONTROL Packages] en verpakkingsgegevens, [!UICONTROL Placements], en [!UICONTROL Ads] weergaven geven of er waarschuwingen beschikbaar zijn voor de items in die weergave. Wanneer het pictogram een blauwe stip heeft (![Pictogram van deelvenster Start wanneer waarschuwingen beschikbaar zijn](/help/dsp/assets/alerts-panel.png "Pictogram van deelvenster Start wanneer waarschuwingen beschikbaar zijn")), zijn waarschuwingen beschikbaar. Wanneer geen punt zichtbaar is (![Pictogram van deelvenster Start wanneer er geen waarschuwingen beschikbaar zijn](/help/dsp/assets/alerts-panel-empty.png "Pictogram van deelvenster Start wanneer er geen waarschuwingen beschikbaar zijn")), zijn er geen waarschuwingen beschikbaar.

* De gegevenstabellen in dezelfde weergaven bevatten een &quot;[!UICONTROL Alerts]&quot; kolom die aangeeft wanneer het item — of de componenten ervan — een uitgave heeft. Waarschuwing-indicatoren omvatten &quot;Kritiek&quot; (![Kritiek](/help/dsp/assets/indicator-critical.png "Kritiek")), &quot;Waarschuwing&quot; (![Waarschuwing](/help/dsp/assets/indicator-warning.png "Waarschuwing")), en &quot;Informatie&quot; (![Informatie](/help/dsp/assets/indicator-information.png "Informatie")).

U kunt de relevante campagnebeheerweergave openen voor elke waarschuwing, zodat u de instellingen naar wens kunt bewerken om het probleem op te lossen.

U kunt er ook voor kiezen een afzonderlijke waarschuwing te negeren, zodat deze uit het dialoogvenster [!UICONTROL Pulse] deelvenster.

Waarschuwings- en waarschuwingsindicatoren verdwijnen automatisch wanneer de onderliggende problemen worden opgelost.

## Waarschuwingen weergeven in het dialoogvenster [!UICONTROL Pulse Panel]

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]**.

1. Voer een van de volgende handelingen uit:

   * (Voor alle waarschuwingen die van toepassing zijn voor de weergave) Klik rechts van de werkbalk in een campagnebeheerweergave op ![Pictogram van deelvenster Start wanneer waarschuwingen beschikbaar zijn](/help/dsp/assets/alerts-panel.png "Pictogram van deelvenster Start wanneer waarschuwingen beschikbaar zijn").

   * (Voor alle waarschuwingen voor een specifieke campagne) Klik op de waarschuwingsindicator voor een campagnerij en klik vervolgens op **[!UICONTROL View in Pulse panel]**.

   * (Voor alle waarschuwingen voor een specifiek pakket, een specifieke plaatsing of een specifieke advertentie) Ga als volgt te werk:

      1. Klik op de naam van de campagne.

      1. Klik in het submenu op **[!UICONTROL Packages]**, **[!UICONTROL Placements]**, of **[!UICONTROL Ads]** de desbetreffende weergave van de campagnecomponent openen.

      1. Klik op de waarschuwingsindicator voor een pakket, plaatsing of advertentierij en klik vervolgens op **[!UICONTROL View in Pulse Panel]**.

   Alle waarschuwingen met betrekking tot de campagne en de onderdelen ervan, inclusief gerichte aanbiedingen, worden vermeld. Standaard worden essentiële waarschuwingen als eerste vermeld.

1. (Optioneel) Als u de waarschuwingen wilt groeperen op basis van de eerste detectiedatum of als u de waarschuwingen wilt filteren op basis van de waarschuwingsstatus, de status van het onderdeel, het type onderdeel of een specifieke campagnenaam, klikt u op ![De knop Filter](/help/dsp/assets/filter.png) in de rechterbovenhoek van het deelvenster selecteert u de filteropties en klikt u vervolgens op **[!UICONTROL Apply]**.

1. Als u een lijst wilt weergeven met alle betrokken campagnecomponenten voor een specifiek type waarschuwing, klikt u op de naam van de waarschuwing, bijvoorbeeld &quot;[!UICONTROL Package: No Active Placement (*N*)]&quot;. Klik op [!UICONTROL EXPAND ALL] of klik op de naam van de component. Om de relevante mening van het campagnebeheer voor om het even welke beïnvloede component te openen zodat kunt u de geadviseerde veranderingen aanbrengen, houd de curseur over de componentennaam en klik ![Ga naar weergave](/help/dsp/assets/go-to-view.png "Ga naar weergave").

1. (Optioneel) Als u een waarschuwing wilt negeren (verbergen), houdt u de cursor boven de componentnaam en klikt u op ![Negeren](/help/dsp/assets/alert-ignore.png "Negeren")en klik vervolgens op **[!UICONTROL Ignore indefinitely]**.  <!-- **[!UICONTROL Ignore alert for three days]**, **[!UICONTROL Ignore alert until next check]**, or **[!UICONTROL Ignore indefinitely] -->

U hebt een paar seconden nadat u een waarschuwing hebt genegeerd om de handeling ongedaan te maken. Nadat het optiemelding is gesloten, kunt u de handeling niet annuleren.

1. (Optioneel) Als u genegeerde waarschuwingen wilt ophalen, filtert u de waarschuwingen om een [!UICONTROL Alert Status] van &quot;[!UICONTROL All]&quot; of &quot;[!UICONTROL Ignored].&quot; Als u een waarschuwing wilt negeren, houdt u de cursor boven de componentnaam en klikt u op ![Negeren ongedaan maken](/help/dsp/assets/alert-un-ignore.png "Negeren ongedaan maken").

## Sluit het dialoogvenster [!UICONTROL Pulse Panel]

* Klik rechts van de werkbalk op ![Pictogram van deelvenster Start wanneer waarschuwingen beschikbaar zijn](/help/dsp/assets/alerts-panel.png "Pictogram van deelvenster Start wanneer waarschuwingen beschikbaar zijn") of ![Pictogram van deelvenster Start wanneer er geen waarschuwingen beschikbaar zijn](/help/dsp/assets/alerts-panel-empty.png "Pictogram van deelvenster Start wanneer er geen waarschuwingen beschikbaar zijn").

>[!MORELIKETHIS]
>
>* [Typen prestatierapporten in Campaign Management-weergaven](campaign-reports-about.md)
