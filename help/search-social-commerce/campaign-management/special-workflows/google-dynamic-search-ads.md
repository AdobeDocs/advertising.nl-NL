---
title: Voer  [!DNL Google Ads]  dynamische onderzoeksadvertenties uit
description: Leer over het werkschema voor vestiging  [!DNL Google Ads]  dynamische onderzoeksadvertenties.
exl-id: 69e5069f-3f82-4ee3-841a-0c1292677223
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# [!DNL Google Ads] dynamische zoekadvertenties implementeren

*[!DNL Google Ads]alleen-zoekcampagnes met alleen creatief of trefwoord- en creatief bijhouden*

Dynamische zoekadvertenties gebruiken inhoud van uw website in plaats van trefwoorden om te bepalen wanneer u uw advertenties wilt weergeven. U kunt de pagina&#39;s in uw websites definiëren waarvan de inhoud wordt gebruikt om uw dynamische zoekadvertenties te activeren door afzonderlijke dynamische zoekdoelen voor de advertentiegroep in te stellen of door een instelling op campageniveau te kiezen om uw advertenties te richten met behulp van de inhoud van uw website.

U kunt dynamische zoekopdrachten afzonderlijk instellen of met behulp van bulksbladen. De volgende instructies bevatten koppelingen naar het maken van afzonderlijke entiteiten.

## Stappen voor het instellen van [!DNL Google Ads] dynamische zoekopdrachten

1. [&#x200B; creeer een campagne &#x200B;](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) voor dynamische onderzoeksadvertenties:

   1. Stel aanvankelijk het campagnebudget in op 10% van uw dagelijkse uitgaven voor de zoekcampagne.

      U kunt het budget later verhogen nadat de advertenties hun waarde hebben bewezen.

   1. (Als u [!DNL Google Ads] dynamische zoekopdrachten wilt laten weergeven op basis van de inhoud van uw website) Geef het hoofddomein en de taal voor het domein op in het gedeelte [!UICONTROL DSA Options] van de instellingen voor de campagne.

      >[!NOTE]
      >
      >Uw domein moet worden geïndexeerd door de [!DNL Google Ads] organische zoekindex die als doel moet worden ingesteld. Ook, als het domein pagina&#39;s in veelvoudige talen bevat en u alle hen wilt richten, creeer een afzonderlijke campagne voor elke taal.

      Als u uw websitedomein niet gebruikt om uw advertenties te richten, creeer dan dynamische onderzoeksdoelstellingen (zie Stap 4) voor elke advertentiegroep. U kunt de doelstellingen [&#x200B; individueel &#x200B;](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) tot stand brengen of [&#x200B; bulkbladen &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) gebruiken.

   1. Zorg ervoor dat de campagne gericht is op het onderzoekskanaal en slechts het [!DNL Google Ads] onderzoeksnetwerk (niet het vertoningsnetwerk). Deze instellingen zijn beschikbaar op het tabblad [!UICONTROL Networks and Devices] .

   1. (Optioneel) Trefwoorden uitsluiten op het tabblad [!UICONTROL Negatives] .

   1. (Optioneel) Configureer een sjabloon voor bijhouden op campagneniveau, dat de sjabloon voor bijhouden op accountniveau overschrijft, maar op lagere niveaus kan worden overschreven.

      (Adverteerders met Adobe Analytics zonder tracering aan de serverzijde) Als u het bijhouden van gegevens voor de reverse-feed van Zoeken, Sociaal en Commerce naar Analytics wilt opnemen, voegt u de trackingcode van de AMO-id toe aan de toevoegingsparameters op accountniveau, waarmee de code aan de uiteindelijke URL wordt toegevoegd. Zie &quot;[&#x200B; Adobe Advertising IDs die door  [!DNL Analytics]](/help/integrations/analytics/ids.md) wordt gebruikt.&quot;

1. [&#x200B; creeer een advertentiegroep &#x200B;](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) binnen de campagne, met inbegrip van de volgende stappen:

   1. Stel de [!UICONTROL Ad Group Type] in op **[!UICONTROL Search Dynamic].**

   1. Stel het standaardbod voor alle advertenties in.

      U kunt het standaardbod voor afzonderlijke dynamische zoekdoelen overschrijven als u deze configureert.

   1. (Optioneel) Configureer een volgsjabloon op ad-groepsniveau, dat eventuele volgsjablonen op hogere niveaus overschrijft, maar op advertentieniveau kan worden overschreven.

      Als u het bijhouden van Adobe Analytics op campagnereniveau hebt toegevoegd en u wilt deze voor de advertentiegroep opnemen, voegt u deze hier toe. Zie stap 1e.

1. [&#x200B; creeer elke dynamische onderzoeksadvertentie &#x200B;](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) binnen de advertentiegroep.

   [!DNL Google Ads] genereert dynamisch de kop, de weergave-URL en de bestemmingspagina-URL voor elke advertentie. U kunt optioneel omleidingen en tekstspatiëring toevoegen aan de sjabloon voor reeksspatiëring op advertentieniveau, die de volgsjablonen op hogere niveaus overschrijft.
Als u het bijhouden van Adobe Analytics&#39;s op hogere niveaus wilt overschrijven met het bijhouden van advertenties, voegt u deze hier toe. Zie de stappen 1e en 2c.

1. (Vereist wanneer u niet het worteldomein en de taal voor het domein in de sectie van Opties DSA van de campagnemontages omvat; facultatief anders) creeer [&#x200B; dynamische onderzoeksdoelstellingen &#x200B;](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) voor de advertentiegroep. U kunt optioneel het advertentieniveau overschrijven met biedingen op doelniveau.

   De doelen bepalen of het advertentienetwerk alle pagina&#39;s of een subset van de pagina&#39;s in uw website gebruikt om uw dynamische zoekadvertenties te richten. Om de prestaties het best te volgen, vorm uw campagne met één ad groep per dynamisch onderzoeksdoel, en omvat een ad groep die alle criteria richt.

1. Zoals noodzakelijk, [&#x200B; geef de campagnemontages &#x200B;](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) uit om het campagnebudget aan te passen en verkeer te verfijnen door extra sleutelwoorden van de campagne te uitsluiten.
