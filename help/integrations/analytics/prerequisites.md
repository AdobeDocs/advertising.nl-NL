---
title: Vereisten en Zeer belangrijke Informatie voor het Uitvoeren  [!DNL Analytics for Advertising]
description: Vereisten en Zeer belangrijke Informatie voor het Uitvoeren  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 1559c2cb83e32d90f4b2fe959d07c4e588d9becf
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Vereisten en belangrijke informatie voor implementatie [!DNL Analytics for Advertising]

*Advertisers met Advertising DSP en[!DNL Advertising Search, Social, & Commerce]*

Controleer de volgende informatie voordat u Adobe Advertising met Adobe Analytics integreert.

## Vereisten voor het rapporteren van gegevens over Adoben Advertising in [!DNL Analytics]

* een van de volgende twee handelingen:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience Cloud Identity Service: `visitorAPI.js` versie 2.0 of hoger
* Elke versie van Adobe Analytics (inclusief [!DNL Prime] , [!DNL Premium] of [!DNL Ultimate] )
* Adobe Analytics: `appMeasurement.js` versie 2.1 of hoger
* (Advertising DSP klanten) een [&#x200B; fragment van Advertising DSP JavaScript &#x200B;](javascript.md) opgesteld in uw webpagina&#39;s om mening-door bezoeken te volgen.

>[!TIP]
>
>Gebruik de meest recente versie van elke bibliotheek om de gegevensgetrouwheid te verbeteren.

## Vereisten voor het delen van analysesegmenten met Adobe Advertising

* Experience Cloud Identity Service: `visitorAPI.js` versie 2.1 of hoger
* Adobe Analytics: `appMeasurement.js` versie 1.8 of hoger

## Vereisten voor het rapporteren van [!DNL Analytics] gegevens in Adobe Advertising

Geef het volgende door aan het implementatieteam van de Adobe Advertising:

* De rapportsuite-id van [!DNL Analytics] die moet worden gebruikt voor rapportage over betaalde mediaactiviteiten en voor het doorvoeren van siteactiviteiten voor optimalisatie en rapportage in Adobe Advertising
* De organisatie-id (Org ID) van het Experience Cloud van het bedrijf.

U kunt allebei van deze IDs op het [&#x200B; Summiere lusje van Debugger van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=nl-NL) vinden.

![&#x200B; het Summiere scherm van het Experience Cloud Debugger &#x200B;](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Gegevens in Adobe Advertising {#lookback-a4adc}

Aangezien [!DNL Analytics] -gegevens naar de Adobe Advertising worden verzonden voor rapportage en optimalisatie, zijn de gegevens onderworpen aan de toewijzingsregels, inclusief de indruk en klik op terugzoekvensters, die voor de adverteerder in Adobe Advertising zijn geconfigureerd.

![&#x200B; adverteerder-vlakke terugkijkvenstermontages in Adobe Advertising &#x200B;](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising-toewijzing klikt op lookback-venster: het aantal dagen na de eerste klik waarin de klik kan worden toegewezen aan een conversie. Deze waarde is standaard 60 dagen; het maximum is 90 dagen
* Terugkijkvenster van de Adobe Advertising van de attributieindruk: Het aantal dagen na een advertentie voorkomt waarin de indruk aan een omzetting kan worden toegeschreven. Deze waarde is standaard ingesteld op 14 dagen; de maximale waarde is 30 dagen

  >[!NOTE]
  >
  > Het venster met de imitatiezoekopdracht is specifiek voor de rapportage van de Adobe Advertising, niet [!DNL Analytics for Advertising] .

De JavaScript van [!DNL Analytics for Advertising] gebruikt deze instellingen om te bepalen hoe ver het is om een doorkijkitem of doorklikitem als geldig voor de site te beschouwen. Voor meer informatie over hoe mening-door en klik-door wordt bepaald, zie &quot;[&#x200B; Adobe Advertising IDs die door Analytics &#x200B;](ids.md) wordt gebruikt.&quot;

## Gegevens Adobe Advertising in [!DNL Analytics]

[!DNL Analytics] stelt Adobe Advertising-id&#39;s (AMO-id&#39;s) in in de hit Analytics, afhankelijk van de persistentie-instelling van de adverteerder [!DNL eVar] , die van toepassing is op doorklikken en doorzoeken. De persistentie die wordt geplaatst wordt gevormd op het achtereind van de Adobe Advertising, en uw Team van de Rekening van de Adobe kan het veranderen.

* [!DNL Analytics for Advertising] [!DNL eVar] verlopen: standaard 60 dagen voor AMO-id&#39;s

>[!NOTE]
>
>Om gegevens voor een verschillend chronologie te segmenteren, kunt u [&#x200B; opstellings douanesegmenten &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=nl-NL) met verschillende raadplegingsvensters binnen Analysis Workspace.

## Ondersteunde advertentie-omgevingen

* Zoeken
* Weergave
* Video
* Online video
* Verbonden tv
* Oorspronkelijk

Neem contact op met het accountteam van de Adobe voor de meest recente ondersteunde advertentieomgevingen in elk kanaal.

## Wat u moet weten voordat u gaat implementeren

* Het Adobe Advertising implementatieteam stelt de integratie in.

* Voor deze integratie worden geen extra kosten in rekening gebracht en bovendien resulteren serveraanroepen niet in extra [!DNL Analytics] - of Adobe Advertising-kosten.

* [!DNL Analytics for Advertising] is niet-identiek aan een server: een doorkijkbewerking of doorklikken kan plaatsvinden vanaf een advertentieserver en de juiste id&#39;s worden gegenereerd bij het invoeren van de site.

* De integratie geeft alleen [!DNL Analytics] standaard- en aangepaste gebeurtenissen door aan Adobe Advertising voor optimale biedingen voor daaropvolgende betaalde media- en advertentiepogingen. [!DNL Analytics] segmenten, berekende meetgegevens en [!DNL eVars] worden niet doorgegeven aan Adobe Advertising voor Bodoptimalisatie.

* De Adobe Advertising leidt tot blijvende IDs binnen [!DNL Analytics] die op laatste geklikte of bekeken reclame wordt gebaseerd alvorens de gebruiker de plaats ingaat, op de [&#x200B; wordt gebaseerd klikt en mening-door raadplegingsvensters &#x200B;](#lookback-a4adc) die in Adobe Advertising worden gevormd. Als een bezoeker van de site beide typen interactie voor site-invoer binnen zijn profiel heeft en de klik zich binnen de terugzoekperiode bevindt, overschrijft de doorklikeid van de bezoeker de weergave-via-id voor siterapportage.

* [!DNL Analytics for Advertising] voor het bijhouden van conversies in Adobe Analytics wordt een configureerbaar terugzoekvenster (standaard 60 dagen) gebruikt. De rapporten van de Adobe Advertising weerspiegelen plaatsomzettingen en betrokkenheid door het eind van dit het volgen raadplegingsvenster.

* Alle advertentietypen worden ondersteund. <!--Clarify what this might include. It used to include CTV, but not anymore: However, not all ad environments are supported. -->

* [!DNL Analytics] -conversies worden momenteel bijgehouden en worden alleen toegewezen aan een bezoeker op hetzelfde apparaat.

* [!DNL Analytics for Advertising] biedt geen ondersteuning voor in-app view-through conversies.

* View-through tracking wordt niet ondersteund voor adverteerders die een serverimplementatie van [!DNL Analytics] gebruiken voor doorsturen.

### Aanvullende id

Zodra de Dienst van de Identiteit van het Experience Cloud voor een plaats wordt uitgevoerd, bevatten de hits die gegevens van [!DNL Analytics] of Adobe Advertising bevatten een extra identiteitskaart

Voorbeeld: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Voor een nauwkeurige gegevensintegratie moeten alle aanroepen van Adoben Advertising die door een [!DNL Analytics for Advertising] -activiteit worden gebruikt om inhoud te leveren of het doel te registreren, een overeenkomende hit van [!DNL Analytics] hebben die dezelfde aanvullende id heeft.

Als u problemen oplost in [!DNL Analytics] , moet u controleren of de aanvullende id aanwezig is voor [!DNL Analytics] -treffers. In [&#x200B; debugger van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=nl-NL), kunt u dit identiteitskaart in het lusje van de Adobe Advertising als `sdid` parameter zien.

>[!NOTE]
>
> Deze implementatie werkt op ongeveer dezelfde manier als de [!DNL Analytics for Target] -integratie.

>[!MORELIKETHIS]
>
>* [&#x200B; Overzicht van  [!DNL Analytics for Advertising]](overview.md)
>* [&#x200B; Code van JavaScript voor Analytics voor Advertising &#x200B;](/help/integrations/analytics/javascript.md)
