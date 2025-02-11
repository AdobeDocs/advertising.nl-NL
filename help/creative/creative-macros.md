---
title: Beschikbare macro's voor het bijhouden van URL's
description: Verwijs naar de macro's die u kunt toevoegen aan de URL's die URL's bijhouden op de bestemmingspagina en aan creatieve derde partijen.
feature: Creative Experiences, Creative Experiences
exl-id: d0cbbb21-467d-4ed1-bc6e-ded1b045b98b
source-git-commit: 926d2a0db933a19f5ebef056eca2089f2de6ca64
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Beschikbare macro&#39;s voor het bijhouden van URL&#39;s

*Gesloten bèta*

<!-- More feature metadata??? -->

U kunt elk van de volgende macro&#39;s opnemen in uw ontwerpen van derden, in URL&#39;s van derden voor uw ervaringen en in URL&#39;s van landingspagina&#39;s voor eigen gebruik.

Sommige beschikbare macro&#39;s, of de equivalente macro&#39;s, worden automatisch opgenomen in ervaringstags.

<!-- Later: 

| Macro | Description | Automatically in experience tags for Advertising DSP? | Automatically in experience tags for [!DNL Google Campaign Manager 360]? |
| --- | --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Tracks and reports the campaign ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ebuy!` |
| `${TM_SITE_ID_NUM}` | Tracks and reports the site ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%esid!` |
| `${TM_PLACEMENT_ID_NUM}` | Tracks and reports the placement ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%epid!` |
| `${TM_AD_ID_NUM}` | Tracks and reports the ad ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%eaid!` |
| `${TM_CREATIVE_ID_NUM}` | Tracks and reports the creative ID from the DSP | N/A | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ecid!` |
| `${TM_SESSION_ID}` | Tracks and reports the impression ID from the DSP. If a value isn't returned, Advertising Creative generates one. | Yes | &mdash; |
| `${TM_ACC_EXPERIENCE_ID}` | Tracks and reports the Advertising Creative experience ID | &mdash; | &mdash; |
| `${TM_ACC_CREATIVE_ID}` | Tracks and reports the Advertising Creative creative ID | &mdash; | &mdash; |
| `${TM_RANDOM}` | A random number between 1 and 1000000 | &mdash; | &mdash; |
| `${TM_TIMESTAMP}` | The Unix Timestamp (in seconds) | &mdash; | &mdash; |
| `${TM_CLICK_URL_URLENC}` | (For third-party ads from vendors who require URL encoding) The encoded click redirect URL, which enables ad servers to track and count ad clicks. When the ad is served and the user clicks on it, the macro is activated, and the click is recorded and counted for reporting purposes. | Yes | &mdash; |

-->

| Macro | Beschrijving | Automatisch tags beleven voor Advertising DSP? |
| --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Traceert en rapporteert de campagne-id van de DSP | Ja |
| `${TM_SITE_ID_NUM}` | Traceert en rapporteert de site-id van de DSP | Ja |
| `${TM_PLACEMENT_ID_NUM}` | Traceert en rapporteert de plaatsings-id van de DSP | Ja |
| `${TM_AD_ID_NUM}` | De advertentie-id bijhouden en rapporteren vanuit de DSP | Ja |
| `${TM_CREATIVE_ID_NUM}` | Hiermee wordt de creatieve id van de DSP bijgehouden en gerapporteerd | NVT |
| `${TM_SESSION_ID}` | Tracks and reports the picture ID from the DSP. Als er geen waarde wordt geretourneerd, genereert Advertising Creative een waarde. | Ja |
| `${TM_ACC_EXPERIENCE_ID}` | Traceert en rapporteert de ervaring-id van Advertising Creative | — |
| `${TM_ACC_CREATIVE_ID}` | Traceert en rapporteert de creatieve id van Advertising Creative | — |
| `${TM_RANDOM}` | Een willekeurig getal tussen 1 en 1000000 | — |
| `${TM_TIMESTAMP}` | De Unix-tijdstempel (in seconden) | — |
| `${TM_CLICK_URL_URLENC}` | (Voor advertenties van derden van leveranciers die URL-codering nodig hebben) Met de gecodeerde klik kunt u URL omleiden. Hierdoor kunnen servers van advertenties URL bijhouden en tellen en klikken. Wanneer de advertentie wordt aangeboden en de gebruiker erop klikt, wordt de macro geactiveerd, en de klik wordt geregistreerd en voor rapporteringsdoeleinden geteld. | Ja |

>[!MORELIKETHIS]
>
>* 
>* 
