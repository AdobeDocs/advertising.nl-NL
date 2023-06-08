---
title: Gegevens downloaden vanuit een campagnebeheerweergave
description: Leer hoe u gegevens kunt downloaden uit de meeste weergaven voor campagnebeheer.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Gegevens downloaden vanuit een campagnebeheerweergave

U kunt gegevens downloaden van de [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] weergaven behalve de [!UICONTROL Keywords] - [!UICONTROL Keyword Negatives], [!UICONTROL Placements] - [!UICONTROL Placement Negatives], [!UICONTROL Audiences], en [!UICONTROL Extensions] weergaven. U kunt een van de volgende twee downloaden:

* Een rapport in [!DNL XLSM] (macro ingeschakeld) [!DNL Microsoft® Excel] spreadsheet). Als u specifieke rijen selecteert in de weergave, bevat het rapport één rij voor elke geselecteerde rij. Als u geen rijen selecteert, wordt er voor elke rij in de weergave één rij gemaakt.

* Een bulksbladbestand in de TXT-indeling dat alle relevante onderliggende entiteiten bevat. Als u rijen selecteert voor entiteiten op meerdere advertentienetwerken, wordt er één bestand gemaakt voor elk relevant advertentienetwerk. Als u geen rijen selecteert, wordt er één bestand gemaakt voor elk advertentienetwerk dat in de weergave wordt weergegeven. De dossiers van het bulksblad die voor verschillende advertentienetwerken worden geproduceerd omvatten verschillende gegevenskolommen.

   Als u gegevens voor veelvoudige campagnes produceert en de gecombineerde gegevens uit meer dan 500.000 rijen bestaan, dan worden de gegevens verder verdeeld door campagne in twee of meer dossiers, zonodig, genoemd `<bulksheet name>_1.txt`, `<bulksheet name>_2.txt`, enzovoort.

   Elk bestand met de opsommingstekens in het dialoogvenster [!UICONTROL Downloads] wordt ook vermeld op het tabblad [!UICONTROL Bulksheets] weergeven. Wanneer het bestand is gemaakt, ontvangt u een e-mailmelding met een koppeling waarmee u het bestand kunt downloaden. afhankelijk van de hoeveelheid gegevens die wordt verzameld, kan de kennisgeving enkele minuten of langer duren. Als het genereren van het bestand echter mislukt, wordt een foutbestand weergegeven in de weergave Opsommingstekens en ontvangt u een e-mailmelding met een koppeling naar het foutbestand. Een bulksbladbestand verwijderen uit het dialoogvenster [!UICONTROL Download] of de [!UICONTROL Bulksheets] verwijdert deze van beide locaties.

1. (Optioneel) Selecteer de afzonderlijke rijen die u in het bestand wilt opnemen.

   Anders worden alle gegevens in de weergave opgenomen.

1. Klik rechts van de werkbalk op ![Downloaden van rapport](/help/search-social-commerce/assets/download.png "Downloaden van rapport").

1. Klikken ![Maken](/help/search-social-commerce/assets/add.png "Maken") **[!UICONTROL Create]** voegt u desgewenst de bestandsnaam toe en klikt u op **[!UICONTROL Report]** of **[!UICONTROL Bulksheet]**.

1. (Optioneel) Als de rapporttaak is voltooid, klikt u op ![Downloaden van rapport](/help/search-social-commerce/assets/download.png "Downloaden van rapport") om de [!UICONTROL Available Reports] en het rapport vervolgens downloaden of verwijderen:

   * Als u het bestand wilt openen of opslaan volgens de normale procedure van uw browser, klikt u op ![Werkblad downloaden](/help/search-social-commerce/assets/download-spreadsheet.png "Werkblad downloaden").

      Raadpleeg de online Help van uw browser voor meer informatie over de browserprocedure.

   * Als u het bestand wilt verwijderen, klikt u op ![Verwijderen](/help/search-social-commerce/assets/delete.png "Verwijderen").

>[!MORELIKETHIS]
>
>[Een rapport met prestatiegegevens of een bulkbestand verwijderen uit het dialoogvenster [!UICONTROL Downloads] menu](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)
