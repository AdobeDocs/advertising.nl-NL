---
title: '[!DNL Microsoft® Advertising] campagne-instellingen'
description: Verwijs naar de instellingen voor [!DNL Microsoft® Advertising] campagnes.
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: 96ff5244c5baedf009c1bac05b609611607bd867
workflow-type: tm+mt
source-wordcount: '1904'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] campagne-instellingen

## \[Scherm Campagne maken\]

**[!UICONTROL Campaign Type]:** (Alleen beschikbaar tijdens het maken van campagnes) Waar kunt u advertenties plaatsen en welke advertentietypes de campagne kan bevatten:

* *[!UICONTROL Search]:* Geeft tekstadvertenties weer op het zoeknetwerk.

* *[!UICONTROL Shopping Network]:* Geeft productadvertenties weer — voor uw producten in uw [!DNL Microsoft® Merchant Center] productcatalogus — op het winkelnetwerk.

* *[!UICONTROL Audience]:* Geeft native/weergaveadvertenties weer op het tabblad [!DNL Microsoft® Audience Network]. U kunt a) automatisch op feed gebaseerde advertenties genereren door de campagne te koppelen aan een winkelcentrum in het [!UICONTROL Shopping Settings] sectie of b) responsieve advertenties maken met tekstmiddelen en geüploade afbeeldingen. Voor beide opties moet u ad-hocgroepen maken waarvoor de gebruiker een doel instelt.

* *[!UICONTROL Shopping Campaigns for Brands]:* (Beta eigenschap) bevordert uw producten door verbonden detailhandelaren over het onderzoek en publieksnetwerken. U kunt onderliggende en productgroepen en productgroepen maken (apps die u wilt promoten) en optionele productadvertenties voor de campagne maken. [!DNL Microsoft® Advertising] maakt automatisch advertenties voor de productgroepen. Gebruik de biedstrategie voor winkelcampagnes voor merken [!UICONTROL Manual CPC]; gebruik de biedstrategie voor het winkelen van merken [!UICONTROL Cost per Sale].

* *[!UICONTROL Microsoft® Store Ads Campaign]:* (Beta-functie) Hiermee promoot u uw apps en games die beschikbaar zijn in de [!DNL Microsoft® Store]. U kunt onderliggende en optionele productgroepen, productgroepen en advertenties voor de campagne maken. [!DNL Microsoft® Advertising] maakt automatisch advertenties voor de productgroepen.

* *[!UICONTROL Audience CTV Video]:* (Bètafunctie) Hiermee kunt u aangesloten tv-videobanden (CTV) weergeven op het publieksnetwerk.

* *[!UICONTROL Audience Video]:* (De eigenschap van Bèta) toont standaardvideoadvertenties op het publieksnetwerk.

* *[!UICONTROL Performance Max]:* (De eigenschap van Bèta) toont veelvoudige advertentietypes over alle netwerken gebruikend [!DNL Microsoft Advertising] slim bieden. Binnen de montages van de campagne, moet u één of meerdere activa specificeren, die beelden, logo&#39;s, koppen, beschrijvingen, een facultatieve vraag aan actie, en publiekssignalen omvatten. Het advertentienetwerk combineert automatisch de activa om advertenties te dienen die op het kanaal worden gebaseerd.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Een campagnenaam die uniek is binnen de account. De maximumlengte is 128 tekens.

**[!UICONTROL Status]:** De weergavestatus van de campagne: *Actief* of *Gepauzeerd*. De standaardwaarde voor nieuwe advertentiecampagnes is *Actief*.

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

* *[!UICONTROL Cost per Sale]:* (Alleen winkelcampagnes) Het advertentienetwerk — niet Zoeken, Sociaal en Commerce — optimaliseert biedingen op basis van de **[!UICONTROL Target CPS]** (kosten per verkoop). Je betaalt alleen wanneer je op je product klikt en de transactie binnen 24 uur plaatsvindt. **Opmerking:** Gebruik deze optie voor campagnes in hybride portefeuilles maar niet standaardportefeuilles.<!-- Verify all -->

  Als je eenmaal een winkelcampagne voor merken hebt opgeslagen met deze biedstrategie, kun je de biedstrategie niet meer wijzigen. Voor andere soorten winkelcampagnes is deze strategie alleen beschikbaar voor nieuwe campagnes.

