---
title: Creatieve optimalisatie en planning aanpassen voor een ervaring
description: Leer hoe u
feature: Creative Experiences
exl-id: 9398df69-6a48-4b72-8c5c-a79341bf3b8a
source-git-commit: 4d0f4b2a46a65c7fa1afec0a4ef419e58b8f8f59
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Aanpassen van creatieve optimalisatie en planning voor een ervaring zonder doelgericht gebruik van beslissingsstructuren

*Ervaringen met bestaande slechts creatieve*
*Gesloten bèta*

Standaard wordt de creatieve rotatie voor een advertentie-ervaringstag op algoritmische wijze bepaald om de algemene doorklikfrequentie te optimaliseren, en de instellingen voor creatieve optimalisatie zijn van toepassing op alle toegewezen creatieve creatieven. U kunt de creatieve rotatie aanpassen om de creatieve creatieven handmatig op basis van relatieve gewichten uit te voeren of u kunt de creatieve rotatie op algoritmische wijze optimaliseren voor een opgegeven aangepaste Advertising DSP-doelstelling. <!-- verify --> U kunt ook specifieke creatieve projecten plannen die tijdens opgegeven opeenvolgende tijdsperioden worden uitgevoerd en aangepaste instellingen voor creatieve rotatie toepassen voor elk programma.

## Creatieve optimalisatie configureren zonder planning

Wanneer creatieve planning is uitgeschakeld, gelden de instellingen voor creatieve optimalisatie voor alle toegewezen creatieve projecten.

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Experiences]** .

1. Voer een van de volgende handelingen uit:

   * Klik in de kaartweergave op **[!UICONTROL ...]** naast de naam van de ervaring en klik vervolgens op **[!UICONTROL Tag Manager]** .

   * Houd in de tabelweergave de cursor boven de rij, klik op **[!UICONTROL More]** en klik vervolgens op **[!UICONTROL Tag Manager]**

1. Houd de curseur over de rij voor de toepasselijke advertentietag en klik ![ het Programma van de Toevoegen ](/help/creative/assets/edit-gray.png " het volgen URLs ") **[!UICONTROL Ad Schedule]** uitgeven. <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— Tagbeheer heeft alleen een lijstweergave, maar geen kaartweergave, vanaf 2/2. >

1. Schakel **[!UICONTROL Schedule]** uit.

1. Selecteer het type creatieve rotatie:

   * &amp;ast;&amp;ast; *Gewogen* &amp;ast;&amp;ast; — roteert de creatieve producten manueel volgens relatieve gewichten. Voer het gewicht voor elke creatieve waarde in als een percentage. De gewichten voor alle geselecteerde creatieve elementen moeten optellen tot 100.

   * &amp;ast;&amp;ast; *Algorithmic* &amp;ast;&amp;ast; — Roteert de creatieve elementen algoritmisch volgens een gespecificeerd optimalisatiedoel.

      * Selecteer voor de **[!UICONTROL Optimization Goal]** de optie *[!UICONTROL Click Through Rate]* of *[!UICONTROL Custom Objective]* .  Als u *[!UICONTROL Custom Objective]* selecteert, dan een bestaand [ douanedoel van Advertising DSP ](/help/dsp/optimization/custom-goal.md) selecteert.<!-- Verify -->

1. Klik op **[!UICONTROL Save]**.

## Creatieve optimalisatie configureren met creatieve planning

U kunt desgewenst specifieke creatieve instellingen plannen die worden gebruikt voor een advertentietolk en die worden uitgevoerd tijdens opgegeven opeenvolgende tijdsperioden tussen de begin- en einddatum van de ervaring, en aangepaste creatieve rotatie-instellingen toepassen voor elk programma. U kunt bijvoorbeeld plannen dat Creative 1 tijdens de eerste twee weken wordt uitgevoerd om de doorklikfrequentie te optimaliseren en Creative 2 gedurende de volgende twee weken om te optimaliseren voor een bepaald doel.

