---
title: Broninstellingen voor publiek
description: Meer informatie over de instellingen voor publieksbronnen.
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: d6416dae58543e1287b7af7df44eada4be023731
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Broninstellingen voor publiek

*eigenschap van Beta*

**[!UICONTROL Data Visibility Level]:** Of de segmenten aan één enkele adverteerder met toegang tot de rekening (*[!UICONTROL Advertiser]*) of aan alle adverteerders met toegang tot de rekening *[!UICONTROL Account]* beschikbaar zijn.

**[!UICONTROL Advertiser]:** (Advertiser-vlakke zicht slechts) de adverteerder voor wie de segmenten beschikbaar zijn. Selecteer een optie in de lijst met adverteerders die toegang hebben tot het account.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] slechts bronnen) de organisatie-ID van Adobe Experience Cloud voor de [!DNL Adobe Experience Platform] rekening.

**[!UICONTROL Convert PII to the following IDs]:** De types van identiteitskaart waaraan u uw persoonlijk identificeerbare informatie (PII) zult omzetten. Als u meerdere typen selecteert, wordt het gegenereerde segment gevuld met waarden voor elk geselecteerd id-type (bijvoorbeeld een [!DNL RampID] en een [!DNL Unified ID2.0] voor elk e-mailadres). Gegevensheffingen worden dienovereenkomstig toegepast.

Voor [!DNL RampID] en [!DNL Unified ID2.0] zoekt de leverancier elk e-mailadres om te controleren of er al een id bestaat en zet het adres om in een overeenkomende id, indien beschikbaar. Als er geen id voor het adres bestaat, wordt er een nieuwe id gemaakt.

>[!NOTE]
>
>U kunt slechts één type id in één plaatsing als doel instellen. Om prestaties door type van identiteitskaart te testen, [ creeer een afzonderlijke plaatsing ](/help/dsp/campaign-management/placements/placement-create.md) voor elk type van identiteitskaart in het segment.

* *[!DNL RampID]:* PII in a om te zetten [!DNL RampID]. U kunt [!DNL RampIDs] gebruiken voor het opnieuw toewijzen van gebruikers die zich aanmelden en voor [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) metingen.

* *[!DNL Unified ID2.0](Beta):* om PII in a [ Verenigde identiteitskaart 2.0 ](https://unifiedid.com) identiteitskaart voor het opnieuw richten van het programma-binnen gebruikers om te zetten.

<!--
 Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** De serviceovereenkomst voor het converteren van PII naar universele id&#39;s. Je of een andere gebruiker in de DSP-account moet de voorwaarden één keer accepteren voordat je gegevens kunt converteren naar een nieuw ID-type. Voor klanten met beheerde servicecontracten krijgt uw Adobe-accountteam uw toestemming en accepteert u de voorwaarden namens uw organisatie. Om de termijnen te lezen, klik **>**. Schuif naar de onderkant van de voorwaarden en klik op **[!UICONTROL Accept]** om de voorwaarden te accepteren.

**[!UICONTROL Source Key]:** (Alleen-lezen; automatisch gegenereerd) De bronsleutel die u kunt gebruiken om een doelverbinding in het klantgegevensplatform te maken om een publiek naar Advertising DSP te sturen. U kunt de waarde naar het klembord kopiëren en deze in de instellingen voor de doelverbinding of in een bestand plakken.

>[!MORELIKETHIS]
>
>* [ beheert publieksbronnen om universele identiteitskaart te activeren ](source-manage.md)
>* [ Ongeveer eerste-partijpublieksbronnen ](source-about.md)
>* [ voert manueel geverifieerde segmenten van  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md) in
>* [ verbinding van Adobe Advertising DSP ](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [ Ongeveer publieksbeheer ](/help/dsp/audiences/audience-about.md)
