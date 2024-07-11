---
title: Pakketinstellingen
description: Zie beschrijvingen van de beschikbare pakketinstellingen.
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: ab3118901b7cd88776f7c0ce8038b928118a7555
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# Pakketinstellingen

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** De pakketnaam. De maximumlengte is 60 tekens.

**[!UICONTROL Description]:** (Optioneel) Een beschrijving van het pakket.

**[!UICONTROL 3rd Party Billed Fees]:** (Optioneel) Een statische vergoeding voor derden die als niet-factureerbare kosten moet worden bijgehouden:

* **[!UICONTROL CPM]:** De kosten per 1000 impressies (CPM).

* **[!UICONTROL Description]:** Een beschrijving van de CPM-vergoeding.

>[!NOTE]
>
>Facultatieve vergoedingen worden weerspiegeld in de [!UICONTROL Net CPM] metrisch.

U kunt de instelling op pakketniveau overschrijven in het dialoogvenster [plaatsingsniveau](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Alleen-lezen voor bestaande pakketten) Op welk niveau moet de plaatsing van de verpakking worden geplaatst en gelimiteerd:

* **[!UICONTROL Package level pacing]:** Deze pakketstrategie werkt door alle inbegrepen plaatsingen als een pakket te plaatsen en te begrenzen *groep*. Deze strategie zorgt ervoor dat alle plaatsingen binnen een bepaald pakket holistisch worden geoptimaliseerd, waarbij uitgaven op basis van prestaties en schaal worden verdeeld naar geselecteerde prestatiekernindicatoren (KPI&#39;s).

* **[!UICONTROL Placement level pacing]:**  Deze pakketstrategie werkt door alle meegeleverde plaatsingen te plaatsen en te begrenzen *individueel*. De beste praktijk is om deze strategie alleen te gebruiken om gegarandeerde transacties op de particuliere markt uit te voeren.

**[!UICONTROL Flight Dates]:** De algemene begindatum en einddatum van het pakket. De vluchtdata moeten worden opgenomen in de vluchtdata voor de campagne.

>[!NOTE]
>
>* De vluchtdata voor alle plaatsen die aan dit pakket zijn toegewezen, moeten binnen deze data worden opgenomen.
> * U kunt de begindatum van het pakket niet bewerken wanneer aangepaste flighting wordt geactiveerd.

**[!UICONTROL Activate Custom Flighting]:** Hiermee kunt u vaste vluchten maken voor het pakket in het dialoogvenster [!UICONTROL Flighting] hieronder. Nadat u aangepaste flighting hebt ingeschakeld en het pakket hebt opgeslagen, kunt u aangepaste flighting niet uitschakelen en de begindatum van het pakket niet meer bewerken.

**[!UICONTROL Budget]:** (Pakketten met alleen pakketniveau) Het bruto-begrotingsmaximum en het begrotingsinterval.

Voor pakketten met aangepaste flighting is de budgetinterval altijd *[!UICONTROL All time]*. Geef voor pakketten zonder aangepaste markering de budgetinterval op: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* of *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Pakketten met alleen pakketniveau en dynamisch margebeheer) Het bruto-begrotingsmaximum voor de duur van het pakket.

