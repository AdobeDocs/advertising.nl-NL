---
title: Pakketinstellingen
description: Zie beschrijvingen van de beschikbare pakketinstellingen.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: f7332ae243daed3fcc45b69a8d71fff74d7caaeb
workflow-type: tm+mt
source-wordcount: '1060'
ht-degree: 0%

---

# Pakketinstellingen

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** De pakketnaam. De maximumlengte is 60 tekens.

**[!UICONTROL Description]:** (Optioneel) Een beschrijving van het pakket.

**[!UICONTROL 3rd Party Billed Fees]:** (Optioneel) Een statische vergoeding van derden die als niet-factureerbare kosten moet worden bijgehouden:

* **[!UICONTROL CPM]:** De kosten per 1000 beelden (CPM).

* **[!UICONTROL Description]:** Een beschrijving van de CPM-vergoeding.

>[!NOTE]
>
>Billable-kosten worden weergegeven in de [!UICONTROL Net CPM] -norm.

U kunt pakket-niveau met voeten treden dat op het [ plaatsingsniveau ](/help/dsp/campaign-management/placements/placement-settings.md) plaatst.

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Alleen-lezen voor bestaande pakketten) Op welk niveau moet de plaatsing in het pakket worden geplaatst en gelimiteerd:

* **[!UICONTROL Package level pacing]:** Deze het Pakkeren strategie werkt door alle inbegrepen plaatsen als a *groep* af te vangen en te begrenzen. Deze strategie zorgt ervoor dat alle plaatsingen binnen een bepaald pakket holistisch worden geoptimaliseerd, waarbij uitgaven op basis van prestaties en schaal worden verdeeld naar geselecteerde prestatiekernindicatoren (KPI&#39;s).

* **[!UICONTROL Placement level pacing]:** Deze het Pakkeren strategie werkt door alle inbegrepen plaatsen *individueel te verpakken en te begrenzen*. De beste praktijk is om deze strategie alleen te gebruiken om gegarandeerde transacties op de particuliere markt uit te voeren.

**[!UICONTROL Flight Dates]:** De algemene begindatum en einddatum van het pakket. De vluchtdata moeten worden opgenomen in de vluchtdata voor de campagne.

>[!NOTE]
>
>* De vluchtdata voor alle plaatsen die aan dit pakket zijn toegewezen, moeten binnen deze data worden opgenomen.
> * U kunt de begindatum van het pakket niet bewerken wanneer aangepaste flighting wordt geactiveerd.

**[!UICONTROL Activate Custom Flighting]:** Hiermee kunt u in de sectie [!UICONTROL Flighting] hieronder vluchten maken die niet gelijkmatig plaatsen voor het pakket. Nadat u aangepaste flighting hebt ingeschakeld en het pakket hebt opgeslagen, kunt u aangepaste flighting niet uitschakelen en de begindatum van het pakket niet meer bewerken.

**[!UICONTROL Budget]:** (Pakketten met pakket-vlakke verpakking slechts) het bruto begrotingsmaximum en het begrotingsinterval.

Voor pakketten met aangepaste flighting is de budgetinterval altijd *[!UICONTROL All time]* . Geef voor pakketten zonder aangepaste markering het budgetinterval op: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* of *[!UICONTROL Weekly]* .

**[!UICONTROL Gross Budget]:** (Pakketten met pakketniveau het passen en dynamisch margebeheer slechts) het bruto begrotingsmaximum voor de duur van het pakket.

**[!UICONTROL Optimization Goal]:** (Pakketten met pakket-vlakke het verpakken slechts) het optimalisatiedoel voor het pakket. Zie beschrijvingen van elk optimalisatiedoel bij [ de Doelstellingen van de Optimalisering en hoe te om hen ](/help/dsp/optimization/optimization-goals.md) te gebruiken.

**[!UICONTROL Custom Goal for Model Learning]:** (Pakketten met &quot;[!UICONTROL Highest Return on Ad Spend]&quot;en &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;optimaliseringsdoelstellingen slechts) A [ douanedoel ](/help/dsp/optimization/custom-goal.md) dat de opbrengst of omzettingsgebeurtenissen omvat die worden gebruikt om metrisch CPA of ROAS te berekenen. Het aangepaste doel kan desgewenst extra gewogen gebeurtenissen met de bovenste funnel (zoals paginabezoeken en winkelwagentoevoegingen) omvatten die naast de CPA of ROAS-metrische gegevens voor pakketoptimalisatie worden gebruikt. Voor meer informatie over douanedoelstellingen, met inbegrip van de beste praktijken voor het creëren voor douanedoelstellingen en campagnes die hen gebruiken, zie &quot;[ Doelen van de Douane ](/help/dsp/optimization/custom-goal.md)&quot; en &quot;[ Beste praktijken voor de Campagnes van Prestaties van de Vestiging ](/help/dsp/optimization/campaign-best-practices-performance.md).&quot;<!-- At some point, all of the objectives will be prefixed with "ADSP_," but probably that won't show up in the Custom Goal list in the DSP UI. -->

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Facultatief; pakketten met &quot;[!UICONTROL Highest Return on Ad Spend]&quot;en &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;optimaliseringsdoelstellingen slechts) vertelt het optimalisatiemodel om slechts van op klik-gebaseerde omzettingen te leren. Anders leert het optimalisatiemodel van zowel klik- als op indruk gebaseerde omzettingen.

