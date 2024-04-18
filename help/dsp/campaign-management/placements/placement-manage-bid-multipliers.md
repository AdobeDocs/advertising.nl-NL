---
title: Bodmultiplicatoren voor plaatsen beheren
description: Meer informatie over het maken en bewerken van biedingsvermenigvuldigers voor opgegeven plaatsingsdoelen.
feature: DSP Placements
source-git-commit: 6994a15af080057889607c0e28dd519a1ddb28de
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 2%

---

# Bodmultiplicatoren voor plaatsen beheren

Met deze functie kun je de biedvermenigvuldigingsfactoren voor je bestaande plaatsingsdoelen wijzigen. Je kunt de biedvermenigvuldigingsfactoren voor één plaatsing tegelijk beheren.<!-- remove that line once we can edit multiple -->

Als u de geselecteerde doelen voor uw plaatsing wilt wijzigen, raadpleegt u &quot;[Een plaatsing bewerken](/help/dsp/campaign-management/placements/placement-edit.md).&quot;

<!-- 
## Manage the Bid Multipliers for a Single Placement
-->

1. Klik in het hoofdmenu op **[!UICONTROL Campaigns]**.

1. Klik op de naam van de campagne.

1. Klik in het submenu op **[!UICONTROL Placements]**.

1. Klik naast de plaatsingsnaam op  **[!UICONTROL ...]** > **[!UICONTROL Bid Multiplier]**.

1. Naar elke [doelspecifiek tabblad](#bid-multiplier-by-target) ([!UICONTROL Geo], [!UICONTROL Inventory], [!UICONTROL Sites], [!UICONTROL Audience], en [!UICONTROL Brand Safety]) en bewerkt u de bestaande waarden voor de plaatsingsdoelen. De meeste doelcategorieën maken een lijst van subcategorieën op de linkerzijde. Klik op een subcategorie om de biedvermenigvuldigingsfactoren voor die subcategorie te beheren, indien van toepassing.

   Standaard is de biedvermenigvuldiger voor een doel 1,00, wat betekent dat het bod niet voor dat doel is aangepast. Waarden kunnen variëren van 0,10 tot 10,00. Een biedwijziging van 0,5 verlaagt bijvoorbeeld een bod van USD 6 naar USD 3 (0,5 x 6). Met biedopties wordt het bod nooit hoger dan het maximumbod.

   Wanneer een veiling in aanmerking komt voor meerdere biedmodifiers, worden alle toepasselijke biedmodifiers vermenigvuldigd.

   U kunt een berichtvermenigvuldiger (met andere waarden dan 1,00) instellen voor een [beperkt aantal streefcijfers](#bid-multiplier-limits-by-target).

1. Klik rechtsboven op **[!UICONTROL Save]**.

## Doeltypen die in aanmerking komen voor biedvermenigvuldigingsfactoren {#bid-multiplier-by-target}

U kunt biedingsbepalingen alleen configureren voor opgenomen doelen, niet voor uitgesloten doelen.

* **Geo-doelen**: geografie (landen, staten en steden), postcodes en DMA&#39;s

* **Voorraaddoelstellingen**: bronnen en feeds voor openbare inventarisatie en [!UICONTROL On Demand] voorraad

* **Sitedoelen:** doelsites/apps, sitecategorieën

* **Doelstellingen voor het publiek:** segmenten, onderdelen en onderwerpen

* **ads.txt-doelen:** (Als u de optie Advertentie.txt uitschakelt), worden alleen advertenties.txt-verkopers, rechtstreekse verkopers en verkopers van advertenties.txt plus sites zonder advertenties.txt.

## Maximum aantal biedvermenigvuldigers per doeltype {#bid-multiplier-limits-by-target}

U kunt biedvermenigvuldigingsfactoren (met andere waarden dan 1,00) instellen voor een beperkt aantal doelen. U kunt bijvoorbeeld biedvermenigvuldigingsfactoren instellen voor maximaal twintig landdoelen. Het maximumaantal doelen voor elk doeltype dat biedvermenigvuldigingsfactoren kan hebben, wordt hieronder vermeld.

| Categorie | Parameter | Maximum aantal |
| -------- | --------- | ----- |
| Geo | Land | 20 |
| Geo | Staat | 100 |
| Geo | Plaats | 100 |
| Geo | Metro | 100 |
| Geo | Postcodes | 100 |
| Inventaris | Bronnen | 100 |
| Inventaris | Feeds | 100 |
| Sites | Categorie Site | 100 |
| Sites | Sites/apps | 100 |
| Publiek | Segmenten | 500 |
| Publiek | Onderwerpen | 100 |
| Merkveiligheid | Ads.txt | NVT |

>[!MORELIKETHIS]
>
>* [Info over Plaatsingsbeheer](placement-about.md)
>* [Een plaatsing bewerken](placement-edit.md)
>* [Het Wijzigingslogboek voor een plaatsing weergeven](placement-change-log.md)
>* [Plaatsingsinstellingen](placement-settings.md)
