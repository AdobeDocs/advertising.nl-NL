---
title: Portefeuilleinstellingen voor bulkbewerking met behulp van bladbestanden
description: Leer hoe u de instellingen voor meerdere portfolio's kunt bewerken met behulp van een bulksheet-bestand.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 20f7419d-9f5e-4477-ae8d-8b85a79b1e81
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Portefeuilleinstellingen voor bulkbewerking met behulp van bladbestanden

*eigenschap van Beta*

Een portfoliowerkblad is een bestand dat portfolioinstellingen in een specifieke indeling bevat en kan worden gebruikt om de instellingen snel te controleren en te wijzigen. U kunt opsommingstekens genereren (downloaden) met instellingen voor een of meer portfolio&#39;s. Het bestand wordt gedownload als een [!DNL Excel] -werkmap met twee werkbladen (XLSX-indeling). Het werkboek omvat:

* Een alleen-lezen [!UICONTROL Instructions] werkblad met informatie over het bewerken van de velden.

* Een [!UICONTROL Portfolio Settings Edit] -tabblad met één rij per opgenomen portfolio. U kunt naar keuze de gebieden uitgeven zoals nodig, sparen het dossier plaatselijk, en dan [&#x200B; uploadt het uitgegeven dossier &#x200B;](#portfolio-bulksheet-upload) aan Onderzoek, Sociale, &amp; Commerce. De bewerkbare velden worden in kleur gemarkeerd.

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

U kunt het statuut van uploaden van de [!UICONTROL Global Sync Status] knoop (![&#x200B; Globale Status van de Synchronisatie &#x200B;](/help/search-social-commerce/assets/global-sync-status.png " Globale Status van de Synchronisatie ")) naast de selecteur van de datumwaaier controleren.<!-- icon similar to Refresh -->. Als een van de wijzigingen niet is gelukt, kunt u een foutbestand downloaden waarin wordt aangegeven wat is mislukt.

De berichten worden ook toegevoegd aan het Centrum van het Bericht, en u kunt de ruit van Meldingen van het ![&#x200B; pictogram van Meldingen &#x200B;](/help/search-social-commerce/assets/notifications-new.png " ") naast de [!UICONTROL Global Sync Status] knoop (![Status van algemene synchronisatie](/help/search-social-commerce/assets/global-sync-status.png "Status van algemene synchronisatie")) openen.

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
>* [&#x200B; (Nieuwe interface) Een portfolio bewerken &#x200B;](portfolio-edit.md)
>* [&#x200B; creeer een portefeuille &#x200B;](portfolio-create.md)
>* [&#x200B; (Nieuwe interface) Informatie over portfolio&#39;s &#x200B;](portfolio-about.md)
