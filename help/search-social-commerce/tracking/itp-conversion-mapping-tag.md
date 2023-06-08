---
title: De omzettingstag voor Adobe-reclame
description: Leer over de op JavaScript-Gebaseerde omzettingstoewijzingstag voor ITP 2.2, die Adobe Advertising toestaat om een omzettingsgebeurtenis te volgen die op een pagina voorkomt die niet de landende pagina is.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---

# De conversietoewijzingstag voor JavaScript-Adobe-reclame

*Adverteerders met alleen het bijhouden van Adobe-advertenties*

Met de conversietoewijzingstag voor Adobe-advertenties op JavaScript-basis kunt u, wanneer deze wordt gebruikt in aanvulling op de conversietag voor Adobe Advertising JavaScript v2 of v3, Adobe-advertenties een conversiegebeurtenis bijhouden die plaatsvindt op een pagina die niet de landingspagina is. De ITP 2.2-oplossing slaat het cookie van een gebruiker lokaal op in een iFrame dat eigendom is van een adverteerder. De lokale opslag kan dan de koekjeswaarde van de klik stroomafwaarts aan de omzettingspagina voortzetten.

Gebruik de conversietoewijzingstag om ervoor te zorgen dat Adobe-advertenties alle conversies kunnen bijhouden die in Apple Safari- en Mozilla Firefox-browsers plaatsvinden, waardoor de persistentie van cookies van andere bedrijven wordt beperkt. <!-- For all requirements to track conversions from Safari, see "Track Conversions from Apple Safari Browsers." -->

De conversietoewijzingstag gebruiken:

1. [De conversietoewijzingstag implementeren](#deploy-conversion-mapping-tag).

1. Als uw organisatie meerdere organisaties-id&#39;s van de Adobe Experience Cloud Identity Service gebruikt (voorheen IMS Org ID&#39;s genoemd), dan [conversietags bijwerken](#update-conversion-tags) om de organisatie-id op te nemen.

1. [De implementatie van tags valideren](#validate-conversion-mapping).

## De JavaScript-conversietoewijzingstag implementeren voor ITP 2.2 {#deploy-conversion-mapping-tag}

>[!NOTE]
>
>Als u de conversietoewijzingstag JavaScript voor ITP 2.0 gebruikt, vervangt u de bestaande tag in alle conversiepagina&#39;s door een van de volgende tags.<!-- any other instructions, too? Point them to the other page on Track Conversions from Safari...." -->

* Als uw organisatie gebruikmaakt van één organisatie-id, die wordt gebruikt voor uw account Zoeken, Sociale zaken en Handel, gebruikt u de volgende tag:

   `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" userid="{AMO User ID}"></script>`

   waar u vervangt `{AMO User ID}` met de unieke gebruikersnaam voor je account voor Zoeken, Sociale Zaken en Handel.

* Als uw organisatie meerdere organisatie-id&#39;s gebruikt, gebruikt u de volgende tag:

   `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="{xxxxxx@AdobeOrg}" userid="{AMO User ID}"></script>`

   waarbij:

   * vervangt u de waarde `{xxxxxx@AdobeOrg}` met de organisatie-id waarvoor de conversies van de pagina worden bijgehouden. Gebruik dezelfde organisatie-id voor alle conversiepagina&#39;s.

   * vervangt u `{AMO User ID}` met de unieke gebruikersnaam voor je account voor Zoeken, Sociale Zaken en Handel.

* Als u een systeem voor tagbeheer gebruikt dat het toevoegen van `imsorgid` gebruikt in plaats daarvan de volgende code:

   *Als uw organisatie één organisatie-id gebruikt:

   ```
   <script>
   window.ad_cloud = window.ad_cloud || {};
   window.ad_cloud.userid = "{AMO User ID}"
   </script>
   <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
   ```

   waar u vervangt `{AMO User ID}` met de unieke gebruikersnaam voor je account voor Zoeken, Sociale Zaken en Handel.

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

      * vervangt u de waarde `{xxxxxx@AdobeOrg}` met de organisatie-id waarvoor de conversies van de pagina worden bijgehouden. Gebruik dezelfde organisatie-id voor alle conversiepagina&#39;s.

      * vervangt u `{AMO User ID}` met de unieke gebruikersnaam voor je account voor Zoeken, Sociale Zaken en Handel.

Als u de waarde van uw organisatie-id of uw gebruikersnaam voor Zoeken, Sociale en Handel niet kent, vraagt u de accountmanager van Adobe.

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

Voeg de tag toe aan elke pagina die een openingspagina kan zijn van een zoekklik (idealiter op alle pagina&#39;s, omdat de bestemmingspagina&#39;s na verloop van tijd kunnen veranderen). Deze moet worden geladen voordat de conversietag JavaScript v3-conversie voor advertenties wordt geplaatst.

Als het binnen een iframe- of containertag is geplaatst, dan:

* Het iframe moet zich op hetzelfde niveau bevinden als het domein op het hoogste niveau.

* De conversietoewijzingstag mag slechts één (1) niveau onder het domein op het hoogste niveau liggen.

## JavaScript-conversietags bijwerken {#update-conversion-tags}

Als uw organisatie meerdere organisatie-id&#39;s gebruikt, voegt u de organisatie-id waarvoor de conversies van een pagina worden bijgehouden, toe aan uw bestaande JavaScript-conversietags.

Als uw organisatie één organisatie-id gebruikt, is deze stap niet nodig.

### JavaScript V2-tags

Voeg de volgende tekenreeks toe aan het begin van de scripttag voor conversie:

`ef_imsorgid="{xxxxxx@AdobeOrg}";`

waar u de waarde vervangt `{xxxxxx@AdobeOrg}` met de organisatie-id waarvoor de conversies van de pagina worden bijgehouden.

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

Na `window.EF` wordt gedefinieerd, voegt u de volgende tekenreeks toe:

`window.EF.imsorgid = "{xxxxxx@AdobeOrg}";`

waar u de waarde vervangt `{xxxxxx@AdobeOrg}` met de organisatie-id waarvoor de conversies van de pagina worden bijgehouden.

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

Vraag het accountteam van uw Adobe om hulp bij het valideren van de conversietoewijzingstag en de reguliere conversietag (als u deze hebt bijgewerkt).
