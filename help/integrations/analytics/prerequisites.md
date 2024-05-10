---
title: Vereisten en belangrijke Informatie voor het Uitvoeren [!DNL Analytics for Advertising]
description: Vereisten en belangrijke Informatie voor het Uitvoeren [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Vereisten en belangrijke Informatie voor het Uitvoeren [!DNL Analytics for Advertising]

*Adverteerders met DSP en[!DNL Advertising Search, Social, & Commerce]*

Controleer de volgende informatie voordat u Adobe Advertising met Adobe Analytics integreert.

## Vereisten voor de rapportage van gegevens over Adoben Advertising in [!DNL Analytics]

* een van de volgende twee handelingen:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Identiteitsdienst Experience Cloud: `visitorAPI.js` versie 2.0 of hoger
* Elke versie van Adobe Analytics (inclusief [!DNL Prime], [!DNL Premium], of [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` versie 2.1 of hoger
* (Reclame DSP klanten) en [Adverteren DSP JavaScript-fragment](javascript.md) geïmplementeerd op uw webpagina&#39;s om doorkijkbezoeken bij te houden.

>[!TIP]
>
>Gebruik de meest recente versie van elke bibliotheek om de gegevensgetrouwheid te verbeteren.

## Vereisten voor het delen van analysesegmenten met Adobe Advertising

* Identiteitsdienst Experience Cloud: `visitorAPI.js` versie 2.1 of hoger
* Adobe Analytics: `appMeasurement.js` versie 1.8 of hoger

## Voorschriften voor rapportage [!DNL Analytics] Gegevens in Adobe Advertising

Geef het volgende door aan het implementatieteam van de Adobe Advertising:

* De [!DNL Analytics] rapportsuite-id die moet worden gebruikt voor rapportage over betaalde mediaactiviteiten en voor het uitvoeren van siteactiviteiten voor optimalisatie en rapportage in Adobe Advertising
* De organisatie-id (Org ID) van het Experience Cloud van het bedrijf.

U kunt beide id&#39;s vinden op het tabblad [Tabblad Overzicht van de Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Samenvattingsscherm Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Gegevens in Adobe Advertising {#lookback-a4adc}

Omdat [!DNL Analytics] de gegevens worden verzonden naar de Adobe Advertising voor rapportering en optimalisering, de gegevens zijn onderworpen aan de attributieregels, met inbegrip van de indruk en klik raadplegingsvensters, die voor de adverteerder in Adobe Advertising worden gevormd.

![de montages van het raadplegingsvenster op adverteerderniveau in Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising-toewijzing klikt op lookback-venster: het aantal dagen na de eerste klik waarin de klik kan worden toegewezen aan een conversie. Deze waarde is standaard 60 dagen; het maximum is 90 dagen
* Terugkijkvenster van de Adobe Advertising van de attributieindruk: Het aantal dagen na een advertentie voorkomt waarin de indruk aan een omzetting kan worden toegeschreven. Deze waarde is standaard ingesteld op 14 dagen; de maximale waarde is 30 dagen

  >[!NOTE]
  >
  > Het venster van de imitatieterugblik is specifiek voor Adobe Advertising, niet [!DNL Analytics for Advertising], rapportage.

De [!DNL Analytics for Advertising] JavaScript gebruikt deze instellingen om te bepalen hoe ver u een doorkijkitem of doorklikitem naar de site als geldig kunt beschouwen. Voor meer informatie over hoe de mening-productie en de klik-productie worden bepaald, zie &quot;[Adobe Advertising-id&#39;s gebruikt door Analytics](ids.md).&quot;

## Gegevens Adobe Advertising in [!DNL Analytics]

[!DNL Analytics] stelt Adobe Advertising-id&#39;s (AMO-id&#39;s) in in de treffer Analytics, afhankelijk van het [!DNL eVar] persistentie-instelling, die van toepassing is op zowel doorklikken als doorzoeken. De persistentie die wordt geplaatst wordt gevormd op het achtereind van de Adobe Advertising, en uw Team van de Rekening van de Adobe kan het veranderen.

* [!DNL Analytics for Advertising] [!DNL eVar] verlopen: standaard 60 dagen voor AMO-id&#39;s

>[!NOTE]
>
>Als u gegevens voor een ander tijdframe wilt segmenteren, kunt u [aangepaste segmenten instellen](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) met verschillende terugzoekvensters in Analysis Workspace.

## Ondersteunde advertentie-omgevingen

* Zoeken
* Weergave
* Video
* Online video
* Oorspronkelijk

Neem contact op met het accountteam van de Adobe voor de meest recente ondersteunde advertentieomgevingen in elk kanaal.

## Wat u moet weten voordat u gaat implementeren

* Het Adobe Advertising implementatieteam stelt de integratie in.

* Voor deze integratie worden geen extra kosten in rekening gebracht en serveraanroepen resulteren niet in extra [!DNL Analytics] of Adobe Advertising.

* [!DNL Analytics for Advertising] is een advertentie voor serveragnost: er kan een doorzicht- of doorklikbewerking optreden vanaf elke advertentieserver en de juiste id&#39;s worden gegenereerd bij het invoeren van de site.

* De integratie gaat alleen over [!DNL Analytics] standaard- en aangepaste evenementen voor Adobe Advertising voor het optimaliseren van biedingen voor latere betaalde media- en advertentietechnieken. Het gaat niet door [!DNL Analytics] segmenten, berekende metriek en [!DNL eVars] naar Adobe Advertising voor Bodoptimalisatie.

* Adobe Advertising maakt permanente id&#39;s binnen [!DNL Analytics] op basis van de laatste advertentie die is aangeklikt of bekeken voordat de gebruiker de site betreedt, op basis van de [klik en mening-door raadplegingsvensters](#lookback-a4adc) geconfigureerd in Adobe Advertising. Als een bezoeker van de site beide typen interactie voor site-invoer binnen zijn profiel heeft en de klik zich binnen de terugzoekperiode bevindt, overschrijft de doorklikeid van de bezoeker de weergave-via-id voor siterapportage.

* [!DNL Analytics for Advertising] Voor het bijhouden van conversies in Adobe Analytics wordt een configureerbaar terugzoekvenster (standaard 60 dagen) gebruikt. De rapporten van de Adobe Advertising weerspiegelen plaatsomzettingen en betrokkenheid door het eind van dit het volgen raadplegingsvenster.

* Alle advertentietypen worden ondersteund. Niet alle advertentieomgevingen worden echter ondersteund.

  Zo worden aangesloten tv-advertenties (CTV-advertenties) niet bijgehouden omdat er geen kliks plaatsvinden in CTV en er geen conversies kunnen plaatsvinden op hetzelfde apparaat. Als de advertentie echter wordt weergegeven in een desktopomgeving, kunnen bepaalde gegevens van de doorkijksite worden bijgehouden.

* [!DNL Analytics] conversies worden momenteel bijgehouden en alleen toegewezen aan een bezoeker op hetzelfde apparaat.

* [!DNL Analytics for Advertising] biedt geen ondersteuning voor in-app view-through conversies.

* Het volgen van mening-door wordt niet gesteund voor adverteerders die een server-zij door:sturen implementatie van [!DNL Analytics].

### Aanvullende id

Zodra de Dienst van de Identiteit van het Experience Cloud voor een plaats wordt uitgevoerd, klappen die gegevens van bevatten [!DNL Analytics] of Adobe Advertising bevat een aanvullende id.

Voorbeeld: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Voor nauwkeurige gegevensintegratie, alle vraag van de Adobe Advertising die door [!DNL Analytics for Advertising] activiteit om inhoud te leveren of het doel te registreren metrisch moet overeenkomstige hebben [!DNL Analytics] hit die dezelfde aanvullende id deelt.

Wanneer u het oplossen van problemen in bent [!DNL Analytics]moet u bevestigen dat de aanvullende id aanwezig is voor [!DNL Analytics] treffers. In de [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html), kunt u deze id op het tabblad Adobe Advertising zien als de `sdid` parameter.

>[!NOTE]
>
> Deze implementatie werkt net als de [!DNL Analytics for Target] integratie.

>[!MORELIKETHIS]
>
>* [Overzicht van [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript-code voor analyses voor advertenties](/help/integrations/analytics/javascript.md)
