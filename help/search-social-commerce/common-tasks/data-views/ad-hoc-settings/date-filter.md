---
title: Gegevens filteren op datumbereik
description: Leer hoe u het globale datumbereikfilter gebruikt.
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: a438e0c24f9ff83941710f890c55c94b74d4d0f3
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Gegevens filteren op datumbereik

<!-- The same in new UI and legacy CM views -->

Dezelfde globale datumbereikfilter wordt toegepast op de meeste gegevensweergaven in al uw adverteerders, behalve voor de standaardweergaven en aangepaste weergaven waarvoor u specifieke datumbereiken hebt opgeslagen. Het standaarddatumbereik van het systeem voor weergaven voor campagnebeheer is &quot;Gisteren&quot;.

De instellingen voor het datumbereik worden opgeslagen in een browserspecifieke cookie. Wijzigingen in het datumbereikfilter worden dus voor alle adverteerders gebruikt wanneer u zich aanmeldt met dezelfde browsertoepassing totdat u het filter wijzigt of het cookie verwijdert. In elke browsertoepassing die u gebruikt, worden de filterinstellingen voor het datumbereik in een ander cookie opgeslagen.

Wanneer u een specifiek datumbereik opslaat voor een standaardweergave of aangepaste weergave, wordt dat bereik toegepast wanneer u de weergave toepast, ongeacht de browsertoepassing die u gebruikt.

>[!NOTE]
>
>* U kunt gegevens van de voorgaande 13 maanden weergeven, maar bestaande aangepaste weergaven kunnen gegevens van maximaal 180 dagen bevatten.
>* Om vroegere gegevens te bekijken, ga naar [[!UICONTROL Reports] mening &#x200B;](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) en stel een basisrapport in werking.
>* U kunt een datumwaaier voor a [&#x200B; standaardmening of douanemening &#x200B;](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) ook bewaren.

## Globale datumfilter wijzigen in campagneweergaven

1. Klik boven een willekeurige gegevenstabel in Zoeken \> Campagnes \> Campagnes op het huidige datumbereik.

1. Geef in het veld **[!UICONTROL Date Range]** het bereik op:

   * Voor een vooraf ingesteld bereik: selecteer een optie in de lijst met veelgebruikte tijdstappen, variërend van *[!UICONTROL Today]* tot *[!UICONTROL Last 180 Days]* . De standaardwaarde is *[!UICONTROL Yesterday]* .

   * Voor een specifiek bereik: selecteer **[!UICONTROL Custom Date Range]** en geef vervolgens de begin- en einddatum op.

     Ga data in het formaat MM/DD/JJJJ of MM-DD-JJJJ in, of klik ![&#x200B; het pictogram van de Kalender 1&rbrace; van de Kalender &#x200B;](/help/search-social-commerce/assets/calendar.png " naast elk gebied om de kalender te openen en een datum te selecteren.")

1. (Optioneel) Vergelijk gegevens voor het opgegeven datumbereik met gegevens voor een tweede datumbereik:

   1. Verplaats de schuifregelaar **[!UICONTROL Comparison]** naar de positie &quot;Aan&quot;.

      Wanneer u deze optie selecteert, worden er twee extra kolommen toegevoegd voor elke gewone gegevenskolom. Bijvoorbeeld, in plaats van het omvatten van enkel één kolom voor &quot;[!UICONTROL Impressions],&quot;omvat de lijst kolommen voor &quot;[!UICONTROL Impressions R1],&quot;&quot;[!UICONTROL Impressions R2],&quot; en &quot;[!UICONTROL Impressions Diff]&quot;.  Als u de gegevens uitvoert, dan worden de zelfde kolommen gespeld zoals &quot;[!UICONTROL Impressions Range 1],&quot;&quot;[!UICONTROL Impressions Range 2],&quot; en &quot;[!UICONTROL Impressions Difference]&quot;.

   1. Geef het tweede datumbereik op.

   1. Kies hoe te om het verschil tussen gegevens in de twee geselecteerde datumwaaiers in &quot;\ [_het gebied van Gegevens_ \] de kolom van het Verschil&quot;uit te drukken:

      * *[!UICONTROL Variance]* (standaardwaarde): geeft het verschil weer als een numerieke waarde.

      * *[!UICONTROL % Change]:* toont het verschil als percentage.

1. Klik op **[!UICONTROL Apply]**.
