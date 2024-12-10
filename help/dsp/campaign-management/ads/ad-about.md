---
title: Over Advertentiebeheer in Advertising DSP
description: Meer informatie over advertentiebeheer.
feature: DSP Ads
exl-id: 41dbe28e-a476-4601-a3d8-a9111eae3f6b
source-git-commit: e9ce180e302f619c85a3d6db813c83903e437d04
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# Over Advertentiebeheer in Advertising DSP

<!-- add "The Ads View (Dashboard?)" section -->

DSP ondersteunt ad-leveranties via tags van derden voor advertenties (zoals Google, Flash Talk of Sizmek) voor verschillende advertentietypen en de directe asset-upload voor native weergaveadvertenties. U kunt tags van derden afzonderlijk of in bulk uploaden. Bulkuploads gebruiken de pagina&#39;s van de partnermarkering of een bulkmarkeringsmalplaatje.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Wanneer uw advertenties zijn ingesteld, koppelt u elke advertentie aan een of meer plaatsingen, die de doelparameters (zoals geo, publiek, apparaat en inventarisgericht) bevatten die bepalen hoe uw campagne werkt. Als u de advertentie wilt uitvoeren, moet u een advertentie aan een plaatsing koppelen.

## Beschikbare advertentietypen {#ad-types}

Alle volgende advertentietypen zijn beschikbaar in DSP. Voor volledige specificaties voor elk advertentietype, zie de [ Specificaties van de Advertentie ](ad-specs.md).

* **AudioAdds (derde slechts)**: De audio advertenties spelen tussen inhoud op digitale uitgeversplaatsen en kunnen standalone als audiodossiers of samen met metgezelbanners worden in werking gesteld. Audio kan het best worden gebruikt om merkbekendheid te geven en om onderweg publiek te maken. Tot de belangrijkste prestatie-indicatoren voor audio behoren [!UICONTROL Completion Rate] en [!UICONTROL Cost per Completion] .

* **Advertenties van de Vertoning (derde slechts)**: De advertenties van de vertoning zijn geanimeerde of statische beelden die in Webbrowsers of in apps worden getoond. Als u op de advertentie-eenheid klikt, gaat de gebruiker naar een site of microsite met merknaam. De vertoning wordt best gebruikt om efficiënte CPMs te drijven, berichtvereniging te verhogen, extra merk of productaanraakpunten toe te voegen, en gebruikers te drijven onderaan de aanschaftrechter. Tot de belangrijkste prestatie-indicatoren voor de weergave behoren [!UICONTROL Clicks] , [!UICONTROL Cost per Click] , [!UICONTROL Conversions] en [!UICONTROL Cost per Conversion] . DSP ondersteunt een groot aantal verschillende advertentiegrootten.

* **Mobiele Advertenties (derde slechts)**: De mobiele advertenties kunnen in pre-rolvideo (VAST, MRAID) of standaardvertoningsformaat zijn. Mobiele voorrolvideo kan automatisch worden afgespeeld of met een klik worden afgespeeld en kan het beste worden gebruikt om gebruikers op verschillende schermen te bereiken. Mobiel standaardbeeldscherm is een statisch beeld dat wordt weergegeven in mobiele webbrowsers of in apps en is het meest geschikt voor het aanvullen van digitale videoaankopen, het koppelen van schijfberichten en het toevoegen van extra branding of productaanraakpunten. Mobiele advertenties kunnen ook functioneren als overnames op volledig scherm of als mobiele interstitiële apparaten. Dit zijn zeer geavanceerde mobiele advertenties die het beste kunnen worden gebruikt om het bewustzijn van het merk voor mobiele doelgroepen en stationsomzettingen te ontwikkelen.

