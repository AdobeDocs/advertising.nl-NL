---
title: Creeer een  [!DNL Excel]  malplaatje voor een voer van het spreadsheetrapport
description: Leer hoe u speciaal opgemaakte werkbladsjablonen maakt.
exl-id: 74bf3cdf-7d56-431a-8aff-11ed3840a7cd
feature: Search Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Een [!DNL Excel] -sjabloon maken voor een feed met een spreadsheetrapport

*voor basisrapporten en modelnauwkeurigheidsrapporten slechts*

Als u spreadsheetfeeds wilt maken, moet u eerst speciaal opgemaakte [!DNL Microsoft Excel] spreadsheetsjablonen maken met behulp van gewone rapportsjablonen. U kunt desgewenst het werkblad van [!DNL Excel] aanpassen om extra kolommen en grafieken op te nemen.

1. In **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**, produceer het gewenste rapporttype gebruikend een [!UICONTROL Date Aggregation] eenheid van &quot;[!UICONTROL Daily]&quot;en met alle andere gegevensparameters u wilt, sparen het rapport als malplaatje.

   >[!NOTE]
   >
   > * U kunt spreadsheetfeeds maken voor [!UICONTROL Portfolio] -, [!UICONTROL Search Engine] -, [!UICONTROL Search Engine Account] -, [!UICONTROL Campaign] -, [!UICONTROL Ad Group] -, [!UICONTROL Ad Variation] -, [!UICONTROL Keyword] - en [!UICONTROL Forecast Accuracy] -rapporten. Als u [!UICONTROL Ad Group Report] gebruikt, beperkt u het aantal advertentiegroepen dat wordt opgenomen voor snellere resultaten.
   > * De eenheid [!UICONTROL Date Range] die in de sjabloon is gedefinieerd, wordt niet gebruikt. U zult de data bepalen waarvoor om gegevens te verfrissen wanneer u de spreadsheetvoer later vormt.

1. Nadat het rapport is gegenereerd, gaat u naar **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]** en exporteert u een TSV- of XLS-versie van de rapportuitvoer naar een bestand.

1. Maak in [!DNL Excel] een aangepaste sjabloon voor het rapport:

   1. Open het rapportbestand in [!DNL Excel] .

   1. Het werkboek voorbereiden:

      1. Schrap de hoogste rijen die de rapportparameters tonen. Voor XLS-bestanden verwijdert u ook de rij &quot;[!UICONTROL Total]&quot;. U kunt desgewenst enkele gegevensrijen verwijderen, maar a) de rij met de gegevenskoptekst met alle kolommen in de oorspronkelijke volgorde en b) ten minste één gegevensrij bewaren. Voeg niet handmatig gegevens toe.

         >[!NOTE]
         >
         > De laatste kolom moet waarden bevatten die niet gelijk zijn aan nul.

      2. Sorteer de gegevens op de begindatum in oplopende volgorde (van de oudste naar de meest recente).

      3. Wijzig de naam van het werkbladlusje van &quot;[!UICONTROL Sheet1]&quot;in &quot;[!UICONTROL RAW]&quot;.

         Met deze specifieke tabnaam kunnen de gegevens worden vernieuwd.

      4. (Facultatief) voeg douanekolommen rechts van de kolommen van het rapportmalplaatje toe, zonodig.

   1. (Optioneel) Maak op een afzonderlijk werkblad een draaitabel. Nadat u klaar bent, klikt u met de rechtermuisknop in een willekeurige cel van de draaitabel en selecteert u **[!UICONTROL Pivot Table Options]** . Vervolgens klikt u op de tab **[!UICONTROL Data]** en selecteert u **[!UICONTROL Refresh data when opening the file]** .

   1. Sla het bestand op als een [!DNL Excel] -spreadsheet in de XLSX-indeling.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer het voer van het spreadsheetrapport &#x200B;](spreadsheet-feed-about.md)
>* [&#x200B; creeer een spreadsheetrapportvoer &#x200B;](spreadsheet-feed-create.md)
>* [&#x200B; geeft de montages van de het spreadsheetvoer van het spreadsheetrapport uit &#x200B;](spreadsheet-feed-edit.md)
>* [&#x200B; montages van de het rapportvoer van het Spreadsheet &#x200B;](spreadsheet-feed-settings.md)
>* [&#x200B; Mening of sparen een dossier van het spreadsheetrapport voer &#x200B;](spreadsheet-feed-view-or-save.md)
>* [&#x200B; vernieuw manueel spreadsheetrapportvoer &#x200B;](spreadsheet-feed-refresh.md)
>* [&#x200B; de feeds van het spreadsheetrapport van de Schrapping &#x200B;](spreadsheet-feed-delete.md)
