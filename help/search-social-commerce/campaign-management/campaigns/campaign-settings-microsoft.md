---
title: '[!DNL Microsoft Advertising] campagne-instellingen'
description: Verwijs de montages voor  [!DNL Microsoft Advertising]  campagnes.
exl-id: f11cb61e-d627-4074-870d-e186f3e65572
feature: Search Campaign Management
source-git-commit: c5739a7c3564f84c57500b54f17ca25591e09a43
workflow-type: tm+mt
source-wordcount: '2075'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] campagne-instellingen

## \[Scherm Campagne maken\]

**[!UICONTROL Campaign Type]:** (Alleen beschikbaar tijdens het maken van campagnes) Waar u advertenties wilt plaatsen en welke soorten advertenties wilt plaatsen
de campagne kan het volgende bevatten :

* *[!UICONTROL Search]:* toont tekstadvertenties op het onderzoeksnetwerk.

* *[!UICONTROL Shopping Network]:* toont productadvertenties — voor uw producten in uw [!DNL Microsoft Merchant Center] productcatalogus — op het winkelnetwerk.

* *[!UICONTROL Audience]:* toont native/weergaveadvertenties op de [!DNL Microsoft Audience Network] . U kunt a) automatisch op feed-based advertenties genereren door de campagne te koppelen aan een winkelcentrum in de [!UICONTROL Shopping Settings] -sectie of b) responsieve advertenties maken met tekstelementen en geüploade afbeeldingen. Voor beide opties moet u ad-hocgroepen maken waarvoor de gebruiker een doel instelt.

* *[!UICONTROL Shopping Campaigns for Brands]:* bevordert uw producten door verbonden detailhandelaren over het onderzoek en publieksnetwerken. U kunt onderliggende en productgroepen en productgroepen maken (apps die u wilt promoten) en optionele productadvertenties voor de campagne maken. [!DNL Microsoft Advertising] maakt automatisch advertenties voor de productgroepen. Gebruik de biedstrategie [!UICONTROL Manual CPC] voor boodschappencampagnes voor merken. Gebruik de biedstrategie [!UICONTROL Cost per Sale] voor het winkelen van promoties voor merken.

* *[!UICONTROL Microsoft Store Ads Campaign]:* Promoot uw apps en games die beschikbaar zijn in de [!DNL Microsoft Store] . U kunt onderliggende en optionele productgroepen, productgroepen en advertenties voor de campagne maken. [!DNL Microsoft Advertising] maakt automatisch advertenties voor de productgroepen.

* *[!UICONTROL Audience CTV Video]:* toont aangesloten TV (CTV) videoadvertenties op het publieksnetwerk.

* *[!UICONTROL Audience Video]:* toont standaardvideoadvertenties op het publieksnetwerk.

* *[!UICONTROL Performance Max]:* toont veelvoudige advertentietypes over alle netwerken gebruikend [!DNL Microsoft Advertising] slimme het bieden. Binnen de instellingen voor de campagne moet u een of meer elementgroepen opgeven, zoals afbeeldingen, logo&#39;s, koppen, beschrijvingen, een optionele call to action en publiekssignalen. Het advertentienetwerk combineert automatisch de activa om advertenties te dienen die op het kanaal worden gebaseerd.

## [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Een campagnenaam die binnen de rekening uniek is. De maximumlengte is 128 tekens.

**[!UICONTROL Status]:** De vertoningsstatus van de campagne: *Actieve* of *Gepauzeerde*. Het gebrek voor nieuwe advertentiecampagnes is *Actief*.

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Contains EU Political Ads]:** (Van toepassing op campagnes die gericht zijn op het publiek in de Europese Unie (EU)) Of de campagne al dan niet politieke reclame bevat per vereisten voor advertenties die in de Europese Unie worden bediend krachtens EU-verordening 2024/90: *[!UICONTROL Yes]* of *[!UICONTROL No]* .

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

**[!UICONTROL Bid strategy]:** De biedstrategie voor de campagne:

* *[!UICONTROL Cost per Sale]:* (Alleen winkelcampagnes) Het advertentienetwerk — niet Zoeken, Sociaal en Commerce — optimaliseert biedingen op basis van [!UICONTROL Target CPS] (kosten per verkoop). Je betaalt alleen wanneer je op je product klikt en de transactie binnen 24 uur plaatsvindt. **Nota:** neem geen campagnes met deze biedingsstrategie in portefeuilles op. Optimalisatie voor zoeken, sociale media en Commerce is niet beschikbaar voor campagnes met deze biedstrategie.

  Als je eenmaal een winkelcampagne voor merken hebt opgeslagen met deze biedstrategie, kun je de biedstrategie niet meer wijzigen. Voor andere soorten winkelcampagnes is deze strategie alleen beschikbaar voor nieuwe campagnes.

* *[!UICONTROL CPV]* (Alleen bij CTV-campagnes voor doelgroep) Gebruikt het model voor de kosten per weergave (CPV). Zoeken, Sociaal en Commerce biedt geen optimalisatie voor campagnes met deze biedstrategie die in portfolio&#39;s zijn opgenomen.

* *[!UICONTROL Enhanced CPC]:* (Campagnes op het publiek, onderzoek, en het winkelen netwerken) gebruikt het verbeterde kosten-per-klikmodel van het advertentienetwerk (eCPC), dat het advertentienetwerk toestaat om de kosten-per-klikbieding (CPC) voor elke veiling automatisch te veranderen in een poging om omzettingen te maximaliseren, gebruikend omzettingen binnen het advertentienetwerk (niet in Onderzoek, Sociale, &amp; Commerce), terwijl het proberen te houden) PC onder uw maximum CPC.

  Wanneer u een campagne met eCPC aan een geoptimaliseerde portefeuille van het Onderzoek toevoegt, sociale, &amp; Commerce, optimaliseert het Onderzoek, Sociale, &amp; Commerce de basisbiedingen en - wanneer &quot;[!UICONTROL Auto adjust campaign budget limits]&quot;optie wordt toegelaten - het campagnebudget. Het advertentienetwerk optimaliseert alle biedingsaanpassingen en kan de door Zoeken, Sociale en Commerce gegenereerde biedingen wijzigen op het moment van de gebruikersquery op basis van eigen gegevens en inzichten. **Voorzichtigheid:** Gebruik eCPC campagnes in portefeuilles slechts wanneer de totale omzettingen die op het advertentienetwerk worden gevolgd zich op het portefeuilledoel richten.

* *[!UICONTROL Manual CPC]*: (Winkelcampagnes voor merken; [!DNL Microsoft Store Ads] campagnes; afgekeurd voor andere soorten campagnes) gebruikt het CPC-model (cost-per-click). Voor sommige advertentietypen kunt u desgewenst het advertentienetwerk toestaan om biedingen voor de campagne te wijzigen:

   * **[!UICONTROL Enable Enhanced CPC]** (standaard uitgeschakeld): deze optie komt overeen met het gebruik van de optie &quot;[!UICONTROL Enhanced CPC]&quot;.

* *[!UICONTROL Manual CPA]:* ([!DNL Microsoft Store Ads] campagnes) gebruikt de kosten per aanschafmodel (CPA).

* *[!UICONTROL Manual CPM]* (Publiek campagnes en publieksvideocampagnes slechts) gebruikt het kosten-per-duizend-impressiemodel (CPM), waarvoor u specificeert wat u per 1.000 bekeken beelden wilt uitgeven. Campagnes met deze biedstrategie worden niet geoptimaliseerd wanneer ze in portfolio&#39;s worden opgenomen.

* *[!UICONTROL Maximize Clicks]:* (Zoeken en winkelen) Het advertentienetwerk — niet Zoeken, Sociaal, &amp; Commerce — optimaliseert biedingen om kliks te maximaliseren. Voer desgewenst een **[!UICONTROL Max CPC]** (kosten per klik) in om ervoor te zorgen dat het advertentienetwerk niet meer betaalt dan een bepaald bedrag voor elke klik. **Voorzichtigheid:** wanneer u een campagne met deze strategie aan een portefeuille toevoegt, drijft het klikgewicht (niet het portefeuilledoel) biedingen.

