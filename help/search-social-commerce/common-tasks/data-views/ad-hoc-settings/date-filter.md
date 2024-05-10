---
title: Gegevens filteren op datumbereik
description: Leer hoe u het globale datumbereikfilter gebruikt.
exl-id: 35c0f63f-84ae-4e8e-8a48-acae7ff24498
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Gegevens filteren op datumbereik

Dezelfde globale datumbereikfilter wordt toegepast op de meeste weergaven van uw campagnegegevens voor al uw adverteerders, behalve voor de standaardweergaven en aangepaste weergaven waarvoor u specifieke datumbereiken hebt opgeslagen. Het standaarddatumbereik van het systeem voor weergaven voor campagnebeheer is &quot;Gisteren&quot;.

De instellingen voor het datumbereik worden opgeslagen in een browserspecifieke cookie. Wijzigingen in het datumbereikfilter worden dus voor alle adverteerders gebruikt wanneer u zich aanmeldt met dezelfde browsertoepassing totdat u het filter wijzigt of het cookie verwijdert. In elke browsertoepassing die u gebruikt, worden de filterinstellingen voor het datumbereik in een ander cookie opgeslagen.

Wanneer u een specifiek datumbereik opslaat voor een standaardweergave of aangepaste weergave, wordt dat bereik toegepast wanneer u de weergave toepast, ongeacht de browsertoepassing die u gebruikt.

>[!NOTE]
>
>* U kunt gegevens van de voorgaande 13 maanden weergeven, maar bestaande aangepaste weergaven kunnen gegevens van maximaal 180 dagen bevatten.
>* Als u eerdere gegevens wilt weergeven, gaat u naar de [[!UICONTROL Reports] weergave](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) en voert u een basisrapport uit.
>* U kunt ook een datumbereik opslaan voor een [standaardweergave of aangepaste weergave](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

## Globale datumfilter wijzigen in campagneweergaven

1. Klik boven een willekeurige gegevenstabel in Zoeken \> Campagnes \> Campagnes op het huidige datumbereik.

1. In de **[!UICONTROL Date Range]** -veld, geeft u het bereik op:

   * Voor een vooraf ingesteld bereik: selecteer een optie in de lijst met veelgebruikte tijdstappen, variërend van *[!UICONTROL Today]* tot *[!UICONTROL Last 180 Days]*. De standaardwaarde is *[!UICONTROL Yesterday]*.

   * Voor een specifiek bereik: Selecteren **[!UICONTROL Custom Date Range]** en geeft u vervolgens de begindatum en de einddatum op.

     Voer datums in in de notatie DD-MM-JJJJ of DD-MM-JJJJ, of klik op ![Kalenderpictogram](/help/search-social-commerce/assets/calendar.png "Kalenderpictogram") naast elk veld om de kalender te openen en een datum te selecteren.

1. (Optioneel) Vergelijk gegevens voor het opgegeven datumbereik met gegevens voor een tweede datumbereik:

   1. Verplaats de **[!UICONTROL Comparison]** schuifregelaar naar *[!UICONTROL On]*.

      Wanneer u deze optie selecteert, worden er twee extra kolommen toegevoegd voor elke gewone gegevenskolom. In plaats van bijvoorbeeld slechts één kolom op te nemen voor &quot;[!UICONTROL Impressions],&quot; bevat de tabel kolommen voor &quot;[!UICONTROL Impressions R1],&quot; &quot;[!UICONTROL Impressions R2],&quot; en &quot;[!UICONTROL Impressions Diff].&quot;  Als u de gegevens exporteert, worden dezelfde kolommen als &quot;[!UICONTROL Impressions Range 1],&quot; &quot;[!UICONTROL Impressions Range 2],&quot; en &quot;[!UICONTROL Impressions Difference].&quot;

   1. Geef het tweede datumbereik op.

   1. Kies hoe u het verschil tussen gegevens in de twee geselecteerde datumbereiken in &quot;\[ wilt uitdrukken _Gegevensveld_\] Verschil&quot; kolom:

      * *[!UICONTROL Variance]* (standaard): geeft het verschil weer als een numerieke waarde.

      * *[!UICONTROL % Change]:*  Hiermee geeft u het verschil weer als een percentage.

1. Klik op **[!UICONTROL Apply]**.
