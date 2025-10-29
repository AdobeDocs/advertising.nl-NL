---
title: Instellingen voor pre-roll-advertentie
description: Zie beschrijvingen van de beschikbare advertentie-instellingen voor pre-roladvertenties.
feature: DSP Ads
exl-id: d0ba4346-13ae-405c-92b6-a0c32dd09d0a
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 0%

---

# Instellingen voor pre-roll-advertentie

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
> Gebruik een naam die u gemakkelijk kunt vinden wanneer u de advertentie aan een plaatsing, in de [!UICONTROL Ads] mening, en in rapporten vastmaakt. Beschrijf bijvoorbeeld het eenheidstype en enkele belangrijke kenmerken (zoals Voorvertoning van vakantieproduct: 30 sec Preroll&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** (Standaard en skippable pre-roladvertenties slechts) de breedte van de volledige advertentie-eenheid. Deze optie is mogelijk vergrendeld, afhankelijk van het type advertentie-eenheid dat u hebt geselecteerd.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** (Standaard en skippable pre-roladvertenties slechts) de hoogte van de volledige advertentie-eenheid. Deze optie is mogelijk vergrendeld, afhankelijk van het type advertentie-eenheid dat u hebt geselecteerd.

**[!UICONTROL Player X]:** De coördinaat van X voor de advertentie-eenheid. De standaardinstelling behouden.

**[!UICONTROL Player Y]:** De Y-coördinaat voor de advertentie-eenheid. De standaardinstelling behouden.

**[!UICONTROL Player Width]:** De breedte van de volledige advertentie-eenheid. Deze optie is mogelijk vergrendeld, afhankelijk van het type advertentie-eenheid dat u hebt geselecteerd.

Dit veld is hetzelfde als het veld **[!UICONTROL Width]** .

**[!UICONTROL Player Height]:** de hoogte van de volledige advertentie-eenheid. Deze optie is mogelijk vergrendeld, afhankelijk van het type advertentie-eenheid dat u hebt geselecteerd.

Dit is hetzelfde als het veld **[!UICONTROL Height]** .

**[!UICONTROL Show Controls]:** Where to include video controls for the add: *[!UICONTROL Under]* , *[!UICONTROL Over]*, *[!UICONTROL Bottom]* of *[!UICONTROL None]* (the default).

**[!UICONTROL Preserve Aspect Ratio]:** Of om de breedte en hoogteverhoudingen van de video (*[!UICONTROL Yes]*) te houden of de video uit te rekken om beschikbare ruimte te vullen (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Toevoegen met alleen VAST-tags; alleen-lezen) De VAST-tag van derden die u hebt ingevoerd als advertentiebron.

**[!UICONTROL Final VAST Tag]:** (Adds gebruikend VAST markeringen slechts; read-only) de derde VAST markering u als advertentiebron met de noodzakelijke [&#x200B; gebruikte het volgen van Advertising DSP macro&#39;s &#x200B;](/help/dsp/campaign-management/macros.md) inging, als toepasselijk.

**[!UICONTROL Wmode]:** (Interactief pre-rol slechts) de vensterwijze: *[!UICONTROL window]*, *[!UICONTROL transparent]*, of *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:** (Interactief pre-rol slechts) het formaat van de advertentiespeler voor potentiële inventaris: *[!UICONTROL VPAID]* of *[!UICONTROL VPAID & VAST]*. Zichtbaarheid wordt altijd gemeten voor VPAID, maar VPAID &amp; VAST bevat voorraad die geen meetbaarheid toestaat. Houd rekening met dit verschil als meetgegevens voor de weergavemogelijkheden belangrijk zijn voor uw campagne.

**[!UICONTROL Clock Number]**: (Alleen interactief pre-roll; alleen gebruikt in het Verenigd Koninkrijk; alleen beschikbaar voor gebruikers met toestemming) Een unieke id die wordt gebruikt om ervoor te zorgen dat de rechteradvertentie wordt uitgezonden. Laat deze instelling leeg als deze niet van toepassing is.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer Advertentiebeheer &#x200B;](ad-about.md)
>* [&#x200B; creeer Één enkele Advertentie &#x200B;](ad-create.md)
>* [&#x200B; maak een lijst van de Plaatsen verbonden aan een Advertentie &#x200B;](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [&#x200B; Advertentiespecificaties &#x200B;](ad-specs.md)
>* [&#x200B; Macro&#39;s van DSP &#x200B;](/help/dsp/campaign-management/macros.md)
