---
title: Beheren [!DNL Microsoft Advertising] dynamisch hermarketingpubliek
description: Leer hoe u creeert en beheert [!DNL Microsoft Advertising] dynamisch hermarketingpubliek.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Beheren [!DNL Microsoft Advertising] dynamisch hermarketingpubliek

*[!DNL Microsoft Advertising]alleen accounts*

U kunt een [!DNL Microsoft Advertising] het dynamische publiek voor opnieuw op de markt brengen wanneer u de conversie- en publiekstrackingtag JavaScript van het zoekprogramma op uw webpagina&#39;s gebruikt. Elk publiek wordt gemaakt met een opgegeven tag die wordt opgenomen in de webpagina&#39;s waarvan de gebruikers het publiek zullen vormen. U kunt meerdere soorten publiek maken met dezelfde tag voor bijhouden. U kunt ook de naam en de gegevensbron voor bestaande doelgroepen wijzigen of bestaande doelgroepen verwijderen.

Dynamisch hermarketingpubliek heeft het type publiek &quot;[!UICONTROL Dynamic Remarketing] \&lt;visitor type=&quot;&quot;>&quot; (zoals &quot;Dynamische opmerkingverleden kopers&quot;).

Zie voor meer informatie over dynamische remarketing en het implementeren van de vereiste JavaScript-tag de [[!DNL Microsoft Advertising] documentatie over dynamische remarketing](https://help.ads.microsoft.com/#apex/ads/en/56910).

## Een dynamisch publiek voor opnieuw marketing maken

>[!NOTE]
>
>Voor [!DNL Microsoft Advertising] accounts, moet de JavaScript-tag de [product-id en paginatypeparameters](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. De naam van de [!DNL Microsoft Advertising] Label voor Universal Event Tracking (UET) dat is opgenomen in de webpagina&#39;s van waaruit het publiek wordt gemaakt.

   U hebt de tagnaam in een latere stap nodig.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Klik op de werkbalk boven de tabel met gegevens op ![Maken](/help/search-social-commerce/assets/add.png "Maken").

1. Selecteer het advertentienetwerk en de accountnaam en klik vervolgens op **[!UICONTROL Continue]**.

1. Geef de publieksinformatie op:

   1. In de **[!UICONTROL Data Source]** menu, selecteert u **[!UICONTROL Dynamic Remarketing List]**.

   1. Voer de **[!UICONTROL Audience Name]**.

   1. Selecteer de naam van de [!DNL Microsoft Advertising] De tag UET die is opgenomen in de webpagina&#39;s waarvan de gebruikers het publiek zullen vormen.

   1. Selecteer het type bezoeker voor het publiek, dat is gebaseerd op acties van bezoekers op de relevante webpagina&#39;s: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]*, of *[!UICONTROL Shopping Cart Abandoners]*.

   1. Geef het aantal **[!UICONTROL Membership Days]**, dit is het aantal dagen dat de cookie van een gebruiker in het publiek blijft. Waarden kunnen variëren van 1 (1) tot 180.

      Gebruik de tijdsduur waarvan u verwacht dat uw advertentie relevant is voor de gebruiker.

1. Klik op **[!UICONTROL Post]**.

>[!NOTE]
>
>Uw [!DNL Microsoft Advertising] dynamische lijsten voor het opnieuw in de handel brengen komen in aanmerking om zich te richten zodra zij ten minste 300 gebruikers omvatten.

## Een dynamisch publiek voor opnieuw marketing bewerken

U kunt de naam en de gegevensbron wijzigen voor een [!DNL Microsoft Advertising] dynamisch hermarketingpubliek. U kunt de waarde van de optie [!UICONTROL Membership Days] instellen.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Schakel het selectievakje naast het publiek dat u wilt bewerken in.

1. Klik op de werkbalk boven de tabel met gegevens op ![Bewerken](/help/search-social-commerce/assets/edit.png "Bewerken").

1. Bewerk de publieksinformatie:

   1. In de **[!UICONTROL Data Source]** sectie, klikt u op ![Bewerken](/help/search-social-commerce/assets/edit.png "Bewerken").

   1. (Optioneel) Wijzig de **[!UICONTROL Audience Name]**.

   1. (Optioneel) Wijzig de naam van de [!DNL Microsoft Advertising] De tag UET die is opgenomen in de webpagina&#39;s waarvan de gebruikers het publiek zullen vormen.

   1. (Optioneel) Wijzig het type bezoeker voor het publiek, dat is gebaseerd op acties van bezoekers op de relevante webpagina&#39;s: *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]*, of *[!UICONTROL Shopping Cart Abandoners]*.

   1. Klik op **[!UICONTROL Post]**.

## Een dynamisch publiek voor opnieuw marketing verwijderen

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. (Optioneel) Filter de lijst om specifieke doelgroepen op te nemen.

1. Schakel het selectievakje naast elk publiek dat u wilt verwijderen in.

   Voor tips over het selecteren van meerdere rijen raadpleegt u &quot;[Meerdere rijen selecteren](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Klik in het bevestigingsbericht op **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Informatie over publiek](audience-about.md)
>* [Maken [!DNL Google Ads] klant stemt doelgroep van [!DNL Adobe] publiek](google-audience-from-adobe-audience.md)
>* [Een [!DNL Google Ads] klant stemt publiek van een Adobe Campaign e-maillijst overeen](google-audience-from-campaign-email-list.md)
>* [Beheer klanten gelijke soorten publiek gebruikend de lijsten van klantengegevens](audience-from-customer-data-list.md)

