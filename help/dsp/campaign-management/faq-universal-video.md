---
title: Veelgestelde vragen over universele video
description: Meer weten over universele videobanden?
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
source-git-commit: 1e307a95d597f20c97683ee20c0a3b99f662f7fd
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Veelgestelde vragen over universele video

[&#x200B; Universele videoadvertenties &#x200B;](/help/dsp/campaign-management/ads/ad-about.md#ad-types) staan u toe om videoinventaris van Desktop, mobiele, en aangesloten milieu&#39;s van TV voor VPAID en VAST inventaris te richten gebruikend één enkele videoplaatsing.

## Hoe kunt u universele videoplaatsen en advertenties maken?

Universal video placements can contain only Universal video ads, and Universal video ads can be attached only to Universal video placements.

Maak universele videoplaatsingen en advertenties die vergelijkbaar zijn met de manier waarop u andere typen plaatsingen en video&#39;s maakt:

1. Binnen de gewenste campagne, [&#x200B; creeer een universele videoplaatsing &#x200B;](/help/dsp/campaign-management/placements/placement-create.md), die [!UICONTROL Placement Type] **[!UICONTROL Universal Video]** selecteert.

   U moet ten minste één omgeving (Desktop, Mobiel, Verbonden tv) opgeven als doel.

1. In de zelfde campagne zoals de universele videoplaatsing, [&#x200B; creeer één enkele universele video en &#x200B;](/help/dsp/campaign-management/ads/ad-create.md) of [&#x200B; creeer veelvoudige universele videoadvertenties &#x200B;](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Als u meerdere advertenties maakt, moet u &quot;[!UICONTROL Universal Video]&quot; opgeven als de [!UICONTROL Ad Type] :

   * Voor [!DNL Google] - of [!DNL Flashtalking] -advertenties: klik in de stap &quot;[!UICONTROL Review ad types]&quot; nadat u het bestand hebt geüpload op het veld **[!UICONTROL Ad Type]** en selecteer **[!UICONTROL Universal Video]** .

   * Voor andere typen advertentietags: binnen het spreadsheetbestand dat u uploadt, geeft u het veld Advertentietype voor elke advertentie op als **[!UICONTROL Universal Video]** .

1. [&#x200B; open de advertentiemontages &#x200B;](/help/dsp/campaign-management/ads/ad-edit.md) voor elke nieuwe advertentie en selecteer het toepasselijke videoformaat:

   * **[!UICONTROL VPAID]:** De weergavabiliteit wordt altijd gemeten.
   * **[!UICONTROL VPAID & VAST (Default)]:** omvat inventaris die viewability meting niet toestaat.
   * **[!UICONTROL VAST]** - Geschikt voor online tv-inventarisatie.

   Zie &quot;[&#x200B; Universele video en montages &#x200B;](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)&quot;voor meer informatie.

1. [&#x200B; maak de nieuwe universele videoadvertenties &#x200B;](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) aan de universele videoplaatsing vast.

## Waarom zijn sommige optimalisatiedoelstellingen en pakketten niet beschikbaar wanneer de aangesloten TV-omgeving wordt geselecteerd voor een universele videoplaatsing?

Doelstellingen die niet compatibel zijn met standaard aangesloten tv-plaatsingen, zoals de laagste kosten per klik, worden niet ondersteund voor de aangesloten tv-omgeving in universele videoplaatsingen. Pakketten met niet-compatibele optimalisatiedoelen kunnen ook niet worden geselecteerd.

## Wanneer moet de video-indeling **[!UICONTROL VAST]** worden gebruikt voor universele videoadvertenties?

Gebruik **[!UICONTROL VAST]** in een van de volgende scenario&#39;s:

* De plaatsingsdoelstellingen verbonden TV-inventaris.
* De plaatsing richt videoinventaris van Google Ad Manager, Appnexus, SpotX, of FreeWheel. Deze SSPs steunt niet VPAID &amp; VAST videoformaat.

## Is het mogelijk om veelvoudige universele videoadvertenties aan de zelfde universele videoplaatsing vast te maken?

Ja.
