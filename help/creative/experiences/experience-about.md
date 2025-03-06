---
title: Ervaringen in Advertising Creative
description: Leer hoe u persoonlijke advertentie-ervaringen configureert en de ad-elementen optimaliseert op basis van prestaties.
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 0a6cd8e32ae87c7fda9ed0e1b50f9b54cd337192
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---

# Ervaringen in Advertising Creative 2.0

*Gesloten bèta*

<!-- Revisit Description metadata  -->

<!-- MORE -->

[!DNL Advertising Creative 2.0] verstrekt twee verschillende structuren van de advertentie voor de advertenties in een creatieve bibliotheek <!-- can use a single library only -->:

* **Ervaringen met beslissingsboom richtend:** [!DNL Creative] staat u toe om gepersonaliseerde ad ervaringen door de klantenreis te vormen gebruikend een model van de beslissingsboom. U kunt alle advertentie-elementen — afbeeldingen, koppen, aanbiedingen en bestemmingspagina&#39;s — aanpassen op basis van het doelpubliek.

  U kunt bijvoorbeeld dezelfde creatieve bundel opgeven voor mensen in Chicago en New York City die zich in een specifiek Adobe Analytics-publiekssegment bevinden, maar mensen in Chicago naar andere bestemmingspagina&#39;s sturen dan New Yorkers. U kon een verschillende bundel voor mensen in het segment ook specificeren die overal behalve Chicago en de Stad van New York wonen, en een derde bundel voor andere mensen die niet in het segment zijn.

  De volgende doelopties zijn beschikbaar:

   * Uw eersteklas publiekssegmenten van Adobe Audience Manager, Adobe Analytics en Advertising Cloud DSP

   * Specifieke geografische locaties, waaronder landen, staten, DMA&#39;s in de Verenigde Staten, steden en postcodes

   * Viewers waarvoor specifieke sleutel-waardeparen (de doelstellingen van de gegevenspas worden overgegaan van DSP, de uitgever of de partner

   * [!DNL Creative] pixels en opgegeven kenmerkwaarden opnieuw toewijzen

   * Specifieke apparaattypen, besturingssystemen en browsers

  U kunt creatieve bundels aan elke ervaring toewijzen. Voor elke ervaring, kunt u optimalisering en het plannen voor de creatieve bundels aanpassen en de standaard het landen pagina&#39;s en het volgen URLs <!-- and any flexible attributes --> voor individuele creatieven in elke bundel veranderen.

* **Ervaringen zonder beslissingsboom richtend:** [!DNL Creative] optimaliseert de ad elementen voor de advertentie ervaring zonder het publiek te verkleinen.<!-- For first-party creatives, [!DNL Creative] serves the ads. --> Voor elke ervaring geeft u de begin- en einddatum en enkele standaardinstellingen op, maar een groot deel van de workflow bevindt zich niet rechtstreeks in de ervaring. In plaats van creatieve elementen rechtstreeks aan de ervaring toe te voegen, gebruikt u [!UICONTROL Tag Manager] om voor elke advertentiegrootte een ad-tag voor de ervaring te maken en er vervolgens creatieve creatieve optimalisatie en planning aan toe te voegen, en de bestemmingspagina&#39;s en URL&#39;s bij te houden aan te passen.

## Adoptimalisatie

<!-- MORE -->
[!DNL Creative] optimaliseert de advertentie-elementen voor elke ervaring op basis van prestaties. Voor ervaringen die specifiek op doelgroepen zijn gericht, kunnen advertenties worden geoptimaliseerd op basis van de prestaties van de afzonderlijke advertentie-elementen voor de doeldoelgroepen. Voor ervaringen zonder specifieke doelwitten voor het publiek worden de advertentie-elementen geoptimaliseerd op basis van de prestaties van de afzonderlijke advertentie-elementen.

## Ervaringen implementeren en beheren

Zodra u een levende ervaring (met alle vereiste ad elementen) creeerde, kunt u [ een JavaScript of iframe markering voor de volledige ervaring ](experience-tag-export.md) produceren. U kunt de ervaringstag als een advertentie uploaden naar een campagne in Adobe Advertising DSP of deze als een advertentie implementeren in een DSP van derden. [!DNL Creative] biedt advertenties voor de ervaring op basis van de opties voor het kiezen en draaien van advertenties en de beschikbare voorraad.

## Prestatiegegevens voor uw ervaringen

Wanneer u de optie [!UICONTROL Metrics] inschakelt in de weergave [!UICONTROL Creative] > [!UICONTROL Experiences] , geeft elke ervaringskaart of rij het aantal indrukken aan en klikt u op de ervaring die u hebt ontvangen.

![ optie van Metriek de optie van Metriek ](/help/creative/assets/metrics-option.png " Metriek ")

<!-- insert screen shot of Metrics option?  If not, then add instructions elsewhere -->

<!-- I don't see this as of 1/9; why only in the table view?   You can also add conversion columns in the table view. -->

U kunt [ gedetailleerde prestatiesgegevens voor om het even welke ervaring ](experience-performance-details.md) van de [!UICONTROL Experiences] mening bekijken.

Om prestaties over uw ervaringen te controleren, creeer het Rapport van Creative van de a [ Douane ](/help/creative/report-custom-creative.md).

## Ervaar statussen {#experience-statuses}

<!-- verify that these are all still the same -->

Het statuut van een ervaring wordt automatisch geplaatst, behalve *geschrapt,* die u manueel plaatst.

*Levend:* de ervaring omvat alle vereiste elementen, zodat kunt u een ervaringsmarkering produceren om als advertentie in een DSP uit te voeren. <!-- A live experience may be scheduled to start in the future -->

*Ontwerp:* Alle takken van de ervaring worden niet toegewezen creatieve personen, zodat is de ervaring onvolledig, en u kunt geen ervaringsmarkering produceren.

*Verwerking:* een eerder-levende ervaring werd uitgegeven maar is nu onvolledig. U kunt er geen ervaringstag voor maken. **Nota:** als u reeds een ervaringsmarkering voor de ervaring uitvoerde, dan kan de eerder-levende versie nog worden gediend. Als u de ervaring later voltooit — en deze live maakt — dan kan de nieuwe versie worden gebruikt met de bestaande implementatie van de tag.

*schrapte:* de ervaring werd geschrapt van [!DNL Creative] en is niet meer zichtbaar in de [!UICONTROL Experiences] meningen.

>[!NOTE]
>
>U kunt de status van een advertentie in een DSP wijzigen zonder dat dit van invloed is op de ervaringsstatus in [!DNL Creative] .

## De weergave [!UICONTROL Experiences]

In de weergave [!UICONTROL Experiences] worden al uw doelgerichte en niet-doelgerichte ervaringen weergegeven. U kunt de ervaringsnamen, de status, de begin- en einddatum, het aantal en de afmetingen van de toegewezen creatieve of creatieve bundels zien, en of de ervaring dynamische advertenties bevat. Wanneer u de optie [!UICONTROL Metrics] inschakelt in de [!UICONTROL Experiences] -weergave, geeft elke ervaringskaart of rij het aantal indrukken aan en klikt u op de ervaring die u hebt ontvangen.

U kunt uw ervaringen maken en beheren, waaronder optimalisatie en het toewijzen van creatieve documenten en creatieve bundels aan uw ervaringen. U kunt ook tags voor advertenties maken en hernoemen en de tags exporteren in JavaScript- en iframe-indelingen voor implementatie op uw DSP&#39;s. Adverteerders met Advertising DSP kunnen optioneel tags als advertenties rechtstreeks uploaden naar een Advertising DSP-campagne.

<!--
### Available actions

* [Download data within the view](experience-download-view.md)

        + [Assign and unassign creative bundles to a final node](/help/creative/experiences/experience-assign-creative-bundles.md)
* Experiences with decision tree targeting: [Create](/help/creative/experiences/experience-create-targeting.md) and [edit](/help/creative/experiences/experience-edit-targeting.md) experiences, [assign and unassign creative bundles](/help/creative/experiences/experience-assign-creative-bundles.md), [customize creative optimization and scheduling](/help/creative/experiences/experience-optimization-scheduling-targeting.md), and [customize the tracking URLs for creatives](/help/creative/experiences/experience-tracking-urls-targeting.md)

* Experiences without decision tree targeting: [Create](experience-create-no-targeting.md) and [edit](/help/creative/experiences/experience-edit-no-targeting.md)

* [Clone](experience-clone.md) an experience

* [Preview](experience-preview.md) an experience

* [Share a demo URL](experience-share-demo-url.md) for an experience

* [Export ad tags for an experience](experience-tag-export.md)

* [Delete](experience-delete.md) an experience

-->

<!-- You can add or remove labels for your experiences.-->

<!-- Add links to workflows once they're done -->

>[!MORELIKETHIS]
>
>* [ creeer een ervaring met beslissingsboom richtend ](experience-create-targeting.md)
>* [ creeer een ervaring zonder zich ](experience-create-no-targeting.md) te richten
