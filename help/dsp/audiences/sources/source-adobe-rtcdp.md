---
title: "Workflow voor het gebruik van de DSP integratie met [!DNL Adobe] [!DNL Real-time CDP]"
description: "Leer hoe u DSP kunt inschakelen om uw [!DNL Adobe] [!DNL Real-time CDP] eerste-partijsegmenten."
feature: DSP Audiences
source-git-commit: fb42e4aacaf0ea22890e0b4a46719725c99fffdc
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Workflow voor het gebruik van de DSP integratie met [!DNL Adobe Real-Time CDP]

1. [DSP toestaan om klantgegevenssegmenten te vertalen in [!DNL LiveRamp RampIDs]](source-universal-id.md) die herkenbaar zijn in een biedbare omgeving.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your Adobe Account Team will perform this configuration. -->

1. [Een publieksbron maken](source-create.md) om soorten publiek te importeren naar uw DSP of een adverteerderaccount.

1. In Experience Platform, vorm een Advertising DSP bestemmingsverbinding gebruikend [!UICONTROL Source Key] die is gegenereerd in de DSP broninstellingen.

   Voor instructies voor het activeren van de DSP bestemmingsverbinding, het selecteren van segmenten, en de toegang tot van controletoestemmingen, zie &quot;[Adobe Advertising Cloud DSP-verbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

Neem voor extra ondersteuning contact op met het accountteam van de Adobe of `adcloud-support@adobe.com`.


>[!MORELIKETHIS]
>
>* [Activeer Erkende Segmenten van de Universele Partners van identiteitskaart](source-universal-id.md)
>* [Creeer een Bron van het Publiek om Eerste Publiek te activeren](source-create.md)
>* [Broninstellingen voor publiek](source-settings.md)
>* [Adobe Advertising DSP-verbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Overzicht van de doelcatalogus](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Workflow voor het gebruik van de DSP integratie met [!DNL Tealium]](/help/dsp/audiences/sources/source-tealium.md)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
