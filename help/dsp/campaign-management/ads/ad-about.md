---
title: Over Advertentiebeheer in DSP
description: Meer informatie over advertentiebeheer.
feature: DSP Ads
exl-id: 41dbe28e-a476-4601-a3d8-a9111eae3f6b
source-git-commit: 9073400eb26957c63378bee90929009fcc82f78f
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 0%

---

# Over Advertentiebeheer in DSP

<!-- add "The Ads View (Dashboard?)" section -->

DSP ondersteunt ad-leveranties via tags van derden voor advertenties (zoals Google, Flash Talk of Sizmek) voor verschillende advertentietypen en de directe asset-upload voor eigen advertenties. U kunt tags van derden afzonderlijk of bulksgewijs uploaden. Bulkuploads gebruiken de pagina&#39;s van de partnermarkering of een bulkmarkeringsmalplaatje.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Wanneer uw advertenties zijn ingesteld, koppelt u elke advertentie aan een plaatsing, die de doelparameters bevat (zoals geo, publiek, apparaat en voorraadgerichtheid) die bepalen hoe uw campagne werkt. U kunt één advertentie aan een of meerdere plaatsen vastmaken.

## Beschikbare advertentietypen {#ad-types}

Alle volgende advertentietypen zijn beschikbaar in DSP. Voor volledige specificaties voor elk advertentietype raadpleegt u de [Advertentiespecificaties](ad-specs.md).

* **Audiolagen (alleen van derden)**: Audioadvertenties kunnen worden afgespeeld tussen inhoud op digitale uitgeversites en kunnen zelfstandig worden uitgevoerd als audiobestanden of samen met bijbehorende banners. Audio kan het best worden gebruikt om merkbekendheid te geven en om onderweg publiek te maken. Tot de belangrijkste prestatie-indicatoren voor audio behoren [!UICONTROL Completion Rate] en [!UICONTROL Cost per Completion].

* **Advertenties weergeven (alleen derden)**: Weergaveadvertenties zijn geanimeerde of statische afbeeldingen die in webbrowsers of in apps worden weergegeven. Als u op de advertentie-eenheid klikt, gaat de gebruiker naar een site of microsite met merknaam. De vertoning wordt best gebruikt om efficiënte CPMs te drijven, berichtvereniging te verhogen, extra merk of productaanraakpunten toe te voegen, en gebruikers te drijven onderaan de aanschaftrechter. Tot de belangrijkste prestatie-indicatoren voor weergave behoren: [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions], en [!UICONTROL Cost per Conversion]. DSP ondersteunt een groot aantal verschillende advertentiegrootten.

* **Mobiele advertenties (alleen van derden)**: Mobiele advertenties kunnen de indeling VAST, MRAID (pre-roll video) of standaard display hebben. Mobiele voorrolvideo kan automatisch worden afgespeeld of met een klik worden afgespeeld en kan het beste worden gebruikt om gebruikers op verschillende schermen te bereiken. Mobiel standaardbeeldscherm is een statisch beeld dat wordt weergegeven in mobiele webbrowsers of in apps en is het meest geschikt voor het aanvullen van digitale videoaankopen, het koppelen van schijfberichten en het toevoegen van extra branding of productaanraakpunten. Mobiele advertenties kunnen ook functioneren als overnames op volledig scherm of als mobiele interstitiële apparaten. Dit zijn zeer geavanceerde mobiele advertenties die het beste kunnen worden gebruikt om het bewustzijn van het merk voor mobiele doelgroepen en stationsomzettingen te ontwikkelen.

* **Eigen weergaveadvertenties (alleen eerste partij)**: Native advertenties worden ondersteund in de standaardweergave-indeling. Native advertenties bevatten een kop en/of titel, beschrijving, logo en afbeelding. De advertentie-elementen worden gecombineerd en gerenderd zodat deze overeenkomen met de paginastijl van de uitgever, zodat de advertentie samenvloeit met de organische inhoud van de uitgever en een hogere betrokkenheid mogelijk maakt. Native wordt het beste gebruikt voor merkbekendheid en voor het aansturen van de kijkcijfers en de betrokkenheid bij viewervriendelijke advertenties. Belangrijke prestatie-indicatoren zijn [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions], en [!UICONTROL Cost Per Conversion].

* **Pre-roll Ads (alleen van derden)**: Pre-roll advertenties (VAST en VPAID) worden getoond vóór premiumvideo-inhoud en bieden een indrukwekkende viewerervaring. Video vóór de rol kan interactief zijn, rijke media eigenschappen, en omvat bekledingen, rollovers, en vraag-aan-actie bevatten. De belangrijkste prestatie-indicatoren voor pre-roll videoadvertenties omvatten [!UICONTROL Video Completion Rate] en [!UICONTROL Viewability Rate].

* **Aangesloten tv-advertenties (alleen van derden)**: Aangesloten tv-advertenties worden weergegeven voor en tijdens hoogwaardige tv-video-inhoud. Alle aangesloten tv-inventarisaties worden uitgevoerd op tv-apparaten. Dit betekent dat video automatisch wordt afgespeeld in een teruggekoppelde, schermvullende omgeving die de kijkers niet kunnen overslaan. Connected TV is de meest verwante digitale video-indeling voor tv-reclames. Belangrijke prestatie-indicatoren voor Connected TV zijn onder andere [!UICONTROL Completion Rate].

* **Universal Video Ads (alleen van derden)**: Met Universal Video ads kunt u de videovoorraad richten op desktopcomputers, mobiele apparaten en aangesloten tv-omgevingen voor VPAID- en VAST-inventarisatie met behulp van één videoplaatsing. Ze combineren alle mogelijkheden van aangesloten tv-advertenties, pre-roll-advertenties en mobiele pre-roll-advertenties en worden voor en tijdens video-inhoud weergegeven. Tot de belangrijkste prestatie-indicatoren voor universele video behoren: [!UICONTROL Completion Rate] en [!UICONTROL Viewability Rate].

   Universele video-advertenties kunnen alleen worden gekoppeld aan universele video-opnamen.

   Zie &quot;[Veelgestelde vragen over Universal Video](/help/dsp/campaign-management/faq-universal-video.md)&quot; voor meer informatie over universele videobaden .

## Goedkeuringen DSP

Wanneer u een advertentie maakt, controleert DSP deze voor gevoelige categorieën, klikt u op URL-functionaliteit en geeft u een voorvertoning van de rendering weer.

In eerste instantie ziet u een rode stip in het dialoogvenster [!UICONTROL Status] kolom. Het herzieningsproces duurt gewoonlijk 24 tot 48 uur. Een verbroken advertentie kan echter langer dan 48 uur in behandeling zijn, dus u hebt tijd om fouten op te lossen voordat de advertentie wordt afgewezen. Geweigerde advertenties bevatten een reden voor de afwijzing.

Wanneer DSP een advertentie goedkeurt, ziet u een groene stip in de kolom Status.

![goedkeuringsindicator in [!UICONTROL Status] kolom](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Uw advertentie zal slechts worden gediend als zowel DSP als het SSP creatief hebben goedgekeurd. Elk SSP heeft zijn eigen goedkeuringsvereisten en proces.

>[!MORELIKETHIS]
>
>* [Eén advertentie maken](ad-create.md)
>* [Meerdere externe advertenties maken](ad-create-multiple.md)
>* [Advertentiespecificaties](ad-specs.md)

