---
title: Creatieve optimalisatie en planning aanpassen voor een ervaring
description: Leer hoe u
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
source-git-commit: a271589a2cb51ec50c37a52254fd8d1b535f279a
workflow-type: tm+mt
source-wordcount: '1073'
ht-degree: 0%

---

# Aanpassen van creatieve optimalisatie en planning voor een ervaring met beslissingsboomdoelen

*knopen van het Doel met bestaande slechts creatieve*

Standaard wordt de creatieve rotatie voor een ervaring op algoritmische wijze bepaald om de algemene doorkliksnelheid te optimaliseren, en de instellingen voor creatieve optimalisatie zijn van toepassing op alle toegewezen bundels. U kunt de creatieve rotatie aanpassen om de creatieve elementen in elke bundel handmatig uit te voeren voor een bepaald aangepast Advertising DSP-doel, volgens een opgegeven bundelreeks, met een opgegeven aantal indrukkingen in elke bundelreeks of volgens relatieve gewichten. U kunt ook specifieke creatieve bundels plannen die tijdens gespecificeerde, opeenvolgende tijdsperioden worden uitgevoerd en aangepaste creatieve rotatie-instellingen toepassen voor elk programma.

>[!NOTE]
>
>Deze functies zijn niet beschikbaar voor knooppunten die de standaardcreatieven gebruiken in plaats van toegewezen creatieven.

## Creatieve optimalisatie configureren zonder planning

Wanneer creatieve planning is uitgeschakeld, gelden de instellingen voor creatieve optimalisatie voor alle toegewezen creatieve projecten.

1. Plaats de cursor op het creatieve bladknooppunt onder het doelknooppunt en klik op **[!UICONTROL ...]** > **[!UICONTROL Creative Optimization]** .

1. Schakel **[!UICONTROL Schedule]** uit.

1. Selecteer het type creatieve rotatie:

   * *[!UICONTROL Weighted]:* roteert de creatieve elementen in elke bundel manueel volgens relatieve gewichten. Voer het gewicht van elke bundel in als een percentage. De gewichten voor alle bundels moeten optellen tot 100.

   * *[!UICONTROL Algorithmic]:* roteert de creatieve elementen in elke bundel algoritmisch volgens een gespecificeerd optimalisatiedoel.

      * Selecteer **[!UICONTROL Optimization Goal]** (standaardvideo en -ervaringen) *[!UICONTROL Click Through Rate]* of *[!UICONTROL Completion Rate]* voor de *[!UICONTROL Custom Objective]* .  Als u *[!UICONTROL Custom Objective]* selecteert, dan selecteer een bestaand [ douanedoel van Advertising DSP ](/help/dsp/optimization/custom-goal.md).

   * *[!UICONTROL Sequencing]:* roteert de bijbehorende creatieve bundels in een gespecificeerde orde (met Bundel 1 het eerst, Bundel 2 het tweede, etc.), met een gespecificeerd totaal aantal indrukkingen over elke bundelopeenvolging. De advertentiegrootten die worden gediend worden bepaald door de beschikbare inventaris. U kunt de definitieve bundel in de opeenvolging vormen aan a \) voor onbepaalde tijd (het gebrek) of b \) lijn terug naar de eerste bundel worden getoond. U kunt bijvoorbeeld een van de creatieve elementen in Bundel 1 weergeven voor drie (3) indrukken, vervolgens een creatieve afbeelding weergeven in Bundel 2 voor één (1) indruk, vervolgens een van de creatieve elementen weergeven in Bundel 3 voor twee (2) indrukken en vervolgens de lus opnieuw beginnen. Als de creatieve elementen in Bundel 3 eenmaal zijn weergegeven, kunt u de creatieve elementen ook in de toekomst in Bundel 3 weergeven, in plaats van een lus te maken. Wanneer u het rangschikken inschakelt:

      1. Sleep de toegewezen bundels naar de gewenste volgorde.

     Standaard worden de toegewezen bundels gerangschikt in de volgorde waarin ze aan de ervaring zijn toegevoegd.

      1. Voer het aantal afbeeldingen voor elke reeks in.

      1. Voor de laatste opeenvolging, verander of aan a\) de definitieve bundel in de opeenvolging voor onbepaalde tijd (*[!UICONTROL Infinite]* (het gebrek) of b\) lijn terug naar de eerste bundel na de definitieve bundel wordt getoond (*[!UICONTROL Keep in Loop]*).

1. Klik op **[!UICONTROL Save]**.

## Creatieve optimalisatie configureren met creatieve planning

U kunt desgewenst specifieke creatieve bundels plannen die tijdens gespecificeerde, opeenvolgende tijdsperioden tussen de ervaringsbegin en einddata worden uitgevoerd, en aangepaste creatieve rotatie-instellingen toepassen voor elk programma. U kunt bijvoorbeeld Bundel 1 plannen om gedurende de eerste twee weken te draaien voor optimalisatie voor doorklikfrequentie en Bundel 2 om gedurende de volgende twee weken te lopen voor een bepaald douanedoel.

Wanneer u het plannen gebruikt, moet u bundels door de duur van de ervaring plannen.