* **Inheemse Advertenties van de Vertoning (eerste partij slechts)**: De inheemse advertenties worden gesteund in standaardvertoningsformaat. Native advertenties bevatten een kop en/of titel, beschrijving, logo en afbeelding. De advertentie-elementen worden gecombineerd en gerenderd zodat deze overeenkomen met de paginastijl van de uitgever, zodat de advertentie samenvloeit met de organische inhoud van de uitgever en een hogere betrokkenheid mogelijk maakt. Native wordt het beste gebruikt voor merkbekendheid en voor het aansturen van de kijkcijfers en de betrokkenheid bij viewervriendelijke reclame. Voorbeelden van belangrijke prestatie-indicatoren zijn [!UICONTROL Clicks] , [!UICONTROL Cost Per Click] , [!UICONTROL Conversions] en [!UICONTROL Cost Per Conversion] .

* **pre-rol Advertenties (derde slechts)**: De pre-rol advertenties (VAST en VPAID) worden getoond vóór premievideo inhoud en verstrekken een indrukwekkende, boeiende kijkervaring. Video vóór de rol kan interactief zijn, rijke media eigenschappen, en omvat bekledingen, rollovers, en vraag-aan-actie bevatten. Voornaamste prestatie-indicatoren voor preroll-videobaden zijn [!UICONTROL Video Completion Rate] en [!UICONTROL Viewability Rate] .

* **Verbonden TV Adds (derde slechts)**: De aangesloten advertenties van TV worden getoond vóór en tijdens PremiumTV videoinhoud. Alle aangesloten tv-inventarisaties worden uitgevoerd op tv-apparaten. Dit betekent dat video automatisch wordt afgespeeld in een teruggekoppelde, schermvullende omgeving die de kijkers niet kunnen overslaan. Connected TV is de meest verwante digitale video-indeling voor tv-reclames. Tot de belangrijkste prestatie-indicatoren voor Connected TV behoren onder andere [!UICONTROL Completion Rate] .

* **Universele VideoAdds (derde slechts)**: De universele videoadvertenties staan u toe om videoinventaris van Desktop, mobiele, en aangesloten milieu&#39;s van TV voor VPAID en VAST inventaris te richten gebruikend één enkele videoplaatsing. Ze combineren alle mogelijkheden van aangesloten tv-advertenties, pre-roll-advertenties en mobiele pre-roll-advertenties en worden voor en tijdens video-inhoud weergegeven. Tot de belangrijkste prestatie-indicatoren voor universele video behoren [!UICONTROL Completion Rate] en [!UICONTROL Viewability Rate] .

  Universele video-advertenties kunnen alleen worden gekoppeld aan universele video-opnamen.

  Zie &quot;[ Veelgestelde vragen over Universele Video ](/help/dsp/campaign-management/faq-universal-video.md)&quot;voor meer informatie over universele videoadvertenties.

## Goedkeuringen DSP

Wanneer u een advertentie maakt, controleert DSP deze voor gevoelige categorieën, klikt u op URL-functionaliteit en geeft u een voorvertoning van de rendering weer.

In eerste instantie wordt in de kolom [!UICONTROL Status] van de advertentie een rode stip weergegeven. Het herzieningsproces duurt gewoonlijk 24 tot 48 uur. Een verbroken advertentie kan echter langer dan 48 uur in behandeling zijn, dus u hebt tijd om fouten op te lossen voordat de advertentie wordt afgewezen. Geweigerde advertenties bevatten een reden voor de afwijzing.

Als DSP een advertentie goedkeurt, wordt in de kolom Status van de advertentie een groene stip weergegeven.

![ goedkeuringsindicator in [!UICONTROL Status] kolom ](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Uw advertentie kan alleen worden aangeboden als zowel DSP als het SSP de creatieve advertentie hebben goedgekeurd. Elk SSP heeft zijn eigen goedkeuringsvereisten en proces.

>[!MORELIKETHIS]
>
>* [ creeer Één enkele Advertentie ](ad-create.md)
>* [ creeer Veelvoudige Derde Advertenties ](ad-create-multiple.md)
>* [ Advertentiespecificaties ](ad-specs.md)