**[!UICONTROL Conversion Metric]:** (Facultatief; pakketten met &quot;[!UICONTROL Highest Return on Ad Spend]&quot;en &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;optimaliseringsdoelstellingen slechts) de definitieve omzettingsgebeurtenis (zoals signups) of opbrengst gebeurtenis/verkoopbedrag (zoals aankoop en aankoopwaarden) aan gebruik voor de berekening van het rendement op advertentie of de kosten per verwerving. Selecteer een optie in de lijst met alle primaire gebeurtenissen (&quot;doelmetriek&quot;) die aan het geselecteerde aangepaste doel zijn toegewezen. Als de lijst leeg is, dan geef het douanedoel uit om minstens één van de onderliggende gebeurtenissen als doel metrisch te omvatten.

**[!UICONTROL Package Goal Type]:** (Pakketten met douaneoptimaliseringsdoelstellingen slechts) het doel van het pakket. Met deze instelling kunt u bepalen hoe het pakket moet worden geoptimaliseerd:

* *[!UICONTROL Prospecting]:* Verkenningspakketten richten zich op het verwerven van nieuwe klanten.

* *[!UICONTROL Retargeting]:* pakketten opnieuw plaatsen richt zich op het opnieuw toegankelijk maken van eerdere bezoekers of klanten.

* *[!UICONTROL Other]:* Alle andere doeleinden.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Pakketten met de doelstellingen van de douaneoptimalisering slechts) Een ander pakket de waarvan historische gegevens als input voor het optimaliseren van het pakket worden gebruikt.

**[!UICONTROL Target]:** (Pakketten met pakket-vlakke het passen slechts) het doeldoel, dat wordt gebruikt om prestaties te volgen.

>[!NOTE]
>
>Dit veld is alleen een benchmark en wordt niet gebruikt voor beslissingen.

**[!UICONTROL Frequency Cap]:** (Pakketten met pakket-vlakke het verpakken slechts) het aantal tijden een uniek apparaat, universele identiteitskaart, of persoon (afhankelijk van gespecificeerde [!UICONTROL Cross Device Level] voor de campagne en het plaatsen [!UICONTROL Targeting] plaatsen van de plaatsing) kan advertenties van het pakket worden gediend. U kunt kiezen uit *[!UICONTROL Unlimited]* of een bepaald bedrag per dag, week of maand.

>[!NOTE]
>
>* U kunt frequentiecappen instellen op campagne-, pakket- en plaatsingsniveaus. DSP respecteert de strengste frequentiegrens in de campagnehiërarchie.
>* De beste praktijken zijn het vaststellen van frequentiecappen voor zowel prospectie als herbestemming op pakketniveau.
> * Hogere frequentiecaps resulteren in hogere uitgaven en indrukken, maar in een lager bereik. Lagere frequentiecaps resulteren in minder uitgaven en indrukken, maar in een hoger bereik.

**[!UICONTROL Pace on]:** (Pakketten met pakket-vlakke het verpakken slechts) wat het verpakken op is gebaseerd:

* *[!UICONTROL Budget]:* (Gebrek) deze optie levert zoveel mogelijk beelden binnen het toegewezen pakketbudget.

* *[!UICONTROL Impressions]:* deze optie levert beelden tot een gespecificeerde hoeveelheid binnen een gespecificeerd interval wordt bereikt. Wanneer u deze optie selecteert, specificeer het aantal beelden en het interval: *Alle tijd,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* of *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Pakketten met pakket-vlakke verpakking slechts) hoe te plaats en levering over de volledige vlucht:

* *[!UICONTROL Even]:* Plaatst gelijkmatig levering door elke vlucht, met een doel van 50% van de levering in de eerste helft van de vlucht.

* *[!UICONTROL Slightly Ahead]:* (het gebrek) versnelt levering zodat het 55-65% volledig halverwege de vluchtduur is.

* *[!UICONTROL Frontload]:* versnelt levering zodat het 65-75% volledig halverwege de vlucht is.

* *[!UICONTROL Aggressive Frontload]:* versnelt levering zodat het 75-85% volledig halverwege de vlucht is.

**[!UICONTROL Intraday pacing]:** (Pakketten met pakket-vlakke verpakking slechts) hoe te plaats en levering over elke dag binnen de vlucht:

* *[!UICONTROL Even]:* (het gebrek) schalen levering op inventarisbeschikbaarheid wordt gebaseerd die. Over het algemeen worden meer advertenties overdag per uur geleverd, wanneer het veilingsvolume hoger is en er minder advertenties &#39;s ochtends en &#39;s avonds worden geleverd.

* *[!UICONTROL ASAP]:* versnelt levering aan tweemaal de snelheid van *Even*.

  >[!CAUTION]
  >
  >Deze optie kan de prestaties negatief beïnvloeden. Gebruik dit alleen als u volledige prioriteit geeft aan levering en meer geld besteedt aan optimalisatie van prestaties.

## [!UICONTROL Flighting]

(Pakketten met pakketniveau-pakket) De vliegperioden van het pakket, inclusief aangepaste vliegperioden binnen de totale [!UICONTROL Flight Dates] voor het pakket. U kunt aangepaste vluchten alleen configureren wanneer de optie [!UICONTROL Activate Custom Flighting] is ingeschakeld in de sectie [!UICONTROL Goals & Budget] .

**[!UICONTROL Automatically rollover remaining flight budget to next flight]:** (Beschikbaar slechts wanneer de [!UICONTROL Activate Custom Flighting] optie wordt toegelaten) voegt automatisch om het even welk resterend budget van de vorige vlucht aan het bestaande budget voor de volgende vlucht toe.

In de [!UICONTROL Packages] -weergave en de [!DNL Package Name] > [!UICONTROL Flights] -weergave bevat het [!UICONTROL Interval Goal] -veld, waarin het huidige vliegdoel wordt weergegeven, een eventuele rolloverbegroting.

**[!DNL Flight N]:** (Beschikbaar slechts wanneer de [!UICONTROL Activate Custom Flighting] optie) wordt toegelaten) voor elke vlucht, specificeer de begindatum, de einddatum, en het doel besteedt doel. Klik op **[!UICONTROL Add Flight]** als u nog een vlucht wilt toevoegen.

Voor bestaande pakketten zonder ingeschakelde optie &quot;[!UICONTROL Automatically rollover remaining flight budget to next flight]&quot;, kunt u naar keuze de montages heropenen om een waarde in de **[!UICONTROL Rollover]** kolom voor om het even welke vlucht in te gaan om potentieel onuitgegeven budget aan de volgende vlucht toe te voegen.

>[!MORELIKETHIS]
>
>* [ Ongeveer het Beheer van het Pakket ](package-about.md)
>* [ creeer een Pakket ](package-create.md)
>* [ geef een Pakket ](package-edit.md) uit
>* [ maak een Plaatsing aan een Pakket ](package-attach-placement.md) vast
>* [ Mening het Logboek van de Verandering voor een Pakket ](package-change-log.md)
>* [ Veelgestelde vragen over Campaign Management ](/help/dsp/campaign-management/faq-campaign-management.md)
