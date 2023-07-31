---
title: Veelgestelde vragen over campagnes
description: Zie antwoorden op vragen over campagnebeheer en de mening van campagnegegevens.
exl-id: b5975869-4bc3-461d-8cb7-eeefab157137
feature: Search Campaign Management
source-git-commit: f21283731d7a1830af585cec43805c54c81c72ff
workflow-type: tm+mt
source-wordcount: '1472'
ht-degree: 0%

---

# Veelgestelde vragen over campagnebeheer

## Algemene informatie

+++Kan ik campagnes en componenten van één rekening naar een andere verplaatsen?

Verplaats of kopieer geen campagne of campagnecomponent, die een unieke identiteitskaart heeft, naar een rekening met een verschillende rekening ID. Dit leidt tot gegevensfouten.
+++

+++Wanneer wordt de klikgegevens bijgewerkt van de advertentienetwerken?

Het proces waarbij de klikgegevens van de vorige dag van de zoekmachines worden opgehaald, begint om 6:00 uur in de tijdzone van de adverteerder.

Daarnaast [!DNL Google Ads] prestaties op campagnereniveau op het onderzoeksnetwerk voor de huidige dag worden getrokken bij 08:00 en 16:00 in de tijdzone van de adverteerder.
+++

+++Welke acties veroorzaken sleutelwoorden en advertenties om hun geschiedenis te verliezen?

>[!NOTE]
>
>(Advertisers met portefeuilles) Verwacht dat de prestaties van nieuwe sleutelwoord en gelijke typecombinaties vluchtig zijn terwijl Onderzoek, Sociale, &amp; Handel gegevens verzamelt om nieuwe modellen tot stand te brengen.

**Handelingen in de [!UICONTROL Search] > [!UICONTROL Campaigns] meningen, in het bulksheet het posten proces, en in de eigen redacteur van het ad netwerk:**

Het bestaande trefwoord of de bestaande advertentie wordt verwijderd en er wordt een andere advertentie gemaakt wanneer:

* ([!DNL Baidu], [!DNL Google Ads], en [!DNL Yandex]) U bewerkt een trefwoordnaam.

* ([!DNL Google Ads], [!DNL Microsoft Advertising], en [!DNL Yandex]) U wijzigt het type overeenkomst van een trefwoord.

* U verplaatst een trefwoord tussen advertentiegroepen.

* ([!DNL Google Ads] dynamische zoekopdrachten, [!DNL Microsoft Advertising] uitgevouwen tekstadvertenties en alle soorten advertenties op andere ondersteunde advertentienetwerken) U bewerkt en kopieert (titel/titel of beschrijving) of een afbeelding van de advertentie.

* U verplaatst een advertentie tussen advertentiegroepen.

**Gebeurtenissen in het proces voor het posten van de feed-in van de productvoorraad:**

Een bestaande advertentie of een bestaand trefwoord wordt verwijderd en er wordt een andere advertentie of trefwoord gemaakt wanneer:

* Een feed-bestand bevat een nieuwe waarde voor een kolom die wordt gebruikt in een advertentievariatie.

* De malplaatjemontages voor een advertentie veranderden sinds de laatste propagatie.

* Een nieuw feed-bestand bevat een rij voor een advertentie of trefwoord dat a) zich in een vorig bestand bevond, maar b) is sindsdien weggelaten en is gepauzeerd of verwijderd volgens de instellingen van de voedergegevens.

Afhankelijk van de [gegevensinstellingen van feed](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings), kan een bestaande advertentie of een bestaand trefwoord worden verwijderd wanneer:

* Een nieuw feed-bestand bevat geen rij voor een bestaande advertentie of een bestaand trefwoord.

* De geplande einddatum voor de componenten van een gepost voederdossier komt voor.

* Het voorraadniveau van een item daalt tot onder een minimum dat is opgegeven in de instellingen voor de voedergegevens.
+++

++([!DNL Google Ads] campagnes) Veranderingen in de vertoningsnamen voor mijn [!DNL Google]-tracked conversies werden teruggedraaid.

Als u de vertoningsnamen van de omzettingsmetriek in Onderzoek, Sociale, &amp; Handel verandert, worden uw veranderingen beschreven met de namen die binnen worden gevormd [!DNL Google Ads]. Wijzig namen in [!DNL Google Ads].
+++

+++ (Google Ads-campagnes) Kan ik een gedeeld budget gebruiken voor campagnes in portfolio&#39;s?

Voor de beste resultaten kunt u het beste de opdracht Niet toevoegen [!DNL Google Ads] campagnes voor een [!DNL Google Ads] gedeelde begroting als zij in geoptimaliseerde portefeuilles zijn die aan &quot; worden gevormd[!UICONTROL Auto adjust campaign budget limits].&quot; Als u dat doet, [!DNL Google Ads] Hiermee overschrijft u de voor de campagne geoptimaliseerde budgetten voor Zoeken, Sociale Zaken en Handel, wat kan leiden tot inefficiënties bij biedingen.
+++

