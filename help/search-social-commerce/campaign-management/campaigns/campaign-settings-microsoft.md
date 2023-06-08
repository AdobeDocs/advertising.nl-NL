---
title: "[!DNL Microsoft Advertising] campagne-instellingen"
description: Verwijs naar de instellingen voor [!DNL Microsoft Advertising] campagnes.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] campagne-instellingen

## \[Scherm Campagne maken\]

**[!UICONTROL Campaign Type]:** (Alleen beschikbaar tijdens het maken van campagnes) Waar kunt u advertenties plaatsen en welke advertentietypes de campagne kan bevatten:

* *[!UICONTROL Search and Display Network]:* Hiermee geeft u alleen tekstadvertenties weer op het zoeknetwerk.

* *[!UICONTROL Shopping Network]:* Geeft productadvertenties en mdashl voor uw producten in uw [!DNL Microsoft Merchant Center] productcatalogus — op het winkelnetwerk

* *[!UICONTROL Audience]:* Geeft native/weergaveadvertenties weer op het tabblad [!DNL Microsoft Audience Network]. U kunt a) automatisch op feed gebaseerde advertenties genereren door de campagne te koppelen aan een winkelcentrum in het [!UICONTROL Shopping Settings] sectie of b) responsieve advertenties maken met tekstmiddelen en geüploade afbeeldingen. Voor beide opties moet u ad-hocgroepen maken waarvoor de gebruiker een doel instelt.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Een campagnenaam die uniek is binnen de account. De maximumlengte is 128 tekens.

**[!UICONTROL Status]:** De weergavestatus van de campagne: *Actief* of *Gepauzeerd*. De standaardinstelling voor nieuwe advertentiecampagnes is *Actief*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** De biedstrategie voor de campagne:

* *[!UICONTROL Enhanced CPC]:* (Campagnes op het publiek, onderzoek, en het winkelen netwerken) gebruikt het verbeterde kosten-per-klikmodel van het advertentienetwerk (eCPC), dat het advertentienetwerk toestaat om de kosten-per-klikbieding (CPC) voor elke veiling automatisch te veranderen in een poging om omzettingen te maximaliseren, gebruikend omzetting(s) binnen het advertentienetwerk (niet in Onderzoek, Sociale, &amp; Handel) worden gespecificeerd, terwijl het proberen om te houden onder uw gemiddelde CPC CPC.

Wanneer u een campagne met eCPC toevoegt aan een geoptimaliseerde portefeuille van Onderzoek, Sociale, &amp; Handel, optimaliseert Onderzoek, Sociale, &amp; Handel de basisbiedingen en — wanneer &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; optie is ingeschakeld — het campagnebudget. Het advertentienetwerk optimaliseert alle biedingsaanpassingen en kan het Onderzoek, Sociale, &amp; Commerce-Gegenereerde bod op het tijdstip van de gebruikersvraag veranderen die op merkgebonden gegevens en inzichten wordt gebaseerd. **Let op:** Gebruik eCPC-campagnes alleen in portfolio&#39;s wanneer de totale conversies die op het advertentienetwerk worden bijgehouden, overeenkomen met de portfoliodoelstelling.

* *[!UICONTROL Manual CPC]* (de standaardinstelling): (Vervangen door [!DNL Microsoft Advertising] (2021) Gebruikt het CPC-model (cost per click). U kunt desgewenst toestaan het advertentienetwerk om biedingen voor de campagne te veranderen:

   * **[!UICONTROL Enable Enhanced CPC]** (standaard uitgeschakeld): Dit is hetzelfde als het gebruik van &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Manual CPM]* (Campagnes op het publieksnetwerk slechts) gebruikt het kosten-per-duizend-impressies (CPM) model, waarvoor u specificeert wat u per 1.000 bekeken beelden wilt uitgeven. Campagnes met deze biedstrategie worden niet geoptimaliseerd wanneer ze in portfolio&#39;s worden opgenomen.

* *[!UICONTROL Maximize Clicks]:* (Zoeken en winkelen) Het advertentienetwerk — niet Zoeken, Sociaal en Handel — optimaliseert biedingen om de klikmogelijkheden te maximaliseren. Voer desgewenst een **[!UICONTROL Max CPC]** (kosten per klik) om ervoor te zorgen dat het advertentienetwerk niet meer dan een specifiek bedrag voor elke klik betaalt. **Let op:** Wanneer u een campagne met deze strategie toevoegt aan een portfolio, worden de biedingen bepaald door het gewicht van de klik en niet door het doel van het portfolio.

* *[!UICONTROL Maximize Conversion Value]:* (Zoeken en winkelen/smart shopping-netwerken) Het advertentienetwerk — niet Zoeken, Sociaal, &amp; Handel — optimaliseert biedingen om de conversiewaarde te maximaliseren. Voer desgewenst een **[!UICONTROL Target Return on Ad Spend]** (ROAS) als een percentage. **Opmerking:** Gebruik deze optie voor campagnes in hybride portefeuilles maar niet standaardportefeuilles.

