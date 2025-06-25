---
title: Een Adobe Advertising-conversietag genereren
description: Leer hoe u een Adobe Advertising-conversietag kunt maken om uw conversiegebeurtenissen bij te houden.
exl-id: 02492162-96a0-4a91-8896-dd0f72199f79
feature: Search Tools, Search Tracking
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 0%

---

# Een Adobe Advertising-conversietag genereren

*Advertisers met slechts het volgen van de omzetting van Adobe Advertising*

Maak een aparte conversietag voor elke set metriek die u wilt bijhouden en geef de tags aan de adverteerder of instantie een lijst met webpagina&#39;s waarop u deze wilt invoegen.

>[!NOTE]
>
>Met deze functie worden geen afbeeldingstags of [!DNL JavaScript] -tags toegevoegd aan de webpagina&#39;s van de adverteerder. De tags moeten worden toegevoegd volgens de normale procedure van de adverteerder voor het bijwerken van webpagina&#39;s.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]** .

1. Specificeer de [ montages van de omzettingsmarkering ](#conversion-tag-settings).

1. Genereer de tag:

   * Als de website HTTP gebruikt, klikt u op **[!UICONTROL Generate Conversion Tag]** .

   * Als de website wordt uitgevoerd op een beveiligde server (HTTPS), klikt u op **[!UICONTROL Generate Secure Conversion Tag]** .

1. Kopieer de tag uit het dialoogvenster en plak deze naar de juiste webpagina&#39;s.

>[!NOTE]
>
>Elke metrische waarde in de nieuwe omzettingsmarkering wordt automatisch vermeld in [!UICONTROL Admin] > [!UICONTROL Conversions], zelfs als het niet wordt uitgevoerd of de webpagina&#39;s het op geen kliks heeft ontvangen. Dit gedrag is anders dan het gedrag van metriek in codes die handmatig of elders zijn gemaakt. Deze worden pas weergegeven in [!UICONTROL Admin] > [!UICONTROL Conversions] nadat een klik is ontvangen op een van de webpagina&#39;s die het bevat. In alle gevallen, echter, is elke metrisch aanvankelijk uitgesloten van portefeuilledoelstellingen, rapporten, en meningen tot u hen uitdrukkelijk ter beschikking stelt. Alvorens u de metriek aan portefeuilledoelstellingen toevoegt, echter, overweeg eerst het ter beschikking stellen van de metriek en het toevoegen van hen aan rapporten om te verifiëren wanneer zij klikken ontvangen.

## Instellingen voor Adobe Advertising-conversietag {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Het type tag dat moet worden gemaakt:

* *[!UICONTROL Image]:* om een afbeeldingstag te maken voor het weergeven van een transparante afbeelding van 1 pixel x 1 pixel (pixel), die onzichtbaar is voor eindgebruikers, op de webpagina. U kunt het beste afbeeldingstags alleen gebruiken als de site een beleid heeft dat is tegen het gebruik van JavaScript-tags.

* *[!UICONTROL JavaScript]:* om een JavaScript-tag te maken.

Voor meer informatie over de verschillen tussen de markeringstypes, zie &quot;[ FAQs over de omzetting van Adobe Advertising en het volgen van de paginamening markeringen ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

**[!UICONTROL Tag Properties]:** Een of meer conversiemetriek die moet worden bijgehouden wanneer een eindgebruiker een pagina met de conversietag weergeeft. Om metrisch aan de lijst toe te voegen, ga metrische naam op het &quot;[!UICONTROL Add new property]&quot;gebied in en klik **[!UICONTROL Add]**.

Wanneer de veelvoudige metriek wordt gevolgd, worden zij aangesloten bij door een en-teken (`&`) in de markering, zoals `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Metrische gegevens die aan deze lijst zijn toegevoegd, worden nergens opgeslagen of geïntegreerd met de lijst [!UICONTROL Conversions] van de client op het tabblad [!UICONTROL Admin] . Metrische gegevens worden echter automatisch toegevoegd aan de lijst [!UICONTROL Conversions] van de client als Adobe Advertising daadwerkelijk gegevens verzamelt voor een metrische waarde. Dit gebeurt wanneer de conversietag op een pagina wordt geïmplementeerd en een eindgebruiker een transactie voltooit die de pagina opent.

**[!UICONTROL Include unique transaction IDs]:** (Facultatief) omvat een bezit van transactieidentiteitskaart (`ev_transid=<transid>`) in de markering. De optie is standaard geselecteerd.

Wanneer u deze optie selecteert, moet de adverteerder een unieke waarde genereren voor `<transid>` (bijvoorbeeld een werkelijke bestellings-id) wanneer de transactie is voltooid en deze teruggeven aan Adobe Advertising, zoals `ev_transid=0123` . Adobe Advertising gebruikt de transactie-id om dubbele transacties met dezelfde transactie-id en eigenschapswaarde te voorkomen. Transactie ID kan geen ampersand symbolen (`&`) bevatten, die als parameterseparators worden gereserveerd. De transactie-id is opgenomen in [ de [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md) . Met deze id kunt u gegevens valideren binnen Zoeken, Sociaal en Commerce met de gegevens van de adverteerder.

Als de gegevens geen unieke id per transactie bevatten, genereert Adobe Advertising nog steeds een id op basis van de transactietijd.

>[!NOTE]
>
>Als u [ de voer van identiteitskaart van de transactie ](/help/search-social-commerce/tracking/feed-transaction-id.md) met omzettingsgegevens voor off-line omzettingen verzendt, dan moet u transactie identiteitskaart (`ev_transid`) voor het online deel van de transactie in de voedergegevens voor off-line delen van de transactie voorleggen.

**[!UICONTROL Page is inside FB app]:** Verouderd

**[!UICONTROL Segment users]:** Verouderd

**[!UICONTROL JS Version]:** ([!DNL JavaScript] markeringen slechts) Welke versie van de [!DNL JavaScript] markering om te creëren: *[!UICONTROL v2]* (het gebrek) of *[!UICONTROL v3]*.

Zie &quot;[ Veelgestelde vragen over de omzetting van Adobe Advertising en de het volgen markeringen van de paginamening ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot; voor meer informatie over de verschillen .

>[!MORELIKETHIS]
>
>* [ Ongeveer conversie-volgende markeringen van Adobe Advertising ](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [ Ongeveer de hulpmiddelen om het volgen markeringen tot stand te brengen en te decoderen ](tracking-tools-about.md)
>* [ Veelgestelde vragen over omzetting en de het volgen markeringen van de paginamening ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [ Formaat van de conversie van JavaScript volgmerkversie 3 ](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [ Formaat van de conversie van JavaScript volgmerkversie 2 ](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [ Formaat van beeldomzetting volgende markeringen ](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [ de de omzettingsafbeelding van Adobe Advertising JavaScript markering ](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [ Ongeveer het leiden van de omzettingsmetriek van een adverteerder ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
