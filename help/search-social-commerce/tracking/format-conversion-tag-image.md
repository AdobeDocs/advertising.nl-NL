---
title: Opmaak van trackingtags voor afbeeldingsconversie
description: Verwijs naar de indeling van de volgende tags voor afbeeldingsomzetting.
exl-id: e23107e1-b719-4572-a471-13e51387465d
feature: Search Tracking
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Opmaak van trackingtags voor afbeeldingsconversie

>[!NOTE]
>
>Zie voor meer informatie over wanneer u afbeeldingstags en JavaScript-tags wilt gebruiken de [Veelgestelde vragen over trackinglabels](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

* Niet-beveiligde tags voor sites met HTTP:

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* Beveiligde tags voor sites met HTTPS:

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

waarbij:

* `<ef-userid>` is een unieke, numerieke gebruikersnaam die door Search, Social &amp; Commerce aan de adverteerder wordt toegewezen.

* `<propertyname>` is de conversie naar track. Als u bijvoorbeeld een conversie bijhoudt met de naam &quot;registratie&quot;, bevat de tag de parameter `ev_registration=<registration>`, en u zou de daadwerkelijke opbrengst voor elke transactie (zoals `ev_registration=1`). Wanneer de veelvoudige eigenschappen worden gevolgd, worden zij aangesloten bij door ampersand (`&`), zoals `ev_registration=<registration>&ev_sale=<sale>` (bijvoorbeeld `ev_registration=1&ev_sale=12.99`). **Opmerking:**  De eigenschapsnaam mag geen speciale tekens bevatten.

* `<transid>` is een unieke transactie-id (zoals een werkelijke bestelling-id) die de adverteerder genereert en doorgeeft om een transactie te identificeren. Het is alleen opgenomen als &quot;[!UICONTROL Include unique transaction IDs]&quot; is geselecteerd.

  Zoeken, Sociaal en Commerce gebruikt de transactie-id om dubbele transacties met dezelfde transactie-id en eigenschapswaarde te voorkomen. De transactie-id is opgenomen in de [!UICONTROL Transaction Report], waarmee u gegevens kunt valideren in Adobe Advertising met de gegevens van de adverteerder. **Opmerking:** Als de gegevens van de adverteerder geen unieke id per transactie bevatten, wordt met Zoeken, Sociaal en Commerce nog steeds een id gegenereerd op basis van de transactietijd.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Tags voor conversie naar Adobe Advertising bijhouden](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Een conversietag voor Adoben Advertising genereren](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Veelgestelde vragen over tags voor conversie en bijhouden van paginaweergaven](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Indeling van JavaScript-tags voor bijhouden van conversie versie 2](format-conversion-tag-jsv2.md)
>* [Indeling van JavaScript-tags voor conversie bijhouden versie 3](format-conversion-tag-jsv3.md)
