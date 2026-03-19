---
title: Een Adobe Advertising-tag voor conversie bijhouden genereren en implementeren
description: Leer hoe u een Adobe Advertising-conversietag kunt maken om uw conversiegebeurtenissen bij te houden.
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: 674c2a40ccb64b6dfcbda2c4030a8b985ce58a45
workflow-type: tm+mt
source-wordcount: '1011'
ht-degree: 0%

---

# Een Adobe Advertising-tag voor conversie bijhouden genereren en implementeren

*Advertisers met slechts het volgen van de omzetting van Adobe Advertising*

Maak een aparte conversietag voor elke set metingen die u wilt bijhouden. U kunt tags genereren in Zoeken, Sociaal en Commerce of door tags te gebruiken in Adobe Experience Platform (voorheen bekend als Adobe Experience Platform Launch) met de Adobe Advertising-extensie.

## Een tag voor het bijhouden van conversies genereren en implementeren in Zoeken, Sociaal en Commerce

>[!NOTE]
>
>Met deze functie worden geen afbeeldingstags of [!DNL JavaScript] -tags toegevoegd aan de webpagina&#39;s van de adverteerder. Geef de tags aan de adverteerder of het bureau een lijst met webpagina&#39;s waarop u ze wilt invoegen. De tags moeten worden toegevoegd volgens de normale procedure van de adverteerder voor het bijwerken van webpagina&#39;s.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]** .

