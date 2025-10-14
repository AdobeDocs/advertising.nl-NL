---
title: Veelgestelde vragen over campagnes
description: Zie antwoorden op vragen over campagnebeheer en de mening van campagnegegevens.
exl-id: 999e5aba-f556-4b34-bb92-5931d5e0dd72
feature: Search Campaign Management
source-git-commit: 88b415fff52d623a5daeb00355bfe00054d5402b
workflow-type: tm+mt
source-wordcount: '1585'
ht-degree: 0%

---

# Veelgestelde vragen over campagnebeheer

## Algemene informatie

+++Kan ik campagnes en componenten van één rekening naar een andere verplaatsen?

Verplaats of kopieer geen campagne of campagnecomponent, die een unieke identiteitskaart heeft, naar een rekening met een verschillende rekening ID. Dit resulteert in gegevensfouten.
+++

+++Wanneer worden de klikgegevens bijgewerkt van de advertentienetwerken?

Het proces om de klikgegevens van de vorige dag van de onderzoeksmotoren te trekken begint bij 06 :00 in de de tijdzone van de adverteerder.

Bovendien [!DNL Google Ads] campagne-vlakke prestatiesmetriek op het onderzoeksnetwerk voor de huidige dag worden getrokken bij 08 :00 en 16 :00 in de de tijdzone van de adverteerder.
+++

+++Welke acties leiden ertoe dat trefwoorden en advertenties hun geschiedenis verliezen?

>[!NOTE]
>
>(Adverteerders met portfolio&#39;s) De prestaties van nieuwe trefwoorden en combinaties van overeenkomende typen zijn volatiel, terwijl Zoeken, Sociaal en Commerce gegevens verzamelen om modellen voor deze combinaties te maken.

**Acties in de [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] meningen, in het bulksheet het posten proces, en in de eigen redacteur van het advertentienetwerk:**

Het bestaande trefwoord of de bestaande advertentie wordt verwijderd en er wordt een andere advertentie gemaakt wanneer:

* ([!DNL Baidu] , [!DNL Google Ads] en [!DNL Yandex]) U bewerkt een trefwoordnaam.

* ([!DNL Google Ads] , [!DNL Microsoft Advertising] en [!DNL Yandex]) U wijzigt het overeenkomende type van een trefwoord.

* U verplaatst een trefwoord tussen advertentiegroepen.

* ([!DNL Google Ads] dynamische zoekadvertenties, [!DNL Microsoft Advertising] uitgebreide tekstadvertenties en alle advertentietypen op andere ondersteunde advertentienetwerken) U bewerkt en kopieert (titel/titel of beschrijving) of een advertentieafbeelding.

* U verplaatst een advertentie tussen advertentiegroepen.

**Gebeurtenissen in het voer van de productinventaris het posten proces:**

Een bestaande advertentie of een bestaand trefwoord wordt verwijderd en er wordt een andere advertentie of trefwoord gemaakt wanneer:

* Een feed-bestand bevat een nieuwe waarde voor een kolom die wordt gebruikt in een advertentievariatie.

* De malplaatjemontages voor een advertentie veranderden sinds de laatste propagatie.

* Een nieuw feed-bestand bevat een rij voor een advertentie of trefwoord dat a) zich in een vorig bestand bevond, maar b) is sindsdien weggelaten en is gepauzeerd of verwijderd volgens de instellingen van de voedergegevens.

