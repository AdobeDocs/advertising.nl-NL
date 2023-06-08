---
title: Classificatiewaarden toewijzen aan accountcomponenten vanuit campagnebeheerweergaven
description: Leer hoe u classificatiewaarden toewijst aan accountcomponenten.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Classificatiewaarden toewijzen aan accountcomponenten vanuit campagnebeheerweergaven

U kunt classificatiewaarden voor de volgende zoekentiteiten toewijzen en verwijderen uit de weergaven voor campagnebeheer: campagne, advertentiegroep, trefwoord, advertentie, plaatsing, productgroep op eenheidsniveau en dynamisch zoekdoel. Indien nodig kunt u tijdens het toewijzingsproces classificaties en classificatiewaarden maken. Elke labelclassificatie kan tot 2000 waarden hebben.

Elke entiteit kan één labelwaarde per classificatie hebben. Shoes_Campaign kan bijvoorbeeld de kleurwaarde &quot;rood&quot; en de Geo-waarde &quot;Los Angeles&quot; hebben, maar niet meerdere waarden voor Kleur of Geo.

De waarden van het etiket worden geërft door kindentiteiten, zodat ga geen waarden voor kindentiteiten in tenzij u de geërfte waarden wilt met voeten treden.

>[!NOTE]
>
>Uw trefwoorden en advertentiekopie voor sommige advertentienetwerken en campagnetypen zijn [niet-veranderbaar](/help/search-social-commerce/campaign-management/faqs-campaigns.md), wat betekent dat bij het bewerken van deze methoden de bestaande entiteit wordt verwijderd en een nieuwe wordt gemaakt. Wanneer een bestaande entiteit op deze manier wordt geschrapt, wordt de etiketclassificatie niet toegewezen aan de nieuwe entiteit.

1. Klikken **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** en selecteer vervolgens de weergave van de accountcomponent.

1. Voer een van de volgende handelingen uit:

   * (Als u waarden wilt toewijzen aan één entiteit) Houd de cursor boven de naam van de entiteit. Klik op ![Knop Menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Knop Menu")en selecteer vervolgens **[!UICONTROL Classification]**.

   * (Ga als volgt te werk om waarden toe te wijzen aan een of meer entiteiten:

      * Schakel het selectievakje naast elke relevante rij in.

         Voor tips over het selecteren van meerdere rijen raadpleegt u &quot;[Meerdere rijen selecteren](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      * Klik op de werkbalk boven de tabel met gegevens op ![Meer](/help/search-social-commerce/assets/more.png "Meer")en klik vervolgens op **[!UICONTROL Classification]**.

1. In de [!UICONTROL Assignment Details]Voer een van de volgende handelingen uit:

   * Als u bestaande classificatiewaarden wilt wijzigen in nieuwe waarden, selecteert u **[!UICONTROL Set To]**.

      De maximumlengte voor elke waarde is 100 tekens en kan ASCII- en niet-ASCII-tekens bevatten.

   * Als u opgegeven classificatiewaarden wilt toewijzen zonder bestaande waarden te verwijderen, selecteert u **[!UICONTROL Assign]**.

   * Als u specifieke, momenteel toegewezen classificatiewaarden wilt verwijderen, selecteert u **[!UICONTROL Remove]**.

      Wanneer u een classificatiewaarde verwijdert, zijn de rapportgegevens voor de waarde niet meer beschikbaar voor de opgegeven accountcomponenten.

   * Als u opgegeven classificatiewaarden wilt verwijderen, selecteert u **[!UICONTROL Delete]**.

      Als u een classificatiewaarde verwijdert, is deze niet meer beschikbaar voor toekomstig gebruik en zijn er geen rapportgegevens meer beschikbaar voor de waarde. Alle toewijzingen tussen de waarden en specifieke accountcomponenten worden verwijderd, maar de accountcomponenten worden niet verwijderd.

1. Voer voor elke toepasselijke indelingswaarde de volgende handelingen uit:

   1. In de **[!UICONTROL Classification]** kolom, geef de classificatienaam op:

      * Als u een bestaande classificatie wilt gebruiken, klikt u op de classificatienaam om deze uit te vouwen.

      * Als u een classificatie wilt maken, klikt u op [!UICONTROL +]. Voer in het invoerveld de indelingsnaam in en klik op ![Opslaan](/help/search-social-commerce/assets/select.png "Opslaan") om de classificatie onmiddellijk op te slaan.

         De naam moet bestaan uit [ASCII-tekens 32-126](https://www.asciitable.com/)en de maximumlengte is 27 single-byte tekens.
   1. In de **[!UICONTROL Value Name]** Geef de naam van de waarde op:

      * Als u een bestaande waarde wilt gebruiken, klikt u op de naam van de waarde om deze te selecteren.

      * Als u een waarde wilt maken, klikt u op [!UICONTROL +]. Voer in het invoerveld de waarde in en klik op ![Opslaan](/help/search-social-commerce/assets/select.png "Opslaan") om de waarde direct op te slaan.

         De maximumlengte is 100 tekens en kan ASCII- en niet-ASCII-tekens bevatten.


1. (Optioneel) Voer aanvullende gegevens in:

   1. Volgende tot **[!UICONTROL Additional Details]**, klikt u op ![Openen](/help/search-social-commerce/assets/chevron-up.png "Openen") om de details uit te breiden.

   1. Voer een optionele **[!UICONTROL Project Name]** en/of facultatief **[!UICONTROL Description]**.

1. Klik op **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [Informatie over labelclassificaties](classification-about.md)
>* [Een labelclassificatie maken](classification-create.md)
>* [Classificatiewaarden toewijzen aan accountcomponenten met behulp van bulksbladen](classification-values-assign-bulksheets.md)
>* [Waarden voor labelclassificatie verwijderen uit accountcomponenten](classification-values-remove.md)
>* [Classificatiewaarden label verwijderen](classification-values-delete.md)
>* [Labelclassificaties verwijderen](classification-delete.md)