++([!DNL Google Ads] campagnes) Kan ik mobiele en niet-mobiele gebruikers naar verschillende bestemmingspagina&#39;s sturen?

U kunt de [!DNL Google Ads] [!DNL ValueTrack] parameters `{ifmobile}` en `{ifnotmobile}` om de domeinnaam van de landingspagina op één van twee manieren te bepalen, zoals toepasselijk voor uw plaatsen:

* De mobiele aanduiding opnemen als hostserver met `{ifmobile:m}{ifnotmobile:www}`.

  Bijvoorbeeld: `http://{ifmobile:m}{ifnotmobile:www}.example.com` gaat mobiele gebruikers naar m.example.com en niet-mobiele gebruikers naar www.example.com.

* De mobiele aanduiding opnemen als het domein op het hoogste niveau dat `{ifmobile:mobi}{ifnotmobile:com}`.

  Bijvoorbeeld: `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` gaat mobiele gebruikers naar www.example.mobi en niet-mobiele gebruikers naar www.example.com.

In beide gevallen bevatten de niet-gecodeerde basis-URL&#39;s met de URL&#39;s voor Zoeken, Sociaal en Handel `{}` tags en eventuele aanvullende parameters die aan de basis-URL zijn toegevoegd.

>[!NOTE]
>
>Gebruik geen volledige URL als waarde voor ifnotmobile- en ifmobile-parameters; gebruik alleen het variabele gedeelte van de URL (zoals &quot;m&quot; versus &quot;www&quot; of &quot;mobi&quot; versus &quot;com&quot;).

+++

++([!DNL Google Ads] campagnes op het onderzoeksnetwerk) Welke gegevens worden getoond voor vandaag?

[!DNL Google Ads] prestaties op campagnereniveau op het onderzoeksnetwerk voor de huidige dag worden getrokken bij 08:00 en 16:00 in de tijdzone van de adverteerder.

In de [!UICONTROL Campaigns] in beide [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] en de [!UICONTROL Optimization] > [!UICONTROL Portfolios] bekijken wanneer u rapporteert over [!UICONTROL Today] Voor een aangepast datumbereik dat de huidige dag bevat, bevatten de gegevens de gegevens die het laatst zijn verzameld.

>[!NOTE]
>
>De gegevens voor kliks, impressies, en omzettingen worden vertraagd met drie uur en zijn niet volledig tot de volgende gegevens trekken.

+++

++([!DNL Google Ads] en [!DNL Microsoft Advertising]) Biedt via Search, Social &amp; Commerce ondersteuning voor parallelle tracering van advertenties in [!DNL Google Ads] of [!DNL Microsoft Advertising]?

Met parallelle tracering worden klanten rechtstreeks van uw advertentie naar de uiteindelijke URL gestuurd en wordt de URL van uw trackingsjabloon (met klikmeting) op de achtergrond geladen. Hierdoor wordt de landingspagina sneller geladen.

