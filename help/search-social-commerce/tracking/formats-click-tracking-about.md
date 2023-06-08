---
title: Over het bijhouden van klikken op URL-indelingen voor de service voor het bijhouden van Adobe-advertenties
description: Meer informatie over de indelingen voor het bijhouden van klikken voor ondersteunde advertentienetwerken.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# Over het bijhouden van klikken op URL-indelingen voor de service voor het bijhouden van Adobe-advertenties

De volgende sjablonen, achtervoegsels bij de landingspagina (laatste URL-achtervoegsels) en doel-URL&#39;s voor advertentieraccounts en campagnes die gebruikmaken van de service voor het bijhouden van Adobe-advertentieconversies hebben de volgende indeling:

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

waarbij:

* `http://pixel.everesttech.net` leidt de gebruiker naar de Adobe Advertising pixelservers.

* `<advertiser_ID>` is een variabele voor de unieke gebruikers-id die aan de adverteerder is toegewezen in Adobe Advertising.

* `<token passing parameter>` is een variabele voor één van het volgende:

   * `cq?` of `rq` geeft aan dat tokendoorgeven is ingeschakeld.

   * `c?` of `r` geeft aan dat tokendoorgeven is uitgeschakeld.

* `<ad network ID>` is een variabele voor numerieke identiteitskaart voor het gespecificeerde ad netwerk, zoals *3* for [!DNL Google Ads], *10* for [!DNL Microsoft Advertising], *45* for [!DNL Meta], *86* for [!DNL Yahoo! Display Network], *87* for [!DNL Naver], *88* for [!DNL Baidu], *90* for [!DNL Yandex], *94* for [!DNL Yahoo! Japan Ads], *105* for [!DNL Yahoo Native] (afgekeurd), of *106* for [!DNL Pinterest] (afgekeurd).

* `<tracking ID>` is een variabele voor een door het systeem gegenereerde id-tekenreeks die een trefwoord, advertentie of plaatsing identificeert die uniek is in de account. De tekenreeks varieert per advertentienetwerk.

* `<the landing page>` is een variabele die de URL op uw site vertegenwoordigt waarnaar eindgebruikers worden geleid. Voor accounts met doel-URL&#39;s is deze waarde een URL. Voor accounts met trackingsjablonen is deze waarde een parameter (zoals `{lpurl}`) die de laatste URL vertegenwoordigt.

Zie de afzonderlijke pagina&#39;s die de [[!DNL Baidu] formaten](formats-click-tracking-baidu.md), [[!DNL Google Ads] formaten](formats-click-tracking-google.md), [[!DNL Microsoft Advertising] formaten](formats-click-tracking-microsoft.md), [[!DNL Naver] formaten](formats-click-tracking-naver.md), [[!DNL Yahoo! Display Network] formaten](formats-click-tracking-yahoo-display-network.md), [[!DNL Yahoo! Japan Ads] formaten](formats-click-tracking-yahoo-japan.md), en [[!DNL Yandex] formaten](formats-click-tracking-yandex.md).

>[!MORELIKETHIS]
>
>* [Opmaak voor het bijhouden van klikken voor gesponsorde advertenties op [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [Opmaak voor het bijhouden van klikken voor [!DNL Google Ads]](formats-click-tracking-google.md)
>* [Opmaak voor het bijhouden van klikken voor [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [Opmaak voor het bijhouden van klikken voor gesponsorde advertenties op [!DNL Naver]](formats-click-tracking-naver.md)
>* [Opmaak voor het bijhouden van klikken voor gesponsorde advertenties op [!DNL Yahoo! Japan Ads]](formats-click-tracking-yahoo-japan.md)
>* [Opmaak voor het bijhouden van klikken voor gesponsorde advertenties op [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)
>* [Opmaak voor het bijhouden van klikken voor gesponsorde advertenties op [!DNL Yandex]](formats-click-tracking-yandex.md)

