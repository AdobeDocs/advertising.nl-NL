---
title: Hoe toewijzingsregels worden berekend
description: Leer hoe Adobe Advertising elk type toewijzingsregel berekent.
exl-id: 15beeadd-bb65-4efe-8c4f-34c4a48cc775
feature: Search Reports, DSP Custom Reports
source-git-commit: 513d81cf835ccbffa16581799f0dc8306681e3ad
workflow-type: tm+mt
source-wordcount: '2711'
ht-degree: 0%

---

# Hoe toewijzingsregels worden berekend voor Adobe Advertising

*Advertisers met slechts het volgen van de omzetting van Adobe Advertising*

<!-- Verify statements about cross-device events -->

De attributieregel op adverteerderniveau wordt gebruikt om conversiegegevens — mogelijk over meerdere advertentiekanalen — toe te wijzen in een reeks gebeurtenissen die tot een conversie leiden.

U kunt ook op de volgende plaatsen een toewijzingsregel selecteren om de regel alleen toe te passen op de resulterende gegevens:

* DSP

   * Aangepaste rapporten met multi-aanraakkenmerk

* Zoeken, sociaal en Commerce

   * Aangepaste rapporten

   * Standaardweergave en aangepaste weergaven

   * (Sommige gebruikersrollen) simulaties op Portfolio-niveau.

>[!NOTE]
>
>* De attributieregels zijn van toepassing op kliks op betaalde advertenties in om het even welk kanaal en op beelden op vertoning en sociale advertenties. Ze zijn niet van toepassing op afbeeldingen voor betaalde zoekopdrachten, die niet op gebeurtenisniveau kunnen worden bijgehouden.
>* Adobe Advertising slaat altijd de volgende gebeurtenissen voor elke surfer van het Web vóór een omzetting op: a) de eerste betaalde klik; b) tot 10 klikken voor elk kanaal (onderzoek, sociale, of vertoning), met inbegrip van de eerste klik; en c) tot 10 vertoningsbeelden.<!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
>* In Advertising DSP en Advertising Creative houden apparaatdefinities alleen rekening met het gebeurtenispad van de geselecteerde toewijzingsregel.<!-- cross-device attribution via LiveRamp only -->
>* In rapporten en beheersmeningen, hangt het aantal decimalen voor een waarde af van de munt, maar Adobe Advertising slaat nauwkeurigere waarden op.

## Laatste gebeurtenis (de standaardwaarde)

