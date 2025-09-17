---
title: (Nieuwe interface) Informatie over portfolio's
description: Meer informatie over portfolio's.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 8d023c22-a1dd-4608-8c72-0a61f055e7e5
source-git-commit: f7c63646b3eae20fd3413446789fe06ce583e23e
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# (Nieuwe interface) Informatie over portfolio&#39;s

*eigenschap van Beta*

U kunt uw advertentiecampagnes collectief beheren gebruikend portefeuilles (gelijkend op beleggingsportefeuilles). Een portfolio is een reeks advertentiecampagnes of advertentiesets, inclusief de bijbehorende trefwoorden en advertenties, die zijn geoptimaliseerd voor één bedrijfsdoel. Een doelstelling kan meerdere gewogen omzettingen en één begroting of prestatiedoel (zoals een maandelijks budget of een streefrendement) omvatten. Omdat afzonderlijke campagnes/advertentiesets, trefwoorden en advertenties verschillend van elkaar kunnen presteren (bijvoorbeeld, kunnen zij verschillende bedragen uitgeven of verschillende ROIs bereiken), gebruikt het optimaliseringsvermogen AI-gedreven modellen om de volledige portefeuille te sturen om collectief het doel te bereiken. Alle campagnes in een portfolio gebruiken dezelfde valuta.

Sommige gebruikersrollen kunnen portefeuilles tot stand brengen en vormen. Afhankelijk van het type portfolio kunnen de portefeuilleinstellingen de portefeuilledoelstelling, de toegewezen campagnes, de uitgavenstrategie, eventuele inschrijvingsbeperkingen op portefeuilleniveau en de parameters voor modellering en optimalisatie omvatten. Als u klaar bent voor Zoeken, Sociale Zaken en Commerce om te beginnen met optimaliseren voor een portfolio, wijzigt u de status in &quot;geoptimaliseerd&quot;.

U kunt portefeuilles naar keuze groeperen in [ portefeuillegroepen ](portfolio-group-manage.md) zodat u samengestelde gegevens voor de volledige groep kunt bekijken.

Afhankelijk van uw rol, kunt u prestatiessimulaties kunnen produceren, die voorspellende modellering gebruiken om uw optimaal uitgavenpunt en gedetailleerde voorspelde nauwkeurigheidsrapporten te identificeren.<!-- Mention this now? In addition, all users can use the Spend Recommendation Tool to identify the optimal budget distribution across portfolios. -->

## Ondersteuning voor optimalisatie door biedstrategie {#optimization-by-bid-strategy}

Campagnes komen in aanmerking voor optimalisatie op basis van de biedstrategie van de campagne of de advertentiegroep.

>[!NOTE]
>
>&quot;Smart bidding&quot; en &quot;automated bidding&quot; worden vaak door elkaar gebruikt, maar ze zijn niet hetzelfde. Slimme biedingen hebben alleen betrekking op [!DNL Google Ads] - en [!DNL Microsoft Advertising] geautomatiseerde biedstrategieën waarbij gebruik wordt gemaakt van veiling-tijd biedend, wat betekent dat het advertentienetwerk op het moment van elke veiling optimaliseert voor conversie- of conversiewaarden.

<!-- Add "Frequency of Bidding (or other actions, like adjusting campaign budget or bid adjustment values?) -->

