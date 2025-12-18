---
title: Ervaringen in Advertising Creative
description: Leer hoe u persoonlijke advertentie-ervaringen configureert en de ad-elementen optimaliseert op basis van prestaties.
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 39f77087769eda3cc200447aeb0a6d1648e23b42
workflow-type: tm+mt
source-wordcount: '1167'
ht-degree: 0%

---

# Ervaringen in Advertising Creative 2.0

Elke advertentie kan één advertentietype bevatten (standaardweergave, standaardvideo of dynamisch scherm). [!DNL Advertising Creative 2.0] biedt twee verschillende advertentiestructuren voor de advertenties in één creatieve bibliotheek.

* **Ervaringen met beslissingsboom richtend:** [!DNL Creative] staat u toe om gepersonaliseerde ad ervaringen door de klantenreis te vormen gebruikend een model van de beslissingsboom. U kunt alle advertentie-elementen — afbeeldingen, koppen, aanbiedingen en bestemmingspagina&#39;s — aanpassen op basis van het doelpubliek.

  U kunt bijvoorbeeld dezelfde creatieve bundel opgeven voor mensen in Chicago en New York City die zich in een specifiek Adobe Analytics-publiekssegment bevinden, maar mensen in Chicago naar andere bestemmingspagina&#39;s sturen dan New Yorkers. U kon een verschillende bundel voor mensen in het segment ook specificeren die overal behalve Chicago en de Stad van New York wonen, en een derde bundel voor andere mensen die niet in het segment zijn.

  De volgende doelopties zijn beschikbaar:

   * Uw publiekssegmenten van Adobe Audience Manager, Adobe Analytics en Advertising DSP; alle andere eerderangssegmenten die voor de account zijn geïmporteerd; uw aangepaste segmenten van Advertising DSP; segmenten van derden die door Advertising DSP worden geleverd; en alle bestaande Advertising DSP-soorten die in Audience Library zijn ingebouwd

   * Specifieke geografische locaties, waaronder landen, staten, DMA&#39;s in de Verenigde Staten, steden en postcodes

   * Viewers waarvoor specifieke sleutel-waardeparen (gegevens overgaan doelstellingen) van DSP, uitgever, of partner (zoals SKU=01234567890123 of Cart=empty) worden overgegaan

   * [!DNL Creative] pixels en opgegeven kenmerkwaarden opnieuw toewijzen

   * Specifieke apparaattypen, besturingssystemen en browsers

  Zodra u een tak van het doelpubliek in de beslissingsboom creeert, kunt u het doelpubliek met potentiële creatieve creatieven associëren door creatieve bundels aan de tak toe te wijzen. Voor elke ervaring, kunt u optimalisering en het plannen voor de creatieve bundels aanpassen en de standaard het landen pagina&#39;s en het volgen URLs <!-- later: and any flexible attributes --> voor individuele creatieven in elke bundel veranderen.

* **Ervaringen zonder beslissingsboom richtend:** [!DNL Creative] optimaliseert de ad elementen voor de advertentie ervaring zonder het publiek te verkleinen. Voor elke ervaring, specificeert u begin en einddata en sommige standaardmontages, maar veel van het werkschema is niet direct binnen de ervaring. In plaats van creatieve elementen rechtstreeks aan de ervaring toe te voegen, gebruik [!UICONTROL Tag Manager] om een ad markering voor elke advertentiegrootte voor de ervaring tot stand te brengen en dan creatieve creatieve optimalisering en het plannen toe te voegen, en de het landen pagina&#39;s en het volgen URLs <!-- later: and any flexible attributes --> aan te passen.

>[!NOTE]
>
> Omdat de twee soorten ervaringen verschillende workflows hebben, kunt u een niet-doelgerichte ervaring niet wijzigen in een doelgerichte ervaring of in een niet-doelgerichte ervaring.

## Advertentie en optimalisatie

<!-- MORE -->
<!-- When multiple ad variants qualify for an impression -->

[!DNL Creative] levert advertenties van eerste partijen en activeert advertenties van derden voor de ervaring die op de gespecificeerde het richten (indien van toepassing), het plannen, en de omwenteling, en optimalisatiedoelopties evenals de beschikbare voorraad wordt gebaseerd.

* **Plannend:** (Facultatieve) Plan specifieke creatieve om tijdens gespecificeerde, opeenvolgende tijdsperioden te lopen.

* **de omwenteling van de Advertentie:** roteer de creatieve creatieven algoritmisch volgens het gespecificeerde optimalisatiedoel; volgens een gespecificeerde bundelopeenvolging; of volgens relatieve gewichten.

