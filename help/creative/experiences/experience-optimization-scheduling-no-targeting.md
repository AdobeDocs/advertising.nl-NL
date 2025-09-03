---
title: Creatieve optimalisatie en planning aanpassen voor een ervaring
description: Leer hoe u
feature: Creative Experiences
exl-id: 9398df69-6a48-4b72-8c5c-a79341bf3b8a
source-git-commit: a271589a2cb51ec50c37a52254fd8d1b535f279a
workflow-type: tm+mt
source-wordcount: '1146'
ht-degree: 0%

---

# Aanpassen van creatieve optimalisatie en planning voor een ervaring zonder doelgericht gebruik van beslissingsstructuren

*Ervaringen met bestaande slechts creatieve*

Standaard wordt de creatieve rotatie voor een advertentie-ervaringstag op algoritmische wijze bepaald om de algemene doorklikfrequentie te optimaliseren, en de instellingen voor creatieve optimalisatie zijn van toepassing op alle toegewezen creatieve creatieven. U kunt de creatieve rotatie aanpassen om de creatieve creatieven handmatig op basis van relatieve gewichten uit te voeren of u kunt de creatieve rotatie op algoritmische wijze optimaliseren voor een opgegeven aangepaste Advertising DSP-doelstelling. U kunt ook specifieke creatieve projecten plannen die tijdens opgegeven opeenvolgende tijdsperioden worden uitgevoerd en aangepaste instellingen voor creatieve rotatie toepassen voor elk programma.

## Creatieve optimalisatie configureren zonder planning

Wanneer creatieve planning is uitgeschakeld, gelden de instellingen voor creatieve optimalisatie voor alle toegewezen creatieve projecten.

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Experiences]** .

1. Voer een van de volgende handelingen uit:

   * Klik in de kaartweergave op **[!UICONTROL ...]** naast de naam van de ervaring en klik vervolgens op **[!UICONTROL Tag Manager]** .

   * Houd in de tabelweergave de cursor boven de rij, klik op **[!UICONTROL More]** en klik vervolgens op **[!UICONTROL Tag Manager]** .

1. Houd de curseur over de rij voor de toepasselijke advertentietag en klik ![ het Programma van de Toevoegen ](/help/creative/assets/edit-gray.png " het volgen URLs ") **[!UICONTROL Creative Optimization]** uitgeven.&lt;!— Tagbeheer heeft alleen een lijstweergave, maar geen kaartweergave, vanaf 2/2. >

1. Schakel **[!UICONTROL Schedule]** uit.

1. Selecteer het type creatieve rotatie:

   * *[!UICONTROL Weighted]:* roteert de creatieve elementen handmatig op basis van relatieve gewichten. Voer het gewicht voor elke creatieve waarde in als een percentage. De gewichten voor alle geselecteerde creatieve elementen moeten optellen tot 100.

   * *[!UICONTROL Algorithmic]:* roteert de creatieve producten algoritmisch volgens een gespecificeerd optimalisatiedoel.

      * Selecteer **[!UICONTROL Optimization Goal]** (standaardvideo en -ervaringen) *[!UICONTROL Click Through Rate]* of *[!UICONTROL Completion Rate]* voor de *[!UICONTROL Custom Objective]* .  Als u *[!UICONTROL Custom Objective]* selecteert, dan een bestaand [ douanedoel van Advertising DSP ](/help/dsp/optimization/custom-goal.md) selecteert.<!-- Verify -->

   * *[!UICONTROL Sequencing]:* roteert de bijbehorende creatieve bundels in een gespecificeerde orde (met Bundel 1 het eerst, Bundel 2 het tweede, etc.), met een gespecificeerd totaal aantal indrukkingen over elke bundelopeenvolging. De advertentiegrootten die worden gediend worden bepaald door de beschikbare inventaris. U kunt de definitieve bundel in de opeenvolging vormen aan a \) voor onbepaalde tijd (het gebrek) of b \) lijn terug naar de eerste bundel worden getoond. U kunt bijvoorbeeld een van de creatieve elementen in Bundel 1 weergeven voor drie (3) indrukken, vervolgens een creatieve afbeelding weergeven in Bundel 2 voor één (1) indruk, vervolgens een van de creatieve elementen weergeven in Bundel 3 voor twee (2) indrukken en vervolgens de lus opnieuw beginnen. Als de creatieve elementen in Bundel 3 eenmaal zijn weergegeven, kunt u de creatieve elementen ook in de toekomst in Bundel 3 weergeven, in plaats van een lus te maken. Wanneer u het rangschikken inschakelt:

      1. Sleep de toegewezen bundels naar de gewenste volgorde.

     Standaard worden de toegewezen bundels gerangschikt in de volgorde waarin ze aan de ervaring zijn toegevoegd.

      1. Voer het aantal afbeeldingen voor elke reeks in.

      1. Voor de laatste opeenvolging, verander of aan a\) de definitieve bundel in de opeenvolging voor onbepaalde tijd (*[!UICONTROL Infinite]* (het gebrek) of b\) lijn terug naar de eerste bundel na de definitieve bundel wordt getoond (*[!UICONTROL Keep in Loop]*).

