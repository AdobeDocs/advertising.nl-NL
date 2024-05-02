---
title: Instellingen voor Universal Video Add
description: Zie beschrijvingen van de beschikbare advertentie-instellingen voor universele videoadvertenties.
feature: DSP Ads
exl-id: 51b7d632-1e73-4726-980b-07ed50447146
source-git-commit: f521cf26d9d3945bdf1abe4577bb37d732432c87
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Instellingen voor Universal Video Add

>[!NOTE]
>
>Universele video-advertenties kunnen alleen worden gekoppeld aan universele video-opnamen.

## [!UICONTROL Insert Ad Tag]

*Alleen nieuwe advertenties*

**[!UICONTROL URL]:** De URL van de VAST-tag.

**[!UICONTROL Title]:** Een titel voor het bestand, die zich in het dialoogvenster [!UICONTROL Ads] bekijken en rapporteren.

>[!TIP]
>
> Als u de geldigheid van een VAST-tag wilt controleren, plakt u deze in een browser en klikt u op de knop **[!UICONTROL Enter]** toets. Als de tag geldig is, ziet u een XML-bestand dat `<VAST>` aan de bovenkant.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Alleen-lezen) Het advertentietype dat u maakt, komt overeen met het plaatsingstype waaraan de advertentie kan worden gekoppeld.

**[!UICONTROL Ad Name]:** De advertentienaam. De titel van het element wordt standaard gebruikt, maar u kunt de naam wijzigen.

>[!TIP]
>
> Gebruik een naam die u gemakkelijk kunt vinden wanneer u de advertentie aan een plaatsing, in [!UICONTROL Ads] en in rapporten. Beschrijf bijvoorbeeld het eenheidstype en enkele belangrijke kenmerken (zoals Voorvertoning van vakantieproduct: 30 sec Universal Video&quot;).

**[!UICONTROL Show Controls]:** Waar moeten videobesturingselementen voor de advertentie worden opgenomen: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]*, of *[!UICONTROL None]* (de standaardwaarde).

**[!UICONTROL Preserve Aspect Ratio]:** Of de breedte- en hoogteverhouding van de video behouden moet blijven (*[!UICONTROL Yes]*) of om de video uit te rekken tot de beschikbare ruimte (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Toevoegen met alleen VAST-tags; alleen-lezen) De VAST-tag van derden die u hebt ingevoerd als advertentiebron.

**[!UICONTROL Final VAST Tag]:** (Toevoegen met alleen VAST-tags; alleen-lezen) De VAST-tag van derden die u als advertentiebron hebt opgegeven, beschikt over de vereiste [Reclame DSP het volgen macro&#39;s](/help/dsp/campaign-management/macros.md) ingevoegd, indien van toepassing.

**[!UICONTROL Wmode]:** De venstermodus: *[!UICONTROL window]*, *[!UICONTROL transparent]*, of *[!UICONTROL opaque]*. Laat deze instelling leeg als deze niet van toepassing is.

**[!UICONTROL Video Format]:** De indeling van de advertentiespeler voor mogelijke inventarisatie: *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]*, of *[!UICONTROL VAST]*. Zichtbaarheid wordt altijd gemeten voor [!UICONTROL VPAID], maar [!UICONTROL VPAID & VAST] bevat een overzicht waarin geen meting van de weergavemogelijkheid is toegestaan. Houd rekening met dit verschil als meetgegevens voor de weergavemogelijkheden belangrijk zijn voor uw campagne.

Gebruiken [!UICONTROL VAST], die geen meting van de weergavekwaliteit toestaat, wanneer u zich richt op aangesloten tv of inventaris die uitsluitend VAST-indeling vereist (gewoonlijk van leveringsbronnen zoals Google Ad Manager, Appnexus, SpotX en Freewiel). Gebruik deze optie ook voor voorraad die eerder compatibel was met de standaardinstellingen voor Pre-roll (VAST) of Phone + Tablet Standard Pre-roll (VAST).

**[!UICONTROL Clock Number]**: (Wordt alleen gebruikt in het Verenigd Koninkrijk; alleen beschikbaar voor gebruikers met toestemming) Een unieke id die wordt gebruikt om ervoor te zorgen dat de rechteradvertentie wordt uitgezonden. Laat deze instelling leeg als deze niet van toepassing is.

### [!UICONTROL Pixel]

Alle bestaande pixels voor het bijhouden van gebeurtenissen voor de plaatsing worden automatisch gekoppeld. U kunt bestaande pixels loskoppelen en nieuwe pixels maken wanneer dat nodig is, op basis van uw behoeften voor bijhouden voor de afzonderlijke advertentie.

De volgende instellingen zijn van toepassing op elke pixel die u maakt of bewerkt.

**[!UICONTROL Integration Event]:** De gebeurtenis die de pixel activeert. Gebruik voor dit advertentietype pixels die op het *[!UICONTROL Impression]* of *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Of de pixel een *[!UICONTROL IMG URL]* (afbeeldingsbestand van 1 x 1 pixel), *[!UICONTROL HTML]*, of *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** De URL van de pixelafbeelding, in de juiste indeling voor de opgegeven [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** De pixelnaam. Gebruik een naam waarmee u de pixel gemakkelijk kunt herkennen.

**[!UICONTROL Pixel Provider]:** De pixelprovider: *[!UICONTROL None]*, *[!UICONTROL Comscore]*, *[!UICONTROL WhiteOps]*, of *[!UICONTROL IAS]*.

>[!MORELIKETHIS]
>
>* [Veelgestelde vragen over Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
>* [Over Advertentiebeheer](ad-about.md)
>* [Eén advertentie maken](ad-create.md)
>* [De aan een advertentie gekoppelde plaatsen weergeven](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Ad-specificaties](ad-specs.md)
>* [DSP Macros](/help/dsp/campaign-management/macros.md)