1. Specificeer de [&#x200B; montages van de omzettingsmarkering &#x200B;](#conversion-tag-settings).

1. Genereer de tag:

   * Als de website HTTP gebruikt, klikt u op **[!UICONTROL Generate Conversion Tag]** .

   * Als de website wordt uitgevoerd op een beveiligde server (HTTPS), klikt u op **[!UICONTROL Generate Secure Conversion Tag]** .

1. Kopieer de tag uit het dialoogvenster en plak deze naar de juiste webpagina&#39;s.

>[!NOTE]
>
>Elke metrische waarde in de nieuwe omzettingsmarkering wordt automatisch vermeld in [!UICONTROL Admin] > [!UICONTROL Conversions], zelfs als het niet wordt uitgevoerd of de webpagina&#39;s het op geen kliks heeft ontvangen. Dit gedrag is anders dan het gedrag van metriek in codes die handmatig of elders zijn gemaakt. Deze worden pas weergegeven in [!UICONTROL Admin] > [!UICONTROL Conversions] nadat een klik is ontvangen op een van de webpagina&#39;s die het bevat. In alle gevallen, echter, is elke metrisch aanvankelijk uitgesloten van portefeuilledoelstellingen, rapporten, en meningen tot u hen uitdrukkelijk ter beschikking stelt. Alvorens u de metriek aan portefeuilledoelstellingen toevoegt, echter, overweeg eerst het ter beschikking stellen van de metriek en het toevoegen van hen aan rapporten om te verifiëren wanneer zij klikken ontvangen.

### Instellingen voor Adobe Advertising-conversietag {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Het type tag dat moet worden gemaakt:

* *[!UICONTROL Image]:* om een afbeeldingstag te maken voor het weergeven van een transparante afbeelding van 1 pixel x 1 pixel (pixel), die onzichtbaar is voor eindgebruikers, op de webpagina. U kunt het beste afbeeldingstags alleen gebruiken als de site een beleid heeft dat is tegen het gebruik van JavaScript-tags.

* *[!UICONTROL JavaScript]:* om een JavaScript-tag te maken.

Voor meer informatie over de verschillen tussen de markeringstypes, zie &quot;[&#x200B; FAQs over de omzetting van Adobe Advertising en het volgen van de paginamening markeringen &#x200B;](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

**[!UICONTROL Tag Properties]:** Een of meer conversiemetriek die moet worden bijgehouden wanneer een eindgebruiker een pagina met de conversietag weergeeft. Om metrisch aan de lijst toe te voegen, ga metrische naam op het &quot;[!UICONTROL Add new property]&quot;gebied in en klik **[!UICONTROL Add]**.

Wanneer de veelvoudige metriek wordt gevolgd, worden zij aangesloten bij door een en-teken (`&`) in de markering, zoals `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Metrische gegevens die aan deze lijst zijn toegevoegd, worden nergens opgeslagen of geïntegreerd met de lijst [!UICONTROL Conversions] van de client op het tabblad [!UICONTROL Admin] . Metrische gegevens worden echter automatisch toegevoegd aan de lijst [!UICONTROL Conversions] van de client als Adobe Advertising daadwerkelijk gegevens verzamelt voor een metrische waarde. Dit gebeurt wanneer de conversietag op een pagina wordt geïmplementeerd en een eindgebruiker een transactie voltooit die de pagina opent.

**[!UICONTROL Include unique transaction IDs]:** (Facultatief) omvat een bezit van transactieidentiteitskaart (`ev_transid=<transid>`) in de markering. De optie is standaard geselecteerd.

Wanneer u deze optie selecteert, moet de adverteerder een unieke waarde genereren voor `<transid>` (bijvoorbeeld een werkelijke bestellings-id) wanneer de transactie is voltooid en deze teruggeven aan Adobe Advertising, zoals `ev_transid=0123` . Adobe Advertising gebruikt de transactie-id om dubbele transacties met dezelfde transactie-id en eigenschapswaarde te voorkomen. Transactie ID kan geen ampersand symbolen (`&`) bevatten, die als parameterseparators worden gereserveerd. De transactie-id is opgenomen in [&#x200B; de [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md) . Met deze id kunt u gegevens valideren binnen Zoeken, Sociaal en Commerce met de gegevens van de adverteerder.

Als de gegevens geen unieke id per transactie bevatten, genereert Adobe Advertising nog steeds een id op basis van de transactietijd.

>[!NOTE]
>
>Als u [&#x200B; de voer van identiteitskaart van de transactie &#x200B;](/help/search-social-commerce/tracking/feed-transaction-id.md) met omzettingsgegevens voor off-line omzettingen verzendt, dan moet u transactie identiteitskaart (`ev_transid`) voor het online deel van de transactie in de voedergegevens voor off-line delen van de transactie voorleggen.

**[!UICONTROL Page is inside FB app]:** Verouderd

**[!UICONTROL Segment users]:** Verouderd

**[!UICONTROL JS Version]:** ([!DNL JavaScript] markeringen slechts) Welke versie van de [!DNL JavaScript] markering om te creëren: *[!UICONTROL v2]* (het gebrek) of *[!UICONTROL v3]*.

Zie &quot;[&#x200B; Veelgestelde vragen over de omzetting van Adobe Advertising en de het volgen markeringen van de paginamening &#x200B;](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot; voor meer informatie over de verschillen .

## Tags voor conversie bijhouden implementeren met Adobe Experience Platform-tags en de Adobe Advertising-extensie

U kunt conversietracering instellen voor Zoeken, Sociaal en Commerce met tags in Adobe Experience Platform. De markeringen zijn beschikbaar aan klanten van Adobe Experience Cloud als inbegrepen, waarde-toevoegt eigenschap.

De volgende taken zijn vereist om conversietrackingtags voor Zoeken, Sociaal en Commerce te configureren vanuit de Experience Platform-gebruikersinterface of vanuit de Experience Platform Data Collection-gebruikersinterface. Voor volledige informatie en instructies voor het vormen van markeringen, zie de Gids van de Markeringen van Experience Platform, die met het &quot;[&#x200B; overzicht van Markeringen &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/tags/home)&quot;begint en &quot;[&#x200B; gids van QuickStart &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/tags/get-started/quick-start).&quot;

>[!PREREQUISITES]
>
>Als u de vereiste tagextensie wilt installeren, vraagt u de systeembeheerder van uw organisatie om toegang tot de functies voor gegevensverzameling in de gebruikersinterface, inclusief de machtiging `manage_properties` .

1. Van [&#x200B; de Inzameling UI van Gegevens &#x200B;](https://experience.adobe.com/#/data-collection/), installeer de Uitbreiding van Adobe Advertising [&#x200B; &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/tags/ui/extensions/overview):

   1. Van het toepasselijke bezit, open de uitbreidingscatalogus en selecteer **Adobe Advertising**.

   1. Van het keuzemenu, uitgezochte **SSC** (voor Onderzoek, Sociale, &amp; Commerce).

   1. Op het **gebied van 0&rbrace; SSC UserID, ga numerieke gebruiker in - identiteitskaart voor het Onderzoek van uw organisatie, Sociale, &amp; rekening van Commerce.**

      Neem contact op met uw Adobe-accountteam als u uw gebruikersnaam niet kent.

   1. Klik **sparen**.

1. Maak een nieuwe regel (bijvoorbeeld &quot;form_completes&quot;) om de conversietag Zoeken, Sociaal en Commerce te activeren:

   1. In de sectie Gebeurtenisconfiguratie:

      1. Selecteer de volgende waarden:

         **Uitbreiding:** `Core`

         **Type van Gebeurtenis:** `Library Loaded (Page Top)`

      1. Klik **houden Veranderingen**.

   1. In de sectie Configuratie voorwaarde:

      1. Geef de volgende waarden op:

         **Logische Type:** `Regular`

         **Uitbreiding:** `Core`

         **Type van Voorwaarde:** `Path Without Query String`

         **terugkeer waar als de weg evenaart:** de weg waar de omzetting (bijvoorbeeld, `/form_complete`) zou moeten worden gevolgd.

      1. Klik **houden Veranderingen**.

   1. In de sectie Configuratie van de Actie:

      1. Geef de volgende waarden op:

         **Uitbreiding:** `Adobe Advertising`

         **Type van Actie:** `AMO Measurement`

         **Naam van het Bezit van de Omzetting:** De naam van het omzettingsbezit (bijvoorbeeld, `form_completes`).

         **Waarde:** de numerieke waarde van het omzettingsbezit (bijvoorbeeld `1` aan track form_completes), of kies een bestaand [&#x200B; gegevenselement &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/tags/ui/data-elements).

      1. Klik **houden Veranderingen**.

   1. Sla de regel op.

1. Publiceer de wijzigingen.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer conversie-volgende markeringen van Adobe Advertising &#x200B;](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [&#x200B; Ongeveer de hulpmiddelen om het volgen markeringen tot stand te brengen en te decoderen &#x200B;](tracking-tools-about.md)
>* [&#x200B; Veelgestelde vragen over omzetting en de het volgen markeringen van de paginamening &#x200B;](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [&#x200B; Formaat van de conversie van JavaScript volgmerkversie 3 &#x200B;](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [&#x200B; Formaat van de conversie van JavaScript volgmerkversie 2 &#x200B;](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [&#x200B; Formaat van beeldomzetting volgende markeringen &#x200B;](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [&#x200B; de de omzettingsafbeelding van Adobe Advertising JavaScript markering &#x200B;](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [&#x200B; Ongeveer het leiden van de omzettingsmetriek van een adverteerder &#x200B;](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
