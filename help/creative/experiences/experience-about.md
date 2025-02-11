---
title: Ervaringen in Advertising Creative
description: Leer hoe u persoonlijke advertentie-ervaringen configureert en de ad-elementen optimaliseert op basis van prestaties.
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 8f81cf8ffaec7ca30ee3bbfd45d3577e75d77faf
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---

# Ervaringen in Advertising Creative 2.0

*Gesloten bèta*

<!-- Revisit Description metadata -->

<!-- MORE -->

[!DNL Advertising Creative 2.0] biedt twee verschillende advertentiestructuren voor advertenties in een creatieve bibliotheek <!-- can use a single library only --> :

* **Ervaringen met beslissingsboom richtend:** [!DNL Creative] staat u toe om gepersonaliseerde ad ervaringen door de klantenreis te vormen gebruikend een model van de beslissingsboom. U kunt alle advertentie-elementen — afbeeldingen, koppen, aanbiedingen en bestemmingspagina&#39;s — aanpassen op basis van het doelpubliek.

  U kunt bijvoorbeeld dezelfde creatieve bundel opgeven voor mensen in Chicago en New York City die zich in een specifiek Adobe Analytics-publiekssegment bevinden, maar mensen in Chicago die zich in hetzelfde segment bevinden naar andere landingspagina&#39;s sturen dan New Yorkers. U kon een verschillende bundel voor mensen in het segment ook specificeren die overal behalve Chicago en de Stad van New York wonen, en een derde bundel voor andere mensen die niet in het segment zijn.

  Tot de doelopties behoren onder andere viewers in uw doelsegmenten van de eerste partij, zoals Adobe Audience Manager, Adobe Analytics en Advertising Cloud DSP; viewers op specifieke geografische locaties, waaronder landen, staten, DMA&#39;s in de Verenigde Staten, steden en ZIP-codes; viewers waarvoor specifieke sleutelwaardeparen (gegevensdoorvoerdoelen) zijn doorgegeven van de DSP, uitgever of partner; viewers met [!DNL Creative] doelgericht op pixels en opgegeven kenmerkwaarden; specifieke apparaattypen, besturingssystemen en browsers.

  U kunt creatieve bundels aan elke ervaring toewijzen, naar keuze het aanpassen optimalisering en het plannen voor de creatieve bundels en het veranderen van de standaard het landen pagina&#39;s en het volgen URLs <!-- and any flexible attributes --> voor individuele creatieven in elke bundel.

* **Ervaringen zonder beslissingsboom richtend:** [!DNL Creative] optimaliseert de ad elementen voor de advertentie ervaring zonder het publiek te verkleinen.<!-- For first-party creatives, [!DNL Creative] serves the ads. --> U geeft de begin- en einddatum en een aantal standaardinstellingen voor elke ervaring op, maar een groot deel van de workflow bevindt zich niet rechtstreeks in de ervaring. In plaats van creatieve elementen rechtstreeks aan de ervaring toe te voegen, maakt u voor elke advertentiegrootte een ad-tag voor de ervaring en voegt u er creatieve creatieve oplossingen aan toe, configureert u de optimalisatie en planning en past u de bestemmingspagina&#39;s en URL&#39;s van de kant van [!UICONTROL Tag Manager] aan.

## Adoptimalisatie

<!-- MORE -->
[!DNL Creative] optimaliseert de advertentie-elementen voor elke ervaring op basis van prestaties. Voor ervaringen die specifiek op doelgroepen zijn gericht, kunnen advertenties worden geoptimaliseerd op basis van de prestaties van de afzonderlijke advertentie-elementen voor de doeldoelgroepen. Voor ervaringen zonder specifieke doelwitten voor het publiek worden de advertentie-elementen geoptimaliseerd op basis van de prestaties van de afzonderlijke advertentie-elementen.

## Ervaringen implementeren en beheren

Zodra u een levende ervaring (met alle vereiste ad elementen) hebt gecreeerd, kunt u [ een JavaScript of iframe markering voor de volledige ervaring ](experience-tag-export.md) produceren, die u naar keuze als advertentie aan een campagne in Adobe Advertising DSP kunt uploaden of als advertentie in derde DSP uitvoeren. [!DNL Creative] biedt advertenties voor de ervaring op basis van de opties voor het kiezen en draaien van advertenties en de beschikbare voorraad.

## Prestatiegegevens voor uw ervaringen

Wanneer u de optie [!UICONTROL Metrics] inschakelt in de [!UICONTROL Experiences] -weergave, geeft elke ervaringskaart of rij het aantal indrukken aan en klikt u op de ervaring die u hebt ontvangen.

![ optie van Metriek de optie van Metriek ](/help/creative/assets/metrics-option.png " Metriek ")

<!-- insert screen shot of Metrics option?  If not, then add instructions elsewhere -->

<!-- I don't see this as of 1/9; why only in the table view?   You can also add conversion columns in the table view. -->

In de weergave [!UICONTROL Creative] > [!UICONTROL Experiences] kunt u gedetailleerde prestatiegegevens weergeven voor elke ervaring. Maak een [!UICONTROL Custom Creative Report] om de prestaties in al uw ervaringen te controleren.

<!--
You can [view detailed performance data for any experience](experience-performance-details.md) from the Creative > Experiences view. To monitor performance across your experiences, [create custom reports](/help/dsp/reports/report-create.md).
-->

## Ervaar statussen {#experience-statuses}

<!-- verify that these are all still the same -->

Het statuut van een ervaring wordt automatisch geplaatst, behalve *geschrapt,* die u manueel plaatst.

*Levend:* de ervaring omvat alle vereiste elementen, zodat kunt u een ervaringsmarkering produceren om als advertentie in een DSP uit te voeren. <!-- A live experience may be scheduled to start in the future -->

*Ontwerp:* Alle takken van de ervaring worden niet toegewezen creatieve personen, zodat is de ervaring onvolledig, en u kunt geen ervaringsmarkering produceren.

*Verwerking:* een eerder-levende ervaring is uitgegeven maar is nu onvolledig. U kunt er geen ervaringstag voor maken. **Nota:** als u reeds een ervaringsmarkering voor de ervaring uitvoerde, dan zal de eerder-levende versie nog worden gediend. Als u de ervaring later voltooit — en deze live maakt — dan wordt de nieuwe versie weergegeven met behulp van de bestaande implementatie van de tag.

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
