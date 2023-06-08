---
title: Beheren [!DNL Google Ads] plaatsing
description: Meer informatie over het maken en beheren van plaatsingen voor [!DNL Google Ads] ad groepen.
source-git-commit: a24b51405bef1e73ed57b1cb9d012bdfbda9cdec
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# Beheren [!DNL Google Ads] plaatsing

*[!DNL Google Ads]alleen accounts*

U kunt plaatsingen voor advertentiegroepen maken en bewerken in [ondersteunde typen campagne](/help/search-social-commerce/introduction/supported-inventory.md) die zich richten op het weergavenetwerk binnen een [gesynchroniseerde netwerkaccount](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)

## Maken [!DNL Google Ads] plaatsing

>[!TIP]
>
>Als u veel plaatsen tegelijk wilt maken, gebruikt u [brochures](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]**.

1. 
   1. Klik op de werkbalk boven de tabel met gegevens op ![Maken](/help/search-social-commerce/assets/add.png "Maken").

1. Selecteer het advertentienetwerk, de account, de campagne en de advertentiegroep en klik vervolgens op **[!UICONTROL Continue]**.

1. Configureer de [plaatsingsinstellingen](#placement-settings).

1. Klik op **[!UICONTROL Post]**.

## Bewerken [!DNL Google Ads] plaatsing

>[!TIP]
>
>Als u veel plaatsen tegelijk wilt bewerken, gebruikt u [brochures](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]**.

1. Schakel het selectievakje naast elke rij die u wilt bewerken in.

   Voor tips over het selecteren van meerdere rijen raadpleegt u &quot;[Meerdere rijen selecteren](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Klik op de werkbalk boven de tabel met gegevens op ![Bewerken](/help/search-social-commerce/assets/edit.png "Bewerken") .

1. Bewerk de [plaatsingsinstellingen](#placement-settings).

   Bij meerdere plaatsingen worden de wijzigingen toegepast op alle geselecteerde plaatsingen. Voor sommige alfanumerieke velden kunt u bestaande waarden wijzigen in een opgegeven waarde, een bestaande tekenreeks vervangen door een opgegeven tekenreeks, een opgegeven voorvoegsel toevoegen aan het begin van elke waarde of een achtervoegsel toevoegen aan het einde van elke waarde. Voor sommige monetaire velden kunt u bestaande waarden wijzigen in een opgegeven waarde of het bedrag met een bepaald percentage of een bepaald geldbedrag verhogen of verlagen, met een limiet.

1. Sla de gegevens op:

   * (Enkele plaatsen) Klik **[!UICONTROL Post]**.

   * (Meerdere plaatsen) Klik op **[!UICONTROL Post Now]**.

## Plaatsingsinstellingen {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** Plaatst op het inhoudsnetwerk waarop uw advertentie kan verschijnen. Voer een geldige URL in, bijvoorbeeld www.example.com, example.com of www.example.com/shoes/kids. Als u meerdere tekenreeksen wilt opgeven, scheidt u deze met komma&#39;s of voert u ze op afzonderlijke regels in. De URL kan geen vraagteken bevatten (`?`). **Opmerking:** U kunt [websiteplaatsing uitsluiten](placement-negative-create.md) van de [!UICONTROL Placements] > [!UICONTROL Negatives] en in de instellingen van de advertentiegroep en de campagne.

**[!UICONTROL Status]:** De weergavestatus van de plaatsing: *Actief* (om biedingen mogelijk te maken; de standaardinstelling), *Gepauzeerd* (om biedingen uit te schakelen), of *Verwijderd* (om de plaatsing te schrappen; alleen bestaande stages).

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (Optioneel) De maximale kosten per klik (CPC) of kosten per duizend zichtbare indrukken (vCPM) voor de op plaatsing gebaseerde advertentie, afhankelijk van de strategie voor het indienen van een campagnebod. Deze waarde overschrijft het bod op advertentieniveau.

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
>* [Informatie over plaatsingen](placement-about.md)
>* [Negatieve plaatsingen maken](placement-negative-create.md)
>* [De status van stages en negatieve stages wijzigen](placement-status-edit.md)
