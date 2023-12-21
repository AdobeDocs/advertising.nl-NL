---
title: Broninstellingen voor publiek
description: Meer informatie over de instellingen voor publieksbronnen.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 6c918b387067237de5d1eae42ae8ad253884d761
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Broninstellingen voor publiek

**[!UICONTROL Data Visibility Level]:** Of de segmenten beschikbaar zijn voor één adverteerder met toegang tot de account (*[!UICONTROL Advertiser]*) of aan alle adverteerders die toegang hebben tot de account *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Alleen de zichtbaarheid op advertentieniveau) De adverteerder voor wie de segmenten beschikbaar zijn. Selecteer een optie in de lijst met adverteerders die toegang hebben tot het account.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] alleen bronnen) De Adobe Experience Cloud-organisatie-id voor de [!DNL Adobe Experience Platform] account.

**[!UICONTROL Convert PII to the following IDs]:** ([!DNL ActionIQ] en [!DNL Tealium] alleen bronnen) Het id-type waarnaar u uw persoonlijk identificeerbare gegevens wilt converteren. Gegevensheffingen worden dienovereenkomstig toegepast.

* *[!DNL RampID]:* PII omzetten in een RampID. Als u *[!DNL RampID]*, uw segmenten worden omgezet in [!DNL RampIDs] automatisch.

* *[!DNL Unified ID2.0]:* ([!DNL ActionIQ] alleen bronnen) Om PII om te zetten in een [Unified ID 2.0](https://unifiedid.com/).

**[!UICONTROL Source Key]:** (Alleen-lezen; automatisch gegenereerd) De bronsleutel die u kunt gebruiken om een doelverbinding te maken in het platform met klantgegevens om het publiek naar DSP te duwen. U kunt de waarde naar het klembord kopiëren en deze in de instellingen voor de doelverbinding of in een bestand plakken.

>[!MORELIKETHIS]
>
>* [Creeer een Bron van het Publiek om Eerste Publiek te activeren](source-create.md)
>* [Ongeveer het Activeren van Authenticated Segmenten van de Bronnen van het Publiek](source-about.md)
>* [Activeer Erkende Segmenten van de Universele Partners van identiteitskaart](source-universal-id.md)
>* [Adobe Advertising DSP-verbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
