---
title: Vereisten en belangrijkste informatie voor het uitvoeren  [!DNL Analytics for Advertising]
description: Vereisten en belangrijkste informatie voor het uitvoeren  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Vereisten en belangrijke informatie voor implementatie [!DNL Analytics for Advertising]

*Advertisers met Advertising DSP en[!DNL Advertising Search, Social, & Commerce]*

Bekijk de volgende informatie voordat u Adobe Advertising integreert met Adobe Analytics.

## Vereisten voor het rapporteren van Adobe Advertising-gegevens in [!DNL Analytics]

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

## Vereisten voor het rapporteren van [!DNL Analytics] -gegevens in Adobe Advertising

Geef het Adobe Advertising-implementatieteam de volgende informatie:

* De rapportsuite-id van [!DNL Analytics] die moet worden gebruikt voor rapportage over betaalde media-activiteiten en voor het doorvoeren van siteactiviteiten voor optimalisatie en rapportage in Adobe Advertising
* De Experience Cloud-organisatie-id (Org ID) van het bedrijf.

U kunt allebei van deze IDs op het [&#x200B; Summiere lusje van Debugger van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=nl-NL) vinden.

![&#x200B; het Summiere scherm van Foutopsporing van de Wolk van de Ervaring &#x200B;](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Gegevens in Adobe Advertising {#lookback-a4adc}

Omdat [!DNL Analytics] -gegevens naar Adobe Advertising worden verzonden voor rapportage en optimalisatie, zijn de gegevens onderworpen aan de toewijzingsregels, inclusief de indruk en klik op terugzoekvensters, die zijn geconfigureerd voor de adverteerder in Adobe Advertising.

![&#x200B; adverteerder-vlakke terugkijkvenstermontages in Adobe Advertising &#x200B;](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising-toewijzing klikt op lookback-venster: het aantal dagen na de eerste klik waarin de klik kan worden toegewezen aan een conversie. Deze waarde is standaard 60 dagen; het maximum is 90 dagen
* Het terugkijkvenster van Adobe Advertising-toewijzingsindruk: het aantal dagen na een advertentie waarin de indruk aan een conversie kan worden toegeschreven. Deze waarde is standaard ingesteld op 14 dagen; de maximale waarde is 30 dagen

  >[!NOTE]
  >
  > Het venster voor het terugzoeken van de indruk is specifiek voor Adobe Advertising, niet [!DNL Analytics for Advertising] voor rapportage.

De JavaScript van [!DNL Analytics for Advertising] gebruikt deze instellingen om te bepalen hoe ver het is om een doorkijkitem of doorklikitem als geldig voor de site te beschouwen. Voor meer informatie over hoe mening-door en klik-door wordt bepaald, zie &quot;[&#x200B; Adobe Advertising IDs die door Analytics &#x200B;](ids.md) wordt gebruikt.&quot;

## Adobe Advertising-gegevens in [!DNL Analytics]

Met [!DNL Analytics] worden Adobe Advertising-id&#39;s (AMO-id&#39;s) ingesteld in de hit Analytics, afhankelijk van de persistentie-instelling van de adverteerder in [!DNL eVar] , die van toepassing is op doorklikken en doorzoeken. De persistentie-instelling wordt geconfigureerd op de Adobe Advertising back-end en uw Adobe-accountteam kan deze wijzigen.

* [!DNL Analytics for Advertising] [!DNL eVar] verlopen: standaard 60 dagen voor AMO-id&#39;s

>[!NOTE]
>
>Om gegevens voor een verschillend chronologie te segmenteren, kunt u [&#x200B; opstellings douanesegmenten &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=nl-NL) met verschillende raadplegingsvensters binnen Analysis Workspace.

## Ondersteunde advertentieomgevingen

* Zoeken
* Weergave
* Video
* Online video
* Verbonden tv
* Oorspronkelijk

Neem contact op met uw Adobe-accountteam voor de meest recente ondersteunde advertentiemogelijkheden in elk kanaal.

## Wat u moet weten voordat u gaat implementeren

* Het Adobe Advertising-implementatieteam stelt de integratie in.

* Voor deze integratie worden geen extra kosten in rekening gebracht en bovendien resulteren serveraanroepen niet in extra [!DNL Analytics] - of Adobe Advertising-kosten.

* [!DNL Analytics for Advertising] is niet-identiek aan een server: een doorkijkbewerking of doorklikken kan plaatsvinden vanaf een advertentieserver en de juiste id&#39;s worden gegenereerd bij het invoeren van de site.

* De integratie geeft alleen [!DNL Analytics] standaard- en aangepaste gebeurtenissen door aan Adobe Advertising voor optimalisatie van biedingen voor daaropvolgende betaalde media- en advertentieactiviteiten. [!DNL Analytics] segmenten, berekende maatstaven en [!DNL eVars] worden niet doorgegeven aan Adobe Advertising voor Bodoptimalisatie.

* Adobe Advertising leidt tot blijvende IDs binnen [!DNL Analytics] die op laatste geklikte of bekeken reclame wordt gebaseerd alvorens de gebruiker de plaats ingaat, op [&#x200B; wordt gebaseerd klikt en mening-door raadplegingsvensters &#x200B;](#lookback-a4adc) die in Adobe Advertising worden gevormd. Als een bezoeker van de site beide typen interactie voor site-invoer binnen zijn profiel heeft en de klik zich binnen de terugzoekperiode bevindt, overschrijft de doorklikeid van de bezoeker de weergave-via-id voor siterapportage.

* [!DNL Analytics for Advertising] voor het bijhouden van conversies in Adobe Analytics wordt een configureerbaar terugzoekvenster (standaard 60 dagen) gebruikt. Adobe Advertising-rapporten weerspiegelen de omzettingen van sites en de betrokkenheid aan het einde van dit terugzoekvenster.

* Alle advertentietypen worden ondersteund. <!--Clarify what this might include. It used to include CTV, but not anymore: However, not all ad environments are supported. -->

* [!DNL Analytics] -conversies worden momenteel bijgehouden en worden alleen toegewezen aan een bezoeker op hetzelfde apparaat.

* [!DNL Analytics for Advertising] biedt geen ondersteuning voor in-app view-through conversies.

* View-through tracking wordt niet ondersteund voor adverteerders die een serverimplementatie van [!DNL Analytics] gebruiken voor doorsturen.

### Aanvullende id

Wanneer de Experience Cloud Identity Service voor een site is geïmplementeerd, bevatten hits die gegevens van [!DNL Analytics] of Adobe Advertising bevatten een aanvullende id.

Voorbeeld: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Voor een nauwkeurige gegevensintegratie moeten alle Adobe Advertising-aanroepen die door een [!DNL Analytics for Advertising] -activiteit worden gebruikt om inhoud te leveren of de doel-metrische waarde op te nemen, een overeenkomende [!DNL Analytics] hit hebben die dezelfde aanvullende id heeft.

Als u problemen oplost in [!DNL Analytics] , moet u controleren of de aanvullende id aanwezig is voor [!DNL Analytics] -treffers. In [&#x200B; Debugger van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html?lang=nl-NL), kunt u deze identiteitskaart in het lusje van Adobe Advertising als `sdid` parameter zien.

>[!NOTE]
>
> Deze implementatie werkt op ongeveer dezelfde manier als de [!DNL Analytics for Target] -integratie.

>[!MORELIKETHIS]
>
>* [&#x200B; Overzicht van  [!DNL Analytics for Advertising]](overview.md)
>* [&#x200B; code van JavaScript voor Analytics voor Advertising &#x200B;](/help/integrations/analytics/javascript.md)
