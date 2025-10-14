---
title: De tag voor het omzetten van Adoben Advertising
description: Leer over de op JavaScript-Gebaseerde omzettingsafbeelding afbeelding voor ITP 2.2, die Adobe Advertising toestaat om een omzettingsgebeurtenis te volgen die op een pagina voorkomt die niet de landende pagina is.
exl-id: cbeaf3cd-f1ab-419d-bba8-58a1c8215352
feature: Search Tracking
source-git-commit: 2c755eaa01f5bc7606074bb0fc276901c21ef807
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# De Adobe Advertising JavaScript-omzettingstoewijzingstag

*Advertisers met slechts het volgen van de omzetting van de Adobe Advertising*

Met de conversietoewijzingstag op JavaScript-basis voor Adobe Advertising kunt u, wanneer deze wordt gebruikt in aanvulling op de trackingtag voor conversie van JavaScript v2 of v3, een conversiegebeurtenis bijhouden die plaatsvindt op een pagina die niet de landingspagina is. De ITP 2.2-oplossing slaat het cookie van een gebruiker lokaal op in een iFrame dat eigendom is van een adverteerder. De lokale opslag kan dan de koekjeswaarde van de klik stroomafwaarts aan de omzettingspagina voortzetten.

Gebruik de conversietoewijzingstag om ervoor te zorgen dat de Adobe Advertising alle omzettingen kan volgen die binnen de browsers van Apple Safari en Mozilla Firefox voorkomen, die de persistentie van eersteklas koekjes beperken. <!-- For all requirements to track conversions from Safari, see "Track Conversions from Apple Safari Browsers." -->

De conversietoewijzingstag gebruiken:

1. [&#x200B; stelt de markering van de omzettingsafbeelding &#x200B;](#deploy-conversion-mapping-tag) op.

1. Als uw organisatie veelvoudige de organisatie IDs van de Dienst van de Identiteit van Adobe Experience Cloud (vroeger genoemd IMS Org IDs) gebruikt, dan [&#x200B; werk uw omzettingsmarkeringen &#x200B;](#update-conversion-tags) bij om organisatieidentiteitskaart te omvatten.

1. [&#x200B; bevestigt de markeringsplaatsing &#x200B;](#validate-conversion-mapping).

## De JavaScript-omzettingstoewijzingstag voor ITP 2.2 implementeren {#deploy-conversion-mapping-tag}

>[!NOTE]
>
>Als u de de omzettingsafbeelding van JavaScript markering voor ITP 2.0 gebruikt, dan vervang de bestaande markering in alle omzettingspagina&#39;s met één van de volgende markeringen.<!-- any other instructions, too? Point them to the other page on Track Conversions from Safari...." -->

* Als uw organisatie gebruikmaakt van één organisatie-id, die wordt gebruikt voor uw account Zoeken, Sociaal en Commerce, gebruikt u de volgende tag:

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" userid="{AMO User ID}"></script>`

  waarbij u `{AMO User ID}` vervangt door de unieke gebruikersnaam voor uw account voor Zoeken, Sociaal en Commerce.

* Als uw organisatie meerdere organisatie-id&#39;s gebruikt, gebruikt u de volgende tag:

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="{xxxxxx@AdobeOrg}" userid="{AMO User ID}"></script>`

  waarbij:

   * U vervangt de waarde `{xxxxxx@AdobeOrg}` door de organisatie-id waarvoor de conversies van de pagina worden bijgehouden. Gebruik dezelfde organisatie-id voor alle conversiepagina&#39;s.

   * vervangt u `{AMO User ID}` door de unieke gebruikersnaam voor uw account voor Zoeken, Sociaal en Commerce.

* Als u een systeem voor tagbeheer gebruikt dat het toevoegen van de variabele `imsorgid` aan de scripttag niet ondersteunt, gebruikt u in plaats daarvan de volgende code:

  *Als uw organisatie één organisatie-id gebruikt:

  ```
  <script>
  window.ad_cloud = window.ad_cloud || {};
  window.ad_cloud.userid = "{AMO User ID}"
  </script>
  <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
  ```

  waarbij u `{AMO User ID}` vervangt door de unieke gebruikersnaam voor uw account voor Zoeken, Sociaal en Commerce.

   * Als uw organisatie meerdere organisatie-id&#39;s gebruikt:

     ```
     <script>
     window.ad_cloud = window.ad_cloud || {};
     window.ad_cloud.imsorgid = "{xxxxxx@AdobeOrg}"
     window.ad_cloud.userid = "{AMO User ID}"
     </script>
     <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
     ```

     waarbij:

      * U vervangt de waarde `{xxxxxx@AdobeOrg}` door de organisatie-id waarvoor de conversies van de pagina worden bijgehouden. Gebruik dezelfde organisatie-id voor alle conversiepagina&#39;s.

      * vervangt u `{AMO User ID}` door de unieke gebruikersnaam voor uw account voor Zoeken, Sociaal en Commerce.

Als u de waarde van uw organisatie-id of uw gebruikersnaam voor Zoeken, Sociaal en Commerce niet kent, vraagt u het accountteam van de Adobe.

### Voorbeelden

```
<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="abc12345@AdobeOrg" userid="99999"></script>`
```

```
<script>
window.ad_cloud = window.ad_cloud || {};
window.ad_cloud.imsorgid = "abc12345@AdobeOrg"
window.ad_cloud.userid = "99999"
</script>
<script src="//www.everestjs.net/static/amo-conversion-mapper.js"></script>
```

### Waar moet de tag worden toegevoegd?

Voeg de tag toe aan elke pagina die een openingspagina kan zijn van een zoekklik (idealiter op alle pagina&#39;s, omdat de bestemmingspagina&#39;s na verloop van tijd kunnen veranderen). Deze moet worden geladen voordat de conversietag JavaScript v3 wordt Adobe Advertising.

Als het binnen een iframe- of containertag is geplaatst, dan:

* Het iframe moet zich op hetzelfde niveau bevinden als het domein op het hoogste niveau.

* De conversietoewijzingstag mag slechts één (1) niveau onder het domein op het hoogste niveau liggen.

## JavaScript-conversietags bijwerken {#update-conversion-tags}

Als uw organisatie meerdere organisatie-id&#39;s gebruikt, voegt u de organisatie-id waarvoor de conversies van een pagina worden bijgehouden, toe aan uw bestaande JavaScript-conversietags.

Als uw organisatie één organisatie-id gebruikt, is deze stap niet nodig.

### JavaScript V2-tags

Voeg de volgende tekenreeks toe aan het begin van de scripttag voor conversie:

`ef_imsorgid="{xxxxxx@AdobeOrg}";`

waarbij u de waarde `{xxxxxx@AdobeOrg}` vervangt door de organisatie-id waarvoor de conversies van de pagina worden bijgehouden.

Voorbeeld:

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
ef_imsorgid = "abc12345@AdobeOrg";
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

### JavaScript V3-tags

Voeg de volgende tekenreeks toe nadat `window.EF` is gedefinieerd:

`window.EF.imsorgid = "{xxxxxx@AdobeOrg}";`

waarbij u de waarde `{xxxxxx@AdobeOrg}` vervangt door de organisatie-id waarvoor de conversies van de pagina worden bijgehouden.

Voorbeeld:

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
        window.EF.imsorgid ="abc12345@AdobeOrg";
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

## De implementatie van tags valideren {#validate-conversion-mapping}

Vraag het accountteam van de Adobe om hulp bij het valideren van de conversietoewijzingstag en de reguliere conversietag (als u deze hebt bijgewerkt).
