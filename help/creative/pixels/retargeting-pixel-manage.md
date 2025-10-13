---
title: Opnieuw doelende pixels beheren
description: Leer hoe u het opnieuw toewijzen van pixels maakt en implementeert voor gebruik als doel voor advertenties.
feature: Creative Pixels
exl-id: dcd13c5a-315d-4380-99f9-6dbab3e1e1be
source-git-commit: ed3bf0200d3d3b31ef80c790c4e702914459c521
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 0%

---

# Opnieuw doelende pixels beheren

<!-- Note to self: These aren't segments -- we don't create a pool of users. -->

U kunt een doelpixel maken om bezoekers van de landingspagina&#39;s of conversiepagina&#39;s van een adverteerder te identificeren aan de hand van gebruikerscookies of universele id&#39;s. De pixel houdt de meest recente gebeurtenis bij die de bezoeker op een pagina uitvoert en vangt specifieke attributen die de pagina voor die bezoekers volgt. Wanneer u de pixel hebt gemaakt, genereert u een pixeltag die u in de relevante webpagina&#39;s wilt invoegen om bezoekers te volgen.<!-- Note to self: surfer id=cookie or universal ID -->

Vervolgens kunt u de pixel gebruiken als het doel voor creatieve advertenties binnen een advertentie-ervaring om alleen advertenties weer te geven aan gebruikers met bepaalde kenmerken die eerder de aan de pixel gekoppelde webpagina&#39;s hebben bezocht. U kunt bijvoorbeeld bezoekers aanspreken die rode schoenen in grootte 10 bekijken als de webpagina&#39;s deze kenmerkwaarden bijhouden.<!-- better example? Make sure they match attribute examples below --> De ervaringsniveaudoelen worden toegepast in combinatie met de DSP-doelopties. De hiërarchische doelgerichtheid kan per DSP variëren.

Profielen voor opnieuw toewijzen worden 180 dagen opgeslagen.

Voorbeeldpixel:

```
<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--Insert ID5_PARTNER_ID--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--"></script>
```

