---
title: Instellingen voor mobiele advertentie
description: Zie beschrijvingen van de beschikbare advertentie-instellingen voor mobiele advertenties.
feature: DSP Ads
exl-id: 45e8da8c-d6a2-4c42-8932-4cf551f6f899
source-git-commit: 9d9330847c9356180928337a4a452f35e7024545
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 0%

---

# Instellingen voor mobiele advertentie

## [!UICONTROL Insert Ad Tag]

*Nieuwe mobiele video adverteert slechts formaten*

**[!UICONTROL URL]** of **[!UICONTROL Ad Tag]**: Een VAST-advertentietag of -advertentietag van derden die creatieve elementen en pixels bijhouden bevat

**[!UICONTROL Ad Title]** of **[!UICONTROL Title]**: Een naam voor de advertentie die wordt gebruikt in de weergave [!UICONTROL Ads] en rapporten.

>[!TIP]
>
> Als u de geldigheid van een VAST-tag wilt controleren, plakt u deze in een browser en drukt u op **[!UICONTROL Enter]** . Als de tag geldig is, ziet u bovenaan een XML-bestand met `<VAST>` .

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: mobiele weergaveadvertenties

**[!UICONTROL Ad Type]:** (read-only) het advertentietype u creeert, dat aan het plaatsingstype beantwoordt waaraan de advertentie kan worden vastgemaakt.

**[!UICONTROL Ad Name]:** De advertentienaam. De titel van het element wordt standaard gebruikt, maar u kunt de naam wijzigen.

>[!TIP]
>
> Gebruik een naam die u gemakkelijk kunt vinden wanneer u de advertentie aan een plaatsing, in de mening van Advertenties, en in rapporten vastmaakt. Beschrijf bijvoorbeeld het eenheidstype en enkele belangrijke kenmerken (zoals Voorvertoning van vakantieproduct: 300 x 250 gamer).

**\[Add Source\]**: (Alleen-lezen) *[!UICONTROL 3rd party]* .

**[!UICONTROL Display Code]:** De URL van het creatieve middel van een derde. Om het even welke [ timestamp ] en [[ timestamp ]] parameters worden vervangen met daadwerkelijke waarden.

