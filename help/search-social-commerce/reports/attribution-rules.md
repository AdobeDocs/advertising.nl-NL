---
title: Hoe toewijzingsregels worden berekend
description: Leer hoe Adobe Advertising elk type attributieregel berekent.
exl-id: b61561fa-8c01-4989-9ef7-620d2b4c2c0b
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '2439'
ht-degree: 0%

---

# Hoe toewijzingsregels worden berekend voor Adobe Advertising

*Adverteerders die alleen de conversie van Adoben Advertising bijhouden*

<!-- Verify statements about cross-device events -->

De attributieregel op adverteerderniveau wordt gebruikt om conversiegegevens — mogelijk over meerdere advertentiekanalen — toe te wijzen in een reeks gebeurtenissen die tot een conversie leiden.

In rapporten, gebrek en douanemeningen voor Advertising Onderzoek, Sociale, &amp; Handel (Onderzoek, Sociale, &amp; Handel), en (sommige gebruikersrollen) portefeuille-vlakke simulaties voor Onderzoek, Sociale, &amp; Handel, wordt de geselecteerde regel gebruikt slechts voor de mening, het rapport, of de simulatiegegevens. De verschillende toewijzingsregels worden als volgt toegepast.

>[!NOTE]
>
>* De attributieregels zijn van toepassing op kliks op betaalde advertenties in om het even welk kanaal en op beelden op vertoning en sociale advertenties. Ze zijn niet van toepassing op afbeeldingen voor betaalde zoekopdrachten, die niet op gebeurtenisniveau kunnen worden bijgehouden.
>* Adobe Advertising slaat altijd de volgende gebeurtenissen voor elke surfer van het Web vóór een omzetting op: a) de eerste betaalde klik; b) tot 10 klikken voor elk kanaal (onderzoek, sociale, of vertoning), met inbegrip van de eerste klik; en c) tot 10 vertoningsindrukken. <!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
>* Bij DSP en Advertising Creative van advertenties houden apparaatdefinities alleen rekening met het gebeurtenispad van de geselecteerde toewijzingsregel.<!-- cross-device attribution via LiveRamp only -->
>* In rapporten en beheersmeningen, hangt het aantal decimalen voor een waarde af van de munt, maar de Adobe Advertising slaat nauwkeurigere waarden op.

## Laatste gebeurtenis (de standaardwaarde)

Kenmerkend voor de conversie naar de laatst betaalde klik in de reeks binnen de adverteerders [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) of, als er geen betaalde klikjes zijn geweest, tot de laatste indruk binnen de adverteerder [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j).