Attributes de omzetting aan de laatste betaalde klik in de reeks binnen het 2} de imitatieraadplegingsvenster van de adverteerder [ klikt raadplegingsvenster ](/help/search-social-commerce/glossary.md#c-d) of, als geen betaalde kliks voorkwam, aan de laatste indruk binnen het 2} imkerraadplegingsvenster van de adverteerder [.](/help/search-social-commerce/glossary.md#i-j)

Wanneer de omzetting slechts door impressies wordt voorafgegaan, dan wordt de omzetting beschouwd a *mening-door*, die of volgens 2} mening-door gewicht dat van de adverteerder [ plaatst of - zoals gespecificeerd - volgens de mening-door waarderingsmethode wordt gewogen die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.](/help/search-social-commerce/glossary.md#uv)

![ de percentages van de de gebeurtenisattributie van de laatste gebeurtenis ](/help/search-social-commerce/assets/attribution-percent-last-event.png " De percentages van de gebeurtenisattributie ")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: Click1, Click2, Click3, Conversie van 120 USD

De conversie wordt toegewezen aan Click 3 voor een bedrag van 120 USD.

### Voorbeeld met zowel afbeeldingen als klikken

**Nota:** de Impressies zijn van toepassing slechts van vertoning en sociale advertenties.

Gebeurtenispad: Impressie 1, Klik op 1, Impressie 2, Conversie van 120 USD

De conversie wordt toegewezen aan Click 1 voor een bedrag van 120 USD.

### Voorbeeld met alle impressies

**Nota:** slechts beelden voor vertoning en sociale advertenties zijn van toepassing.

Event path: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

De conversie wordt toegeschreven aan Impression 3. Omdat de conversie een doorkijkbenadering is, wordt de doorkijkwaarderingsmethode toegepast die is geselecteerd in het gedeelte &quot;Conversiekenmerk&quot; van de rapportinstellingen:

* Als de rapportparameter een gewogen mening-door gewicht specificeert, dan wordt dat gewicht toegepast op mening-door. Als het doorkijkgewicht van de adverteerder bijvoorbeeld 40% is, dan is 120 USD x 40% = 48 USD, zodat 48 USD wordt toegeschreven aan Impression 3.

* Als de rapportparameter het gebruiken van ruwe waarden voor mening-door specificeert, dan wordt geen mening-door gewicht toegepast op mening-door, en volledige 120 USD wordt toegeschreven aan Indrukking 3.

+++

<!-- end examples as collapsible content -->

## Eerste gebeurtenis

Attributes de omzetting aan de eerste betaalde klik in de reeks binnen het 2} de imitatieraadplegingsvenster van de adverteerder [ klikt raadplegingsvenster ](/help/search-social-commerce/glossary.md#c-d) of, als geen betaalde kliks voorkwam, aan de eerste indruk binnen het 2} imkerraadplegingsvenster van de adverteerder [. ](/help/search-social-commerce/glossary.md#i-j) Deze regel is alleen beschikbaar voor gebeurtenissen op afzonderlijke apparaten.

Wanneer de omzetting slechts door impressies wordt voorafgegaan, wordt de omzetting beschouwd a *mening-door*, die of volgens het 2} mening-door gewicht dat van de adverteerder [ plaatst of - zoals gespecificeerd - volgens de mening-door waarderingsmethode wordt gewogen die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.](/help/search-social-commerce/glossary.md#uv)

![ de percentages van de gebeurtenisattributie van de eerste gebeurtenis ](/help/search-social-commerce/assets/attribution-percent-first-event.png " Eerste percentages van de gebeurtenisattributie ")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: klik op 1, klik op 2, klik op 3, zet 120 USD om

De conversie wordt toegewezen aan Click 1 voor een bedrag van 120 USD.

### Voorbeeld met zowel afbeeldingen als klikken

**Nota:** de Impressies zijn van toepassing slechts van vertoning en sociale advertenties.

Gebeurtenispad: Impressie 1, Klik op 1, Impressie 2, Conversie van 120 USD

De conversie wordt toegewezen aan Click 1 voor een bedrag van 120 USD.

### Voorbeeld met alle impressies

**Nota:** slechts beelden voor vertoning en sociale advertenties zijn van toepassing.

Event path: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

De conversie wordt toegeschreven aan Impression 1. Omdat de conversie een doorkijkbenadering is, wordt de waarderingsmethode die is geselecteerd in de conversie &quot;(Weergavecampagnes)
De sectie &quot;Attributie&quot; van de rapportinstellingen wordt toegepast:

* Als de rapportparameter een gewogen mening-door gewicht specificeert, dan wordt dat gewicht toegepast op mening-door. Als het doorkijkgewicht van de adverteerder bijvoorbeeld 40% is, dan is 120 x 40% = 48 USD, dus wordt 48 USD toegewezen aan Impression 1.

* Als de rapportparameter het gebruiken van ruwe waarden voor mening-door specificeert, dan wordt geen mening-door gewicht toegepast op mening-door, en volledige 120 USD wordt toegeschreven aan Indrukking 1.

+++

<!-- end examples as collapsible content -->

## Dikte eerste gebeurtenis meer

Attributes de omzetting aan alle gebeurtenissen in de reeks die binnen het paneel van de adverteerder [ voorkwamen klikken raadplegingsvenster ](/help/search-social-commerce/glossary.md#c-d) en [ het venster van de imitatieraadpleging ](/help/search-social-commerce/glossary.md#i-j), maar geeft het meeste gewicht aan de eerste gebeurtenis en opeenvolgend minder gewicht aan de volgende gebeurtenissen.Deze regel is beschikbaar voor gebeurtenissen over enige slechts apparaten.

Wanneer de omzetting slechts door impressies wordt voorafgegaan, wordt de omzetting beschouwd a *mening-door*, die of volgens het 2} mening-door gewicht dat van de adverteerder [ plaatst of - zoals gespecificeerd - volgens de mening-door waarderingsmethode wordt gewogen die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.](/help/search-social-commerce/glossary.md#uv)

Wanneer het conversiepad zowel &#39;betaal&#39; als &#39;impressions&#39; bevat, worden de afbeeldingen door verschillende Adobe Advertising-producten anders behandeld:

* In Onderzoek, Sociaal, &amp; Commerce, wordt de [ impressie met voeten getreden gewicht ](/help/search-social-commerce/glossary.md#i-j) — die in de de impressie van de adverteerder het gewicht dat en in rapport wordt gespecificeerd, mening, of de parameters van de douanesimulatie — eerst toegepast op de beelden.

* In DSP worden de afbeeldingen genegeerd en worden alleen de klikken gewogen. DSP houdt geen rekening met de indruk dat gewichten voorrang hebben op gewichten.

![ de eerste gebeurtenis van het gewicht van 0} eerste gebeurtenis meer attributiepercentages {van 1} Gewicht eerste gebeurtenis meer attributiepercentages ](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: klik op 1, klik op 2, klik op 3, zet 120 USD om

Attributie: klik 1 = 60 USD, klik 2 = 40 USD, klik 3 = 20 USD (totaal 120 USD)

### Voorbeelden met zowel afbeeldingen als klikken

**Nota:** de Impressies zijn van toepassing slechts van vertoning en sociale advertenties.

Gebeurtenispad: Impressie 1, Klik op 1, Impressie 2, klik op 2, Conversie van 120 USD

#### (Alleen zoeken, Sociaal en Commerce) De standaard &#39;Gewicht bij indrukken overschrijven&#39; van 10% gebruiken

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, is het gewicht van de impressie met voeten getreden.

Attributie: Impressie 1 = 8 USD, Klik 1 = 72 USD, Impressie 2 = 4 USD, klik 2 = 36 USD (120 USD in totaal)

#### Als u (alleen DSP) geen Dikte voor indrukking overschrijft of (alleen Zoeken, Sociaal en Commerce) een Gewicht voor indrukken overschrijven van 0% gebruikt

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, worden de indrukkingen genegeerd.

Attributie: Impressie 1 = 0 USD, Klik 1 = 80 USD, Impressie 2 = 0 USD, klik 2 = 40 USD (in totaal 120 USD)

### Voorbeeld met alle impressies

**Nota:** slechts beelden voor vertoningsadvertenties zijn van toepassing.

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

Attributes evenzeer aan elke gebeurtenis in de reeks die binnen het van de adverteerder [ voorkwam klikken raadplegingsvenster ](/help/search-social-commerce/glossary.md#c-d) en [ het venster van de imkerraadpleging ](/help/search-social-commerce/glossary.md#i-j).

Wanneer de omzetting slechts door impressies wordt voorafgegaan, wordt de omzetting beschouwd a *mening-door*, die of volgens het 2} mening-door gewicht dat van de adverteerder [ plaatst of - zoals gespecificeerd - volgens de mening-door waarderingsmethode wordt gewogen die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.](/help/search-social-commerce/glossary.md#uv)

Wanneer het conversiepad zowel &#39;betaal&#39; als &#39;impressions&#39; bevat, worden de afbeeldingen door verschillende Adobe Advertising-producten anders behandeld:

* In Onderzoek, Sociaal, &amp; Commerce, wordt de [ impressie met voeten getreden gewicht ](/help/search-social-commerce/glossary.md#i-j) — die in de de impressie van de adverteerder het gewicht dat en in rapport wordt gespecificeerd, mening, of de parameters van de douanesimulatie — eerst toegepast op de beelden.

* In DSP worden de afbeeldingen genegeerd en worden alleen de klikken gewogen. DSP houdt geen rekening met de indruk dat gewichten voorrang hebben op gewichten.

![ Even attributiepercentages ](/help/search-social-commerce/assets/attribution-percent-even.png " de attributiepercentages ")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: klik op 1, klik op 2, klik op 3, zet 120 USD om

Geen beelden leidden tot de omzetting, zodat is de indruk overschrijven gewicht niet van toepassing, en de omzetting is gelijk verdeeld tussen de drie klikken:

Attributie: klik 1 = 40 USD, klik 2 = 40 USD, klik 3 = 40 USD (totaal 120 USD)

### Voorbeelden met zowel afbeeldingen als klikken

**Nota:** de Impressies zijn van toepassing slechts van vertoning en sociale advertenties.

Gebeurtenispad: Impressie 1, Klik op 1, Impressie 2, klik op 2, Conversie van 120 USD

#### (Alleen zoeken, Sociaal en Commerce) De standaard &#39;Gewicht bij indrukken overschrijven&#39; van 10% gebruiken

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, is het gewicht van de impressie met voeten getreden.

Attributie: Impressie 1 = 6 USD, Klik 1 = 54 USD, Impressie 2 = 6 USD, klik 2 = 54 USD (120 USD in totaal)

#### Als u (alleen Adobe Advertising DSP) geen Dikte voor indrukking overschrijft of (alleen Zoeken, Sociaal en Commerce) een Gewicht voor indrukken overschrijven van 0% gebruikt

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, worden de indrukkingen genegeerd.

Attributie: Impressie 1 = 0 USD, Klik 1 = 60 USD, Impressie 2 = 0 USD, klik 2 = 60 USD (totaal 120 USD)

## Voorbeeld met alle impressies

**Nota:** slechts beelden voor vertoningsadvertenties zijn van toepassing.

Event path: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

Omdat de conversie een doorkijkbenadering is, wordt de doorkijkwaarderingsmethode — in plaats van de impressiegraad — toegepast om de waarde van elke impressie te bepalen:

* Als in de rapportparameter een gewogen doorkijkgewicht is opgegeven, wordt dat gewicht toegepast op de waarden van de indruk. Als het doorkijkgewicht bijvoorbeeld 40% is, dan is Impressie 1 = 16 USD, Impression 2 = 16 USD, Impression 3 = 16 USD (48 USD in totaal)

* Als in de rapportparameter onbewerkte waarden worden gebruikt voor doorzicht, wordt geen doorkijkgewicht toegepast op de indruk en wordt de volledige 120 USD verdeeld over de drie indrukken: Impressie 1 = 40 USD, Impression 2 = 40 USD, Impression 3 = 40 USD (totaal 120 USD)

+++

<!-- end examples as collapsible content -->

## Dikte laatste gebeurtenis meer

Attributes de omzetting aan alle gebeurtenissen in de reeks die binnen het paneel van de adverteerder [ voorkwamen klikken raadplegingsvenster ](/help/search-social-commerce/glossary.md#c-d) en [ venster van de imitatieraadpleging ](/help/search-social-commerce/glossary.md#i-j), maar geeft het meeste gewicht aan de laatste gebeurtenis en opeenvolgend minder gewicht aan de voorafgaande gebeurtenissen.

Wanneer de omzetting slechts door impressies wordt voorafgegaan, wordt de omzetting beschouwd a *mening-door*, die of volgens het 2} mening-door gewicht dat van de adverteerder [ plaatst of - zoals gespecificeerd - volgens de mening-door waarderingsmethode wordt gewogen die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.](/help/search-social-commerce/glossary.md#uv)

Wanneer het conversiepad zowel &#39;betaal&#39; als &#39;impressions&#39; bevat, worden de afbeeldingen door verschillende Adobe Advertising-producten anders behandeld:

* In Onderzoek, Sociaal, &amp; Commerce, wordt de [ impressie met voeten getreden gewicht ](/help/search-social-commerce/glossary.md#i-j) — die in de de impressie van de adverteerder het gewicht dat en in rapport wordt gespecificeerd, mening, of de parameters van de douanesimulatie — eerst toegepast op de beelden.

* In DSP worden de afbeeldingen genegeerd en worden alleen de klikken gewogen. DSP houdt geen rekening met de indruk dat gewichten voorrang hebben op gewichten.

![ Dikte laatste gebeurtenis meer attributiepercentages ](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png " Dikte laatste gebeurtenis meer attributiepercentages ")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: klik op 1, klik op 2, klik op 3, zet 120 USD om

Attributie: klik 3 = 60 USD, klik 2 = 40 USD, klik 1 = 20 USD (totaal 120 USD)

### Voorbeelden met zowel afbeeldingen als klikken

**Nota:** de Impressies zijn van toepassing slechts van vertoning en sociale advertenties.

Gebeurtenispad: Impressie 1, Klik op 1, Impressie 2, klik op 2, Conversie van 120 USD

#### (Alleen zoeken, Sociaal en Commerce) De standaard &#39;Gewicht bij indrukken overschrijven&#39; van 10% gebruiken

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, is het gewicht van de impressie met voeten getreden.

Attributie: Impressie 1 = 4 USD, Klik 1 = 36 USD, Impressie 2 = 8 USD, klik 2 = 72 USD (120 USD in totaal)

#### Als u (alleen DSP) geen Dikte voor indrukking overschrijft of (alleen Zoeken, Sociaal en Commerce) een Gewicht voor indrukken overschrijven van 0% gebruikt

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, worden de indrukkingen genegeerd.

Attributie: Impressie 1 = 0 USD, Klik 1 = 40 USD, Impressie 2 = 0 USD, klik 2 = 80 USD (totaal 120 USD)

### Voorbeeld met alle impressies

**Nota:** de Impressies zijn van toepassing slechts van vertoning en sociale advertenties.

Event path: Impression 1, Impression 2, Impression 3, Conversion of 120 USD

Omdat de conversie een doorkijkbenadering is, wordt de doorkijkwaarderingsmethode — in plaats van de impressiegraad — toegepast om de waarde van elke impressie te bepalen:

* Als in de rapportparameter een gewogen doorkijkgewicht is opgegeven, wordt dat gewicht toegepast op de waarden van de indruk. Als het doorkijkgewicht bijvoorbeeld 40% is, vermenigvuldigt u elke waarde in het &quot;Voorbeeld met alle klikken&quot; met 40%: Impressie 3 = 24 USD, Impressie 2 = 16 USD, Impressie 1 = 8 USD (48 USD in totaal)

* Als de rapportparameter het gebruiken van ruwe waarden voor mening-productie specificeert, dan volledig 120 USD wordt verdeeld over de drukken: Indrukking 3 = 60 USD, Indrukking 2 = 40 USD, Indrukking 1 = 20 USD (totaal 120 USD)

+++

<!-- end examples as collapsible content -->

## U-gevormd

Attributes de omzetting aan alle gebeurtenissen in de reeks die binnen het paneel van de adverteerder [ voorkwamen klikken raadplegingsvenster ](/help/search-social-commerce/glossary.md#c-d) en [ venster van de imitatieraadpleging ](/help/search-social-commerce/glossary.md#i-j), maar geeft het meeste gewicht aan de eerste gebeurtenis en laatste gebeurtenissen, met opeenvolgend minder gewicht aan de gebeurtenissen in het midden van de omzettingsweg.

Wanneer de omzetting slechts door impressies wordt voorafgegaan, wordt de omzetting beschouwd a *mening-door*, die of volgens het 2} mening-door gewicht dat van de adverteerder [ plaatst of - zoals gespecificeerd - volgens de mening-door waarderingsmethode wordt gewogen die in het rapport, de mening, of de parameters van de douanesimulatie wordt gespecificeerd.](/help/search-social-commerce/glossary.md#uv)

Wanneer het conversiepad zowel &#39;betaal&#39; als &#39;impressions&#39; bevat, worden de afbeeldingen door verschillende Adobe Advertising-producten anders behandeld:

* In Onderzoek, Sociaal, &amp; Commerce, wordt de [ impressie met voeten getreden gewicht ](/help/search-social-commerce/glossary.md#i-j) — die in de de impressie van de adverteerder het gewicht dat en in rapport wordt gespecificeerd, mening, of de parameters van de douanesimulatie — eerst toegepast op de beelden.

* In DSP worden de afbeeldingen genegeerd en worden alleen de klikken gewogen. DSP houdt geen rekening met de indruk dat gewichten voorrang hebben op gewichten.

![ U vormde attributiepercentages ](/help/search-social-commerce/assets/attribution-percent-u-shaped.png " U vormde attributiepercentages ")

<!-- start examples as collapsible content -->

+++Voorbeelden van gebeurtenisberekeningen

### Voorbeeld met alle klikken

Gebeurtenispad: klik op 1, klik op 2, klik op 3, klik op 4, zet 120 USD om

Attributie: klik 1 = 36 USD, klik 2 = 24 USD, klik 3 = 24 USD, klik 4 = 36 USD (in totaal 120 USD)

### Voorbeelden met zowel afbeeldingen als klikken

**Nota:** de Impressies zijn van toepassing slechts van vertoning en sociale advertenties.

Gebeurtenispad: Impressie 1, Klik op 1, Impressie 2, klik op 2, Conversie van 120 USD

#### (Alleen zoeken, Sociaal en Commerce) De standaard &#39;Gewicht bij indrukken overschrijven&#39; van 10% gebruiken

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, is het gewicht van de impressie met voeten getreden.

Attributie: Impressie 1 = 6 USD, Klik 1 = 54 USD, Impressie 2 = 6 USD, klik 2 = 54 USD (120 USD in totaal)

#### Als u (alleen DSP) geen indruk overschrijft, of (Alleen zoeken, Sociaal en Commerce) een &quot;Dikte voor indrukken&quot; van 0% gebruikt

Omdat de gebeurtenisreeks zowel indrukken als klikken bevatte, worden de indrukkingen genegeerd.

Attributie: Impressie 1 = 0 USD, Klik 1 = 60 USD, Impressie 2 = 0 USD, klik 2 = 60 USD (totaal 120 USD)

### Voorbeeld met alle impressies

**Nota:** slechts beelden voor vertoningsadvertenties zijn van toepassing.

Event path: Impression 1, Impression 2, Impression 3, Impression 4, Conversion of 120 USD

Omdat de conversie een doorkijkbenadering is, wordt de doorkijkwaarderingsmethode — in plaats van de impressiegraad — toegepast om de waarde van elke impressie te bepalen:

* Als in de rapportparameter een gewogen doorkijkgewicht is opgegeven, wordt dat gewicht toegepast op de waarden van de indruk. Bijvoorbeeld, als het mening-door gewicht 40% is, dan klik 1 = 14.40 USD, klik 2 = 9.60 USD, klik 3 = 9.60 USD, klik 4 = 14.40 USD (48 USD totaal)

* Als de rapportparameter het gebruiken van ruwe waarden voor mening-productie specificeert, dan volledig 120 USD wordt verdeeld tussen de drukken: Klik 1 = 36 USD, klik 2 = 24 USD, klik 3 = 24 USD, klik 4 = 36 USD (totaal 120 USD)

+++

<!-- end examples as collapsible content -->
