---
title: Informatie over simulaties
description: Meer informatie over portfoliosimulaties.
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Informatie over simulaties

*eigenschap van Beta*

Simulatierapporten tonen de geraamde marginale kosten-naar-objectieve waarde, de kosten, het aantal kliks en de objectieve waarde die u voor een portefeuille op diverse bestedingsniveaus (kosten) en de overeenkomstige dagelijkse begrotingen of andere doelstellingen kunt verwachten. U kunt naar keuze de mening <!-- add link --> aanpassen om extra verkeersmetriek, simulatie montages, en slechts een specifiek simulatietype ([!UICONTROL Weekly] of [!UICONTROL Custom]) te zien.

<!-- Not available as of 6/21/25:
When the portfolio has a daily budget, you can optionally change the portfolio's spend target to any of the spend targets listed in the simulation.
-->

## Typen simulaties

* **Geautomatiseerde wekelijkse simulaties:** de rapporten van de Simulatie worden in werking gesteld automatisch elke week gebruikend de huidige portefeuillemontages. De geautomatiseerde wekelijkse simulaties zijn beschikbaar slechts voor periodes waarin de portefeuille [ wordt geoptimaliseerd of actief ](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md).

  Elke gedownloade wekelijkse simulatie bestaat uit één werkboek. Elk werkboek omvat het doel voor elk van 20 stapniveaus en de verwachte kosten, klikken, gewogen opbrengst (objectieve waarde), en omzettingsmetriek inbegrepen in het doel, die op het overeenkomstige doel wordt gebaseerd. Voor de eerste 20 gegevensrijen werden geen beperkingen toegepast; voor de overige gegevensrijen werden beperkingen toegepast.

* **Douane, gebruiker-geproduceerde simulaties:** u kunt een rapport van de douanesimulatie voor één enkel [ geoptimaliseerde of actieve ](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-about.md) portefeuille tot stand brengen gebruikend de huidige portefeuillemontages of gebruikend de montages van de douaneportefeuille om de resultaten te zien die die montages zouden produceren zonder hen eigenlijk te veranderen. Bijvoorbeeld, kon u een douanesimulatie tot stand brengen om het effect te zien van het gebruiken van een verschillende het uitgeven strategie of het leren begroting <!-- Not available yet:  , or without considering active constraints on bid units in the portfolio-->. U kunt de geschatte prestaties weergeven op het niveau van het portfolio, de campagne, de biedeenheid en het apparaat. De simulaties van de douane erven de beperkingen die het uitgeven plaatsen van de portefeuille.

  >[!NOTE]
  >
  > In het nieuwe aangepaste simulatieformulier worden dezelfde instellingen gebruikt als in het oude formulier, behalve dat het de beperkingsgegevens van de biedingseenheid overneemt van de portfolioinstellingen. U kunt de beperkingen van de biedingseenheid niet negeren, zoals u hebt gedaan op de pagina met oude aangepaste simulatie-instellingen.

  Elke gedownloade douanesimulatie bestaat uit één werkboek. Elk werkboek omvat één aantekenvel voor elk gespecificeerd entiteitniveau van simulatie (portefeuilles, campagnes, en groepen, biedingseenheden) wanneer de gegevens voor dat niveau beschikbaar zijn. Wanneer u gegevens op apparaatniveau opgeeft, bevat elk werkblad een [!UICONTROL Device] -kolom. Elk aantekenvel omvat één rij met gegevens voor elke toepasselijke entiteit en (wanneer gespecificeerd voor het rapport) en apparatentype voor elk van 20 stappen (bijvoorbeeld, één rij per campagne). De gegevens in elke rij omvatten de geprojecteerde marginale kosten-naar-opbrengst, kosten, kliks, gewogen opbrengsten (objectieve waarde), het apparatentype, en omzettingsmetriek inbegrepen in de doelstelling, die op het overeenkomstige doel wordt gebaseerd. Het werkblad op portfolioniveau bevat ook het doel voor de stappen en het werkblad op entiteitniveau bevat het advertentienetwerk, de account, de campagne en (indien van toepassing) de advertentiegroep.   <!-- I don't see a Bid Units tab when specified; clarify when it is and isn't included -->

## De weergave [!UICONTROL Simulations]

In de weergave [!UICONTROL Simulations] worden wekelijkse simulaties en aangepaste simulaties weergegeven. De beheerder en sommige andere gebruikerstypes <!-- Verify which --> kunnen douanesimulaties zien die door andere gebruikers worden gecreeerd. Alle andere gebruikers kunnen alleen de aangepaste simulaties zien die ze maken.

De gegevenstabel bevat de voortgang van elke simulatie, een [!UICONTROL Target Midpoint] -kolom die voor elke rij wordt gevuld en kolommen voor de voorspellingen van de kosten/impositie/klik/objectieve waarde, werkelijke waarden en nauwkeurigheid. U kunt desgewenst extra aangepaste kolommen toevoegen (inclusief liftmetriek, zoals de werkelijke objectieve waarde gedeeld door de kosten).

### Beschikbare acties {#simulations-actions}

* [ pas de mening ](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) aan om extra metriek, met inbegrip van de geschatte beelden te omvatten; de daadwerkelijke kosten, kliks, impressies, en objectieve waarde; de kosten-aan-objectieve waarde; de kostennauwkeurigheid, kliknauwkeurigheid, en objectieve waardeconfliciteit; en het verschil (delta) tussen de voorspelde en daadwerkelijke objectieve waarde en kosten-aan-objectieve waarde. U kunt ook kolommen voor de meeste simulatie-instellingen en het simulatietype ([!UICONTROL Custom] of [!UICONTROL Weekly] ) opnemen.

* [ produceer of hervat een douanesimulatie ](simulation-create.md) voor één enkele portefeuille. U kunt of een nieuwe simulatie tot stand brengen of een bestaande simulatie in de lijst regenereren.

* [ Download wekelijkse en douanesimulaties ](simulation-download.md) als [!DNL Microsoft Excel] werkboeken in de dossiers van het PIT.

* Open met de knop [!UICONTROL Spend Planner] het oude gereedschap Aanbeveling voor uitgaven, waarmee u de optimale uitgavenverdeling over portfolio&#39;s kunt identificeren.

## Aanbevolen procedures

De simulatierapporten van de monitor in de volgende situaties:

* Voordat u een portfolio start om de prestaties te ramen die u kunt verwachten met de overeenkomende portfolioinstellingen; gebruik minimaal twee weken gegevens. Als de simulatieresultaten op lagere prestaties wijzen dan u zou verwachten gebaseerd op historische gegevens voor inbegrepen campagnes, onderzoek en los de kwesties alvorens de portefeuille te lanceren.

* Na elke belangrijke wijziging in een portfolio, zoals het toevoegen van een campagne of het wijzigen van het doel. Als u veranderingen in de modelleringsbegindatum van de portefeuille aanbrengt, het gewicht van metrisch, of de klikwaarde van een doelstelling, dan wacht tot na 17:00 PST de volgende dag om de simulatie in werking te stellen, wanneer de bijgewerkte kosten en opbrengstmodellen beschikbaar zijn.

* Periodiek om prestatietrends op het omzettingsmetrische niveau te controleren.

>[!MORELIKETHIS]
>
>* [ Looppas of hervat een simulatie ](simulation-create.md)
>* [ simulaties van de Download ](simulation-download.md)
