---
title: Overzicht van het uitvoeren van en netwerkrekeningen en campagnes
description: Leer over de taken betrokken bij vestiging, het synchroniseren, en het beheren van uw rekeningen van het advertentienetwerk.
exl-id: 401c5ebb-258c-4614-96e8-ca604fc698c0
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 0%

---

# Overzicht van het uitvoeren van en netwerkrekeningen en campagnes

Adobe werkt met elke adverteerder aan opstelling zijn rekeningen en campagnes van het advertentienetwerk. Dit omvat het configureren van Zoeken, Sociale &amp; Handel om verbinding te maken met en te synchroniseren met de accounts van de adverteerder, het maken van nieuwe campagnes en campagnecomponenten indien nodig, het instellen van tracering voor componentadvertenties, het optioneel toevoegen van campagnes aan portfolio&#39;s om Zoeken, Sociale &amp; Handel toe te staan om de biedingen op advertenties te optimaliseren en het valideren van de initiële kosten-, klik- en inkomstengegevens.

Nadat een campagne is geactiveerd en optioneel aan een portfolio is toegevoegd, moeten het Adobe-accountbeheerteam, het agententeam of de adverteerder (afhankelijk van de voorwaarden van de serviceniveau-overeenkomst) elke-campagne volgen en de relevante onderdelen en instellingen zo nodig wijzigen om aan de doelstellingen van de adverteerder te voldoen.

Deze pagina bevat informatie over alle accounttypen, zoals hoe u de campagnestructuur voor gesynchroniseerde accounts kunt instellen. Voor aanvullende instructies voor het instellen van alleen-trackingaccounts voor [!DNL Naver], zie &quot;[Implementeren [!DNL Naver] accounts met alleen traceren](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

## Eerste instellingstaken voor accounts en campagnes

[!DNL Adobe] en/of uw bureau werkt met u als volgt samen:

1. (Nieuwe adverteerderaccounts) Administratieve accounts instellen:

   1. Stel het account van de adverteerder in.

   1. (Indien nodig) Maak gebruikersaccounts voor de adverteerder om de campagnegegevens te bekijken en te beheren en rapporten te genereren.

1. (Sommige advertentienetwerken) Verkrijg vergunning voor Onderzoek, Sociale, &amp; Handel om tot elke rekening toegang te hebben gebruikend API van het advertentienetwerk en het Onderzoek, Sociale, &amp; de gebruikersinterface van de Handel.

1. Voor elke advertentie-netwerkaccount:

   1. (Indien nodig) Stel de account in op het advertentienetwerk.

   1. Integreren met de account van [een corresponderend accountrecord maken](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) in Zoeken, Sociale Zaken, &amp; Handel die de de toegangsgeloofsbrieven van de rekeningstoegang en het volgen opties bevatten, en de rekeningsstatus plaatsen aan toegelaten.

      Zoek, Sociale, &amp; Handel synchroniseert dan met het advertentienetwerk. Als de account al campagnegegevens bevat, zijn de gegevens over ongeveer 24 uur beschikbaar.

   1. ([Typen toevoegen die u kunt maken/bewerken](/help/search-social-commerce/introduction/supported-inventory.md) in Zoeken, Sociaal, &amp; Handel) Als de account nog geen campagnegegevens bevat, maakt u dan een campagnestructuur en campagnecomponenten vanuit Zoeken, Sociale Zaken en Handel met een van de volgende methoden die beschikbaar zijn voor het advertentietype:

      * (Google Ads, Microsoft Advertising, Yahoo! Advertenties en alleen Yandex-accounts) Een [geautomatiseerd proces voor het maken van dynamische advertenties en trefwoorden voor elk item in uw voorraad](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) op basis van een ad-netwerkspecifieke advertentiesjabloon die u maakt en de inhoud van voorraadgegevensbestanden die u uploadt naar een FTP-locatie.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads en alleen Yandex-accounts) Uploaden [bulksheet-bestanden](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) die zoveel gegevens bevatten als u wilt voor een account en deze vervolgens naar de advertentienetwerken posten.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads (en alleen Yandex-accounts) Voer gegevens voor afzonderlijke componenten rechtstreeks in de interface in. Voor de meeste campagne en advertentietypes, kunt u gegevens op campagnereniveau, en groepsniveau, en individuele sleutelwoord, plaatsing, en advertentieniveaus tot stand brengen.

      Voor sommige campagne- en advertentietypen zijn echter unieke workflows vereist. Zie instructies voor het instellen [[!DNL Microsoft Advertising] winkelcampagnes](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md), [[!DNL Google Ads] dynamische zoekopdrachten](/help/search-social-commerce/campaign-management/special-campaign-types/google-dynamic-search-ads.md), [[!DNL Google Ads] maximale prestatiecampagnes](/help/search-social-commerce/campaign-management/special-campaign-types/google-performance-max-campaigns.md), en [[!DNL Google Ads] winkelcampagnes](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md).

   1. ([!DNL Naver] alleen accounts voor bijhouden) Uploaden [bulksheet-bestanden](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) met gegevens die de bestaande campagnes, groepen en trefwoorden in Zoeken, Sociale Zaken en Handel moeten repliceren zonder ze naar te posten [!DNL Naver].

