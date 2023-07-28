---
title: Een [!DNL Excel] sjabloon voor een spreadsheetrapportfeed
description: Leer hoe u speciaal opgemaakte werkbladsjablonen maakt.
exl-id: d675cb8c-b7a9-4d7b-8435-5dd662d151a3
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Een [!DNL Excel] sjabloon voor een spreadsheetrapportfeed

*Alleen voor basisverslagen en modelnauwkeurigheidsrapporten*

Als u spreadsheetfeeds wilt maken, moet u eerst speciaal opgemaakte feeds maken [!DNL Microsoft® Excel] spreadsheetsjablonen met behulp van gewone rapportsjablonen. U kunt desgewenst de [!DNL Excel] spreadsheet om extra kolommen en grafieken te omvatten.

1. In **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**, produceert het gewenste rapporttype gebruikend een [!UICONTROL Date Aggregation] eenheid van &quot;[!UICONTROL Daily]&quot; en met alle andere gegevensparameters wilt u, sparen het rapport als malplaatje.

   >[!NOTE]
   >
   > * U kunt werkbladfeeds maken voor [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword], en [!UICONTROL Forecast Accuracy] rapporten. Als u het [!UICONTROL Ad Group Report], beperkt u het aantal advertentiegroepen dat wordt opgenomen voor snellere resultaten.
   > * De [!UICONTROL Date Range] eenheid in het malplaatje wordt bepaald niet gebruikt. U zult de data bepalen waarvoor om gegevens te verfrissen wanneer u de spreadsheetvoer later vormt.

1. Nadat het rapport is gegenereerd, gaat u naar **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** en exporteer een TSV- of XLS-versie van de rapportuitvoer naar een bestand.

1. In [!DNL Excel], creeer een douanemalplaatje voor het rapport:

   1. Open het rapportbestand in [!DNL Excel].

   1. Het werkboek voorbereiden:

      1. Schrap de hoogste rijen die de rapportparameters tonen. Voor XLS-bestanden verwijdert u ook &quot;[!UICONTROL Total]&quot; Rij. U kunt desgewenst enkele gegevensrijen verwijderen, maar a) de rij met de gegevenskoptekst met alle kolommen in de oorspronkelijke volgorde en b) ten minste één gegevensrij bewaren. Voeg niet handmatig gegevens toe.

         >[!NOTE]
         >
         > De laatste kolom moet waarden bevatten die niet gelijk zijn aan nul.

      2. Sorteer de gegevens op de begindatum in oplopende volgorde (van de oudste naar de meest recente).

      3. De naam van het werkbladtabblad wijzigen in &quot;[!UICONTROL Sheet1]&quot; in &quot;[!UICONTROL RAW].&quot;

         Met deze specifieke tabnaam kunnen de gegevens worden vernieuwd.

      4. (Facultatief) voeg douanekolommen rechts van de kolommen van het rapportmalplaatje toe, zonodig.

   1. (Optioneel) Maak op een afzonderlijk werkblad een draaitabel. Nadat u klaar bent, klikt u met de rechtermuisknop in een willekeurige cel van de draaientabel en selecteert u **[!UICONTROL Pivot Table Options]** klikt u op de knop **[!UICONTROL Data]** en selecteert u vervolgens **[!UICONTROL Refresh data when opening the file]**.

   1. Sla het bestand op als een [!DNL Excel] spreadsheet in .XLSX formaat.

>[!MORELIKETHIS]
>
>* [Info over werkbladrapportfeeds](spreadsheet-feed-about.md)
>* [Een feed voor een spreadsheetrapport maken](spreadsheet-feed-create.md)
>* [Invoerinstellingen voor spreadsheetrapporten bewerken](spreadsheet-feed-edit.md)
>* [Feed-instellingen voor werkbladrapporten](spreadsheet-feed-settings.md)
>* [Een feed-bestand voor een spreadsheetrapport weergeven of opslaan](spreadsheet-feed-view-or-save.md)
>* [Werkbladrapportfeeds handmatig vernieuwen](spreadsheet-feed-refresh.md)
>* [feeds voor spreadsheetrapporten verwijderen](spreadsheet-feed-delete.md)
