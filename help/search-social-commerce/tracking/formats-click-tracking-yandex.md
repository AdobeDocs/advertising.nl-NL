---
title: Opmaak voor het bijhouden van klikken voor  [!DNL Yandex]
description: Leer over de klik-volgende formaten voor  [!DNL Yandex]  rekeningen.
exl-id: bcbd369b-b98d-491c-a921-58bf79e01744
feature: Search Tracking
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Opmaak voor het bijhouden van klikken op gesponsorde advertenties op [!DNL Yandex]

De volgende basis-bestemmings-URL-indeling is van toepassing op gesponsorde advertenties:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

Voorbeeld:

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` is een variabele voor de unieke id van de adverteerder in Adobe Advertising.
>
>* Deze indeling geeft aan dat tokendoorgeven is ingeschakeld voor de campagne (de standaardinstelling). Als tokendoorgeven is uitgeschakeld, vervangt u `cq?` after `<advertiser_ID>` with `c?` .
>
>* `<the landing page>` is een variabele die de URL op uw site vertegenwoordigt waarnaar eindgebruikers worden geleid.
>
>* `source_type` is het overeenkomende type.
>
>* `source` geeft aan of de advertentie is weergegeven op een site met zoekopdrachten of op inhoud.
>
>* `position` is het positienummer voor de advertentie in het blok. Voor niet-onderzoeksverkeer, is de waarde &quot;0.&quot;
>
>* `position_type` is het blok waarin de advertentie is weergegeven op [!DNL Yandex] . Mogelijke waarden: &quot;premium&quot; (bovenste blok), &quot;other&quot; (rechterblok) of &quot;none&quot; (niet-zoekverkeer).

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer klik-volgende formaten URL voor de conversie het volgen dienst van Adobe Advertising &#x200B;](formats-click-tracking-about.md)
>* [&#x200B; formaten van identiteitskaart AMO &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