1. Stel het bijhouden van wijzigingen in voor alle advertenties waarvoor de Adobe Advertising conversies bijhoudt:

   1. (Adverteerders met de dienst voor het bijhouden van Adoben Advertising) Indien nodig, [instellen, klik bijhouden](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) voor advertenties, en optioneel voor trefwoorden, plaatsingen en extensies door URL&#39;s voor het bijhouden van klikken op Zoeken, Sociale media en Handel te genereren en te uploaden.

      Voor [!DNL Google Ads] maximale prestatiecampagnes, alle &#39;tracking&#39; instellen in de [instellingen voor bijhouden van campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md).

1. Voor het volgen-slechts campagnes, moet u bestemmings URLs in plaats daarvan produceren gebruikend bulksbladen, en dan de geproduceerde bestemmings URLs toevoegen aan de relevante entiteiten gebruikend de inheemse redacteur van het advertentienetwerk.

   1. Conversie bijhouden instellen. Afhankelijk van de implementatie kan dit het toevoegen van codes voor het bijhouden van conversies aan de webpagina&#39;s van de adverteerder en/of het instellen van een dagelijkse feed-drop voor conversiegegevens die de adverteerder afzonderlijk heeft verzameld.

      Als u de service voor het bijhouden van Adoben Advertising voor conversie gebruikt, kunt u conversietags genereren [binnen Zoeken, Sociale &amp; Handel](/help/search-social-commerce/tools/conversion-tag-generate.md) of [gebruiken, Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html).

   1. Valideer de gegevens die worden bijgehouden.

   Zie het hoofdstuk over &quot;Tekstspatiëring&quot; voor meer informatie over het instellen van tekstspatiëring.

1. (Adverteerders met Adobe Analytics) [Adobe Advertising en analyse integreren](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) zodat zij gegevens kunnen uitwisselen.

1. (Zoeken, sociale zaken en handel toestaan om biedingen en/of campagnebudgetten te optimaliseren; [ondersteunde typen campagne](/help/search-social-commerce/introduction/supported-inventory.md) alleen) [De campagne toewijzen aan een portfolio](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md).

   Als het portfolio nog niet is gestart (voor het optimaliseren van biedingen en/of budgetten), kunt u ervoor zorgen dat de optimalisatiefunctie voldoende gegevens verzamelt om kosten- en inkomstenmodellen te maken, zodat u de basislijnprestaties voor het portfolio kunt bepalen voordat u het portfolio start.

   Als het portfolio al is gestart, schakelt u het leren voor het portfolio in. Zie &quot;De portfoliostrategieën aanpassen&quot; voor meer informatie. U zou moeten verwachten dat de portefeuille vluchtig is nadat u nieuwe campagnes toevoegt, terwijl de optimaliseringscapaciteit gegevens over de de biedingseenheden van de campagne verzamelt. Het bieden wordt automatisch binnen een tot drie weken aangepast.

   Zie de Optimalisatiegids, die beschikbaar is in Zoeken, Sociale &amp; Handel, voor meer informatie over portfolio&#39;s.<!-- verify convention for referencing Optimization Guide here -->

1. (Als er nieuwe omzettingen worden bijgehouden voor de adverteerder) [De conversies beschikbaar maken](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) voor rapporten, campagnebeheerweergaven en portfoliodoelstellingen.

1. Voor elke campagne, verifieer dat Onderzoek, Sociale, &amp; Handel klikgegevens van het advertentienetwerk ontvangt, en de opbrengstgegevens bevestigt die in Onderzoek, Sociale, &amp; Handel met de eigen inkomstengegevens van adverteerders worden getoond.

1. (Optioneel) Automatiseer rapportage door rapportsjablonen, spreadsheetfeeds en FTP-levering van geplande rapporten in te stellen.

   Zie het hoofdstuk over &quot;Rapporten&quot; voor instructies.

>[!MORELIKETHIS]
>
>* [Informatie over campagnebeheer in Zoeken, Sociale Zaken en Handel](campaign-management-about.md)
>* [De prestaties van uw advertentienetwerkcampagnes bewaken en beheren](monitor-performance-campaigns.md)
>* [Google Ads-conversiegegevens in Zoeken, Sociale Zaken en Handel](google-conversion-data.md)
>* [Ondersteunde voorraad](/help/search-social-commerce/introduction/supported-inventory.md)
