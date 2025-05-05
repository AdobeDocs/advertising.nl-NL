---
title: Broninstellingen voor publiek
description: Meer informatie over de instellingen voor publieksbronnen.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Broninstellingen voor publiek

*Beta, functie*

**[!UICONTROL Data Visibility Level]:** Of de segmenten beschikbaar zijn voor één adverteerder met toegang tot de account (*[!UICONTROL Advertiser]*) of aan alle adverteerders die toegang hebben tot de account *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Alleen de zichtbaarheid op advertentieniveau) De adverteerder voor wie de segmenten beschikbaar zijn. Selecteer een optie in de lijst met adverteerders die toegang hebben tot het account.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] alleen bronnen) De Adobe Experience Cloud-organisatie-id voor de [!DNL Adobe Experience Platform] account.

**[!UICONTROL Convert PII to the following IDs]:** De id-typen waarnaar u uw persoonlijk identificeerbare gegevens (PII) converteert. Als u meerdere typen selecteert, wordt het gegenereerde segment gevuld met waarden voor elk geselecteerd id-type (zoals een [!DNL RampID] en [!DNL Unified ID2.0] voor elk e-mailadres). Gegevensheffingen worden dienovereenkomstig toegepast.

Voor [!DNL RampID] en [!DNL Unified ID2.0], zoekt de leverancier elk e-mailadres op om te zien of er al een id bestaat en zet het adres om in een overeenkomstige id, indien beschikbaar. Als er geen id voor het adres bestaat, wordt er een nieuwe id gemaakt.

>[!NOTE]
>
>U kunt slechts één type id in één plaatsing als doel instellen. Prestaties testen op ID-type [een aparte plaatsing maken](/help/dsp/campaign-management/placements/placement-create.md) voor elk type ID in het segment.

* *[!DNL RampID]:* PII omzetten in een [!DNL RampID]. U kunt [!DNL RampIDs] voor het opnieuw richten van login gebruikers en voor [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) meting.

* *[!DNL Unified ID2.0] (Beta):* PII omzetten in een [Unified ID 2.0](https://unifiedid.com) ID voor het opnieuw richten van login gebruikers.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** De serviceovereenkomst voor de conversie van PII naar universele id&#39;s. U of een andere gebruiker in de DSP account moet de voorwaarden één keer accepteren voordat u gegevens kunt converteren naar een nieuw id-type. Voor klanten met beheerde de dienstcontracten, zal uw Team van de Rekening van de Adobe uw toestemming krijgen en zal de termijnen namens uw organisatie goedkeuren. Als u de voorwaarden wilt lezen, klikt u op **>**. Als u de voorwaarden wilt accepteren, schuift u naar de onderkant van de voorwaarden en klikt u op **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Alleen-lezen; automatisch gegenereerd) De bronsleutel die u kunt gebruiken om een doelverbinding te maken in het platform met klantgegevens om het publiek naar DSP te duwen. U kunt de waarde naar het klembord kopiëren en deze in de instellingen voor de doelverbinding of in een bestand plakken.

>[!MORELIKETHIS]
>
>* [Bronnen voor publiek beheren om Universal ID-publiek te activeren](source-manage.md)
>* [Ongeveer de Bronnen van het Publiek van de Eerste Partij](source-about.md)
>* [Geverifieerde segmenten handmatig importeren uit [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Adobe Advertising DSP-verbinding](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Informatie over Audience Management](/help/dsp/audiences/audience-about.md)
