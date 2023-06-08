---
title: Informatie over het automatiseren en beheren van voorraden
description: Leer meer over geavanceerd campagnebeheer, waarmee u automatisch de accountstructuur kunt beheren en dynamische advertenties kunt leveren op basis van gegevens over uw product- of servicevoorraad.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# Informatie over het automatiseren en beheren van voorraden

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (alleen handelingen verwijderen), en [!DNL Yandex] alleen accounts*

De [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] Dankzij de weergave voor geavanceerd campagnebeheer kunt u automatisch een structuur van een netwerkaccount maken en bijwerken en dynamische advertenties leveren op basis van gegevens over uw product- of servicevoorraad. U kunt nieuwe bestanden uploaden met productgegevens dagelijks of zo vaak als u wilt, of rechtstreeks koppelen naar een [!DNL Google] of [!DNL Microsoft®] zakelijke rekening. Met deze functie kunt u:

* Nieuwe campagnes maken op basis van geordende gegevensbronnen.

* Tekst en responsieve zoekopdrachten dynamisch bijwerken, [!DNL Google Ads] winkeladvertenties, of [!DNL Microsoft® Advertising] winkeladvertenties wanneer nieuwe gegevens worden verwerkt, met behulp van dynamische variabelen voor veranderbare gegevenselementen (zoals de prijs of de hoeveelheid). Elke keer dat u de gegevens wijzigt, worden de bestaande advertenties verwijderd en worden er nieuwe gemaakt.

* Pauzeert of verwijdert automatisch ad groepen, sleutelwoorden, en advertenties wanneer de voorraad onder een specifiek niveau, volgens een gespecificeerde einddatum daalt, of wanneer een bestaande component wordt weggelaten uit inputgegevens.

Als u uw advertenties wilt instellen, maakt u een voorraadfeed-sjabloon met variabelen (plaatsaanduidingen) en vervangt u de variabelen door de feitelijke gegevenskolommen uit een geüpload bestand of een [Google of Microsoft® Business Center-account dat wordt gesynchroniseerd](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). De variabelen kunnen ook wijzigingsgroepen bevatten die u hebt ingesteld in een bestand of afzonderlijke rijen in het bestand om meerdere advertenties, trefwoorden, campagnes of ad-groepen te maken voor elke toepasselijke rij in het gegevensbestand. Als u bijvoorbeeld een modifier-groepsvariabele in een advertentiekop gebruikt en de modifier-groep twee modifiers bevat (&quot;voor goedkoop&quot; en &quot;tegen een korting&quot;), worden twee aparte advertenties gemaakt voor elk product — één voor elke modifier. Voor [!DNL Google Ads] en [!DNL Microsoft® Advertising] dynamische zoekopdrachten kunt u ook waarden voor adverteerders opnemen.

| [!UICONTROL Ad Variation] Sjabloonsectie | Modifiers in Search, Social &amp; Commerce | Voederinhoud | Resulterende advertenties |
|----|----|----|----|
| Titel: Kopen op hoog niveau \{<i>Productcategorie</i>\} &lt;<i>CheapList</i>>.<br><br>Omschrijving 1: Uitgebreide inventarisatie van \{<i>Productnaam</i>\}.<br><br>Omschrijving 2: Beschikbaar op \{<i>Discontopercentage</i>\}% korting. | Waarden voor wijzigingsgroep &quot;CheapList&quot;:<br><br>&quot;voor goedkoop&quot;<br><br>&quot;tegen een korting&quot; | Productcategorie,productnaam,kortingspercentage<br>elektronica,iPods,10<br><br>kledingstuk,Hemden,15<br><br><b>Opmerking:</b> U kunt waarden scheiden met komma&#39;s of tabs. | <u>Koop geavanceerde elektronica voor goedkope producten.</u><br>Grote voorraad tabletten. Beschikbaar met 10% korting.<br><br><u>Koop geavanceerde elektronica tegen een korting.</u><br>Grote voorraad tabletten. Beschikbaar met 10% korting.<br><br><u>Koop hoogwaardige kleding voor goedkope producten.</u><br>Enorme inventarisatie van overhemden. Beschikbaar met 15% korting.<br><br><u>Koop hoogwaardige kleding tegen een korting.</u><br>Enorme inventarisatie van overhemden. Beschikbaar met 15% korting. |

Nadat u de advertenties hebt gegenereerd, kunt u deze desgewenst reviseren en vervolgens op het advertentienetwerk plaatsen.

>[!NOTE]
>Zie &quot;[Campagnegegevens beheren met behulp van bulksbladen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot;

>[!MORELIKETHIS]
>
>* [Workflow voor het beheer van campagnegegevens met behulp van voorraadfeeds](inventory-feeds-workflow.md)
>* [Wanneer worden accountcomponenten gemaakt of verwijderd door voorraadfeeds?](when-are-components-created-deleted.md)

