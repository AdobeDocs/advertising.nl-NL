---
title: Beschikbare velden voor dynamische en feed-bestanden
description: Leer meer over de velden die u kunt opnemen in de feed-bestanden die u gebruikt om dynamische advertenties te maken.
feature: Creative Dynamic Ads
source-git-commit: 0d7a7ab23173a061961c4b5c66ace5b69a746e86
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Bijlage: Beschikbare velden voor dynamische en feed-bestanden

De volgende feed-velden zijn beschikbaar op de Advertising Creative-achtergrond. U kunt a [&#x200B; voederdossier &#x200B;](/help/creative/feeds/asset-manage.md) uploaden dat uw organisatie-specifieke gebiedsnamen gebruikt. Nochtans, alvorens u a [&#x200B; catalogus &#x200B;](/help/creative/feeds/catalog-manage.md) van uw voederdossier kunt tot stand brengen, moet u elk gebied in het voederdossier aan één van de volgende gebieden in het [&#x200B; voedermalplaatje &#x200B;](/help/creative/feeds/feed-template-manage.md) in kaart brengen dat u zult gebruiken om de catalogus tot stand te brengen.

Het enige veld dat een equivalent moet hebben in het feed-bestand is `PART_NUM` .

<!-- Questions:

What are these?
Rank
PROFILE_FILTER fields



Do geo fields need be populated as follows:
Country: 2 Letter country code (example: US)
State: state code_2 letter country code (example: CA_US)
City: City name_State code_2 letter country code (example: San Jose_CA_US)
DMA: DMA _2 letter country code (example: 201_US)
Zipcode: Zip code_2 letter country code (example: 94086_US)


TRUE?   GEO fields(Country/State/City/DMA/Zip), UT fields (UT1/UT2/UT3/UT4/UT5) [do we have an equivalent now?], Filtering fields(F1/F2/F3/F4/F5) can have comma separated values. We can have upto 2K characters.

TRUE FOR CSV AND TSV? character encoding on text format files should be UTF-8 -- If yes, then add that with feed file requirements.

-->

| Veldnaam | Gegevenstype | Vereist? |
|------------|-----------|-----------|
| PART_NUM | varchar(64) | JA |
| PRODUCT_NAME | text | NEE |
| PRODUCT_URL | text | NEE |
| PRIJS | decimaal (10,2) | NEE |
| DISCOUNT_PRICE | decimaal (10,2) | NEE |
| AFBEELDING | varchar(1024) | NEE |
| IMAGE_HEIGHT | int | NEE |
| IMAGE_WIDTH | int | NEE |
| IMAGE_1 | varchar(1024) | NEE |
| IMAGE_2 | varchar(1024) | NEE |
| IMAGE_3 | varchar(1024) | NEE |
| IMAGE_4 | varchar(1024) | NEE |
| IMAGE_5 | varchar(1024) | NEE |
| IMAGE_6 | varchar(1024) | NEE |
| IMAGE_7 | varchar(1024) | NEE |
| IMAGE_8 | varchar(1024) | NEE |
| IMAGE_9 | varchar(1024) | NEE |
| IMAGE_10 | varchar(1024) | NEE |
| TEXT_1 | text | NEE |
| TEXT_2 | text | NEE |
| TEXT_3 | text | NEE |
| TEXT_4 | text | NEE |
| TEXT_5 | text | NEE |
| TEXT_6 | text | NEE |
| TEXT_7 | text | NEE |
| TEXT_8 | text | NEE |
| TEXT_9 | text | NEE |
| TEXT_10 | text | NEE |
| TEXT_11 | text | NEE |
| TEXT_12 | text | NEE |
| TEXT_13 | text | NEE |
| TEXT_14 | text | NEE |
| TEXT_15 | text | NEE |
| ADDITIONAL_PRICE_1 | decimaal (10,2) | NEE |
| ADDITIONAL_PRICE_2 | decimaal (10,2) | NEE |
| ADDITIONAL_PRICE_3 | decimaal (10,2) | NEE |
| AD_SIZE | varchar(32) | NEE |
| RANK | int | NEE |
| LAND | text | NEE |
| STAAT | text | NEE |
| STAD | text | NEE |
| ZIP | text | NEE |
| DMA | text | NEE |
| PROFILE_FILTER_1 | text | NEE |
| PROFILE_FILTER_2 | text | NEE |
| PROFILE_FILTER_3 | text | NEE |
| PROFILE_FILTER_4 | text | NEE |
| PROFILE_FILTER_5 | text | NEE |
| DATAPASS_FILTER_1 | text | NEE |
| DATAPASS_FILTER_2 | text | NEE |
| DATAPASS_FILTER_3 | text | NEE |
| DATAPASS_FILTER_4 | text | NEE |
| DATAPASS_FILTER_5 | text | NEE |
| AUDIENCE_SEGMENT | text | NEE |
| TAAL | text | NEE |
| CREATIVE_ATTRIBUTE_1 | varchar(256) | NEE |
| CREATIVE_ATTRIBUTE_2 | varchar(256) | NEE |
| CREATIVE_ATTRIBUTE_3 | varchar(256) | NEE |
| CREATIVE_ATTRIBUTE_4 | varchar(256) | NEE |
| CREATIVE_ATTRIBUTE_5 | varchar(256) | NEE |
| CREATIVE_ATTRIBUTE_6 | varchar(256) | NEE |
| CREATIVE_ATTRIBUTE_7 | varchar(256) | NEE |
| CREATIVE_ATTRIBUTE_8 | varchar(256) | NEE |
| CREATIVE_ATTRIBUTE_9 | varchar(256) | NEE |
| CREATIVE_ATTRIBUTE_10 | varchar(256) | NEE |
| IS_DEFAULT | enum | NEE |

>[!MORELIKETHIS]
>
>* [&#x200B; Werkstromen voor dynamische advertenties &#x200B;](/help/creative/introduction/workflow-dynamic-ads.md)
>* [&#x200B; beheert activa dossiers &#x200B;](/help/creative/feeds/asset-manage.md)
>* [&#x200B; beheer voedermalplaatjes &#x200B;](/help/creative/feeds/feed-template-manage.md)
>* [&#x200B; beheert catalogi &#x200B;](/help/creative/feeds/catalog-manage.md)