| Bodemstrategie | Slim bieden? | Bieden op trefwoord-/productgroepniveau? | Ondersteuningsniveau | Objecttype | Bodemeenheid | Wat stelt Adobe in? | Wat plaatst het netwerk van de ADD? |
|---|---|---|---|---|---|---|---|
| Handmatige CPC ([!DNL Google Ads] - slechts optie) | — | Ja | Maken, bewerken, optimaliseren | Single of multi-property doelstelling met een willekeurige gewichtswaarde | Trefwoord + Type afstemmen + Campagne | Trefwoord bieden, campagnebudget, waarden voor biedingsaanpassingen | nvt |
| ECPC (Enhanced CPC) | Ja | Ja | Maken, bewerken, optimaliseren | Single of multi-property doelstelling met een willekeurige gewichtswaarde | Trefwoord + Type afstemmen + Campagne | Trefwoordbod, campagnebudget | Inschrijvingen in real time aanpassen |
| Klikken maximaliseren [^1 ] | — | — | Maken, bewerken, optimaliseren | Geen; optimaliseert alleen voor klikken | Campagne | Campagnebudget | Past bod in real time aan om kliks binnen het budget te maximaliseren |
| Conversies maximaliseren <br> (met of zonder TCPA) | Ja | — | Maken, bewerken, optimaliseren | Single-property-doelstelling met een gewicht van 1 | Campagne of ad groep ([!DNL Google Ads]) <br> slechts Campagne ([!DNL Microsoft Advertising]) | Het budget van de campagne, Doel CPA wanneer reeks <br> TCPA een standalone biedingsstrategie in [!DNL Microsoft Advertising] kan zijn) | Past bod in real time aan om orden/lood binnen de begroting te maximaliseren, die een CPA doel bereiken wanneer het doel wordt geplaatst |
| Conversiewaarde maximaliseren <br> (met of zonder TROAS) | Ja | — | Maken, bewerken, optimaliseren | Gemengde-vermogensdoelstelling met een gewichtswaarde of doelstelling van één eigendom met een gewichtswaarde groter dan 1 (om een monetaire waarde te vertegenwoordigen) | Campagne of ad groep ([!DNL Google Ads]) <br> slechts Campagne ([!DNL Microsoft Advertising]) | Het budget van de campagne, ROAS van het Doel wanneer de reeks <br> TROAS een standalone biedingsstrategie in [!DNL Microsoft Advertising] kan zijn) | Past inschrijvingen in real time aan om inkomsten/winst binnen de begroting te maximaliseren, die een ROAS-doelstelling bereiken wanneer het doel wordt vastgesteld |
| Doel voor delen van indrukking | — | — | Maken, bewerken | nvt | nvt | n.v.t. - kan niet worden toegewezen aan een portfolio | Past biedingen in real time aan om een indruk te ontmoeten deelt doel |

[^1 ]: De instelling van de [!UICONTROL Maximize Clicks] biedstrategie op het advertentienetwerk is niet hetzelfde als de doelstelling Zoeken, Sociaal, en Commerce [!UICONTROL Maximize Clicks] . Als de biedstrategie [!UICONTROL Maximize Clicks] is, moet u deze alleen toewijzen aan een portfolio met optimalisatie op campagnereniveau of op groepsniveau, niet aan een portfolio met optimalisatie op trefwoordniveau.

## Portfolio-statussen {#portfolio-status}

Een portfolio kan de volgende statussen hebben:

<!-- **Link to include file for "Portfolio status"** -->

{{$include /help/_includes/search-portfolio-status.md}}

## De weergave [!UICONTROL Portfolios]

In de weergave [!UICONTROL Portfolios] worden uw bestaande portfolio&#39;s weergegeven met aanpasbare prestatiegegevens. U kunt [ de kolommen binnen de mening ](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) en filtergegevens aanpassen om specifieke portefeuilles [ van de toolbar ](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) of van de [ kolomrubriek ](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md) te omvatten.

<!-- No options yet to edit anything within the grid, view bid changes, add a portfolio to a portfolio group, edit the Target column, or import/export DOW targets. -->

### Beschikbare acties

<!-- Update with any new options -->

<!-- within row:
* [Rename a portfolio](portfolio-rename.md)

* [View the constraints for a portfolio](portfolio-view-constraint.md)

* [View the change history for a portfolio](portfolio-view-change-history.md)
-->

* [Een portfolio maken](portfolio-create.md)

* [Een portfolio dupliceren](portfolio-duplicate.md)

* [Portefeuilleinstellingen bewerken](portfolio-edit.md)

* [Portefeuilleinstellingen voor bulkbewerking met behulp van bladbestanden](portfolio-bulksheets.md)

* [Gegevens over portfolioprestaties weergeven](portfolio-details.md)

* [ gegevens van de Download in de [!UICONTROL Portfolios] mening ](portfolio-view-report.md)

>[!MORELIKETHIS]
>
>* [ creeer een portefeuille ](portfolio-create.md)
>* [ Dupliceer een portefeuille ](portfolio-duplicate.md)
>* [ geef een portefeuille ](portfolio-edit.md) uit
>* [ beheert de rapporten van de gegevensmening van de [!UICONTROL Portfolios] mening ](portfolio-view-report.md)
