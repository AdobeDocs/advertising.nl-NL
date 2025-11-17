---
title: Gegevensverzameling, gegevensoverdracht en rapportage instellen
description: Leer hoe u gegevensverzameling, gegevensoverdracht en rapportage instelt.
feature: Integration with Adobe Customer Journey Analytics
exl-id: a955e2b0-ea1b-4b5c-937b-f8c66603cd36
source-git-commit: 168a43e0d3b7ccf5e519d76bcbb6bb955fada7e8
workflow-type: tm+mt
source-wordcount: '1567'
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

### Gegevens van Adobe Advertising als dataset verzamelen en verzenden naar Experience Platform Edge Network

1. In Experience Platform, [ bepaal een handschema ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas) voor de gegevens u wilt verzamelen gebruikend het Model van de Gegevens van de Ervaring (XDM).

   * Selecteer [!UICONTROL Schema Details] in het **[!UICONTROL Experience Event]** als basisklasse voor het schema om site-gebeurtenissen vast te leggen. Geef het schema een naam en klik op **[!UICONTROL Finish]** .

   * Voeg in het linkerdeelvenster de veldgroep `[Adobe Advertising Cloud ExperienceEvent Full Extension](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension)` toe om velden toe te voegen die specifiek zijn voor Adobe Advertising. Bij een minimum, omvat het voorwerp conversionDetails met `trackingCode` en `trackingIdentities` eigenschappen, die [ identiteitskaart van AMO en EF identiteitskaart ](ids.md) omvatten. De andere velden zijn optioneel.

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

### De websitegegevens van uw organisatie naar uw Experience Platform-gegevensstroom verzenden

