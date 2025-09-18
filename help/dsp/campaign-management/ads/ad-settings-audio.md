---
title: Instellingen voor audio toevoegen
description: Zie beschrijvingen van de beschikbare advertentie-instellingen voor audioadvertenties.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 0%

---

# Instellingen voor audio toevoegen

## [!UICONTROL Insert Ad Tag]

*Nieuwe slechts advertenties*

**[!UICONTROL URL]**: De URL van de VAST-tag.

**[!UICONTROL Title]**: Een naam voor het bestand, die wordt gebruikt in de weergave en rapporten van [!UICONTROL Ads] .

>[!TIP]
>
> Als u de geldigheid van een VAST-tag wilt controleren, plakt u deze in een browser en drukt u op **[!UICONTROL Enter]** . Als de tag geldig is, ziet u bovenaan een XML-bestand met `<VAST>` .

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (read-only) het advertentietype u creeert, dat aan het plaatsingstype beantwoordt waaraan de advertentie kan worden vastgemaakt. De standaardwaarde is *[!UICONTROL Audio]* .

**[!UICONTROL Ad Name]:** De advertentienaam. De titel van het element wordt standaard gebruikt, maar u kunt de naam wijzigen.

>[!TIP]
>
> Gebruik een naam die u gemakkelijk kunt vinden wanneer u de advertentie aan een plaatsing, in de [!UICONTROL Ads] mening, en in rapporten vastmaakt. Beschrijf bijvoorbeeld het eenheidstype en enkele belangrijke kenmerken (zoals Voorvertoning van vakantieproduct: 30 sec audio&quot;).

**[!UICONTROL Ad Duration]:** De lengte van het audiodossier. Deze wordt automatisch ingesteld als [!UICONTROL 15] of [!UICONTROL 30] , afhankelijk van de geselecteerde advertentie-eenheid.

Dit veld kan al dan niet worden weergegeven, afhankelijk van de accountmachtigingen.

**[!UICONTROL VAST Tag]:** (Toevoegen met alleen VAST-tags) Een URL voor een advertentiebron van derden. Zorg ervoor dat de VAST-tag alleen audiomediabestanden bevat.

**[!UICONTROL Final VAST Tag]:** (Adds die VAST markeringen gebruiken slechts) URL voor de derde en bron met de noodzakelijke [ het volgen van Advertising DSP macro&#39;s ](/help/dsp/campaign-management/macros.md) opgenomen, als toepasselijk.

**[!UICONTROL Select Rate]:** (Gebruikers met slechts toestemming) een vooraf onderhandelde tarief dat door Adobe in rekening wordt gebracht, of één van de tarieven die u hebt onderhandeld en door de verkoper in rekening wordt gebracht. Neem contact op met uw Adobe-accountteam als u een tarief wilt toevoegen.

### [!UICONTROL Pixel]

Alle bestaande pixels voor het bijhouden van gebeurtenissen voor de plaatsing worden automatisch gekoppeld. U kunt bestaande pixels loskoppelen en nieuwe pixels maken wanneer dat nodig is, op basis van uw behoeften voor bijhouden voor de afzonderlijke advertentie. **Uiteinde:** om de derde volgende pixel voor veelvoudige advertenties in een plaatsing uit te geven meteen gebruikend de [!UICONTROL Ad Tools] mening, zie &quot;[ het Volgen Pixels van de Derde aan Ads in een Plaatsing ](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads) vastmaken.&quot;

De volgende instellingen zijn van toepassing op elke pixel die u maakt of bewerkt.

**[!UICONTROL Integration Event]:** De gebeurtenis die de pixel in brand zet. Gebruik voor dit advertentietype pixels die op *[!UICONTROL Impression]* of *[!UICONTROL Click-through]* worden geactiveerd.

**[!UICONTROL Pixel Type]:** Of de pixel een *[!UICONTROL IMG URL]* (1x1 pixelafbeeldingsbestand), *[!UICONTROL HTML]* of *[!UICONTROL JavaScript URL]* is.

**[!UICONTROL Pixel URL or Code]:** De URL van het pixelbeeld, in het aangewezen formaat voor het gespecificeerde Type van Pixel.

**[!UICONTROL Pixel Name]:** De pixelnaam. Gebruik een naam waarmee u de pixel gemakkelijk kunt herkennen.

**[!UICONTROL Pixel Provider]:** De pixelprovider:*[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]* of *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [ Ongeveer Advertentiebeheer ](ad-about.md)
>* [ creeer Één enkele Advertentie ](ad-create.md)
>* [ maak een lijst van de Plaatsen verbonden aan een Advertentie ](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [ Advertentiespecificaties ](ad-specs.md)
>* [ Macro&#39;s van DSP ](/help/dsp/campaign-management/macros.md)