* *[!UICONTROL Maximize Conversion Value]:* (Zoeken en winkelen/Smart shopping-netwerken, maximale prestatiecampagnes) Het advertentienetwerk — niet Zoeken, Sociaal en Commerce — optimaliseert biedingen om de conversiewaarde te maximaliseren. Voer desgewenst een **[!UICONTROL Target Return on Ad Spend]** (ROAS) in als een percentage. **Nota:** gebruik deze optie voor campagnes in hybride portefeuilles maar niet standaardportefeuilles. In hybride portefeuilles, optimaliseert het Onderzoek, Sociale, &amp; Commerce het Doel ROAS.

* *[!UICONTROL Maximize Conversions]:* (De maximumcampagnes en de campagnes van Prestaties op het onderzoeksnetwerk of publieksnetwerk (maar niet kijkvideo&#39;s of aangesloten TV) het ad netwerk — niet Onderzoek, Sociale, &amp; Commerce — optimaliseert biedingen om omzettingen te maximaliseren. Voer desgewenst een **[!UICONTROL Target CPC]** (kosten per klik) in. Voor publiekscampagnes kunt u ook een optionele **[!UICONTROL Target CPA]** (kosten per aankoop) invoeren. **Nota:** gebruik deze optie voor campagnes in hybride portefeuilles maar niet standaardportefeuilles. In hybride portefeuilles, optimaliseert het Onderzoek, Sociale, &amp; Commerce Doel CPA.

* *[!UICONTROL Target CPA]:* (Campagnes op het onderzoeksnetwerk) het advertentienetwerk — niet Onderzoek, Sociale, &amp; Commerce — optimaliseert biedingen die op facultatieve **[!UICONTROL Target CPA]** (kosten per verwerving) worden gebaseerd, die het gemiddelde bedrag 30 dagen is u voor een verwerving (omzetting) wilt betalen. **Nota:** gebruik deze optie voor campagnes in hybride portefeuilles (maar niet standaardportefeuilles) met om het even welke uitgavenstrategie behalve [!UICONTROL Weekly] of [!UICONTROL Google Target CPA]. In hybride portefeuilles, optimaliseert het Onderzoek, Sociale, &amp; Commerce Doel CPA.

  Gemiddelde positie en CPC-biedgegevens zijn niet beschikbaar voor campagnes met deze biedstrategie.

* *[!UICONTROL Target Impression Share]:* (Campagnes op het onderzoeksnetwerk) het advertentienetwerk — niet Onderzoek, Sociale, &amp; Commerce — optimaliseert biedingen om een doelimitatieaandeel en een advertentiepositie te bereiken. Voer desgewenst een **[!UICONTROL Target Impression Share]** in als een percentage, de **[!UICONTROL Target Ad Position]** en een **[!UICONTROL Max CPC]** (kosten per klik). **Nota:** deze optie wordt niet gesteund in hybride portefeuilles.

* *[!UICONTROL Target Return on Ad Spend]:* (Campagnes op de zoek en het winkelen netwerken) Het advertentienetwerk — niet Zoeken, Sociaal, &amp; Commerce — optimaliseert biedingen op basis van uw **[!UICONTROL Target ROAS]** (rendement op advertentie-uitgaven), opgegeven als een percentage. Voer desgewenst een **[!UICONTROL Max CPC]** (kosten per klik) in om ervoor te zorgen dat het advertentienetwerk niet meer betaalt dan een bepaald bedrag voor elke klik. **Nota:** gebruik deze optie voor campagnes in hybride portefeuilles (maar niet standaardportefeuilles) met om het even welke uitgavenstrategie behalve [!UICONTROL Weekly] of [!UICONTROL Google Target ROAS]. In hybride portefeuilles, optimaliseert het Onderzoek, Sociale, &amp; Commerce het Doel ROAS.

  Gemiddelde positie en CPC-biedgegevens zijn niet beschikbaar voor campagnes met deze biedstrategie.

## [!UICONTROL Shopping Settings]

**[!UICONTROL Sales Country]:** (Alleen winkelcampagnes; alleen-lezen voor bestaande campagnes) Het land waarin
de producten van de campagne worden verkocht . Omdat de producten met doellanden worden geassocieerd, bepaalt dit het plaatsen welke producten in de campagne worden geadverteerd.

<!-- **[!UICONTROL Campaign Priority]:** -->

**[!UICONTROL Link with Microsoft Merchant Center]:** (Poortcampagnes slechts; facultatief) Verbindt de campagne met een specifieke handelscentrum opslag voor geautomatiseerde op diervoeder-gebaseerde advertenties eerder dan ontvankelijke advertenties. Wanneer u deze optie selecteert, geeft u de waarden [!UICONTROL Merchant ID] en [!UICONTROL Products] op. U moet advertentiegroepen maken voor de campagne, maar u hoeft geen advertenties te maken.

Als u de campagne eenmaal aan een winkel hebt gekoppeld en de instellingen hebt opgeslagen, kunt u deze optie niet meer wijzigen.

{{$include /help/_includes/campaign-priority.md}}

<!-- **[!UICONTROL Merchant ID]:** -->

{{$include /help/_includes/merchant-id.md}}

**[!UICONTROL Products]:** (Poortcampagnes die alleen zijn gekoppeld aan een winkel in een winkelcentrum) De producten die moeten worden geadverteerd. Standaard is *[!UICONTROL All products]* geselecteerd. Als u alleen producten met specifieke kenmerken wilt adverteren, selecteert u *[!UICONTROL Filter products]* en geeft u maximaal zeven combinaties van productdimensies en kenmerken op waarop u uw producten wilt filteren. Voor advertenties die voor het product worden weergegeven, moeten alle opgegeven waarden van toepassing zijn. Als u bijvoorbeeld advertenties wilt weergeven voor de producten van de huisdieren Acme, maakt u de filters `Custom Label 1=animals` , `Category=pet supplies` en `Brand=Acme Pet Supplies` .

<!-- **[!UICONTROL Inventory Filter]:** -->

{{$include /help/_includes/inventory-filter.md}}

## [!UICONTROL Campaign Targeting]

**[!UICONTROL Languages]:** (De maximum campagnes van Prestaties slechts) de taal van de advertentie, die de taal van de plaatsen zou moeten aanpassen waarop uw advertentie kan verschijnen. [!DNL Microsoft Advertising] bepaalt de taal van een gebruiker van diverse signalen, met inbegrip van de vraag van de gebruiker, het land van de uitgever, en de taalmontages van de gebruiker.

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

**[!UICONTROL Negative Websites]:** (Campagnes op de vertoning/het inheemse netwerk slechts; facultatief) Plaatsen op het vertoningsnetwerk waarop u uw advertenties niet wilt worden getoond. Voer een geldige URL in, bijvoorbeeld www.example.com. Als u meerdere tekenreeksen wilt opgeven, scheidt u deze met komma&#39;s of voert u ze op afzonderlijke regels in.

Voor informatie over beschikbaarheid, zie de hulp van Microsoft Advertising &quot;[&#x200B; verhinderen advertenties op specifieke websites &#x200B;](https://help.ads.microsoft.com/#apex/bae/en/14061/0) verschijnen.&quot;

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

**[!UICONTROL Track Product Group]:** (alleen voor [!UICONTROL EF Redirect] ) Niet geïmplementeerd

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

## [!UICONTROL Asset Groups] (per elementgroep)

**[!UICONTROL Asset Group Name]:** De naam van de elementenmap (elementgroep).

**[!UICONTROL Asset Group Status]:** De status van de elementgroep: *[!UICONTROL Active]* of *[!UICONTROL Paused]* .

**[!UICONTROL Final URL]:** De laatste URL voor alle advertenties die zijn gemaakt op basis van de elementgroep.

**[!UICONTROL Images]:** Maximaal 20 afbeeldingen voor de advertentie, inclusief ten minste één vierkante afbeelding en één liggende afbeelding. Zie de [[!DNL Microsoft Advertising]  beeldrichtlijnen &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/60204/0). U kunt afbeeldingen uploaden of ze selecteren vanuit uw [!UICONTROL Asset Library] , maar niet in beide bewerkingen.

* Afbeeldingen uploaden:

   1. Klik op het tabblad [!UICONTROL Upload from Device] op **[!UICONTROL +]** en selecteer afbeeldingen van uw apparaat of netwerk.

   1. Voor elke afbeelding:

      1. Selecteer de hoogte-breedteverhouding.

      1. Sleep het uitsnijdvak naar de gewenste plaats om het zichtbare gedeelte van de afbeelding te selecteren en wijzig zo nodig de grootte van het zichtbare gedeelte van de afbeelding.

      1. (Optioneel) Selecteer aanvullende hoogte-breedteverhoudingen en wijzig desgewenst de positie en de grootte van de afbeelding voor elke geselecteerde hoogte-breedteverhouding.

         Er wordt één element gemaakt voor elke geselecteerde hoogte-breedteverhouding.

      1. Klik op **[!UICONTROL Proceed]**.

   1. Wanneer u klaar bent met het opgeven van afbeeldingen, klikt u op **[!UICONTROL Upload]** .

* Als u afbeeldingen in uw [!UICONTROL Asset Library] wilt selecteren, klikt u op **[!UICONTROL Asset Library]** en selecteert u de afbeeldingen.

**[!UICONTROL Logos]:** minstens één embleem. U kunt maximaal vijf opnemen. Zie de [[!DNL Microsoft Advertising]  activarichtlijnen &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/60204/0). U kunt afbeeldingen uploaden of ze selecteren vanuit uw [!UICONTROL Asset Library] , maar niet in beide bewerkingen.

* Afbeeldingen uploaden:

   1. Klik op het tabblad [!UICONTROL Upload from Device] op **[!UICONTROL +]** en selecteer afbeeldingen van uw apparaat of netwerk.

   1. Voor elke afbeelding:

      1. Selecteer de hoogte-breedteverhouding.

      1. Sleep het uitsnijdvak naar de gewenste plaats om het zichtbare gedeelte van de afbeelding te selecteren en wijzig zo nodig de grootte van het zichtbare gedeelte van de afbeelding.

      1. (Optioneel) Selecteer aanvullende hoogte-breedteverhoudingen en wijzig desgewenst de positie en de grootte van de afbeelding voor elke geselecteerde hoogte-breedteverhouding.

         Er wordt één element gemaakt voor elke geselecteerde hoogte-breedteverhouding.

      1. Klik op **[!UICONTROL Proceed]**.

   1. Wanneer u klaar bent met het opgeven van afbeeldingen, klikt u op **[!UICONTROL Upload]** .

* Als u afbeeldingen in uw [!UICONTROL Asset Library] wilt selecteren, klikt u op **[!UICONTROL Asset Library]** en selecteert u de afbeeldingen.

**[!UICONTROL Headlines]:** minimaal drie en maximaal 15 korte kopregels met elk maximaal 30 tekens. U kunt tekst invoeren of elementen selecteren in uw [!UICONTROL Asset Library], maar niet in beide bewerkingen.

* U voert als volgt tekst in:

   1. Voer op het tabblad [!UICONTROL Enter Text] de tekst in.

   1. (Optioneel) Als u nog een tekenreeks wilt toevoegen, klikt u op **[!UICONTROL + Add]** en voert u de tekenreeks in.

* Als u elementen wilt selecteren in uw [!UICONTROL Asset Library] , klikt u op **[!UICONTROL Asset Library]** en selecteert u de elementen.

**[!UICONTROL Long Headlines]:** minstens één, en tot vijf, lange kopregels met een maximum van 90 karakters elk. U kunt tekst invoeren of elementen selecteren in uw [!UICONTROL Asset Library], maar niet in beide bewerkingen.

* U voert als volgt tekst in:

   1. Voer op het tabblad [!UICONTROL Enter Text] de tekst in.

   1. (Optioneel) Als u nog een tekenreeks wilt toevoegen, klikt u op **[!UICONTROL + Add]** en voert u de tekenreeks in.

* Als u elementen wilt selecteren in uw [!UICONTROL Asset Library] , klikt u op **[!UICONTROL Asset Library]** en selecteert u de elementen.

**[!UICONTROL Descriptions]:** minstens twee, en tot vijf, beschrijvingen met een maximum van 90 karakters elk. U kunt tekst invoeren of elementen selecteren in uw [!UICONTROL Asset Library], maar niet in beide bewerkingen.

* U voert als volgt tekst in:

   1. Voer op het tabblad [!UICONTROL Enter Text] de tekst in.

   1. (Optioneel) Als u nog een tekenreeks wilt toevoegen, klikt u op **[!UICONTROL + Add]** en voert u de tekenreeks in.

* Als u elementen wilt selecteren in uw [!UICONTROL Asset Library] , klikt u op **[!UICONTROL Asset Library]** en selecteert u de elementen.

**[!UICONTROL Call to Action]:** De call to action die in de advertentie moet worden opgenomen. Standaard is *[!UICONTROL Act Now]* geselecteerd.

**[!UICONTROL Business Name]:** De bedrijfsnaam, met een maximum van 25 karakters. Het kan geen manuscripten, HTML, of andere prijsverhogingstaal bevatten.

**[!UICONTROL Audience Signal]:** (Optioneel) [!DNL Microsoft Advertising] publiek dat als publiekssignalen voor de campagne moet worden gebruikt. [!DNL Microsoft Advertising] computerleermodellen gebruiken het publiek om vergelijkbare websurfers te vinden die u als doel wilt gebruiken en kunnen ook advertenties aan het publiek tonen die niet als signalen worden opgegeven om u te helpen uw prestatiedoelen te bereiken. Kies het publiek dat het meest waarschijnlijk wordt omgezet.

>[!NOTE]
>De signalen van het publiek zijn verschillend van [&#x200B; en groep-vlakke publieksdoelstellingen &#x200B;](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md).

<!-- **[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** -->

{{$include /help/_includes/display-path1-2.md}}

**[!UICONTROL Add new asset group]:** Hiermee kunt u een andere elementgroep opgeven.

## [!UICONTROL Conversion Goals]

**[!UICONTROL Conversion Goal]:** Of *[!UICONTROL Use account conversion goals for this campaign]* (de standaardwaarde) of *[!UICONTROL Use campaign specific conversion goals]*. Als u verkiest om omzettingsdoelstellingen voor de campagne te specificeren, dan selecteer de doelstellingen van de lijst van alle beschikbare doelstellingen. **Nota:** de Doelstellingen worden gesynchroniseerd dagelijks, zodat kunnen de doelstellingen die in de vorige 24 uren worden gecreeerd niet worden vermeld. Om de lijst bij te werken, [&#x200B; synchroniseert manueel de gegevens van het advertentienetwerk &#x200B;](/help/search-social-commerce/campaign-management/campaigns/sync-network.md).

>[!TIP]
>
>Als de campagne deel uitmaakt van een hybride portfolio, kunt u het beste campagnedoelen gebruiken die overeenkomen met de conversiedoelstellingen in de doelstelling van de portfolio. Het opnemen van aanvullende conversiedoelstellingen kan van invloed zijn op de prestaties van het portfolio.
>
> Nochtans, voor campagnes in hybride portefeuilles waarvoor u [&#x200B; doelstellingen aan het advertentienetwerk &#x200B;](/help/search-social-commerce/tools/objective-upload-to-networks.md) uploadt, doe het volgende binnen de redacteur van het advertentienetwerk in plaats van hier: a) voeg het geuploade Onderzoek toe, Sociale, &amp; de portefeuilledoelstelling van Commerce (die met &quot;O_ACS_OBJ&quot;begint) als omzettingsdoel voor de campagne, en b) voeg om het even welke campagnedoelstellingen toe die omzettingen omvatten die door de [!DNL Microsoft Advertising] universele gebeurtenis het volgen (markering van UET worden gevolgd) omdat de ad netwerk-geleide metriek niet aan het ad netwerk met het doel worden geupload.

>[!MORELIKETHIS]
>
>* [&#x200B; beheert campagnes &#x200B;](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
