---
title: Classificatiewaarden toewijzen aan accountcomponenten met behulp van bulksbladen
description: Leer hoe u met opsommingstekens classificatiewaarden kunt toewijzen aan accountcomponenten.
exl-id: b2dfd487-097c-45f8-a6a5-24395fdb2b85
feature: Search Label Classifications
source-git-commit: d68107b04762ea149dd74fb30ab7ea9d8850915f
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---

# Classificatiewaarden toewijzen aan accountcomponenten met behulp van bulksbladen

U kunt labelclassificaties aan waarden voor de volgende zoekentiteiten koppelen met behulp van bulksbladen: campagne, ad groep, trefwoord, ad, placement, productgroep op eenheidsniveau en dynamisch zoekdoel. Elke labelclassificatie kan tot 2000 waarden hebben.

Elke entiteit kan één labelwaarde per classificatie hebben. Shoes_Campaign kan bijvoorbeeld de kleurwaarde &quot;rood&quot; en de Geo-waarde &quot;Los Angeles&quot; hebben, maar niet meerdere waarden voor Kleur of Geo.

De waarden van het etiket worden geërft door kindentiteiten, zodat ga geen waarden voor kindentiteiten in tenzij u de geërfte waarden wilt met voeten treden.

>[!NOTE]
>
>Uw sleutelwoorden en advertentiekopie voor sommige advertentienetwerken en campagneretypes zijn [ niet-veranderbaar ](/help/search-social-commerce/campaign-management/faqs-campaigns.md), zo betekent het dat het uitgeven van hen de bestaande entiteit schrapt en tot nieuwe leidt. Wanneer een bestaande entiteit op deze manier wordt geschrapt, wordt de etiketclassificatie niet toegewezen aan de nieuwe entiteit.

1. [ Download een bulksheet ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) dat de entiteiten omvat waaraan u de waarden van de etiketclassificatie wilt toewijzen:

   * Vouw op het tabblad [!UICONTROL Rows and Columns] de lijst [!UICONTROL Campaign] in het deelvenster [!UICONTROL Bulksheet Columns] uit.

   * Vouw de lijst [!UICONTROL Label Classification] uit.

   * Selecteer elke classificatie waarvoor u een kolom in het bulkbladbestand wilt opnemen.

     Als u bijvoorbeeld de labelclassificaties &quot;Kleur&quot; en &quot;Geo&quot; opneemt, bevat het opsommingsteken de kolommen &quot;Kleur&quot; en &quot;Geo&quot;.

1. Open het bestand in een editor en voeg labelwaarden toe aan de kolommen met labelclassificatie voor de entiteiten waaraan u deze wilt koppelen. De maximumlengte voor elke waarde is 100 tekens en kan ASCII- en niet-ASCII-tekens bevatten.

   Zie de voorbeeldwaarden in de volgende sectie.

   Naast het toevoegen van waarden, kunt u bestaande waarden ook schrappen door hen uit de relevante rijen te verwijderen. Om waarden te verwijderen uit zowel een moederentiteit als haar onderliggende entiteiten, ofwel a) alleen de rij van de moederentiteit opnemen en de bestaande classificatiewaarde verwijderen, ofwel b) zowel de moederentiteit als haar onderliggende entiteiten opnemen, en de bestaande classificatiewaarde verwijderen uit alle bovenliggende en onderliggende rijen.

1. [ upload het dossier ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) om de verenigingen tot stand te brengen.<!-- Update once the new bulksheet UI is GA -->

De geüploade labelwaarden zijn zichtbaar in de relevante entiteitsweergaven.

## Voorbeeld van classificatiewaarden van label die in bulksbladen moeten worden geüpload

Dit voorbeeld bevat kolommen voor de labelindelingen &quot;Color&quot; en &quot;Geo&quot;. Voor uw eigen bulksbladen, substitueer kolommen voor uw eigen namen van de etiketclassificatie.

| Account | Campagne | Advertentiegroep | Trefwoord | Advertentie | Plaatsing | Labels | Kleur | Geo |
|---|---|---|---|---|---|---|---|---|
| ACT1 | C1 | | | | | | Groen | |
| ACT1 | C1 | AG1 | | | | | | |
| ACT1 | C1 | AG1 | K1 | | | | | VK |
| ACT1 | C1 | AG1 | K2 | | | | Rood | AU |
| ACT1 | C1 | AG1 | K3 | | | | Blauw | DE |
| ACT1 | C1 | AG1 | | A1 | | | | |
| ACT1 | C1 | AG1 | | A1 | | | Rood | |
| ACT1 | C1 | AG1 | | | P1 | | Rood | AU |
| ACT1 | C1 | AG1 | | | P2 | | Blauw | DE |

>[!MORELIKETHIS]
>
>* [ Ongeveer etiketclassificaties ](classification-about.md)
>* [ creeer een etiketclassificatie ](classification-create.md)
>* [ wijs classificatiewaarden aan rekeningscomponenten van de meningen van het campagnebeheer toe ](classification-values-assign-campaign-management.md)
>* [ verwijdert de waarden van de etiketclassificatie uit rekeningscomponenten ](classification-values-remove.md)
>* [ schrapt etiketclassificatiewaarden ](classification-values-delete.md)
>* [ schrapt etiketclassificaties ](classification-delete.md)
