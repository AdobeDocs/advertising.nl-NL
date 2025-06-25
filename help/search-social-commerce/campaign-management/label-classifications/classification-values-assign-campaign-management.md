---
title: Classificatiewaarden toewijzen aan accountcomponenten vanuit campagnebeheerweergaven
description: Leer hoe u classificatiewaarden toewijst aan accountcomponenten.
exl-id: 5a3cb059-9cff-4a2e-b8aa-be8626774377
feature: Search Label Classifications
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# Classificatiewaarden toewijzen aan accountcomponenten vanuit campagnebeheerweergaven

U kunt classificatiewaarden voor de volgende zoekentiteiten toewijzen en verwijderen uit de campagnebeheerweergaven: campagne, ad-groep, trefwoord, advertentie, plaatsing, productgroep op eenheidsniveau en dynamisch zoekdoel. Indien nodig kunt u tijdens het toewijzingsproces classificaties en classificatiewaarden maken. Elke labelclassificatie kan tot 2000 waarden hebben.

Elke entiteit kan één labelwaarde per classificatie hebben. Shoes_Campaign kan bijvoorbeeld de kleurwaarde &quot;rood&quot; en de Geo-waarde &quot;Los Angeles&quot; hebben, maar niet meerdere waarden voor Kleur of Geo.

De waarden van het etiket worden geërft door kindentiteiten, zodat ga geen waarden voor kindentiteiten in tenzij u de geërfte waarden wilt met voeten treden.

>[!NOTE]
>
>Uw sleutelwoorden en advertentiekopie voor sommige advertentienetwerken en campagneretypes zijn [ niet-veranderbaar ](/help/search-social-commerce/campaign-management/faqs-campaigns.md), zo betekent het dat het uitgeven van hen de bestaande entiteit schrapt en tot nieuwe leidt. Wanneer een bestaande entiteit op deze manier wordt geschrapt, wordt de etiketclassificatie niet toegewezen aan de nieuwe entiteit.

1. Klik op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** en selecteer vervolgens de weergave van de accountcomponent.

1. Voer een van de volgende handelingen uit:

   * (Om waarden aan één enkele entiteit toe te wijzen) Houd de curseur over de entiteitsnaam, klik ](/help/search-social-commerce/assets/arrow-dropdown-menu.png " knoop van het Menu "), en selecteer dan **[!UICONTROL Classification]**.![

   * (Ga als volgt te werk om waarden toe te wijzen aan een of meer entiteiten:

      * Schakel het selectievakje naast elke relevante rij in.

        Voor uiteinden bij het selecteren van veelvoudige rijen, zie &quot;[ Uitgezochte veelvoudige rijen ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      * In de toolbar boven de gegevenslijst, klik ![ Meer ](/help/search-social-commerce/assets/more.png " "), en klik dan **[!UICONTROL Classification]**.

1. Voer in het [!UICONTROL Assignment Details] een van de volgende handelingen uit:

   * Selecteer **[!UICONTROL Set To]** als u bestaande classificatiewaarden wilt wijzigen in nieuwe waarden.

     De maximumlengte voor elke waarde is 100 tekens en kan ASCII- en niet-ASCII-tekens bevatten.

   * Selecteer **[!UICONTROL Assign]** als u opgegeven classificatiewaarden wilt toewijzen zonder bestaande waarden te verwijderen.

   * Selecteer **[!UICONTROL Remove]** als u specifieke, momenteel toegewezen classificatiewaarden wilt verwijderen.

     Wanneer u een classificatiewaarde verwijdert, zijn de rapportgegevens voor de waarde niet meer beschikbaar voor de opgegeven accountcomponenten.

   * Selecteer **[!UICONTROL Delete]** als u opgegeven classificatiewaarden wilt verwijderen.

     Als u een classificatiewaarde verwijdert, is deze niet meer beschikbaar voor toekomstig gebruik en zijn er geen rapportgegevens meer beschikbaar voor de waarde. Alle toewijzingen tussen de waarden en specifieke accountcomponenten worden verwijderd, maar de accountcomponenten worden niet verwijderd.

1. Voer voor elke toepasselijke indelingswaarde de volgende handelingen uit:

   1. Geef in de kolom **[!UICONTROL Classification]** de classificatienaam op:

      * Als u een bestaande classificatie wilt gebruiken, klikt u op de classificatienaam om deze uit te vouwen.

      * Klik op [!UICONTROL +] om een classificatie te maken. Op het inputgebied, ga de classificatienaam in, en klik dan ![ sparen ](/help/search-social-commerce/assets/select.png " ") om de classificatie onmiddellijk te bewaren.

        De naam moet uit [ karakters 32-126 van ASCII ](https://www.asciitable.com/) bestaan, en de maximumlengte is 27 single-byte karakters.

   1. Geef in de kolom **[!UICONTROL Value Name]** de naam van de waarde op:

      * Als u een bestaande waarde wilt gebruiken, klikt u op de naam van de waarde om deze te selecteren.

      * Klik op [!UICONTROL +] om een waarde te maken. Op het inputgebied, ga de waarde in, en klik dan ![ sparen ](/help/search-social-commerce/assets/select.png " ") om de waarde onmiddellijk te bewaren.

        De maximumlengte is 100 tekens en kan ASCII- en niet-ASCII-tekens bevatten.

1. (Optioneel) Voer aanvullende gegevens in:

   1. Naast **[!UICONTROL Additional Details]**, klik ![ Open ](/help/search-social-commerce/assets/chevron-up.png " ") om de details uit te breiden.

   1. Voer een optionele **[!UICONTROL Project Name]** en/of optionele **[!UICONTROL Description]** in.

1. Klik op **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [ Ongeveer etiketclassificaties ](classification-about.md)
>* [ creeer een etiketclassificatie ](classification-create.md)
>* [ wijs classificatiewaarden aan rekeningscomponenten toe gebruikend bulksheets ](classification-values-assign-bulksheets.md)
>* [ verwijdert de waarden van de etiketclassificatie uit rekeningscomponenten ](classification-values-remove.md)
>* [ schrapt etiketclassificatiewaarden ](classification-values-delete.md)
>* [ schrapt etiketclassificaties ](classification-delete.md)
