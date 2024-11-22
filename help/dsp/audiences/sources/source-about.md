---
title: Ongeveer de Bronnen van het Publiek van de Eerste Partij
description: Leer over het omzetten van andere gebruikers herkenningstekens in uw eerste-partijsegmenten in universele IDs voor het kokieloze richten.
feature: DSP Audiences
exl-id: ba056440-fa2b-4472-bbfd-16dd0af887f1
source-git-commit: 3a641db6b145e67e6e1f1daca271dd524973e075
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# Ongeveer de Bronnen van het Publiek van de Eerste Partij

*eigenschap van Beta*

DSP kan eerste-partijsegmenten die uit gehakt e-mailIDs worden samengesteld binnen uw platform van klantengegevens (CDP) worden opgenomen en hen omzetten in segmenten die van universele IDs worden samengesteld. Elke resulterende identiteitskaart is op mensen-gebaseerd, en de frequentiecappen worden toegepast op het niveau van identiteitskaart <!-- Move that info. to somewhere else? -->.

Segmentdetails omvatten de grootte van elk universeel id-type en de grootte voor elk apparaattype dat door cookies of apparaat-id&#39;s wordt bijgehouden.

## Universal ID-typen {#universal-id-types}

<!--  Replace below with this once ID5 sources are possible 

Using your first-party data, you can create segments with IDs from the following universal ID partners.

* Authenticated (deterministic) IDs using hashed email addresses:

-->

U kunt uw eerste-partijsegmenten aan segmenten met voor authentiek verklaarde (deterministische) IDs van de volgende universele partners van identiteitskaart vertalen.

