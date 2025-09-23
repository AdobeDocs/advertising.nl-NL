---
source-git-commit: 0cf325946fdc3852b8b94acb29678bf6c47227a0
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---
# Adobe Advertising AMO-id&#39;s

## Adobe Advertising AMO-id&#39;s {#amo-id}

De AMO-id houdt elke unieke advertentiecombinatie bij op een minder korrelig niveau en wordt gebruikt voor [!DNL Analytics] - en Customer Journey Analytics-gegevensclassificatie en -opname van advertentiemetriek (zoals indrukken, klikken en kosten) vanuit Adobe Advertising.

Voor [!DNL Analytics], wordt identiteitskaart AMO opgeslagen in een [ eVar ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) of rVar afmeting (identiteitskaart van AMO).

Voor Customer Journey Analytics, wordt identiteitskaart van AMO opgeslagen in het `trackingCode` bezit van het `conversionDetails` voorwerp, dat deel van [ uitmaakt [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension] ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension).

De AMO-id wordt ook wel de `s_kwcid` genoemd, die soms wordt uitgesproken als &quot;[!DNL squid]&quot;.

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
