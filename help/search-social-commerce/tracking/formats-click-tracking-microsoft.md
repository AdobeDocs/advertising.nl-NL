---
title: Opmaak voor het bijhouden van klikken voor  [!DNL Microsoft Advertising]
description: Leer over de klik-volgende formaten voor  [!DNL Microsoft Advertising]  rekeningen.
exl-id: 4970ac33-4978-4768-8701-6fdd3252bbd1
feature: Search Tracking
source-git-commit: 70629247a18a78b12a7fc8b166a0272764bb20b8
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# Opmaak voor het bijhouden van klikken voor [!DNL Microsoft Advertising]

Hieronder vindt u de sjabloon voor het bijhouden van de basis en de achtervoegsels van de bestemmingspagina (laatste URL-achtervoegsel) die u nodig hebt voor Zoeken, Sociaal en Commerce [!DNL Microsoft Advertising] .

## Sjabloonindelingen bijhouden

### Zoeken en publieksnetwerken (behalve voor sitelinks)

De volgende indeling is van toepassing op alle trackable advertentietypen op zoek- en publieksnetwerken.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Voorbeeld:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder in Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als tokendoorgeven is uitgeschakeld, vervangt u `cq?` after `<advertiser_ID>` with `c?` .
>
>* `{TargetId}` vertegenwoordigt identiteitskaart van a) of het sleutelwoord of b) het sleutelwoord en remarketing lijst (publiek) die de advertentie teweegbracht (bijvoorbeeld, &quot;kwd-123:aud-456&quot;voor zowel een sleutelwoord als een remarketing lijst of &quot;kwd-123&quot;voor slechts sleutelwoord).

### Sitelinks

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

Voorbeeld:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder in Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als tokendoorgeven is uitgeschakeld, vervangt u `cq?` after `<advertiser_ID>` with `c?` .
>
>* `{TargetId}` vertegenwoordigt identiteitskaart van a) of het sleutelwoord of b) het sleutelwoord en remarketing lijst (publiek) die de advertentie teweegbracht (bijvoorbeeld, &quot;kwd-123:aud-456&quot;voor zowel een sleutelwoord als een remarketing lijst of &quot;kwd-123&quot;voor slechts sleutelwoord).
>
>* `{adextensionid}` wordt niet gebruikt.
>
>* (Sitelinks) U kunt zien welke omzettingen het resultaat zijn van een klik op een sitelink door een [!UICONTROL Transaction Report] te genereren. De kolomwaarde [!UICONTROL Link Type] voor een sitelink is `sl:<Sitelink text>` , zoals `sl:See Current Offers` .

### Winkelnetwerk

De volgende formaten zijn van toepassing voor het winkelen van advertenties in het winkelen netwerken. U kunt een sjabloon voor bijhouden opgeven op account-, campagne-, groep- of productgroepniveau.

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

Voorbeeld:

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder in Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als tokendoorgeven is uitgeschakeld, vervangt u `cq?` after `<advertiser_ID>` with `c?` .
>
>* `{TargetId}` vertegenwoordigt identiteitskaart van a) of het sleutelwoord of b) het sleutelwoord en remarketing lijst (publiek) die de advertentie teweegbracht (bijvoorbeeld, &quot;kwd-123:aud-456&quot;voor zowel een sleutelwoord als een remarketing lijst of &quot;kwd-123&quot;voor slechts sleutelwoord).
>
>* (Optioneel) In plaats van volgsjablonen in te voeren op account-, campagne-, groep- of productgroepniveau, kunt u de URL voor het bijhouden van de gegevens toevoegen aan de productgegevens in de [!DNL Microsoft Merchant Center] -account. Om dit te doen, omvat het volgen URL, samen met de waarde op &quot;`link`&quot; of &quot;`mobile_link`&quot;gebied, zoals aangewezen, in een douanekolom &quot;[ bingads_redirect ](https://help.bingads.microsoft.com/#apex/3/en/51084/0)&quot;binnen de productvoer. De waarde op het &quot;`bingads_redirect`&quot;gebied vervangt de waarden op &quot;`link`&quot; en &quot;`mobile_link`&quot;gebieden. URL&#39;s die met deze methode worden gegenereerd, bevatten geen volgparameters die zijn opgegeven in de instellingen voor Zoeken, Sociaal zoeken en Commerce.

## Opmaak voor het achtervoegsel van de landingspagina (laatste URL-achtervoegsel)

>[!NOTE]
>
>Achtervoegsels op lagere niveaus van de bestemmingspagina hebben voorrang op het achtervoegsel op accountniveau. Gebruik voor een eenvoudiger onderhoud alleen het achtervoegsel op accountniveau, tenzij het bijhouden van wijzigingen voor afzonderlijke accountcomponenten nodig is. Om een achtervoegsel op het niveau van de advertentiegroep of lager te vormen, gebruik de redacteur van het advertentienetwerk.

### Zoeken en publieksnetwerken

Accounts die gebruikmaken van het bijhouden van Adobe Advertising-conversies, moeten de klikidentificatie (`msclkid` for [!DNL Microsoft Advertising] ) van het advertentienetwerk opnemen in het achtervoegsel:

* Wanneer de adverteerder een Adobe Analytics-integratie heeft, moet het achtervoegsel het volgende bevatten:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}`

* Wanneer de adverteerder geen Adobe Analytics-integratie heeft, moet het achtervoegsel het volgende bevatten:

  `&ev_efid={msclkid}:G:s`

### Winkelnetwerk

Accounts die gebruikmaken van het bijhouden van Adobe Advertising-conversies, moeten de klikidentificatie (`msclkid` for [!DNL Microsoft Advertising] ) van het advertentienetwerk opnemen in het achtervoegsel:

* Wanneer de adverteerder een Adobe Analytics-integratie heeft, moet het achtervoegsel het volgende bevatten:

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`

* Wanneer de adverteerder geen Adobe Analytics-integratie heeft, moet het achtervoegsel het volgende bevatten:

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [ Ongeveer klik-volgende formaten URL voor de conversie het volgen dienst van Adobe Advertising ](formats-click-tracking-about.md)
>* [ formaten van identiteitskaart AMO ](/help/integrations/analytics/ids.md#amo-id-formats)