1. Klik op **[!UICONTROL Save]**.

## Creatieve optimalisatie configureren met creatieve planning

U kunt desgewenst specifieke creatieve instellingen plannen die worden gebruikt voor een advertentietolk en die worden uitgevoerd tijdens opgegeven opeenvolgende tijdsperioden tussen de begin- en einddatum van de ervaring, en aangepaste creatieve rotatie-instellingen toepassen voor elk programma. U kunt bijvoorbeeld plannen dat Creative 1 gedurende de eerste twee weken wordt uitgevoerd om de doorklikfrequentie te optimaliseren en Creative 2 gedurende de volgende twee weken om te optimaliseren voor een bepaald aangepast doel.

Wanneer u het plannen gebruikt, moet u creatieve middelen door de duur van de ervaring plannen.

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Experiences]** .

1. Voer een van de volgende handelingen uit:

   * Klik in de kaartweergave op **[!UICONTROL ...]** naast de naam van de ervaring en klik vervolgens op **[!UICONTROL Tag Manager]** .

   * Houd in de tabelweergave de cursor boven de rij, klik op **[!UICONTROL More]** en klik vervolgens op **[!UICONTROL Tag Manager]** .

1. Houd de curseur over de rij voor de toepasselijke advertentietag en klik ![ het Programma van de Toevoegen ](/help/creative/assets/edit-gray.png " het volgen URLs ") **[!UICONTROL Creative Optimization]** uitgeven. <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— Tagbeheer heeft alleen een lijstweergave, maar geen kaartweergave, vanaf 2/2. >

1. Schakel **[!UICONTROL Schedule]** in.

