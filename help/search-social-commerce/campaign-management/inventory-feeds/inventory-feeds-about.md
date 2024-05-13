---
title: Informatie over het automatiseren en beheren van voorraden
description: Leer meer over geavanceerd campagnebeheer, waarmee u automatisch de accountstructuur kunt beheren en dynamische advertenties kunt leveren op basis van gegevens over uw product- of servicevoorraad.
exl-id: 46e78f32-96ef-4a23-bbe3-f18b84309463
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# Informatie over het automatiseren en beheren van voorraden

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (alleen handelingen verwijderen), en [!DNL Yandex] alleen accounts*

De [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] Dankzij de weergave voor geavanceerd campagnebeheer kunt u automatisch een structuur van een netwerkaccount maken en bijwerken en dynamische advertenties leveren op basis van gegevens over uw product- of servicevoorraad. U kunt nieuwe bestanden uploaden met productgegevens dagelijks of zo vaak als u wilt, of rechtstreeks koppelen naar een [!DNL Google] of [!DNL Microsoft] zakelijke rekening. Met deze functie kunt u:

* Nieuwe campagnes bouwen van geordende gegevensbronnen.

* Tekst en responsieve zoekopdrachten dynamisch bijwerken, [!DNL Google Ads] winkeladvertenties, of [!DNL Microsoft Advertising] winkeladvertenties wanneer nieuwe gegevens worden verwerkt, met behulp van dynamische variabelen voor veranderbare gegevenselementen (zoals de prijs of de hoeveelheid). Elke keer dat u de gegevens wijzigt, worden de bestaande advertenties verwijderd en worden er nieuwe gemaakt.

* Pauzeert of verwijdert automatisch ad groepen, sleutelwoorden, en advertenties wanneer de voorraad onder een specifiek niveau, volgens een gespecificeerde einddatum daalt, of wanneer een bestaande component wordt weggelaten uit inputgegevens.

Als u uw advertenties wilt instellen, maakt u een voorraadfeed-sjabloon met variabelen (plaatsaanduidingen) en vervangt u de variabelen door de feitelijke gegevenskolommen uit een geüpload bestand of een [Google- of Microsoft-account voor handelscentra gesynchroniseerd](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). De variabelen kunnen ook wijzigingsgroepen bevatten die u hebt ingesteld in een bestand of afzonderlijke rijen in het bestand om meerdere advertenties, trefwoorden, campagnes of ad-groepen te maken voor elke toepasselijke rij in het gegevensbestand. Als u bijvoorbeeld een modifier-groepsvariabele in een advertentiekop gebruikt en de modifier-groep twee modifiers bevat (&quot;voor goedkoop&quot; en &quot;tegen een korting&quot;), worden twee aparte advertenties gemaakt voor elk product — één voor elke modifier. Voor [!DNL Google Ads] en [!DNL Microsoft Advertising] dynamische zoekopdrachten kunt u ook waarden voor adverteerders opnemen.

| [!UICONTROL Ad Variation] Sjabloonsectie | Modifiers in Search, Social &amp; Commerce | Voederinhoud | Resulterende advertenties |
|----|----|----|----|
| Titel: koop high-end \{<i>Productcategorie</i>\} &lt;<i>CheapList</i>>.<br><br>Beschrijving 1: Grote inventaris van \{<i>Productnaam</i>\}.<br><br>Beschrijving 2: Beschikbaar op \{<i>Korting percentage</i>\}% korting. | Waarden voor wijzigingsgroep &quot;CheapList&quot;:<br><br>&quot;voor goedkoop&quot;<br><br>&quot;tegen een korting&quot; | Productcategorie,productnaam,kortingspercentage<br>elektronica,iPods,10<br><br>kledingstuk,Hemden,15<br><br><b>Opmerking:</b> U kunt waarden scheiden met komma&#39;s of tabs. | <u>Koop geavanceerde elektronica voor goedkope producten.</u><br>Grote voorraad tabletten. Beschikbaar met 10% korting.<br><br><u>Koop geavanceerde elektronica tegen een korting.</u><br>Grote voorraad tabletten. Beschikbaar met 10% korting.<br><br><u>Koop hoogwaardige kleding voor goedkope producten.</u><br>Enorme inventarisatie van overhemden. Beschikbaar met 15% korting.<br><br><u>Koop hoogwaardige kleding tegen een korting.</u><br>Enorme inventarisatie van overhemden. Beschikbaar met 15% korting. |

