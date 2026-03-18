---
title: Handmatig geverifieerde segmenten importeren uit  [!DNL LiveRamp]
description: Leer over het activeren van voor authentiek verklaard publiek door  [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 21ed5558a39ea9b097be8e70ef81bcf8e59c14b4
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# Geautoriseerde segmenten handmatig importeren uit [!DNL LiveRamp]

*eigenschap van Beta*

Met het dashboard [!DNL LiveRamp] [!DNL LiveRamp] kunt u geverifieerde [!DNL Connect] -segmenten handmatig naar DSP verzenden. U kunt geïmporteerde segmenten gebruiken voor plaatsing als doel. Voor de segmenten van de eerste partij bedragen de vergoedingen 0,15 USD per geleverde display en indruk en 0,25 USD per video en indruk.

Het in kaart brengen en uploaden van segmenten voor elke invoerbaan kan tot zeven dagen duren.

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. Voer de volgende stappen uit in het dashboard van [!DNL Connect] :

   1. Activeer de doeltegel **[!DNL AAC API 1P Onboarding]** .

   1. Stel [!DNL Identifier Settings] alleen in op **[!DNL Ramp ID]** .

      ![&#x200B; montages van het Herkenningsteken &#x200B;](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Optioneel) Als u nog steeds op cookies gebaseerde id&#39;s wilt ontvangen, maakt u een tweede [!DNL AAC API 1P Onboarding] doeltegel met &quot;[!DNL Cookies]&quot;, &quot;[!DNL IDFA]&quot; en &quot;[!DNL AAID]&quot; geselecteerd.

   1. Controleer in de publieksbibliotheek (die beschikbaar is wanneer u een publiek maakt of bewerkt vanuit [!UICONTROL Audiences] > [!UICONTROL All Audiences] of binnen de plaatsingsinstellingen) of het gehele aantal segmenten is geïmporteerd.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer de Bronnen van het Publiek van de Eerste Partij &#x200B;](source-about.md)
>* [&#x200B; beheert de Bronnen van het Publiek om Universele Soorten van identiteitskaart &#x200B;](source-manage.md) te activeren
>* [&#x200B; Verbinding van Adobe Advertising DSP &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [&#x200B; Ongeveer het Beheer van het Publiek &#x200B;](/help/dsp/audiences/audience-about.md)
