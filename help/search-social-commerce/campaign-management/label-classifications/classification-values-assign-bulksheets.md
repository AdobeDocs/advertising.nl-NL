---
title: Classificatiewaarden toewijzen aan accountcomponenten met behulp van bulksbladen
description: Leer hoe u met opsommingstekens classificatiewaarden kunt toewijzen aan accountcomponenten.
exl-id: 9bb38f28-d6bc-41f4-9c28-b391d9b9e412
feature: Search Label Classifications
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 6%

---

# Classificatiewaarden toewijzen aan accountcomponenten met behulp van bulksbladen

U kunt labelclassificaties aan waarden voor de volgende zoekentiteiten koppelen met behulp van bulksbladen: campagne, ad groep, trefwoord, ad, placement, productgroep op eenheidsniveau en dynamisch zoekdoel. Elke labelclassificatie kan tot 2000 waarden hebben.

Elke entiteit kan één labelwaarde per classificatie hebben. Shoes_Campaign kan bijvoorbeeld de kleurwaarde &quot;rood&quot; en de Geo-waarde &quot;Los Angeles&quot; hebben, maar niet meerdere waarden voor Kleur of Geo.

De waarden van het etiket worden geërft door kindentiteiten, zodat ga geen waarden voor kindentiteiten in tenzij u de geërfte waarden wilt met voeten treden.

>[!NOTE]
>
>Uw trefwoorden en advertentiekopie voor sommige advertentienetwerken en campagnetypen zijn [niet-veranderbaar](/help/search-social-commerce/campaign-management/faqs-campaigns.md), wat betekent dat bij het bewerken van deze methoden de bestaande entiteit wordt verwijderd en een nieuwe wordt gemaakt. Wanneer een bestaande entiteit op deze manier wordt geschrapt, wordt de etiketclassificatie niet toegewezen aan de nieuwe entiteit.

1. [Een werkblad downloaden](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) die de entiteiten omvat waaraan u de waarden van de etiketclassificatie wilt toewijzen:

   * Op de [!UICONTROL Rows and Columns] tabblad, vouwt u de [!UICONTROL Campaign] in de lijst [!UICONTROL Bulksheet Columns] venster.

   * Breid uit [!UICONTROL Label Classification] lijst.

   * Selecteer elke classificatie waarvoor u een kolom in het bulkbladbestand wilt opnemen.

     Als u bijvoorbeeld de labelclassificaties &quot;Kleur&quot; en &quot;Geo&quot; opneemt, bevat het opsommingsteken de kolommen &quot;Kleur&quot; en &quot;Geo&quot;.

1. Open het bestand in een editor en voeg labelwaarden toe aan de kolommen met labelclassificatie voor de entiteiten waaraan u deze wilt koppelen. De maximumlengte voor elke waarde is 100 tekens en kan ASCII- en niet-ASCII-tekens bevatten.

   Zie de voorbeeldwaarden in de volgende sectie.

   Naast het toevoegen van waarden, kunt u bestaande waarden ook schrappen door hen uit de relevante rijen te verwijderen. Om waarden te verwijderen uit zowel een moederentiteit als haar onderliggende entiteiten, ofwel a) alleen de rij van de moederentiteit opnemen en de bestaande classificatiewaarde verwijderen, ofwel b) zowel de moederentiteit als haar onderliggende entiteiten opnemen, en de bestaande classificatiewaarde verwijderen uit alle bovenliggende en onderliggende rijen.

1. [Het bestand uploaden](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) om de verenigingen op te richten.

De geüploade labelwaarden zijn zichtbaar in de relevante entiteitsweergaven.

## Voorbeeld van classificatiewaarden van label die in bulksbladen moeten worden geüpload

Dit voorbeeld bevat kolommen voor de labelindelingen &quot;Color&quot; en &quot;Geo&quot;. Voor uw eigen bulksbladen, substitueer kolommen voor uw eigen namen van de etiketclassificatie.

| Account | Campagne | Advertentiegroep | Trefwoord | Advertentie | Plaatsing | Labels | Kleur | Geo |
|---|---|---|---|---|---|---|---|---|
| Acct1 | C1 | | | | | | Groen | |
| Acct1 | C1 | AG1 | | | | | | |
| Acct1 | C1 | AG1 | K1 | | | | | VK |
| Acct1 | C1 | AG1 | K2 | | | | Rood | AU |
| Acct1 | C1 | AG1 | K3 | | | | Blauw | DE |
| Acct1 | C1 | AG1 | | A1 | | | | |
| Acct1 | C1 | AG1 | | A1 | | | Rood | |
| Acct1 | C1 | AG1 | | | P1 | | Rood | AU |
| Acct1 | C1 | AG1 | | | P2 | | Blauw | DE |

>[!MORELIKETHIS]
>
>* [Informatie over labelclassificaties](classification-about.md)
>* [Een labelclassificatie maken](classification-create.md)
>* [Classificatiewaarden toewijzen aan accountcomponenten vanuit campagnebeheerweergaven](classification-values-assign-campaign-management.md)
>* [Waarden voor labelclassificatie verwijderen uit accountcomponenten](classification-values-remove.md)
>* [Classificatiewaarden label verwijderen](classification-values-delete.md)
>* [Labelclassificaties verwijderen](classification-delete.md)
