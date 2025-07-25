---
title: Portefeuilleinstellingen voor bulkbewerking met behulp van bladbestanden
description: Leer hoe u de instellingen voor meerdere portfolio's kunt bewerken met behulp van een bulksheet-bestand.
feature: Search Portfolios, Search Optimization
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 0%

---

# Portefeuilleinstellingen voor bulkbewerking met behulp van bladbestanden

*eigenschap van Beta*

Een portfoliowerkblad is een bestand dat portfolioinstellingen in een specifieke indeling bevat en kan worden gebruikt om de instellingen snel te controleren en te wijzigen. U kunt opsommingstekens genereren (downloaden) met instellingen voor een of meer portfolio&#39;s. Het bestand wordt gedownload als een [!DNL Excel] -werkmap met twee werkbladen (XLSX-indeling). Het werkboek omvat:

* Een alleen-lezen [!UICONTROL Instructions] werkblad met informatie over het bewerken van de velden.

* Een [!UICONTROL Portfolio Settings Edit] -tabblad met één rij per opgenomen portfolio. U kunt naar keuze de gebieden uitgeven zoals nodig, sparen het dossier plaatselijk, en dan [ uploadt het uitgegeven dossier ](#portfolio-bulksheet-upload) aan Onderzoek, Sociale, &amp; Commerce.

## Een bulkbladbestand met portfolioinstellingen downloaden

1. Schakel het selectievakje naast elk portfolio in dat u wilt opnemen in het werkblad.

1. Klik op **[!UICONTROL Bulk Operations]** > **[!UICONTROL Export Selected Portfolios]** op de werkbalk boven de datatabel.

1. Voer de naam in van het bestand met opsommingstekens dat u wilt maken en klik op **[!UICONTROL Export Now]** .

   Het bestand wordt opgeslagen in de standaardmap Downloads van uw browser.

## Een bulksbladbestand met bijgewerkte portfolioinstellingen uploaden {#portfolio-bulksheet-upload}

Het bestand moet de XLSX-indeling hebben.

1. Klik op **[!UICONTROL Bulk Operations]** > **[!UICONTROL Import Portfolio Details]** op de werkbalk boven de datatabel. &lt;!— Moet &quot;Import Portfolio Settings&quot; zijn — &quot;Details&quot; kunnen te vaag zijn en suggereren dat het iets anders kan bevatten. —>

1. In het dialoogvenster [!UICONTROL Import Portfolio Details File] :<!-- reword if we change the name of the operation -->

   1. Sleep een bestand naar het vak of klik op **[!UICONTROL Browse File]**<!-- "Browse for file" or just "Browse"??? -->om een bestand van het apparaat of het netwerk te selecteren.

   1. Klik op **[!UICONTROL Import]**.

U kunt het statuut van uploaden van de [!UICONTROL Global Sync Status] knoop (![ Globale Status van de Synchronisatie ](/help/search-social-commerce/assets/global-sync-status.png " Globale Status van de Synchronisatie ")) naast de selecteur van de datumwaaier controleren.<!-- icon similar to Refresh -->. Als een van de wijzigingen niet is gelukt, kunt u een foutbestand downloaden waarin wordt aangegeven wat is mislukt.

De berichten worden ook toegevoegd aan het Centrum van het Bericht, en u kunt de ruit van Meldingen van het ![ pictogram van Meldingen ](/help/search-social-commerce/assets/notifications-new.png " ") naast de [!UICONTROL Global Sync Status] knoop (![Status van algemene synchronisatie](/help/search-social-commerce/assets/global-sync-status.png "Status van algemene synchronisatie")) openen.

## Gegevensvereisten voor geüploade bulkbladbestanden

Zie het tabblad [!UICONTROL Instructions] in het gedownloade bulksbladbestand.

Zie de Optimalisatiegids, die beschikbaar is in Zoeken, Sociaal en Commerce, voor uitleg over de kolommen met instellingen voor portfolio&#39;s op het tabblad [!UICONTROL Portfolio Settings Edit] .

<!--
## Data fields on the [!UICONTROL Portfolio Settings Edit] tab

| Field | Required to import data? | Description |
| ----- | ------------------------ | ----------- |
| Portfolio ID |  |  |
| Portfolio Name |  |  |
| Status |  |  |
| Spend Strategy |  |  |
| Target |  |  |
| Hybrid |  |  |
| Auto adjust campaign budgets |  |  |
| Spend Multiple |  |  |
| Minimum Campaign Budget |  |  |
| Objective |  |  |
| Cost Half-Life |  |  |
| Revenue Half-Life |  |  |
| Min. Target CPA |  |  |
| Max. Target CPA |  |  |
| Min. Target ROAS |  |  |
| Max. Target ROAS |  |  |

-->

>[!MORELIKETHIS]
>
>* [ (Nieuwe interface) Een portfolio bewerken ](portfolio-edit.md)
>* [ creeer een portefeuille ](portfolio-create.md)
>* [ (Nieuwe interface) Informatie over portfolio&#39;s ](portfolio-about.md)
