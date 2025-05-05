---
title: Overzicht van het uitvoeren van en netwerkrekeningen en campagnes
description: Leer over de taken betrokken bij vestiging, het synchroniseren, en het beheren van uw rekeningen van het advertentienetwerk.
exl-id: 36307e65-81f8-4794-8a75-a37623b294ed
feature: Search Campaign Management
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# Overzicht van het uitvoeren van en netwerkrekeningen en campagnes

Adobe werkt met elke adverteerder aan opstelling zijn rekeningen en campagnes van het advertentienetwerk. Dit omvat het configureren van Zoeken, Sociaal, &amp; Commerce voor verbinding en synchronisatie met de accounts van de adverteerder, het maken van nieuwe campagnes en campagnecomponenten, het instellen van tracering voor componentadvertenties, het optioneel toevoegen van campagnes aan portfolio&#39;s om Zoeken, Sociaal en Commerce in staat te stellen om het bod op advertenties te optimaliseren en het valideren van de initiële kosten, klikken en inkomstengegevens.

Nadat een campagne is geactiveerd en optioneel aan een portfolio is toegevoegd, moeten het accountbeheerteam van de Adobe, het agententeam of de adverteerder (afhankelijk van de voorwaarden van de serviceovereenkomst) elke campagne volgen en de relevante onderdelen en instellingen zo nodig wijzigen om aan de doelstellingen van de adverteerder te voldoen.