Afhankelijk van de [&#x200B; montages van voedergegevens &#x200B;](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings), kan een bestaande advertentie of een sleutelwoord worden geschrapt wanneer:

* Een nieuw feed-bestand bevat geen rij voor een bestaande advertentie of een bestaand trefwoord.

* De geplande einddatum voor de componenten van een gepost voederdossier komt voor.

* Het voorraadniveau van een item daalt tot onder een minimum dat is opgegeven in de instellingen voor de voedergegevens.
+++

+++([!DNL Google Ads] campagnes) De veranderingen in de vertoningsnamen voor mijn [!DNL Google] - gevolgd omzettingen werden teruggedraaid.

Als u de weergavenamen van de conversiemetriek wijzigt in Zoeken, Sociaal en Commerce, worden de wijzigingen overschreven met de namen die zijn geconfigureerd in [!DNL Google Ads] . Wijzig de naam in [!DNL Google Ads] .
+++

+++(Google Ads-campagnes) Kan ik een gedeeld budget gebruiken voor campagnes in portfolio&#39;s?

Voor beste resultaten, voeg geen [!DNL Google Ads] campagnes aan een [!DNL Google Ads] gedeelde begroting toe als zij in geoptimaliseerde portefeuilles zijn die aan &quot; [!UICONTROL Auto adjust campaign budget limits]&quot;worden gevormd.&quot; Als u dat doet, overschrijft [!DNL Google Ads] de voor de campagne geoptimaliseerde budgetten voor Zoeken, Sociaal zoeken en Commerce, wat tot inefficiënties bij biedingen kan leiden.
+++

+++([!DNL Google Ads] campagnes) Kan ik mobiele en niet-mobiele gebruikers naar verschillende bestemmingspagina&#39;s sturen?

Met de [!DNL Google Ads] [!DNL ValueTrack] parameters `{ifmobile}` en `{ifnotmobile}` kunt u op twee manieren de domeinnaam van de bestemmingspagina bepalen, zoals van toepassing is op uw sites:

* Neem de mobiele aanduiding op als de hostserver met `{ifmobile:m}{ifnotmobile:www}` .

  `http://{ifmobile:m}{ifnotmobile:www}.example.com` neemt mobiele gebruikers bijvoorbeeld naar m.example.com en niet-mobiele gebruikers naar www.example.com.

* Neem de mobiele aanduiding op als het domein op het hoogste niveau met `{ifmobile:mobi}{ifnotmobile:com}` .

  `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` neemt mobiele gebruikers bijvoorbeeld naar www.example.mobi en niet-mobiele gebruikers naar www.example.com.

In beide gevallen bevatten de basis-URL&#39;s met URL&#39;s voor zoeken, sociaal en Commerce-tracking de niet-gecodeerde `{}` -tags en eventuele aanvullende parameters die aan de basis-URL zijn toegevoegd.

>[!NOTE]
>
>Gebruik geen volledige URL als waarde voor ifnotmobile- en ifmobile-parameters; gebruik alleen het variabele gedeelte van de URL (zoals &quot;m&quot; versus &quot;www&quot; of &quot;mobi&quot; versus &quot;com&quot;).

+++

+++([!DNL Google Ads] campagnes op het onderzoeksnetwerk) Welke gegevens voor vandaag worden getoond?

[!DNL Google Ads] campagne-vlakke prestatiesmetriek op het onderzoeksnetwerk voor de huidige dag wordt getrokken bij 08 :00 en 16 :00 in de de tijdzone van de adverteerder.

Op het tabblad [!UICONTROL Campaigns] in zowel de [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] -weergave als de [!UICONTROL Optimization] > [!UICONTROL Portfolios] -weergave bevatten de gegevens de laatst gesynchroniseerde gegevens wanneer u rapporteert over [!UICONTROL Today] of een aangepast datumbereik dat de huidige dag bevat.

>[!NOTE]
>
>De gegevens voor kliks, impressies, en omzettingen worden vertraagd met drie uur en zijn niet volledig tot de volgende gegevens trekken.

+++

+++Wat is het verschil tussen een volgsjabloon en een achtervoegsel van een landingspagina?

Gebruik het achtervoegsel van een bestemmingspagina alleen voor advertentienetwerken die parallelle tracking ondersteunen. In Zoeken, Sociaal, &amp; Commerce, zowel zouden het volgen malplaatjes als het landen van paginaaanvoegsels een klikherkenningsteken van het advertentienetwerk moeten omvatten, maar het volgen malplaatjes omvatten extra het volgen parameters.

Zie volgende Veelgestelde vragen over [&#x200B; parallelle het volgen steun &#x200B;](#parallel-tracking) voor meer informatie over hoe het volgen malplaatjes en het landen paginaaparaafjes worden geladen wanneer een gebruiker een advertentie klikt.

+++

+++([!DNL Google Ads] en [!DNL Microsoft Advertising]) Biedt Search, Social en Commerce ondersteuning voor parallelle tracering voor advertenties in [!DNL Google Ads] of [!DNL Microsoft Advertising] ? {#parallel-tracking}

Parallel volgen verzendt klanten direct van uw advertentie naar uw definitieve URL, die toegevoegde parameters van een definitief achtervoegsel URL, of &quot;het landen paginaachtervoegsel&quot;kan omvatten. De URL van de trackingsjabloon (met extra parameters voor klikmeting) wordt afzonderlijk geladen op de achtergrond. Hierdoor wordt de landingspagina sneller geladen.

Zoeken, Sociaal en Commerce ondersteunt parallelle tracering voor zoek- en winkelcampagnes met de klikidentificatie van het advertentienetwerk (`msclkid` for [!DNL Microsoft Advertising]; `gclid` for [!DNL Google Ads] ). Gebruik een [&#x200B; rekening-niveau &#x200B;](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings) of [&#x200B; campagne-niveau &#x200B;](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix] (geroepen &quot;[!DNL final URL suffix]&quot;in de advertentienetwerken), die aan het landen van pagina URLs wordt toegevoegd om kliks op kindadvertenties van browsers te volgen die parallel volgen steunen. Zie [&#x200B; vereiste achtervoegselformaten voor  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) en [&#x200B; vereiste achtervoegselformaten voor  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

Wanneer een gebruiker uw advertentie weergeeft in een browser die geen parallelle tracering ondersteunt, gebruikt het advertentienetwerk in plaats daarvan sequentiële tracking: klanten worden eerst verzonden naar de URL van de trackingsjabloon, die klanten kan doorsturen naar tussenliggende trackingservers voordat ze worden doorgestuurd naar de laatste URL (die mogelijk aanvullende parameters bevat in het achtervoegsel van een bestemmingspagina). Alle volgende sjablonen voor een advertentienetwerkaccount moeten dezelfde klikid-parameter bevatten die u in de [!UICONTROL Landing Page Suffix] gebruikt. Zie [&#x200B; het volgen malplaatjevormen voor  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) en [&#x200B; het volgen malplaatjeformaten voor  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).
+++

+++Waarom bevat het bijhouden van URL&#39;s voor mijn advertenties &quot;`&EV_HASH={<hash>}`&quot;?

Wanneer u advertenties uploadt gebruikend de voer van de a [&#x200B; productinventaris &#x200B;](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) voor een rekening met het Onderzoek, Sociale, &amp; de pixelomleiding van Commerce en met sleutelwoord en creatief-vlakke volgen, dan voegt het Onderzoek, Sociale, &amp; Commerce de knoeiboelparameter en waarde aan het volgende malplaatje of bestemmingsURL van de advertentie toe om te identificeren dat het gebruikend de eigenschap van de inventarisvoer werd gecreeerd.
+++

## Voorraadvoeding

+++(Productvoorraadfeeds) Moet ik advertenties pauzeren of verwijderen die verouderd zijn of bestemd zijn voor een product waarvan het voorraadniveau onder een bepaald minimum ligt?

Dit hangt af van de zakelijke vereisten van de adverteerder.

Als u advertenties pauzeert, worden ze opnieuw geactiveerd als u dezelfde advertentie opnieuw verzendt of als het voorraadniveau boven het minimum ligt. Zo kunt u de geschiedenis van de advertentie behouden.

Wanneer u advertenties verwijdert en opnieuw verzendt, worden nieuwe advertenties gemaakt en moeten historische gegevens worden verzameld voor de nieuwe advertenties. Als u verwijderde advertenties niet verwacht opnieuw te verzenden, is het echter niet belangrijk historische gegevens te hebben.
+++

+++(Productvoorraadfeeds) Als ik een advertentiesjabloon verwijder en vervolgens een nieuwe, identieke sjabloon maak, worden ontbrekende items in het volgende voederbestand gepauzeerd (wanneer de instellingen van het feed-bestand hiervoor zijn geconfigureerd)?

Als het volgende voederdossier regelpunten mist en u niet eerder die lijnpunten van het nieuwe malplaatje via een vorig voederdossier hebt gepost, dan worden de ontbrekende lijnpunten niet erkend als &quot;ontbrekend,&quot;zodat worden zij niet gecreeerd. Om dit te vermijden, verspreidt u het vorige voederdossier door het nieuwe malplaatje en post de gegevens alvorens gegevens van een nieuw dossier te verspreiden en te posten.
+++

+++(Productvoorraadfeeds) Kan ik de prijzen voor mijn producten bijwerken zonder dat dit van invloed is op de kwaliteitsscore van een advertentie?

Voor [!DNL Google Ads] -campagnes ja: met de variabelen [!DNL Google Ads] `{Param 1}` en `{Param 2}` kunt u dynamisch numerieke waarden in een advertentievariatie invoegen zonder de advertentie te verwijderen en opnieuw te maken, en dus zonder dat dit van invloed is op de kwaliteitsscore.

Als u een variabele `{Param 1}` of `{Param 2}` voor uw prijsgegevens wilt gebruiken, wijst u de prijskolom in het gegevensbestand toe aan die variabele in de desbetreffende voedersjablonen en neemt u vervolgens de variabele op in uw advertentiesjablonen.

Als de kolom bijvoorbeeld Prijs heet, opent u de feed-sjabloon waarmee de advertenties worden gemaakt, klikt u in het invoerveld naast **[!UICONTROL Param 1]** en vervolgens op de kolom **[!UICONTROL Price]** in de lijst [!UICONTROL Feeds/Available Columns] , die `[Price]` als waarde voor [!UICONTROL Param 1] invoegt. Voeg vervolgens in de advertentiesjabloon onder aan de feed-sjabloon `{param1:default text}` in, waarbij &#39;standaardtekst&#39; tekst is die moet worden gebruikt als de parameterkolom in het feed-bestand leeg is voor een advertentierij.

Wanneer u gegevens verzendt, kunnen de gegevensvelden voor de kolommen [!UICONTROL Param1] en [!UICONTROL Param2] maximaal 25 tekens bevatten, waaronder numerieke gegevens, valutasymbolen en valutacodes, en de volgende niet-numerieke tekens: `, . % + - /`
+++

+++Mijn campagnes die zijn gegenereerd op basis van voorraadfeeds hebben veel verweesde transacties.

Als de [&#x200B; montages van voedergegevens &#x200B;](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) worden gevormd om advertenties in diverse situaties te schrappen, dan om het even welke vertraagde omzettingen die na kliks op de advertentie voorkomen kunnen [&#x200B; wezen transacties &#x200B;](/help/search-social-commerce/glossary.md#o-p) veroorzaken. De beste manier is om advertenties te pauzeren in plaats van ze te verwijderen. Als een advertentie na lange tijd nog steeds geen inkomsten heeft ontvangen, kunt u deze verwijderen via een bulksblad of de weergave Advertentiebeheer.
+++

## Prestatieproblemen met betrekking tot account en campagne

+++Sommige van mijn campagnes geven min of meer uit dan de campagnebegrotingen.

* Dit is normaal in een geoptimaliseerde portefeuille die met &quot;[!UICONTROL Auto adjust campaign budget limits]&quot;optie wordt gevormd. Wanneer deze optie wordt toegelaten, kunt u tot *N* keer de begroting van elke campagne doorgeven, waar *N* de waarde van &quot;[!UICONTROL Multiple]&quot;het plaatsen is. Met deze optie kan de optimalisatiecapaciteit de uitgaven voor afzonderlijke campagnes zo nodig aanpassen en de hele portfolio zo sturen dat de doelstelling wordt gehaald.
* Als [!DNL Google Ads] campagnes een gedeeld budget gebruiken, dan [!DNL Google Ads] past uitgaven voor individuele campagnes zonodig aan om het volledige gedeelde budget uit te geven.
+++
