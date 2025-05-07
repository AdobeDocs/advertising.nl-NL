---
title: Accountinstellingen voor adverteerders
description: Zie beschrijvingen van de beschikbare adverteerderinstellingen.
role: User, Admin
source-git-commit: 1f8a76e060612cdcc8ee3709bdf49654faf31b57
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 0%

---

# Accountinstellingen voor adverteerders

*niet Beschikbaar aan Read-only Gebruikers*

<!-- Not published -->

## [!UICONTROL General] Instellingen

**[!UICONTROL Advertiser Name]:** De naam van de adverteerder.

**[!UICONTROL Category]:** De categorie waarin de zaken van de adverteerder werken. De rubriek wordt aan de uitgevers meegedeeld wanneer je op voorraad biedt. Kies een categorie die is uitgelijnd op uw advertenties of uitgevers kunnen uw advertenties afwijzen.

>[!NOTE]
>
>Als u *[!UICONTROL Other]* selecteert, heeft de adverteerder geen toegang tot DSP [!DNL On Demand Inventory] .

**[!UICONTROL Advertiser URL]:** De URL van de startpagina of hoofdwebsite van de adverteerder (die begint met `http://` of `https://` ).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (De Nieuwe rekeningen van adverteerders slechts) maakt alle privé uitwisselingsvoer voor de rekening van DSP van de organisatie van de organisatie aan de adverteerder beschikbaar wordt gevormd.

### [!UICONTROL Adobe IMS IDs]

Adverteerders met extra Adobe Experience Cloud-producten kunnen gegevens over bepaalde producten delen met behulp van de unieke id van de organisatie voor Experience Cloud. U kunt specifieke productintegratie configureren in de sectie [!UICONTROL Integrations] .

**[!UICONTROL Account IMS org and ID]:** (Adverteerders met extra Experience Cloud-producten die een licentie hebben via een Experience Cloud-account met meerdere adverteerders; optioneel) De Experience Cloud-organisatie-id van de adverteerder.

**[!UICONTROL Advertiser IMS org and ID]:** (Advertisers met directe licenties voor extra Experience Cloud-producten; optioneel) De Experience Cloud-organisatie-id van de adverteerder.

### [!UICONTROL Integrations]

(Optioneel) Aanvullende Experience Cloud-producten gekoppeld aan de DSP-account. De producten moeten worden gekoppeld aan dezelfde Experience Cloud-organisatie-id in de sectie [!UICONTROL Adobe IMS IDs] .

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]:** (Adverteerders met [!DNL Advertising Search, Social, & Commerce] of die Adobe Advertising-conversiepixels gebruiken) Een [!DNL Search, Social, & Commerce] -account waarmee DSP toewijzingsgegevens uitwisselt.

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]:** (Advertisers met Adobe Analytics; optioneel; alleen van toepassing op gegevens die zijn verzameld met trackingtags voor Adobe Advertising-conversie die alleen een [!DNL EF Redirect] en token bevatten) Een of meer [!DNL Analytics] rapportsuites waarnaar DSP gegevens verzendt die het verzamelt van uitgevers en partners aan de aanbodzijde. Analytics verzendt ook de gegevens die het van de cliëntplaats aan DSP verzamelt.

Voor de gegevens die in de rapportsuites worden weergegeven, moet de juiste instelling op het niveau van de [!DNL Search, Social, & Commerce] adverteerder zijn ingeschakeld. Daarnaast moet het [!DNL Analytics] -account van de adverteerder zijn geconfigureerd voor het ontvangen van gegevens van Adobe Advertising.

>[!WARNING]
>
>Als u een eerder gekoppelde rapportsuite verwijdert, wisselt DSP geen gegevens meer uit met die suite. Verwacht gegevensschommelingen te zien.

Voor meer informatie over de integratie met [!DNL Analytics], zie &quot;[ Overzicht van  [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).&quot;

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]:** (Advertisers met Adobe Audience Manager of Adobe Analytics; optioneel) Een Audience Manager- of [!DNL Analytics] -account waaruit DSP segmentmetagegevens, hiërarchiegegevens en unieke publieksgegevens opvraagt voor het gehele Adobe-publiek van de adverteerder. Dit omvat gegevens voor:

* Audience Manager-segmenten
* [!DNL Analytics] segmenten die naar Adobe Experience Cloud worden gepubliceerd
* Segmenten die zijn gemaakt met de Adobe Experience Cloud [!DNL Audience Library]
* Segmenten die in Adobe Experience Platform zijn gemaakt en via Audience Manager naar Adobe Advertising zijn verzonden

De eerste synchronisatie duurt ongeveer 24 uur. Daarna worden gegevens in real-time gesynchroniseerd met een vertraging van 1 tot 2 seconden.
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] Instellingen

U kunt naar keuze standaarddoelstellingen voor de nieuwe plaatsen van de adverteerder vormen. Gebruikers kunnen de standaarddoelen voor elke nieuwe plaatsing overschrijven.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** Het standaardland voor het geo-richten van elke plaatsing. De gebruikers kunnen het land veranderen, en specifieker geo-gericht vormen, voor elke plaatsing.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** Om het even welk publiek of segmenten om door gebrek te onderdrukken. Gebruikers kunnen de uitsluitingen voor elke plaatsing wijzigen.

### [!UICONTROL Media Quality]

<!-- See placement settings for specs on applicable ad/device types -->

#### [!UICONTROL Contextual Filtering]

Typen [!DNL Comscore]-, [!DNL DoubleVerify] -, [!DNL Integral Ad Science] - en [!DNL Peer39] contextuele filters die moeten worden toegepast. U kunt de adverteerder-vlakke montages op het [ plaatsingsniveau ](/help/dsp/campaign-management/placements/placement-settings.md) met voeten treden.

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (Facultatief) Één of meerdere soorten voorraadcontext om door gebrek te blokkeren. Er kunnen extra kosten van toepassing zijn.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (Optioneel) Een of meer typen voorraadkenmerken die standaard als doel moeten worden ingesteld. Er kunnen extra kosten van toepassing zijn.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (Optioneel) Een of meer typen voorraadkenmerken die standaard moeten worden geblokkeerd. Er kunnen extra kosten van toepassing zijn.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Optioneel) De mate van inhoud voor volwassenen waarvoor standaardadvertenties moeten worden geblokkeerd: *[!UICONTROL Do Not Block]* (de standaardinstelling), *[!UICONTROL Standard]* of *[!UICONTROL Strict]* . Er kunnen extra kosten van toepassing zijn.

**[!UICONTROL Alcohol Content]:** (Optioneel) De mate van het alcoholgehalte waarvoor advertenties standaard worden geblokkeerd: *[!UICONTROL Do Not Block]* (de standaardwaarde), *[!UICONTROL Standard]* of *[!UICONTROL Strict]* . Er kunnen extra kosten van toepassing zijn.

#### [!UICONTROL Pre-Bid Fraud Blocking] {#prebid-fraud-blocking}

Soorten sites die moeten worden geblokkeerd op basis van frauduleus verkeer en verdachte activiteiten die worden gemeten via [!DNL DoubleVerify] , [!DNL Integral Ad Science] en [!DNL Peer39] . U kunt de adverteerder-vlakke montages op het [ plaatsingsniveau ](/help/dsp/campaign-management/placements/placement-settings.md) met voeten treden.

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Door gebrek, blokkeert al 100% ongeldig verkeer, met inbegrip van verkeer op gekaapte apparaten, voor nieuwe plaatsingen. Er kunnen extra kosten van toepassing zijn.

**[!UICONTROL Also block sites with]:** (Optioneel) Een extra niveau van fraude en ongeldig verkeer waardoor DSP advertenties standaard blokkeert: *[!UICONTROL None]* (de standaardinstelling, die geen extra verkeer blokkeert), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* of *[!UICONTROL >25% Average Fraud/IVT levels]* . Er kunnen extra kosten van toepassing zijn.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (Optioneel) Een of meer soorten fraude waardoor DSP standaard advertenties blokkeert: *[!UICONTROL Fraud]* (die alle sites blokkeert met fraude), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* en/of *[!UICONTROL Fraud: Zero Ads]* . Er kunnen extra kosten van toepassing zijn.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (Optioneel) Een type verdachte website- of app-activiteit waardoor DSP advertenties standaard blokkeert: *[!UICONTROL None]* (de standaardinstelling, die advertenties niet blokkeert op basis van verdachte activiteiten), *[!UICONTROL Suspicious Activity - High Risk]* of *[!UICONTROL Suspicious Activity - High or Moderate Risk]* . Er kunnen extra kosten van toepassing zijn.

