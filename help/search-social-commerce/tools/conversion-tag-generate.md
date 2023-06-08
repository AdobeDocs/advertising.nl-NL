---
title: Een conversietag voor Adobe-reclame genereren
description: Leer hoe u een conversietag voor reclame-Adobe maakt om uw conversiegebeurtenissen bij te houden.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---

# Een conversietag voor Adobe-reclame genereren

*Adverteerders met alleen het bijhouden van Adobe-advertenties*

Maak een aparte conversietag voor elke set metriek die u wilt bijhouden en geef de tags aan de adverteerder of instantie een lijst met webpagina&#39;s waarop u deze wilt invoegen.

>[!NOTE]
>
>Deze functie voegt geen afbeeldingstags of [!DNL JavaScript] -tags aan de webpagina&#39;s van de adverteerder. De tags moeten worden toegevoegd volgens de normale procedure van de adverteerder voor het bijwerken van webpagina&#39;s.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Tags]**.

1. Geef de [instellingen voor conversietags](#conversion-tag-settings).

1. Genereer de tag:

   * Als de website HTTP gebruikt, klikt u op **[!UICONTROL Generate Conversion Tag]**.

   * Als de website wordt uitgevoerd op een beveiligde server (HTTPS), klikt u op **[!UICONTROL Generate Secure Conversion Tag]**.

1. Kopieer de tag uit het dialoogvenster en plak deze naar de juiste webpagina&#39;s.

>[!NOTE]
>
>Elke metrische waarde in de nieuwe omzettingscode wordt automatisch vermeld in [!UICONTROL Admin] > [!UICONTROL Transaction Properties], zelfs als het niet wordt uitgevoerd of de webpagina&#39;s het op heeft geen kliks ontvangen. Dit gedrag verschilt van het gedrag van metriek in manueel of elders gemaakte markeringen, die niet in worden vermeld [!UICONTROL Admin] > [!UICONTROL Transaction Properties] totdat een van de webpagina&#39;s waarop het staat een klik heeft ontvangen. In alle gevallen, echter, is elke metrisch aanvankelijk uitgesloten van portefeuilledoelstellingen, rapporten, en meningen tot u hen uitdrukkelijk ter beschikking stelt. Alvorens u de metriek aan portefeuilledoelstellingen toevoegt, echter, overweeg eerst het ter beschikking stellen van de metriek en het toevoegen van hen aan rapporten om te verifiëren wanneer zij klikken ontvangen.

## Instellingen voor conversietags voor Adobe voor advertenties {#conversion-tag-settings}

**[!UICONTROL Tag Type]:** Het type label dat moet worden gemaakt:

* *[!UICONTROL Image]:* Een afbeeldingstag maken om een transparante afbeelding (pixel) van 1 pixel x 1 pixel, die onzichtbaar is voor eindgebruikers, weer te geven op de webpagina. De beste manier is om alleen afbeeldingstags te gebruiken als de site een beleid heeft tegen het gebruik van JavaScript-tags.

* *[!UICONTROL JavaScript]:* Een JavaScript-tag maken.

Zie &quot;[Veelgestelde vragen over conversie van Adobe-advertenties en labels voor het bijhouden van paginaweergaven](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

**[!UICONTROL Tag Properties]:** Een of meer transactieeigenschappen (metriek) die moeten worden bijgehouden wanneer een eindgebruiker een pagina met de conversietag weergeeft. Als u metrische gegevens aan de lijst wilt toevoegen, voert u de naam van de metrische waarde in het veld &quot;[!UICONTROL Add new property]&quot; veld en klik op **[!UICONTROL Add]**.

Wanneer de veelvoudige metriek wordt gevolgd, worden zij aangesloten bij door ampersand (`&`) in de tag, zoals `ev_Property1=<Property1>&ev_Property2=<Property2>`.

>[!NOTE]
>
>Metrische gegevens die aan deze lijst zijn toegevoegd, worden nergens opgeslagen of geïntegreerd met de client [!UICONTROL Transaction Properties] op de lijst [!UICONTROL Admin] tab. Metrische gegevens worden echter toegevoegd aan de [!UICONTROL Transaction Properties] Deze lijst wordt automatisch weergegeven wanneer Adobe Advertising gegevens verzamelt voor een metrische waarde. Dit gebeurt wanneer de conversietag op een pagina wordt geïmplementeerd en een eindgebruiker een transactie voltooit die die pagina opent.

**[!UICONTROL Include unique transaction IDs]:** (Optioneel) Bevat een transactie-id-eigenschap (`ev_transid=<transid>`) in de tag. De optie is standaard geselecteerd.

Wanneer u deze optie selecteert, moet de adverteerder een unieke waarde genereren voor `<transid>` (bijvoorbeeld een werkelijke bestellings-id) wanneer de transactie is voltooid en deze teruggeeft aan Adobe Advertising, zoals `ev_transid=0123`. In advertentie van Adobe wordt de transactie-id gebruikt om dubbele transacties met dezelfde transactie-id en eigenschapswaarde te voorkomen. De transactie-id mag geen ampersand-symbolen bevatten (`&`), die zijn gereserveerd als parameterscheidingstekens. De transactie-id is opgenomen in [de [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), die u kunt gebruiken om gegevens te valideren binnen Zoeken, Sociale Zaken en Handel met de gegevens van de adverteerder.

Als de gegevens geen unieke id per transactie bevatten, genereert Adobe-advertentie nog steeds een id op basis van de transactietijd.

>[!NOTE]
>
>Als u [feeds van transactie-id](/help/search-social-commerce/tracking/feed-transaction-id.md) met conversiegegevens voor offline conversies moet u de transactie-id (`ev_transid`) voor het online gedeelte van de transactie in de feed-gegevens voor offline delen van de transactie.

**[!UICONTROL Page is inside FB app]:** Achterhaald

**[!UICONTROL Segment users]:** Achterhaald

**[!UICONTROL JS Version]:** ([!DNL JavaScript] (alleen tags) Welke versie van de [!DNL JavaScript] te maken tag: *[!UICONTROL v2]* (de standaardwaarde) of *[!UICONTROL v3]*.

Zie &quot;[Veelgestelde vragen over conversie van Adobe-advertenties en labels voor het bijhouden van paginaweergaven](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot; voor meer informatie over de verschillen .

>[!MORELIKETHIS]
>
>* [Informatie over conversietags voor Adobe-advertenties](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Over de gereedschappen voor het maken en decoderen van trackingcodes](tracking-tools-about.md)
>* [Veelgestelde vragen over tags voor conversie en bijhouden van paginaweergaven](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [Indeling van JavaScript-tags voor conversie bijhouden versie 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)
>* [Indeling van JavaScript-tags voor bijhouden van conversie versie 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)
>* [Opmaak van trackingtags voor afbeeldingsconversie](/help/search-social-commerce/tracking/format-conversion-tag-image.md)
>* [De conversietoewijzingstag voor JavaScript-Adobe-reclame](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
>* [Informatie over het beheren van de transactieeigenschappen van een adverteerder](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md)

