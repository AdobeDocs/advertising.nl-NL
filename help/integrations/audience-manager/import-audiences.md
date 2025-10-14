---
title: Adobe Audience Manager-segmenten importeren voor advertentiedoeleinden
description: Leer hoe te om uw  [!DNL Adobe]  publiek in Advertising DSP en Onderzoek in te voeren gebruikend Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Adobe Audience Manager-segmenten importeren voor advertentiedoeleinden

Advertising DSP en [!DNL Advertising Search, Social, & Commerce] kunnen elk metagegevens, hiërarchiegegevens en unieke publieksgegevens ophalen voor het [!DNL Adobe] publiek <!-- segments or audiences? Standardize terms per AAM's docs --> van alle adverteerders of bureaus, waaronder:

* Adobe Audience Manager-segmenten

* Adobe Analytics-segmenten die naar Adobe Experience Cloud worden gepubliceerd

* Segmenten die zijn gemaakt met de Adobe Experience Cloud [!DNL Audience Library]

* Segmenten die in Adobe Experience Platform zijn gemaakt en via Audience Manager naar Adobe Advertising zijn verzonden

Als u toegang wilt tot [!DNL Adobe] publiek in DSP of [!DNL Creative] , moet u het publiek importeren in DSP. Als u toegang wilt krijgen tot [!DNL Adobe] publiek in [!DNL Search, Social, & Commerce] , moet u het publiek importeren in [!DNL Search, Social, & Commerce] .

## Vereisten