* **het doel van de Optimalisering:** optimaliseer en elementen voor of het beste klik-door tarief of een bestaand [ de douanedoel van Advertising DSP ](/help/dsp/optimization/custom-goal.md)

  [!DNL Creative] optimaliseert en ervaart door de indruk te wekken dat de best presterende elementen in de ervaring worden gedeeld. Voor ervaringen die specifiek op doelgroepen zijn gericht, kunnen advertenties worden geoptimaliseerd op basis van de prestaties van de afzonderlijke advertentie-elementen voor de doeldoelgroepen. Voor ervaringen zonder specifieke doelwitten voor het publiek worden de advertentie-elementen uitsluitend geoptimaliseerd op basis van de prestaties van de afzonderlijke advertentie-elementen.

U kunt bijvoorbeeld plannen dat Creative 1 gedurende de eerste twee weken wordt uitgevoerd om de doorklikfrequentie te optimaliseren en Creative 2 gedurende de volgende twee weken om te optimaliseren voor een bepaald aangepast doel.

## Ervaringen implementeren en beheren

Zodra u een levende ervaring (met alle vereiste ad elementen) creeert, kunt u [ een JavaScript of iframe markering voor de volledige ervaring ](experience-tag-export.md) produceren. U kunt de ervaringstag als een advertentie uploaden naar een campagne in Adobe Advertising DSP of deze als een advertentie implementeren in een DSP van derden.

>[!NOTE]
>
>Het gedrag voor hiërarchische activering kan per DSP variëren. Advertising DSP hanteert een ad-level gerichte aanpak boven op het doel op het plaatsingsniveau.

## Prestatiegegevens voor uw ervaringen

De volgende prestatiegegevens zijn beschikbaar:

* Wanneer u de optie [!UICONTROL Metrics] inschakelt in de weergave [!UICONTROL Creative] > [!UICONTROL Experiences] , geeft elke ervaringskaart of rij het aantal indrukken aan en klikt u op de ervaring die u hebt ontvangen.

  ![ optie van Metriek de optie van Metriek ](/help/creative/assets/metrics-option.png " Metriek ")

* U kunt [ gedetailleerde prestatiesgegevens voor om het even welke ervaring ](experience-performance-details.md) van de [!UICONTROL Experiences] mening bekijken.

* Om prestaties over uw ervaringen te controleren, creeer het Rapport van Creative van de a [ Douane ](/help/creative/reports/report-manage.md).

## Waarschuwingsindicatoren

Een kolom &quot;[!UICONTROL Alerts]&quot;wijst erop wanneer een ervaring, of om het even welk kind creatief onder het, een kwestie heeft. Een [!UICONTROL Pulse Panel] pictogram rechts van de werkbalk geeft aan of er waarschuwingen beschikbaar zijn voor de ervaring, inclusief een van de onderliggende creatieve elementen. Zie &quot;[ Alarm van de Mening ](/help/creative/reports/alerts-view.md)&quot;voor meer informatie.

## Ervaar statussen {#experience-statuses}

Het statuut van een ervaring wordt automatisch geplaatst, behalve *Geschrapt,* die u manueel plaatst.

| Status | Beschrijving |
| ------ | ----------- |
| [!UICONTROL Live] | De ervaring omvat alle vereiste elementen, zodat kunt u een ervaringsmarkering produceren om als advertentie in een DSP uit te voeren. In de toekomst kan een live-ervaring worden gestart. |
| [!UICONTROL Draft] | Aan alle vertakkingen van de ervaring zijn geen creatieve elementen toegewezen, zodat de ervaring onvolledig is en u geen ervaringstag kunt genereren. |
| [!UICONTROL Processing] | Een eerdere live ervaring is bewerkt, maar is nu onvolledig. U kunt er geen ervaringstag voor maken. **Nota:** als u reeds een ervaringsmarkering voor de ervaring uitvoerde, dan kan de vorige levende versie nog worden gediend. Als u de ervaring later voltooit — en deze live maakt — dan kan de nieuwe versie worden gebruikt met de bestaande implementatie van de tag. |
| [!UICONTROL Deleted] | De ervaring is verwijderd uit [!DNL Creative] en is niet meer zichtbaar in de weergaven van [!UICONTROL Experiences] . |

>[!NOTE]
>
>U kunt de status van een advertentie in een DSP wijzigen zonder dat dit van invloed is op de ervaringsstatus in [!DNL Creative] .

## De weergave [!UICONTROL Experiences]

In de weergave [!UICONTROL Experiences] worden al uw doelgerichte en niet-doelgerichte ervaringen weergegeven. U kunt de ervaringsnamen, de status, de begin- en einddatum, het aantal en de afmetingen van de toegewezen creatieve of creatieve bundels zien, en of de ervaring dynamische advertenties bevat. Wanneer u de optie [!UICONTROL Metrics] inschakelt in de [!UICONTROL Experiences] -weergave, geeft elke ervaringskaart of rij het aantal indrukken aan en klikt u op de ervaring die u hebt ontvangen. In de kaartmodus kunt u met behulp van de &lt;- en >-knoppen door de creatieve functies bladeren in een ervaring met meerdere creatieve projecten.

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
