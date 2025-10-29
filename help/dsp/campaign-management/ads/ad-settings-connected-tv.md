---
title: Instellingen voor aangesloten tv-advertentie
description: Zie beschrijvingen van de beschikbare advertentie-instellingen voor aangesloten tv-advertenties.
feature: DSP Ads
exl-id: d8e47f7e-7480-400f-8ffa-ecf41ce2ebfb
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Instellingen voor aangesloten tv-advertentie

## [!UICONTROL Insert Ad Tag]

*Nieuwe slechts advertenties*

**[!UICONTROL URL]**: De URL van de VAST-tag.

**[!UICONTROL Title]**: Een naam voor het bestand, die wordt gebruikt in de weergave Advertenties en rapporten.

>[!TIP]
>
> Als u de geldigheid van een VAST-tag wilt controleren, plakt u deze in een browser en drukt u op **[!UICONTROL Enter]** . Als de tag geldig is, ziet u bovenaan een XML-bestand met `<VAST>` .

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (read-only) het advertentietype u creeert, dat aan het plaatsingstype beantwoordt waaraan de advertentie kan worden vastgemaakt.

**[!UICONTROL Ad Name]:** De advertentienaam. De titel van het element wordt standaard gebruikt, maar u kunt de naam wijzigen.

>[!TIP]
>
> Gebruik een naam die u gemakkelijk kunt vinden wanneer u de advertentie aan een plaatsing, in de [!UICONTROL Ads] mening, en in rapporten vastmaakt. Beschrijf bijvoorbeeld het eenheidstype en enkele belangrijke kenmerken (zoals Voorvertoning van vakantieproduct: 30 sec CTV).

**[!UICONTROL Width | Ad Unit Width]:** De breedte van de volledige advertentie-eenheid. Deze optie is mogelijk vergrendeld, afhankelijk van het type advertentie-eenheid dat u hebt geselecteerd.

**[!UICONTROL Height | Ad Unit Height]:** de hoogte van de volledige advertentie-eenheid. Deze optie is mogelijk vergrendeld, afhankelijk van het type advertentie-eenheid dat u hebt geselecteerd.

**[!UICONTROL Player X]:** De coördinaat van X voor de advertentie-eenheid. De standaardinstelling behouden.

**[!UICONTROL Player Y]:** De Y-coördinaat voor de advertentie-eenheid. De standaardinstelling behouden.

**[!UICONTROL Player Width]:** De breedte van de volledige advertentie-eenheid. Deze optie is mogelijk vergrendeld, afhankelijk van het type advertentie-eenheid dat u hebt geselecteerd.

Dit is hetzelfde als het veld **[!UICONTROL Width]** .

**[!UICONTROL Player Height]:** de hoogte van de volledige advertentie-eenheid. Deze optie is mogelijk vergrendeld, afhankelijk van het type advertentie-eenheid dat u hebt geselecteerd.

Dit is hetzelfde als het veld **[!UICONTROL Height]** .

**[!UICONTROL Show Controls]:** Where to include video controls for the add: *[!UICONTROL Under]* , *[!UICONTROL Over]*, *[!UICONTROL Bottom]* of *[!UICONTROL None]* (the default).

**[!UICONTROL Preserve Aspect Ratio]:** Of om de breedte en hoogteverhoudingen van de video te houden (*[!UICONTROL Yes]*) of de video uit te rekken om beschikbare ruimte te vullen (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Toevoegen met alleen VAST-tags; alleen-lezen) De VAST-tag van derden die u hebt ingevoerd als advertentiebron.

**[!UICONTROL Final VAST Tag]:** (Adds gebruikend VAST markeringen slechts; read-only) de derde VAST markering u als advertentiebron met de noodzakelijke [ gebruikte het volgen van Advertising DSP macro&#39;s ](/help/dsp/campaign-management/macros.md) inging, als toepasselijk.

**[!UICONTROL Clock Number]**: (Wordt alleen gebruikt in het Verenigd Koninkrijk; alleen beschikbaar voor gebruikers met toestemming) Een unieke id die wordt gebruikt om ervoor te zorgen dat de juiste advertentie wordt uitgezonden. Laat deze instelling leeg als deze niet van toepassing is.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [ Ongeveer Advertentiebeheer ](ad-about.md)
>* [ creeer Één enkele Advertentie ](ad-create.md)
>* [ maak een lijst van de Plaatsen verbonden aan een Advertentie ](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [ Advertentiespecificaties ](ad-specs.md)
>* [ Macro&#39;s van DSP ](/help/dsp/campaign-management/macros.md)
