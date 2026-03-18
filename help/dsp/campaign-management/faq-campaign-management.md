---
title: Veelgestelde vragen over campagnebeheer
description: Meer informatie over campagnebeheer, waaronder de latentieperiode voor wijzigingen en wat er gebeurt wanneer u budgetwijzigingen aanbrengt tijdens een vlucht.
feature: DSP Packages, DSP Placements
exl-id: 8a443543-ebb1-4273-a007-afef07d32d8c
source-git-commit: 21ed5558a39ea9b097be8e70ef81bcf8e59c14b4
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# Veelgestelde vragen over campagnebeheer

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Latentie bij het instellen van wijzigingen

* Wanneer u een plaatsing of pakketinstelling wijzigt, wanneer wordt de wijziging van kracht?

  Wijzigingen in instellingen worden gewoonlijk onmiddellijk van kracht, maar kunnen tot 12 uur in beslag nemen.

  Als het de laatste leveringsdag is, breng vroegtijdig veranderingen aan zodat DSP genoeg tijd heeft om het pakket opnieuw te kalibreren gebaseerd op de veranderingen. Als u bijvoorbeeld overschakelt van een pacing naar een frontload-overeenkomst, moet DSP opnieuw beoordelen hoe de uitgaven gedurende de rest van de vlucht moeten worden verdeeld. Breng dat soort verandering niet aan als je maar één uur over hebt om op de laatste dag van de vlucht te leveren.

## Tussentijdse begrotingsupdates

* Hoe lang duurt het voor DSP het budget van het pakket herverdeelt wanneer u een wijziging aanbrengt in een plaatsing?

  De begrotingstoewijzing is gebaseerd op de prestaties bij plaatsing, die worden beoordeeld aan de hand van een gemiddelde van 14 dagen. Wijzigingen in een plaatsing leiden alleen tot wijzigingen in de begrotingstoewijzing wanneer de prestaties tijdens het gemiddelde van 14 dagen worden gewijzigd.

  Wanneer de prestatiesveranderingen voorkomen, wijst DSP het pakketbudget onder de plaatsen dienovereenkomstig tijdens de volgende cyclus van de begrotingsoptimalisering, die om middernacht (00 :00) in de de tijdzone van de campagne voorkomt.

* Hoe wordt het budget opnieuw toegewezen wanneer een plaatsing uit een pakket wordt verwijderd en aan een ander pakket wordt toegevoegd?

  De volledige doorloophistorie van een plaatsing wordt aan de plaatsing gekoppeld en wordt hiermee van pakket naar pakket verplaatst.

  Wanneer u een plaatsing uit een pakket verwijdert, heeft het pakket niet langer een geschiedenis van de uitgaven van de plaatsing. Het budget voor het pakket wordt (budget voor het pakketbudget - budget voor plaatsing verwijderd) / het resterende tijdsinterval tijdens de vlucht. De pakketbegroting wordt vervolgens toegewezen aan de overblijvende plaatsen in het pakket.

  En als u dezelfde plaatsing toevoegt aan een ander pakket, houdt DSP rekening met de doorloopgeschiedenis van de plaatsing wanneer het budget toewijst voor alle plaatsingen in het nieuwe pakket.

* Hoe verandert het pakket op de laatste dag van een vlucht?

  Op de laatste dag van een vlucht wordt de dag verkort van 24 uur tot 23 uur, zodat het budget voor het pakket niet wordt overschreden. Ook, verandert de het verpakken van het pakket vulstrategie automatisch in &quot;[!UICONTROL Frontload],&quot;zelfs als het aan &quot;[!UICONTROL even]&quot;wordt geplaatst. Dit betekent 65% van de dagelijkse begroting tegen 11 :30 a.m. EST zou moeten leveren.

>[!MORELIKETHIS]
>
>* [ de Montages van het Pakket ](/help/dsp/campaign-management/packages/package-settings.md)
>* [ Montages van de Plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md)
>* [ Beste praktijken voor de Campagnes van Prestaties van de Opstelling ](/help/dsp/optimization/campaign-best-practices-performance.md)
