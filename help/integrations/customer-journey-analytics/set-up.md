---
title: Gegevensverzameling, gegevensoverdracht en rapportage instellen
description: Leer hoe u gegevensverzameling, gegevensoverdracht en rapportage instelt.
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: 2d6cba8d5a3d966b272c5048404ac8fdf0185b74
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---

# Gegevensverzameling, gegevensoverdracht en rapportage instellen

*eigenschap van Beta*

De volgende taken zijn vereist voor het weergeven van Cloud-advertentiegegevens in Customer Journey Analytics.

1. (Het Webanalist van uw organisatie; facultatief) [ verzamel historische gegevens voor AMO IDs en EF IDs ](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}.

   Deze stap is alleen van toepassing voor adverteerders met [!DNL Analytics for Advertising] .

1. (Uw de plaatsbeheerder van uw organisatie voor Adobe Experience Platform) [ de inzameling van opstellingsgegevens in Experience Platform en voert omzetting volgende markeringen ](#data-collection) uit.

1. (Uw de plaatsbeheerder van uw organisatie voor Customer Journey Analytics) [ creeert een verbinding aan uw datasets van Experience Platform in Customer Journey Analytics ](#dataset-connection).

1. (Het Webanalist van uw organisatie) [ de meningen van opstellingsgegevens in Customer Journey Analytics ](#cja-data-views).

1. (Het Webanalist van uw organisatie) [ de rapporten en visualisaties van de Opstelling in Customer Journey Analytics Workspace ](#cja-reports).

De volgende secties bevatten gedetailleerde procedures, die de taken en instellingen omvatten die voor de integratie zijn vereist, maar waarin niet alle functies worden uitgelegd die beschikbaar zijn in de workflows. Zie de gekoppelde bronnen voor volledige informatie.

## Gegevensverzameling instellen in Adobe Experience Platform en op uw website {#data-collection}

De volgende taken zijn vereist om gegevensverzameling in Experience Platform in te stellen en conversietags te implementeren. De sitebeheerder van uw organisatie voor Experience Platform kan deze taken uitvoeren, maar de IT-afdeling van uw organisatie kan hulp nodig hebben bij het implementeren van trackingtags.

1. Gegevens van Adobe Advertising als dataset verzamelen en naar Experience Platform Edge Network verzenden:

   1. In Experience Platform, [ bepaal een handschema ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas) voor de gegevens u wilt verzamelen gebruikend het Model van de Gegevens van de Ervaring (XDM).

      * Selecteer [!UICONTROL Schema Details] in het **[!UICONTROL Experience Event]** als basisklasse voor het schema om site-gebeurtenissen vast te leggen. Geef het schema een naam en klik op **[!UICONTROL Finish]** .

      * Voeg in het linkerdeelvenster de veldgroep `Adobe Advertising Cloud ExperienceEvent Full Extension` toe om velden toe te voegen die specifiek zijn voor Adobe Advertising.<!-- Add link once published --> Bij een minimum, omvat het voorwerp conversionDetails met `trackingCode` en `trackingIdentities` eigenschappen, die [ identiteitskaart van AMO en EF identiteitskaart ](ids.html) omvatten. De andere velden zijn optioneel.

      * (Optioneel) Voeg zo nodig extra veldgroepen toe om extra gegevensvelden te koppelen aan Adobe Advertising-gegevens.

      **Nota:** u kunt veelvoudige schema&#39;s tot stand brengen, maar u kunt slechts één schema per dataset en per gegevensstroom gebruiken, die u in de volgende stappen zult creëren.

   1. [ creeer een dataset ](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create) die op het schema wordt gebaseerd om de inzameling van gebeurtenisgegevens op te slaan en te beheren.

      * Kies de optie **[!UICONTROL Create dataset from schema]** en selecteer het schema.

        Adobe Advertising maakt aanvullende gegevenssets voor de gerelateerde gegevens over samenvattingsmetriek (zoals omzettingswaarden) en opzoekgegevens (afmetingen/classificatiemetagegevens, zoals de naam van de Adobe Advertising-campagne) op basis van uw gebeurtenisdataset. De gegevens voor de datasets worden dagelijks in Experience Platform ingevuld.

   1. [ creeer een gegevensstroom ](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) voor het schema.

      * Selecteer het schema voor de instelling [!UICONTROL Mapping schema] .

      * Voeg de services `Adobe Advertising` en `Adobe Experience Platform` toe aan de gegevensstroom en schakel deze in.

        Deze diensten laten de Edge Network toe om de dataset op te slaan en het aan Adobe Advertising te leiden.

      * Selecteer uw gegevensset voor de instelling [!UICONTROL Event dataset] .

        Elke gegevensstroom kan gegevens in slechts één dataset opnemen.

1. Verzend de websitegegevens van uw organisatie naar uw Experience Platform-gegevensstroom:

   1. De markeringen van Experience Platform van het gebruik [ (vroeger gekend als ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home)) om een markering van JavaScript te produceren om de websitegegevens van uw organisatie naar de datastream te verzenden.[!DNL Launch]

      * Maak een eigenschap tag, de container voor de tagconfiguratie.

      * Voor uw bezit, [ installeer de uitbreiding &quot;Adobe Experience Platform Web SDK&quot;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) van de uitbreidingscatalogus.

        Deze extensie verzendt gegevens van uw wegeigenschappen naar Experience Cloud via de Experience Platform Edge Network.

        Gebruik de extensie Adobe Advertising niet.

      * Een aangepaste Web SDK-build maken:

         * In de [!UICONTROL Custom build components] sectie, laat de **Advertising** component toe.

           Deze component bevat alle JavaScript-code die nodig is voor Adobe Advertising in de tag. Er wordt ook een &quot;Advertising&quot;-instelling toegevoegd aan tagregels (optioneel) om te bepalen hoe advertentiegegevens worden gebruikt voor attributiemeting.

           U kunt desgewenst aanvullende componenten inschakelen.

         * In de sectie [!UICONTROL SDK Instances] :

            * Selecteer in de [!UICONTROL Datastreams] -instellingen de gegevensstroom die u voor elk van uw webomgevingen wilt gebruiken (productie, staging, ontwikkeling).

            * (Alleen organisaties met Adobe Advertising DSP) In de [!UICONTROL Adobe Advertising] -instellingen:

               * Schakel de instelling **[!UICONTROL Adobe Advertising DSP]** in om doorzicht bijhouden in te schakelen.

               * Geef de adverteerders op waarvoor doorzicht mogelijk moet zijn.

               * (Optioneel) Voer de id5-partner van uw organisatie in om id&#39;s te verzamelen.

               * (Optioneel) Voer het pad in voor de [!DNL LiveRamp RampID] JavaScript-code (ats.js) van uw organisatie voor het verzamelen van id&#39;s.

            * Sla de build op.

      * (Facultatief) [ creeer regels ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules) zoals nodig om te bepalen wanneer het Web SDK gegevens naar Edge Network zou moeten verzenden.

         * Definieer bij de instelling [!UICONTROL Advertising] hoe advertentiegegevens worden gebruikt voor attributiemeting. Dit het plaatsen is nuttig wanneer de regel een opeenvolging van veelvoudige acties omvat en beschikbaar slechts wanneer u &quot; [!UICONTROL Advertising]&quot;component voor de douane hebt geselecteerd bouwt component. U kunt onder andere de volgende opties kiezen:

           *Automatisch:* staat reclamegegevens toe om voor het meten en attributie op de huidige `sendEvent` actie worden gebruikt die op gegevens in het geheime voorgeheugen wordt gebaseerd. In dit geval wordt de gebeurtenis advertentie geactiveerd wanneer deze de kans krijgt en is deze mogelijk niet beschikbaar voor de huidige gebeurtenis. Als u bijvoorbeeld een aankoopgebeurtenis activeert en er geen advertentiegegevens beschikbaar zijn in de cache, wordt de uitcheckgebeurtenis niet toegewezen aan de advertentiepositie.

           *wacht:* vertraagt de uitvoering van de vraag tot de reclamegegevens met succes van de server worden teruggewonnen en worden opgelost, die nauwkeurige attributiemeting verzekert. U kunt bijvoorbeeld wachten tot de advertentiegebeurtenis is opgelost voordat u een afhandelingsgebeurtenis activeert. **Nota:** Het oplossen IDs kan een paar seconden afhankelijk van browser en het type van identiteitskaart vergen. Gebruik deze optie als de huidige `sendEvent` actie een paar seconden vertraging kan verwerken.

           *Gehandicapten:* (het gebrek) sluit reclamegegevens van het verzoek uit dat u, makend het niet voor attributie of het verwante volgen vuurt.

           *verstrek een gegevenselement:* gebruik een gegevenselement om reclamegegevens tijdens paginading te omvatten of uit te sluiten. De opgeloste waarden voor het gegevenselement kunnen `automatic`, `wait`, en `disabled` omvatten. Zie de volgende stap.

        Als u geen regel gebruikt om een `sendEvent` actie te vormen, dan worden de reclamegegevens verzonden als afzonderlijke Advertisement verrijkingsgebeurtenis.

      * Creeer [ gegevenselementen ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) zoals nodig om variabelen op uw website aan de structuur van het XDM schema in kaart te brengen u eerder creeerde.

   1. [ publiceer de markering ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) aan een testmilieu waarin u op de ontwikkeling van markeringen kunt herhalen.

   1. Valideer levering van de datasets, en dan [ publiceer de markering aan uw levende productiemilieu ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow).

      De IT-afdeling of andere groep van uw organisatie moet mogelijk de implementatie van tags plannen of hierover worden geïnformeerd.

## Verbinding maken met uw Experience Platform-gegevenssets in Customer Journey Analytics {#dataset-connection}

Voer de volgende stappen uit om Adobe Advertising-gegevens van uw Experience Platform-gegevenssets naar Customer Journey Analytics te halen. De sitebeheerder van uw organisatie voor Customer Journey Analytics kan deze taken uitvoeren.

*Binnenkort*

## Gegevensweergaven instellen in Customer Journey Analytics {#cja-data-views}

In Customer Journey Analytics maakt u een of meer gegevensweergaven om de maatstaven en afmetingen voor rapportage te definiëren. Een webanalist kan deze taken uitvoeren.

*Binnenkort*

## Rapporten en visualisaties instellen in Customer Journey Analytics Workspace {#cja-reports}

Voer in Customer Journey Analytics Workspace de volgende stappen uit om rapporten en visualisaties te configureren. Een webanalist kan deze taken uitvoeren.

1. [ creeer een project ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) in Workspace om rapporten en visualisaties te bouwen die op de afmetingen en metriek worden gebaseerd die binnen de gegevensmening worden gevormd.

1. (Als u gegevens van [!DNL Google Ads] of [!DNL Microsoft Advertising] hebt) Maak een rapport van door de uitgever bijgehouden omzettingen met velden voor netwerkspecifieke metriek, die worden gegroepeerd als `googleConversions` en `microsoftConversions` .

>[!MORELIKETHIS]
>
>* [ Overzicht ](overview.md)
>* [ Eerste vereisten ](prerequisites.md)
>* [ Adobe Advertising IDs die door  [!DNL Customer Journey Analytics]](ids.md) wordt gebruikt
>* [ de metriek en de afmetingen van Adobe Advertising in Customer Journey Analytics ](advertising-data-in-cja.md)
>* [ verzamel Historische Gegevens voor AMO IDs en EF IDs voor Gebruik in Adobe Customer Journey Analytics ](/help/integrations/analytics/rvars-to-evars.md).
>* [ Gids van Customer Journey Analytics ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* Customer Journey Analytics [ gids van de Gebruiker voor de gebruikers van Adobe Analytics ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