>[!NOTE]
>
> * [!DNL Creative] ondersteunt alleen universele id&#39;s voor Advertising DSP.
>* U kunt uw eerste-partijpubliek van Adobe Audience Manager en Adobe Analytics als [&#x200B; creatieve doelstellingen voor uw ervaringen &#x200B;](/help/creative/experiences/experience-settings-targeting.md) ook gebruiken.
>* Wanneer u een ervaring als advertentie gebruikt binnen een plaatsing van Advertising DSP, kunt u de plaatsing aan alle publiek richten beschikbaar aan u in DSP. U kunt [&#x200B; markeringen van het douanesegment &#x200B;](/help/dsp/audiences/custom-segment-create.md) ook tot stand brengen om alle bezoekers aan specifieke het landen pagina&#39;s te volgen en dan die segmenten als creatieve doelstellingen voor een plaatsing te gebruiken. Advertising DSP past een ad-level gerichte aanpak toe boven op (niet in plaats van) plaatsing-niveau gerichte doelframes.
>* Bezoekers van websites die ervoor hebben gekozen om geen advertenties meer te volgen voor advertenties, ontvangen geen advertenties met persoonlijke creatieve inhoud op basis van het doelsegment of het doelprofiel.

## Een nieuwe doelpixel maken

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]** .

1. Klik boven de datatabel op **[!UICONTROL Creative]** en selecteer vervolgens > **[!UICONTROL Retargeting Pixel]** .

1. Specificeer [&#x200B; het opnieuw richten pixelmontages &#x200B;](#retargeting-pixel-settings).

1. Klik op **[!UICONTROL Save]**.

1. [&#x200B; produceer de pixelmarkering &#x200B;](#retargeting-pixel-generate) om aan de adverteerder of websitecontact te verstrekken.

   De pixeltag voor herbestemming moet de laatste handeling op de pagina zijn.<!-- verify here and below -->

   De IT-afdeling of andere groep van de adverteerder moet mogelijk de implementatie van de tag plannen of hierover worden geïnformeerd.

## Een herrichtingspixel bewerken

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]** .

1. Plaats de cursor op de naam van de pixel en klik op **[!UICONTROL Edit]** .

1. Bewerk [&#x200B; opnieuw richtend pixelmontages &#x200B;](#retargeting-pixel-settings).

1. Klik op **[!UICONTROL Save]**.

1. [&#x200B; produceer de pixelmarkering &#x200B;](#retargeting-pixel-generate) om aan de adverteerder of websitecontact te verstrekken zodat zij de originele markering kunnen vervangen.

   De pixeltag voor herbestemming moet de laatste handeling op de bestemmingspagina zijn.

   De IT-afdeling of andere groep van de adverteerder moet mogelijk de implementatie van de tag plannen of hierover worden geïnformeerd.

## Een label genereren voor een herrichtingspixel {#retargeting-pixel-generate}

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]** .

1. Plaats de cursor op de naam van de pixel en klik op **[!UICONTROL Generate Tag]** .

1. Klik op **[!UICONTROL Copy to Clipboard]** om de code naar het klembord van de computer te kopiëren, waaruit u de tekst kunt plakken in een bestand dat u wilt opslaan.

1. In de pixelmarkering, specificeer een waarde voor elk attribuut in zowel de `<img src>` als `<script src>` secties door elk &quot;`Insert <attribute>`&quot;met een waarde te vervangen. Geef een ID5-partner-id op als de tag een universele id vastlegt.

   Als u handmatig aanvullende kenmerken toevoegt, neemt u URL-codering op.

   Als u bijvoorbeeld de kenmerken &quot;category&quot;, &quot;color&quot; en &quot;size&quot; hebt opgenomen en ID5 universele id&#39;s hebt vastgelegd, bevat de pixeltag de volgende parameters: `&ut1=--Insert category--&ut2=--Insert color--&ut3=--Insert size--` en `&id5pid=--Insert ID5_PARTNER_ID--` . Als u gebruikers wilt aanwijzen die rode sandalen in grootte 10 selecteren, wijzigt u de parameters in zowel de afbeeldingstag als de scripttag in `&ut1=sandals&ut2=red&ut3=10` en voert u ook de id van uw ID5-partner in de scripttag in, zoals `&id5pid=0123456789` .

   `<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--0123456789--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--"></script>`

1. Geef de ingevulde pixeltag door aan de adverteerder of websitecontactpersoon, samen met een lijst van de relevante bestemmingspagina&#39;s waarin deze moet worden ingevoegd.

   De pixeltag voor herbestemming moet de laatste handeling op de bestemmingspagina zijn.

   De IT-afdeling of andere groep van de adverteerder moet mogelijk de implementatie van de tag plannen of hierover worden geïnformeerd.

## Een herrichtingspixel verwijderen

1. Klik in het hoofdmenu op **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]** .

1. Plaats de cursor op de naam van de pixel en klik op **[!UICONTROL Delete]** .

1. Klik in het bevestigingsbericht op **[!UICONTROL Delete]** .

## Pixelinstellingen opnieuw instellen {#retargeting-pixel-settings}

**[!UICONTROL Pixel Name]:** De naam van de pixel. **Nota:** de pixelmarkering omvat pixelidentiteitskaart (`pxId=<ID>`), niet de pixelnaam.

**[!UICONTROL Advertiser]:** (Alleen-lezen voor bestaande pixels) De adverteerder waarvoor de pixel wordt bijgehouden.

**[!UICONTROL Attribute 1]:** Een kenmerk dat in de pixeltag moet worden opgenomen, zoals &quot;SKU&quot;, &quot;categorie&quot;, &quot;grootte&quot; of andere kenmerken van de pagina of het product dat op de pagina wordt weergegeven. Geef een waarde op voor het kenmerk in de pixeltag voordat u het invoegt in de relevante webpagina&#39;s.

Wanneer u doelt en ervaringen opdoet met gebruikers die aan de pixel worden blootgesteld, geven de instellingen voor het aanwijzen de kenmerkwaarden op die aanwezig moeten zijn om de creatieve elementen weer te geven.

**[!UICONTROL Attribute 2]** , **[!UICONTROL Attribute 3]** , **[!UICONTROL Attribute 4]** , **[!UICONTROL Attribute 5]:** (Optioneel) Aanvullende kenmerken die in de pixeltag moeten worden opgenomen. Geef een waarde op voor elk extra kenmerk in de pixeltag voordat u het invoegt in de relevante webpagina&#39;s.

Wanneer u doelt en ervaringen opdoet met gebruikers die aan de pixel worden blootgesteld, geven de instellingen voor het aanwijzen de kenmerkwaarden op die aanwezig moeten zijn om de creatieve elementen weer te geven.

**[!UICONTROL Advanced]** > **[!UICONTROL Universal IDs]:** (Alleen nieuwe pixels; optioneel) Typen universele id&#39;s voor de bij te houden pixeltag:

* *[!UICONTROL ID5]:* De pixeltag traceert [!DNL ID5] id&#39;s. Er worden geen kosten in rekening gebracht voor afbeeldingen die aan universele id&#39;s worden geleverd.

* *[!UICONTROL Ramp ID]:* De pixellabeltracks [!DNL Ramp IDs] . Er worden geen kosten in rekening gebracht voor afbeeldingen die aan universele id&#39;s worden geleverd.

Als u deze functie wilt gebruiken, moet u of een andere gebruiker van de DSP-account de serviceovereenkomst voor het gebruik van universele id&#39;s één keer accepteren voordat u universele id&#39;s voor een nieuw type id kunt gebruiken. Voor klanten met beheerde servicecontracten krijgt uw Adobe-accountteam uw toestemming en accepteert u de voorwaarden namens uw organisatie. Klik op **[!UICONTROL Terms of Service]** om de termen te lezen. Schuif naar de onderkant van de voorwaarden en klik op **[!UICONTROL Accept]** om de voorwaarden te accepteren.

>[!MORELIKETHIS]
>
>* [&#x200B; Gericht en ervaringsmontages &#x200B;](/help/creative/experiences/experience-settings-targeting.md)
>* [&#x200B; Ongeveer en ervaringen &#x200B;](/help/creative/experiences/experience-about.md)
