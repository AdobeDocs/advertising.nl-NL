---
title: Informatie over campagnebeheer in Zoeken, Sociale Zaken en Handel
description: Meer informatie over functies voor campagnebeheer in Zoeken, Sociaal en Handel.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 0%

---

# Informatie over campagnebeheer in Zoeken, Sociale Zaken en Handel

Met Zoeken, Sociaal en Handel kunt u uw zoekacties, weergave/inhoud, sociale campagnes, winkelen, publiek en maximale prestaties op één locatie bijhouden en/of beheren. Afhankelijk van het advertentienetwerk en het type campagne, kan de beschikbare functionaliteit synchronisatie met uw advertentienetwerken omvatten, creeer en geef capaciteiten, het volgen en conversie attributie, rapportering, en bieder en begrotingsoptimalisering uit. Voor details over de functionaliteit beschikbaar voor elk advertentienetwerk, zie &quot;[Ondersteunde voorraad](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

Terwijl u campagnegegevens toevoegt en bewerkt in het dialoogvenster [!UICONTROL Campaigns] weergaven, Zoeken, Sociaal en Handel zorgt ervoor dat de gegevenswijzigingen direct in het advertentienetwerk worden doorgevoerd. Zoek, Sociale zaken en Handel verkrijgt ook de gegevens van de campagnestructuur en klikt op gegevens van gesynchroniseerde en netwerkaccounts eenmaal per dag (of vaker wanneer nieuwe campagnes worden gedetecteerd) en op verzoek.

## Toegang tot uw advertentienetwerkaccounts instellen

Om de prestaties van advertenties in een advertentienetwerkaccount van een adverteerder te volgen (en mogelijk biedingen voor de advertenties te plaatsen), het accountteam van Adobe [een corresponderend accountrecord maken](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) in Search, Social, &amp; Commerce. De accountrecord bevat opties voor bijhouden.

Voor accounts die zijn gesynchroniseerd via de API van het advertentienetwerk, bevat de accountrecord ook de toegangsreferenties voor de account. Zodra de rekening wordt toegelaten, worden de rekeningsgegevens getrokken van met het advertentienetwerk. U kunt dan de bestaande accountgegevens bekijken en de campagnestructuur en -gegevens maken en bewerken.

## Klik op bijhouden om de klikken aan conversies te koppelen

Als u de service Adobe Advertising Tracking Service gebruikt, moet u code voor zoeken, sociale zaken en handel opnemen in het achtervoegsel van de bestemmingspagina, sjablonen voor het bijhouden van advertenties en de URL&#39;s voor de eindgebruiker/bestemming voor advertenties, trefwoorden en plaatsingen, sitelinks en productlijsten. Voor [ondersteunde advertentienetwerken en campagneretypen](/help/search-social-commerce/introduction/supported-inventory.md) waarvan de campagne-instellingen &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload],&quot; Onderzoek, Sociale, &amp; Handel voegt automatisch zijn eigen omleiding en het volgen code toe wanneer u sparen het verslag, zodat te hoeven u niet het manueel toe te voegen. Anders moet u de code handmatig toevoegen aan de volgende sjablonen of uiteindelijke URL&#39;s.

Zie het hoofdstuk over &quot;Tekstspatiëring&quot; voor meer informatie over tekstspatiëring.

## Automatiseren van biedingen en begrotingsbeheer

Voor [ondersteunde advertentienetwerken en campagneretypen](/help/search-social-commerce/introduction/supported-inventory.md), kunt u uw campagnes groeperen in portefeuilles, elk met een specifiek bedrijfsdoel en een specifiek begroting of prestatiesdoel. In standaardportfolio&#39;s optimaliseert Search, Social en Commerce CPC-trefwoordbiedingen en campagnebudgetten. Hybride portefeuilles combineren optimalisatietechnologieën van Onderzoek, Sociale, &amp; Handel en uw advertentienetwerken.

Zie het hoofdstuk Optimalisatiegids over &quot;Portfolio beheren&quot;, dat beschikbaar is in Zoeken, Sociale &amp; Handel, voor meer informatie over de beschikbare portfolioopties en hoe u portfolio&#39;s kunt instellen.<!-- verify convention for referencing Optimization Guide here -->

## Weergaven van het campagnebeheer

Met de weergaven voor campagnebeheer kunt u uw zoekaccounts controleren en beheren. De volgende weergaven zijn beschikbaar:

* **[!UICONTROL Campaigns]** — De [!UICONTROL Campaigns] de meningen tonen gegevens van elke verbonden en netwerkrekening. U kunt kosten bekijken, klikken, indruk, en opbrengstgegevens over alle rekeningen van het advertentienetwerk en over individuele rekeningen, campagnes, en groepen, sleutelwoorden, advertenties, het winkelen productgroepen, plaatsingen, autodoelstellingen (dynamische onderzoeksdoelstellingen), publiek, en de bibliotheken van de toevoegingsuitbreiding en hun bijbehorende rekeningsentiteiten. Voor [ondersteunde campagneretypen op ondersteunde advertentienetwerken](/help/search-social-commerce/introduction/supported-inventory.md)kunt u gegevens voor afzonderlijke campagnes en campagnecomponenten rechtstreeks in de interface maken en bewerken. U kunt de gegevens in de meeste subweergaven optioneel exporteren naar een spreadsheetbestand.

   >[!NOTE]
   >
   >Gegevens op advertentieniveau zijn niet beschikbaar voor [!DNL Google Ads] dynamic search ad (DSA), performance max, smart shopping en [!DNL YouTube] campagnes.

* **[!UICONTROL Products]** — De [!UICONTROL Products] weergaven geven gegevens voor elke [[!DNL Google] or [!DNL Microsoft] gesynchroniseerde zakelijke account](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). De standaardwaarde [!UICONTROL Accounts] een overzicht van alle gesynchroniseerde accounts; sommige gebruikerstypen kunnen nieuwe accounts toevoegen vanuit deze weergave. De [!UICONTROL Products] In een subweergave wordt elk product in de account weergegeven.

* **[!UICONTROL Advanced (ACM)]** — Van de [!DNL Advanced] ([!DNL AMC]Voor de weergave Geavanceerd Campaign Management) kunt u geautomatiseerde processen instellen om [dynamische advertenties en trefwoorden voor elk object in je voorraad](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) volgens een ad-netwerkspecifieke advertentiesjabloon die u maakt en de inhoud van [!DNL Google Merchant Center] accounts of voorraadgegevensbestanden die u uploadt naar een FTP-locatie. Subviews bevatten details over elke voedersjabloon voor de adverteerder en elke campagne, advertentiegroep, trefwoord en advertentie die is opgenomen in een feed die is doorgegeven via een voedersjabloon maar niet naar het advertentienetwerk is gepost.

* **[!UICONTROL Bulksheets]** — Gebruik de [!UICONTROL Bulksheets] te maken weergave [bulksheet-bestanden](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) die zoveel gegevens bevatten als u wilt voor een account op een [ondersteund advertentienetwerk](/help/search-social-commerce/introduction/supported-inventory.md)en vervolgens naar het advertentienetwerk te posten.

* **[!UICONTROL Audiences]** — [De [!UICONTROL Audiences] views](/help/search-social-commerce/campaign-management/campaigns/audience-about.md) bevat alle [!DNL Google Ads] en [!DNL Microsoft Advertising] publiek dat wordt gegenereerd op basis van verschillende soorten gebruikerslijsten. U kunt [!DNL Google Ads] publiek van uw bestaande Adobe Experience Cloud-publiek en uw e-maillijsten van klanten. U kunt ook doelwitten en uitsluitingen voor uw publiek weergeven en beheren [!DNL Google Ads] en [!DNL Microsoft Advertising] advertenties.

* **[!UICONTROL Label Classifications]** — Gebruik deze weergave om te maken en te verwijderen [labelclassificaties](/help/search-social-commerce/campaign-management/label-classifications/classification-about.md), waarmee u uw labels kunt groeperen in betekenisvolle sets.

>[!MORELIKETHIS]
>
>* [Overzicht van het uitvoeren van en netwerkrekeningen en campagnes](campaign-implemention-overview.md)
>* [De prestaties van uw advertentienetwerkcampagnes bewaken en beheren](monitor-performance-campaigns.md)
>* [Google Ads-conversiegegevens in Zoeken, Sociale Zaken en Handel](google-conversion-data.md)

