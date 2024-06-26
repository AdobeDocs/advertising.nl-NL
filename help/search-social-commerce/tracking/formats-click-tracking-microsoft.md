---
title: Opmaak voor het bijhouden van klikken voor [!DNL Microsoft Advertising]
description: Meer informatie over de indelingen voor klikken en bijhouden voor [!DNL Microsoft Advertising] rekeningen.
exl-id: 4970ac33-4978-4768-8701-6fdd3252bbd1
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# Opmaak voor het bijhouden van klikken voor [!DNL Microsoft Advertising]

Hieronder vindt u de sjabloon voor het bijhouden van de basis en de achtervoegsels van de bestemmingspagina (laatste URL-achtervoegsel), waarvoor Zoeken, Sociaal en Commerce vereist is [!DNL Microsoft Advertising].

## Sjabloonindelingen bijhouden

### Zoeken en publieksnetwerken (behalve voor sitelinks)

De volgende indeling is van toepassing op alle trackable advertentietypen op zoek- en publieksnetwerken.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Voorbeeld:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder binnen de Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als het doorgeven van token is uitgeschakeld, kunt u dit vervangen `cq?` na `<advertiser_ID>` with `c?`.
>
>* `{TargetId}` vertegenwoordigt identiteitskaart van a) of het sleutelwoord of b) het sleutelwoord en remarketing lijst (publiek) die de advertentie teweegbracht (bijvoorbeeld, &quot;kwd-123:aud-456&quot;voor zowel een sleutelwoord als een remarketing lijst of &quot;kwd-123&quot;voor slechts sleutelwoord).

### Sitelinks

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Voorbeeld:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder binnen de Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als het doorgeven van token is uitgeschakeld, kunt u dit vervangen `cq?` na `<advertiser_ID>` with `c?`.
>
>* `{TargetId}` vertegenwoordigt identiteitskaart van a) of het sleutelwoord of b) het sleutelwoord en remarketing lijst (publiek) die de advertentie teweegbracht (bijvoorbeeld, &quot;kwd-123:aud-456&quot;voor zowel een sleutelwoord als een remarketing lijst of &quot;kwd-123&quot;voor slechts sleutelwoord).
>
>* `{adextensionid}` niet wordt gebruikt.
>
>* (Sitelinks) U kunt zien welke omzettingen het resultaat zijn van een klik op een sitelink door een [!UICONTROL Transaction Report]. De [!UICONTROL Link Type] kolomwaarde voor een sitelink is `sl:<Sitelink text>`, zoals `sl:See Current Offers`.

### Winkelnetwerk

De volgende formaten zijn van toepassing voor het winkelen van advertenties in het winkelen netwerken. U kunt een sjabloon voor bijhouden opgeven op account-, campagne-, groep- of productgroepniveau.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

Voorbeeld:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder binnen de Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als het doorgeven van token is uitgeschakeld, kunt u dit vervangen `cq?` na `<advertiser_ID>` with `c?`.
>
>* `{TargetId}` vertegenwoordigt identiteitskaart van a) of het sleutelwoord of b) het sleutelwoord en remarketing lijst (publiek) die de advertentie teweegbracht (bijvoorbeeld, &quot;kwd-123:aud-456&quot;voor zowel een sleutelwoord als een remarketing lijst of &quot;kwd-123&quot;voor slechts sleutelwoord).
>
>* (Optioneel) In plaats van trackingsjablonen in te voeren op account-, campagne-, groep- of productgroepniveau, kunt u de URL voor bijhouden toevoegen aan de productgegevens in het dialoogvenster [!DNL Microsoft Merchant Center] account. Hiervoor neemt u de URL voor tekstspatiëring op, samen met de waarde in het veld &quot;`link`&quot; of &quot;`mobile_link`&quot;veld, naar gelang van het geval, in een aangepaste kolom &quot;[bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0)&quot; in het voer van het product. De waarde in het veld &quot;`bingads_redirect`&quot; worden de waarden in &quot;`link`&quot; en &quot;`mobile_link`&quot;. URL&#39;s die met deze methode worden gegenereerd, bevatten geen volgparameters die zijn opgegeven in de instellingen voor Zoeken, Sociaal zoeken en Commerce.

## Opmaak voor het achtervoegsel van de landingspagina (laatste URL-achtervoegsel)

>[!NOTE]
>
>Achtervoegsels op lagere niveaus van de bestemmingspagina hebben voorrang op het achtervoegsel op accountniveau. Gebruik voor een eenvoudiger onderhoud alleen het achtervoegsel op accountniveau, tenzij het bijhouden van wijzigingen voor afzonderlijke accountcomponenten nodig is. Om een achtervoegsel op het niveau van de advertentiegroep of lager te vormen, gebruik de redacteur van het advertentienetwerk.

### Zoeken en publieksnetwerken

Accounts die Adobe Advertising conversion tracking gebruiken, moeten de click identifier van het advertentienetwerk (`msclkid` for [!DNL Microsoft Advertising]) in het achtervoegsel:

* Wanneer de adverteerder een Adobe Analytics-integratie heeft, moet het achtervoegsel het volgende bevatten:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* Wanneer de adverteerder geen Adobe Analytics-integratie heeft, moet het achtervoegsel het volgende bevatten:

  `&ev_efid={msclkid}:G:s`

### Winkelnetwerk

Accounts die Adobe Advertising conversion tracking gebruiken, moeten de click identifier van het advertentienetwerk (`msclkid` for [!DNL Microsoft Advertising]) in het achtervoegsel:

* Wanneer de adverteerder een Adobe Analytics-integratie heeft, moet het achtervoegsel het volgende bevatten:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* Wanneer de adverteerder geen Adobe Analytics-integratie heeft, moet het achtervoegsel het volgende bevatten:

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [Over URL-indelingen voor het bijhouden van klikken voor de service Adobe Advertising converteren](formats-click-tracking-about.md)
>* [AMO ID-indelingen](/help/integrations/analytics/ids.md#amo-id-formats)
