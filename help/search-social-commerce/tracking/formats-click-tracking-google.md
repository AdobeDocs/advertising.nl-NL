---
title: Opmaak voor het bijhouden van klikken voor [!DNL Google Ads]
description: Meer informatie over de indelingen voor klikken en bijhouden voor [!DNL Google Ads] rekeningen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# Opmaak voor het bijhouden van klikken voor [!DNL Google Ads]

Hieronder vindt u de basissjabloon voor bijhouden en de achtervoegsels van de landingspagina (het laatste URL-achtervoegsel) waarvoor Zoeken, Sociale zaken en Handel vereist zijn [!DNL Google Ads].

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
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als het doorgeven van token is uitgeschakeld, kunt u dit vervangen `cq?` na `<advertiser_ID>` with `c?`.
>
>* De [!DNL ValueTrack] parameters om uiteindelijke URL&#39;s in trackingsjablonen aan te geven, moeten `{lpurl}` of `!{unescapedurl}`.
>
>* (Tekstadvertenties) Wanneer u op trefwoord biedt, wordt de parameter `ev_pl` (voor plaatsingen) heeft geen waarde. Wanneer je op plaatsing biedt, `ev_ln` (voor trefwoorden) heeft geen waarde. Wanneer je biedt op advertentiegroep of op een andere dimensie, beide `ev_ln` en `ev_pl` hebben geen waarden.
>
>* (Dynamische zoekopdrachten) `{keyword}` Hiermee wordt de dynamische zoekdoelexpressie aangegeven, zoals `_cat:[VALUE]` of `_url:[VALUE]`.
>
>* (Dynamische zoekopdrachten) [!DNL Google Ads] bepaalt dynamisch definitieve URL, zodat te hoeven u niet om in te gaan.
>
>* (Sitelinks) U kunt zien welke omzettingen het resultaat zijn van een klik op een sitelink door een [!UICONTROL Transaction Report]. De [!UICONTROL Link Type] kolomwaarde voor een sitelink is `sl:<Sitelink text>`, zoals `sl:See Current Offers`.


### Winkelnetwerk

De volgende indeling is van toepassing op winkeladvertenties en productgroepen in winkelnetwerken. U kunt een sjabloon voor bijhouden opgeven op account-, campagne-, groep- of productgroepniveau.

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

Voorbeeld:

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder in Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als het doorgeven van token is uitgeschakeld, kunt u dit vervangen `cq?` na `<advertiser_ID>` with `c?`.
>
>* De [!DNL ValueTrack] parameters om uiteindelijke URL&#39;s in trackingsjablonen aan te geven, moeten `{lpurl}` of `!{unescapedurl}`.
>
>* [!DNL Google Ads] gebruikt product-URL&#39;s in de Google Merchant Center-feed als de uiteindelijke URL&#39;s, zodat u geen definitieve URL&#39;s hoeft in te voeren voor uw productgegevens of productgroepen.
>
>* U kunt zien welke omzettingen het resultaat zijn van een klik op een advertentie door een [!UICONTROL Transaction Report]. De [!UICONTROL Link Type] kolomwaarde voor een productadvertentie is plus:`<product ID>`, zoals `pla:8525822`.


## Opmaak voor het achtervoegsel van de landingspagina (laatste URL-achtervoegsel)

Accounts die Adobe Advertising conversion tracking gebruiken, moeten de klikidentificatie van het advertentienetwerk bevatten (`gclid` for [!DNL Google Ads]) in het achtervoegsel:

* Wanneer de adverteerder een Adobe Analytics-integratie heeft, moet het achtervoegsel een van de volgende elementen bevatten:

   * [!DNL Google Ads] accounts die gebruikmaken van de meest recente `s_kwcid` formaat, dat campagne-en ad groep-vlakke rapportering voor prestaties maximumcampagnes en concepten en experimentatiecampagnes steunt:

      `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

      Als voor de account een s_kwcid-implementatie aan de serverzijde en de account- of campagne-instelling &quot;[!UICONTROL Auto Upload]&quot; is ingeschakeld, wordt de parameter automatisch toegevoegd. Anders moet u het handmatig toevoegen.

   * Alle andere [!DNL Google Ads] accounts:

      `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* Wanneer de adverteerder geen Adobe Analytics-integratie heeft, moet het achtervoegsel het volgende bevatten:

   `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* Achtervoegsels op lagere niveaus van de bestemmingspagina hebben voorrang op het achtervoegsel op accountniveau. Gebruik voor een eenvoudiger onderhoud alleen het achtervoegsel op accountniveau, tenzij het bijhouden van wijzigingen voor afzonderlijke accountcomponenten nodig is. Om een achtervoegsel op het niveau van de advertentiegroep of lager te vormen, gebruik de redacteur van het ad netwerk.
>
>* (Dynamische zoekopdrachten; adverteerders met Adobe Analytics en zonder tracking op de server) Als u tracering wilt opnemen voor de reverse feed van Adobe Advertising naar Analytics, voegt u de `s_kwcid` volgcode tot het einde van het achtervoegsel van de landingspagina op accountniveau.


>[!MORELIKETHIS]
>
>* [Over het bijhouden van klikken op URL-indelingen voor de service voor het bijhouden van Adobe-advertenties](formats-click-tracking-about.md)
>* [Opmaak voor de s\_kwcid-trackingcode](skwcid-tracking-parameter.md)