* *[!UICONTROL CPV]* (Alleen CTV-videocampagnes van het publiek) Gebruikt het model voor de kosten per weergave (CPV). <!-- Campaigns with this bid strategy aren't optimized when they're included in portfolios. -->

* *[!UICONTROL Enhanced CPC]:* (Campagnes op het publiek, onderzoek, en het winkelen netwerken) gebruikt het verbeterde kosten-per-klikmodel van het advertentienetwerk (eCPC), dat het advertentienetwerk toestaat om de kosten-per-klikbieding (CPC) voor elke veiling automatisch te veranderen in een poging om omzettingen te maximaliseren, gebruikend omzettingen binnen het advertentienetwerk (niet in Onderzoek, Sociale, &amp; Commerce) worden gespecificeerd, terwijl het proberen om te houden uw gemiddelde CPC onder uw maximum.

  Wanneer u een campagne met eCPC toevoegt aan een geoptimaliseerde portefeuille van Zoeken, Sociale, &amp; Commerce, optimaliseert het Onderzoek, Sociale, &amp; Commerce de basisbiedingen en — wanneer &quot;[!UICONTROL Auto adjust campaign budget limits]&quot; optie is ingeschakeld — het campagnebudget. Het advertentienetwerk optimaliseert alle biedingsaanpassingen en kan de door Zoeken, Sociale en Commerce gegenereerde biedingen wijzigen op het moment van de gebruikersquery op basis van eigen gegevens en inzichten. **Let op:** Gebruik eCPC-campagnes alleen in portfolio&#39;s wanneer de totale conversies die op het advertentienetwerk worden bijgehouden, overeenkomen met de portfoliodoelstelling.

* *[!UICONTROL Manual CPC]*: (Winkelcampagnes voor merken; [!DNL Microsoft Store Ads] campagnes; vervangen door [!DNL Microsoft® Advertising] in 2021 voor andere campagnetypen) Gebruikt het kosten-per-klikmodel (CPC). Voor sommige advertentietypen kunt u desgewenst het advertentienetwerk toestaan om biedingen voor de campagne te wijzigen:

   * **[!UICONTROL Enable Enhanced CPC]** (standaard uitgeschakeld): dit is hetzelfde als het gebruik van &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Manual CPA]:* ([!DNL Microsoft Store Ads] campagnes) gebruikt de kosten per aanschafmodel (CPA).

* *[!UICONTROL Manual CPM]* (De campagnes van het publiek en de campagnes van de publieksvideo slechts) gebruiken het kosten-per-duizend-impressies (CPM) model, waarvoor u specificeert wat u per 1.000 bekeken beelden wilt uitgeven. Campagnes met deze biedstrategie worden niet geoptimaliseerd wanneer ze in portfolio&#39;s worden opgenomen.

* *[!UICONTROL Maximize Clicks]:* (Zoeken en winkelen) Het advertentienetwerk — niet Zoeken, Sociaal en Commerce — optimaliseert biedingen om de klikmogelijkheden te maximaliseren. Voer desgewenst een **[!UICONTROL Max CPC]** (kosten per klik) om ervoor te zorgen dat het advertentienetwerk niet meer dan een specifiek bedrag voor elke klik betaalt. **Let op:** Wanneer u een campagne met deze strategie toevoegt aan een portfolio, worden de biedingen bepaald door het gewicht van de klik en niet door het doel van het portfolio.

* *[!UICONTROL Maximize Conversion Value]:* (Zoeken en winkelen/slim winkelen, maximale prestatiecampagnes) Het advertentienetwerk — niet Zoeken, Sociaal en Commerce — optimaliseert biedingen om de conversiewaarde te maximaliseren. Voer desgewenst een **[!UICONTROL Target Return on Ad Spend]** (ROAS) als een percentage. **Opmerking:** Gebruik deze optie voor campagnes in hybride portefeuilles maar niet standaardportefeuilles.