Nadat u de advertenties hebt gegenereerd, kunt u deze desgewenst reviseren en vervolgens op het advertentienetwerk plaatsen.

>[!NOTE]
>Als u campagnegegevens bulksgewijs wilt maken of bewerken met spreadsheetbestanden, raadpleegt u &quot;[Campagnegegevens beheren met behulp van bulksbladen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot;

## Workflow voor het beheer van campagnegegevens met behulp van voorraadfeeds

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (alleen handelingen verwijderen), en [!DNL Yandex] alleen accounts*

Eerst test u ten minste één feed-bestand of -account en vervolgens kunt u het proces volledig automatiseren of het bij elke stap blijven beheren:

1. (Optioneel) Neem contact op met het accountteam van de Adobe om een FTP-map in te stellen voor het opslaan van gegevensbestanden.

   Als u de FTP-map gebruikt, controleert de feed-service elke twee uur of er nieuwe bestanden zijn.

   Anders kunt u bestanden handmatig uploaden in het dialoogvenster [!UICONTROL Advanced (ACM)] weergeven.

1. Set [parameters voor de verwerking van voedergegevens](feed-settings-manage.md#feed-data-settings).

   Als u FTP gebruikt, post automatisch geen gegevens aan de advertentienetwerken aanvankelijk. Nadat u de uitvoer van het eerste bestand hebt gecontroleerd en tevreden bent met het resultaat, kunt u de instellingen wijzigen.

1. Upload een gegevensbestand naar de directory FTP. [een gegevensbestand handmatig uploaden](feed-files-manage.md) in de [!UICONTROL Advanced (ACM) view], of [toegang verlenen tot een Google- of Microsoft-zakelijke centrumaccount](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Als u bestanden handmatig wilt uploaden, kunt u wachten totdat u een sjabloon maakt waarin het gegevensbestand wordt gebruikt.

1. (Optioneel) Groepen maken van [modifiers](modifiers-manage.md) gebruiken als variabelen in verschillende gegevensvelden in voedergegevenssjablonen.

1. [Een of meer sjablonen maken](ad-templates/ad-template-manage.md) die de gegevenskolommen gebruiken om campagnes, ad groepen, sleutelwoorden, en/of exemplaren voor een specifieke ad netwerkrekening tot stand te brengen.

1. [Doorvoergegevens doorgeven via de sjablonen](feed-data-propagate.md), waardoor de kolomnamen in de sjabloon worden vervangen door gegevens in het bestand of de account. Afhankelijk van de sjabloonopties maakt u met Zoeken, Sociaal en Commerce ofwel een nieuwe accountstructuur (campagnes, groepen en trefwoorden) voor de advertenties met de standaardinstellingen of wijst u de advertenties toe aan de bestaande accountstructuur.

1. (Optioneel) [De uitvoer voorvertonen](propagated-data-view.md) in de [!UICONTROL Advanced (ACM)] en eventueel een overzicht bekijken van de gegevenswijzigingen in het dialoogvenster [!UICONTROL Propagations] tab.

1. [De gegevens verzenden](propagated-data-post.md) aan de relevante advertentienetwerkrekeningen.

1. (Als u uw gegevens uploadt met FTP of een bedrijfscentrum-account; optioneel) Nadat u de uitvoer van het eerste feed-bestand hebt gevalideerd, [de parameters bewerken](feed-settings-manage.md#feed-data-settings) om verdere gegevens door de bijbehorende malplaatjes automatisch te verspreiden en het te posten aan relevante ad netwerken.

1. (Wanneer u nieuwe gegevensdossiers hebt) zonodig, upload nieuwe dossiers, verspreidt de gegevens door malplaatjes, en post de gegevens aan het relevante ad netwerk. U kunt de gegevens desgewenst in één stap verspreiden en plaatsen.

>[!MORELIKETHIS]
>
>* [Wanneer worden accountcomponenten gemaakt of verwijderd door voorraadfeeds?](when-are-components-created-deleted.md)
