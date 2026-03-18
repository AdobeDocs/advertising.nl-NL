---
title: Apparaatoplossingen
description: Meer informatie over functies voor verschillende apparaten.
feature: DSP Introduction
exl-id: d21917ef-5cac-46f8-8222-099667797683
source-git-commit: 21ed5558a39ea9b097be8e70ef81bcf8e59c14b4
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Apparaatoplossingen

Dankzij de Advertising DSP-integratie met [!DNL LiveRamp] kunt u uw publiek uitbreiden naar alle bekende apparaten van een persoon, en niet alleen naar de apparaten die uw merk heeft bijgehouden. De integratie biedt ook frequentiecapping en attributie-meting voor alle apparaten.

Wanneer u een ondersteunde apparaatgrafiek gebruikt, kunt u:

* Stem het publiek af via kanalen en apparaten om advertenties te leveren aan mensen en huishoudens in plaats van aan apparaten.
* Balans en blootstelling door inzicht te krijgen in de frequentie van de begrenzing van personen.
* Teststrategieën die publiek toegankelijk maken ten opzichte van publiek converteren naar kanalen of apparaten.

## Voordelen van de apparaatgrafiek van [!DNL LiveRamp]

* Verstrekt een deterministische gegevenspool, met inbegrip van off-line klantengegevens

* Biedt een gelijkmatige dekking tussen cookie-id&#39;s en mobiele apparaat-id&#39;s

* Inclusief gegevens voornamelijk uit de Verenigde Staten

* Is gratis voor frequentiecalfakanalen en attribuutmetingen

* Gratis naar $0,35 CPM voor uitgebreide indrukken (indrukkingen die alleen worden geleverd met de apparaatgrafiek van [!DNL LiveRamp] in plaats van op apparaten die worden gevonden binnen de doelpubliekssegmenten)

  De snelheid wordt weergegeven op je creditcard met accountsnelheden.

## Frequentiebeheer op basis van personen

Met op personen gebaseerd frequentiebeheer kunt u frequentiecappen op persoonlijk niveau in plaats van op apparaatniveau opgeven voor een werkelijke controle van de mediablootstelling.

### Frequentiebeheer op basis van personen activeren

* **Campagnes:** wanneer u een nieuwe campagne creeert, kunt u a [!UICONTROL Cross-Device Level] het plaatsen specificeren. Schakel &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People]&quot; in en selecteer een apparaatgrafiek. De gespecificeerde apparatengrafiek wordt gebruikt voor zowel dwars-apparaat richtend op het plaatsingsniveau als voor op mensen-gebaseerd frequentiebeheer op de campagne, het pakket, en plaatsingsniveau. De frequentiecaps zijn van toepassing op alle bekende apparaten van een persoon.