**[!UICONTROL Optimization Goal]:** (Pakketten met alleen pakketniveau) Het optimalisatiedoel voor het pakket. Zie beschrijvingen van elk optimalisatiedoel op [Optimalisatiedoelstellingen en hoe deze te gebruiken](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]:** (Verpakt met &quot;[!UICONTROL Highest Return on Ad Spend]&quot; en &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;uitsluitend optimalisatiedoelstellingen&quot; A [aangepast doel](/help/dsp/optimization/custom-goal.md) die de opbrengsten of conversiegebeurtenissen omvat die worden gebruikt om de metrische waarde van de CPA of ROAS te berekenen. Het aangepaste doel kan desgewenst extra gewogen gebeurtenissen met de bovenste funnel (zoals paginabezoeken en winkelwagentoevoegingen) omvatten die naast de CPA of ROAS-metrische gegevens voor pakketoptimalisatie worden gebruikt. Voor meer informatie over douanedoelstellingen, met inbegrip van de beste praktijken voor het creëren voor douanedoelstellingen en campagnes die hen gebruiken, zie &quot;[Aangepaste doelen](/help/dsp/optimization/custom-goal.md)&quot; en &quot;[Beste praktijken voor de Campagnes van Prestaties van de Opstelling](/help/dsp/optimization/campaign-best-practices-performance.md).&quot;<!-- At some point, all of the objectives will be prefixed with "ADSP_," but probably that won't show up in the Custom Goal list in the DSP UI. -->

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** (Optioneel); pakketten met de &quot;[!UICONTROL Highest Return on Ad Spend]&quot; en &quot;[!UICONTROL Lowest Cost per Acquisition]De &quot;optimalisatiedoelstellingen slechts) vertelt het optimalisatiemodel om slechts van op klik-gebaseerde omzettingen te leren. Anders leert het optimalisatiemodel van zowel klik- als op indruk gebaseerde omzettingen.

**[!UICONTROL Conversion Metric]:** (Optioneel); pakketten met de &quot;[!UICONTROL Highest Return on Ad Spend]&quot; en &quot;[!UICONTROL Lowest Cost per Acquisition]&quot;alleen optimalisatiedoelstellingen) De laatste conversiegebeurtenis (zoals abonnementen) of het bedrag aan inkomstengebeurtenis/verkoop (zoals aankoop- en aankoopwaarden) die moet worden gebruikt voor het berekenen van het rendement op advertentie-uitgaven of de kosten per aankoop. Selecteer een optie in de lijst met alle primaire gebeurtenissen (&quot;doelmetriek&quot;) die aan het geselecteerde aangepaste doel zijn toegewezen. Als de lijst leeg is, dan geef het douanedoel uit om minstens één van de onderliggende gebeurtenissen als doel metrisch te omvatten.

**[!UICONTROL Package Goal Type]:** (Pakketten met alleen aangepaste optimalisatiedoelen) Het doel van het pakket. Met deze instelling kunt u bepalen hoe het pakket moet worden geoptimaliseerd:

* *[!UICONTROL Prospecting]:* Pakketten met vooruitzichten zijn gericht op het aanschaffen van nieuwe klanten.

* *[!UICONTROL Retargeting]:* Bij het opnieuw samenstellen van pakketten worden eerdere bezoekers of klanten opnieuw belicht.

* *[!UICONTROL Other]:* Alle andere doeleinden.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Pakketten met alleen aangepaste optimalisatiedoelen) Een ander pakket waarvan de historische gegevens worden gebruikt als invoer voor het optimaliseren van het pakket.

**[!UICONTROL Target]:** (Pakketten met pakket-vlakke het verpakken slechts) het doeldoel, dat wordt gebruikt om prestaties te volgen.

>[!NOTE]
>
>Dit veld is alleen een benchmark en wordt niet gebruikt voor beslissingen.

**[!UICONTROL Frequency Cap]:** (Pakketten met alleen pakketniveau) Het aantal keren dat een uniek apparaat, een universele id of een persoon (afhankelijk van het opgegeven [!UICONTROL Cross Device Level] voor de campagne en de plaatsing [!UICONTROL Targeting] (instellen) kan advertenties vanuit het pakket worden aangeboden. Opties omvatten *[!UICONTROL Unlimited]* of een specifiek bedrag per dag, week of maand.

>[!NOTE]
>
>* U kunt frequentiecappen instellen op campagne-, pakket- en plaatsingsniveaus. DSP respecteert de strengste frequentiegrens in de campagnehiërarchie.
>* De beste praktijken zijn het vaststellen van frequentiecappen voor zowel prospectie als herbestemming op pakketniveau.
> * Hogere frequentiecaps resulteren in hogere uitgaven en indrukken, maar in een lager bereik. Lagere frequentiecaps resulteren in minder uitgaven en indrukken, maar in een hoger bereik.

**[!UICONTROL Pace on]:** (Pakketten met alleen pakketniveau) Waarop de verpakking is gebaseerd:

* *[!UICONTROL Budget]:* (Standaard) Met deze optie krijgt u zoveel mogelijk indruk binnen het toegewezen pakketbudget.

* *[!UICONTROL Impressions]:* Met deze optie worden afbeeldingen afgedrukt totdat een opgegeven hoeveelheid binnen een opgegeven interval wordt bereikt. Wanneer u deze optie selecteert, geeft u het aantal afbeeldingen en het interval op: *Alle tijd,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* of *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Pakketten met alleen pakketniveau) Hoe plaats en levering over de volledige vlucht:

* *[!UICONTROL Even]:* Plaatst de levering op dezelfde wijze gedurende elke vlucht, met als doel 50% van de levering in de eerste helft van de vlucht.

* *[!UICONTROL Slightly Ahead]:* (De standaardwaarde) versnelt de levering zodat deze 55-65% volledig halverwege de vliegduur is.

* *[!UICONTROL Frontload]:* Versnelt de levering, zodat deze 65-75% volledig is halverwege de vlucht.

* *[!UICONTROL Aggressive Frontload]:* Versnelt levering zodat het 75-85% volledig halverwege de vlucht is.

**[!UICONTROL Intraday pacing]:** (Pakketten met alleen pakketniveau) Hoe plaats en levering elke dag binnen de vlucht:

* *[!UICONTROL Even]:* (De standaardinstelling) Schaalt de levering op basis van de beschikbaarheid van de voorraad. Over het algemeen worden meer advertenties overdag per uur geleverd, wanneer het veilingsvolume hoger is en er minder advertenties &#39;s ochtends en &#39;s avonds worden geleverd.

* *[!UICONTROL ASAP]:* Versnelt levering aan tweemaal de snelheid van *Gelijk*.

  >[!CAUTION]
  >
  >Deze optie kan de prestaties negatief beïnvloeden. Gebruik dit alleen als u volledige prioriteit geeft aan levering en meer geld besteedt aan optimalisatie van prestaties.

## [!UICONTROL Flighting]

(Pakketten met pakketniveau-interval) De vliegperioden van het pakket, met inbegrip van aangepaste vliegperioden binnen het totaal [!UICONTROL Flight Dates] voor het pakket. U kunt aangepaste vluchten alleen configureren wanneer de [!UICONTROL Activate Custom Flighting] optie is ingeschakeld in het dialoogvenster [!UICONTROL Goals & Budget] sectie.

**[!DNL Flight N]:** (Alleen beschikbaar als de [!UICONTROL Activate Custom Flighting] (optie is ingeschakeld) Geef voor elke vlucht de startdatum, einddatum en het doel voor de uitgave op. Als u nog een vlucht wilt toevoegen, klikt u op **[!UICONTROL Add Flight]**.

Voor bestaande pakketten kunt u desgewenst een waarde invoeren in het dialoogvenster [!UICONTROL Rollover] kolom voor elke vlucht om het potentiële niet-bestede budget toe te voegen aan de volgende vlucht. De geprojecteerde waarde in de [!UICONTROL Adjusted Goal (Goal + Rollover)] wordt de kolom dienovereenkomstig gewijzigd.<!-- clarify usage -->

>[!MORELIKETHIS]
>
>* [Info over Pakketbeheer](package-about.md)
>* [Een pakket maken](package-create.md)
>* [Een pakket bewerken](package-edit.md)
>* [Een plaatsing koppelen aan een pakket](package-attach-placement.md)
>* [Het Wijzigingslogboek voor een pakket weergeven](package-change-log.md)
>* [Veelgestelde vragen over Campaign Management](/help/dsp/campaign-management/faq-campaign-management.md)
