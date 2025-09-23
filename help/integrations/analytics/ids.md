---
title: Adobe Advertising-id's gebruikt door  [!DNL Analytics]
description: Adobe Advertising-id's gebruikt door  [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 0cf325946fdc3852b8b94acb29678bf6c47227a0
workflow-type: tm+mt
source-wordcount: '1122'
ht-degree: 0%

---

# Adobe Advertising-id&#39;s gebruikt door [!DNL Analytics]

*Advertisers met slechts een integratie Adobe Advertising-Adobe Analytics*

*Van toepassing op Advertising DSP en[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertising gebruikt twee IDs voor prestaties het volgen ter plaatse: *EF identiteitskaart* en *identiteitskaart van AMO*.

Wanneer een advertentie-impositie optreedt, maakt Adobe Advertising de waarden voor de AMO-id en EF-id en slaat het deze op. Wanneer een bezoeker die een advertentie heeft gezien de site betreedt zonder op een advertentie te klikken, roept [!DNL Analytics] deze waarden aan vanuit Adobe Advertising via de [!DNL Analytics for Advertising] JavaScript-code. Voor doorkijkverkeer genereert [!DNL Analytics] een aanvullende id (`SDID` ) die wordt gebruikt om de EF-id en AMO-id aan te sluiten in [!DNL Analytics] . Voor doorklikverkeer worden deze id&#39;s opgenomen in de URL van de bestemmingspagina met behulp van de parameters `ef_id` en `s_kwcid` (voor de AMO ID) van de queryreeks.

Adobe Advertising maakt een onderscheid tussen een doorklikitem of een doorkijkitem op de website aan de hand van de volgende criteria:

* Een view-through ingang wordt gevangen wanneer een gebruiker de plaats na het bekijken van een advertentie bezoekt maar niet het klikt. [!DNL Analytics] registreert een mening-door als twee voorwaarden worden voldaan:

   * De bezoeker heeft geen klik-door voor a [!DNL DSP] of [!DNL Search, Social, & Commerce] en tijdens [ klikt raadplegingsvenster ](/help/integrations/analytics/prerequisites.md#lookback-a4adc).

   * De bezoeker heeft minstens één [!DNL DSP] en tijdens het [ venster van de imkerraadpleging ](/help/integrations/analytics/prerequisites.md#lookback-a4adc) gezien. De laatste indruk wordt doorgegeven als de doorkijkhoek.

* Een doorklikitem wordt vastgelegd wanneer een sitebezoeker op een advertentie klikt voordat hij de site betreedt. [!DNL Analytics] legt een doorklikken vast wanneer een van de volgende omstandigheden zich voordoet:

   * De URL bevat een EF-id en een AMO-id die Adobe Advertising aan de URL van de bestemmingspagina heeft toegevoegd.

   * De URL bevat geen volgcodes, maar de Adobe Advertising JavaScript-code detecteert een klik binnen de laatste twee minuten.

![ op mening-gebaseerde Adobe Advertising [!DNL Analytics] integratie ](/help/integrations/assets/a4adc-view-through-process.png)

*Figuur 1: Op mening-gebaseerde Adobe Advertising [!DNL Analytics] integratie*

![ Adobe Advertising klikt op URL-Gebaseerde [!DNL Analytics] integratie ](/help/integrations/assets/a4adc-click-through-process.png)

*Figuur 2: Adobe Advertising klikt op URL-Gebaseerde [!DNL Analytics] integratie*

## Adobe Advertising EF-id&#39;s

De EF-id is een unieke token die Adobe Advertising gebruikt om activiteit te koppelen aan een online klik of belichting op het niveau van de afzonderlijke browser of het apparaat. EF-id&#39;s fungeren voornamelijk als sleutels voor het verzenden van [!DNL Analytics] -gegevens en Customer Journey Analytics-gegevens naar Adobe Advertising voor het melden en optimaliseren van biedingen binnen Adobe Advertising.

Voor [!DNL Analytics], wordt EF identiteitskaart opgeslagen in [ an  [!DNL Analytics] [!DNL eVar] ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) of [!DNL rVar] (gereserveerde [!DNL eVar]) dimensie (Adobe Advertising EF identiteitskaart).

Voor Customer Journey Analytics, wordt EF identiteitskaart opgeslagen in het `trackingIdentities` bezit van het `conversionDetails` voorwerp, dat deel van [ uitmaakt [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension] ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension).

### EF-ID-indelingen {#ef-id-formats}

>[!NOTE]
>
>EF-id&#39;s zijn hoofdlettergevoelig. Als een [!DNL Analytics] - of Customer Journey Analytics-implementatie URL-tracking in kleine letters forceert, herkent Adobe Advertising de EF-id niet. Dit is van invloed op Adobe Advertising-biedingen en -rapporten, maar heeft geen invloed op Adobe Advertising-rapportage binnen [!DNL Analytics] of Customer Journey Analytics.

#### [!DNL Google Ads] zoekopdrachten

```
{gclid}:G:s
```

waarbij:

* `gclid` is de [!DNL Google Click ID] (GCLID).
* `s` is het netwerktype (&quot;s&quot; voor onderzoek).

#### [!DNL Microsoft Advertising] zoekopdrachten

```
{msclkid}:G:s
```

waarbij:

* `msclkid` is de [!DNL Microsoft Click ID] (MSCLKID).
* `s` is het netwerktype (&quot;s&quot; voor onderzoek).

#### Advertenties en zoekadvertenties weergeven op andere zoekmachines

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

waarbij:

* &lt;*identiteitskaart van de bezoeker van Adobe Advertising*> is een unieke identiteitskaart per bezoeker (zoals UWKVaAABCkJ0mDt). Ook geroepen *surfer identiteitskaart*.

* &lt;*timestamp*> is de tijd in formaat YYYMMDDHHMMSS (zoals 20190821192533 voor Jaar 2019, Maand 08, Dag 21, Tijd 19 :25: 33).

* &lt;*kanaaltype*> is het kanaaltype verantwoordelijk voor de klik of de blootstelling:

   * `d` voor een klik op een DSP-advertentie (klik-via tonen)
   * `i` voor een indruk van een DSP-advertentie (display view-through)
   * `s` voor een klik op een zoekadvertentie (doorzoekklik).

Voorbeeld `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### De EF-id Dimension in [!DNL Analytics]

In [!DNL Analytics] -rapporten kunt u EF-id-gegevens vinden door te zoeken naar de [!UICONTROL EF ID] -dimensie en de [!UICONTROL EF ID Instance] -metrische waarde te gebruiken.

Voor EF-id&#39;s geldt de limiet van 500 kB voor unieke identificatiekenmerken in Analysis Workspace. Zodra de waarde 500k wordt bereikt, worden alle nieuwe volgcodes gemeld onder de één-lijn-punt titel &quot;[!UICONTROL Low Traffic]&quot;. Vanwege de mogelijkheid dat rapportprecisie ontbreekt, worden de EF-id&#39;s niet geclassificeerd en mag u deze niet gebruiken voor segmenten of voor rapportage in [!DNL Analytics] .

<!-- ## Adobe Advertising AMO IDs {#amo-id} -->

{{$include /help/_includes/amo-id.md}}

### Manieren om de AMO-id te implementeren {#amo-id-implement}

De parameter wordt op een van de volgende manieren toegevoegd aan de URL&#39;s die worden gevolgd:

* (Aanbevolen) Wanneer de invoegfunctie op de server is geïmplementeerd.

   * DSP-klanten: de pixelserver voegt automatisch de parameter s_kwcid toe aan de achtervoegsels van de bestemmingspagina wanneer een eindgebruiker een weergaveadvertentie met de Adobe Advertising-pixel weergeeft.

   * Zoek-, sociale en Commerce-klanten:

      * Voor [!DNL Google Ads] - en [!DNL Microsoft Advertising] -accounts waarvoor de [!UICONTROL Auto Upload] -instelling is ingeschakeld voor de account of campagne, voegt de pixelserver automatisch de parameter s_kwcid toe aan de achtervoegsels van de bestemmingspagina wanneer een eindgebruiker op een advertentie met de Adobe Advertising-pixel klikt.

      * Voor andere advertentienetwerken, of [!DNL Google Ads] en [!DNL Microsoft Advertising] rekeningen met [!UICONTROL Auto Upload] gehandicapten plaatsen, voeg manueel de parameter aan uw [ rekening-niveau parameters ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} toe, die het aan uw basis URLs toevoegen.

* Wanneer de invoegfunctie op de server niet is geïmplementeerd:

   * De klanten van DSP: De [ code van JavaScript ](javascript.md) registreert automatisch klik-door:gaan en mening-door. Wanneer een browser geen cookies van derden ondersteunt, kunt u nog steeds op klikken gebaseerde conversies bijhouden voor de volgende soorten advertenties:

      * Voor [!DNL Flashtalking] ad markeringen, neem manueel extra macro&#39;s per &quot;[ op voeg  [!DNL Analytics for Advertising]  Macro&#39;s aan  [!DNL Flashtalking]  toe - Markeringen ](/help/integrations/analytics/macros-flashtalking.md).&quot; **Nota:** Deze procedure is niet noodzakelijk als uw organisatie een direct partnerschap met [!DNL Flashtalking] heeft en u gegevens-pas macro&#39;s gebruikt om de `s_kwcid` en `ef_id` volgende parameters per de [!DNL Flashtalking] steundocumentatie bij [ https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros ](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros) te volgen.

      * Voor [!DNL Google Campaign Manager 360] ad markeringen, neem manueel extra macro&#39;s per &quot;[ op voeg  [!DNL Analytics for Advertising]  Macro&#39;s aan  [!DNL Google Campaign Manager 360]  toe - Markeringen ](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

   * Zoek-, sociale en Commerce-klanten:

      * Voor ([!DNL Google Ads] en [!DNL Microsoft Advertising]) advertenties, voeg manueel de parameter van identiteitskaart van AMO aan uw het landen paginaapara&#39;s toe, idealiter bij het [ rekeningsniveau ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} tenzij het verschillend volgen voor individuele rekeningscomponenten noodzakelijk is.

      * Voor advertenties op alle andere advertentienetwerken, voeg manueel de parameter van identiteitskaart AMO aan uw [ rekening-niveau parameters ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} toe, die het aan uw basis URLs toevoegen.

Neem contact op met uw Adobe-accountteam als u de invoegfunctie aan de serverzijde wilt implementeren of de beste optie voor uw bedrijf wilt bepalen.

### AMO ID Dimension in [!DNL Analytics]

In analyserapporten kunt u zoeken naar AMO-id-gegevens door te zoeken naar de [!UICONTROL AMO ID] -dimensie en de [!UICONTROL AMO ID Instances] -parameter te gebruiken. In de [!UICONTROL AMO ID] -dimensie worden alle vastgelegde AMO-id-waarden opgeslagen, terwijl de [!UICONTROL AMO ID Instances] -meting aangeeft hoe vaak een AMO-id-waarde door de site is vastgelegd. Als bijvoorbeeld vier keer op dezelfde zoekopdracht werd geklikt en Analytics zeven sittems bijhield, zou [!UICONTROL AMO ID Instances] zeven (7) zijn en [!UICONTROL Clicks] vier (4).

Voor elke rapportage of controle binnen [!DNL Analytics] kunt u het beste de AMO-id en de bijbehorende instantie gebruiken. Voor meer informatie, zie &quot;[ Klik-door de Bevestiging van Gegevens voor  [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot;in &quot;Verwachte Variaties van Gegevens tussen [!DNL Analytics] en Adobe Advertising.&quot;

## Informatie over analytische classificaties

In [!DNL Analytics], is de a [ classificatie ](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) een stuk van meta-gegevens voor een bepaalde het volgen code, zoals Rekening, Campagne, of Advertentie. Adobe Advertising categoriseert onbewerkte Adobe Advertising-gegevens aan de hand van classificaties, zodat u de gegevens op verschillende manieren kunt weergeven (bijvoorbeeld op Advertentietype of Campagne) wanneer u rapporten genereert. Classificaties vormen de basis voor Adobe Advertising-rapportage in [!DNL Analytics] en kunnen worden gebruikt met AMO-metriek, zoals [!UICONTROL Adobe Advertising Cost] , [!UICONTROL Adobe Advertising Impressions] en [!UICONTROL AMO Clicks] , en met aangepaste en standaard onsite gebeurtenissen zoals [!UICONTROL Visits] , [!UICONTROL Leads] , [!UICONTROL Orders] en [!UICONTROL Revenue] .

>[!MORELIKETHIS]
>
>* [ Overzicht van  [!DNL Analytics for Advertising]](overview.md)
>* [ Verwachte Variaties van Gegevens tussen  [!DNL Analytics]  en Adobe Advertising ](data-variances.md)
