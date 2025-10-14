---
title: Opmaak voor het bijhouden van klikken voor  [!DNL Google Ads]
description: Leer over de klik-volgende formaten voor  [!DNL Google Ads]  rekeningen.
exl-id: d09c3b4e-1274-45fb-abb6-dddfe60f1477
feature: Search Tracking
source-git-commit: 70629247a18a78b12a7fc8b166a0272764bb20b8
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Opmaak voor het bijhouden van klikken voor [!DNL Google Ads]

Hieronder vindt u de sjabloon voor het bijhouden van de basis en de achtervoegsels van de bestemmingspagina (laatste URL-achtervoegsel) die u nodig hebt voor Zoeken, Sociaal en Commerce [!DNL Google Ads] .

## Sjabloonindelingen bijhouden

### Netwerk voor zoeken/weergeven, inclusief sitelinks

De volgende indeling is van toepassing op alle traceerbare advertentietypen op zoek- en weergavenetwerken en voor sitelinks.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Voorbeeld:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder in Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als tokendoorgeven is uitgeschakeld, vervangt u `cq?` after `<advertiser_ID>` with `c?` .
>
>* De parameters [!DNL ValueTrack] om uiteindelijke URL&#39;s in trackingsjablonen aan te geven, moeten `{lpurl}` of `!{unescapedurl}` zijn.
>
>* (Tekstadvertenties) Wanneer u op trefwoord biedt, heeft de parameter `ev_pl` (voor plaatsingen) geen waarde. Wanneer u op plaatsing biedt, heeft `ev_ln` (voor trefwoorden) geen waarde. Wanneer u op een advertentiegroep of op een andere dimensie biedt, hebben zowel `ev_ln` als `ev_pl` geen waarden.
>
>* (Dynamische zoekopdrachten) `{keyword}` geeft de dynamische zoekdoelexpressie aan, zoals `_cat:[VALUE]` of `_url:[VALUE]` .
>
>* (Dynamische zoekopdrachten) [!DNL Google Ads] bepaalt de uiteindelijke URL dynamisch, zodat u er geen hoeft in te voeren.
>
>* (Sitelinks) U kunt zien welke omzettingen het resultaat zijn van een klik op een sitelink door een [!UICONTROL Transaction Report] te genereren. De kolomwaarde [!UICONTROL Link Type] voor een sitelink is `sl:<Sitelink text>` , zoals `sl:See Current Offers` .

### Winkelnetwerk

De volgende indeling is van toepassing op winkeladvertenties en productgroepen in winkelnetwerken. U kunt een sjabloon voor bijhouden opgeven op account-, campagne-, groep- of productgroepniveau.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Voorbeeld:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder in Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als tokendoorgeven is uitgeschakeld, vervangt u `cq?` after `<advertiser_ID>` with `c?` .
>
>* De parameters [!DNL ValueTrack] om uiteindelijke URL&#39;s in trackingsjablonen aan te geven, moeten `{lpurl}` of `!{unescapedurl}` zijn.
>
>* [!DNL Google Ads] gebruikt product-URL&#39;s in de Google Merchant Center-feed als de uiteindelijke URL&#39;s, zodat u geen definitieve URL&#39;s hoeft in te voeren voor uw productgegevens of productgroepen.
>
>* U kunt zien welke conversies het resultaat zijn van een klik op een advertentie door een [!UICONTROL Transaction Report] te genereren. De [!UICONTROL Link Type] -kolomwaarde voor een productadvertentie is .pla:`<product ID>`, zoals `pla:8525822` .

## Opmaak voor het achtervoegsel van de landingspagina (laatste URL-achtervoegsel)

Accounts die gebruikmaken van het bijhouden van Adobe Advertising-conversies, moeten de klikidentificatie (`gclid` for [!DNL Google Ads] ) van het advertentienetwerk opnemen in het achtervoegsel:

* Wanneer de adverteerder een Adobe Analytics-integratie heeft, moet het achtervoegsel een van de volgende elementen bevatten:

   * [!DNL Google Ads] rekeningen die het recentste [&#x200B; formaat van identiteitskaart van AMO &#x200B;](/help/integrations/analytics/ids.md#amo-id-formats) (beginnend met `s_kwcid`) gebruiken, dat campagne- en ad groep-vlakke rapportering voor prestaties max campagnes en concepten en experimentatiecampagnes steunt:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

     Als de rekening een server-kant implementatie van identiteitskaart van AMO heeft en de rekening of campagne die &quot; [!UICONTROL Auto Upload]&quot;plaatsen wordt toegelaten, dan wordt de parameter automatisch toegevoegd. Anders moet u het handmatig toevoegen. Zie &quot;[&#x200B; Adobe Advertising IDs die door  [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id-implement) wordt gebruikt.&quot;

   * Alle andere [!DNL Google Ads] -accounts:

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* Wanneer de adverteerder geen Adobe Analytics-integratie heeft, moet het achtervoegsel het volgende bevatten:

  `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* Achtervoegsels op lagere niveaus van de bestemmingspagina hebben voorrang op het achtervoegsel op accountniveau. Gebruik voor een eenvoudiger onderhoud alleen het achtervoegsel op accountniveau, tenzij het bijhouden van wijzigingen voor afzonderlijke accountcomponenten nodig is. Om een achtervoegsel op het niveau van de advertentiegroep of lager te vormen, gebruik de redacteur van het advertentienetwerk.
>
>* (Dynamische zoekadvertenties; adverteerders met Adobe Analytics en zonder tracering op de server) Als u tracering voor de reverse feed van Adobe Advertising naar Analytics wilt opnemen, voegt u de trackingcode van de AMO-id toe aan het einde van het achtervoegsel van de landingspagina op accountniveau.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer klik-volgende formaten URL voor de conversie het volgen dienst van Adobe Advertising &#x200B;](formats-click-tracking-about.md)
>* [&#x200B; formaten van identiteitskaart AMO &#x200B;](/help/integrations/analytics/ids.md#amo-id-formats)
