---
title: Gebruikend Adobe Advertising IDs om  [!DNL Marketing Channels]  regels tot stand te brengen
description: Leer hoe te om Adobe Advertising IDs te gebruiken om verwerkingsregels voor  [!DNL Analytics Marketing Channels] tot stand te brengen.
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 0813a8bddc1ecf238f4a62c4fcefd8584f32e152
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# Adobe Advertising-id&#39;s gebruiken om [!DNL Marketing Channels] -verwerkingsregels te maken

*Advertisers met slechts een integratie Adobe Advertising-Adobe Analytics*

U kunt Adobe Advertising IDs ([ identiteitskaart van AMO en EF identiteitskaart ](../ids.md)) gebruiken om [!DNL Marketing Channels] verwerkingsregels in Adobe Analytics te vormen. Gebruik Adobe Advertising-id&#39;s voor specifieke regels voor Adobe Advertising-campagnes. De volgorde waarin u de regels verwerkt, bepaalt of alle mogelijke gegevens correct worden vastgelegd.

## De AMO-id in verwerkingsregels

De AMO-id is de primaire trackingcode die wordt gebruikt om Adobe Advertising-gegevens binnen [!DNL Analytics] te rapporteren. De AMO-id is een aaneenschakeling van dynamische waarden die door Adobe worden beheerd voor korrelige rapportage binnen [!DNL Analytics] . Het is opgeslagen in een [!DNL Analytics] [ eVar ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) of rVar dimensie (identiteitskaart van AMO). De AMO-id kan op twee manieren worden ingesteld in [!DNL Analytics] :

* Doorklikken: Adobe Advertising stelt de parameter voor de `s_kwcid` querytekenreeks in een koppeling in en [!DNL Analytics] haalt de parameter op via de URL van de bestemmingspagina wanneer er doorklikken plaatsvindt.

* Beeld-door het volgen ([!DNL DSP] slechts): [!DNL Last Event Service] ontdekt een mening-door op de serverzijde en verzendt AMO identiteitskaart naar [!DNL Analytics]. In dit geval bevat de URL geen parameter `s_kwcid` .

De dynamische waarden binnen AMO-id&#39;s geven het marketingkanaal aan dat is bijgehouden:

* Het voorvoegsel in de AMO-id kan worden gebruikt om het kanaal op hoofdniveau binnen [!DNL Marketing Channels] te identificeren.

* Tekenzinnen in de hoofdtekst van de AMO-id geven een specifieker campagneretype aan.

* Het achtervoegsel &quot;vt&quot; is aanwezig voor [!DNL DSP] view-through-verkeer en kan worden gebruikt om afzonderlijke doorklikkanalen en doorkijkkanalen [!DNL DSP] te maken.

De rest van de AMO-id kan worden genegeerd.

| [!UICONTROL AMO ID] | Kanaal | Regellogica |
|--------|---------|--------------------|
| !ctv (achtervoegsel) | [!UICONTROL DSP Connected TV ViewThrough] | Eindigt met |
| !d! (body) | [!UICONTROL Display Network] | Bevat |
| !g! (body) | [!UICONTROL Google Search] | Bevat |
| !s! (body) | [!UICONTROL Search Partner] | Bevat |
| !u! (body) | [!UICONTROL Smart Shopping Campaign] | Bevat |
| !ytv! (body) | [!UICONTROL YouTube Video Ad] | Bevat |
| !yts! (body) | [!UICONTROL YouTube Search Ad] | Bevat |
| !vp! (body) | [!UICONTROL Google Video Partners] | Bevat |
| !vt (achtervoegsel) | [!UICONTROL DSP ViewThrough] | Eindigt met |
| AL! (voorvoegsel) | [!UICONTROL Paid Search] | Begint met |
| AC! (voorvoegsel) | [!UICONTROL DSP Display] | Begint met |

## EF-ID in verwerkingsregels