* *[!UICONTROL Maximize Conversions]:* (Prestatiecampagnes en campagnes op het onderzoeksnetwerk of publieksnetwerk (maar niet kijkvideo&#39;s of aangesloten TV) Het advertentienetwerk — niet Onderzoek, Sociale, &amp; Commerce — optimaliseert biedingen om omzettingen te maximaliseren. Voer desgewenst een **[!UICONTROL Target CPC]** (kosten per klik). Voor publiekscampagnes kunt u ook een optionele **[!UICONTROL Target CPA]** (kosten per overname). **Opmerking:** Gebruik deze optie voor campagnes in hybride portefeuilles maar niet standaardportefeuilles.

* *[!UICONTROL Target CPA]:* (Campagnes op het zoeknetwerk) Het advertentienetwerk — niet Zoeken, Sociaal, &amp; Commerce — optimaliseert biedingen op basis van een optionele **[!UICONTROL Target CPA]** (kosten per overname), dat is het gemiddelde bedrag van 30 dagen dat u voor een overname (omzetting) wilt betalen. **Opmerking:** Gebruik deze optie voor campagnes in hybride portefeuilles (maar niet standaardportefeuilles) met om het even welke uitgavenstrategie behalve [!UICONTROL Weekly] of [!UICONTROL Google Target CPA].

  Gemiddelde positie en CPC-biedgegevens zijn niet beschikbaar voor campagnes met deze biedstrategie.

* *[!UICONTROL Target Impression Share]:* (Campagnes op het onderzoeksnetwerk) Het advertentienetwerk — niet Onderzoek, Sociaal, &amp; Commerce — optimaliseert biedingen om een doelimitatieaandeel en een advertentiepunten te bereiken. Voer desgewenst een **[!UICONTROL Target Impression Share]** als percentage, de **[!UICONTROL Target Ad Position]** en **[!UICONTROL Max CPC]** (kosten per klik). **Opmerking:** Deze optie wordt niet ondersteund in hybride portfolio&#39;s.

* *[!UICONTROL Target Return on Ad Spend]:*  (Campagnes op de zoek- en winkelnetwerken) Het advertentienetwerk — niet Zoeken, Sociaal en Commerce — optimaliseert biedingen op basis van uw **[!UICONTROL Target ROAS]** (Retourneren bij advertentie-uitgaven), opgegeven als een percentage. Voer desgewenst een **[!UICONTROL Max CPC]** (kosten per klik) om ervoor te zorgen dat het advertentienetwerk niet meer dan een specifiek bedrag voor elke klik betaalt. **Opmerking:** Gebruik deze optie voor campagnes in hybride portefeuilles (maar niet standaardportefeuilles) met om het even welke uitgavenstrategie behalve [!UICONTROL Weekly] of [!UICONTROL Google Target ROAS].

  Gemiddelde positie en CPC-biedgegevens zijn niet beschikbaar voor campagnes met deze biedstrategie.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Alleen winkelcampagnes; alleen-lezen voor bestaande campagnes) Het land waar de producten van de campagne worden verkocht. Omdat de producten met doellanden worden geassocieerd, bepaalt dit het plaatsen welke producten in de campagne worden geadverteerd.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft® Merchant Center]:** (Alleen campagnes van het publiek; optioneel) Koppelt de campagne aan een specifieke winkel voor automatische advertenties op basis van feed in plaats van responsieve advertenties. Wanneer u deze optie selecteert, geeft u de opdracht [!UICONTROL Merchant ID] en [!UICONTROL Products]. U moet advertentiegroepen maken voor de campagne, maar u hoeft geen advertenties te maken.

Als u de campagne eenmaal aan een winkel hebt gekoppeld en de instellingen hebt opgeslagen, kunt u deze optie niet meer wijzigen.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Products]:** (Poortcampagnes die alleen zijn gekoppeld aan een winkelcentrum) De producten die moeten worden geadverteerd. Standaard, *[!UICONTROL All products]* is geselecteerd. Als u alleen producten met specifieke kenmerken wilt adverteren, selecteert u *[!UICONTROL Filter products]* en geef maximaal zeven combinaties van productafmetingen en kenmerken op waarop u uw producten wilt filteren. Voor advertenties die voor het product worden weergegeven, moeten alle opgegeven waarden van toepassing zijn. Als u bijvoorbeeld advertenties wilt weergeven voor de producten van Acme-huisdieren, kunt u de filters maken `Custom Label 1=animals`, `Category=pet supplies`, en `Brand=Acme Pet Supplies`.

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (Alleen prestatiecampagnes) De taal van de advertentie, die moet overeenkomen met de taal van de sites waarop de advertentie wordt weergegeven. [!DNL Microsoft Advertising] bepaalt de taal van een gebruiker van diverse signalen, met inbegrip van de vraag van de gebruiker, het land van de uitgever, en de taal die van de gebruiker plaatsen.

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

