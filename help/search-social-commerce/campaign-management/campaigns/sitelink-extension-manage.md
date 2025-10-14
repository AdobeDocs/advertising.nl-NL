---
title: Gedeelde sitelinks beheren
description: Leer hoe u gedeelde sitelink-extensies kunt maken en beheren.
exl-id: e510f53b-f48c-4129-887c-351a840b8398
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# Gedeelde sitelinks beheren

*[!DNL Google Ads]en [!DNL Microsoft Advertising] only*

U kunt gedeelde sitelinks op accountniveau maken en beheren voor elke gesynchroniseerde [!DNL Google Ads] of [!DNL Microsoft Advertising] -account in de [!UICONTROL Extensions] > [!UICONTROL Sitelinks] -bibliotheek.

## Een gedeelde sitelink maken

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** . Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]** .

1. In de toolbar boven de gegevenslijst, leidt de klik ![&#x200B; &#x200B;](/help/search-social-commerce/assets/add.png " tot ").

1. Selecteer het advertentienetwerk en de accountnaam en klik op **[!UICONTROL Continue]** .

1. Ga de [&#x200B; gedeelde sitelink montages &#x200B;](#shared-sitelink-settings) in.

1. Klik op **[!UICONTROL Post]**.

Zodra u een sitelink creeert, kunt u het [&#x200B; toewijzen aan een rekening, een campagne, of een ad groep &#x200B;](sitelink-extension-associate.md).

## Instellingen voor gedeelde sitelink bewerken

U kunt één gedeelde sitelink tegelijk bewerken.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** . Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]** .

1. Schakel het selectievakje naast de te bewerken sitelink in.

1. In de toolbar boven de gegevenslijst, geeft de klik ![&#x200B; &#x200B;](/help/search-social-commerce/assets/edit.png " uit ").

1. Bewerk de [&#x200B; gedeelde sitelink montages &#x200B;](#shared-sitelink-settings).

1. Klik op **[!UICONTROL Post]**.

## Gedeelde sitelinks verwijderen

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]** . Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]** .

1. Schakel het selectievakje in naast elke gedeelde sitelink die u wilt verwijderen.

   Voor uiteinden bij het selecteren van veelvoudige rijen, zie &quot;[&#x200B; Uitgezochte veelvoudige rijen &#x200B;](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. In de toolbar, klik ![&#x200B; Meer &#x200B;](/help/search-social-commerce/assets/more.png " ") en selecteer **[!UICONTROL Delete]**.

1. Klik in het bevestigingsbericht op **[!UICONTROL Delete]** .

## Instellingen voor gedeelde sitelink {#shared-sitelink-settings}

Voor extra beleid en redenen voor sitelink afkeuring, zie [[!DNL Google Ads] &#x200B;](https://support.google.com/adspolicy/answer/1054210) en [[!DNL Microsoft Advertising] &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/ext60206) vereisten van de sitelink uitbreiding.

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** De tekst die voor de verbinding moet verschijnen. Deze kan maximaal 25 single-byte of 12 double-byte tekens bevatten. De koppelingstekst moet uniek zijn binnen de account of campagne.

>[!NOTE]
>
>([!DNL Google Ads]) Bestaande tekst van 35 tekens wordt weergegeven in advertenties op desktops en tablets, maar niet op mobiele apparaten.

**[!UICONTROL Status]:** De weergavestatus van de sitelink: *[!UICONTROL Active]* of *[!UICONTROL Deleted]* (alleen bestaande sitelinks). De standaardwaarde voor nieuwe sitelinks is *[!UICONTROL Active]* .

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Extra tekst die de zoekmachine onder de koppelingstekst kan weergeven. Als u een beschrijving wilt opnemen, voert u waarden in voor beide beschrijvingsvelden. Elk beschrijvingsveld kan maximaal 35 single-byte of 17 double-byte tekens bevatten.

**[!UICONTROL Start Date]:** (Campagnes met bestaande verouderde sitelinks of alleen geen sitelinks; optioneel) De eerste datum waarop de sitelink met advertenties in de campagne kan worden weergegeven. De standaardwaarde voor nieuwe sitelinks is de huidige dag. Als u een toekomstige begindatum wilt opgeven, voert u een datum in de notatie MM/DD/JJJJ of M/D/JJJJ in of klikt u op   en selecteer een datum.

**[!UICONTROL End Date]:** (Facultatief) de laatste datum waarop de sitelink met advertenties in de campagne kan worden getoond. Standaard kan de sitelink oneindig worden weergegeven. Als u een einddatum wilt opgeven, voert u een datum in de notatie MM/DD/JJJJ of M/D/JJJJ in of klikt u op   en selecteer een datum.

**[!UICONTROL Mobile Preference]:** (Optioneel) Hiermee staat u het netwerk toe te proberen de advertentie-extensie weer te geven voor gebruikers van mobiele apparaten in plaats van voor gebruikers van computers of tablets. De optie is standaard niet ingeschakeld en de extensie voor de advertentie wordt op elk apparaattype weergegeven.

>[!NOTE]
>
>Het netwerk garandeert niet dat de advertentie-extensie wordt weergegeven op het voorkeurstype.

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]** De URL van de bestemmingspagina waarnaar gebruikers van zoekprogramma&#39;s worden geleid wanneer zij op uw advertentie klikken. Neem alle parameters op die de inhoud van de pagina bepalen. Als u een waarde opgeeft, wordt de basis-URL voor de advertentie hierdoor genegeerd.

Nadat u de record hebt opgeslagen, bevat de basis-URL alle toevoegingsparameters die zijn geconfigureerd voor de campagne of account.

>[!NOTE]
>
>* (Accounts met final URL&#39;s) De basis-URL kan omleidingen bevatten binnen het domein of subdomein van de bestemmingspagina, maar geen omleidingen buiten het domein van de landingspagina. Het advertentienetwerk extraheert het domein van deze URL en voegt eventuele optionele weergavepaden voor de advertentie toe om de weergave-URL voor de advertentie te maken.
>* ([!DNL Google Ads]) Elke sitelink in een campagne of advertentiegroep moet een unieke bestemmingspagina hebben, en de inhoud voor elke sitelink landende pagina moet ongeveer 80% unieke inhoud hebben. U kunt bijvoorbeeld geen sitelinks met koppelingen naar meerdere ankers op dezelfde pagina hebben.
>* ([!DNL Google Ads]) vermijd het gebruiken van macro&#39;s, die niet voor kliks van bronnen substitueren die parallel het volgen toelaten. Als de adverteerder macro&#39;s moet gebruiken, moet het Adobe-accountteam samenwerken met Customer Support of het implementatieteam om deze toe te voegen.

**[!UICONTROL Tracking Template]:** (Facultatief) het volgen malplaatje of het volgen URL, die alle off-landing domein omleidt en het volgen parameters specificeert en ook definitieve/het landen pagina URL in een parameter inbedt. Voorbeeld: `{lpurl}?source={network}&id=5` of `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` om een omleiding op te nemen.

* Voor het bijhouden van Adobe Advertising-conversies, die wordt toegepast wanneer de campagneinstellingen &quot;[!UICONTROL EF Redirect]&quot; en &quot;Automatisch uploaden&quot; bevatten, wordt bij Zoeken, Sociaal en Commerce automatisch een voorvoegsel gemaakt voor de eigen code voor het bijhouden van klikken wanneer u de record opslaat.

* Voor gesteunde parameters om definitieve URL in te bedden, zie ([!DNL Microsoft Advertising] slechts) [[!DNL Microsoft Advertising]  documentatie &#x200B;](https://help.ads.microsoft.com/#apex/3/en/56799) of ([!DNL Google Ads] slechts) de &quot;Volgend malplaatje slechts&quot;parameters in de sectie over &quot;Beschikbare [!DNL ValueTrack] Parameters&quot;in de [[!DNL Google Ads]  documentatie &#x200B;](https://support.google.com/google-ads/answer/6305348).

* U kunt optioneel URL-parameters en aangepaste parameters die voor de campagne zijn gedefinieerd, van elkaar scheiden door en-tekens (&amp;), zoals `{lpurl}?matchtype={matchtype}&device={device}` .

* U kunt desgewenst omleidingen en tekstspatiëring van derden toevoegen.

>[!NOTE]
>
>* Wanneer de campagnemontages &quot;[!UICONTROL EF Redirect]&quot;en &quot;[!UICONTROL Auto Upload] omvatten,&quot;Onderzoek, Sociale, &amp; Commerce vooraf bevestigt automatisch zijn eigen omleiding en het volgen code wanneer u sparen het verslag.
>* De volgende sjabloon op het meest granulaire niveau overschrijft de waarden op alle hogere niveaus. Als zowel de accountinstellingen als de trefwoordinstellingen bijvoorbeeld een waarde bevatten, wordt de trefwoordwaarde toegepast.
>* ([!DNL Google Ads]) als u een het volgen malplaatje bij sitelink, of sleutelwoordniveau bijwerkt, dan worden de relevante advertenties opnieuw voorgelegd voor overzicht. U kunt de trackingsjablonen op account-, campagne- of advertentieniveau bijwerken zonder uw advertenties opnieuw ter goedkeuring in te dienen.
>* ([!DNL Microsoft Advertising]) U kunt de trackingsjablonen op elk niveau bijwerken zonder uw advertenties opnieuw ter goedkeuring in te dienen.
>* Gebruik bij [!DNL Google Ads] geen macro&#39;s, die niet worden vervangen door klikken vanuit bronnen die parallelle tracering mogelijk maken. Als de adverteerder macro&#39;s moet gebruiken, moet het Adobe-accountteam samenwerken met Customer Support of het implementatieteam om deze toe te voegen.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer sitelink uitbreidingen &#x200B;](sitelink-extension-about.md)
>* [&#x200B; associeerde gedeelde sitelinks met rekeningen, campagnes, en ad groepen &#x200B;](sitelink-extension-associate.md)