De EF-id (EF-id) van AMO is de tweede trackingcode die wordt gebruikt in de [!DNL Analytics for Advertising] -integratie. Het hoofddoel is het bijhouden en doorgeven van [!DNL Analytics] -gebeurtenisgegevens aan Adobe Advertising. Telkens wanneer een klik-door of een mening-door voorkomt, wordt een unieke EF identiteitskaart geproduceerd, zelfs als het de nauwkeurige zelfde advertentie voor de zelfde bezoeker is. De EF-id wordt niet gebruikt in de gebruikersinterface van de [!DNL Analytics] -rapportage, omdat deze doorgaans de unieke waarden van 500 kB per variabele in [!DNL Analytics] overschrijdt, waardoor deze onbruikbaar wordt voor rapportage. De metriek en de meta-gegevens van Adobe Advertising worden niet toegepast op EF identiteitskaart; zij worden toegepast slechts op AMO identiteitskaart De toegevoegde granulariteit van het volgen is vereist voor campagtimalisatie in Adobe Advertising, zodat worden beide IDs vereist.

Hoewel de EF-id-dimensie niet rechtstreeks wordt gebruikt in [!DNL Analytics] -rapportage, kan de EF-id nuttig zijn bij het maken van marketingkanalen. Het EF-id-achtervoegsel geeft het kanaal (weergave of zoekopdracht) aan en geeft aan of het bezoek is aangestuurd door een doorklik of een doorzicht. Het scheidingsteken in de EF-id is een dubbele punt in plaats van het uitroepteken in de AMO-id.

| Achtervoegsel EF-ID | Kanaal |
|-------|---------|
| :s | [!UICONTROL Paid Search Click-through] |
| :d | [!UICONTROL Display ClickThrough] |
| :i | [!UICONTROL Display ViewThrough] |

## Voorbeelden van verwerkingsregels voor Adobe Advertising

De volgende voorbeeldregelreeks concentreert zich op de regels voor de reclamekanalen (Betaalde Onderzoek, Vertoning ClickThrough, en WeergaveThrough). De geadviseerde regel voor de opsporing van het Gesteunde Onderzoek (met inbegrip van hoe die regel met de Natuurlijke logica van het Kanaal van de Marketing van het Onderzoek) en een facultatieve update aan de Natuurlijke Verwijzende Regels van Domeinen in wisselwerking staat wordt ook aangetoond.

**Nota:** de Vertoning kan als twee kanalen worden gescheiden of in één enkel kanaal worden samengevoegd dat op adverteerdervoorkeur wordt gebaseerd.

Andere kanalen zijn opgenomen in het voorbeeldraster dat is opgenomen om de aanbevolen volgorde van de activiteiten van de reclamekanalen ten opzichte van andere kanalen in een standaardimplementatie te illustreren.

