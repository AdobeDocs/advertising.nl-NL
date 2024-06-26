---
title: Adobe Audience Manager-segmenten importeren voor advertentiedoeleinden
description: Leer hoe u uw [!DNL Adobe] publiek naar Advertising DSP en Search met Adobe Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 6ff80699-9554-4b39-a019-d8055d68c174
source-git-commit: e6635abdb34444bc40d833a3c6a5eaf07f9f1789
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# Adobe Audience Manager-segmenten importeren voor advertentiedoeleinden

Advertising DSP en [!DNL Advertising Search, Social, & Commerce] kan elke gebruiker metagegevens, hiërarchiegegevens en unieke publieksgegevens voor alle adverteerders of agentschappen ophalen [!DNL Adobe] publiek<!-- segments or audiences? Standardize terms per AAM's docs -->, inclusief:

* Adobe Audience Manager-segmenten

* Adobe Analytics-segmenten die naar Adobe Experience Cloud worden gepubliceerd

* Segmenten die zijn gemaakt met de Adobe Experience Cloud [!DNL Audience Library]

* Segmenten die in Adobe Experience Platform zijn gemaakt en via Audience Manager naar de Adobe Advertising worden verzonden

Toegang tot [!DNL Adobe] publiek in DSP of [!DNL Creative], moet u het publiek in DSP importeren. Toegang tot [!DNL Adobe] publiek in [!DNL Search, Social, & Commerce], moet u het publiek importeren in [!DNL Search, Social, & Commerce].

## Vereisten