#### [!UICONTROL Pre-Bid Viewability]

Optionele weergavefilters vóór biedingen door [!DNL DoubleVerify] en [!DNL Integral Ad Science] om toe te passen op plaatsingen. De standaardinstellingen op adverteerderniveau worden geselecteerd voor nieuwe plaatsingen. U kunt de adverteerder-vlakke montages op het [ plaatsingsniveau ](/help/dsp/campaign-management/placements/placement-settings.md) met voeten treden.

##### [!UICONTROL DoubleVerify] {#doubleverify-viewability}

###### Video

**&#x200B; **&#x200B;[!UICONTROL Include URL's whose average video viewability rate is]** . Selecteer met deze optie de criteria.

**&#x200B; **&#x200B;[!UICONTROL Impressions with Insufficient IAB Viewability Data]**

**&#x200B; **&#x200B;[!UICONTROL Include URL's whose average completion & fully viewable rate is]** . Selecteer met deze optie de criteria.

**&#x200B; **&#x200B;[!UICONTROL Include URL's whose average player size composition is]** . Selecteer met deze optie de criteria.

**&#x200B; **&#x200B;[!UICONTROL Impressions with Insufficient Player Size Statistics]**

###### Weergave

**&#x200B; **&#x200B;[!UICONTROL Only target URL's or Apps that have historically achieved a display viewability rate of]** . Selecteer met deze optie de criteria.

* **[!UICONTROL Impressions with Insufficient IAB Viewability Performance Data]**

* **[!UICONTROL Include Apps and URL's whose average entire creative (100% of pixels) viewable duration is]**. Selecteer met deze optie de criteria.

* **[!UICONTROL Impressions with Insufficient BXD Performance Data]**

##### [!UICONTROL Integral Ad Science] {#ias-viewability}

Een optioneel **[!UICONTROL Video Viewability Targets]** filter en een optioneel **[!UICONTROL Display Viewability Targets]** filter. Er kunnen extra kosten van toepassing zijn.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** Door gebrek, welk niveau van [[!DNL Ads.txt]  pre-bieder filtreren ](https://iabtechlab.com/ads-txt-about/) aan gebruik door de lijst van elke uitgever [!DNL Authorized Digital Sellers] leveraging:
* *[!UICONTROL Opt out of ads.txt (default)]*: voorraad kopen van alle verkopers.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: prioriteit geven aan inkoopvoorraad van geautoriseerde directe verkopers en wederverkopers van een domein.
* *[!UICONTROL Ads.txt sellers only]*: voorraad alleen kopen bij geautoriseerde directe verkopers en wederverkopers van een domein.
* *[!UICONTROL Ads.txt sellers only]*: voorraad alleen kopen bij geautoriseerde directe verkopers van een domein.

U kunt adverteerder-niveau met voeten treden die op het [ plaatsingsniveau ](/help/dsp/campaign-management/placements/placement-settings.md) plaatsen.

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** Door gebrek, laat een filter in real time, post-bid toe om ervoor te zorgen dat de advertenties op de plaatsen dienen die de adverteerder richt. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Suitability]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] alleen klanten; optioneel) A [!DNL DoubleVerify Authentic Brand Safety] segment-id die is gekoppeld aan de account van de organisatie [!DNL DoubleVerify] en die standaard voor alle plaatsen moet worden gebruikt. Het specificeren van een identiteitskaart blokkeert impressies na-bieding gebruikend de veiligheidsregels van het douanemerk die voor gespecificeerde segment ID worden gevormd. DSP factureert uw account voor gebruik voor de segment-id.

De id moet beginnen met &quot;51&quot; en uit acht cijfers bestaan. U kunt de id op advertentieniveau op plaatsingsniveau wijzigen of verwijderen.

>[!MORELIKETHIS]
>
>* [ creeer een Rekening Advertiser ](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
