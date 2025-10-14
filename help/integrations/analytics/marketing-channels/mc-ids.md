---
title: Gebruikend Adobe Advertising IDs om  [!DNL Marketing Channels]  Regels te creëren
description: Leer hoe te om Adobe Advertising IDs te gebruiken om verwerkingsregels voor  [!DNL Analytics Marketing Channels] tot stand te brengen.
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 96a0add168c7fb7a6d80cf1b81ef4b315fbba89f
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Adobe Advertising-id&#39;s gebruiken om [!DNL Marketing Channels] verwerkingsregels te maken

*Advertisers met Adobe Advertising-Adobe Analytics slechts Integratie*

U kunt Adobe Advertising IDs ([&#x200B; identiteitskaart van AMO en EF identiteitskaart &#x200B;](../ids.md)) gebruiken om [!DNL Marketing Channels] verwerkingsregels in Adobe Analytics te vormen. Gebruik Adobe Advertising-id&#39;s voor specifieke regels voor uw Adobe Advertising-campagnes.

## De AMO-id in verwerkingsregels

De AMO-id is de primaire trackingcode die wordt gebruikt om Adobe Advertising-gegevens binnen [!DNL Analytics] te rapporteren. De AMO-id is een aaneenschakeling van dynamische waarden die door Adobe worden beheerd voor korrelige rapportage binnen [!DNL Analytics] . Het wordt opgeslagen in een [!DNL Analytics] [&#x200B; eVar &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=nl-NL) of rVar dimensie (identiteitskaart van AMO). De AMO-id kan op twee manieren worden ingesteld in [!DNL Analytics] :

* Doorklikken: Adobe Advertising stelt de parameter van de `s_kwcid` querytekenreeks in een koppeling in en [!DNL Analytics] haalt de parameter op van de bestemmingspagina-URL wanneer een doorklikken plaatsvindt.
* Beeld-door het volgen ([!DNL DSP] slechts): De Laatste Dienst van de Gebeurtenis ontdekt een mening-door op de serverzijde en verzendt AMO identiteitskaart naar [!DNL Analytics]. In dit geval bevat de URL geen parameter `s_kwcid` .

De dynamische waarden binnen AMO-id&#39;s geven het marketingkanaal aan dat is bijgehouden:

* Het voorvoegsel in de AMO-id kan worden gebruikt om het kanaal op hoofdniveau binnen [!DNL Marketing Channels] te identificeren.

* Tekenzinnen in de hoofdtekst van de AMO-id geven een specifieker campagneretype aan.

* Het achtervoegsel &quot;vt&quot; is aanwezig voor [!DNL DSP] view-through-verkeer en kan worden gebruikt om afzonderlijke doorklikkanalen en doorkijkkanalen [!DNL DSP] te maken.

De rest van de AMO-id kan worden genegeerd.

| [!UICONTROL AMO ID] | Kanaal | Regellogica |
|--------|---------|--------------------|
| !ctv (achtervoegsel) | [!UICONTROL DSP Connected TV View-through] | Eindigt met |
| !d! (body) | [!UICONTROL Display Network] | Bevat |
| !g! (body) | [!UICONTROL Google Search] | Bevat |
| !s! (body) | [!UICONTROL Search Partner] | Bevat |
| !u! (body) | [!UICONTROL Smart Shopping Campaign] | Bevat |
| !ytv! (body) | [!UICONTROL YouTube Video Ad] | Bevat |
| !yts! (body) | [!UICONTROL YouTube Search Ad] | Bevat |
| !vp! (body) | [!UICONTROL Google Video Partners] | Bevat |
| !vt (achtervoegsel) | [!UICONTROL DSP View-through] | Eindigt met |
| AL! (voorvoegsel) | [!UICONTROL Paid Search] | Begint met |
| AC! (voorvoegsel) | [!UICONTROL DSP] | Begint met |

### Voorbeelden van verwerkingsregels die de AMO-id gebruiken

De [!DNL Marketing Channels] -verwerkingsregel voor het [!UICONTROL Paid Search] -kanaal ziet er als volgt uit:

![&#x200B; Voorbeeld van a [!UICONTROL Paid Search] regel &#x200B;](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

De [!DNL Marketing Channels] -verwerkingsregel voor het [!UICONTROL YouTube Video Ads] -kanaal ziet er als volgt uit:

![&#x200B; Voorbeeld van a [!UICONTROL YouTube Video Ads] regel &#x200B;](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Ben zeker om uw regels in volgorde van specificiteit in werking te stellen. Als de bovenstaande twee regels op volgorde stonden, zouden de video en het verkeer van [!DNL YouTube] allemaal onder het [!UICONTROL Paid Search] -kanaal vallen omdat de AMO-id beide zou beginnen met &quot;AL!&quot; en bevatten &quot;!ytv!&quot;.

## EF-id in verwerkingsregels

De EF-id (EF-id) van AMO is de tweede trackingcode die wordt gebruikt in de [!DNL Analytics for Advertising] -integratie. Het hoofddoel is het bijhouden en doorgeven van [!DNL Analytics] -gebeurtenisgegevens in Adobe Advertising. Telkens wanneer een klik-door of een mening-door voorkomt, wordt een unieke EF identiteitskaart geproduceerd, zelfs als het de nauwkeurige zelfde advertentie voor de zelfde bezoeker is. De EF-id wordt niet gebruikt in de gebruikersinterface van de [!DNL Analytics] -rapportage, omdat deze doorgaans de unieke waarden van 500 kB per variabele in [!DNL Analytics] overschrijdt, waardoor deze onbruikbaar wordt voor rapportage. De metriek en de meta-gegevens van de Adobe Advertising worden niet toegepast op EF identiteitskaart; zij worden toegepast slechts op AMO identiteitskaart De toegevoegde granulariteit van het volgen is vereist voor campagnetoepassing in Adobe Advertising, zodat worden allebei IDs vereist.

Hoewel de EF-id-dimensie niet rechtstreeks wordt gebruikt in [!DNL Analytics] -rapportage, kan de EF-id nuttig zijn bij het maken van marketingkanalen. Het EF-id-achtervoegsel geeft het kanaal (weergave of zoekopdracht) aan en geeft aan of het bezoek is aangestuurd door een doorklik of een doorzicht. Het scheidingsteken in de EF-id is een dubbele punt in plaats van het uitroepteken in de AMO-id.

| Achtervoegsel EF-ID | Kanaal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Voorbeelden van verwerkingsregels die gebruikmaken van de EF-id

#### Doorklikregel weergeven

Maak een marketingkanaal Doorklikken weergeven door alleen doorklikbewerkingen vast te leggen. Omdat AMO ID het zelfde voor zowel klik-door als mening-door is, gebruikt deze regel de EF variabele van identiteitskaart en de `ef_id` parameter van het vraagkoord.

Soms worden doorklikkingen gevolgd door URL (het gebrek). In andere gevallen worden doorklikbewerkingen bijgehouden via de laatste gebeurtenisservice aan de serverzijde en bevat de URL dus niet de parameter `ef_id` . De regel controleert daarom op voorwaarden waarin de EF ID-variabele of de `ef_id` query string parameter eindigt met &quot;:d&quot;. Gebruik &quot;`Any`&quot;exploitant omdat u deze regel voor één van beide voorwaarde wilt teweegbrengen.

![&#x200B; Voorbeeld van een vertoning klik-door regel &#x200B;](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Weergave-through-regel

Maak een regel waarin de EF-id eindigt met &quot;:i&quot; om een weergavedoorvoerkanaal te maken. Omdat de bezoeker niet op de advertentie heeft geklikt, bevat de doorkijkbewerking niet de `ef_id` of `s_kwcid` in de URL, zodat de regel slechts één voorwaarde vereist.

![&#x200B; Voorbeeld van een vertoning mening-door regel &#x200B;](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [&#x200B; Grondbeginselen van  [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [&#x200B; waarom de Gegevens van het Kanaal tussen Adobe Advertising en  [!DNL Marketing Channels]](mc-data-variances.md) kunnen variëren
>* [&#x200B; Gebruikend  [!DNL Analytics Marketing Channels]  met de Gegevens van de Adobe Advertising &#x200B;](mc-ac-data.md)
>* [&#x200B; Video: Gebruikend  [!DNL Marketing Channels]  voor Adobe Advertising die &#x200B;](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=nl-NL) meldt
>* [&#x200B; Adobe Advertising IDs die door  [!DNL Analytics]](/help/integrations/analytics/ids.md) wordt gebruikt