Search, Social &amp; Commerce ondersteunt parallelle tracering voor zoek- en winkelcampagnes met behulp van de klikidentificatie van het advertentienetwerk (`msclkid` for [!DNL Microsoft Advertising]; `gclid` for [!DNL Google Ads]). Een [op rekeningniveau](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings) of [campagneniveau](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix] (wordt &quot;[!DNL final URL suffix]&quot; in de advertentienetwerken), die aan het landen van pagina URLs wordt toegevoegd om te volgen klikt op kindadvertenties van browsers die parallel volgen steunen. Zie de [vereiste achtervoegselformaten voor [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) en [vereiste achtervoegselformaten voor [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

Wanneer een gebruiker uw advertentie weergeeft in een browser die geen parallelle tracering ondersteunt, gebruikt het advertentienetwerk sequentiële tracking in plaats daarvan: klanten worden eerst naar de URL van de trackingsjabloon verzonden, die klanten kan doorsturen naar tussenliggende trackingservers voordat ze naar de uiteindelijke URL worden omgeleid. Alle het volgen malplaatjes voor een advertentienetwerkrekening zouden de zelfde klik herkenningsteken parameter moeten omvatten die u in gebruikt [!UICONTROL Landing Page Suffix]. Zie de [sjabloonindelingen bijhouden voor [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) en de [sjabloonindelingen bijhouden voor [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).
+++

+++Waarom worden URL&#39;s voor mijn advertenties bijgehouden met &quot;`&EV_HASH={<hash>}`?&quot;

Wanneer u advertenties uploadt met een [productinventarisfeed](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) voor een account met de Pixelomleiding Zoeken, Sociale Zaken &amp; Handel en met het traceren van trefwoorden en creatief niveau, voegt Search, Social &amp; Commerce de hash-parameter en de waarde toe aan de trackingsjabloon of de doel-URL van de advertentie om te bepalen dat deze is gemaakt met de voorraadfeed-functie.
+++

## Voorraadvoeding

+++ (Product voorraad feeds) Moet ik advertenties pauzeren of verwijderen die verouderd zijn of bestemd zijn voor een product waarvan de voorraad onder een bepaald minimum ligt?

Dit hangt af van de zakelijke vereisten van de adverteerder.

Als u advertenties pauzeert, worden ze opnieuw geactiveerd als u dezelfde advertentie opnieuw verzendt of als het voorraadniveau boven het minimum ligt. Zo kunt u de geschiedenis van de advertentie behouden.

Wanneer u advertenties verwijdert en opnieuw verzendt, worden nieuwe advertenties gemaakt en moeten historische gegevens worden verzameld. Als u verwijderde advertenties niet verwacht opnieuw te verzenden, is het echter niet belangrijk historische gegevens te hebben.
+++

+++ (voer voor productinventarisatie) Als ik een advertentiesjabloon verwijder en vervolgens een nieuwe, identieke sjabloon maak, worden ontbrekende items in het volgende voederbestand gepauzeerd (wanneer de instellingen voor het voederbestand hiervoor zijn geconfigureerd)?

Als het volgende voederdossier regelpunten mist en u niet eerder die lijnpunten van het nieuwe malplaatje via een vorig voederdossier hebt gepost, dan worden de ontbrekende lijnpunten niet erkend als &quot;ontbrekend,&quot;zodat worden zij niet gecreeerd. Om dit te vermijden, verspreidt u het vorige voederdossier door het nieuwe malplaatje en post de gegevens alvorens gegevens van een nieuw dossier te verspreiden en te posten.
+++

+++ (Product voorraad feeds) Kan ik de prijzen voor mijn producten bijwerken zonder dat dit van invloed is op de kwaliteitsscore van een advertentie?

Voor [!DNL Google Ads] campagnes, ja: de [!DNL Google Ads] `{Param 1}` en `{Param 2}` Met variabelen kunt u dynamisch numerieke waarden in een advertentievariatie invoegen zonder de advertentie te verwijderen en opnieuw te maken, en dus zonder dat dit van invloed is op de kwaliteitsscore.

Een `{Param 1}` of `{Param 2}` variabele voor uw prijsgegevens, wijs de prijskolom in uw gegevensdossier aan die variabele in de aangewezen voedermalplaatjes toe, en neem dan de variabele in uw malplaatjes van de advertentievariatie op.

Als de kolom bijvoorbeeld Prijs heet, opent u de feed-sjabloon waarmee de advertenties worden gemaakt en klikt u in het invoerveld naast **[!UICONTROL Param 1]** en klik vervolgens op de knop **[!UICONTROL Price]** in de [!UICONTROL Feeds/Available Columns] lijst, die invoegt `[Price]` als de waarde voor [!UICONTROL Param 1]. Voeg vervolgens in de variatiesjabloon onder aan de voedersjabloon in `{param1:default text}`, waarbij &#39;standaardtekst&#39; tekst is die moet worden gebruikt als de parameterkolom in het feed-bestand leeg is voor een advertentierij.

Wanneer u gegevens verzendt, worden de gegevensvelden voor de [!UICONTROL Param1] en [!UICONTROL Param2] kolommen kunnen maximaal 25 tekens bevatten, waaronder numerieke gegevens, valutasymbolen en valutacodes, en de volgende niet-numerieke tekens: `, . % + - /`
+++

+++Mijn campagnes die uit voorraadfeeds worden geproduceerd hebben vele verweesde transacties.

Als de [gegevensinstellingen van feed](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) zijn geconfigureerd om advertenties in verschillende situaties te verwijderen, en eventuele vertraagde conversies die optreden nadat op de advertentie is geklikt, kunnen [verweesde transacties](/help/search-social-commerce/glossary.md#o-p). De beste manier is om advertenties te pauzeren in plaats van ze te verwijderen. Als een advertentie na een lange periode nog steeds geen inkomsten heeft ontvangen, kunt u deze verwijderen via een bulksblad of de weergave Advertentiebeheer.
+++

## Prestatieproblemen met betrekking tot account en campagne

+++Sommige van mijn campagnes geven meer of minder uit dan de campagnebegrotingen.

* Dit is normaal in een geoptimaliseerde portefeuille die met &quot;[!UICONTROL Auto-adjust campaign budget limits]&quot;. Als deze optie is ingeschakeld, kunt u maximaal *N* keer de begroting van elke campagne, waar *N* is de waarde van &quot;[!UICONTROL Multiple]&quot; instellen. Met deze optie kan de optimalisatiecapaciteit de uitgaven voor afzonderlijke campagnes zo nodig aanpassen en de hele portfolio zo sturen dat de doelstelling wordt gehaald.
* Indien [!DNL Google Ads] campagnes gebruiken een gedeeld budget, dan [!DNL Google Ads] de uitgaven voor individuele campagnes worden zo nodig aangepast om de gehele gedeelde begroting uit te geven .
+++