Wanneer u het plannen gebruikt, moet u creatieve middelen door de duur van de ervaring plannen.

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Experiences]** .

1. Voer een van de volgende handelingen uit:

   * Klik in de kaartweergave op **[!UICONTROL ...]** naast de naam van de ervaring en klik vervolgens op **[!UICONTROL Tag Manager]** .

   * Houd in de tabelweergave de cursor boven de rij, klik op **[!UICONTROL More]** en klik vervolgens op **[!UICONTROL Tag Manager]**

1. Houd de curseur over de rij voor de toepasselijke advertentietag en klik ![ het Programma van de Toevoegen ](/help/creative/assets/edit-gray.png " het volgen URLs ") **[!UICONTROL Ad Schedule]** uitgeven. <!-- For targeted experiences, this is "Edit Schedules" -->&lt;!— Tagbeheer heeft alleen een lijstweergave, maar geen kaartweergave, vanaf 2/2. >

1. Schakel **[!UICONTROL Schedule]** in.

1. Voor het eerste schema:

   1. Schakel in de linkerkolom het selectievakje naast elke creatieve waarde in om aan het eerste schema toe te voegen.

   1. Geef de begin- en einddatum voor het schema op.

   1. Selecteer het type creatieve rotatie:

      * &amp;ast;&amp;ast; *Gewogen* &amp;ast;&amp;ast; — roteert de creatieve producten manueel volgens relatieve gewichten. Voer het gewicht voor elke creatieve waarde in als een percentage. De gewichten voor alle geselecteerde creatieve elementen moeten optellen tot 100.

      * &amp;ast;&amp;ast; *Algorithmic* &amp;ast;&amp;ast; — Roteert de creatieve elementen algoritmisch volgens een gespecificeerd optimalisatiedoel.

         * Selecteer voor de **[!UICONTROL Optimization Goal]** de optie *[!UICONTROL Click Through Rate]* of *[!UICONTROL Custom Objective]* .  Als u *[!UICONTROL Custom Objective]* selecteert, dan een bestaand [ douanedoel van Advertising DSP ](/help/dsp/optimization/custom-goal.md) selecteert.<!-- Verify -->

1. Voor elk aanvullend schema:

   1. Klik op **[!UICONTROL + Add Schedule]**.

   1. Schakel in de linkerkolom het selectievakje naast elke creatieve waarde in om aan het eerste schema toe te voegen.

   1. Geef de begin- en einddatum voor het schema op.

   1. Selecteer het type creatieve rotatie:

      * &amp;ast;&amp;ast; *Gewogen* &amp;ast;&amp;ast; — roteert de creatieve producten manueel volgens relatieve gewichten. Voer het gewicht voor elke creatieve waarde in als een percentage. De gewichten voor alle geselecteerde creatieve elementen moeten optellen tot 100.

      * &amp;ast;&amp;ast; *Algorithmic* &amp;ast;&amp;ast; — Roteert de creatieve elementen algoritmisch volgens een gespecificeerd optimalisatiedoel.

         * Selecteer voor de **[!UICONTROL Optimization Goal]** de optie *[!UICONTROL Click Through Rate]* of *[!UICONTROL Custom Objective]* .  Als u *[!UICONTROL Custom Objective]* selecteert, dan een bestaand [ douanedoel van Advertising DSP ](/help/dsp/optimization/custom-goal.md) selecteert.<!-- Verify -->

1. Klik op **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [ creeer manueel een ad markering voor een toepasselijke creatieve grootte ](/help/creative/experiences/experience-tag-create-manually.md)
>* [ wijs creatieve elementen aan een ad markering voor ervaringen toe zonder zich te richten ](experience-tag-assign-creatives.md)
>* [ pas het volgen URLs voor een ervaring zonder beslissingsboom aan richtend ](experience-tracking-urls-no-targeting.md)