**[!UICONTROL Negative Websites]:** (Alleen campagnes op het scherm/native netwerk; optioneel) Sites op het weergavenetwerk waarop u uw advertenties niet wilt weergeven. Voer een geldige URL in, bijvoorbeeld www.example.com. Als u meerdere tekenreeksen wilt opgeven, scheidt u deze met komma&#39;s of voert u ze op afzonderlijke regels in.

Voor informatie over beschikbaarheid raadpleegt u de Help bij Microsoft® Advertising voor &quot;[Voorkomen dat advertenties op bepaalde websites worden weergegeven](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

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

## [!UICONTROL Asset Groups] (per elementgroep)

**[!UICONTROL Asset Group Name]:** De naam van de elementenmap (elementgroep).

**[!UICONTROL Asset Group Status]:** De status van de activagroep: *[!UICONTROL Active]* of *[!UICONTROL Paused]*.

**[!UICONTROL Final URL]:** De laatste URL voor alle advertenties die zijn gemaakt op basis van de elementgroep.

**[!UICONTROL Images]:** Maximaal 20 afbeeldingen voor de advertentie, inclusief ten minste één vierkante afbeelding en één liggende afbeelding. Zie de [[!DNL Microsoft Advertising] richtlijnen voor afbeeldingen](https://help.ads.microsoft.com/#apex/ads/en/60204/0). U kunt afbeeldingen uploaden of ze selecteren vanuit uw [!UICONTROL Asset Library] — maar niet beide in dezelfde handeling.

* Afbeeldingen uploaden:

   1. Op de [!UICONTROL Upload from Device] tabblad, klikt u op **[!UICONTROL +]** en selecteer afbeeldingen van uw apparaat of netwerk.

   1. Voor elke afbeelding:

      1. Selecteer de hoogte-breedteverhouding.

      1. Sleep het uitsnijdvak naar de gewenste plaats om het zichtbare gedeelte van de afbeelding te selecteren en wijzig zo nodig de grootte van het zichtbare gedeelte van de afbeelding.

      1. (Optioneel) Selecteer aanvullende hoogte-breedteverhoudingen en wijzig desgewenst de positie en de grootte van de afbeelding voor elke geselecteerde hoogte-breedteverhouding.

         Er wordt één element gemaakt voor elke geselecteerde hoogte-breedteverhouding.

      1. Klik op **[!UICONTROL Proceed]**.

   1. Wanneer u klaar bent met het opgeven van afbeeldingen, klikt u op **[!UICONTROL Upload]**.

* Als u afbeeldingen wilt selecteren in uw [!UICONTROL Asset Library], klikt u op **[!UICONTROL Asset Library]** en selecteert u de afbeeldingen.

**[!UICONTROL Logos]:** Ten minste één logo. U kunt maximaal vijf opnemen. Zie de [[!DNL Microsoft Advertising] richtlijnen voor elementen](https://help.ads.microsoft.com/#apex/ads/en/60204/0). U kunt afbeeldingen uploaden of ze selecteren vanuit uw [!UICONTROL Asset Library] — maar niet beide in dezelfde handeling.

* Afbeeldingen uploaden:

   1. Op de [!UICONTROL Upload from Device] tabblad, klikt u op **[!UICONTROL +]** en selecteer afbeeldingen van uw apparaat of netwerk.

   1. Voor elke afbeelding:

      1. Selecteer de hoogte-breedteverhouding.

      1. Sleep het uitsnijdvak naar de gewenste plaats om het zichtbare gedeelte van de afbeelding te selecteren en wijzig zo nodig de grootte van het zichtbare gedeelte van de afbeelding.

      1. (Optioneel) Selecteer aanvullende hoogte-breedteverhoudingen en wijzig desgewenst de positie en de grootte van de afbeelding voor elke geselecteerde hoogte-breedteverhouding.

         Er wordt één element gemaakt voor elke geselecteerde hoogte-breedteverhouding.

      1. Klik op **[!UICONTROL Proceed]**.

   1. Wanneer u klaar bent met het opgeven van afbeeldingen, klikt u op **[!UICONTROL Upload]**.

* Als u afbeeldingen wilt selecteren in uw [!UICONTROL Asset Library], klikt u op **[!UICONTROL Asset Library]** en selecteert u de afbeeldingen.

**[!UICONTROL Headlines]:** Minimaal drie en maximaal 15 korte kopregels met elk maximaal 30 tekens. U kunt tekst invoeren of elementen selecteren in uw [!UICONTROL Asset Library] — maar niet beide in dezelfde handeling.

* U voert als volgt tekst in:

   1. Op de [!UICONTROL Enter Text] voert u de tekst in.

   1. (Optioneel) Klik op **[!UICONTROL + Add]** en voer de tekenreeks in.

* Elementen selecteren uit uw [!UICONTROL Asset Library], klikt u op **[!UICONTROL Asset Library]** en selecteert u de elementen.

**[!UICONTROL Long Headlines]:** Minstens één, en tot vijf, lange kopregels met een maximum van 90 karakters elk. U kunt tekst invoeren of elementen selecteren in uw [!UICONTROL Asset Library] — maar niet beide in dezelfde handeling.

* U voert als volgt tekst in:

   1. Op de [!UICONTROL Enter Text] voert u de tekst in.

   1. (Optioneel) Klik op **[!UICONTROL + Add]** en voer de tekenreeks in.

* Elementen selecteren uit uw [!UICONTROL Asset Library], klikt u op **[!UICONTROL Asset Library]** en selecteert u de elementen.

**[!UICONTROL Descriptions]:** Minimaal twee en maximaal vijf beschrijvingen met elk maximaal 90 tekens. U kunt tekst invoeren of elementen selecteren in uw [!UICONTROL Asset Library] — maar niet beide in dezelfde handeling.

* U voert als volgt tekst in:

   1. Op de [!UICONTROL Enter Text] voert u de tekst in.

   1. (Optioneel) Klik op **[!UICONTROL + Add]** en voer de tekenreeks in.

* Elementen selecteren uit uw [!UICONTROL Asset Library], klikt u op **[!UICONTROL Asset Library]** en selecteert u de elementen.

**[!UICONTROL Call to Action]:** De oproep tot actie om op te nemen in de advertentie. Standaard, *[!UICONTROL Act Now]* is geselecteerd.

**[!UICONTROL Business Name]:** De firmanaam, met een maximum van 25 karakters. Het kan geen manuscripten, HTML, of andere prijsverhogingstaal bevatten.

**[!UICONTROL Audience Signal]:** (Optioneel) [!DNL Microsoft Advertising] publiek dat als publiekssignalen voor de campagne moet worden gebruikt. [!DNL Microsoft Advertising] In modellen voor machinaal leren wordt het publiek gebruikt om vergelijkbare surfers te zoeken die kunnen worden gebruikt en kunnen ook advertenties aan het publiek worden getoond die niet zijn opgegeven als signalen om u te helpen uw prestatiedoelen te bereiken. Kies het publiek dat het meest waarschijnlijk wordt omgezet.

>[!NOTE]
>De signalen van het publiek zijn verschillend van [doelgroepen op groepsniveau](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]:** Hiermee kunt u een andere elementgroep opgeven.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Of *[!UICONTROL Use account conversion goals for this campaign]* (de standaardwaarde) of *[!UICONTROL Use campaign specific conversion goals]*. Als u verkiest om omzettingsdoelstellingen voor de campagne te specificeren, dan selecteer de doelstellingen van de lijst van alle beschikbare doelstellingen. **Opmerking:** De doelstellingen worden gesynchroniseerd dagelijks, zodat kunnen de doelstellingen die in de vorige 24 uren worden gecreeerd niet worden vermeld. Om de lijst bij te werken, [de netwerkgegevens van de advertentie handmatig synchroniseren](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

Als de campagne deel uitmaakt van een portfolio, gebruikt u dezelfde conversiedoelstellingen als de doelstelling van de portfolio. Het gebruik van verschillende conversiedoelstellingen kan van invloed zijn op de prestaties van het portfolio.

>[!MORELIKETHIS]
>
>* [Campagnes beheren](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
