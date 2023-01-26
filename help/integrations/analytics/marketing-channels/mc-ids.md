---
title: Adobe-advertentie-id's gebruiken om te maken [!DNL Marketing Channels] Regels
description: Leer hoe u met Adobe-advertentie-id's verwerkingsregels maakt voor [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 4fcdd586-e9c5-4405-a6dc-7799d2bac93e
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Adobe-advertentie-id&#39;s gebruiken om te maken [!DNL Marketing Channels] Verwerkingsregels

*Adverteerders met een Adobe Advertising-Adobe Analytics Integration Only*

Je kunt Adobe-advertentie-id&#39;s gebruiken ([AMO-id en EF-id](../ids.md)) om te configureren [!DNL Marketing Channels] verwerkingsvoorschriften in Adobe Analytics. Gebruik Adobe-advertentie-id&#39;s voor specifieke regels voor uw reclamecampagnes voor Adobe.

## De AMO-id in verwerkingsregels

De AMO-id is de primaire trackingcode die wordt gebruikt voor het rapporteren van Adobe-advertentiegegevens binnen [!DNL Analytics]. De AMO-id is een aaneenschakeling van dynamische waarden die door Adobe worden beheerd voor korrelige rapportage binnen [!DNL Analytics]. Het is opgeslagen in een [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) of de rVar dimensie (AMO ID). De AMO-id kan worden ingesteld in [!DNL Analytics] op twee manieren :

* Doorklikken: Adobe Advertising stelt de `s_kwcid` querytekenreeksparameter in een koppeling, en [!DNL Analytics] haalt de parameter van de bestemmingspagina URL op wanneer een klik-door voorkomt.
* Doorzicht ([!DNL DSP] Alleen): De laatste gebeurtenisservice detecteert een weergave aan de serverzijde en verzendt de AMO-id naar [!DNL Analytics]. In dit geval bevat de URL geen `s_kwcid` parameter.

De dynamische waarden binnen AMO-id&#39;s geven het marketingkanaal aan dat is bijgehouden:

* Het voorvoegsel in de AMO-id kan worden gebruikt om het kanaal op hoofdniveau binnen [!DNL Marketing Channels].

* Tekenzinnen in de hoofdtekst van de AMO-id geven een specifieker campagneretype aan.

* Het achtervoegsel &quot;vt&quot; is aanwezig voor [!DNL DSP] mening-door verkeer en kan worden gebruikt om afzonderlijke klik-door en mening-door te creëren [!DNL DSP] kanalen.

De rest van de AMO-id kan worden genegeerd.

| AMO-id | Kanaal | Regellogica |
|--------|---------|--------------------|
| AL! (voorvoegsel) | [!UICONTROL Paid Search] | Begint met |
| AC! (voorvoegsel) | [!UICONTROL DSP] | Begint met |
| !g! (body) | [!UICONTROL Google Search] | Bevat |
| !s! (body) | [!UICONTROL Search Partner] | Bevat |
| !d! (body) | [!UICONTROL Display Network] | Bevat |
| !u! (body) | [!UICONTROL Smart Shopping Campaign] | Bevat |
| !ytv! (body) | [!UICONTROL YouTube Video Ad] | Bevat |
| !yts! (body) | [!UICONTROL YouTube Search Ad] | Bevat |
| !vp! (body) | [!UICONTROL Google Video Partners] | Bevat |
| !vt (achtervoegsel) | [!UICONTROL DSP View-through] | Eindigt met |

### Voorbeelden van verwerkingsregels die de AMO-id gebruiken

De [!DNL Marketing Channels] verwerkingsregel voor de [!UICONTROL Paid Search] het kanaal kan er als volgt uitzien:

![Voorbeeld van een [!UICONTROL Paid Search] regel](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

De [!DNL Marketing Channels] verwerkingsregel voor de [!UICONTROL YouTube Video Ads] het kanaal kan er als volgt uitzien:

![Voorbeeld van een [!UICONTROL YouTube Video Ads] regel](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Ben zeker om uw regels in volgorde van specificiteit in werking te stellen. Indien de twee bovenstaande regels in orde zijn, [!DNL YouTube] video en verkeer zouden onder [!UICONTROL Paid Search] kanaal omdat de AMO-id beide zou beginnen met &quot;AL!&quot; en bevatten &quot;!ytv!&quot;.

## EF-id in verwerkingsregels

De EF-id van AMO (EF-ID) is de tweede trackingcode die wordt gebruikt in de [!DNL Analytics for Advertising] integratie. Het hoofddoel is het volgen en passeren [!DNL Analytics] gebeurtenisgegevens naar Adobe Advertising. Telkens wanneer een klik-door of een mening-door voorkomt, wordt een unieke EF identiteitskaart geproduceerd, zelfs als het de nauwkeurige zelfde advertentie voor de zelfde bezoeker is. De EF-id wordt niet gebruikt in de [!DNL Analytics] het melden van gebruikersinterface omdat het typisch de 500k unieke waarden per veranderlijke grens in overschrijdt [!DNL Analytics], waardoor het onbruikbaar wordt voor rapportage. De Adobe-gegevens en metagegevens voor reclame worden niet op de EF-id toegepast; ze worden alleen toegepast op de AMO-id. De toegevoegde granulariteit van het volgen is vereist voor campagtimalisatie in Adobe Advertising, zodat beide id&#39;s vereist zijn.

Hoewel de EF-id-dimensie niet rechtstreeks wordt gebruikt in [!DNL Analytics] de EF-id kan nuttig zijn voor het maken van marketingkanalen. Het EF-id-achtervoegsel geeft het kanaal (weergave of zoekopdracht) aan en geeft aan of het bezoek is aangestuurd door een doorklik of een doorzicht. Het scheidingsteken in de EF-id is een dubbele punt in plaats van het uitroepteken in de AMO-id.

| Achtervoegsel EF-ID | Kanaal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Voorbeelden van verwerkingsregels die gebruikmaken van de EF-id

#### Doorklikregel weergeven

Maak een marketingkanaal Doorklikken weergeven door alleen doorklikbewerkingen vast te leggen. Omdat de identiteitskaart van AMO voor zowel klik-door als mening-door het zelfde is, gebruikt deze regel de EF veranderlijke identiteitskaart en `ef_id` querytekenreeksparameter.

Soms worden doorklikkingen gevolgd door URL (het gebrek). In andere gevallen worden doorklikbewerkingen bijgehouden via de laatste gebeurtenisservice aan de serverzijde. De URL bevat daarom niet de `ef_id` parameter. De regel controleert daarom op voorwaarden waarin de EF-ID-variabele of de `ef_id` parameter querytekenreeks eindigt met &quot;:d&quot;. Gebruik de &quot;`Any`&quot;, omdat u deze regel voor een van beide voorwaarden wilt activeren.

![Voorbeeld van een klikregel voor weergave](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Weergave-through-regel

Maak een regel waarin de EF-id eindigt met &quot;:i&quot; om een weergavedoorvoerkanaal te maken. Omdat de bezoeker niet op de advertentie heeft geklikt, bevat de doorkijktracking geen `ef_id` of `s_kwcid` in de URL, zodat de regel slechts één voorwaarde vereist.

![Voorbeeld van een weergaveregel](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Grondbeginselen van [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Waarom kanaalgegevens kunnen verschillen tussen Adobe-reclame en [!DNL Marketing Channels]](mc-data-variances.md)
>* [Gebruiken [!DNL Analytics Marketing Channels] met Adobe-advertentiegegevens](mc-ac-data.md)
>* [Video: Gebruiken [!DNL Marketing Channels] voor Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Adobe advertentie-id&#39;s gebruikt door [!DNL Analytics]](/help/integrations/analytics/ids.md)

