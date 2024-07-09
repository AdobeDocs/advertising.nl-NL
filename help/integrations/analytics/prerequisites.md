---
title: Vereisten en belangrijke Informatie voor het Uitvoeren [!DNL Analytics for Advertising]
description: Vereisten en belangrijke Informatie voor het Uitvoeren [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 7c477900-ebb0-4c0e-811a-ab8bc6069599
source-git-commit: 8481227a8ccb1f1e6e715e34e14732967110c168
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# Vereisten en belangrijke Informatie voor het Uitvoeren [!DNL Analytics for Advertising]

*Adverteerders met DSP voor advertenties en[!DNL Advertising Search, Social, & Commerce]*

Lees de volgende informatie voordat u Adobe Advertising integreert met Adobe Analytics.

## Vereisten voor het rapporteren van Adobe-advertentiegegevens in [!DNL Analytics]

* een van de volgende twee handelingen:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience Cloud Identity Service: `visitorAPI.js` versie 2.0 of hoger
* Elke versie van Adobe Analytics (inclusief [!DNL Prime], [!DNL Premium], of [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` versie 2.1 of hoger
* (Advertising DSP-klanten) en [DSP JavaScript-fragment voor reclame](javascript.md) geïmplementeerd op uw webpagina&#39;s om doorkijkbezoeken bij te houden.

>[!TIP]
>
>Gebruik de meest recente versie van elke bibliotheek om de gegevensgetrouwheid te verbeteren.

## Vereisten voor het delen van analysesegmenten met Adobe Advertising

* Experience Cloud Identity Service: `visitorAPI.js` versie 2.1 of hoger
* Adobe Analytics: `appMeasurement.js` versie 1.8 of hoger

## Voorschriften voor rapportage [!DNL Analytics] Gegevens in Adobe-advertentie

Geef het Adobe Advertising Implementation-team het volgende op:

* De [!DNL Analytics] rapportsuite-id die moet worden gebruikt voor rapportage over betaalde mediaactiviteiten en voor het doorvoeren van siteactiviteiten voor optimalisatie en rapportage in Adobe Advertising
* The company&#39;s Experience Cloud Organization ID (Org ID).

U kunt beide id&#39;s vinden op het tabblad [Tabblad Overzicht van Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Ervaar het overzichtsscherm van Foutopsporing in de cloud](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Gegevens in Adobe-advertentie {#lookback-a4adc}

Omdat [!DNL Analytics] gegevens voor rapportage en optimalisatie naar Adobe Advertising worden verzonden, zijn de gegevens onderworpen aan de toewijzingsregels, waaronder de indruk en klik op lookback windows, die voor de adverteerder in Adobe Advertising zijn geconfigureerd.

![Instellingen voor terugkijkvensters op adverteerderniveau in Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* De kenmerk Advertising van Adobe klikt op lookback-venster: het aantal dagen na de eerste klik waarin de klik kan worden toegewezen aan een conversie. Deze waarde is standaard 60 dagen; het maximum is 90 dagen
* Adobe Advertising attribution lookback window: Het aantal dagen na een advertentie waarin de indruk aan een conversie kan worden toegeschreven. Deze waarde is standaard ingesteld op 14 dagen; de maximale waarde is 30 dagen

  >[!NOTE]
  >
  > Het venster met de imitatiezoekopdracht is specifiek voor Adobe Advertising en niet [!DNL Analytics for Advertising], rapportage.

De [!DNL Analytics for Advertising] JavaScript gebruikt deze instellingen om te bepalen hoe ver u een doorkijkitem of doorklikitem naar de site als geldig kunt beschouwen. Voor meer informatie over hoe de mening-productie en de klik-productie worden bepaald, zie &quot;[Adobe-id&#39;s voor advertenties die door Analytics worden gebruikt](ids.md).&quot;

## Adobe-advertentiegegevens in [!DNL Analytics]

[!DNL Analytics] Hiermee stelt u Adobe-advertentie-id&#39;s (AMO-id&#39;s) in in de hit Analytics, afhankelijk van het [!DNL eVar] persistentie-instelling, die van toepassing is op zowel doorklikken als doorzoeken. De persistentie-instelling is geconfigureerd op de achterkant van Adobe Advertising en uw Adobe-accountteam kan deze wijzigen.

* [!DNL Analytics for Advertising] [!DNL eVar] verlopen: standaard 60 dagen voor AMO-id&#39;s

>[!NOTE]
>
>Als u gegevens voor een ander tijdframe wilt segmenteren, kunt u [aangepaste segmenten instellen](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) met verschillende terugzoekvensters binnen de Werkruimte van de Analyse.

## Ondersteunde advertentie-omgevingen

* Zoeken
* Weergave
* Video
* Online video
* Verbonden tv
* Oorspronkelijk

Neem contact op met uw Adobe-accountteam voor de meest recente ondersteunde advertentieomgevingen in elk kanaal.

## Wat u moet weten voordat u gaat implementeren

* Het Adobe Advertising Implementation-team stelt de integratie in.

* Voor deze integratie worden geen extra kosten in rekening gebracht en serveraanroepen resulteren niet in extra [!DNL Analytics] of Adobe-advertentiekosten.

* [!DNL Analytics for Advertising] is een advertentie voor serveragnost: er kan een doorzicht- of doorklikbewerking optreden vanaf elke advertentieserver en de juiste id&#39;s worden gegenereerd bij het invoeren van de site.

* De integratie gaat alleen over [!DNL Analytics] standaard- en aangepaste gebeurtenissen voor Adobe Advertising voor de optimalisatie van biedingen voor latere betaalde media en advertenties. Het gaat niet door [!DNL Analytics] segmenten, berekende metriek en [!DNL eVars] naar Adobe Advertising voor Bodoptimalisatie.

* Adobe Advertising maakt permanente id&#39;s binnen [!DNL Analytics] op basis van de laatste advertentie die is aangeklikt of bekeken voordat de gebruiker de site betreedt, op basis van de [klik en mening-door raadplegingsvensters](#lookback-a4adc) geconfigureerd in Adobe Advertising. Als een bezoeker van de site beide typen interactie voor site-invoer binnen zijn profiel heeft en de klik zich binnen de terugzoekperiode bevindt, overschrijft de doorklikeid van de bezoeker de weergave-via-id voor siterapportage.

* [!DNL Analytics for Advertising] Voor het bijhouden van conversies in Adobe Analytics wordt een configureerbaar terugzoekvenster (standaard 60 dagen) gebruikt. In Adobe-advertentierapporten worden de siteconversies en de betrokkenheid tot aan het einde van dit terugzoekvenster weergegeven.

* Alle advertentietypen worden ondersteund. Niet alle advertentieomgevingen worden echter ondersteund.

* [!DNL Analytics] conversies worden momenteel bijgehouden en alleen toegewezen aan een bezoeker op hetzelfde apparaat.

* [!DNL Analytics for Advertising] biedt geen ondersteuning voor in-app view-through conversies.

* Het volgen van mening-door wordt niet gesteund voor adverteerders die een server-zij door:sturen implementatie van [!DNL Analytics].

### Aanvullende id

Zodra de Experience Cloud Identity Service is geïmplementeerd voor een site, worden hits weergegeven die gegevens bevatten van [!DNL Analytics] of Adobe Advertising bevatten een aanvullende id.

Voorbeeld: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Voor een nauwkeurige gegevensintegratie worden alle Adobe Advertising-oproepen van een [!DNL Analytics for Advertising] activiteit om inhoud te leveren of het doel te registreren metrisch moet overeenkomstige hebben [!DNL Analytics] hit die dezelfde aanvullende id deelt.

Wanneer u het oplossen van problemen in bent [!DNL Analytics]moet u bevestigen dat de aanvullende id aanwezig is voor [!DNL Analytics] treffers. In de [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html), kunt u deze id op het tabblad Adobe-reclame zien als de `sdid` parameter.

>[!NOTE]
>
> Deze implementatie werkt net als de [!DNL Analytics for Target] integratie.

>[!MORELIKETHIS]
>
>* [Overzicht van [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript-code voor analyses voor advertenties](/help/integrations/analytics/javascript.md)
