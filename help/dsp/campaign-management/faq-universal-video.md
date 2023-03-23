---
title: Veelgestelde vragen over Universal Video
description: Meer weten over universele videobanden?
feature: DSP Placements, DSP Ads
source-git-commit: 17a47e9d7ddb18b36da998d289f949e540beded8
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Veelgestelde vragen over Universal Video

[Universele video-advertenties](/help/dsp/campaign-management/ads/ad-about.md) kunt u de videovoorraad van desktop-, mobiel- en aangesloten tv-omgevingen richten op VPAID- en VAST-inventarisatie met behulp van één videoplaatsing.

## Hoe kunt u universele videoplaatsen en advertenties maken?

Universal video placements can contain only Universal video ads, and Universal video ads can be attached only to Universal video placements.

Maak universele videoplaatsingen en advertenties die vergelijkbaar zijn met de manier waarop u andere typen plaatsingen en video&#39;s maakt:

1. In de gewenste campagne [universele videoplaatsing maken](/help/dsp/campaign-management/placements/placement-create.md), selecteert u de [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   U moet ten minste één omgeving (Desktop, Mobiel, Verbonden tv) opgeven om als doel in te stellen.

1. In dezelfde campagne als de universele videoplaatsing, [één universele video-advertentie maken](/help/dsp/campaign-management/ads/ad-create.md) of [meerdere universele videobanden maken](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   Als u meerdere advertenties maakt, moet u &quot;[!UICONTROL Universal Video]&quot; als de [!UICONTROL Ad Type]:

   * Voor [!DNL Google] of [!DNL Flashtalking] advertenties: In het veld &quot;[!UICONTROL Review ad types]&quot; nadat u het bestand hebt geüpload, klikt u op de knop **[!UICONTROL Ad Type]** veld en selecteer **[!UICONTROL Universal Video]**.

   * Voor andere typen advertentietags: Geef in het werkbladbestand dat u uploadt het veld Advertentietype voor elke advertentie op als **[!UICONTROL Universal Video]**.

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

* De plaatsingsdoelstellingen verbonden TV-inventaris.
* De plaatsing is gericht op videoinventarisatie van Google Ad Manager, Appnexus, SpotX of Freeschijf. Deze SSPs steunt niet VPAID &amp; VAST videoformaat.

## Is het mogelijk om veelvoudige universele videoadvertenties aan de zelfde universele videoplaatsing vast te maken?

Ja.
