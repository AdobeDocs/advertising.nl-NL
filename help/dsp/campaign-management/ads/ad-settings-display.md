---
title: Ad-instellingen weergeven
description: Zie beschrijvingen van de beschikbare advertentie-instellingen voor weergaveadvertenties.
feature: DSP Ads
exl-id: cff65a48-486f-401e-9759-2bb63871448f
source-git-commit: 863bf7a4d8304e42b7004742de59b9e1a09f81b7
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Ad-instellingen weergeven

De volgende instellingen gelden voor standaardweergaveadvertenties.

## [!UICONTROL Ad Options]

### Basis

**[!UICONTROL Ad Type]:** (read-only) het advertentietype u creeert, dat aan het plaatsingstype beantwoordt waaraan de advertentie kan worden vastgemaakt. De standaardwaarde is *[!UICONTROL Display]* .

**[!UICONTROL Ad Name]:** De advertentienaam. De titel van het element wordt standaard gebruikt, maar u kunt de naam wijzigen.

>[!TIP]
>
> Gebruik een naam die u gemakkelijk kunt vinden wanneer u de advertentie aan een plaatsing, in de [!UICONTROL Ads] mening, en in rapporten vastmaakt. Beschrijf bijvoorbeeld het eenheidstype en enkele belangrijke kenmerken (zoals Voorvertoning van vakantieproduct: 300 x 250 gamer).

**\[Add Source\]**: (Alleen-lezen) *[!UICONTROL 3rd party]* .

**[!UICONTROL This is an expandable Banner]:** (Alleen advertenties van derden) Geeft aan dat de advertentie een uitbreidbare banneradvertentie is. De gerelateerde uitbreidingsinstellingen bepalen welke voorraad moet worden aangeschaft, zodat deze het advertentiegedrag weerspiegelen.

**[!UICONTROL Expansion Method]:** (Alleen banneradvertenties van derden die kunnen worden uitgebreid) Of de banner wordt uitgebreid *[!UICONTROL Click]* of *[!UICONTROL Rollover]* .

**[!UICONTROL Expansion Directions]:** (Uitgebreide banneradvertenties van derden alleen) De richting waarin de advertentie wordt uitgebreid: *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]* of *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (Alleen externe banneradvertenties) De gecertificeerde leverancier waarvoor de advertentie beschikbaar is: *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]* of *[!UICONTROL Jivox]* .

**[!UICONTROL Display Code]:** (Alleen advertenties van derden) De URL van het creatieve middel van derden. Om het even welke [ timestamp ] en [[ timestamp ]] parameters worden vervangen met daadwerkelijke waarden.

**[!UICONTROL Final Display Code]:** (De derdeadvertenties slechts) URL voor de derde creatieve activa, met de noodzakelijke [&#x200B; het volgen van Advertising DSP macro&#39;s &#x200B;](/help/dsp/campaign-management/macros.md) opgenomen, als toepasselijk.

**[!UICONTROL Ad Size]:** De breedte en hoogte van de advertentie. Het moet a [&#x200B; gesteunde standaardvertoning en grootte &#x200B;](ad-specs.md) zijn. U kunt de advertentiegrootte handmatig invoeren voordat u de advertentie uploadt of een [!UICONTROL Display Code] invoeren. Als u de advertentiegrootte niet invoert, worden de afmetingen van de geüploade advertentie of advertentietag automatisch ingevoerd als alleen-lezen.

>[!IMPORTANT]
>
> De advertentiegrootte die in de velden width en height wordt gedeclareerd, komt overeen met binnenkomende biedaanvragen. U kunt leveringsproblemen ervaren als de afmetingen van de advertentie niet overeenkomen met de opgegeven advertentiegrootte.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer Advertentiebeheer &#x200B;](ad-about.md)
>* [&#x200B; creeer Één enkele Advertentie &#x200B;](ad-create.md)
>* [&#x200B; maak een lijst van de Plaatsen verbonden aan een Advertentie &#x200B;](ad-list-placements.md)
>* [&#x200B; Advertentiespecificaties &#x200B;](ad-specs.md)
>* [&#x200B; Macro&#39;s van DSP &#x200B;](/help/dsp/campaign-management/macros.md)
