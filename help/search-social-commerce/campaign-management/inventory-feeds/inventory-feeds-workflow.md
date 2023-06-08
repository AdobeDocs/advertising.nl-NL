---
title: Informatie over het automatiseren en beheren van voorraden
description: Meer informatie over de workflow voor het automatisch beheren van de accountstructuur en het leveren van dynamische advertenties op basis van gegevens over uw product- of servicevoorraad.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Workflow voor het beheer van campagnegegevens met behulp van voorraadfeeds

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (alleen handelingen verwijderen), en [!DNL Yandex] alleen accounts*

Eerst test u ten minste één feed-bestand of -account en vervolgens kunt u het proces volledig automatiseren of het bij elke stap blijven beheren:

1. (Optioneel) Neem contact op met uw Adobe-accountteam om een FTP-map in te stellen voor het opslaan van gegevensbestanden.

   Als u de FTP-map gebruikt, controleert de feed-service elke twee uur of er nieuwe bestanden zijn.

   Anders kunt u bestanden handmatig uploaden in het dialoogvenster [!UICONTROL Advanced (ACM)] weergeven.

1. Set [parameters voor de verwerking van voedergegevens](feed-settings-manage.md#feed-data-settings).

   Als u FTP gebruikt, post automatisch geen gegevens aan de advertentienetwerken aanvankelijk. Nadat u de uitvoer van het eerste bestand hebt gecontroleerd en tevreden bent met het resultaat, kunt u de instellingen wijzigen.

1. Upload een gegevensbestand naar de directory FTP. [een gegevensbestand handmatig uploaden](feed-files-manage.md) in de [!UICONTROL Advanced (ACM) view], of [toegang tot een Google- of Microsoft® Business Center-account mogelijk maken](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Als u bestanden handmatig wilt uploaden, kunt u wachten totdat u een sjabloon maakt waarin het gegevensbestand wordt gebruikt.

1. (Optioneel) Groepen maken van [modifiers](modifiers-manage.md) gebruiken als variabelen in verschillende gegevensvelden in voedergegevenssjablonen.

1. [Een of meer sjablonen maken](ad-templates/ad-template-manage.md) die de gegevenskolommen gebruiken om campagnes, ad groepen, sleutelwoorden, en/of exemplaren voor een specifieke ad netwerkrekening tot stand te brengen.

1. [Doorvoergegevens doorgeven via de sjablonen](feed-data-propagate.md), waardoor de kolomnamen in de sjabloon worden vervangen door gegevens in het bestand of de account. Afhankelijk van de sjabloonopties maakt u met Zoeken, Sociaal en Handel een nieuwe accountstructuur (campagnes, groepen en trefwoorden) voor advertenties met behulp van standaardinstellingen of wijst u de advertenties toe aan de bestaande accountstructuur.

1. (Optioneel) [De uitvoer voorvertonen](propagated-data-view.md) in de [!UICONTROL Advanced (ACM)] en eventueel een overzicht bekijken van de gegevenswijzigingen in het dialoogvenster [!UICONTROL Propagations] tab.

1. [Gegevens verzenden](propagated-data-post.md) aan de relevante advertentienetwerkrekeningen.

1. (Als u uw gegevens uploadt met FTP of een bedrijfscentrum-account; (optioneel) Nadat u de uitvoer van het eerste feed-bestand hebt gevalideerd, [de parameters bewerken](feed-settings-manage.md#feed-data-settings) om verdere gegevens door de bijbehorende malplaatjes automatisch te verspreiden en het te posten aan relevante ad netwerken.

1. (Wanneer u nieuwe gegevensdossiers hebt) zonodig, upload nieuwe dossiers, verspreidt de gegevens door malplaatjes, en post de gegevens aan het relevante ad netwerk. U kunt de gegevens desgewenst in één stap verspreiden en plaatsen.

>[!MORELIKETHIS]
>
>* [Informatie over het automatiseren en beheren van voorraden](inventory-feeds-about.md)
>* [Wanneer worden accountcomponenten gemaakt of verwijderd door voorraadfeeds?](when-are-components-created-deleted.md)

