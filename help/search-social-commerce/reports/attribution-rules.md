---
title: Hoe toewijzingsregels worden berekend
description: Leer hoe Adobe Advertising elk type attributieregel berekent.
source-git-commit: 6436866ae7684a330f74c14e58ee30d365de80a1
workflow-type: tm+mt
source-wordcount: '2431'
ht-degree: 0%

---

# Hoe de toewijzingsregels worden berekend voor Adobe-reclame

*Adverteerders die alleen de conversie van Adoben Advertising bijhouden*

<!-- Verify statements about cross-device events -->

De attributieregel op adverteerderniveau wordt gebruikt om conversiegegevens — mogelijk over meerdere advertentiekanalen — toe te wijzen in een reeks gebeurtenissen die tot een conversie leiden.

In rapporten, gebrek en douanemeningen voor Advertising Onderzoek, Sociale, &amp; Handel (Onderzoek, Sociale, &amp; Handel), en (sommige gebruikersrollen) portefeuille-vlakke simulaties voor Onderzoek, Sociale, &amp; Handel, wordt de geselecteerde regel gebruikt slechts voor de mening, het rapport, of de simulatiegegevens. De verschillende toewijzingsregels worden als volgt toegepast.

>[!NOTE]
>
>* De attributieregels zijn van toepassing op kliks op betaalde advertenties in om het even welk kanaal en op beelden op vertoning en sociale advertenties. Ze zijn niet van toepassing op afbeeldingen voor betaalde zoekopdrachten, die niet op gebeurtenisniveau kunnen worden bijgehouden.
>* Adobe Advertising slaat altijd de volgende gebeurtenissen voor elke surfer van het Web vóór een omzetting op: a) de eerste betaalde klik; b) maximaal 10 klikken voor elk kanaal (zoeken, sociale weergave of weergave), inclusief de eerste klik; en c) maximaal 10 beeldschermafbeeldingen. <!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
* Bij DSP en Advertising Creative van advertenties houden apparaatdefinities alleen rekening met het gebeurtenispad van de geselecteerde attributieregel.<!-- cross-device attribution via LiveRamp only -->
* In rapporten en beheersmeningen, hangt het aantal decimalen die voor een waarde worden getoond van de munt af, maar de Adobe Advertising slaat nauwkeurigere waarden op.

## Laatste gebeurtenis (de standaardwaarde)

Kenmerkend voor de conversie naar de laatst betaalde klik in de reeks binnen de adverteerders [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) of, als er geen betaalde klikjes zijn geweest, tot de laatste indruk binnen de adverteerder [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j).

