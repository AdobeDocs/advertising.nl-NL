---
title: Instellingen voor aangesloten tv-advertentie
description: Zie beschrijvingen van de beschikbare advertentie-instellingen voor aangesloten tv-advertenties.
feature: DSP Ads
exl-id: d8e47f7e-7480-400f-8ffa-ecf41ce2ebfb
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Instellingen voor aangesloten tv-advertentie

## [!UICONTROL Insert Ad Tag]

*Alleen nieuwe advertenties*

**[!UICONTROL URL]**: De URL van de VAST-tag.

**[!UICONTROL Title]**: Een naam voor het bestand, die wordt gebruikt in de weergave Advertenties en in rapporten.

>[!TIP]
>
> Als u de geldigheid van een VAST-tag wilt controleren, plakt u deze in een browser en klikt u op de knop **[!UICONTROL Enter]** toets. Als de tag geldig is, wordt een XML-bestand weergegeven dat `<VAST>` aan de bovenkant.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Alleen-lezen) Het advertentietype dat u maakt, komt overeen met het plaatsingstype waaraan de advertentie kan worden gekoppeld.

**[!UICONTROL Ad Name]:** De advertentienaam. De titel van het element wordt standaard gebruikt, maar u kunt de naam wijzigen.

>[!TIP]
>
> Gebruik een naam die u gemakkelijk kunt vinden wanneer u de advertentie aan een plaatsing, in [!UICONTROL Ads] en in rapporten. Beschrijf bijvoorbeeld het eenheidstype en enkele belangrijke kenmerken (zoals Voorvertoning van vakantieproduct: 30 sec CTV).

**[!UICONTROL Width | Ad Unit Width]:** De breedte van de gehele advertentie-eenheid. Deze optie is mogelijk vergrendeld, afhankelijk van het type advertentie-eenheid dat u hebt geselecteerd.

**[!UICONTROL Height | Ad Unit Height]:** De hoogte van de gehele advertentie-eenheid. Deze optie is mogelijk vergrendeld, afhankelijk van het type advertentie-eenheid dat u hebt geselecteerd.

**[!UICONTROL Player X]:** De X-coördinaat voor de advertentie-eenheid. De standaardinstelling behouden.

**[!UICONTROL Player Y]:** De Y-coördinaat voor de advertentie-eenheid. De standaardinstelling behouden.

**[!UICONTROL Player Width]:** De breedte van de gehele advertentie-eenheid. Deze optie is mogelijk vergrendeld, afhankelijk van het type advertentie-eenheid dat u hebt geselecteerd.

Dit is hetzelfde als **[!UICONTROL Width]** veld.

**[!UICONTROL Player Height]:** De hoogte van de gehele advertentie-eenheid. Deze optie is mogelijk vergrendeld, afhankelijk van het type advertentie-eenheid dat u hebt geselecteerd.

Dit is hetzelfde als **[!UICONTROL Height]** veld.

**[!UICONTROL Show Controls]:** Waar moeten videobesturingselementen voor de advertentie worden opgenomen: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, of *[!UICONTROL None]* (de standaardwaarde).

**[!UICONTROL Preserve Aspect Ratio]:** Of de breedte- en hoogteverhouding van de video behouden moet blijven (*[!UICONTROL Yes]*) of om de video uit te rekken tot de beschikbare ruimte (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Toevoegen met alleen VAST-tags; alleen-lezen) De VAST-tag van derden die u hebt ingevoerd als advertentiebron.

**[!UICONTROL Final VAST Tag]:** (Toevoegen met alleen VAST-tags; alleen-lezen) De VAST-tag van derden die u als advertentiebron hebt opgegeven, beschikt over de vereiste [Reclame DSP het volgen macro&#39;s](/help/dsp/campaign-management/macros.md) ingevoegd, indien van toepassing.

**[!UICONTROL Clock Number]**: (Wordt alleen gebruikt in het Verenigd Koninkrijk; alleen beschikbaar voor gebruikers met toestemming) Een unieke id die wordt gebruikt om ervoor te zorgen dat de rechteradvertentie wordt uitgezonden. Laat deze instelling leeg als deze niet van toepassing is.

### [!UICONTROL Pixel]

Alle bestaande pixels voor het bijhouden van gebeurtenissen voor de plaatsing worden automatisch gekoppeld. U kunt bestaande pixels loskoppelen en nieuwe pixels maken wanneer dat nodig is, op basis van uw behoeften voor bijhouden voor de afzonderlijke advertentie. **Tip:** De volgende pixels van derden voor meerdere advertenties tegelijk bewerken met de opdracht [!UICONTROL Ad Tools] bekijken, zie &quot;[Pixels van derden bijvoegen bij advertenties in een plaatsing](/help/dsp/campaign-management/ads/ad-attach-to-placement.md#attach-pixels-ads).&quot;

De volgende instellingen zijn van toepassing op elke pixel die u maakt of bewerkt.

**[!UICONTROL Integration Event]:** De gebeurtenis die de pixel activeert. Gebruik voor dit advertentietype pixels die op het *[!UICONTROL Impression]* of *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Of de pixel een *[!UICONTROL IMG URL]* (afbeeldingsbestand van 1 x 1 pixel), *[!UICONTROL HTML]*, of *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** De URL van de pixelafbeelding, in de juiste indeling voor het opgegeven pixeltype.

**[!UICONTROL Pixel Name]:** De pixelnaam. Gebruik een naam waarmee u de pixel gemakkelijk kunt herkennen.

**[!UICONTROL Pixel Provider]:** De pixelprovider: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, of *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Over Advertentiebeheer](ad-about.md)
>* [Eén advertentie maken](ad-create.md)
>* [De aan een advertentie gekoppelde plaatsen weergeven](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Ad-specificaties](ad-specs.md)
>* [DSP Macros](/help/dsp/campaign-management/macros.md)