Voor meer informatie, zie [&#x200B; Montages van de Campagne &#x200B;](/help/dsp/campaign-management/campaigns/campaign-settings.md).

Wanneer u een campagne hebt opgeslagen, kunt u de instelling voor [!UICONTROL Cross Device Level] niet meer wijzigen.

* **Pakketten:** u kunt naar keuze extra frequentiecappen op het pakketniveau plaatsen. DSP respecteert de strengste frequentiegrens in de campagnehiërarchie.

* **Plaatsen:** u kunt naar keuze extra frequentiecappen op het plaatsingsniveau plaatsen. DSP respecteert de strengste frequentiegrens in de campagnehiërarchie.

## Doelstelling voor mensen

Door op mensen gebaseerde doelgroepen te kiezen, kunt u klanten zoeken op verschillende desktops en mobiele apparaten.

### Activeren op basis van personen

* **Campagnes:** wanneer u een nieuwe campagne creeert, kunt u a [!UICONTROL Cross-Device Level] het plaatsen specificeren. Schakel &quot;[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People]&quot; in en selecteer een apparaatgrafiek. De gespecificeerde apparatengrafiek wordt gebruikt voor zowel dwars-apparaat richtend op het plaatsingsniveau als voor op mensen-gebaseerd frequentiebeheer.

Voor meer informatie, zie [&#x200B; Montages van de Campagne &#x200B;](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **Plaatsen:** wanneer u publieksdoelstellingen voor een plaatsing in een campagne met een gespecificeerde apparatengrafiek selecteert, staat een [!UICONTROL Cross-Device Targeting] optie u toe om uw het richten over alle bekende apparaten van een persoon (per de apparatengrafiek uit te breiden die in de campagnemontages wordt gespecificeerd), zelfs apparaten die niet in de gespecificeerde segmenten zijn.

### Rapportage instellen voor op mensen gebaseerde doelwitten

U kunt de volgende metriek in douanerapporten omvatten:

* **Uitgebreide Beelden:** (in de [!UICONTROL Build Your Report] sectie onder [!UICONTROL Metrics] > [!UICONTROL Std. Metrics]) het volume van stijgende die indrukkingen door een apparatengrafiek (en niet binnen de originele publiekssegmenten worden gevonden) leveraging worden geleverd. Deze maatstaf wordt ook gebruikt voor de berekening van de toepasselijke vergoedingen voor het gebruik van een apparaatgrafiek van derden.

  Om de kosten van uw uitgebreide indrukken tijdens een tijdspanne te bepalen, stel een douanerapport in dat de [!UICONTROL Extended Impressions] kolom omvat, en vermenigvuldig dan het totale aantal uitgebreide indrukkingen met $0.00035 ($0.35/1000 drukken).

  De geaggregeerde kosten worden ook opgenomen in de kolom [!UICONTROL Billable Other Net Spend] (onder [!UICONTROL Metrics] > [!UICONTROL Spend] ), hoewel die metrische waarde ook andere campagnekosten bevat die u mogelijk hebt toegevoegd.

* **Grafiek van het Apparaat:** (in de [!UICONTROL Build Your Report] sectie onder [!UICONTROL Dimensions] > [!UICONTROL Campaign]) de geselecteerde apparatengrafiek voor een bepaalde campagne, een pakket, of een plaatsing.

## Waarderingsmeting op basis van personen

*Advertisers met slechts het volgen van de omzetting van Adobe Advertising*

Met op mensen gebaseerde attributie, kunt u omzettingen verklaren die op een verschillend apparaat dan het apparaat plaatsvonden waarop de media blootstelling voorkwam. Over DSP, [!DNL Adobe Advertising Creative] en [!DNL Adobe Advertising Search, Social, & Commerce] zijn maateenheden voor individuele toewijzingen beschikbaar voor adverteerders die Adobe Advertising-conversiepixels op hun sites hebben geïmplementeerd.

### Op personen gebaseerde attribuutmeting inschakelen

Neem contact op met het Adobe-accountteam als u de meting voor apparaattoewijzing wilt activeren.

### [!UICONTROL Conversion] Rapporten instellen voor toewijzing van apparaatconversie

#### [!UICONTROL Conversion] Rapportinstellingen

Wanneer een apparaatgrafiek is ingeschakeld voor attributiemeting, bevat het rapport [!UICONTROL Conversion] een instelling [!UICONTROL Cross-Device Breakout] , waarmee u maximaal drie aparte kolommen voor elke conversiemetrie kunt opnemen, waaronder:

* &lt;*Omzetting*> [!UICONTROL (tp)]: Omvat de totale omzettingen (totale mensen), die zowel de omzettingen van het zelfde-apparaat en dwars-apparatenomzettingen (als toepasselijk) omvat. In het rapport, &quot;[!UICONTROL (tp)]&quot;wordt toegevoegd aan de metrische naam van de omzetting, regeltype, en omzettingstypes in de omzettingsweg (bijvoorbeeld, &quot;Reacties (le) (tl) (tp))).

* &lt;*Omzetting*> [!UICONTROL (sd)]: (Facultatief) omvat slechts omzettingen waarvoor slechts één enkel apparaat in de omzettingsweg werd gevolgd. In het rapport, &quot;[!UICONTROL (sd)]&quot;wordt toegevoegd aan de metrische naam van de omzetting, regeltype, en omzettingstypes in de omzettingsweg (bijvoorbeeld, &quot;Reacties (le) (tl) (sd))).

* &lt;*Omzetting*> [!UICONTROL (xd)]: (Facultatief) omvat slechts omzettingen waarvoor meer dan één apparaat in de omzettingsweg werd gevolgd. In het rapport, &quot;[!UICONTROL (xd)]&quot;wordt toegevoegd aan de metrische naam van de omzetting, regeltype, en omzettingstypes in de omzettingsweg (bijvoorbeeld, &quot;Reacties (le) (tl) (xd))).

#### Het rapport [!UICONTROL Conversion] interpreteren

Sorteer het percentage van totale omzettingen die dwars-apparaat ([!UICONTROL (xd)] zijn/ [!UICONTROL (tl)]) van hoog aan laag om te begrijpen wat boven-gemiddelde dwars-apparatenomzettingen drijft. U kunt dit gebruiken om uw creatieve of het richten strategie te informeren om overseinen en kanaalinvestering aan gebruikersgedrag aan te passen.

* Pakketten — Zie welke pakketten de meeste totale omzettingen drijven, en welke degenen een hoog percentage van dwars-apparatenomzettingen hebben. Dit kan u helpen begrijpen waar te om uitgaven te concentreren.

* Plaatsen — Vergelijk plaatsingsprestaties en attributie (bijvoorbeeld, een mobiele Web en kan omzettingen op Desktop drijven). Zonder apparaatgrafiek voor attributie kunt u de invloed van een mobiele webplaatsing op desktopconversies missen. Het is ook mogelijk dat deze wordt begraven als de meeste gebruikers de conversie op het bureaublad en niet op het mobiele web uitvoeren.

* Advertenties — Ontdek welke advertenties tot hogere omzettingen leiden en kwantificeer de waarde en impact ervan in zowel webbrowsers als mobiele toepassingsomgevingen.

* Sites — Optimaliseren voor alle sites in plaats van sites handmatig uit te sluiten. Als een website conversies tussen apparaten aandrijft, dan kunt u zien op welke apparaten dit gedrag voorkomt.

* Deals — Verbeter handmatige optimalisering door te verifiëren welke inventarisovereenkomsten de omzettingen van verschillende apparaten leveren, en dan te beslissen of u uw richten zou moeten uitbreiden om meer apparaten en kanalen in die overeenkomsten te omvatten.

>[!MORELIKETHIS]
>
>* [&#x200B; Montages van het Rapport &#x200B;](/help/dsp/reports/report-settings.md)
>* [&#x200B; Montages van de Campagne &#x200B;](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [&#x200B; de Montages van het Pakket &#x200B;](/help/dsp/campaign-management/packages/package-settings.md)
>* [&#x200B; Montages van de Plaatsing &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md)
