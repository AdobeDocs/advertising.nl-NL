---
title: Beheer  [!DNL Google Ads]  plaatsen
description: Leer hoe te om biddable plaatsen voor  [!DNL Google Ads]  ad groepen tot stand te brengen en te beheren.
exl-id: 80cb6fc6-e778-4b19-9e52-e0b57bde0d73
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# [!DNL Google Ads] -plaatsingen beheren

*[!DNL Google Ads]alleen accounts*

U kunt plaatsen voor ad groepen in [&#x200B; gesteunde campagneretypes &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md) tot stand brengen en uitgeven die het vertoningsnetwerk binnen a [&#x200B; gesynchroniseerde en netwerkrekening &#x200B;](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md) richten

## [!DNL Google Ads] plaatsen maken

>[!TIP]
>
>Om vele plaatsen tezelfdertijd tot stand te brengen, gebruik [&#x200B; campagnebulksbladen &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** . Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]** .

1. &#x200B;
   1. In de toolbar boven de gegevenslijst, leidt de klik ![&#x200B; &#x200B;](/help/search-social-commerce/assets/add.png " tot ").

1. Selecteer het advertentienetwerk, de account, de campagne en de advertentiegroep en klik op **[!UICONTROL Continue]** .

1. Vorm de [&#x200B; plaatsingsmontages &#x200B;](#placement-settings).

1. Klik op **[!UICONTROL Post]**.

## Plaatsen [!DNL Google Ads] bewerken

>[!TIP]
>
>Om vele plaatsen in één keer uit te geven, gebruik [&#x200B; campagnebulksbladen &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** . Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]** .

1. Schakel het selectievakje naast elke rij die u wilt bewerken in.

   Voor uiteinden bij het selecteren van veelvoudige rijen, zie &quot;[&#x200B; Uitgezochte veelvoudige rijen &#x200B;](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. In de toolbar boven de gegevenslijst, geeft de klik ![&#x200B; &#x200B;](/help/search-social-commerce/assets/edit.png " uit ").

1. Bewerk de [&#x200B; plaatsingsmontages &#x200B;](#placement-settings).

   Bij meerdere plaatsingen worden de wijzigingen toegepast op alle geselecteerde plaatsingen. Voor sommige alfanumerieke velden kunt u bestaande waarden wijzigen in een opgegeven waarde, een bestaande tekenreeks vervangen door een opgegeven tekenreeks, een opgegeven voorvoegsel toevoegen aan het begin van elke waarde of een achtervoegsel toevoegen aan het einde van elke waarde. Voor sommige monetaire velden kunt u bestaande waarden wijzigen in een opgegeven waarde of het bedrag met een bepaald percentage of een bepaald geldbedrag verhogen of verlagen, met een limiet.

1. Sla de gegevens op:

   * (Enkele plaatsen) Klik op **[!UICONTROL Post]** .

   * (Meerdere plaatsen) Klik op **[!UICONTROL Post Now]** .

## Plaatsingsinstellingen {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** Plaatsen op het inhoudsnetwerk waarop uw advertentie kan verschijnen. Voer een geldige URL in, bijvoorbeeld www.example.com, example.com of www.example.com/shoes/kids. Als u meerdere tekenreeksen wilt opgeven, scheidt u deze met komma&#39;s of voert u ze op afzonderlijke regels in. URL kan geen vraagteken (`?`) omvatten. **Nota:** u kunt [&#x200B; websiteplaatsing &#x200B;](placement-negative-create.md) van [!UICONTROL Placements] uitsluiten > [!UICONTROL Negatives] mening en in de ad groep en campagnemontages.

**[!UICONTROL Status]:** de vertoningsstatus van de plaatsing: *Actief* (om het bieden toe te laten; het gebrek), *Gepauzeerd* (om het bieden onbruikbaar te maken), of *Geschrapt* (om de plaatsing te schrappen; bestaande plaatsen slechts).

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (Facultatief) de maximumkosten per klik (CPC) of kosten per duizend viewable beelden (vCPM) voor de op plaatsing-gebaseerde advertentie, afhankelijk van de strategie van de campagneaanbieding. Deze waarde overschrijft het bod op advertentieniveau.

<!-- If the placement is in a standard optimized portfolio, then the specified bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations. -->

### [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URL]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- note -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer plaatsen &#x200B;](placement-about.md)
>* [&#x200B; creeer negatieve plaatsingen &#x200B;](placement-negative-create.md)
>* [&#x200B; verander het statuut van plaatsingen en negatieve plaatsingen &#x200B;](placement-status-edit.md)
