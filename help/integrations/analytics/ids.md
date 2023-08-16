---
title: Adobe Advertising-id's gebruikt door [!DNL Analytics]
description: Adobe Advertising-id's gebruikt door [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 336664e00f626a7841c328b53b8f5cea1444f3d7
workflow-type: tm+mt
source-wordcount: '1667'
ht-degree: 0%

---

# Adobe Advertising-id&#39;s gebruikt door [!DNL Analytics]

*Adverteerders met alleen Adobe Advertising-Adobe Analytics-integratie*

*Van toepassing op DSP en[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising gebruikt twee id&#39;s voor het on-site bijhouden van prestaties: de *EF-id* en de *AMO-id*.

Wanneer een advertentie-impositie optreedt, maakt Adobe Advertising de waarden voor AMO-id en EF-id en slaat deze op. Wanneer een bezoeker die een advertentie heeft gezien, de site betreedt zonder op een advertentie te klikken, [!DNL Analytics] roept deze waarden van Adobe Advertising door [!DNL Analytics for Advertising] JavaScript-code. Voor doorkijkverkeer, [!DNL Analytics] Hiermee wordt een aanvullende id gegenereerd (`SDID`), dat wordt gebruikt om de EF-id en de AMO-id in te voegen [!DNL Analytics]. Voor doorklikverkeer worden deze id&#39;s opgenomen in de URL van de bestemmingspagina met behulp van de `ef_id` en `s_kwcid` (voor de AMO ID) query string parameters.

Bij de Adobe Advertising wordt aan de hand van de volgende criteria onderscheid gemaakt tussen een doorklikitem of een doorkijkitem op de website:

* Een view-through ingang wordt gevangen wanneer een gebruiker de plaats na het bekijken van een advertentie bezoekt maar niet het klikt. [!DNL Analytics] registreert een mening-door als twee voorwaarden worden voldaan:

   * De bezoeker heeft geen doorklikken voor een [!DNL DSP] of [!DNL Search, Social, & Commerce] advertentie tijdens de [klik terugkijkvenster](#lookback-a4adc).

   * De bezoeker heeft minstens één [!DNL DSP] advertentie tijdens de [terugkijkvenster van indruk](#lookback-a4adc). De laatste indruk wordt doorgegeven als de doorkijkhoek.

* Een doorklikitem wordt vastgelegd wanneer een sitebezoeker op een advertentie klikt voordat hij de site betreedt. [!DNL Analytics] vangt een klik-door wanneer één van beiden van de volgende voorwaarden voorkomt:

   * De URL bevat een EF-id en een AMO-id die via Adobe Advertising aan de URL van de bestemmingspagina zijn toegevoegd.

   * De URL bevat geen volgcodes, maar de JavaScript-code van de Adobe Advertising detecteert een klik binnen de laatste twee minuten.

![Op weergave gebaseerde Adobe Advertising [!DNL Analytics] integratie](/help/integrations/assets/a4adc-view-through-process.png)

*Afbeelding 1: Op weergave gebaseerde Adobe Advertising [!DNL Analytics] integratie*

![Adobe Advertising klikken op URL [!DNL Analytics] integratie](/help/integrations/assets/a4adc-click-through-process.png)

*Afbeelding 2: Adobe Advertising klikken op URL [!DNL Analytics] integratie*

## Adobe Advertising EF-id&#39;s

De EF-id is een unieke token die de Adobe Advertising gebruikt om activiteit te koppelen aan een online klik of advertentie. De EF-id wordt opgeslagen in [een [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) of [!DNL rVar] (voorbehouden) [!DNL eVar]) (Adobe Advertising EF-id) en houdt elke muisklik of belichting op het niveau van de afzonderlijke browser of het apparaat bij. EF-id&#39;s fungeren voornamelijk als sleutels voor het verzenden [!DNL Analytics] gegevens aan Adobe Advertising voor rapportage en optimalisering van biedingen binnen de Adobe Advertising.

### EF-id-indeling

>[!NOTE]
>
>EF-id&#39;s zijn hoofdlettergevoelig. Als een [!DNL Analytics] de implementatie forceert URL-tracking naar kleine letters en de Adobe Advertising herkent de EF-id dan niet. Dit heeft gevolgen voor de Adobe Advertising van biedingen en rapportage, maar heeft geen invloed op de rapportage van Adoben Advertising binnen [!DNL Analytics].

#### [!DNL Google Ads] zoekopdrachten

```
{gclid}:G:s
```

waarbij:

* `gclid` is de [!DNL Google Click ID] (GCLID).
* `s` is het netwerktype (&quot;s&quot; voor onderzoek).

#### Microsoft Adverteren, zoekadvertenties

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

* &lt;*Adobe Advertising-bezoeker-id*> is een unieke id per bezoeker (zoals EhKVaAABCkJ0mDt). Wordt ook de *surfer-id*.

* &lt;*tijdstempel*> is de tijd in de notatie YYYYMMDDHHMMSS (zoals 20190821192533 voor 2019, maand 08, dag 21, tijd 19):25:33).

* &lt;*kanaaltype*> is het kanaaltype dat verantwoordelijk is voor de klik of de blootstelling:

   * `d` voor een klik op een DSP (klik-door tonen)
   * `i` voor een indruk van een DSP (display view-through)
   * `s` voor een klik op een zoekadvertentie (doorzoekklik).

Voorbeeld `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### Het EF-id-Dimension in [!DNL Analytics]

In [!DNL Analytics] rapporten, kunt u EF-ID gegevens vinden door naar [!UICONTROL EF ID] dimensie en het gebruik van de [!UICONTROL EF ID Instance] metrisch.

Voor EF-id&#39;s geldt de limiet van 500 kB voor unieke identificatiekenmerken in Analysis Workspace. Zodra de waarde van 500 k is bereikt, worden alle nieuwe volgcodes gerapporteerd onder de titel van één regel-item &quot;[!UICONTROL Low Traffic].&quot; Omdat het mogelijk is dat de rapportbetrouwbaarheid ontbreekt, worden de EF-id&#39;s niet geclassificeerd en mag u deze niet gebruiken voor segmenten of voor rapportage in [!DNL Analytics].

## AMO-id&#39;s Adoben Advertising {#amo-id}

De AMO-id volgt elke unieke advertentiecombinatie op een minder granulair niveau en wordt gebruikt voor [!DNL Analytics] gegevensclassificatie en opname van advertentiemetriek (zoals indrukken, klikken en kosten) van Adobe Advertising. De AMO-id is opgeslagen in een [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) of de rVar-dimensie (AMO-id) en wordt uitsluitend gebruikt voor rapportage in [!DNL Analytics].

De AMO-id wordt ook wel de `s_kwcid`, die soms wordt uitgesproken als &quot;[!DNL the squid].&quot;

### Manieren om de AMO-id te implementeren

De parameter wordt op een van de volgende manieren toegevoegd aan de URL&#39;s die worden gevolgd:

* (Aanbevolen) De invoegfunctie aan de serverzijde is geïmplementeerd.

   * DSP klanten: De pixelserver voegt automatisch de parameter s_kwcid aan uw het landen paginaachtervoegsels toe wanneer een eind - gebruiker een vertoningsadvertentie met de Adobe Advertising pixel bekijkt.

   * Zoek-, sociale en commerciële klanten:

      * Voor [!DNL Google Ads] en [!DNL Microsoft® Advertising] rekeningen bij de [!UICONTROL Auto Upload] Wanneer de pixelserver de voor de account of campagne ingeschakelde instelling instelt, voegt deze automatisch de parameter s_kwcid toe aan de achtervoegsels van de bestemmingspagina wanneer een eindgebruiker op een advertentie met de Adobe Advertising pixel klikt.

      * voor andere advertentienetwerken, of [!DNL Google Ads] en [!DNL Microsoft® Advertising] rekeningen bij de [!UICONTROL Auto Upload] instellen uitgeschakeld, handmatig [voeg de parameter aan uw rekening-vlakke toevoegingsparameters toe](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, die deze toevoegen aan uw basis-URL&#39;s.

* De invoegfunctie aan de serverzijde is niet geïmplementeerd:

   * DSP klanten:

      * Voor [!DNL Flashtalking] ad-tags, voeg handmatig extra macro&#39;s in per &quot;[Toevoegen [!DNL Analytics for Advertising] Macro&#39;s naar [!DNL Flashtalking] Labels toevoegen](/help/integrations/analytics/macros-flashtalking.md).&quot;

      * Voor [!DNL Google Campaign Manager 360] ad-tags, voeg handmatig extra macro&#39;s in per &quot;[Toevoegen [!DNL Analytics for Advertising] Macro&#39;s naar [!DNL Google Campaign Manager 360] Labels toevoegen](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

  <!--  * For all other ads, XXXX. -->

   * Zoek-, sociale en commerciële klanten:

      * Voor ([!DNL Google Ads] en [!DNL Microsoft® Advertising]), handmatig de parameter AMO ID toevoegen aan de achtervoegsels van de bestemmingspagina, idealiter op de [accountniveau](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} tenzij afzonderlijke onderdelen van een account anders moeten worden getraceerd.

      * Voor advertenties op alle andere advertentienetwerken, handmatig [voeg de parameter AMO ID toe aan de toevoegingsparameters op accountniveau](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"}, die deze toevoegen aan uw basis-URL&#39;s.

Als u de invoegfunctie aan de serverzijde wilt implementeren of de beste optie voor uw bedrijf wilt bepalen, neemt u contact op met het accountteam van de Adobe.

### AMO-id-indelingen {#amo-id-formats}

#### AMO-id-indeling voor [!DNL DSP]

`s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}`

waarbij:

* `AC` Hiermee wordt het weergavekanaal aangegeven.

* `{TM_AD_ID}` is de door de Adobe Advertising gegenereerde alfanumerieke advertentietoets. De id wordt gebruikt als een unieke id voor een advertentie en fungeert als sleutel voor het omzetten van metagegevens van een Adobe Advertising-entiteit in leesbaar [!DNL Analytics] afmetingen.

* `{TM_PLACEMENT_ID}` is de door de Adobe Advertising gegenereerde alfanumerieke plaatsingssleutel. Het gebruikt een unieke herkenningsteken voor een plaatsing en dient als sleutel voor het omzetten van de meta-gegevens van de Adobe Advertising entiteit in leesbaar [!DNL Analytics] afmetingen.

Voorbeeld-AMO-id: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### AMO ID-indelingen voor advertenties voor zoeken, sociale media en handel

De parameters variëren per advertentienetwerk, maar de volgende parameters zijn gemeenschappelijk voor allen:

* `AL` Hiermee wordt het zoekkanaal aangegeven. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` is een unieke gebruikersnaam die aan de adverteerder is toegewezen.

* `{sid}` wordt vervangen door de numerieke id van de advertentienetwerkaccount van de adverteerder: *3* for [!DNL Google Ads], *10* for [!DNL Microsoft Advertising], *45* for [!DNL Meta], *86* for [!DNL Yahoo! Display Network], *87* for [!DNL Naver], *88* for [!DNL Baidu], *90* for [!DNL Yandex], *94* for [!DNL Yahoo! Japan Ads], *105* for [!DNL Yahoo Native] (afgekeurd), of *106* for [!DNL Pinterest] (vervangen).

##### [!DNL Baidu]

`s_kwcid=AL!{userid}!{sid}!{creative}!{placement}!{keywordid}`

waarbij:

* `{creative}` Dit is de unieke numerieke id van het advertentienetwerk voor creatieve gebruikers.
* `{placement}` is de website waarop op de advertentie is geklikt.
* `{keywordid}` Dit is de unieke numerieke id van het advertentienetwerk voor het trefwoord dat de advertentie activeerde.

##### [!DNL Google Ads]

Hieronder vallen ook boodschappencampagnes die [!DNL Google Merchant Center].

* Accounts die gebruikmaken van de nieuwste AMO ID-indeling, die rapportage op campagne- en groepsniveau voor maximale prestaties ondersteunt voor campagnes en concepten en experimentatiecampagnes:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

* Alle overige rekeningen:

  `s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

waarbij:

<!-- VERIFY CREATIVE description. Also, are there more networks now (audience and shopping?) -->

* `{creative}` is de [!DNL Google Ads] unieke numerieke id voor creatieve doeleinden.
* `{matchtype}` is het matchype van het sleutelwoord dat de advertentie teweegbracht: `e` voor exact, `p` voor woordgroep, of `b` voor het algemeen.
* `{placement}` Dit is de domeinnaam van de website waarop op de advertentie is geklikt. Er is een waarde beschikbaar voor advertenties in op plaatsing gerichte campagnes en voor advertenties in op trefwoorden gerichte campagnes die op inhoudssites worden weergegeven.
* `{network}` Hiermee wordt het netwerk aangegeven vanwaar de klik heeft plaatsgevonden: `g` for [!DNL Google] zoeken (alleen voor advertenties die op trefwoorden zijn gericht), `s` voor een zoekpartner (alleen voor advertenties die op trefwoorden zijn gericht), of `d` voor het weergavenetwerk (voor ofwel doeltrefwoorden ofwel plaatsingsadvertenties).
* `{product_partition_id}` Dit is de unieke numerieke id van het advertentienetwerk voor de productgroep die wordt gebruikt met productadvertenties.
* `{keyword}` is of het specifieke sleutelwoord dat uw advertentie (op onderzoeksplaatsen) of het best-passende sleutelwoord (op inhoudsplaatsen) teweegbracht.
* `{campaignid}` Dit is de unieke numerieke id van het advertentienetwerk voor de campagne.
* `{adgroupid}` Dit is de unieke numerieke id van het advertentienetwerk voor de advertentiegroep.

>[!NOTE]
>
>* Voor dynamische zoekopdrachten {keyword} wordt gevuld met het automatische doel.
>* Wanneer u tekstspatiëring genereert voor [!DNL Google] winkeladvertenties, een product-id-parameter, `{adwords_producttargetid}`, wordt ingevoegd vóór de trefwoordparameter. De parameter product-id wordt niet weergegeven in het dialoogvenster [!DNL Google Ads] parameters voor het bijhouden op accountniveau en op campagnereniveau.
>* Als u de nieuwste trackingcode voor de AMO-id wilt gebruiken, raadpleegt u &quot;[De trackingcode van de AMO-id bijwerken voor een [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot; <!-- Update terminology there too. -->

<!--

##### [!DNL Meta]

`s_kwcid=AL!{userid}!{sid}!{{ad.id}}!{{campaign.id}}!{{adset.id}}`

where:

* `{{ad.id}}` is the unique numeric ID for the ad/creative.

* `{{campaign.id}}` is the unique ID for the campaign.

* `{{adset.id}}` is the unique ID for the ad set.

-->

##### [!DNL Microsoft Advertising]

* Zoekcampagnes:

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Winkelcampagnes (gebruiken [!DNL Microsoft Merchant Center]):

  `s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Campagnes van het netwerk van het publiek:

  `s_kwcid=AL!{userid}!{sid}!{AdId}`

waarbij:

* `{AdId}` Dit is de unieke numerieke id van het advertentienetwerk voor creatieve gebruikers.
* `{OrderItemId}` is de numerieke id van het advertentienetwerk voor het trefwoord.
* `{CriterionId}` is de numerieke id van het advertentienetwerk voor de productgroep die wordt gebruikt met productadvertenties.

##### [!DNL Yahoo! Japan Ads]

`s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{network}!{keyword}`

waarbij:

* `{creative}` Dit is de unieke numerieke id van het advertentienetwerk voor creatieve gebruikers.
* `{matchtype}` is het matchype van het sleutelwoord dat de advertentie teweegbracht: `be` voor exact, `bp` voor woordgroep, of `bb` voor het algemeen.
* `{network}` Hiermee wordt het netwerk aangegeven vanwaar de klik heeft plaatsgevonden: `n` voor native of `s` voor zoekopdracht.
* `{keyword}` Dit is het trefwoord dat de advertentie heeft geactiveerd.

##### [!DNL Yandex]

`s_kwcid=AL!{userid}!{sid}!{ad_id}!{source_type}!!!{phrase_id}`

waarbij:

* `{ad_id}` Dit is de unieke numerieke id van het advertentienetwerk voor creatieve gebruikers.
* `{source_type}` is het type site waarop de advertentie is weergegeven: *b* voor zoekopdrachten, *c* voor context (inhoud), of *ct* voor categorie.
* `{phrase_id}` is de numerieke id van het advertentienetwerk voor het trefwoord.

### AMO ID-Dimension in [!DNL Analytics]

In analyserapporten kunt u zoeken naar AMO ID-gegevens [!UICONTROL AMO ID] dimensie en het gebruik van de [!UICONTROL AMO ID Instance] metrisch. De [!UICONTROL AMO ID] dimensie bevat alle vastgelegde AMO-id-waarden, terwijl de [!UICONTROL AMO ID Instance] De metrische waarde geeft aan hoe vaak een AMO-id-waarde door de site is vastgelegd. Als bijvoorbeeld vier keer op dezelfde zoekopdracht is geklikt, maar Analytics zeven sitems heeft bijgehouden, [!UICONTROL AMO ID Instance] zou zeven (7) zijn en [!UICONTROL Clicks] zou vier (4) zijn.

Voor elke rapportage of controle binnen [!DNL Analytics]De beste manier is om de AMO-id samen met het bijbehorende exemplaar te gebruiken. Zie voor meer informatie &quot;[Gegevensvalidatie voor [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot; in &quot;Verwachte gegevensvariaties tussen [!DNL Analytics] en Adobe Advertising.&quot;

## Informatie over analytische classificaties

In [!DNL Analytics], [classificatie](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) is een stuk van meta-gegevens voor een bepaalde het volgen code, zoals Rekening, Campagne, of Advertentie. De Adobe Advertising categoriseert ruwe gegevens van de Adobe Advertising gebruikend classificaties zodat u de gegevens op verschillende manieren (zoals door het Type van Advertentie of Campagne) kunt tonen wanneer u rapporten produceert. Classificaties vormen de basis voor de rapportage van Adoben Advertising in [!DNL Analytics] en kan worden gebruikt met de AMO-metriek, zoals [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions], en [!UICONTROL AMO Clicks]en met aangepaste en standaard onsite gebeurtenissen zoals [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders], en [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Overzicht van [!DNL Analytics for Advertising]](overview.md)
>* [Verwachte gegevensvariaties tussen [!DNL Analytics] en Adobe Advertising](data-variances.md)
