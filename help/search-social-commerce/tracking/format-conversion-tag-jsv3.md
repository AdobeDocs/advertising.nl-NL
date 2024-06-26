---
title: Indeling van JavaScript-tags voor conversie bijhouden versie 3
description: Verwijs naar de indeling van JavaScript conversie tracking-tags versie 3.
exl-id: 9fc6bb15-d880-4353-a8c5-260b7932ab34
feature: Search Tracking
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Indeling van JavaScript-tags voor conversie bijhouden versie 3

De volgende indeling is voor sites die gebruikmaken van HTTPS. Voor sites die HTTP gebruiken, moeten de URL&#39;s beginnen met &quot;http&quot;.

>[!NOTE]
>
>Voor informatie over wanneer om Versie 2 tegenover Versie 3 te gebruiken, zie [Veelgestelde vragen over trackinglabels](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script type='text/javascript'>
    (function() {
        var f = function() {
              EF.init({ eventType: "transaction",
                        transactionProperties : "ev_property=<property name>&ev_transid=<transid>",
                        segment : "",
                        searchSegment : "",
                        sku : "",
                        userid : "ef-userid",
                        pixelHost : "pixel.everesttech.net"
                        
                        , allow3rdPartyPixels: 1});
              EF.main();
        };
        window.EF = window.EF || {};
        if (window.EF.main) {
            f();
            return;
        }
        window.EF.onloadCallbacks = window.EF.onloadCallbacks || [];
        window.EF.onloadCallbacks[window.EF.onloadCallbacks.length] = f;
        if (!window.EF.jsTagAdded) {
            var efjs = document.createElement('script'); efjs.type = 'text/javascript'; efjs.async = true;
            efjs.src = 'https://www.everestjs.net/static/st.v3.js';
            var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(efjs, s);
            window.EF.jsTagAdded=1;
        }
    })();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

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
>* [Opmaak van trackingtags voor afbeeldingsconversie](format-conversion-tag-image.md)
