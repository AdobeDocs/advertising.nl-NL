---
title: Geverifieerde segmenten handmatig importeren uit [!DNL LiveRamp]
description: Ervaar meer over het activeren van geverifieerde doelgroepen via [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# Geverifieerde segmenten handmatig importeren uit [!DNL LiveRamp]

*Beta, functie*

U kunt geverifieerde gegevens handmatig verzenden [!DNL LiveRamp] segmenten die moeten worden DSP [!DNL LiveRamp] [!DNL Connect] dashboard. U kunt geïmporteerde segmenten gebruiken voor plaatsing als doel. Voor de segmenten van de eerste partij bedragen de vergoedingen 0,15 USD per geleverde display en indruk en 0,25 USD per video en indruk.

Het in kaart brengen en uploaden van segmenten voor elke invoerbaan kan tot zeven dagen duren.

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. Voer de volgende stappen uit in het dialoogvenster [!DNL Connect] dashboard:

   1. De doeltegel activeren **[!DNL AAC API 1P Onboarding]**.

   1. Set [!DNL Identifier Settings] tot **[!DNL Ramp ID]** alleen.

      ![Instellingen voor id](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Optioneel) Als u nog steeds op cookies gebaseerde id&#39;s wilt ontvangen, maakt u een tweede id [!DNL AAC API 1P Onboarding] doeltegel met &quot;[!DNL Cookies],&quot; &quot;[!DNL IDFA],&quot; en &quot;[!DNL AAID]&quot; geselecteerd.

   1. Verifieer in uw publieksbibliotheek (die beschikbaar is wanneer u een publiek maakt of bewerkt vanuit [!UICONTROL Audiences] > [!UICONTROL All Audiences] of binnen plaatsingsinstellingen) dat het gehele aantal segmenten is geïmporteerd.

>[!MORELIKETHIS]
>
>* [Ongeveer de Bronnen van het Publiek van de Eerste Partij](source-about.md)
>* [Bronnen voor publiek beheren om Universal ID-publiek te activeren](source-manage.md)
>* [Adobe Advertising DSP-verbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=nl-NL)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
