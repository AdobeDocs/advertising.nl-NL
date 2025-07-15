---
title: Beperkingstoewijzingen voor campagnes beheren
description: Leer hoe u beperkingen aan campagnes kunt toewijzen.
feature: Search Optimization, Search Campaign Management
hide: true
source-git-commit: 62de95d7e3d21ae6c7f0a6f40e97352af71411e1
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# (Nieuwe interface) Beperkingstoewijzingen voor campagnes beheren

*eigenschap van Beta*

U kunt biedingsbeperkingen toewijzen en verwijderen voor de volgende zoekentiteiten: campagne, advertentiegroep, trefwoord, plaatsing, productgroep op eenheidsniveau en dynamisch zoekdoel. Elke entiteit kan slechts één beperking hebben.

Restricties worden overgeërfd door onderliggende entiteiten, zodat u geen beperkingen voor onderliggende entiteiten hoeft toe te wijzen, tenzij u de overgeërfde waarden wilt overschrijven.

Als u de toewijzing van een beperking opheft, wordt de koppeling met de accountcomponenten en alle onderliggende componenten verwijderd en zijn de rapportgegevens voor de beperking niet meer beschikbaar voor die componenten. Als u de toewijzing van een beperking opheft, worden de beperking en de accountcomponenten zelf niet verwijderd.

>[!NOTE]
>
>* Als u later een trefwoord of de advertentiekopie voor een advertentie bewerkt — waarbij een nieuw trefwoord of een nieuwe advertentie wordt gemaakt — wordt de beperking niet toegewezen aan de nieuwe entiteit.
>* Actieve beperkingen beperken alleen biedingen voor toegewezen biedingseenheden in geoptimaliseerde oudere portfolio&#39;s op trefwoordniveau. Ze worden genegeerd voor biedingseenheden in actieve portefeuilles, in hybride portefeuilles of niet in portfolio&#39;s.

## Beperk geselecteerde campagnes vanuit de nieuwe [!UICONTROL Campaigns] weergave tot een beperking

U kunt één beperking toewijzen aan een of meer campagnes.

1. Klik in het hoofdmenu op **[!UICONTROL Manage]>[!UICONTROL Campaigns]** .

1. Schakel het selectievakje naast elke campagne in waaraan u één beperking wilt toewijzen.

1. In de toolbar, klik ![ Meer Acties ](/help/search-social-commerce/assets/more-actions.png " Meer Acties ") **[!UICONTROL More Actions]** > ![Toewijzen](/help/search-social-commerce/assets/assign.png "Toewijzen") **[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Selecteer de restrictie.

1. Klik op **[!UICONTROL Assign Now]**.

## Beperk een beperking van de oude [!UICONTROL Campaigns] weergaven aan geselecteerde eenheden met zoekopdrachten

1. Selecteer in **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** de weergave van de accountcomponent.

1. Schakel het selectievakje naast elke relevante rij in.

   Voor uiteinden bij het selecteren van veelvoudige rijen, zie &quot;[ Uitgezochte veelvoudige rijen ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Klik in de werkbalk boven de datatabel op **[!UICONTROL More]** en klik vervolgens op **[!UICONTROL Assign]** > **[!UICONTROL Constraint]** .

1. Selecteer de toepasselijke beperking.

1. (Optioneel) Voer aanvullende gegevens in:

   1. Klik naast [!UICONTROL Additional Details] op **[!UICONTROL Open]** om de details uit te vouwen.

   1. Voer een optionele **[!UICONTROL Project Name]** en/of optionele **[!UICONTROL Description]** in.

1. Klik op **[!UICONTROL Save]**.

## Toewijzing van restricties uit geselecteerde campagnes ongedaan maken vanuit de nieuwe [!UICONTROL Campaigns] weergave

1. Klik in het hoofdmenu op **[!UICONTROL Manage]>[!UICONTROL Campaigns]** .

1. Schakel het selectievakje naast elke campagne uit waarvan u de toewijzing van beperkingen ongedaan maakt.

1. In de toolbar, klik ![ Meer Acties ](/help/search-social-commerce/assets/more-actions.png " Meer Acties ") **[!UICONTROL More Actions]** > ![Toewijzen](/help/search-social-commerce/assets/unassign.png "Toewijzen ongedaan maken") **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Klik op **[!UICONTROL Confirm]**.

## Toewijzing van beperkingen van zoekbiedingseenheden uit de oudere [!UICONTROL Campaigns] -weergaven ongedaan maken

>[!NOTE]
>
>Als u een beperking wilt verwijderen en deze niet meer beschikbaar wilt maken voor toekomstig gebruik, raadpleegt u &quot;Restricties voor zoekbiedingen verwijderen&quot; in het hoofdstuk over &quot;Bodrestricties&quot; in de Optimalisatiegids, die beschikbaar is in Zoeken, Sociaal en Commerce.<!-- verify convention for referencing Optimization Guide here -->

1. Selecteer in **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** de weergave van de accountcomponent.

1. Schakel het selectievakje in naast de componenten waaruit u de restrictie wilt verwijderen.

   Voor uiteinden bij het selecteren van veelvoudige rijen, zie &quot;[ Uitgezochte veelvoudige rijen ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Klik in de werkbalk boven de datatabel op **[!UICONTROL More]** en klik vervolgens op **[!UICONTROL Unassign]** > **[!UICONTROL Constraint]** .

1. Selecteer **[!UICONTROL Yes, Unassign]** in het bevestigingsdialoogvenster.

>[!MORELIKETHIS]
>
>* [ beheert beperkingstaken voor ad groepen ](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)