* De adverteerder moet [&#x200B;  [!DNL Adobe Experience Cloud Identity (ECID) Service] &#x200B;](https://experienceleague.adobe.com/nl/docs/id-service/using/intro/overview) versie 2.0 of hoger uitvoeren. [!DNL Identity Service] biedt een universele, permanente id die uw bezoekers identificeert voor alle oplossingen in Experience Cloud.

  Implementatie omvat het toevoegen van de [!DNL Identity service] -code aan elke webpagina op de sites van de adverteerder.

* De organisatie moet [&#x200B; worden toegelaten voor de diensten van Experience Cloud &#x200B;](https://experienceleague.adobe.com/nl/docs/core-services/interface/services/overview) en een Experience Cloud [!DNL Organization ID] hebben (vroeger genoemd [!DNL IMS org ID]).

  Met [!UICONTROL Organization ID] kunnen organisaties met meerdere Adobe Experience Cloud-producten gegevens delen tussen bepaalde producten.

* (Advertisers met [!DNL Analytics]) de adverteerder moet [&#x200B;  [!DNL Analytics]  uitvoeren gebruikend `appMeasurement.js` &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/implementation/js/overview) versie 1.6.4 of hoger.

* De bezoekers van de website van de adverteerder hebben geen groot aantal [!DNL Apple Safari] gebruikers.

* (Aanbevolen wanneer de adverteerder zowel Audience Manager als [!DNL Analytics] gebruikt) Om aanroepen naar elke webpagina te beperken, verwijdert u de bestaande Audience Manager [!DNL Data Integration Library] -code voor gegevensverzameling en schakelt u in plaats daarvan het doorsturen aan de serverzijde voor elke [!DNL Analytics] -rapportsuite in. Voor meer informatie, zie &quot;[&#x200B; server-kant door:sturen overzicht &#x200B;](https://experienceleague.adobe.com/nl/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* (Aanbevolen) Voor hogere match-rates, verzend slechts de gegevens van de eerste-partijwebsite naar Adobe Advertising. Als de adverteerder gegevens van derden of offlinegegevens van een systeem voor het beheer van klantrelaties bundelt, kan gegevenslekken tot een lagere frequentie leiden.

## Audience Manager-soorten publiek importeren naar DSP

### Stappen voor het importeren van soorten publiek naar DSP

De [!DNL Adobe] account- en gegevensbewerkingsteams voeren de volgende stappen uit.

1. Het team van de Rekening van Adobe zou adverteerder-niveau moeten vormen die &quot; [!UICONTROL Adobe Analytics Cloud]&quot;plaatst.

1. Het Adobe-accountteam moet bij het team voor gegevensbewerkingen een verzoek indienen om de Audience Manager-segmenten van de organisatie te importeren met behulp van de Advertising DSP native API-integratie.

### Welke veranderingen zijn het resultaat in Audience Manager?

De API automatisch:

* Creeert twee bestemmingen van DSP in Audience Manager:

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* Zet de twee bestemmingen aan alle segmenten van Audience Manager in kaart, toelatend Audience Manager om de segmenten met de de adverteerderrekening van DSP te delen die met de zelfde Experience Cloud [!DNL Organization ID] verbonden is die voor Audience Manager wordt gebruikt.

  De organisatie kan naar keuze ongewenste segmenten uit de bestemmingen binnen Audience Manager verwijderen.

* Voegt de volgende uitwisselingskoekje-synchronisatiepixel aan de container van Audience Manager van de organisatie toe om het bereik van klantencampagnes te verbeteren:

   * Adobe AdCloud: 411 (Deze pixel wordt standaard en automatisch als onderdeel van [!DNL Identity Service] versie 2.0 geleverd. Organisaties met lagere [!DNL Identity Service] -versies dan 2.0 dienen deze pixel toe te voegen aan hun Audience Manager-container.

## Audience Manager-soorten publiek importeren naar [!DNL Search, Social, & Commerce]

### Stappen voor het importeren van soorten publiek naar [!DNL Search, Social, & Commerce]

[!DNL Adobe] -personeel voert de meeste of alle volgende stappen uit.

1. Het Adobe-accountteam moet bij het team voor gegevensbewerkingen een verzoek indienen om een integratie tussen [!DNL Search, Social, & Commerce] en Audience Manager in te stellen. Neem de namen op van de Audience Manager-segmenten waarnaar u wilt exporteren [!DNL Search, Social, & Commerce] .

1. Configureer in Audience Manager doelen voor [!DNL Search, Social, & Commerce]:

   1. Maak twee nieuwe doelen: `[!UICONTROL Adobe Media Optimizer (HTTP)]` en `[!UICONTROL Adobe Media Optimizer Batch Destination]` .

      [!DNL Media Optimizer] is een vroegere naam voor [!DNL Search, Social, & Commerce] .

   1. Geef de segmenten voor elk van de bestemmingen op.

      Met de optie [!UICONTROL Automatically map all current and future segments] worden alle segmenten dagelijks toegewezen en gesynchroniseerd.

      Met de optie [!UICONTROL Manually map segments] kunt u de segmenten handmatig toewijzen om te synchroniseren met de batchbestemming (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Er hoeven geen segmenten handmatig te worden toegewezen aan de HTTP-bestemming.

1. In [!DNL Search, Social, & Commerce] moet het [!DNL Search, Social, & Commerce] -implementatieteam of een gebruiker met de directe rol van de client-beheerder voor toegang het importeren starten vanuit [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup] .

   De Experience Cloud [!DNL Organization ID] ([!DNL IMS org ID]) van de organisatie is vereist. De id moet dezelfde zijn als de id die wordt gebruikt voor de Audience Manager-account van de organisatie.

### Welke veranderingen zijn het resultaat in Audience Manager?

Er zijn twee [!DNL Search, Social, & Commerce] -doelen beschikbaar voor de organisatie in Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## Gegevenssynchronisatie

De eerste importbewerking duurt ongeveer 24 uur. Na de eerste importbewerking worden de gegevens in real-time gesynchroniseerd met een vertraging van 1 tot 2 seconden.

Gegevens over een segmentlidmaatschap worden alleen verzonden nadat een van de volgende gebeurtenissen plaatsvindt:

* (Adverteerders met DSP):

   * Het segment is gericht op een Adobe Advertising-advertentie.

   * Het segment wordt toegevoegd aan de batch- en realtime-doelen van [!DNL Adobe AdCloud Cross-Channel] in de Audience Manager-gebruikersinterface.

* (Adverteerders met [!DNL Search, Social, & Commerce]):

   * Het segment wordt gebruikt in een zoekadvertentie van Adobe Advertising.

   * Het segment wordt toegevoegd aan de [!DNL Adobe Media Optimizer] batch- en HTTP-doelen in de Audience Manager-gebruikersinterface.

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### Hoe DSP de gegevens synchroniseert

DSP synchroniseert de gegevens automatisch met behulp van de [!DNL Adobe Experience Cloud Identity (ECID) Service] . Tijdens synchronisatie roept [!DNL ECID Service] Adobe Advertising aan bij [!DNL cm.everesttech.net] . Omdat Adobe Advertising een vertrouwd domein is, vindt de synchronisatie van identiteitskaart plaats van binnen de bestemmings het publiceren iframes, zoals zij met de meeste derde activeringspartners doen. Audience Manager identificeert unieke gebruikers door apparaat IDs, gebruikend [&#x200B; Audience Manager  [!DNL Unique User ID (AAM UUID)] &#x200B;](https://experienceleague.adobe.com/nl/docs/audience-manager/user-guide/reference/ids-in-aam), ook genoemd [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### Hoe zoeken, sociale media en Commerce de gegevens synchroniseren

Met Zoeken, Sociaal en Commerce worden de gegevens automatisch gesynchroniseerd met de [!DNL Adobe Experience Cloud Identity (ECID) Service] . Tijdens synchronisatie roept [!DNL ECID Service] Adobe Advertising aan bij [!DNL cm.everesttech.net] , een vertrouwd domein dat tot Adobe Advertising behoort. Audience Manager identificeert unieke gebruikers door apparaat IDs, gebruikend [&#x200B; Audience Manager  [!DNL Unique User ID (AAM UUID)] &#x200B;](https://experienceleague.adobe.com/nl/docs/audience-manager/user-guide/reference/ids-in-aam), ook genoemd [!DNL Device ID].

## Waar kunt u uw gesynchroniseerde segmenten vinden

### In DSP

DSP organiseert de segmentnamen door de taxonomie van Audience Manager en omvat het overeenkomstige aantal segmentleden in:

* [&#x200B; montages van de Plaatsing &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): Op het [!UICONTROL Adobe Segments] lusje van de [!UICONTROL Audience Targeting] sectie.

* In [&#x200B; publieksmontages &#x200B;](/help/dsp/audiences/audience-settings.md): Op het [!UICONTROL Adobe Segments] lusje.

### In Advertising Creative

In [!DNL Creative] zijn de segmenten beschikbaar in de ervaringsinstellingen voor doelknooppunten.

### In [!DNL Advertising Search, Social, & Commerce]

In [!DNL Search, Social, & Commerce] zijn de segmenten beschikbaar wanneer u een [!DNL Google] publiek maakt met [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; van [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library] .

Voor elk publiek van [!DNL Google] dat u creeert, levert [!DNL Google] de publieksgrootte.

>[!MORELIKETHIS]
>
>* [&#x200B; Integraties van Adobe Advertising met Adobe Audience Manager &#x200B;](/help/integrations/audience-manager/overview.md)