* [[!DNL LiveRamp] [!DNL RampIDs] ](https://liveramp.com/identity-resolution):

   * Voor het opnieuw richten van het programma geopende gebruikers.

     [!DNL RampIDs] zijn beschikbaar voor gebruikers in Noord-Amerika, Australië en Nieuw-Zeeland.

     De kosten zijn USD 0,15 per beeldscherm en bij het afspelen van de indruk en USD 0,25 per video en afdruk.

   * Voor meting met [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* [[!DNL Unified ID 2.0 (UID2.0)]  IDs ](https://unifiedid.com):

   * Voor het opnieuw richten van het programma geopende gebruikers.

     [!DNL UID2 IDs] zijn niet beschikbaar voor gebruikers in de Europese Economische Ruimte en enkele andere landen. Zie de [ lijst van verboden landen ](/help/policies/universal-id-policy.md#prohibited-countries-uid2).

     De kosten zijn USD 0,15 per beeldscherm en bij het afspelen van de indruk en USD 0,25 per video en afdruk.

<!-- Not yet

* Probabilistic (unauthenticated) IDs using hashed email addresses:

  * [[!DNL ID5] IDs](https://id5.io): For retargeting unauthenticated site traffic, prospecting using third-party data, and measurement for both using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md). ID5 IDs are available for no fee.

    ID5 creates an ID by stitching together user signals (hashed email address) with various browser signals (such as IP address and timestamp).

    [!DNL Analytics] measurement requires all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and the [AMO ID and EF ID in your tracking URLs](/help/integrations/analytics/ids.md). You also must sign an agreement with [!DNL ID5] and set a parameter within your existing JavaScript tracking tags. <!-- Contact your Adobe Account Team for instructions. -->

<!--
    >[!NOTE]
    >
    >Third-party segments from [!DNL Eyeota] may automatically include ID5 IDs, in addition to users tracked by cookies or device IDs. The segment details include the size for each type. The usual usage fee for each segment, which is stated next to the segment name, applies; no additional fees are charged for the ID5 IDs.
-->

## Ondersteunde gegevensplatforms van de Klant voor eerste-partijsegmenten

DSP heeft schakelaars aan volgende CDPs gevestigd om uw eerste-partijsegmenten snel in te voeren.

DSP kan ook verbinding maken met aanvullende CDP&#39;s via batch-, streaming- of API-gegevensdeling. Neem contact op met het accountteam van de Adobe als u wilt integreren met een nieuwe CDP.

### [!DNL Adobe Real-Time CDP]

DSP is een geïntegreerde *bestemming* voor [  [!DNL Adobe Real-Time CDP] ](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), die deel van Adobe Experience Platform uitmaakt.

In [!DNL Real-Time CDP] zijn doelen verbindingen met externe gegevensplatforms die een naadloze activering van gegevens mogelijk maken. U kunt bestemmingen gebruiken om uw gehakte e-mailadressen voor gerichte reclame in DSP te activeren. Voor meer informatie over bestemmingen, zie de Gids van de Doelen van het Experience Platform [ ](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), met inbegrip van een overzicht van het product, instructies voor [ het creëren van bestemmingswerkruimten ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) en [ het creëren van bestemmingsverbindingen ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html), en [ het activeren van gegevens aan bestemmingen ](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

Om DSP toe te laten om uw [!DNL Adobe] [!DNL Real-time CDP] eerste-partijsegmenten in te voeren en uw gehakte e-mailadressen in universele IDs om te zetten, zie &quot;[ Gebruiker IDs van  [!DNL Adobe Real-Time CDP]  omzetten in Universal IDs ](/help/dsp/audiences/sources/source-adobe-rtcdp.md).&quot;

### [!DNL ActionIQ]

U kunt de gegevens van de eerste partij van uw organisatie van het [!DNL ActionIQ] klantengegevensplatform met DSP delen om uw gehakte e-mailadressen in universele IDs voor gerichte reclame in DSP om te zetten. Deze integratie vereist aanpassing. Neem contact op met het accountteam van de Adobe voor meer informatie.

### [!DNL Amperity]

U kunt de gegevens van de eerste partij van uw organisatie van het [!DNL Amperity] klantengegevensplatform met DSP delen om uw gehakte e-mailadressen in universele IDs voor gerichte reclame in DSP om te zetten. Voor meer informatie, zie &quot;[ Verandert Gebruiker IDs van  [!DNL Amperity]  in Universal IDs ](/help/dsp/audiences/sources/source-amperity.md).&quot;

### [!DNL Optimizely]

U kunt de gegevens van de eerste partij van uw organisatie van het [!DNL Optimizely] klantengegevensplatform met DSP delen om uw gehakte e-mailadressen in universele IDs voor gerichte reclame in DSP om te zetten. Voor meer informatie, zie &quot;[ Verandert Gebruiker IDs van  [!DNL Optimizely]  in Universal IDs ](/help/dsp/audiences/sources/source-optimizely.md).&quot;

### [!DNL Tealium]

U kunt de gegevens van de eerste partij van uw organisatie van het [!DNL Tealium] klantengegevensplatform delen gebruikend [!DNL Amazon Web Services]. Voor meer informatie over het omzetten van uw gehakte e-mailadressen in universele IDs voor gerichte reclame in DSP, zie &quot;[ Verandert Gebruiker IDs van  [!DNL Tealium]  in Universele IDs ](/help/dsp/audiences/sources/source-tealium.md).&quot;

>[!MORELIKETHIS]
>
>* [ beheert de Bronnen van het Publiek om Universele Soorten van identiteitskaart ](source-manage.md) te activeren
>* [ Steun voor het Activeren van Universal IDs ](/help/dsp/audiences/universal-ids.md)
>* [ zet Gebruiker IDs van  [!DNL Adobe Real-Time CDP]  in Universal IDs ](/help/dsp/audiences/sources/source-adobe-rtcdp.md) om
>* [ zet Gebruiker IDs van  [!DNL Amperity]  in Universal IDs ](/help/dsp/audiences/sources/source-amperity.md) om
>* [ zet Gebruiker IDs van  [!DNL Optimizely]  in Universal IDs ](/help/dsp/audiences/sources/source-optimizely.md) om
>* [ zet Gebruiker IDs van  [!DNL Tealium]  in Universal IDs ](/help/dsp/audiences/sources/source-tealium.md) om
>* [ Ongeveer het Beheer van het Publiek ](/help/dsp/audiences/audience-about.md)
>* [ Montages van de Plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md)
