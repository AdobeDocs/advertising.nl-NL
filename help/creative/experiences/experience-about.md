---
title: Ervaringen in Advertising Creative
description: Leer hoe u persoonlijke advertentie-ervaringen configureert en de ad-elementen optimaliseert op basis van prestaties.
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 2ddda1e23e3a3413ef93ca0705f0b9688c893f64
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---

# Ervaringen in Advertising Creative 2.0

*Gesloten bèta*

[!DNL Advertising Creative 2.0] verstrekt twee verschillende structuren van de advertentie voor de advertenties in een creatieve bibliotheek <!-- can use a single library only -->:

* **Ervaringen met beslissingsboom richtend:** [!DNL Creative] staat u toe om gepersonaliseerde ad ervaringen door de klantenreis te vormen gebruikend een model van de beslissingsboom. U kunt alle advertentie-elementen — afbeeldingen, koppen, aanbiedingen en bestemmingspagina&#39;s — aanpassen op basis van het doelpubliek.

  U kunt bijvoorbeeld dezelfde creatieve bundel opgeven voor mensen in Chicago en New York City die zich in een specifiek Adobe Analytics-publiekssegment bevinden, maar mensen in Chicago naar andere bestemmingspagina&#39;s sturen dan New Yorkers. U kon een verschillende bundel voor mensen in het segment ook specificeren die overal behalve Chicago en de Stad van New York wonen, en een derde bundel voor andere mensen die niet in het segment zijn.

  De volgende doelopties zijn beschikbaar:

   * Uw eersteklas publiekssegmenten van Adobe Audience Manager, Adobe Analytics en Advertising Cloud DSP

   * Specifieke geografische locaties, waaronder landen, staten, DMA&#39;s in de Verenigde Staten, steden en postcodes

   * Viewers waarvoor specifieke sleutel-waardeparen (de doelstellingen van de gegevenspas worden overgegaan van DSP, de uitgever of de partner

   * [!DNL Creative] pixels en opgegeven kenmerkwaarden opnieuw toewijzen

   * Specifieke apparaattypen, besturingssystemen en browsers

  Zodra u een tak van het doelpubliek in de beslissingsboom creeert, kunt u het doelpubliek met potentiële creatieve creatieven associëren door creatieve bundels aan de tak toe te wijzen. Voor elke ervaring, kunt u optimalisering en het plannen voor de creatieve bundels aanpassen en de standaard het landen pagina&#39;s en het volgen URLs <!-- later: and any flexible attributes --> voor individuele creatieven in elke bundel veranderen.

* **Ervaringen zonder beslissingsboom richtend:** [!DNL Creative] optimaliseert de ad elementen voor de advertentie ervaring zonder het publiek te verkleinen. Voor elke ervaring, specificeert u begin en einddata en sommige standaardmontages, maar veel van het werkschema is niet direct binnen de ervaring. In plaats van creatieve elementen rechtstreeks aan de ervaring toe te voegen, gebruikt u [!UICONTROL Tag Manager] om een ad-tag voor elke advertentiegrootte voor de ervaring te maken en er vervolgens creatieve creatieve optimalisatie en planning aan toe te voegen, en de bestemmingspagina&#39;s aan te passen en URL&#39;s te volgen <!-- later: and any flexible attributes -->.

## Adoptimalisatie

<!-- MORE -->
[!DNL Creative] optimaliseert de advertentie-elementen voor elke ervaring op basis van prestaties. Voor ervaringen die specifiek op doelgroepen zijn gericht, kunnen advertenties worden geoptimaliseerd op basis van de prestaties van de afzonderlijke advertentie-elementen voor de doeldoelgroepen. Voor ervaringen zonder specifieke doelwitten voor het publiek worden de advertentie-elementen geoptimaliseerd op basis van de prestaties van de afzonderlijke advertentie-elementen.

## Ervaringen implementeren en beheren

Zodra u een levende ervaring (met alle vereiste ad elementen) creeert, kunt u [ een JavaScript of iframe markering voor de volledige ervaring ](experience-tag-export.md) produceren. U kunt de ervaringstag als een advertentie uploaden naar een campagne in Adobe Advertising DSP of deze als een advertentie implementeren in een DSP van derden. [!DNL Creative] dient voor advertenties van eerste partijen en activeert advertenties van derden voor de ervaring op basis van de opties voor aanwijzen en ad-rotatie en de beschikbare voorraad voor advertenties.

## Prestatiegegevens voor uw ervaringen

De volgende prestatiegegevens zijn beschikbaar:

* Wanneer u de optie [!UICONTROL Metrics] inschakelt in de weergave [!UICONTROL Creative] > [!UICONTROL Experiences] , geeft elke ervaringskaart of rij het aantal indrukken aan en klikt u op de ervaring die u hebt ontvangen.

  ![ optie van Metriek de optie van Metriek ](/help/creative/assets/metrics-option.png " Metriek ")

  <!-- insert screen shot of Metrics option?  If not, then add instructions elsewhere -->

  <!-- I don't see this as of 1/9; why only in the table view?   You can also add conversion columns in the table view. -->

* U kunt [ gedetailleerde prestatiesgegevens voor om het even welke ervaring ](experience-performance-details.md) van de [!UICONTROL Experiences] mening bekijken.

* Om prestaties over uw ervaringen te controleren, creeer het Rapport van Creative van de a [ Douane ](/help/creative/report-custom-creative.md).

## Ervaar statussen {#experience-statuses}

Het statuut van een ervaring wordt automatisch geplaatst, behalve *Geschrapt,* die u manueel plaatst.

| Status | Beschrijving |
| ------ | ----------- |
| [!UICONTROL Live] | De ervaring omvat alle vereiste elementen, zodat kunt u een ervaringsmarkering produceren om als advertentie in een DSP uit te voeren. In de toekomst kan een live-ervaring worden gestart. |
| [!UICONTROL Draft] | Aan alle vertakkingen van de ervaring zijn geen creatieve elementen toegewezen, zodat de ervaring onvolledig is en u geen ervaringstag kunt genereren. |
| [!UICONTROL Processing] | Een ervaring die u eerder hebt opgedaan, is bewerkt, maar nu onvolledig. U kunt er geen ervaringstag voor maken. **Nota:** als u reeds een ervaringsmarkering voor de ervaring uitvoerde, dan kan de eerder-levende versie nog worden gediend. Als u de ervaring later voltooit — en deze live maakt — dan kan de nieuwe versie worden gebruikt met de bestaande implementatie van de tag. |
| [!UICONTROL Deleted] | De ervaring is verwijderd uit [!DNL Creative] en is niet meer zichtbaar in de weergaven van [!UICONTROL Experiences] . |

>[!NOTE]
>
>U kunt de status van een advertentie in een DSP wijzigen zonder dat dit van invloed is op de ervaringsstatus in [!DNL Creative] .

## De weergave [!UICONTROL Experiences]

In de weergave [!UICONTROL Experiences] worden al uw doelgerichte en niet-doelgerichte ervaringen weergegeven. U kunt de ervaringsnamen, de status, de begin- en einddatum, het aantal en de afmetingen van de toegewezen creatieve of creatieve bundels zien, en of de ervaring dynamische advertenties bevat. Wanneer u de optie [!UICONTROL Metrics] inschakelt in de [!UICONTROL Experiences] -weergave, geeft elke ervaringskaart of rij het aantal indrukken aan en klikt u op de ervaring die u hebt ontvangen.

U kunt uw ervaringen maken en beheren, labels voor advertenties maken en hernoemen en de labels exporteren in JavaScript- en iframe-indelingen voor implementatie op uw DSP&#39;s. Adverteerders met Advertising DSP kunnen optioneel advertentietags rechtstreeks uploaden naar een Advertising DSP-campagne.

### Beschikbare acties

Hier volgen enkele belangrijke acties. Voor een volledige lijst, zie de inhoudstafel voor het Creative > hoofdstuk van Ervaring.

* [Gegevens downloaden in de weergave](experience-download-view.md)

* [ creeer ](/help/creative/experiences/experience-create-targeting.md) en [ geef ](/help/creative/experiences/experience-edit-targeting.md) een ervaring met het richten uit

* [ creeer ](/help/creative/experiences/experience-create-no-targeting.md), [ geef ](/help/creative/experiences/experience-edit-no-targeting.md) uit, en [ creeer manueel een ad markering ](/help/creative/experiences/experience-tag-create-manually.md) voor een ervaring zonder zich het richten

* [ Kloon ](experience-clone.md) een ervaring

* [ Voorproef ](experience-preview.md) een ervaring

* [ Deel een demo URL ](experience-share-demo-url.md) voor een ervaring

* [ de uitvoer ad markeringen voor een ervaring ](experience-tag-export.md), met inbegrip van naar keuze het uploaden van ad markeringen rechtstreeks aan een campagne van Advertising DSP

* [ Schrap ](experience-delete.md) een ervaring

>[!MORELIKETHIS]
>
>* [ creeer een ervaring met beslissingsboom richtend ](experience-create-targeting.md)
>* [ creeer een ervaring zonder zich ](experience-create-no-targeting.md) te richten
