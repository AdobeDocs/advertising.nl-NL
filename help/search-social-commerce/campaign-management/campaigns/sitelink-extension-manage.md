---
title: Gedeelde sitelinks beheren
description: Leer hoe u gedeelde sitelink-extensies kunt maken en beheren.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# Gedeelde sitelinks beheren

*[!DNL Google Ads]en [!DNL Microsoft Advertising] alleen*

Gedeelde sitelinks op accountniveau maken en beheren voor elke gesynchroniseerde toepassing [!DNL Google Ads] of [!DNL Microsoft Advertising] van de [!UICONTROL Extensions] > [!UICONTROL Sitelinks] bibliotheek.

## Een gedeelde sitelink maken

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Klik op de werkbalk boven de tabel met gegevens op ![Maken](/help/search-social-commerce/assets/add.png "Maken").

1. Selecteer het advertentienetwerk en de accountnaam en klik vervolgens op **[!UICONTROL Continue]**.

1. Voer de [gedeelde site-instellingen](#shared-sitelink-settings).

1. Klik op **[!UICONTROL Post]**.

Wanneer u een sitelink maakt, kunt u [toewijzen aan een account, campagne of advertentiegroep](sitelink-extension-associate.md).

## Instellingen voor gedeelde sitelink bewerken

U kunt één gedeelde sitelink tegelijk bewerken.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Schakel het selectievakje naast de te bewerken sitelink in.

1. Klik op de werkbalk boven de tabel met gegevens op ![Bewerken](/help/search-social-commerce/assets/edit.png "Bewerken").

1. Bewerk de [gedeelde site-instellingen](#shared-sitelink-settings).

1. Klik op **[!UICONTROL Post]**.

## Gedeelde sitelinks verwijderen

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Klik in de submenu&#39;s op **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Schakel het selectievakje in naast elke gedeelde sitelink die u wilt verwijderen.

   Voor tips over het selecteren van meerdere rijen raadpleegt u &quot;[Meerdere rijen selecteren](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Klik op de werkbalk op ![Meer](/help/search-social-commerce/assets/more.png "Meer") en selecteert u **[!UICONTROL Delete]**.

1. Klik in het bevestigingsbericht op **[!UICONTROL Delete]**.

## Instellingen voor gedeelde site {#shared-sitelink-settings}

Voor extra beleid en redenen voor sitelink-afkeuring raadpleegt u de [[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210) en [[!DNL Microsoft Advertising]](https://about.ads.microsoft.com/en-us/resources/policies/ad-extensions-policies) vereisten voor de uitbreiding van sitelink.

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** De tekst die voor de koppeling moet worden weergegeven. Deze kan maximaal 25 single-byte of 12 double-byte tekens bevatten. De koppelingstekst moet uniek zijn binnen de account of campagne.

>[!NOTE]
>
>([!DNL Google Ads]) Bestaande tekst van 35 tekens wordt weergegeven in advertenties op desktops en tablets, maar niet op mobiele apparaten.

**[!UICONTROL Status]:** De weergavestatus van de sitelink:  *[!UICONTROL Active]* of *[!UICONTROL Deleted]* (alleen bestaande sitelinks). De standaardinstelling voor nieuwe sitelinks is *[!UICONTROL Active]*.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Extra tekst die het zoekprogramma onder de koppelingstekst kan weergeven. Als u een beschrijving wilt opnemen, voert u waarden in voor beide beschrijvingsvelden. Elk beschrijvingsveld kan maximaal 35 single-byte of 17 double-byte tekens bevatten.

**[!UICONTROL Start Date]:** (Campagnes met bestaande verouderde sitelinks of uitsluitend zonder sitelinks; (optioneel) De eerste datum waarop de sitelink in de campagne met advertenties kan worden weergegeven. De standaardwaarde voor nieuwe sitelinks is de huidige dag. Als u een toekomstige begindatum wilt opgeven, voert u een datum in in de notatie DD-MM-JJJJ of D-M-JJJJ of klikt u en selecteert u een datum.

**[!UICONTROL End Date]:** (Optioneel) De laatste datum waarop de sitelink in de campagne met advertenties kan worden weergegeven. Standaard kan de sitelink oneindig worden weergegeven. Als u een einddatum wilt opgeven, voert u een datum in de notatie MM/DD/JJJJ of M/D/JJJJ in of klikt u en selecteert u een datum.

**[!UICONTROL Mobile Preference]:** (Optioneel) Hiermee kan het netwerk proberen de advertentie-extensie weer te geven voor gebruikers van mobiele apparaten in plaats van voor gebruikers van desktops of tablets. De optie is standaard niet ingeschakeld en de extensie voor de advertentie wordt op elk apparaattype weergegeven.

>[!NOTE]
>
>Het netwerk garandeert niet dat de advertentie-extensie wordt weergegeven op het voorkeurstype.

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]** De bestemmingspagina-URL waarnaar de gebruikers van de onderzoeksmotor worden genomen wanneer zij uw advertentie klikken. Neem alle parameters op die de inhoud van de pagina bepalen. Als u een waarde opgeeft, wordt de basis-URL voor de advertentie hierdoor genegeerd.

Nadat u de record hebt opgeslagen, bevat de basis-URL alle toevoegingsparameters die zijn geconfigureerd voor de campagne of account.

>[!NOTE]
>
>* (Accounts met final URL&#39;s) De basis-URL kan omleidingen bevatten binnen het domein of subdomein van de bestemmingspagina, maar geen omleidingen buiten het domein van de landingspagina. Het advertentienetwerk extraheert het domein van deze URL en voegt eventuele optionele weergavepaden voor de advertentie toe om de weergave-URL voor de advertentie te maken.
>* ([!DNL Google Ads]) Elke sitelink in een campagne of advertentiegroep moet een unieke bestemmingspagina hebben, en de inhoud voor elke sitelink-landingspagina moet ongeveer 80% unieke inhoud hebben. U kunt bijvoorbeeld geen sitelinks met koppelingen naar meerdere ankers op dezelfde pagina hebben.
>* ([!DNL Google Ads]) Vermijd het gebruik van macro&#39;s, die niet worden vervangen door klikken van bronnen die parallelle tracering mogelijk maken. Als de adverteerder macro&#39;s moet gebruiken, moet het accountteam van Adobe samenwerken met de klantenondersteuning of het implementatieteam om deze toe te voegen.


**[!UICONTROL Tracking Template]:** (Optioneel) De URL voor reeksspatiëring of reeksspatiëring, die alle omleidingen en volgparameters van het niet-landende domein opgeeft en ook de URL van de laatste/landingspagina in een parameter insluit. Voorbeeld: `{lpurl}?source={network}&id=5` of `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` om een omleiding op te nemen.

* Voor het bijhouden van reclame-omzettingen in Adobe, die wordt toegepast wanneer de instellingen voor de campagne &#39;EF-omleiding&#39; en &#39;Automatisch uploaden&#39;, &#39;Zoeken, Sociaal en Handel&#39; bevatten, wordt automatisch de eigen code voor het bijhouden van klikken vooraf vastgelegd wanneer u de record opslaat.

* Zie voor ondersteunde parameters om de laatste URL in te sluiten ([!DNL Microsoft Advertising] alleen) [[!DNL Microsoft Advertising] documentatie](https://help.ads.microsoft.com/#apex/3/en/56799) of ([!DNL Google Ads] alleen) de &quot;Volgsjabloon alleen&quot;-parameters in het gedeelte over &quot;Beschikbare ValueTrack-parameters&quot; in het gedeelte [[!DNL Google Ads] documentatie](https://support.google.com/google-ads/answer/6305348).

* U kunt optioneel URL-parameters en aangepaste parameters die zijn gedefinieerd voor de campagne opnemen, gescheiden door en-tekens (&amp;), zoals `{lpurl}?matchtype={matchtype}&device={device}`.

* U kunt desgewenst omleidingen en tekstspatiëring van derden toevoegen.

>[!NOTE]
>
>* Wanneer de campagne-instellingen &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload],&quot; Onderzoek, Sociale, &amp; Handel vooraf fixeert automatisch zijn eigen omleiding en het volgen code wanneer u sparen het verslag.
>* De het volgen malplaatje op het meest korrelige niveau treedt de waarden op alle hogere niveaus met voeten. Als zowel de accountinstellingen als de trefwoordinstellingen bijvoorbeeld een waarde bevatten, wordt de trefwoordwaarde toegepast.
>* ([!DNL Google Ads]) Als u een trackingsjabloon op sitelink- of trefwoordniveau bijwerkt, worden de relevante advertenties opnieuw verzonden voor revisie. U kunt de trackingsjablonen op account-, campagne- of advertentieniveau bijwerken zonder uw advertenties opnieuw ter goedkeuring in te dienen.
>* ([!DNL Microsoft Advertising]) Je kunt je trackingsjablonen op elk niveau bijwerken zonder je advertenties opnieuw ter goedkeuring in te dienen.
>* Voor [!DNL Google Ads], vermijd het gebruiken van macro&#39;s, die niet voor kliks van bronnen substitueren die parallel volgen toelaten. Als de adverteerder macro&#39;s moet gebruiken, moet het Adobe Account Team met de Klantenondersteuning of het implementatieteam samenwerken om deze toe te voegen.


>[!MORELIKETHIS]
>
>* [Extensies voor sitelink](sitelink-extension-about.md)
>* [Gedeelde sitelinks koppelen aan accounts, campagnes en ad-groepen](sitelink-extension-associate.md)