Wanneer de conversie alleen wordt voorafgegaan door indrukken, wordt de conversie beschouwd als een *doorzien*, die wordt gewogen volgens de [instelling voor doorkijkgewicht](/help/search-social-commerce/glossary.md#uv) of — zoals gespecificeerd — volgens de view-through waarderingsmethode die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.

![Percentage voor laatste gebeurtenistoewijzing](/help/search-social-commerce/assets/attribution-percent-last-event.png "Percentage voor laatste gebeurtenistoewijzing")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: Click1, Click2, Click3, Conversie van 120 USD

De conversie wordt toegewezen aan Click 3 voor een bedrag van 120 USD.

### Voorbeeld met zowel afbeeldingen als klikken

**Opmerking:** Impressies zijn alleen van toepassing op weergave- en sociale advertenties.

Gebeurtenispad: Impressie 1, Klik op 1, Impressie 2, Conversie van 120 USD

De conversie wordt toegewezen aan Click 1 voor een bedrag van 120 USD.

### Voorbeeld met alle impressies

**Opmerking:** Alleen afbeeldingen voor weergave en sociale advertenties zijn van toepassing.

Event path: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

De conversie wordt toegeschreven aan Impression 3. Omdat de conversie een doorkijkbenadering is, wordt de doorkijkwaarderingsmethode toegepast die is geselecteerd in het gedeelte &quot;Conversiekenmerk&quot; van de rapportinstellingen:

* Als de rapportparameter een gewogen mening-door gewicht specificeert, dan wordt dat gewicht toegepast op mening-door. Als het doorkijkgewicht van de adverteerder bijvoorbeeld 40% is, dan is 120 USD x 40% = 48 USD, zodat 48 USD wordt toegeschreven aan Impression 3.

* Als de rapportparameter het gebruiken van ruwe waarden voor mening-door specificeert, dan wordt geen mening-door gewicht toegepast op mening-door, en volledige 120 USD wordt toegeschreven aan Indrukking 3.

+++

<!-- end examples as collapsible content -->

## Eerste gebeurtenis

Kenmerkend voor de conversie naar de eerste betaalde klik in de reeks binnen de adverteerders [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) of, indien er geen betaalde klikjes zijn geweest, de eerste indruk binnen de adverteerder [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j). Deze regel is alleen beschikbaar voor gebeurtenissen op afzonderlijke apparaten.

Wanneer de conversie alleen wordt voorafgegaan door impressies, wordt de conversie beschouwd als een *doorzien*, die wordt gewogen volgens de [instelling voor doorkijkgewicht](/help/search-social-commerce/glossary.md#uv) of — zoals gespecificeerd — volgens de view-through waarderingsmethode die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.

![Toewijzingspercentage eerste gebeurtenis](/help/search-social-commerce/assets/attribution-percent-first-event.png "Toewijzingspercentage eerste gebeurtenis")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: klik op 1, klik op 2, klik op 3, zet 120 USD om

De conversie wordt toegewezen aan Click 1 voor een bedrag van 120 USD.

### Voorbeeld met zowel afbeeldingen als klikken

**Opmerking:** Impressies zijn alleen van toepassing op weergave- en sociale advertenties.

Gebeurtenispad: Impressie 1, Klik op 1, Impressie 2, Conversie van 120 USD

De conversie wordt toegewezen aan Click 1 voor een bedrag van 120 USD.

### Voorbeeld met alle impressies

**Opmerking:** Alleen afbeeldingen voor weergave en sociale advertenties zijn van toepassing.

Event path: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

De conversie wordt toegeschreven aan Impression 1. Aangezien de conversie een doorkijkbenadering is, wordt de waarderingsmethode die is geselecteerd in het gedeelte Conversiekenmerken (Weergavecampagnes) van de rapportinstellingen toegepast:

* Als de rapportparameter een gewogen mening-door gewicht specificeert, dan wordt dat gewicht toegepast op mening-door. Als het doorkijkgewicht van de adverteerder bijvoorbeeld 40% is, dan is 120 x 40% = 48 USD, dus wordt 48 USD toegewezen aan Impression 1.

* Als de rapportparameter het gebruiken van ruwe waarden voor mening-door specificeert, dan wordt geen mening-door gewicht toegepast op mening-door, en volledige 120 USD wordt toegeschreven aan Indrukking 1.

+++

<!-- end examples as collapsible content -->

## Dikte eerste gebeurtenis meer

Kenmerken de omzetting aan alle gebeurtenissen in de reeks die binnen adverteerders voorkwamen [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j), maar geeft het grootste gewicht aan de eerste gebeurtenis en achtereenvolgens minder gewicht aan de volgende gebeurtenissen. Deze regel is alleen beschikbaar voor gebeurtenissen op afzonderlijke apparaten.

Wanneer de conversie alleen wordt voorafgegaan door impressies, wordt de conversie beschouwd als een *doorzien*, die wordt gewogen volgens de [instelling voor doorkijkgewicht](/help/search-social-commerce/glossary.md#uv) of — zoals gespecificeerd — volgens de view-through waarderingsmethode die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.

Wanneer het omzettingspad zowel &#39;betaal&#39; als &#39;impressions&#39; bevat, worden de afbeeldingen door verschillende Adobe Advertising-producten anders behandeld:

* In Zoeken, Sociale &amp; Handel, [dikte van indruk overschrijven](/help/search-social-commerce/glossary.md#i-j) — die in de indruk van de adverteerder wordt opgegeven, overschrijft de gewichtsinstelling en in de parameters report, view of custom simulatie — wordt eerst toegepast op de afbeeldingen.

* In DSP worden de afbeeldingen genegeerd en worden alleen de klikken gewogen. DSP neemt geen indruk met voorrang van gewichten in overweging voor attributie.

![Gewicht eerste gebeurtenis meer toewijzingspercentages](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "Gewicht eerste gebeurtenis meer toewijzingspercentages")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: klik op 1, klik op 2, klik op 3, zet 120 USD om

Attributie: klik 1 = 60 USD, klik 2 = 40 USD, klik 3 = 20 USD (totaal 120 USD)

### Voorbeelden met zowel afbeeldingen als klikken

**Opmerking:** Impressies zijn alleen van toepassing op weergave- en sociale advertenties.

Gebeurtenispad: Impressie 1, Klik op 1, Impressie 2, klik op 2, Conversie van 120 USD

#### (Alleen zoeken, Sociaal en Handel) De standaard &#39;Gewicht bij indrukken overschrijven&#39; van 10% gebruiken

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, is het gewicht van de impressie met voeten getreden.

Attributie: Impressie 1 = 8 USD, Klik 1 = 72 USD, Impressie 2 = 4 USD, klik 2 = 36 USD (120 USD in totaal)

#### Het gebruiken van (DSP slechts) geen Gewicht van de Overschrijving van de Indrukking of (Onderzoek, Sociale, &amp; Handel slechts) een &quot;Gewicht van de Overschrijving van de Indrukking van 0%

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, worden de indrukkingen genegeerd.

Attributie: Impressie 1 = 0 USD, Klik 1 = 80 USD, Impressie 2 = 0 USD, klik 2 = 40 USD (in totaal 120 USD)

### Voorbeeld met alle impressies

**Opmerking:** Alleen afbeeldingen voor weergave-advertenties zijn van toepassing.

Event path: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

Omdat de conversie een doorkijkbenadering is, wordt de doorkijkwaarderingsmethode — in plaats van de impressiegraad — toegepast om de waarde van elke impressie te bepalen:

* Als in de rapportparameter een gewogen doorkijkgewicht is opgegeven, wordt dat gewicht toegepast op de waarden van de indruk. Als het doorkijkgewicht bijvoorbeeld 40% is, dan is Impressie 1 = 24 USD, Impression 2 = 16 USD, Impression 3 = 8 USD (48 USD in totaal)

* Als in de rapportparameter onbewerkte waarden worden gebruikt voor doorzicht, wordt geen doorkijkgewicht toegepast op de indruk en wordt de volledige 120 USD verdeeld over de drie indrukken: Impressie 1 = 60 USD, Impression 2 = 40 USD, Impression 3 = 20 USD (totaal 120 USD)

+++

<!-- end examples as collapsible content -->

## Even verdelen

>[!NOTE]
>
>Deze regel is alleen beschikbaar voor gebeurtenissen op afzonderlijke apparaten.

Kenmerkt de omzetting gelijkelijk aan elke gebeurtenis in de reeks die binnen adverteerders optrad [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j).

Wanneer de conversie alleen wordt voorafgegaan door impressies, wordt de conversie beschouwd als een *doorzien*, die wordt gewogen volgens de [instelling voor doorkijkgewicht](/help/search-social-commerce/glossary.md#uv) of — zoals gespecificeerd — volgens de view-through waarderingsmethode die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.

Wanneer het omzettingspad zowel &#39;betaal&#39; als &#39;impressions&#39; bevat, worden de afbeeldingen door verschillende Adobe Advertising-producten anders behandeld:

* In Zoeken, Sociale &amp; Handel, [dikte van indruk overschrijven](/help/search-social-commerce/glossary.md#i-j) — die in de indruk van de adverteerder wordt opgegeven, overschrijft de gewichtsinstelling en in de parameters report, view of custom simulatie — wordt eerst toegepast op de afbeeldingen.

* In DSP worden de afbeeldingen genegeerd en worden alleen de klikken gewogen. DSP neemt geen indruk met voorrang van gewichten in overweging voor attributie.

![Even-toewijzingspercentages](/help/search-social-commerce/assets/attribution-percent-even.png "Even-toewijzingspercentages")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: klik op 1, klik op 2, klik op 3, zet 120 USD om

Geen beelden leidden tot de omzetting, zodat is de indruk overschrijven gewicht niet van toepassing, en de omzetting is gelijk verdeeld tussen de drie klikken:

Attributie: klik 1 = 40 USD, klik 2 = 40 USD, klik 3 = 40 USD (totaal 120 USD)

### Voorbeelden met zowel afbeeldingen als klikken

**Opmerking:** Impressies zijn alleen van toepassing op weergave- en sociale advertenties.

Gebeurtenispad: Impressie 1, Klik op 1, Impressie 2, klik op 2, Conversie van 120 USD

#### (Alleen zoeken, Sociaal en Handel) De standaard &#39;Gewicht bij indrukken overschrijven&#39; van 10% gebruiken

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, is het gewicht van de impressie met voeten getreden.

Attributie: Impressie 1 = 6 USD, Klik 1 = 54 USD, Impressie 2 = 6 USD, klik 2 = 54 USD (120 USD in totaal)

#### Het gebruiken (slechts Adobe Advertising DSP) geen Gewicht van de Overschrijving van de Indrukking of (Onderzoek, Sociale, &amp; Handel slechts) een &quot;Gewicht van de Overschrijving van de Indrukking van 0%

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, worden de indrukkingen genegeerd.

Attributie: Impressie 1 = 0 USD, Klik 1 = 60 USD, Impressie 2 = 0 USD, klik 2 = 60 USD (totaal 120 USD)

## Voorbeeld met alle impressies

**Opmerking:** Alleen afbeeldingen voor weergave-advertenties zijn van toepassing.

Event path: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

Omdat de conversie een doorkijkbenadering is, wordt de doorkijkwaarderingsmethode — in plaats van de impressiegraad — toegepast om de waarde van elke impressie te bepalen:

* Als in de rapportparameter een gewogen doorkijkgewicht is opgegeven, wordt dat gewicht toegepast op de waarden van de indruk. Als het doorkijkgewicht bijvoorbeeld 40% is, dan is Impressie 1 = 16 USD, Impression 2 = 16 USD, Impression 3 = 16 USD (48 USD in totaal)

* Als in de rapportparameter onbewerkte waarden worden gebruikt voor doorzicht, wordt geen doorkijkgewicht toegepast op de indruk en wordt de volledige 120 USD verdeeld over de drie indrukken: Impressie 1 = 40 USD, Impression 2 = 40 USD, Impression 3 = 40 USD (totaal 120 USD)

+++

<!-- end examples as collapsible content -->

## Dikte laatste gebeurtenis meer

Kenmerken de omzetting aan alle gebeurtenissen in de reeks die binnen adverteerders voorkwamen [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j), maar geeft het grootste belang aan het laatste evenement en achtereenvolgens minder gewicht aan de voorafgaande gebeurtenissen.

Wanneer de conversie alleen wordt voorafgegaan door impressies, wordt de conversie beschouwd als een *doorzien*, die wordt gewogen volgens de [instelling voor doorkijkgewicht](/help/search-social-commerce/glossary.md#uv) of — zoals gespecificeerd — volgens de view-through waarderingsmethode die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.

Wanneer het omzettingspad zowel &#39;betaal&#39; als &#39;impressions&#39; bevat, worden de afbeeldingen door verschillende Adobe Advertising-producten anders behandeld:

* In Zoeken, Sociale &amp; Handel, [dikte van indruk overschrijven](/help/search-social-commerce/glossary.md#i-j) — die in de indruk van de adverteerder wordt opgegeven, overschrijft de gewichtsinstelling en in de parameters report, view of custom simulatie — wordt eerst toegepast op de afbeeldingen.

* In DSP worden de afbeeldingen genegeerd en worden alleen de klikken gewogen. DSP neemt geen indruk met voorrang van gewichten in overweging voor attributie.

![Gewicht laatste gebeurtenis meer toewijzingspercentages](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png "Gewicht laatste gebeurtenis meer toewijzingspercentages")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: klik op 1, klik op 2, klik op 3, zet 120 USD om

Attributie: klik 3 = 60 USD, klik 2 = 40 USD, klik 1 = 20 USD (totaal 120 USD)

### Voorbeelden met zowel afbeeldingen als klikken

**Opmerking:** Impressies zijn alleen van toepassing op weergave- en sociale advertenties.

Gebeurtenispad: Impressie 1, Klik op 1, Impressie 2, klik op 2, Conversie van 120 USD

#### (Alleen zoeken, Sociaal en Handel) De standaard &#39;Gewicht bij indrukken overschrijven&#39; van 10% gebruiken

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, is het gewicht van de impressie met voeten getreden.

Attributie: Impressie 1 = 4 USD, Klik 1 = 36 USD, Impressie 2 = 8 USD, klik 2 = 72 USD (120 USD in totaal)

#### Het gebruiken van (DSP slechts) geen Gewicht van de Overschrijving van de Indrukking of (Onderzoek, Sociale, &amp; Handel slechts) een &quot;Gewicht van de Overschrijving van de Indrukking van 0%

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, worden de indrukkingen genegeerd.

Attributie: Impressie 1 = 0 USD, Klik 1 = 40 USD, Impressie 2 = 0 USD, klik 2 = 80 USD (totaal 120 USD)

### Voorbeeld met alle impressies

**Opmerking:** Impressies zijn alleen van toepassing op weergave- en sociale advertenties.

Event path: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

Omdat de conversie een doorkijkbenadering is, wordt de doorkijkwaarderingsmethode — in plaats van de impressiegraad — toegepast om de waarde van elke impressie te bepalen:

* Als in de rapportparameter een gewogen doorkijkgewicht is opgegeven, wordt dat gewicht toegepast op de waarden van de indruk. Als het doorkijkgewicht bijvoorbeeld 40% is, vermenigvuldigt u elke waarde in het &quot;Voorbeeld met alle klikken&quot; met 40%: Impressie 3 = 24 USD, Impressie 2 = 16 USD, Impressie 1 = 8 USD (48 USD in totaal)

* Als de rapportparameter het gebruiken van ruwe waarden voor mening-productie specificeert, dan volledig 120 USD wordt verdeeld over de drukken: Indrukking 3 = 60 USD, Indrukking 2 = 40 USD, Indrukking 1 = 20 USD (totaal 120 USD)

+++

<!-- end examples as collapsible content -->

## U-gevormd

Kenmerken de omzetting aan alle gebeurtenissen in de reeks die binnen adverteerders voorkwamen [klik terugkijkvenster](/help/search-social-commerce/glossary.md#c-d) en [terugkijkvenster van indruk](/help/search-social-commerce/glossary.md#i-j), maar geeft het grootste belang aan het eerste en laatste evenement, met achtereenvolgens minder gewicht aan de gebeurtenissen in het midden van het conversiepad.

Wanneer de conversie alleen wordt voorafgegaan door impressies, wordt de conversie beschouwd als een *doorzien*, die wordt gewogen volgens de [instelling voor doorkijkgewicht](/help/search-social-commerce/glossary.md#uv) of — zoals gespecificeerd — volgens de view-through waarderingsmethode die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.

Wanneer het omzettingspad zowel &#39;betaal&#39; als &#39;impressions&#39; bevat, worden de afbeeldingen door verschillende Adobe Advertising-producten anders behandeld:

* In Zoeken, Sociale &amp; Handel, [dikte van indruk overschrijven](/help/search-social-commerce/glossary.md#i-j) — die in de indruk van de adverteerder wordt opgegeven, overschrijft de gewichtsinstelling en in de parameters report, view of custom simulatie — wordt eerst toegepast op de afbeeldingen.

* In DSP worden de afbeeldingen genegeerd en worden alleen de klikken gewogen. DSP neemt geen indruk met voorrang van gewichten in overweging voor attributie.

![U-vormig toewijzingspercentage](/help/search-social-commerce/assets/attribution-percent-u-shaped.png "U-vormig toewijzingspercentage")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: klik op 1, klik op 2, klik op 3, klik op 4, zet 120 USD om

Attributie: klik 1 = 36 USD, klik 2 = 24 USD, klik 3 = 24 USD, klik 4 = 36 USD (in totaal 120 USD)

### Voorbeelden met zowel afbeeldingen als klikken

**Opmerking:** Impressies zijn alleen van toepassing op weergave- en sociale advertenties.

Gebeurtenispad: Impressie 1, Klik op 1, Impressie 2, klik op 2, Conversie van 120 USD

#### (Alleen zoeken, Sociaal en Handel) De standaard &#39;Gewicht bij indrukken overschrijven&#39; van 10% gebruiken

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, is het gewicht van de impressie met voeten getreden.

Attributie: Impressie 1 = 6 USD, Klik 1 = 54 USD, Impressie 2 = 6 USD, klik 2 = 54 USD (120 USD in totaal)

#### Het gebruiken van (DSP slechts) geen indruk overschrijft gewicht of (Onderzoek, Sociale, &amp; Handel slechts) een &quot;Gewicht van de Overschrijving van de Indrukking van 0%

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, worden de indrukkingen genegeerd.

Attributie: Impressie 1 = 0 USD, Klik 1 = 60 USD, Impressie 2 = 0 USD, klik 2 = 60 USD (totaal 120 USD)

### Voorbeeld met alle impressies

**Opmerking:** Alleen afbeeldingen voor weergave-advertenties zijn van toepassing.

Event path: Impression 1, Impression 2, Impression 3, Impression 4, Conversion of 120 USD

Omdat de conversie een doorkijkbenadering is, wordt de doorkijkwaarderingsmethode — in plaats van de impressiegraad — toegepast om de waarde van elke impressie te bepalen:

* Als in de rapportparameter een gewogen doorkijkgewicht is opgegeven, wordt dat gewicht toegepast op de waarden van de indruk. Bijvoorbeeld, als het mening-door gewicht 40% is, dan klik 1 = 14.40 USD, klik 2 = 9.60 USD, klik 3 = 9.60 USD, klik 4 = 14.40 USD (48 USD totaal)

* Als de rapportparameter het gebruiken van ruwe waarden voor mening-productie specificeert, dan volledig 120 USD wordt verdeeld tussen de drukken: Klik 1 = 36 USD, klik 2 = 24 USD, klik 3 = 24 USD, klik 4 = 36 USD (totaal 120 USD)

+++

<!-- end examples as collapsible content -->