>[!IMPORTANT]
>
>Zie &quot;[ Orde van verrichtingen voor  [!DNL Marketing Channels]  regels ](#rule-order)&quot;voor informatie over de orde waarin uw regels zouden moeten worden verwerkt.

![ Voorbeeld van een reeks verwerkingsregels ](/help/integrations/assets/a4adc-mc-rule-set-example.png)

### Toegepaste zoekregel

U kunt het beste twee voorwaarden opnemen met de operator &quot;Any&quot; voor een [!UICONTROL Paid Search] -regel:

* De kosten-/klik-/afbeeldingsgegevens bevatten de AMO-id, dus de AMO-id. De AMO-id moet beginnen met &quot;AL!&quot; om klikgegevens/kosten-imitatiegegevens correct toe te wijzen aan [!UICONTROL Paid Search].<!-- Is this just called AMO ID there, not s_kwcid=XXX? What's the difference? -->

* De URL&#39;s voor [!UICONTROL Paid Search] click-through bevatten altijd de parameter van de `s_kwcid` querytekenreeks, dus neem deze op om ervoor te zorgen dat de duplicatie op de juiste wijze plaatsvindt als de bezoeker teruggaat naar de bestemmingspagina. Inclusief &quot;AL!&quot; vóór de `s_kwcid` om klik-/kosten-/afbeeldingsgegevens correct toe te wijzen aan [!UICONTROL Paid Search] .

Stel de waarde van het kanaal niet in op de AMO-id. In plaats daarvan, plaats het aan iets zoals het Verwijzen Domein, de Motor van het Onderzoek + Sleutelwoord, of Pagina. (Dit is relevant voor alle [!DNL Marketing Channels]).

<!-- Explain that comment about relevancy -- do I need to repeat this for each rule example?  -->

![ Voorbeeld van een Betaalde regel van het Onderzoek ](/help/integrations/assets/a4adc-mc-rule-paid-search.png " Voorbeeld van een Betaalde regel van het Onderzoek ")

### Natuurlijke zoekregel

Voor [!UICONTROL Natural Search], zorg ervoor dat uw [[!UICONTROL Paid Search] ontdekkingsregels ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/t-paid-search-detection) de `ef_id` en `s_kwcid` parameters van het vraagkoord omvatten. (Dit wordt meestal automatisch geconfigureerd wanneer Advertising Search, Social &amp; Commerce is geïntegreerd in [!DNL Analytics] , maar controleer dit voor het geval een [!DNL Analytics] -beheerder de logica heeft gewijzigd nadat de integratie was geconfigureerd.)

Stel de regel in op &quot;Regels voor zoeken in overeenkomst met natuurlijke zoekopdrachten&quot; (dit is doorgaans de standaardinstelling voor dit kanaal).

![ Voorbeeld van een Natuurlijke regel van het Onderzoek ](/help/integrations/assets/a4adc-mc-rule-natural-search.png " Voorbeeld van een Natuurlijke regel van het Onderzoek ")

### Doorklikregel 1 weergeven

Creeer een marketing kanaal van ClickThrough van de Vertoning door slechts klik-door te vangen. Omdat AMO ID het zelfde voor zowel klik-door als mening-door is, gebruikt deze regel de EF variabele van identiteitskaart en de `ef_id` parameter van het vraagkoord.

Soms worden doorklikkingen gevolgd door URL (het gebrek). In andere gevallen worden doorklikbewerkingen bijgehouden via de laatste gebeurtenisservice aan de serverzijde en bevat de URL dus niet de parameter `ef_id` . De regel controleert daarom voorwaarden waarin de EF identiteitskaart variabele of de `ef_id` parameter van het vraagkoord met &quot;:d&quot;beëindigt. Gebruik &quot;`Any`&quot;exploitant omdat u deze regel voor één van beide voorwaarde wilt teweegbrengen.

![ Voorbeeld van een eerste Display ClickThrough regel ](/help/integrations/assets/a4adc-mc-rule-display-ct.png " Voorbeeld van een eerste DisplayClickThrough regel ")

### Regel voor natuurlijke verwijzende domeinen

(Optioneel) U kunt het beste een voorwaarde &#39;Is First Page of Visit&#39; met de operator &#39;Any&#39; toevoegen aan de standaardregel [!UICONTROL Natural Referring Domains] . Hoewel deze regel optioneel is, kan deze helpen voorkomen dat het randhoofdlettergebruik van natuurlijke referenties wordt ingesteld wanneer de gebruiker op de knop Terug klikt om terug te keren naar de bestemmingspagina.

![ Voorbeeld van een Natuurlijke Verwijzende regel van Domeinen ](/help/integrations/assets/a4adc-mc-rule-natural-referring-domains.png " Voorbeeld van een Natuurlijke Verwijzende regel van Domeinen ")

### Doorkijkregel voor CTV weergeven

Als u de [!DNL DSP] weergave van een aangesloten tv (CTV) wilt bijhouden, maakt u een regel waarbij de AMO-id eindigt met `"!ctv"` . Omdat de bezoeker niet op de advertentie heeft geklikt, bevat de doorkijkbewerking de URL `ef_id` of `s_kwcid` niet en is voor de regel slechts één voorwaarde vereist.

![ Voorbeeld van een CTV van de Vertoning regel ](/help/integrations/assets/a4adc-mc-rule-display-ctv-vt.png " Voorbeeld van een CTV van de Vertoning regel ")

### Weergaveregel

Om een kanaal tot stand te brengen DisplayThrough, creeer een regel waarin EF identiteitskaart met &quot;:i&quot;beëindigt. Omdat de bezoeker niet op de advertentie heeft geklikt, bevat de doorkijkbewerking de URL `ef_id` of `s_kwcid` niet en is voor de regel slechts één voorwaarde vereist.

![ Voorbeeld van een DisplayThrough regel ](/help/integrations/assets/a4adc-mc-rule-display-vt.png " Voorbeeld van een regel DisplayThrough ")

### Doorklikregel nr. 2 weergeven

Voor de tweede regel van Display ClickThrough, plaats **identiteitskaart van AMO begint met &quot;AC!&quot;**. Deze tweede regel bestaat voor het vastleggen van de klik-/kosten-/afbeeldingsgegevens voor het weergavekanaal dat rechtstreeks van Adobe Advertising naar [!DNL Analytics] afkomstig is. Deze gegevens worden toegeschreven aan een AMO-id, maar bevatten geen URL met de queryreeks `ef_id` , zodat deze resultaten niet zijn gekoppeld aan een AMO EF-id, wat de eerste Display ClickThrough-regel vastlegt.

![ Voorbeeld van een tweede DisplayClickThrough regel ](/help/integrations/assets/a4adc-mc-rule-display-ct2.png " Voorbeeld van een tweede DisplayClickThrough regel ")

## Volgorde van bewerkingen voor [!DNL Marketing Channels] regels {#rule-order}

![ Ideale orde van verrichtingen voor op Adobe Advertising betrekking hebbende regels ](/help/integrations/assets/a4adc-mc-rule-order.png " Ideale orde van verrichtingen voor op Adobe Advertising betrekking hebbende regels ")

* Zet [!UICONTROL Paid Search] *vóór* [!UICONTROL Natural Search]. Anders kunnen betaalde zoekgegevens worden toegewezen aan natuurlijke zoekopdrachten.

* Zet **eerst** [!UICONTROL Display ClickThrough] *vóór* [!UICONTROL Natural Referring Domains] en [!UICONTROL Natural Social].

* Wanneer u [!UICONTROL CTV view-throughs] gebruikt, zet het *vóór* [!UICONTROL Display ViewThroughs]. Anders worden de CTV-weergaveoverzichten vastgelegd als DisplayThroughs.

* Plaats [!UICONTROL Display ViewThroughs] *na* andere kanalen maar vóór [!UICONTROL Internal] en [!UICONTROL Direct] omdat het mogelijk is dat een mening-door en een niet [!DNL Advertising] klik-door in de zelfde landende gebeurtenis kan voorkomen. Een bezoeker ziet bijvoorbeeld een Adobe Advertising-advertentie, krijgt een indruk en gaat vervolgens door [!UICONTROL Natural Search] naar de site.

  De beste manier is om voorrang te geven aan de andere kanalen (behalve [!UICONTROL Internal] en [!UICONTROL Direct]) boven doorzicht.

* Sommige adverteerders kiezen ervoor om [!UICONTROL Display ViewThroughs] over [!UICONTROL Natural Referring Domains] te kiezen. Doe dit door de verwerkingsorde van de twee regels te ruilen.

* De **tweede** [!UICONTROL Display ClickThrough] regel is daar om de klik/kosten/immengegevens te vangen die van Adobe Advertising aan [!DNL Analytics] direct binnen komen. Aangezien deze gegevens alleen worden toegeschreven aan een AMO-id, zijn deze resultaten niet verbonden met een AMO EF-id. Als u deze regel niet instelt, vallen alle klik-/kosten-/afbeeldingsgegevens onder het [!UICONTROL Direct] -kanaal. Dit is het standaardkanaal voor alle gegevens die niet overeenkomen met een [!DNL Marketing Channel] . Deze regel moet *na* de mening-door regel komen of het zal om het even welke mening-door ophalen.

<!-- WORDING!!!!  Check on this, and if it's necessary still with the other info about order:  If you include additional marketing channels, be sure to run your rules in order of specificity. For example, say you create a processing rule for [!DNL YouTube] video ad traffic tracked by Advertising Search, Social, & Commerce. The AMO ID for video traffic starts with with "AL!" and contain "!ytv!". If you run the rule for Paid Search (for which the AMO ID starts with "AL!") and then run the rule for video traffic, the YouTube video ad traffic would all fall under the Paid Search channel. -->

>[!MORELIKETHIS]
>
>* [ Grondbeginselen van  [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [ waarom de kanaalgegevens tussen Adobe Advertising en  [!DNL Marketing Channels]](mc-data-variances.md) kunnen variëren
>* [ Gebruikend  [!DNL Analytics Marketing Channels]  met de gegevens van Adobe Advertising ](mc-ac-data.md)
>* [ Video: Gebruikend  [!DNL Marketing Channels]  voor Adobe Advertising die ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html) meldt
>* [ Adobe Advertising IDs die door  [!DNL Analytics]](/help/integrations/analytics/ids.md) wordt gebruikt