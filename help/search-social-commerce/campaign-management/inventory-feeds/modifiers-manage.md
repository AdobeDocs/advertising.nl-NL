---
title: Wijzigingsopties beheren
description: Leer hoe u modifiers voor uw advertentiesjablonen voor de invoer van inventarisgegevens configureert en beheert.
exl-id: 74c9a7c7-0979-4f78-9225-43bc6c94acd7
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Wijzigingstoetsen beheren

*[!DNL Google Ads], [!DNL Microsoft Advertising] , [!DNL Yahoo! Japan Ads] (alleen acties verwijderen) en [!DNL Yandex] alleen accounts*

Modifiers zijn adjectives of adverbs die kunnen worden toegevoegd aan of verwijderd uit een zin zonder de basisstructuur van de zin te wijzigen. U kunt groepen modifiers tot stand brengen om als variabelen in diverse gegevensgebieden in de malplaatjes van voedergegevens te gebruiken. Door wijzigingstoetsen op te nemen in de velden accountstructuur (campagne en advertentiegroep), trefwoorden, basis-URL&#39;s en advertenties, maakt u één waarde voor elke bijbehorende wijzigingwaarde. Als u bijvoorbeeld een modifier-groepsvariabele in een advertentiecoloptekst gebruikt en de modifier-groep drie wijzigingstoetsen bevat (&quot;goedkoop&quot;, &quot;korting&quot; en &quot;betaalbaar&quot;), worden er drie aparte advertenties gemaakt voor elke gegevensrij in de gegevensinvoer — één voor elke modifier. Als u een wijziginggroep met meerdere waarden opneemt in de basis-URL voor een advertentiegroep, wordt er één set trefwoorden gemaakt voor elk van de resulterende basis-URL&#39;s.

Elke wijziginggroep kan zoveel opties bevatten als u wilt. Elke sjabloon kan slechts één wijziginggroep gebruiken.

## Een wijziginggroep maken

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** .

1. Klik in de werkbalk boven de gegevenstabel op **[!UICONTROL Modifiers]** .

1. Klik boven de lijst met wijziginggroepen op **[!UICONTROL Create]** .

1. Geef de instellingen voor de wijzigingengroep op:

   **[!UICONTROL Name]:** De naam van de bepalingsgroep.

   **[!UICONTROL Modifiers]:** De wijzigingwaarden voor de groep (één per regel).

1. Klik op **[!UICONTROL Save]**.

## Een wijzigingsgroep bewerken

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** .

1. Klik in de werkbalk boven de gegevenstabel op **[!UICONTROL Modifiers]** .

1. Klik in de lijst met wijziginggroepen op de naam van de wijziginggroep.

1. Bewerk de instellingen van de wijzigingengroep:

   **[!UICONTROL Name]:** De naam van de bepalingsgroep.

   **[!UICONTROL Modifiers]:** De wijzigingwaarden voor de groep (één per regel).

1. Klik op **[!UICONTROL Save]**.

## Modificatiegroepen verwijderen

>[!IMPORTANT]
>
>Wanneer u een wijziginggroep verwijdert, verwijdert u alle variabelen voor die wijziginggroep (aangeduid als `<modifier_group_name>` ) uit de velden met bestaande sjablonen. Als u probeert om gegevens door een malplaatje te verspreiden gebruikend variabelen voor bepalingen die niet bestaan, ontbreekt de baan1.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** .

1. Klik in de werkbalk boven de gegevenstabel op **[!UICONTROL Modifiers]** .

1. Schakel het selectievakje in naast elke wijzigingsgroep die u wilt verwijderen.

1. Klik boven de lijst met wijziginggroepen op **[!UICONTROL Delete]** .

1. Klik in het bevestigingsbericht op **[!UICONTROL Yes]** .

1. (Indien nodig) [ verwijder verwijzingen naar de bepaling ](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) van alle toepasselijke malplaatjes.

>[!MORELIKETHIS]
>
>* [ Ongeveer inventarisvoer ](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [ beheer en malplaatjes ](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