* De adverteerder moet [de [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/en/docs/id-service/using/intro/overview) versie 2.0 of hoger. De [!DNL Identity Service] biedt een universele, permanente id die uw bezoekers identificeert voor alle oplossingen in het Experience Cloud.

  Implementatie omvat het toevoegen van de [!DNL Identity service] code naar elke webpagina op de sites van de adverteerder.

* De organisatie moet [Toegelaten voor de diensten van het Experience Cloud](https://experienceleague.adobe.com/en/docs/core-services/interface/services/overview) en een Experience Cloud hebben [!DNL Organization ID] (voorheen [!DNL IMS org ID]).

  De [!UICONTROL Organization ID] kunnen organisaties met meerdere Adobe Experience Cloud-producten gegevens uitwisselen tussen bepaalde producten.

* (Adverteerders met [!DNL Analytics]) De adverteerder moet [uitvoeren [!DNL Analytics] gebruiken `appMeasurement.js`](https://experienceleague.adobe.com/en/docs/analytics/implementation/js/overview) versie 1.6.4 of hoger.

* De bezoekers van de website van de adverteerder hebben geen groot aantal [!DNL Apple Safari] gebruikers.

* (Aanbevolen wanneer de adverteerder zowel Audience Manager als [!DNL Analytics]) Als u aanroepen naar elke webpagina wilt beperken, verwijdert u de bestaande Audience Manager [!DNL Data Integration Library] code voor gegevensinzameling en laat server-zijhet door:sturen voor elk toe [!DNL Analytics] rapportsuite. Zie voor meer informatie &quot;[Server-kant door:sturen overzicht](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/server-side-forwarding/ssf).

* (Aanbevolen) Als de zoekresultaten hoger zijn, stuurt u alleen de gegevens van de website van de eerste partij naar de Adobe Advertising. Als de adverteerder gegevens van derden of offlinegegevens van een systeem voor het beheer van klantrelaties bundelt, kan gegevenslekken tot een lagere frequentie leiden.

## Soorten publiek in Audience Manager importeren naar DSP

### Stappen voor het importeren van soorten publiek naar DSP

De [!DNL Adobe] account- en gegevensbewerkingsteams voeren de volgende stappen uit.

1. Het accountteam van de Adobe moet de instelling op adverteerderniveau &quot;[!UICONTROL Adobe Analytics Cloud].&quot;

1. Het team van de Rekening van de Adobe zou een verzoek aan het team van gegevensverrichtingen moeten voorleggen om de segmenten van de Audience Manager van de organisatie in te voeren gebruikend de AdvertisingDSP inheemse API integratie.

### Welke veranderingen resulteren in Audience Manager?

De API automatisch:

* Maakt twee DSP doelen in Audience Manager:

   * **[!UICONTROL Adobe AdCloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)]**

* Zet de twee bestemmingen aan alle segmenten van de Audience Manager in kaart, toestaand Audience Manager om de segmenten met de DSP adverteerderrekening te delen die met het zelfde Experience Cloud wordt geassocieerd [!DNL Organization ID] gebruikt voor Audience Manager.

  De organisatie kan naar keuze ongewenste segmenten uit de bestemmingen binnen Audience Manager verwijderen.

* Voegt de volgende uitwisselingskoekje-synchronisatiepixel aan de container van de Audience Manager van de organisatie toe om het bereik van klantencampagnes te verbeteren:

   * Adobe AdCloud: 411 (deze pixel wordt standaard en automatisch als onderdeel van [!DNL Identity Service] versie 2.0. Organisaties met [!DNL Identity Service] In versies onder 2.0 moet u deze pixel toevoegen aan de container van de Audience Manager.

## Soorten publiek in Audience Manager importeren naar [!DNL Search, Social, & Commerce]

### Stappen voor het importeren van soorten publiek naar [!DNL Search, Social, & Commerce]

[!DNL Adobe] voert de meeste of alle volgende stappen uit.

1. Het team van de Rekening van de Adobe zou een verzoek aan het team van gegevensverrichtingen moeten voorleggen om opstelling een integratie tussen [!DNL Search, Social, & Commerce] en Audience Manager. Neem de namen op van de Audience Manager-segmenten waarnaar u wilt exporteren [!DNL Search, Social, & Commerce].

1. Binnen Audience Manager, vorm bestemmingen voor [!DNL Search, Social, & Commerce]:

   1. Maak twee nieuwe doelen: `[!UICONTROL Adobe Media Optimizer (HTTP)]` en `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] is een vroegere naam voor [!DNL Search, Social, & Commerce].

   1. Geef de segmenten voor elk van de bestemmingen op.

      Met de [!UICONTROL Automatically map all current and future segments] alle segmenten worden dagelijks toegewezen en gesynchroniseerd.

      De [!UICONTROL Manually map segments] kunt u de segmenten handmatig toewijzen aan synchronisatie met de batchbestemming (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Er hoeven geen segmenten handmatig te worden toegewezen aan de HTTP-bestemming.

1. Within [!DNL Search, Social, & Commerce], ofwel [!DNL Search, Social, & Commerce] het implementatieteam of een gebruiker met de directe rol van de manager van de toegangscliënt zou de invoer van moeten in werking stellen [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Het Experience Cloud van de organisatie [!DNL Organization ID] ([!DNL IMS org ID]) is vereist. De id moet dezelfde zijn als de id die wordt gebruikt voor de account van de Audience Manager van de organisatie.

### Welke veranderingen resulteren in Audience Manager?

Twee [!DNL Search, Social, & Commerce] de Audience Manager beschikt over de volgende bestemmingen :

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination]**

## Gegevenssynchronisatie

De eerste importbewerking duurt ongeveer 24 uur. Na de eerste importbewerking worden de gegevens in real-time gesynchroniseerd met een vertraging van 1 tot 2 seconden.

Gegevens over een segmentlidmaatschap worden alleen verzonden nadat een van de volgende gebeurtenissen plaatsvindt:

* (Adverteerders met DSP):

   * Het segment wordt gericht in een de vertoningsadvertentie van de Adobe Advertising.

   * Het segment wordt toegevoegd aan de [!DNL Adobe AdCloud Cross-Channel] partij en in real time bestemmingen binnen het gebruikersinterface van de Audience Manager.

* (Adverteerders met [!DNL Search, Social, & Commerce]):

   * Het segment wordt gericht in een Adobe Advertising onderzoek advertentie.

   * Het segment wordt toegevoegd aan de [!DNL Adobe Media Optimizer] batch- en HTTP-doelen binnen de gebruikersinterface van de Audience Manager.

<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

### Hoe DSP de gegevens synchroniseert

DSP de gegevens automatisch synchroniseert met de [!DNL Adobe Experience Cloud Identity (ECID) Service]. Tijdens synchronisatie [!DNL ECID Service] roept Adobe Advertising bij [!DNL cm.everesttech.net]. Omdat Adobe Advertising een vertrouwd domein is, vinden id-synchronisaties plaats vanaf bovenliggende pagina&#39;s in plaats van binnen de doelpublicatieiframes, zoals bij de meeste activeringspartners van derden. Audience Manager identificeert unieke gebruikers op apparaat-id&#39;s met behulp van de [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), ook wel de [!DNL Device ID].

<!--
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)
-->

### Hoe zoeken, sociale media en Commerce de gegevens synchroniseren

Met Zoeken, Sociaal en Commerce worden de gegevens automatisch gesynchroniseerd met de [!DNL Adobe Experience Cloud Identity (ECID) Service]. Tijdens synchronisatie [!DNL ECID Service] roept Adobe Advertising bij [!DNL cm.everesttech.net], een vertrouwd domein dat bij Adobe Advertising hoort. Audience Manager identificeert unieke gebruikers op apparaat-id&#39;s met behulp van de [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/reference/ids-in-aam), ook wel de [!DNL Device ID].

## Waar kunt u uw gesynchroniseerde segmenten vinden

### In DSP

DSP organiseert de segmentnamen door de taxonomie van de Audience Manager en omvat de overeenkomstige tellingen van het segmentlidmaatschap in:

* [Plaatsingsinstellingen](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): Over de [!UICONTROL Adobe Segments] tabblad van het [!UICONTROL Audience Targeting] sectie.

* In [doelinstellingen](/help/dsp/audiences/audience-settings.md): Over de [!UICONTROL Adobe Segments] tab.

### In Advertising Creative

In [!DNL Creative], zijn de segmenten beschikbaar in de ervaringsmontages voor doelknopen.

### In [!DNL Advertising Search, Social, & Commerce]

In [!DNL Search, Social, & Commerce], zijn de segmenten beschikbaar wanneer u een [!DNL Google] publiek dat de [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; van [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Voor elke [!DNL Google] publiek dat u maakt, [!DNL Google] levert de omvang van het publiek.

>[!MORELIKETHIS]
>
>* [Integratie van Adobe Advertising met Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
