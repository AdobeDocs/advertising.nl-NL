---
title: Veelgestelde vragen over Universal Video
description: Meer weten over universele videobanden?
feature: DSP Placements, DSP Ads
source-git-commit: 8e0237355e834f4ae2b9ef1ed211e047b41cafe7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# # Veelgestelde vragen over universele video

## Hoe kunt u universele videoplaatsen en advertenties maken?

Universal video placements can contain only Universal video ads, and Universal video ads can be attached only to Universal video placements.

Maak ze op dezelfde manier als andere typen plaatsingen en video&#39;s:

1. In de gewenste campagne [universele videoplaatsing maken](/help/dsp/campaign-management/placements/placement-create.md), selecteert u de [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   U moet ten minste één omgeving opgeven (Desktop, Mobiel, Verbonden tv) als doel.

1. In dezelfde campagne als de universele videoplaatsing, [één universele video-advertentie maken](/help/dsp/campaign-management/ads/ad-create.md) of [meerdere universele videobanden maken](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Als u meerdere advertenties maakt, moet u &quot;[!UICONTROL Universal Video]&quot; als de [!UICONTROL Ad Type]. Voor [!DNL Google] of [!DNL Flashtalking] adverteert, nadat u het bestand hebt geüpload, klikt u op het veld Advertentietype in het dialoogvenster &quot;[!UICONTROL Review ad types]&quot; stap en bewerk deze. Voor andere typen advertentietags geeft u het advertentietype op in het spreadsheetbestand dat u uploadt.

1. [De advertentie-instellingen openen](/help/dsp/campaign-management/ads/ad-edit.md) voor elke nieuwe advertentie en selecteer het toepasselijke videoformaat:

   * **[!UICONTROL VPAID]:** Zichtbaarheid wordt altijd gemeten.
   * **[!UICONTROL VPAID & VAST (Default)]:** Omvat voorraad die geen viewability meting toestaat.
   * **[!UICONTROL VAST]** - Geschikt voor online tv-inventarisatie.

   Zie &quot;[Instellingen voor Universal Video Add](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)&quot; voor meer informatie .

1. [De nieuwe Universal Video Adads bijvoegen](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) naar de universele plaatsing van video.

## Waarom zijn sommige optimalisatiedoelstellingen en pakketten niet beschikbaar wanneer de Connected TV-omgeving is geselecteerd voor een universele plaatsing van video?

Doelstellingen die niet compatibel zijn met standaard aangesloten tv-plaatsingen, zoals de laagste kosten per klik, worden niet ondersteund voor de aangesloten tv-omgeving in universele videoplaatsingen. Pakketten met niet-compatibele optimalisatiedoelen kunnen ook niet worden geselecteerd.

## Wanneer moet de **[!UICONTROL VAST]** video-indeling wordt gebruikt voor universele videoadvertenties?

Gebruiken **[!UICONTROL VAST]** in een van de volgende scenario&#39;s:

* De plaatsing is gericht op de inventarisatie van aangesloten tv.
* De plaatsing richt videoinventaris van Google Ad Manager, Appnexus, SpotX, of Freeschijf. Deze SSPs steunt niet VPAID &amp; VAST videoformaat.

## Is het mogelijk om veelvoudige universele videoadvertenties aan de zelfde universele videoplaatsing vast te maken?

Ja.
