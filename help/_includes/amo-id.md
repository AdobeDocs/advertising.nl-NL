---
source-git-commit: 6fa4e5d06271789edc915d67d320f775a83ed653
workflow-type: tm+mt
source-wordcount: '992'
ht-degree: 0%

---
# Adobe Advertising AMO-id&#39;s

## Adobe Advertising AMO-id&#39;s {#amo-id}

De AMO-id houdt elke unieke advertentiecombinatie bij op een minder korrelig niveau en wordt gebruikt voor [!DNL Analytics] - en Customer Journey Analytics-gegevensclassificatie en -opname van advertentiemetriek (zoals indrukken, klikken en kosten) vanuit Adobe Advertising.

Voor [!DNL Analytics], wordt identiteitskaart AMO opgeslagen in een [ eVar ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) of rVar afmeting (identiteitskaart van AMO).

Voor Customer Journey Analytics wordt de AMO-id opgeslagen in de eigenschap `trackingCode` van het `conversionDetails` -object, dat deel uitmaakt van de [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension] -id.

De AMO-id wordt ook wel de `s_kwcid` genoemd, die soms wordt uitgesproken als &quot;[!DNL squid]&quot;.

### ([!DNL Analytics] gebruikers) Manieren om AMO-id te implementeren {#amo-id-implement}

<!-- Add info about implementing in CJA -->

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

* `{TM_AD_ID}` is de door Adobe Advertising gegenereerde alfanumerieke advertentietoets. De klasse gebruikt een unieke id voor een advertentie en fungeert als sleutel voor het omzetten van metagegevens van Adobe Advertising-entiteiten in leesbare [!DNL Analytics] - en Customer Journey Analytics-afmetingen.

* `{TM_PLACEMENT_ID}` is de door Adobe Advertising gegenereerde alfanumerieke plaatsingssleutel. De klasse gebruikt een unieke id voor een plaatsing en dient als sleutel voor het omzetten van metagegevens van Adobe Advertising-entiteiten in leesbare [!DNL Analytics] - en Customer Journey Analytics-afmetingen.

Voorbeeld-AMO-id: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

#### AMO-id-indelingen voor advertenties op zoek, op sociaal gebied en in Commerce {#amo-id-format-search}

De parameters variëren per advertentienetwerk, maar de volgende parameters zijn gemeenschappelijk voor allen:

* `AL` geeft het zoekkanaal aan. <!-- what about social/Facebook, and display ads on Google (like Gmail, YouTube)? -->

* `{userid}` is een unieke gebruikersnaam die aan de adverteerder is toegewezen.

* `{sid}` wordt vervangen door numerieke identiteitskaart voor de advertentienetwerkrekening van adverteerders: *3* voor [!DNL Google Ads], *10* voor [!DNL Microsoft Advertising], *45* voor [!DNL Meta], *86* voor [!DNL Yahoo! Display Network], *87* voor [!DNL Naver], *88* voor [!DNL Baidu], *90* voor [!DNL Yandex], *94* voor [!DNL Yahoo! Japan Ads], *105* voor [!DNL Yahoo Native] (afgekeurd), of *106 29&rbrace; for* (afgekeurd).[!DNL Pinterest]

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
> &#x200B;>Ondertussen werken de oudere indelingen nog steeds als volgt:
>* Zoekcampagnes:
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}!!{CampaignId}!{AdGroupId}`
>* Winkelcampagnes (met [!DNL Microsoft Merchant Center]):
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`
>* Campagnes van het netwerk van het publiek:
>  &#x200B;>  `s_kwcid=AL!{userid}!10!{AdId}`

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
