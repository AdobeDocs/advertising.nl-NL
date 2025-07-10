---
title: De indeling van de beslissingstructuur
description: Leer over de lay-out van de beslissingsboom voor ervaringen met het richten.
feature: Creative Experiences
exl-id: 1d997422-8177-4a6b-b56a-e1c742b96ad2
source-git-commit: 4b780760e5a7a0c3d370054fce8b1c15fbc6802d
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# De indeling van de beslissingsboomstructuur voor [!DNL Creative] ervaringen

*Gesloten bèta*

Wanneer u &quot;[!UICONTROL Targeting]&quot;optie voor een ervaring toelaat, plaatst u opstelling de ervaring gebruikend een beslissingsboom.

Aanvankelijk, begint elke beslissingsboom met het wortelniveau, &quot;allen.&quot; U kunt één of meerdere doelknopen toevoegen, en dan creatieve bundels toewijzen aan de definitieve knopen in elke tak van de beslissingsboom. Standaard wordt de beslissingsstructuur verticaal weergegeven, maar u kunt de structuur desgewenst horizontaal weergeven.

![ Voorbeeld van een verticale besluitvormingsboom zonder doelstellingen ](/help/creative/assets/experience-decision-tree-no-targets.png " Voorbeeld van een verticale besluitvormingsboom zonder doelstellingen ")

![ Voorbeeld van een horizontale besluitvormingsboom zonder doelstellingen ](/help/creative/assets/experience-decision-tree-no-targets-horizontal.png " Voorbeeld van een horizontale besluitvormingsboom zonder doelstellingen ")

<!--
>[!NOTE]
>
>You can optionally assign creative bundles to the root level, without targets. However, the [XXXX workflow](experience-create-no-targeting.md) XXXXX is better XXX.<!-- Explain the diff and why to choose the other option. -->
>—>

## Voorwaarden

**Boom:** de algemene beslissingsstructuur als boom met takken.

**Knoop van het Doel:** een doel binnen een tak.

**Knoop van het Blad:** een reeks creatieven die aan een definitieve doelknoop worden toegewezen.

## Streefcijfers in een beslissingsstructuur

Elke beslissingsboom kan tot vijf niveaus van doelstellingen hebben. Elk doelniveau kan meerdere vertakkingen bevatten, elk met een of meer knooppunten met hetzelfde doeltype (doelsegment, type geografische locatie, waarden voor opgegeven gegevensdoorvoersleutels, kenmerken voor een opgegeven herrichtingspixel of apparaatcategorie). U kunt creatieve bundels in elke advertentiegrootte toewijzen waarvoor u een standaardbeeld creatief of video creatief aan de laag-vlakke doelknopen hebt gespecificeerd.

![ Voorbeeld van een besluitvormingsboom met doelstellingen ](/help/creative/assets/experience-decision-tree.png " Voorbeeld van een besluitvormingsboom met doelstellingen ")

Wanneer u een doelknoop aan het definitieve niveau toevoegt, specificeert u het doel voor de nieuwe knoop. Een extra sibling knoop, &quot;Al Else,&quot;wordt automatisch gecreeerd voor iedereen die niet het gespecificeerde doel aanpast. U kunt dan extra sibling knopen met verschillende doelstellingen van het zelfde type toevoegen.

Wanneer u een doelknoop tussen bestaande niveaus opneemt, echter, wordt de eerste knoop voor het nieuwe niveau aanvankelijk toegewezen aan &quot;allen.&quot; Om een specifiek doel te identificeren, creeer een sibling doelknoop op het zelfde niveau, waarvoor u het daadwerkelijke doel specificeert. Met deze actie maakt u het doelknooppunt en vervangt u het knooppunt &quot;All&quot; door het knooppunt &quot;All Else&quot; (dat alle creatieve bundels bevat die eerder aan All zijn toegewezen). U kunt dan extra sibling knopen met verschillende doelstellingen van het zelfde type toevoegen.

Voor alle bovenliggende knooppunten kunt u optioneel alle onderliggende doelknooppunten en creatieve bundels kopiëren en deze in een ander knooppunt op hetzelfde niveau plakken. U kunt de geplakte knooppunten toevoegen aan het bestaande framework of het bestaande framework vervangen door deze knooppunten.

## Creatieve personen in een beslissingsstructuur

U kunt creatieve bundels toewijzen aan elk doelknooppunt in de ervaring.

Binnen elke knoop met creatieve bundels, kunt u naar keuze de inbegrepen creatieve creatieven of a) volgens gespecificeerde gewichten of b) algoritmisch roteren om de klikthrough tarief of een douanedoelstelling te optimaliseren. U kunt de creatieve elementen optioneel ook in een bepaalde tijdreeks roteren met dezelfde opties.

U kunt desgewenst de URL&#39;s van de bestemmingspagina, de URL&#39;s voor het bijhouden van de indruk en de URL&#39;s voor het bijhouden van de klikken aanpassen voor de afzonderlijke creatieve personen. <!-- Not in the UI as of 1/31: For flexible HTML5 creatives, you can customize any of the flexible attributes. -->

>[!MORELIKETHIS]
>
>* [ Ongeveer ervaringen in Advertising Creative 2.0 ](experience-about.md)
>* [ creeer een ervaring met het richten ](/help/creative/experiences/experience-create-targeting.md)
>* [ gerichte ervaringsmontages ](/help/creative/experiences/experience-settings-targeting.md)
