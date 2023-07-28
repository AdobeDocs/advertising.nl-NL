---
title: Opmaak voor het bijhouden van klikken voor [!DNL Yandex]
description: Meer informatie over de indelingen voor klikken en bijhouden voor [!DNL Yandex] rekeningen.
exl-id: cf1d6c4b-9bcd-4b82-919f-c14dbaff9a76
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Opmaak voor het bijhouden van klikken voor gesponsorde advertenties op [!DNL Yandex]

De volgende basis-bestemmings-URL-indeling is van toepassing op gesponsorde advertenties:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

Voorbeeld:

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder binnen de Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als het doorgeven van token is uitgeschakeld, kunt u dit vervangen `cq?` na `<advertiser_ID>` with `c?`.
>
>* `<the landing page>` is een variabele die de URL op uw site vertegenwoordigt waarnaar eindgebruikers worden geleid.
>
>* `source_type`  is het overeenkomende type.
>
>* `source` is of de advertentie is weergegeven op een site met zoekopdrachten of op inhoud.
>
>* `position` is het positienummer voor de advertentie in het blok. Voor niet-onderzoeksverkeer, is de waarde &quot;0.&quot;
>
>* `position_type` is het blok waarin de advertentie is weergegeven [!DNL Yandex]. Mogelijke waarden: &quot;premium&quot; (bovenste blok), &quot;other&quot; (rechterblok) of &quot;none&quot; (niet-zoekverkeer).

>[!MORELIKETHIS]
>
>* [Over URL-indelingen voor het bijhouden van klikken voor de service Adobe Advertising converteren](formats-click-tracking-about.md)
>* [Opmaak voor de s\_kwcid-trackingcode](skwcid-tracking-parameter.md)
