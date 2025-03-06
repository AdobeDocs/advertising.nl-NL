---
title: Creatieve optimalisatie en planning aanpassen voor een ervaring
description: Leer hoe u
feature: Creative Experiences
exl-id: 47d1a249-decd-4c3b-ac88-260488d5bcd2
source-git-commit: 4abb83d08a6633c36aa47b5acd67df3d4cc0923b
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 0%

---

# Aanpassen van creatieve optimalisatie en planning voor een ervaring met beslissingsboomdoelen

*knopen van het Doel met bestaande slechts creatieve*
*Gesloten bèta*

Standaard wordt de creatieve rotatie voor een ervaring op algoritmische wijze bepaald om de algemene doorkliksnelheid te optimaliseren, en de instellingen voor creatieve optimalisatie zijn van toepassing op alle toegewezen bundels. U kunt de creatieve rotatie zodanig aanpassen dat de creatieve elementen in elke bundel handmatig worden uitgevoerd op basis van relatieve gewichten of dat ze op algoritmische wijze worden geoptimaliseerd voor een bepaald aangepast Advertising DSP-doel. U kunt ook specifieke creatieve bundels plannen die tijdens gespecificeerde, opeenvolgende tijdsperioden worden uitgevoerd en aangepaste creatieve rotatie-instellingen toepassen voor elk programma.

>[!NOTE]
>
>Deze functies zijn niet beschikbaar voor knooppunten die de standaardversie van de afbeelding gebruiken in plaats van toegewezen creatieven.

## Creatieve optimalisatie configureren zonder planning

Wanneer creatieve planning is uitgeschakeld, gelden de instellingen voor creatieve optimalisatie voor alle toegewezen creatieve projecten.

1. Plaats de cursor op het creatieve bladknooppunt onder het doelknooppunt en klik op **[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]** .

1. Schakel **[!UICONTROL Schedule]** uit.

1. Selecteer het type creatieve rotatie:

   * *[!UICONTROL Weighted]:* roteert de creatieve elementen in elke bundel manueel volgens relatieve gewichten. Voer het gewicht van elke bundel in als een percentage. De gewichten voor alle bundels moeten optellen tot 100.

   * *[!UICONTROL Algorithmic]:* roteert de creatieve elementen in elke bundel algoritmisch volgens een gespecificeerd optimalisatiedoel.

      * Selecteer voor de **[!UICONTROL Optimization Goal]** de optie *[!UICONTROL Click Through Rate]* of *[!UICONTROL Custom Objective]* .  Als u *[!UICONTROL Custom Objective]* selecteert, dan selecteer een bestaand [ douanedoel van Advertising DSP ](/help/dsp/optimization/custom-goal.md).

1. Klik op **[!UICONTROL Save]**.

## Creatieve optimalisatie configureren met creatieve planning

U kunt desgewenst specifieke creatieve bundels plannen die tijdens gespecificeerde, opeenvolgende tijdsperioden tussen de ervaringsbegin en einddata worden uitgevoerd, en aangepaste creatieve rotatie-instellingen toepassen voor elk programma. U kunt bijvoorbeeld Bundel 1 plannen om gedurende de eerste twee weken te draaien voor optimalisatie voor doorklikfrequentie en Bundel 2 om gedurende de volgende twee weken te lopen voor een bepaald douanedoel.

Wanneer u het plannen gebruikt, moet u bundels door de duur van de ervaring plannen.

1. Plaats de cursor op het creatieve bladknooppunt onder het doelknooppunt en klik op **[!UICONTROL ...]** > **[!UICONTROL Edit Schedules]** .

1. Schakel **[!UICONTROL Schedule]** in.

1. Voor het eerste schema:

   1. Selecteer in de linkerkolom het selectievakje naast elke creatieve bundel die u aan het eerste schema wilt toevoegen.

   1. Geef de begin- en einddatum voor het schema op.

   1. Selecteer het type creatieve rotatie:

      * *[!UICONTROL Weighted]:* roteert de creatieve elementen in elke bundel manueel volgens relatieve gewichten. Voer het gewicht van elke bundel in als een percentage. De gewichten voor alle geselecteerde bundels moeten optellen tot 100.

      * *[!UICONTROL Algorithmic]:* roteert de creatieve elementen in elke bundel algoritmisch volgens een gespecificeerd optimalisatiedoel.

         * Selecteer voor de **[!UICONTROL Optimization Goal]** de optie *[!UICONTROL Click Through Rate]* of *[!UICONTROL Custom Objective]* .  Als u *[!UICONTROL Custom Objective]* selecteert, dan selecteer een bestaand [ douanedoel van Advertising DSP ](/help/dsp/optimization/custom-goal.md).

1. Voor elk aanvullend schema:

   1. Klik op **[!UICONTROL + Add Schedule]**.

   1. Selecteer in de linkerkolom het selectievakje naast elke creatieve bundel die u aan het eerste schema wilt toevoegen.

   1. Geef de begin- en einddatum voor het schema op.

   1. Selecteer het type creatieve rotatie:

      * *[!UICONTROL Weighted]:* roteert de creatieve elementen in elke bundel manueel volgens relatieve gewichten. Voer het gewicht van elke bundel in als een percentage. De gewichten voor alle geselecteerde bundels moeten optellen tot 100.

      * *[!UICONTROL Algorithmic]:* roteert de creatieve elementen in elke bundel algoritmisch volgens een gespecificeerd optimalisatiedoel.

         * Selecteer voor de **[!UICONTROL Optimization Goal]** de optie *[!UICONTROL Click Through Rate]* of *[!UICONTROL Custom Objective]* .  Als u *[!UICONTROL Custom Objective]* selecteert, dan selecteer een bestaand [ douanedoel van Advertising DSP ](/help/dsp/optimization/custom-goal.md).

1. Klik op **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [ wijs creatieve bundels aan een definitieve knoop in een ervaring toe en unassign ](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [ pas het volgen URLs voor creatieve personen ](/help/creative/experiences/experience-tracking-urls-targeting.md) aan