1. Plaats de cursor op het creatieve bladknooppunt onder het doelknooppunt en klik op **[!UICONTROL ...]** > **[!UICONTROL Creative Optimization]** .

1. Schakel **[!UICONTROL Schedule]** in.

1. Voor het eerste schema:

   1. Selecteer in de linkerkolom het selectievakje naast elke creatieve bundel die u aan het eerste schema wilt toevoegen.

   1. Geef de begin- en einddatum voor het schema op.

   1. Selecteer het type creatieve rotatie:

      * *[!UICONTROL Weighted]:* roteert de creatieve elementen in elke bundel manueel volgens relatieve gewichten. Voer het gewicht van elke bundel in als een percentage. De gewichten voor alle geselecteerde bundels moeten optellen tot 100.

      * *[!UICONTROL Algorithmic]:* roteert de creatieve elementen in elke bundel algoritmisch volgens een gespecificeerd optimalisatiedoel.

         * Selecteer **[!UICONTROL Optimization Goal]** (standaardvideo en -ervaringen) *[!UICONTROL Click Through Rate]* of *[!UICONTROL Completion Rate]* voor de *[!UICONTROL Custom Objective]* .  Als u *[!UICONTROL Custom Objective]* selecteert, dan selecteer een bestaand [ douanedoel van Advertising DSP ](/help/dsp/optimization/custom-goal.md).

      * *[!UICONTROL Sequencing]:* roteert de bijbehorende creatieve bundels in een gespecificeerde orde (met Bundel 1 het eerst, Bundel 2 het tweede, etc.), met een gespecificeerd totaal aantal indrukkingen over elke bundelopeenvolging. De advertentiegrootten die worden gediend worden bepaald door de beschikbare inventaris. U kunt de definitieve bundel in de opeenvolging vormen aan a \) voor onbepaalde tijd (het gebrek) of b \) lijn terug naar de eerste bundel worden getoond. U kunt bijvoorbeeld een van de creatieve elementen in Bundel 1 weergeven voor drie (3) indrukken, vervolgens een creatieve afbeelding weergeven in Bundel 2 voor één (1) indruk, vervolgens een van de creatieve elementen weergeven in Bundel 3 voor twee (2) indrukken en vervolgens de lus opnieuw beginnen. Als de creatieve elementen in Bundel 3 eenmaal zijn weergegeven, kunt u de creatieve elementen ook in de toekomst in Bundel 3 weergeven, in plaats van een lus te maken. Wanneer u het rangschikken inschakelt:

         1. Sleep de toegewezen bundels naar de gewenste volgorde.

            Standaard worden de toegewezen bundels gerangschikt in de volgorde waarin ze aan de ervaring zijn toegevoegd.

         1. Voer het aantal afbeeldingen voor elke reeks in.

         1. Voor de laatste opeenvolging, verander of aan a\) de definitieve bundel in de opeenvolging voor onbepaalde tijd (*[!UICONTROL Infinite]* (het gebrek) of b\) lijn terug naar de eerste bundel na de definitieve bundel wordt getoond (*[!UICONTROL Keep in Loop]*).

1. Voor elk aanvullend schema:

   1. Klik op **[!UICONTROL + Add Schedule]**.

   1. Selecteer in de linkerkolom het selectievakje naast elke creatieve bundel die u aan het eerste schema wilt toevoegen.

   1. Geef de begin- en einddatum voor het schema op.

   1. Selecteer het type creatieve rotatie:

      * *[!UICONTROL Weighted]:* roteert de creatieve elementen in elke bundel manueel volgens relatieve gewichten. Voer het gewicht van elke bundel in als een percentage. De gewichten voor alle geselecteerde bundels moeten optellen tot 100.

      * *[!UICONTROL Algorithmic]:* roteert de creatieve elementen in elke bundel algoritmisch volgens een gespecificeerd optimalisatiedoel.

         * Selecteer voor de **[!UICONTROL Optimization Goal]** de optie *[!UICONTROL Click Through Rate]* of *[!UICONTROL Custom Objective]* .  Als u *[!UICONTROL Custom Objective]* selecteert, dan selecteer een bestaand [ douanedoel van Advertising DSP ](/help/dsp/optimization/custom-goal.md).

      * *[!UICONTROL Sequencing]:* roteert de bijbehorende creatieve bundels in een gespecificeerde orde, met een gespecificeerd totaal aantal beelden over elke bundelopeenvolging. Wanneer u het rangschikken inschakelt:

         1. Sleep de toegewezen bundels naar de gewenste volgorde.

            Standaard worden de toegewezen bundels gerangschikt in de volgorde waarin ze aan de ervaring zijn toegevoegd.

         1. Voer het aantal afbeeldingen voor elke reeks in.

         1. Voor de laatste opeenvolging, verander of aan a\) de definitieve bundel in de opeenvolging voor onbepaalde tijd (*[!UICONTROL Infinite]* (het gebrek) of b\) lijn terug naar de eerste bundel na de definitieve bundel wordt getoond (*[!UICONTROL Keep in Loop]*).

1. Klik op **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [ wijs creatieve bundels aan een definitieve knoop in een ervaring toe en unassign ](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [ pas het volgen URLs voor creatieve personen ](/help/creative/experiences/experience-tracking-urls-targeting.md) aan
