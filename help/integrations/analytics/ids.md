---
title: Adobe Advertising-id's gebruikt door  [!DNL Analytics]
description: Adobe Advertising-id's gebruikt door  [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: dbbba0bd75f3b1003325b665d06bce003c5ee054
workflow-type: tm+mt
source-wordcount: '1761'
ht-degree: 0%

---

# Adobe Advertising-id&#39;s gebruikt door [!DNL Analytics]

*Advertisers met slechts een integratie Adobe Advertising-Adobe Analytics*

*Van toepassing op Advertising DSP en[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising gebruikt twee IDs voor prestaties het volgen ter plaatse: *EF identiteitskaart* en *identiteitskaart van AMO*.

Wanneer een advertentie-impositie optreedt, maakt Adobe Advertising de waarden voor de AMO-id en EF-id en slaat het deze op. Wanneer een bezoeker die een advertentie heeft gezien de site betreedt zonder op een advertentie te klikken, roept [!DNL Analytics] deze waarden aan vanuit Adobe Advertising via de [!DNL Analytics for Advertising] JavaScript-code. Voor doorkijkverkeer genereert [!DNL Analytics] een aanvullende id (`SDID` ) die wordt gebruikt om de EF-id en AMO-id aan te sluiten in [!DNL Analytics] . Voor doorklikverkeer worden deze id&#39;s opgenomen in de URL van de bestemmingspagina met behulp van de parameters `ef_id` en `s_kwcid` (voor de AMO ID) van de queryreeks.

Adobe Advertising maakt een onderscheid tussen een doorklikitem of een doorkijkitem op de website aan de hand van de volgende criteria:

* Een view-through ingang wordt gevangen wanneer een gebruiker de plaats na het bekijken van een advertentie bezoekt maar niet het klikt. [!DNL Analytics] registreert een mening-door als twee voorwaarden worden voldaan:

   * De bezoeker heeft geen klik-door voor a [!DNL DSP] of [!DNL Search, Social, & Commerce] en tijdens [ klikt raadplegingsvenster ](/help/integrations/analytics/prerequisites.md#lookback-a4adc).

   * De bezoeker heeft minstens één [!DNL DSP] en tijdens het [ venster van de imkerraadpleging ](/help/integrations/analytics/prerequisites.md#lookback-a4adc) gezien. De laatste indruk wordt doorgegeven als de doorkijkhoek.

* Een doorklikitem wordt vastgelegd wanneer een sitebezoeker op een advertentie klikt voordat hij de site betreedt. [!DNL Analytics] legt een doorklikken vast wanneer een van de volgende omstandigheden zich voordoet:

   * De URL bevat een EF-id en een AMO-id die Adobe Advertising aan de URL van de bestemmingspagina heeft toegevoegd.

   * De URL bevat geen volgcodes, maar de Adobe Advertising JavaScript-code detecteert een klik binnen de laatste twee minuten.

![ op mening-gebaseerde Adobe Advertising [!DNL Analytics] integratie ](/help/integrations/assets/a4adc-view-through-process.png)

*Figuur 1: Op mening-gebaseerde Adobe Advertising [!DNL Analytics] integratie*

![ Adobe Advertising klikt op URL-Gebaseerde [!DNL Analytics] integratie ](/help/integrations/assets/a4adc-click-through-process.png)

*Figuur 2: Adobe Advertising klikt op URL-Gebaseerde [!DNL Analytics] integratie*

## Adobe Advertising EF-id&#39;s

De EF-id is een unieke token die Adobe Advertising gebruikt om activiteit te koppelen aan een online klik of advertentie. EF identiteitskaart wordt opgeslagen in [ een  [!DNL Analytics] [!DNL eVar] ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) of [!DNL rVar] (gereserveerde [!DNL eVar]) afmeting (Adobe Advertising EF identiteitskaart) en volgt elke en klik of blootstelling op individuele browser of apparatenniveau. EF-id&#39;s fungeren voornamelijk als sleutels voor het verzenden van [!DNL Analytics] -gegevens naar Adobe Advertising voor rapportage en optimalisatie van biedingen in Adobe Advertising.

### EF-id-indeling

>[!NOTE]
>
>EF-id&#39;s zijn hoofdlettergevoelig. Als een [!DNL Analytics] -implementatie het bijhouden van URL&#39;s in kleine letters dwingt, herkent Adobe Advertising de EF-id niet. Dit is van invloed op Adobe Advertising-biedingen en -rapporten, maar heeft geen invloed op Adobe Advertising-rapportage binnen [!DNL Analytics] .

#### [!DNL Google Ads] zoekopdrachten

```
{gclid}:G:s
```

waarbij:

* `gclid` is de [!DNL Google Click ID] (GCLID).
* `s` is het netwerktype (&quot;s&quot; voor onderzoek).

#### [!DNL Microsoft Advertising] zoekopdrachten

```
{msclkid}:G:s
```

waarbij:

* `msclkid` is de [!DNL Microsoft Click ID] (MSCLKID).
* `s` is het netwerktype (&quot;s&quot; voor onderzoek).

#### Advertenties en zoekadvertenties weergeven op andere zoekmachines

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

waarbij:

* &lt;*identiteitskaart van de bezoeker van Adobe Advertising*> is een unieke identiteitskaart per bezoeker (zoals UWKVaAABCkJ0mDt). Ook geroepen *surfer identiteitskaart*.

* &lt;*timestamp*> is de tijd in formaat YYYMMDDHHMMSS (zoals 20190821192533 voor Jaar 2019, Maand 08, Dag 21, Tijd 19 :25: 33).

* &lt;*kanaaltype*> is het kanaaltype verantwoordelijk voor de klik of de blootstelling:

   * `d` voor een klik op een DSP-advertentie (klik-via tonen)
   * `i` voor een indruk van een DSP-advertentie (display view-through)
   * `s` voor een klik op een zoekadvertentie (doorzoekklik).

Voorbeeld `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### De EF-id Dimension in [!DNL Analytics]

In [!DNL Analytics] -rapporten kunt u EF-id-gegevens vinden door te zoeken naar de [!UICONTROL EF ID] -dimensie en de [!UICONTROL EF ID Instance] -metrische waarde te gebruiken.

Voor EF-id&#39;s geldt de limiet van 500 kB voor unieke identificatiekenmerken in Analysis Workspace. Zodra de waarde 500k wordt bereikt, worden alle nieuwe volgcodes gemeld onder de één-lijn-punt titel &quot;[!UICONTROL Low Traffic]&quot;. Vanwege de mogelijkheid dat rapportprecisie ontbreekt, worden de EF-id&#39;s niet geclassificeerd en mag u deze niet gebruiken voor segmenten of voor rapportage in [!DNL Analytics] .

## Adobe Advertising AMO-id&#39;s {#amo-id}

De AMO-id houdt elke unieke advertentiecombinatie bij op een minder korrelig niveau en wordt gebruikt voor [!DNL Analytics] gegevensclassificatie en opname van advertentiemetriek (zoals indrukken, klikken en kosten) van Adobe Advertising. Identiteitskaart van AMO wordt opgeslagen in [!DNL Analytics] [ eVar ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) of rVar afmeting (identiteitskaart van AMO) en wordt uitsluitend gebruikt voor het melden in [!DNL Analytics].

De AMO-id wordt ook wel de `s_kwcid` genoemd, die soms wordt uitgesproken als &quot;[!DNL squid]&quot;.

### Manieren om de AMO-id te implementeren {#amo-id-implement}

De parameter wordt op een van de volgende manieren toegevoegd aan de URL&#39;s die worden gevolgd:

* (Aanbevolen) Wanneer de invoegfunctie op de server is geïmplementeerd.

   * DSP-klanten: de pixelserver voegt automatisch de parameter s_kwcid toe aan de achtervoegsels van de bestemmingspagina wanneer een eindgebruiker een weergaveadvertentie met de Adobe Advertising-pixel weergeeft.

   * Zoek-, sociale en Commerce-klanten:

      * Voor [!DNL Google Ads] - en [!DNL Microsoft Advertising] -accounts waarvoor de [!UICONTROL Auto Upload] -instelling is ingeschakeld voor de account of campagne, voegt de pixelserver automatisch de parameter s_kwcid toe aan de achtervoegsels van de bestemmingspagina wanneer een eindgebruiker op een advertentie met de Adobe Advertising-pixel klikt.

      * Voor andere advertentienetwerken, of [!DNL Google Ads] en [!DNL Microsoft Advertising] rekeningen met [!UICONTROL Auto Upload] gehandicapten plaatsen, voeg manueel de parameter aan uw [ rekening-niveau parameters ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} toe, die het aan uw basis URLs toevoegen.

* Wanneer de invoegfunctie op de server niet is geïmplementeerd:

   * De klanten van DSP: De [ code van JavaScript ](javascript.md) registreert automatisch klik-door:gaan en mening-door. Wanneer een browser geen cookies van derden ondersteunt, kunt u nog steeds op klikken gebaseerde conversies bijhouden voor de volgende soorten advertenties:

      * Voor [!DNL Flashtalking] ad markeringen, neem manueel extra macro&#39;s per &quot;[ op voeg  [!DNL Analytics for Advertising]  Macro&#39;s aan  [!DNL Flashtalking]  toe - Markeringen ](/help/integrations/analytics/macros-flashtalking.md).&quot; **Nota:** Deze procedure is niet noodzakelijk als uw organisatie een direct partnerschap met [!DNL Flashtalking] heeft en u gegevens-pas macro&#39;s gebruikt om de `s_kwcid` en `ef_id` volgende parameters per de [!DNL Flashtalking] steundocumentatie bij [ https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros ](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros) te volgen.

      * Voor [!DNL Google Campaign Manager 360] ad markeringen, neem manueel extra macro&#39;s per &quot;[ op voeg  [!DNL Analytics for Advertising]  Macro&#39;s aan  [!DNL Google Campaign Manager 360]  toe - Markeringen ](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

   * Zoek-, sociale en Commerce-klanten:

      * Voor ([!DNL Google Ads] en [!DNL Microsoft Advertising]) advertenties, voeg manueel de parameter van identiteitskaart van AMO aan uw het landen paginaapara&#39;s toe, idealiter bij het [ rekeningsniveau ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} tenzij het verschillend volgen voor individuele rekeningscomponenten noodzakelijk is.

      * Voor advertenties op alle andere advertentienetwerken, voeg manueel de parameter van identiteitskaart AMO aan uw [ rekening-niveau parameters ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} toe, die het aan uw basis URLs toevoegen.

Neem contact op met uw Adobe-accountteam als u de invoegfunctie aan de serverzijde wilt implementeren of de beste optie voor uw bedrijf wilt bepalen.

### AMO-id-indelingen {#amo-id-formats}

#### AMO ID Format voor [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

waarbij:

* `AC` geeft het weergavekanaal aan.

* `{TM_AD_ID}` is de door Adobe Advertising gegenereerde alfanumerieke advertentietoets. Deze gebruikt een unieke id voor een advertentie en fungeert als sleutel voor het omzetten van metagegevens van Adobe Advertising-entiteiten in leesbare [!DNL Analytics] -afmetingen.

* `{TM_PLACEMENT_ID}` is de door Adobe Advertising gegenereerde alfanumerieke plaatsingssleutel. De klasse gebruikt een unieke id voor een plaatsing en dient als sleutel voor het omzetten van metagegevens van Adobe Advertising-entiteiten in leesbare [!DNL Analytics] -afmetingen.

Voorbeeld-AMO-id: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### AMO-id-indelingen voor advertenties op zoek, op sociaal gebied en in Commerce {#amo-id-format-search}

De parameters variëren per advertentienetwerk, maar de volgende parameters zijn gemeenschappelijk voor allen:

* `AL` geeft het zoekkanaal aan. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` is een unieke gebruikersnaam die aan de adverteerder is toegewezen.

* `{sid}` wordt vervangen door numerieke identiteitskaart voor de advertentienetwerkrekening van adverteerders: *3* voor [!DNL Google Ads], *10* voor [!DNL Microsoft Advertising], *45* voor [!DNL Meta], *86* voor [!DNL Yahoo! Display Network], *87* voor [!DNL Naver], *88* voor [!DNL Baidu], *90* voor [!DNL Yandex], *94* voor [!DNL Yahoo! Japan Ads], *105* voor [!DNL Yahoo Native] (afgekeurd), of *106 29} for* (afgekeurd).[!DNL Pinterest]

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!88!{creative}!{placement}!{keywordid}`

waarbij:

* `{creative}` is de unieke numerieke id van het advertentienetwerk voor creatieve gebruikers.
* `{placement}` is de website waarop op de advertentie is geklikt.
* `{keywordid}` is de unieke numerieke id van het advertentienetwerk voor het trefwoord dat de advertentie heeft geactiveerd.

##### [!DNL Google Ads]

Dit zijn onder andere winkelcampagnes met [!DNL Google Merchant Center] .

* Accounts die gebruikmaken van de nieuwste AMO ID-indeling, die rapportage op campagne- en groepsniveau voor maximale prestaties ondersteunt voor campagnes en concepten en experimentatiecampagnes:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Alle overige rekeningen:

  `s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

waarbij:

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` is de [!DNL Google Ads] unieke numerieke id voor creatieve projecten.
* `{matchtype}` is het hoofdtype van het trefwoord dat de advertentie heeft geactiveerd: `e` for exact, `p` for express of `b` for wide.
* `{placement}` is de domeinnaam van de website waarop op de advertentie is geklikt. Er is een waarde beschikbaar voor advertenties in op plaatsing gerichte campagnes en voor advertenties in op trefwoorden gerichte campagnes die op inhoudssites worden weergegeven.
* `{network}` geeft het netwerk aan vanwaar de klik plaatsvond: `g` voor [!DNL Google] zoeken (alleen voor advertenties met trefwoordtags), `s` voor een zoekpartner (alleen voor advertenties met trefwoordtags) of `d` voor het weergavenetwerk (voor advertenties met trefwoordtags of voor advertenties met plaatsingsdoelen).
* `{product_partition_id}` is de unieke numerieke id van het advertentienetwerk voor de productgroep die wordt gebruikt met productadvertenties.
* `{keyword}` is ofwel het specifieke trefwoord dat de advertentie heeft geactiveerd (op zoeksites), ofwel het best overeenkomende trefwoord (op inhoudssites).
* `{campaignid}` is de unieke numerieke id van het advertentienetwerk voor de campagne.
* `{adgroupid}` is de unieke numerieke id van het advertentienetwerk voor de advertentiegroep.

>[!NOTE]
>
>* Voor dynamische zoekopdrachten wordt in {keyword} het automatische doel ingevuld.
>* Wanneer u reeksspatiëring genereert voor [!DNL Google] winkeladvertenties, wordt een product-id-parameter `{adwords_producttargetid}` ingevoegd vóór de trefwoordparameter. De parameter voor de product-id wordt niet weergegeven in de trackingparameters op accountniveau en op campagneniveau van [!DNL Google Ads] .
>* Om de recentste het volgen van identiteitskaart van AMO code te gebruiken, zie &quot;[ Update de het volgen code van identiteitskaart AMO voor a  [!DNL Google Ads]  rekening ](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!45!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* Alle soorten campagne:

  `s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}`

waarbij:

* `{AdId}` is de unieke numerieke id van het advertentienetwerk voor creatieve gebruikers.
* `{OrderItemId}` is de numerieke id van het advertentienetwerk voor het trefwoord.
* `{CampaignId}` is de unieke numerieke id van het advertentienetwerk voor de campagne.
* `{AdGroupId}` is de unieke numerieke id van het advertentienetwerk voor de advertentiegroep.

>[!NOTE]
>
> Voor accounts met campagnes zonder de optie [!UICONTROL Auto Upload] bijhouden die nog niet naar de nieuwe indeling waren gemigreerd, werkt u handmatig elk achtervoegsel van de bestemmingspagina bij en voegt u de bovenstaande indeling in.
> >Ondertussen werken de oudere indelingen nog steeds als volgt:
>* Zoekcampagnes:
>  >  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Winkelcampagnes (met [!DNL Microsoft Merchant Center]):
>  >  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* Campagnes van het netwerk van het publiek:
>  >  `s_kwcid=AL!{userid}!10!{AdId}`

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!94!{creative}!{matchtype}!{network}!{keyword}`

waarbij:

* `{creative}` is de unieke numerieke id van het advertentienetwerk voor creatieve gebruikers.
* `{matchtype}` is het hoofdtype van het trefwoord dat de advertentie heeft geactiveerd: `be` for exact, `bp` for express of `bb` for wide.
* `{network}` geeft het netwerk aan vanwaar de klik plaatsvond: `n` voor native of `s` voor zoekopdracht.
* `{keyword}` is het trefwoord dat de advertentie heeft geactiveerd.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!90!{ad_id}!{source_type}!!!{phrase_id}`

waarbij:

* `{ad_id}` is de unieke numerieke id van het advertentienetwerk voor creatieve gebruikers.
* `{source_type}` is het type van plaats waarop de advertentie is getoond: *b* voor onderzoek, *c* voor context (inhoud), of *ct* voor categorie.
* `{phrase_id}` is de numerieke id van het advertentienetwerk voor het trefwoord.

### AMO ID Dimension in [!DNL Analytics]

In analyserapporten kunt u zoeken naar AMO-id-gegevens door te zoeken naar de [!UICONTROL AMO ID] -dimensie en de [!UICONTROL AMO ID Instances] -parameter te gebruiken. In de [!UICONTROL AMO ID] -dimensie worden alle vastgelegde AMO-id-waarden opgeslagen, terwijl de [!UICONTROL AMO ID Instances] -meting aangeeft hoe vaak een AMO-id-waarde door de site is vastgelegd. Als bijvoorbeeld vier keer op dezelfde zoekopdracht werd geklikt en Analytics zeven sittems bijhield, zou [!UICONTROL AMO ID Instances] zeven (7) zijn en [!UICONTROL Clicks] vier (4).

Voor elke rapportage of controle binnen [!DNL Analytics] kunt u het beste de AMO-id en de bijbehorende instantie gebruiken. Voor meer informatie, zie &quot;[ Klik-door de Bevestiging van Gegevens voor  [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot;in &quot;Verwachte Variaties van Gegevens tussen [!DNL Analytics] en Adobe Advertising.&quot;

## Informatie over analytische classificaties

In [!DNL Analytics], is de a [ classificatie ](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) een stuk van meta-gegevens voor een bepaalde het volgen code, zoals Rekening, Campagne, of Advertentie. Adobe Advertising categoriseert onbewerkte Adobe Advertising-gegevens aan de hand van classificaties, zodat u de gegevens op verschillende manieren kunt weergeven (bijvoorbeeld op Advertentietype of Campagne) wanneer u rapporten genereert. Classificaties vormen de basis voor Adobe Advertising-rapportage in [!DNL Analytics] en kunnen worden gebruikt met AMO-metriek, zoals [!UICONTROL Adobe Advertising Cost] , [!UICONTROL Adobe Advertising Impressions] en [!UICONTROL AMO Clicks] , en met aangepaste en standaard onsite gebeurtenissen zoals [!UICONTROL Visits] , [!UICONTROL Leads] , [!UICONTROL Orders] en [!UICONTROL Revenue] .

>[!MORELIKETHIS]
>
>* [ Overzicht van  [!DNL Analytics for Advertising]](overview.md)
>* [ Verwachte Variaties van Gegevens tussen  [!DNL Analytics]  en Adobe Advertising ](data-variances.md)