1. Voor het eerste schema:

   1. Schakel in de linkerkolom het selectievakje naast elke creatieve waarde in om aan het eerste schema toe te voegen.

   1. Geef de begin- en einddatum voor het schema op.

   1. Selecteer het type creatieve rotatie:

      * *[!UICONTROL Weighted]:* roteert de creatieve elementen handmatig op basis van relatieve gewichten. Voer het gewicht voor elke creatieve waarde in als een percentage. De gewichten voor alle geselecteerde creatieve elementen moeten optellen tot 100.

      * *[!UICONTROL Algorithmic]:* roteert de creatieve producten algoritmisch volgens een gespecificeerd optimalisatiedoel.

         * Selecteer **[!UICONTROL Optimization Goal]** (standaardvideo en -ervaringen) *[!UICONTROL Click Through Rate]* of *[!UICONTROL Completion Rate]* voor de *[!UICONTROL Custom Objective]* .  Als u *[!UICONTROL Custom Objective]* selecteert, dan een bestaand [ douanedoel van Advertising DSP ](/help/dsp/optimization/custom-goal.md) selecteert.<!-- Verify -->

      * *[!UICONTROL Sequencing]:* roteert de bijbehorende creatieve bundels in een gespecificeerde orde (met Bundel 1 het eerst, Bundel 2 het tweede, etc.), met een gespecificeerd totaal aantal indrukkingen over elke bundelopeenvolging. De advertentiegrootten die worden gediend worden bepaald door de beschikbare inventaris. U kunt de definitieve bundel in de opeenvolging vormen aan a \) voor onbepaalde tijd (het gebrek) of b \) lijn terug naar de eerste bundel worden getoond. U kunt bijvoorbeeld een van de creatieve elementen in Bundel 1 weergeven voor drie (3) indrukken, vervolgens een creatieve afbeelding weergeven in Bundel 2 voor één (1) indruk, vervolgens een van de creatieve elementen weergeven in Bundel 3 voor twee (2) indrukken en vervolgens de lus opnieuw beginnen. Als de creatieve elementen in Bundel 3 eenmaal zijn weergegeven, kunt u de creatieve elementen ook in de toekomst in Bundel 3 weergeven, in plaats van een lus te maken. Wanneer u het rangschikken inschakelt:

         1. Sleep de toegewezen bundels naar de gewenste volgorde.

            Standaard worden de toegewezen bundels gerangschikt in de volgorde waarin ze aan de ervaring zijn toegevoegd.

         1. Voer het aantal afbeeldingen voor elke reeks in.

         1. Voor de laatste opeenvolging, verander of aan a\) de definitieve bundel in de opeenvolging voor onbepaalde tijd (*[!UICONTROL Infinite]* (het gebrek) of b\) lijn terug naar de eerste bundel na de definitieve bundel wordt getoond (*[!UICONTROL Keep in Loop]*).

1. Voor elk aanvullend schema:

   1. Klik op **[!UICONTROL + Add Schedule]**.

   1. Schakel in de linkerkolom het selectievakje naast elke creatieve waarde in om aan het eerste schema toe te voegen.

   1. Geef de begin- en einddatum voor het schema op.

   1. Selecteer het type creatieve rotatie:

      * *[!UICONTROL Weighted]:* roteert de creatieve elementen handmatig op basis van relatieve gewichten. Voer het gewicht voor elke creatieve waarde in als een percentage. De gewichten voor alle geselecteerde creatieve elementen moeten optellen tot 100.

      * *[!UICONTROL Algorithmic]:* roteert de creatieve producten algoritmisch volgens een gespecificeerd optimalisatiedoel.

         * Selecteer voor de **[!UICONTROL Optimization Goal]** de optie *[!UICONTROL Click Through Rate]* of *[!UICONTROL Custom Objective]* .  Als u *[!UICONTROL Custom Objective]* selecteert, dan een bestaand [ douanedoel van Advertising DSP ](/help/dsp/optimization/custom-goal.md) selecteert.<!-- Verify -->

      * *[!UICONTROL Sequencing]:* roteert de bijbehorende creatieve bundels in een gespecificeerde orde, met een gespecificeerd totaal aantal beelden over elke bundelopeenvolging. Wanneer u het rangschikken inschakelt:

         1. Sleep de toegewezen bundels naar de gewenste volgorde.

            Standaard worden de toegewezen bundels gerangschikt in de volgorde waarin ze aan de ervaring zijn toegevoegd.

         1. Voer het aantal afbeeldingen voor elke reeks in.

         1. Voor de laatste opeenvolging, verander of aan a\) de definitieve bundel in de opeenvolging voor onbepaalde tijd (*[!UICONTROL Infinite]* (het gebrek) of b\) lijn terug naar de eerste bundel na de definitieve bundel wordt getoond (*[!UICONTROL Keep in Loop]*).

1. Klik op **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [ creeer manueel een ad markering voor een toepasselijke creatieve grootte ](/help/creative/experiences/experience-tag-create-manually.md)
>* [ wijs creatieve elementen aan een ad markering voor ervaringen toe zonder zich te richten ](experience-tag-assign-creatives.md)
>* [ pas het volgen URLs voor een ervaring zonder beslissingsboom aan richtend ](experience-tracking-urls-no-targeting.md)
