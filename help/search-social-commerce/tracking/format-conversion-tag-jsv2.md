---
title: Formaat voor trackingtags voor JavaScript-conversie versie 2
description: Verwijs naar de indeling van JavaScript conversion tracking-tags versie 2.
exl-id: 75e96f97-a3f0-4f5b-8bbb-4b1e8986f01a
feature: Search Tracking
source-git-commit: dda4ff8e7538bc742caa50862575cb4e46a1371d
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Formaat voor trackingtags voor JavaScript-conversie versie 2

De volgende indeling is voor sites die gebruikmaken van HTTPS. Voor sites die HTTP gebruiken, moeten de URL&#39;s beginnen met &quot;http&quot;.

>[!NOTE]
>
>Voor informatie over wanneer om Versie 2 tegen Versie 3 te gebruiken, zie [ FAQs op het volgen markeringen ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
window.id5PartnerId=<ID5_PartnerID>
var ef_event_type="transaction";
var ef_transaction_properties = "ev_property name=<property name>&ev_transid=<transid>";
/*
 * Do not modify below this line
 */
var ef_segment = "";
var ef_search_segment = "";
var ef_userid="ef-userid";
var ef_pixel_host="pixel.everesttech.net";
var ef_fb_is_app = 0;
var ef_allow_3rd_party_pixels = 1;
effp();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property name=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

waarbij:

* `<ef-userid>` is een unieke, numerieke gebruikersnaam die door Search, Social &amp; Commerce aan de adverteerder wordt toegewezen.

* `<ID5_PartnerID>` is de ID5-partner-id van de organisatie die de organisatie ontvangt na ondertekening van een overeenkomst met [!DNL ID5] . Omvat deze variabele slechts wanneer de organisatie DSP gebruikt en [ douanesegmenten heeft die gebruikers bijhouden verbonden aan ID5 universele IDs ](/help/dsp/audiences/universal-ids.md).

* `<propertyname>` is de conversie naar track. Als u bijvoorbeeld een conversie bijhoudt die &#39;registratie&#39; wordt genoemd, bevat de tag de parameter `ev_registration=<registration>` en moet u de werkelijke inkomsten voor elke transactie (zoals `ev_registration=1` ) doorgeven. Wanneer meerdere eigenschappen worden bijgehouden, worden ze samengevoegd door een en-teken (`&`), zoals `ev_registration=<registration>&ev_sale=<sale>` (bijvoorbeeld `ev_registration=1&ev_sale=12.99` ). **Nota:** de bezitsnaam kan geen speciale karakters omvatten.

* `<transid>` is een unieke transactie-id (zoals een werkelijke bestelling-id) die de adverteerder genereert en doorgeeft om een transactie te identificeren. Het is inbegrepen slechts wanneer &quot;[!UICONTROL Include unique transaction IDs]&quot;optie wordt geselecteerd.

  Zoeken, Sociaal en Commerce gebruikt de transactie-id om dubbele transacties met dezelfde transactie-id en eigenschapswaarde te voorkomen. De transactie-id wordt opgenomen in de [!UICONTROL Transaction Report] , waarmee u gegevens kunt valideren in Adobe Advertising met de gegevens van de adverteerder. **Nota:** als de gegevens van de adverteerder geen unieke identiteitskaart per transactie omvatten, dan leidt het Onderzoek, Sociale, &amp; Commerce nog tot één gebaseerd op transactietijd.

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [ Ongeveer Adobe Advertising omzetting-volgende markeringen ](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [ produceer een markering van de Adobe Advertising omzetting ](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [ Veelgestelde vragen over omzetting en de het volgen markeringen van de paginamening ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [ Formaat van de conversie van JavaScript volgmerkversie 2 ](format-conversion-tag-jsv2.md)
>* [ Formaat van de conversie van JavaScript volgmerkversie 3 ](format-conversion-tag-jsv3.md)
>* [ Formaat van beeldomzetting volgende markeringen ](format-conversion-tag-image.md)
