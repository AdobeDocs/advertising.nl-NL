---
title: Instellingen voor Universal Video Add
description: Zie beschrijvingen van de beschikbare advertentie-instellingen voor universele videoadvertenties.
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# Instellingen voor Universal Video Add

>[!NOTE]
>
>Universele video-advertenties kunnen alleen worden gekoppeld aan universele video-opnamen.

## [!UICONTROL Insert Ad Tag]

*Nieuwe slechts advertenties*

**[!UICONTROL URL]:** De URL van de tag VAST.

**[!UICONTROL Title]:** Een titel voor het bestand, die in de weergave en rapporten van [!UICONTROL Ads] staat.

>[!TIP]
>
> Als u de geldigheid van een VAST-tag wilt controleren, plakt u deze in een browser en drukt u op **[!UICONTROL Enter]** . Als de tag geldig is, ziet u bovenaan een XML-bestand met `<VAST>` .

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (read-only) het advertentietype u creeert, dat aan het plaatsingstype beantwoordt waaraan de advertentie kan worden vastgemaakt.

**[!UICONTROL Ad Name]:** De advertentienaam. De titel van het element wordt standaard gebruikt, maar u kunt de naam wijzigen.

>[!TIP]
>
> Gebruik een naam die u gemakkelijk kunt vinden wanneer u de advertentie aan een plaatsing, in de [!UICONTROL Ads] mening, en in rapporten vastmaakt. Beschrijf bijvoorbeeld het eenheidstype en enkele belangrijke kenmerken (zoals Voorvertoning van vakantieproduct: 30 sec Universal Video&quot;).

**[!UICONTROL Show Controls]:** Where to include video controls for the add: *[!UICONTROL Under]* , *[!UICONTROL Over]*, *[!UICONTROL Bottom]* of *[!UICONTROL None]* (the default).

**[!UICONTROL Preserve Aspect Ratio]:** Of om de breedte en hoogteverhoudingen van de video (*[!UICONTROL Yes]*) te houden of de video uit te rekken om beschikbare ruimte te vullen (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Toevoegen met alleen VAST-tags; alleen-lezen) De VAST-tag van derden die u hebt ingevoerd als advertentiebron.

**[!UICONTROL Final VAST Tag]:** (Adds gebruikend VAST markeringen slechts; read-only) de derde VAST markering u als advertentiebron met de noodzakelijke [ gebruikte het volgen van Advertising DSP macro&#39;s ](/help/dsp/campaign-management/macros.md) inging, als toepasselijk.

**[!UICONTROL Wmode]:** De venstermodus: *[!UICONTROL window]* , *[!UICONTROL transparent]* of *[!UICONTROL opaque]* . Laat deze instelling leeg als deze niet van toepassing is.

**[!UICONTROL Video Format]:** De indeling van de advertentiespeler voor mogelijke inventarisatie: *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]* of *[!UICONTROL VAST]* . De weergavebaarheid wordt altijd gemeten voor [!UICONTROL VPAID] , maar [!UICONTROL VPAID & VAST] bevat een overzicht waarin de zichtbaarheid niet kan worden gemeten. Houd rekening met dit verschil als meetgegevens voor de weergavemogelijkheden belangrijk zijn voor uw campagne.

Gebruik [!UICONTROL VAST] , dat geen meetbaarheid toestaat, wanneer u zich richt op aangesloten tv of inventaris die uitsluitend VAST-indeling vereist (gewoonlijk van leveringsbronnen zoals Google Ad Manager, Appnexus, SpotX en Freewiel). Gebruik deze optie ook voor voorraad die eerder compatibel was met de standaardinstellingen voor Pre-roll (VAST) of Phone + Tablet Standard Pre-roll (VAST).

**[!UICONTROL Clock Number]**: (Wordt alleen gebruikt in het Verenigd Koninkrijk; alleen beschikbaar voor gebruikers met toestemming) Een unieke id die wordt gebruikt om ervoor te zorgen dat de juiste advertentie wordt uitgezonden. Laat deze instelling leeg als deze niet van toepassing is.

### [!UICONTROL Pixel]

Alle bestaande pixels voor het bijhouden van gebeurtenissen voor de plaatsing worden automatisch gekoppeld. U kunt bestaande pixels loskoppelen en nieuwe pixels maken wanneer dat nodig is, op basis van uw behoeften voor bijhouden voor de afzonderlijke advertentie. **Uiteinde:** om de derde volgende pixel voor veelvoudige advertenties in een plaatsing uit te geven meteen gebruikend de [!UICONTROL Ad Tools] mening, zie &quot;[ het Volgen Pixels van de Derde aan Ads in een Plaatsing ](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads) vastmaken.&quot;

De volgende instellingen zijn van toepassing op elke pixel die u maakt of bewerkt.

**[!UICONTROL Integration Event]:** De gebeurtenis die de pixel in brand zet. Gebruik voor dit advertentietype pixels die op *[!UICONTROL Impression]* of *[!UICONTROL Click-through]* worden geactiveerd.

**[!UICONTROL Pixel Type]:** Of de pixel een *[!UICONTROL IMG URL]* (1x1 pixelafbeeldingsbestand), *[!UICONTROL HTML]* of *[!UICONTROL JavaScript URL]* is.

**[!UICONTROL Pixel URL or Code]:** De URL van de pixelafbeelding, in de juiste indeling voor de opgegeven afbeelding [!UICONTROL Pixel Type] .

**[!UICONTROL Pixel Name]:** De pixelnaam. Gebruik een naam waarmee u de pixel gemakkelijk kunt herkennen.

**[!UICONTROL Pixel Provider]:** De pixelprovider: *[!UICONTROL None]* , *[!UICONTROL Comscore]* , *[!UICONTROL WhiteOps]* of *[!UICONTROL IAS]* .

>[!MORELIKETHIS]
>
>* [ Veelgestelde vragen over Universele Video ](/help/dsp/campaign-management/faq-universal-video.md)
>* [ Ongeveer Advertentiebeheer ](ad-about.md)
>* [ creeer Één enkele Advertentie ](ad-create.md)
>* [ maak een lijst van de Plaatsen verbonden aan een Advertentie ](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [ Advertentiespecificaties ](ad-specs.md)
>* [ Macro&#39;s van DSP ](/help/dsp/campaign-management/macros.md)