**[!UICONTROL Final Display Code]:** URL voor de derde creatieve activa, met de noodzakelijke [ het volgen van Advertising DSP macro&#39;s ](/help/dsp/campaign-management/macros.md) opgenomen, als toepasselijk.

### [!UICONTROL Basic]: video-advertenties

**[!UICONTROL Ad Type]:** (read-only) het advertentietype u creeert, dat aan het plaatsingstype beantwoordt waaraan de advertentie kan worden vastgemaakt.

**[!UICONTROL Ad Name]:** De advertentienaam. De titel van het element wordt standaard gebruikt, maar u kunt de naam wijzigen.

>[!TIP]
>
> Gebruik een naam die u gemakkelijk kunt vinden wanneer u de advertentie aan een plaatsing, in de mening van Advertenties, en in rapporten vastmaakt. Beschrijf bijvoorbeeld het eenheidstype en enkele belangrijke kenmerken (zoals Voorvertoning van vakantieproduct: 30 seconden telefoonpreroll&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** de breedte van de volledige advertentie-eenheid. Deze optie is mogelijk vergrendeld, afhankelijk van het type advertentie-eenheid dat u hebt geselecteerd.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** de hoogte van de volledige advertentie-eenheid. Deze optie is mogelijk vergrendeld, afhankelijk van het type advertentie-eenheid dat u hebt geselecteerd.

**[!UICONTROL Player X]:** De coördinaat van X voor de advertentie-eenheid. De standaardinstelling behouden.

**[!UICONTROL Player Y]:** De Y-coördinaat voor de advertentie-eenheid. De standaardinstelling behouden.

**[!UICONTROL Player Width]:** De breedte van de volledige advertentie-eenheid. Deze optie is mogelijk vergrendeld, afhankelijk van het type advertentie-eenheid dat u hebt geselecteerd.

Dit is hetzelfde als het veld **[!UICONTROL Width]** .

**[!UICONTROL Player Height]:** de hoogte van de volledige advertentie-eenheid. Deze optie is mogelijk vergrendeld, afhankelijk van het type advertentie-eenheid dat u hebt geselecteerd.

Dit is hetzelfde als het veld **[!UICONTROL Height]** .

**[!UICONTROL Show Controls]:** Where to include video controls for the add: *[!UICONTROL Under]* , *[!UICONTROL Over]*, *[!UICONTROL Bottom]* of *[!UICONTROL None]* (the default).

**[!UICONTROL Preserve Aspect Ratio]:** Of om de breedte en hoogteverhoudingen van de video te houden (*[!UICONTROL Yes]*) of de video uit te rekken om beschikbare ruimte te vullen (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Sommige advertenties typen) Het aantal seconden dat nodig is om de weergave van de sluitknop te vertragen.

**[!UICONTROL VAST Tag]:** (Toevoegen met alleen VAST-tags; alleen-lezen) De VAST-tag van derden die u hebt ingevoerd als het creatieve element.

**[!UICONTROL Final VAST Tag]:** (Adds die VAST markeringen gebruiken slechts; read-only) de derde VAST markering u als creatief activa met de noodzakelijke [ gebruikte het volgen van Advertising DSP macro&#39;s ](/help/dsp/campaign-management/macros.md) inging, als toepasselijk.

**[!UICONTROL Wmode]:** (Sommige advertenties) De venstermodus: *[!UICONTROL window]*, *[!UICONTROL transparent]* of *[!UICONTROL opaque]* .

### [!UICONTROL Pixel]

Alle bestaande pixels voor het bijhouden van gebeurtenissen voor de plaatsing worden automatisch gekoppeld. U kunt bestaande pixels loskoppelen en nieuwe pixels maken wanneer dat nodig is, op basis van uw behoeften voor bijhouden voor de afzonderlijke advertentie. **Uiteinde:** om de derde volgende pixel voor veelvoudige advertenties in een plaatsing uit te geven meteen gebruikend de [!UICONTROL Ad Tools] mening, zie &quot;[ het Volgen Pixels van de Derde aan Ads in een Plaatsing ](/help/dsp/campaign-management/ads/ad-pixel-attach-detach.md#attach-pixels-ads) vastmaken.&quot;

De volgende instellingen zijn van toepassing op elke pixel die u maakt of bewerkt.

**[!UICONTROL Integration Event]:** De gebeurtenis die de pixel in brand zet. Gebruik voor dit advertentietype pixels die op *[!UICONTROL Impression]* of *[!UICONTROL Click-through]* worden geactiveerd.

**[!UICONTROL Pixel Type]:** Of de pixel een *[!UICONTROL IMG URL]* (1x1 pixelafbeeldingsbestand), *[!UICONTROL HTML]* of *[!UICONTROL JavaScript URL]* is.

**[!UICONTROL Pixel URL or Code]:** De URL van de pixelafbeelding, in de juiste indeling voor de opgegeven afbeelding [!UICONTROL Pixel Type] .

**[!UICONTROL Pixel Name]:** De pixelnaam. Gebruik een naam waarmee u de pixel gemakkelijk kunt herkennen.

**[!UICONTROL Pixel Provider]:** De pixelprovider: *[!UICONTROL None]* , *[!UICONTROL Comscore]* , *[!UICONTROL WhiteOps]* of *[!UICONTROL IAS]* .

### [!UICONTROL Sharing]

Vervangen

>[!MORELIKETHIS]
>
>* [ Ongeveer Advertentiebeheer ](ad-about.md)
>* [ creeer Één enkele Advertentie ](ad-create.md)
>* [ maak een lijst van de Plaatsen verbonden aan een Advertentie ](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [ Advertentiespecificaties ](ad-specs.md)
>* [ Macro&#39;s van DSP ](/help/dsp/campaign-management/macros.md)