* *[!UICONTROL Maximize Conversions]:* (Campagnes op het onderzoeksnetwerk <!-- future: and audience network -->) Het advertentienetwerk — niet Zoeken, Sociaal, &amp; Handel — optimaliseert biedingen om omzettingen te maximaliseren. Voer desgewenst een **[!UICONTROL Target CPC]** (kosten per klik)<!-- future: ; for audience campaigns, you can also enter an optional [!UICONTROL Target CPA] (cost per acquisition) -->. **Opmerking:** Gebruik deze optie voor campagnes in hybride portefeuilles maar niet standaardportefeuilles.

* *[!UICONTROL Target CPA]:* (Campagnes op het onderzoeksnetwerk) Het advertentienetwerk — niet Onderzoek, Sociale, &amp; Handel — optimaliseert biedingen die op facultatief worden gebaseerd **[!UICONTROL Target CPA]** (kosten per overname), dat is het gemiddelde bedrag van 30 dagen dat u voor een overname (omzetting) wilt betalen. **Opmerking:** Gebruik deze optie voor campagnes in hybride portefeuilles (maar niet standaardportefeuilles) met om het even welke uitgavenstrategie behalve [!UICONTROL Weekly] of [!UICONTROL Google Target CPA].

   Gemiddelde positie en CPC-biedgegevens zijn niet beschikbaar voor campagnes met deze biedstrategie.

* *[!UICONTROL Target Impression Share]:* (Campagnes op het onderzoeksnetwerk) Het advertentienetwerk — niet Onderzoek, Sociale, &amp; Handel — optimaliseert biedingen om een doelimitatieaandeel en een advertentiepositie te bereiken. Voer desgewenst een **[!UICONTROL Target Impression Share]** als percentage, **[!UICONTROL Target Ad Position]** en **[!UICONTROL Max CPC]** (kosten per klik). **Opmerking:** Deze optie wordt niet ondersteund in hybride portfolio&#39;s.

* *[!UICONTROL Target Return on Ad Spend]:*  (Campagnes op de zoek en het winkelen netwerken) Het advertentienetwerk — niet Zoeken, Sociaal, &amp; Handel — optimaliseert biedingen op basis van uw **[!UICONTROL Target ROAS]** (Retourneren bij advertentie), opgegeven als een percentage. Voer desgewenst een **[!UICONTROL Max CPC]** (kosten per klik) om ervoor te zorgen dat het advertentienetwerk niet meer betaalt dan een bepaald bedrag voor elke klik. **Opmerking:** Gebruik deze optie voor campagnes in hybride portefeuilles (maar niet standaardportefeuilles) met om het even welke uitgavenstrategie behalve [!UICONTROL Weekly] of [!UICONTROL Google Target ROAS].

   Gemiddelde positie en CPC-biedgegevens zijn niet beschikbaar voor campagnes met deze biedstrategie.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Alleen koopcampagnes; alleen-lezen voor bestaande campagnes) Het land waar de campagneproducten worden verkocht. Omdat de producten met doellanden worden geassocieerd, bepaalt dit het plaatsen welke producten in de campagne worden geadverteerd.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]:** (alleen campagnes van het publiek; (optioneel) Koppelt de campagne aan een specifieke winkel voor automatische advertenties op basis van feed-in in plaats van responsieve advertenties. Wanneer u deze optie selecteert, geeft u de opdracht [!UICONTROL Merchant ID] en [!UICONTROL Products]. U moet advertentiegroepen maken voor de campagne, maar u hoeft geen advertenties te maken.

Als u de campagne eenmaal aan een winkel hebt gekoppeld en de instellingen hebt opgeslagen, kunt u deze optie niet meer wijzigen.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}


**[!UICONTROL Products]:** (Poortcampagnes die alleen zijn gekoppeld aan een winkelcentrum) De producten die moeten worden geadverteerd. Standaard, *[!UICONTROL All products]* is geselecteerd. Als u alleen producten met specifieke kenmerken wilt adverteren, selecteert u *[!UICONTROL Filter products]* en geef maximaal zeven combinaties van productafmetingen en kenmerken op waarop u uw producten wilt filteren. Voor advertenties die voor het product worden weergegeven, moeten alle opgegeven waarden van toepassing zijn. Als u bijvoorbeeld advertenties wilt weergeven voor de producten van Acme-huisdieren, kunt u de filters maken `Custom Label 1=animals`, `Category=pet supplies`, en `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

<!-- **[!UICONTROL Landing Page Suffix]:** -->

{{$include /help/_includes/landing-page-suffix.md}}

## [!UICONTROL DSA Options]

<!-- **[!UICONTROL Website Domain]:** -->

{{$include /help/_includes/website-domain.md}}

<!-- **[!UICONTROL DSA Language]:** -->

{{$include /help/_includes/dsa-language.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** (Alleen campagnes op het display/native netwerk; (optioneel) Sites op het weergavenetwerk waarop u uw advertenties niet wilt weergeven. Voer een geldige URL in, bijvoorbeeld www.example.com. Als u meerdere tekenreeksen wilt opgeven, scheidt u deze met komma&#39;s of voert u ze op afzonderlijke regels in.

Raadpleeg voor meer informatie over beschikbaarheid de Help bij Microsoft Advertising voor &quot;[Voorkomen dat advertenties op bepaalde websites worden weergegeven](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

## [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (Voor [!UICONTROL EF Redirect] alleen) Niet geïmplementeerd

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

>[!MORELIKETHIS]
>
>* [Campagnes beheren](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)

