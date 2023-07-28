---
title: Bewerkingen die u kunt uitvoeren in bulksbladen
description: Verwijs naar algemene informatie over het toevoegen, bewerken en verwijderen van campagnegegevens met behulp van bulksbladen.
exl-id: 82969bb8-dff8-48e7-b37d-1446a2a90072
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Bewerkingen die u kunt uitvoeren in bulksbladen

U kunt campagnegegevens toevoegen, bewerken en verwijderen via bulksbladen voor [ondersteunde advertentienetwerken](../bulksheet-about.md#bulksheet-functionality-by-network).

Neem een aparte gegevensregel op voor elke campagnecomponent (campagne, groep, trefwoord of tekstadvertentie) die u wilt toevoegen, bewerken of verwijderen, of voor de eigenschappen die u wilt toevoegen, bewerken of verwijderen. Als u bijvoorbeeld een campagne wilt maken met één advertentiegroep, één trefwoord en één advertentie (in totaal vier componenten), hebt u vier aparte gegevensregels nodig. Als u de opdracht [!UICONTROL Ad Group Name] voor een advertentiegroep (één component) hebt u echter slechts één regel nodig. Op dezelfde manier hebt u slechts één regel nodig als u vier verschillende eigenschappen voor één advertentiegroep (één component) wilt bewerken.

De volgende regels zijn van toepassing op het werken met campagnecomponenten en hun eigenschappen.

* Toevoegen:

   * Als u een component wilt toevoegen, neemt u alle velden op die nodig zijn om die component toe te voegen, plus eventueel velden voor een van de eigenschappen van de component.

   * Een eigenschap toevoegen voor een bestaande component, zoals de eigenschap [!UICONTROL Ad Group End Date] voor een advertentiegroep, omvat alle gebieden die worden vereist om die component (ad groep) uit te geven plus het gebied voor het bezit ([!UICONTROL Ad Group End Date]).

* Als u een eigenschap voor een bestaande component wilt bewerken, neemt u alle velden op die vereist zijn om die component te bewerken, plus het veld voor de eigenschap.

  Als u het eigenschapveld leeg laat, blijft de bestaande waarde behouden.

* Verwijderen:

   * Als u een bestaande component wilt verwijderen, neemt u alle velden op die nodig zijn om die component te bewerken en wijzigt u de status in [!UICONTROL Deleted]. Als u bijvoorbeeld een [!DNL Google Ads] advertentiegroep, neemt u de [!UICONTROL Campaign Name], [!UICONTROL Ad Group Name], [!UICONTROL Ad Group Status] met een waarde van <i>[!UICONTROL Deleted]</i>, en [!UICONTROL Ad Group ID].

   * ([!UICONTROL Param1], [!UICONTROL Param2], en [!UICONTROL Param3] Alleen waarden) Een bestaande [!DNL paramN] waarde voor een trefwoord, alle velden opnemen die nodig zijn om het trefwoord te bewerken en ook de bestaande [!DNL paramN] waarde door de waarde in te voeren `[delete]` (inclusief de haakjes) in het desbetreffende veld.

   * (Toegestane eigenschapsvelden) Als u een bestaande eigenschapswaarde voor een component wilt verwijderen, neemt u alle velden op die nodig zijn om die component te bewerken en verwijdert u ook de eigenschapswaarde door de waarde in te voeren `[delete]` (inclusief de haakjes). Toegestane velden zijn:

      * ([!UICONTROL Google Ads] alleen) [!UICONTROL Description Line 1], [!UICONTROL Description Line 2]

      * ([!DNL Google Ads] en [!DNL Microsoft® Advertising] alleen) [!UICONTROL Product Scope Filter], [!UICONTROL Base URL/Final URL], [!UICONTROL Tracking Template]

>[!NOTE]
>
>Wanneer u een waarde opneemt in een veld dat niet van toepassing is op de handeling, wordt de waarde die in het veld wordt ingevoerd, genegeerd.

>[!MORELIKETHIS]
>
>* [Campagnegegevens beheren met behulp van bulksbladen](../bulksheet-about.md)
>* [Ondersteunde bestandsindelingen voor bulksbladen](bulksheet-file-formats.md)
>* [Bijlage - Fouten in bladbladen](../bulksheet-errors.md)
>* [Een bulkbladbestand downloaden/maken](../bulksheet-download.md)