Deze pagina bevat informatie over alle accounttypen, zoals hoe u de campagnestructuur voor gesynchroniseerde accounts kunt instellen. Voor extra instructies bij vestiging het volgen-slechts rekeningen voor [!DNL Naver], zie &quot;[ uitvoeren  [!DNL Naver]  het volgen-slechts rekeningen ](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

## Eerste instellingstaken voor accounts en campagnes

[!DNL Adobe] en/of uw bureau werkt met u als volgt samen:

1. (Nieuwe adverteerderaccounts) Administratieve accounts instellen:

   1. Stel het account van de adverteerder in.

   1. (Indien nodig) Maak gebruikersaccounts voor de adverteerder om de campagnegegevens te bekijken en te beheren en rapporten te genereren.

1. (Sommige advertentienetwerken) Verkrijg vergunning voor Onderzoek, Sociale, &amp; Commerce om tot elk rekening toegang te hebben gebruikend API van het advertentienetwerk en het Onderzoek, Sociale, &amp; gebruikersinterface van Commerce.

1. Voor elke advertentie-netwerkaccount:

   1. (Indien nodig) Stel de account in op het advertentienetwerk.

   1. Integreer met de rekening door [ het creëren van een overeenkomstig rekeningsverslag ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#create-account) in Onderzoek, Sociaal, &amp; Commerce die de geloofsbrieven van de rekeningstoegang en het volgen opties bevatten, en plaats de rekeningsstatus aan toegelaten.

      Zoek, Sociaal, &amp; Commerce synchroniseert dan met het advertentienetwerk. Als de account al campagnegegevens bevat, zijn de gegevens over ongeveer 24 uur beschikbaar.

   1. ([ de types van Advertentie u ](/help/search-social-commerce/introduction/supported-inventory.md) in Onderzoek, Sociale, &amp; Commerce) kunt tot stand brengen/uitgeven als de rekening reeds campagnegegevens bevat, dan campagnestructuur en campagnecomponenten van binnen Onderzoek, Sociale, &amp; Commerce door om het even welke volgende methodes tot stand brengen die voor het advertentietype beschikbaar zijn:

      * (Google Ads, Microsoft Advertising, Yahoo! Adds, en Yandex slechts rekeningen) Opstelling een [ geautomatiseerd proces om dynamische advertenties en sleutelwoorden tot stand te brengen die aan elk punt in uw inventaris ](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) volgens een ad netwerk-specifiek advertentiemalplaatje worden gericht u en de inhoud van inventarisgegevensdossiers creeert u aan een plaats van FTP uploadt.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Adds, en Yandex slechts rekeningen) uploadt [ bulksheet dossiers ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) die zo veel gegevens bevatten aangezien u voor een rekening en dan hen aan de advertentienetwerken wilt posten.

      * (Baidu, Google Ads, Microsoft Advertising, Yahoo! Japan Ads (en alleen Yandex-accounts) Voer gegevens voor afzonderlijke componenten rechtstreeks in de interface in. Voor de meeste campagne en advertentietypes, kunt u gegevens op campagnereniveau, en groepsniveau, en individuele sleutelwoord, plaatsing, en advertentieniveaus tot stand brengen.

      Voor sommige campagne- en advertentietypen zijn echter unieke workflows vereist. Zie instructies voor vestiging [[!DNL Microsoft Advertising]  het winkelen campagnes ](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md), [[!DNL Google Ads]  dynamische onderzoeksadvertenties ](/help/search-social-commerce/campaign-management/special-workflows/google-dynamic-search-ads.md), [[!DNL Google Ads]  prestaties maximum campagnes ](/help/search-social-commerce/campaign-management/special-workflows/google-performance-max-campaigns.md), en [[!DNL Google Ads]  het winkelen campagnes ](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md).

   1. ([!DNL Naver] het volgen-slechts rekeningen) uploadt [ bulksheet dossiers ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) met gegevens om de bestaande campagnes, en groepen en sleutelwoorden in Onderzoek, Sociale, &amp; Commerce te herhalen zonder hen te posten aan [!DNL Naver].

1. Stel het bijhouden van wijzigingen in voor alle advertenties waarvoor de Adobe Advertising conversies bijhoudt:

   1. (Advertisers met de Adobe Advertising omzetting volgende dienst) indien nodig, [ opstelling klikt het volgen ](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) voor advertenties, en naar keuze voor sleutelwoorden, plaatsen, en voegt uitbreidingen door Onderzoek, Sociale, &amp; klik-volgende URLs te produceren en te uploaden Commerce.

      Voor [!DNL Google Ads] prestaties maximumcampagnes, opstelling allen die in de [ het volgen montages van de campagne volgen ](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) volgen.

1. Voor het volgen-slechts campagnes, moet u bestemmings URLs in plaats daarvan produceren gebruikend bulksbladen, en dan de geproduceerde bestemmings URLs toevoegen aan de relevante entiteiten gebruikend de inheemse redacteur van het advertentienetwerk.

   1. Conversie bijhouden instellen. Afhankelijk van de implementatie kan dit het toevoegen van codes voor het bijhouden van conversies aan de webpagina&#39;s van de adverteerder en/of het instellen van een dagelijkse feed-drop voor conversiegegevens die de adverteerder afzonderlijk heeft verzameld.

      Als u de Adobe Advertising conversie volgende dienst gebruikt, kunt u conversie volgende markeringen [ binnen Onderzoek, Sociaal, &amp; Commerce ](/help/search-social-commerce/tools/conversion-tag-generate.md) of [ produceren gebruikend Adobe Experience Platform ](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud.html?lang=nl-NL).

   1. Valideer de gegevens die worden bijgehouden.

   Zie het hoofdstuk over &quot;Tekstspatiëring&quot; voor meer informatie over het instellen van tekstspatiëring.

1. (Advertisers met Adobe Analytics) [ integreer Adobe Advertising en Analytics ](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=nl-NL) zodat zij gegevens kunnen ruilen.

1. (Om Onderzoek toe te staan, sociaal, &amp; Commerce om biedingen, campagnebegrotingen, en/of de strategiedoelstellingen van de campagnebiet te optimaliseren; [ gesteunde campagnetypes ](/help/search-social-commerce/introduction/supported-inventory.md) slechts) [ wijs de campagne aan een portefeuille ](/help/search-social-commerce/campaign-management/campaign-assign-to-portfolio.md) toe.

   Als het portfolio nog niet is gestart (voor het optimaliseren van biedingen en/of budgetten), kunt u ervoor zorgen dat de optimalisatiefunctie voldoende gegevens verzamelt om kosten- en inkomstenmodellen te maken, zodat u de basislijnprestaties voor het portfolio kunt bepalen voordat u het portfolio start.

   Als het portfolio al is gestart, schakelt u het leren voor het portfolio in. Zie &quot;De portfoliostrategieën aanpassen&quot; voor meer informatie. U zou moeten verwachten dat de portefeuille vluchtig is nadat u nieuwe campagnes toevoegt, terwijl de optimaliseringscapaciteit gegevens over de de biedingseenheden van de campagne verzamelt. Het bieden wordt automatisch binnen een tot drie weken aangepast.

   Voor meer informatie over portefeuilles, zie de Gids van de Optimalisering, die van binnen Onderzoek, Sociale, &amp; Commerce beschikbaar is.<!-- verify convention for referencing Optimization Guide here -->

1. (Als om het even welke nieuwe omzettingen voor adverteerder) [ zullen worden gevolgd maak de omzettingen beschikbaar ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) voor rapporten, de meningen van het campagnebeheer, en portefeuilledoelstellingen.

1. Voor elke campagne, verifieer dat Onderzoek, Sociaal, &amp; Commerce klikgegevens van het advertentienetwerk ontvangt, en de opbrengstgegevens die in Onderzoek, Sociale, &amp; Commerce met de eigen inkomstengegevens van adverteerders worden getoond bevestigt.

1. (Optioneel) Automatiseer rapportage door rapportsjablonen, spreadsheetfeeds en FTP-levering van geplande rapporten in te stellen.

   Zie het hoofdstuk over &quot;Rapporten&quot; voor instructies.

>[!MORELIKETHIS]
>
>* [ Ongeveer campagnebeheer in Onderzoek, Sociale, &amp; Commerce ](campaign-management-about.md)
>* [ Monitor en beheer de prestaties van uw campagnes van het advertentienetwerk ](monitor-performance-campaigns.md)
>* [ de omzettingsgegevens van Advertenties Google in Onderzoek, Sociale, &amp; Commerce ](google-conversion-data.md)
>* [ Gesteunde inventaris ](/help/search-social-commerce/introduction/supported-inventory.md)