1. De markeringen van Experience Platform van het gebruik [ (vroeger gekend als ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home)) om een markering van JavaScript te produceren om de websitegegevens van uw organisatie naar de datastream te verzenden.[!DNL Launch]

   * Maak een eigenschap tag, de container voor de tagconfiguratie.

   * Voor uw bezit, [ installeer de uitbreiding &quot;Adobe Experience Platform Web SDK&quot;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) van de uitbreidingscatalogus.

     Deze extensie verzendt gegevens van uw wegeigenschappen naar Experience Cloud via de Experience Platform Edge Network.

     Gebruik de extensie Adobe Advertising niet.

   * Creeer de bouwstijl van SDK van het a [ douaneWeb ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build):

      * In de [!UICONTROL Custom build components] sectie, laat de **Advertising** component toe.

        Deze component bevat alle JavaScript-code die nodig is voor Adobe Advertising in de tag. Er wordt ook een &quot;Advertising&quot;-instelling toegevoegd aan tagregels (optioneel) om te bepalen hoe advertentiegegevens worden gebruikt voor attributiemeting.

        U kunt desgewenst aanvullende componenten inschakelen.

      * In de sectie [!UICONTROL SDK Instances] :

         * Selecteer in de [!UICONTROL Datastreams] -instellingen de gegevensstroom die u voor elk van uw webomgevingen wilt gebruiken (productie, staging, ontwikkeling).

         * (Organisaties met alleen Adobe Advertising DSP) Schakel in de [[!UICONTROL Adobe Advertising] instellingen ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#general) **[!UICONTROL Adobe Advertising DSP]** in om doorzicht mogelijk te maken en geef de adverteerders op waarvoor ze doorzicht moeten inschakelen. U kunt desgewenst id&#39;s verzamelen van universele id&#39;s.

         * Sla de build op.

   * (Facultatief) [ creeer regels ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules) zoals nodig om te bepalen wanneer het Web SDK gegevens naar Edge Network zou moeten verzenden.

      * Voor `[sendEvent](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/action-types#send-event)` acties, gebruik [[!UICONTROL Advertising] het plaatsen ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/action-types#advertising) om te bepalen hoe de reclamegegevens voor attributiemeting worden gebruikt. Dit het plaatsen is nuttig wanneer de regel een opeenvolging van veelvoudige acties omvat en beschikbaar slechts wanneer u &quot; [!UICONTROL Advertising]&quot;component voor de douane hebt geselecteerd bouwt component.

   * Creeer [ gegevenselementen ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) zoals nodig om variabelen op uw website aan de structuur van het XDM schema in kaart te brengen u eerder creeerde.

1. [ publiceer de markering ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) aan een testmilieu waarin u op de ontwikkeling van markeringen kunt herhalen.

1. Valideer levering van de datasets, en dan [ publiceer de markering aan uw levende productiemilieu ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow).

   De IT-afdeling of andere groep van uw organisatie moet mogelijk de implementatie van tags plannen of hierover worden geïnformeerd.

## Verbinding maken met uw Experience Platform-gegevenssets in Customer Journey Analytics {#dataset-connection}

Voer de volgende stappen uit om Adobe Advertising-gegevens van uw Experience Platform-gegevenssets naar Customer Journey Analytics te halen. De sitebeheerder van uw organisatie voor Customer Journey Analytics kan deze taken uitvoeren.

1. In Customer Journey Analytics, [ creeer een verbinding ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection) die uw datasets en schema van Experience Platform omvat.

   **Nota:** momenteel, moet u gegevens voor alle DSP en Onderzoek, Sociale, &amp; rekeningen van Commerce naar één enkele instantie en zandbak van Experience Platform verzenden.

   * Voeg uw Experience Platform-gegevensset (metriek), overzichtsgegevensset (metriek) en dimensies (classificaties/metagegevens) toe.

     Uw team creeerde de gebeurtenisdataset, en Adobe Advertising creeerde de samenvatting en dimensies datasets die op uw gebeurtenisdataset worden gebaseerd.

     U kunt desgewenst aanvullende gegevenssets opnemen.

   * Wijs de dimensies dataset aan de gebeurtenissendataset toe:

      1. Open de montages voor de afmetingsdataset.

         De rubriek op de montagespagina is &quot;[!UICONTROL Lookup Dataset],&quot;die erop wijst dat u uw dimensiedataset met één van uw metrisch-specifieke datasets kunt aansluiten.

      1. Wijs in de sectie [!UICONTROL Adobe Advertising Dimensions] de dimensies van de dataset toe aan de gebeurtenissendataset:

         1. Selecteer voor het veld [!UICONTROL Key] het veld dat u wilt gebruiken als de sleutel voor de gegevensset afmetingen: `Adobe Advertising ID` (dit is hetzelfde als het veld `trackingCode` in het schema).

         1. Selecteer voor het veld [!UICONTROL Matching key] het veld dat u wilt gebruiken als de overeenkomende sleutel voor de gegevensset met gebeurtenissen. De beschikbare veldnamen bevatten de naam van de gegevensset tussen haakjes. Bijvoorbeeld, als u uw dimensiedataset aan uw gebeurtenissendataset in kaart brengt, selecteer `Tracking Code (Event datasets)`.

         Later, zult u de gebeurtenissendataset aan de summiere dataset ook in kaart brengen wanneer u opstelling uw gegevensmening (#cja-data-views).

1. Controleer na een paar uur of de gegevens beschikbaar zijn in Customer Journey Analytics.

   1. Ga in Customer Journey Analytics naar **[!UICONTROL Connections]** en selecteer uw verbinding.

   1. In de lijst van getoonde gegevensreeksen, verifieer dat &quot;[!UICONTROL Number of Records]&quot;rapport toont dat het gegeven werd toegevoegd.

## Gegevensweergaven instellen in Customer Journey Analytics {#cja-data-views}

In Customer Journey Analytics maakt u een of meer gegevensweergaven om de maatstaven en afmetingen voor rapportage te definiëren. Een webanalist kan deze taken uitvoeren.

1. In Customer Journey Analytics, [ creeer een gegevensmening ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview).

1. Vorm de mening om de volgende informatie te omvatten.

   * Als u een Adobe Analytics-account hebt, gebruikt u [!UICONTROL Time Zone] voor uw [!DNL Analytics] -account in de sectie [!UICONTROL Calendar] van het tabblad [!UICONTROL Configure] .

   * Op het tabblad [!UICONTROL Components] :

      * Voeg uw dimensies, gebeurtenissen, en summiere datasets toe.

      * Kies metriek van uw gebeurtenissen (metriek) dataset en uw dimensies (classificaties/meta-gegevens) dataset om in de gegevensmening te omvatten.

        U ging reeds bij deze twee datasets in de verbinding die u in de [ laatste procedure ](#dataset-connection) creeerde.

      * Sluit zich aan bij de gebeurtenissendataset aan de summiere dataset, die nog niet aan bij om het even welk wordt aangesloten:

         * Voor elke afmeting met summiere gegevens die u in Customer Journey Analytics beschikbaar wilt zijn, [ creeer een afgeleid gebied ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/derived-fields).

           Als u bijvoorbeeld samenvattingsgegevens voor campagnes wilt weergeven, maakt u een afgeleid veld voor de dimensie `Adobe Advertising Campaign` .

           U koppelt de twee datasets gebruikend de passende sleutel `trackingCode` (die het schemagebied voor identiteitskaart van Adobe Advertising is).

            * In de [!UICONTROL Lookup] sectie van de afgeleide regelbouwer:

               * Voor het **[!UICONTROL Value]** gebied, selecteer &quot;[!UICONTROL Tracking Code]&quot;van de summiere dataset van metriek.

               * Selecteer voor het veld **[!UICONTROL Lookup dataset]** de gegevensset met afmetingen (zoals &quot;Adobe Advertising Classification&quot;).

               * Voor het **[!UICONTROL Matching Key]** gebied, selecteer &quot;[!UICONTROL Tracking Code]&quot;van de classificatiedataset.

               * Voor het **[!UICONTROL Values to return]** gebied, selecteer de afmeting (zoals &quot;[!UICONTROL Adobe Advertising Campaign]&quot;)&quot;van de classificatiedataset.

           De afgeleide veldnaam wordt toegevoegd met &quot;(DF)&quot;, zoals `Adobe Advertising Campaign(DF)`.

         * Voor elk afgeleid veld:

            * Voeg in de sectie [!UICONTROL Included components] het afgeleide veld toe.

              Twee namen worden nu vermeld voor dezelfde dimensie (bijvoorbeeld &quot;Adobe Advertising Campaign(DF)&quot; (het afgeleide veld) en &quot;Adobe Advertising Campaign&quot; (het veld in de summiere dataset)).

            * Selecteer de dimensie in de summiere dataset (zoals &quot;Campagne van Adobe Advertising&quot;) en geef de montages voor de dataset uit.

              De instellingen worden rechts geopend.

               * Selecteer in de sectie Samenvattingsgegevensgroep de optie die u wilt **[!UICONTROL Create grouping]** .

               * Selecteer voor het veld **[!UICONTROL Dimension]** het afgeleide veld (dat wordt toegevoegd met &quot;(DF)&quot;, zoals &quot;Adobe Advertising Campaign(DF)&quot;).

               * Selecteer de optie voor **[!UICONTROL Hide in reporting]** , die de afgeleide veldnaam in Workspace verbergt.

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