Wanneer de conversie alleen wordt voorafgegaan door indrukken, wordt de conversie beschouwd als een *doorzien*, die volgens de [instelling voor doorkijkgewicht](/help/search-social-commerce/glossary.md#uv) of — zoals gespecificeerd — volgens de view-through waarderingsmethode die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.

![Percentage voor laatste gebeurtenistoewijzing](/help/search-social-commerce/assets/attribution-percent-last-event.png "Percentage voor laatste gebeurtenistoewijzing")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: Klik1, Click2, Click3, Omzetting van 120 USD

De conversie wordt toegewezen aan Click 3 voor een bedrag van 120 USD.

### Voorbeeld met zowel afbeeldingen als klikken

**Opmerking:** Impressies zijn alleen van toepassing op weergave- en sociale advertenties.

Gebeurtenispad: Impressie 1, klik 1, Impressie 2, Omzetting van 120 USD

De conversie wordt toegewezen aan Click 1 voor een bedrag van 120 USD.

### Voorbeeld met alle impressies

**Opmerking:** Alleen afbeeldingen voor weergave en sociale advertenties zijn van toepassing.

Gebeurtenispad: Impressie 1, Impressie 2, Impressie 3, Omzetting van 120 USD

De conversie wordt toegeschreven aan Impression 3. Omdat de conversie een doorkijkbenadering is, wordt de doorkijkwaarderingsmethode toegepast die is geselecteerd in de sectie &quot;Conversiekenmerk&quot; van de rapportinstellingen:

* Als de rapportparameter een gewogen mening-door gewicht specificeert, dan wordt dat gewicht toegepast op mening-door. Als het doorkijkgewicht van de adverteerder bijvoorbeeld 40% is, dan is 120 USD x 40% = 48 USD, zodat 48 USD wordt toegeschreven aan Impression 3.

* Als de rapportparameter het gebruiken van ruwe waarden voor mening-door specificeert, dan wordt geen mening-door gewicht toegepast op mening-door, en volledige 120 USD wordt toegeschreven aan Indrukking 3.

+++

<!-- end examples as collapsible content -->

## Eerste gebeurtenis

Kenmerkend voor de conversie naar de eerste betaalde klik in de reeks binnen de adverteerders [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) of, indien er geen betaalde klikjes zijn geweest, de eerste indruk binnen de adverteerder [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j). Deze regel is alleen beschikbaar voor gebeurtenissen op afzonderlijke apparaten.

Wanneer de conversie alleen wordt voorafgegaan door impressies, wordt de conversie beschouwd als een *doorzien*, die volgens de [instelling voor doorkijkgewicht](/help/search-social-commerce/glossary.md#uv) of — zoals gespecificeerd — volgens de view-through waarderingsmethode die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.

![Toewijzingspercentage eerste gebeurtenis](/help/search-social-commerce/assets/attribution-percent-first-event.png "Toewijzingspercentage eerste gebeurtenis")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: Klik 1, klik 2, klik 3, Omzetting van 120 USD

De conversie wordt toegewezen aan Click 1 voor een bedrag van 120 USD.

### Voorbeeld met zowel afbeeldingen als klikken

**Opmerking:** Impressies zijn alleen van toepassing op weergave- en sociale advertenties.

Gebeurtenispad: Impressie 1, klik 1, Impressie 2, Omzetting van 120 USD

De conversie wordt toegewezen aan Click 1 voor een bedrag van 120 USD.

### Voorbeeld met alle impressies

**Opmerking:** Alleen afbeeldingen voor weergave en sociale advertenties zijn van toepassing.

Gebeurtenispad: Impressie 1, Impressie 2, Impressie 3, Omzetting van 120 USD

De conversie wordt toegeschreven aan Impression 1. Aangezien de conversie een doorkijkbenadering is, wordt de waarderingsmethode die is geselecteerd in het gedeelte Conversiekenmerken (Weergavecampagnes) van de rapportinstellingen toegepast:

* Als de rapportparameter een gewogen mening-door gewicht specificeert, dan wordt dat gewicht toegepast op mening-door. Als het doorkijkgewicht van de adverteerder bijvoorbeeld 40% is, dan is 120 x 40% = 48 USD, dus wordt 48 USD toegewezen aan Impression 1.

* Als de rapportparameter het gebruiken van ruwe waarden voor mening-door specificeert, dan wordt geen mening-door gewicht toegepast op mening-door, en volledige 120 USD wordt toegeschreven aan Indrukking 1.

+++

<!-- end examples as collapsible content -->

## Dikte eerste gebeurtenis meer

Kenmerkt de omzetting aan alle gebeurtenissen in de reeks die binnen adverteerders voorkwamen [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j), maar geeft het grootste gewicht aan de eerste gebeurtenis en achtereenvolgens minder gewicht aan de volgende gebeurtenissen. Deze regel is alleen beschikbaar voor gebeurtenissen op afzonderlijke apparaten.

Wanneer de conversie alleen wordt voorafgegaan door impressies, wordt de conversie beschouwd als een *doorzien*, die volgens de [instelling voor doorkijkgewicht](/help/search-social-commerce/glossary.md#uv) of — zoals gespecificeerd — volgens de view-through waarderingsmethode die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.

Wanneer het omzettingspad zowel &#39;betaal&#39; als &#39;impressions&#39; bevat, worden de afbeeldingen door verschillende Adobe Advertising-producten anders behandeld:

* In Search, Social, &amp; Commerce, [dikte van indruk overschrijven](/help/search-social-commerce/glossary.md#i-j) — die in de indruk van de adverteerder wordt opgegeven, overschrijft de gewichtsinstelling en in de parameters report, view of custom simulatie — wordt eerst toegepast op de afbeeldingen.

* In DSP worden de afbeeldingen genegeerd en worden alleen de klikken gewogen. DSP neemt geen indruk met voorrang van gewichten in overweging voor attributie.

![Gewicht eerste gebeurtenis meer toewijzingspercentages](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "Gewicht eerste gebeurtenis meer toewijzingspercentages")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: Klik 1, klik 2, klik 3, Omzetting van 120 USD

Attributie: Klik op 1 = 60 USD, klik op 2 = 40 USD, klik op 3 = 20 USD (totaal 120 USD)

### Voorbeelden met zowel afbeeldingen als klikken

**Opmerking:** Impressies zijn alleen van toepassing op weergave- en sociale advertenties.

Gebeurtenispad: Afdruk 1, klik 1, Indrukking 2, klik 2, Omzetting van 120 USD

#### (Alleen zoeken, Sociaal en Handel) De standaard &#39;Gewicht bij indrukken overschrijven&#39; van 10% gebruiken

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, is het gewicht van de impressie met voeten getreden.

Attributie: Impressie 1 = 8 USD, klik 1 = 72 USD, Impressie 2 = 4 USD, klik 2 = 36 USD (120 USD in totaal)

#### Het gebruiken van (DSP slechts) geen Gewicht van de Overschrijving van de Indrukking of (Onderzoek, Sociale, &amp; Handel slechts) een &quot;Gewicht van de Overschrijving van de Indrukking van 0%

Aangezien de gebeurtenisreeks zowel afbeeldingen als klikken bevat, worden de indrukkingen genegeerd.

Attributie: Impressie 1 = 0 USD, klik 1 = 80 USD, Impressie 2 = 0 USD, klik 2 = 40 USD (totaal 120 USD)

### Voorbeeld met alle impressies

**Opmerking:** Alleen afbeeldingen voor weergave-advertenties zijn van toepassing.

Gebeurtenispad: Impressie 1, Impressie 2, Impressie 3, Omzetting van 120 USD

Omdat de conversie een doorkijkbenadering is, wordt de doorkijkwaarderingsmethode — in plaats van de impressiegraad — toegepast om de waarde van elke impressie te bepalen:

* Als in de rapportparameter een gewogen doorkijkgewicht is opgegeven, wordt dat gewicht toegepast op de waarden van de indruk. Als het doorkijkgewicht bijvoorbeeld 40% is, dan is Impressie 1 = 24 USD, Impression 2 = 16 USD, Impression 3 = 8 USD (48 USD in totaal)

* Als de rapportparameter het gebruiken van ruwe waarden voor mening-door specificeert, dan wordt geen mening-door gewicht toegepast op de indruk, en volledige 120 USD wordt verdeeld tussen de drie beelden: Impressie 1 = 60 USD, Impressie 2 = 40 USD, Impressie 3 = 20 USD (120 USD in totaal)

+++

<!-- end examples as collapsible content -->

## Even verdelen

>[!NOTE]
>
>Deze regel is alleen beschikbaar voor gebeurtenissen op afzonderlijke apparaten.

Kenmerkt de omzetting gelijkelijk aan elke gebeurtenis in de reeks die binnen adverteerders optrad [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j).

Wanneer de conversie alleen wordt voorafgegaan door impressies, wordt de conversie beschouwd als een *doorzien*, die volgens de [instelling voor doorkijkgewicht](/help/search-social-commerce/glossary.md#uv) of — zoals gespecificeerd — volgens de view-through waarderingsmethode die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.

Wanneer het omzettingspad zowel &#39;betaal&#39; als &#39;Ongewenste&#39; afbeeldingen bevat, worden de afbeeldingen door verschillende Adobe-advertentieproducten anders behandeld:

* In Search, Social, &amp; Commerce, [dikte van indruk overschrijven](/help/search-social-commerce/glossary.md#i-j) — die in de indruk van de adverteerder wordt opgegeven, overschrijft de gewichtsinstelling en in de parameters report, view of custom simulatie — wordt eerst toegepast op de afbeeldingen.

* In DSP worden de afbeeldingen genegeerd en worden alleen de klikken gewogen. DSP neemt geen indruk met voorrang van gewichten in overweging voor attributie.

![Even-toewijzingspercentages](/help/search-social-commerce/assets/attribution-percent-even.png "Even-toewijzingspercentages")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: Klik op 1, klik op 2, klik op 3, zet 120 USD om

Geen beelden leidden tot de omzetting, zodat is de indruk overschrijven gewicht niet van toepassing, en de omzetting is gelijk verdeeld tussen de drie klikken:

Attributie: Klik op 1 = 40 USD, klik op 2 = 40 USD, klik op 3 = 40 USD (totaal 120 USD)

### Voorbeelden met zowel afbeeldingen als klikken

**Opmerking:** Impressies zijn alleen van toepassing op weergave- en sociale advertenties.

Gebeurtenispad: Afdruk 1, klik 1, Indrukking 2, klik 2, Omzetting van 120 USD

#### (Alleen zoeken, Sociaal en Handel) De standaard &#39;Gewicht bij indrukken overschrijven&#39; van 10% gebruiken

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, is het gewicht van de impressie met voeten getreden.

Attributie: Impressie 1 = 6 USD, klik 1 = 54 USD, Impressie 2 = 6 USD, klik 2 = 54 USD (in totaal 120 USD)

#### Het gebruiken (slechts Adobe Advertising DSP) geen Gewicht van de Overschrijving van de Indrukking of (Onderzoek, Sociale, &amp; Handel slechts) een &quot;Gewicht van de Overschrijving van de Indrukking van 0%

Aangezien de gebeurtenisreeks zowel afbeeldingen als klikken bevat, worden de indrukkingen genegeerd.

Attributie: Impressie 1 = 0 USD, klik 1 = 60 USD, Impressie 2 = 0 USD, klik 2 = 60 USD (totaal 120 USD)

## Voorbeeld met alle impressies

**Opmerking:** Alleen afbeeldingen voor weergave-advertenties zijn van toepassing.

Gebeurtenispad: Impressie 1, Impressie 2, Impressie 3, Omzetting van 120 USD

Omdat de conversie een doorkijkbenadering is, wordt de doorkijkwaarderingsmethode — in plaats van de impressiegraad — toegepast om de waarde van elke impressie te bepalen:

* Als in de rapportparameter een gewogen doorkijkgewicht is opgegeven, wordt dat gewicht toegepast op de waarden van de indruk. Als het doorkijkgewicht bijvoorbeeld 40% is, dan is Impressie 1 = 16 USD, Impression 2 = 16 USD, Impression 3 = 16 USD (48 USD in totaal)

* Als de rapportparameter het gebruiken van ruwe waarden voor mening-door specificeert, dan wordt geen mening-door gewicht toegepast op de indruk, en volledige 120 USD wordt verdeeld tussen de drie beelden: Impressie 1 = 40 USD, Impressie 2 = 40 USD, Impressie 3 = 40 USD (120 USD in totaal)

+++

<!-- end examples as collapsible content -->

## Dikte laatste gebeurtenis meer

Kenmerkt de omzetting aan alle gebeurtenissen in de reeks die binnen adverteerders voorkwamen [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j), maar geeft het grootste belang aan het laatste evenement en achtereenvolgens minder gewicht aan de voorafgaande gebeurtenissen.

Wanneer de conversie alleen wordt voorafgegaan door impressies, wordt de conversie beschouwd als een *doorzien*, die volgens de [instelling voor doorkijkgewicht](/help/search-social-commerce/glossary.md#uv) of — zoals gespecificeerd — volgens de view-through waarderingsmethode die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.

Wanneer het omzettingspad zowel &#39;betaal&#39; als &#39;Ongewenste&#39; afbeeldingen bevat, worden de afbeeldingen door verschillende Adobe-advertentieproducten anders behandeld:

* In Search, Social, &amp; Commerce, [dikte van indruk overschrijven](/help/search-social-commerce/glossary.md#i-j) — die in de indruk van de adverteerder wordt opgegeven, overschrijft de gewichtsinstelling en in de parameters report, view of custom simulatie — wordt eerst toegepast op de afbeeldingen.

* In DSP worden de afbeeldingen genegeerd en worden alleen de klikken gewogen. DSP neemt geen indruk met voorrang van gewichten in overweging voor attributie.

![Gewicht laatste gebeurtenis meer toewijzingspercentages](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png "Gewicht laatste gebeurtenis meer toewijzingspercentages")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: Klik 1, klik 2, klik 3, Omzetting van 120 USD

Attributie: Klik 3 = 60 USD, klik 2 = 40 USD, klik 1 = 20 USD (totaal 120 USD)

### Voorbeelden met zowel afbeeldingen als klikken

**Opmerking:** Impressies zijn alleen van toepassing op weergave- en sociale advertenties.

Gebeurtenispad: Afdruk 1, klik 1, Indrukking 2, klik 2, Omzetting van 120 USD

#### (Alleen zoeken, Sociaal en Handel) De standaard &#39;Gewicht bij indrukken overschrijven&#39; van 10% gebruiken

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, is het gewicht van de impressie met voeten getreden.

Attributie: Impressie 1 = 4 USD, klik 1 = 36 USD, Impressie 2 = 8 USD, klik 2 = 72 USD (in totaal 120 USD)

#### Het gebruiken van (DSP slechts) geen Gewicht van de Overschrijving van de Indrukking of (Onderzoek, Sociale, &amp; Handel slechts) een &quot;Gewicht van de Overschrijving van de Indrukking van 0%

Aangezien de gebeurtenisreeks zowel afbeeldingen als klikken bevat, worden de indrukkingen genegeerd.

Attributie: Impressie 1 = 0 USD, klik 1 = 40 USD, Impressie 2 = 0 USD, klik 2 = 80 USD (totaal 120 USD)

### Voorbeeld met alle impressies

**Opmerking:** Impressies zijn alleen van toepassing op weergave- en sociale advertenties.

Gebeurtenispad: Impressie 1, Impressie 2, Impressie 3, Omzetting van 120 USD

Omdat de conversie een doorkijkbenadering is, wordt de doorkijkwaarderingsmethode — in plaats van de impressiegraad — toegepast om de waarde van elke impressie te bepalen:

* Als in de rapportparameter een gewogen doorkijkgewicht is opgegeven, wordt dat gewicht toegepast op de waarden van de indruk. Als het doorkijkgewicht bijvoorbeeld 40% is, vermenigvuldigt u elke waarde in het vak &quot;Voorbeeld met alle klikken&quot; met 40%: Impressie 3 = 24 USD, Impressie 2 = 16 USD, Impressie 1 = 8 USD (48 USD in totaal)

* Als de rapportparameter het gebruiken van ruwe waarden voor mening-productie specificeert, dan volledig 120 USD wordt verdeeld tussen de beelden: Impressie 3 = 60 USD, Impressie 2 = 40 USD, Impressie 1 = 20 USD (120 USD in totaal)

+++

<!-- end examples as collapsible content -->

## U-vormig

Kenmerkt de omzetting aan alle gebeurtenissen in de reeks die binnen adverteerders voorkwamen [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j), maar geeft het grootste belang aan het eerste en laatste evenement, met achtereenvolgens minder gewicht aan de gebeurtenissen in het midden van het conversiepad.

Wanneer de conversie alleen wordt voorafgegaan door impressies, wordt de conversie beschouwd als een *doorzien*, die volgens de [instelling voor doorkijkgewicht](/help/search-social-commerce/glossary.md#uv) of — zoals gespecificeerd — volgens de view-through waarderingsmethode die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.

Wanneer het omzettingspad zowel &#39;betaal&#39; als &#39;Ongewenste&#39; afbeeldingen bevat, worden de afbeeldingen door verschillende Adobe-advertentieproducten anders behandeld:

* In Search, Social, &amp; Commerce, [dikte van indruk overschrijven](/help/search-social-commerce/glossary.md#i-j) — die in de indruk van de adverteerder wordt opgegeven, overschrijft de gewichtsinstelling en in de parameters report, view of custom simulatie — wordt eerst toegepast op de afbeeldingen.

* In DSP worden de afbeeldingen genegeerd en worden alleen de klikken gewogen. DSP neemt geen indruk met voorrang van gewichten in overweging voor attributie.

<!-- ![U-shaped attribution percentages](/help/search-social-commerce/assets/attribution-percent-u-shaped.png "U-shaped event attribution percentages") -->

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: Klik op 1, klik op 2, klik op 3, klik op 4, zet 120 USD om

Attributie: Klik op 1 = 36 USD, klik op 2 = 24 USD, klik op 3 = 24 USD, klik op 4 = 36 USD (120 USD in totaal)

### Voorbeelden met zowel afbeeldingen als klikken

**Opmerking:** Impressies zijn alleen van toepassing op weergave- en sociale advertenties.

Gebeurtenispad: Afdruk 1, klik 1, Indrukking 2, klik 2, Omzetting van 120 USD

#### (Alleen zoeken, Sociaal en Handel) De standaard &#39;Gewicht bij indrukken overschrijven&#39; van 10% gebruiken

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, is het gewicht van de impressie met voeten getreden.

Attributie: Impressie 1 = 6 USD, klik 1 = 54 USD, Impressie 2 = 6 USD, klik 2 = 54 USD (in totaal 120 USD)

#### Het gebruiken van (DSP slechts) geen indruk overschrijft gewicht of (Onderzoek, Sociale, &amp; Handel slechts) een &quot;Gewicht van de Overschrijving van de Indrukking van 0%

Aangezien de gebeurtenisreeks zowel afbeeldingen als klikken bevat, worden de indrukkingen genegeerd.

Attributie: Impressie 1 = 0 USD, klik 1 = 60 USD, Impressie 2 = 0 USD, klik 2 = 60 USD (totaal 120 USD)

### Voorbeeld met alle impressies

**Opmerking:** Alleen afbeeldingen voor weergave-advertenties zijn van toepassing.

Gebeurtenispad: Impressie 1, Impressie 2, Impressie 3, Impressie 4, Omzetting van 120 USD

Omdat de conversie een doorkijkbenadering is, wordt de doorkijkwaarderingsmethode — in plaats van de impressiegraad — toegepast om de waarde van elke impressie te bepalen:

* Als in de rapportparameter een gewogen doorkijkgewicht is opgegeven, wordt dat gewicht toegepast op de waarden van de indruk. Bijvoorbeeld, als het mening-door gewicht 40% is, dan klik 1 = 14.40 USD, klik 2 = 9.60 USD, klik 3 = 9.60 USD, klik 4 = 14.40 USD (48 USD totaal)

* Als de rapportparameter het gebruiken van ruwe waarden voor mening-productie specificeert, dan volledig 120 USD wordt verdeeld tussen de beelden: Klik op 1 = 36 USD, klik op 2 = 24 USD, klik op 3 = 24 USD, klik op 4 = 36 USD (120 USD in totaal)

+++

<!-- end examples as collapsible content -->
