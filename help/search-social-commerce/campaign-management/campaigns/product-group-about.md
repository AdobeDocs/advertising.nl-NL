---
title: Over winkelproductgroepen
description: Meer informatie over het winkelen van productgroepen tijdens winkelcampagnes.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 0%

---

# Over winkelproductgroepen

*[!DNL Google Ads]en [!DNL Microsoft Advertising] alleen winkelcampagnes*

Bij winkelcampagnes bepalen de productgroepen — en niet de trefwoorden — de producten in uw winkelcentrum-account waarvoor winkeladvertenties worden weergegeven. Elke productgroep is gebaseerd op één enkel productkenmerk (zoals categorie, producttype, merk, voorwaarde, product-id of aangepaste labels) en gebruikt hetzelfde bod voor alle overeenkomende producten. U kunt biedingen voor de producten in elke groep opnemen of uitsluiten.

U vormt productgroepen op het niveau van de advertentiegroep om te bepalen welke producten in uw bedrijfscentra rekeningen in de het winkelen advertenties voor de advertentiegroep verschijnen. Zelfs als de advertentiegroep geen ad entiteiten omvat, toont het advertentienetwerk nog advertenties voor de producten.

Wanneer hetzelfde product in meer dan één campagne is opgenomen, gebruikt het advertentienetwerk eerst de campagneprioriteit om te bepalen welke campagne (en het bijbehorende bod) in aanmerking komt voor de advertentieveiling. Wanneer alle campagnes dezelfde prioriteit hebben, is de campagne met het hoogste bod subsidiabel.

Meer informatie over [!DNL Google] winkelcampagnes en advertenties , zie &quot;[Implementeren [!DNL Google Ads] winkelcampagnes](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)&quot; en de [Google Ads-documentatie](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1). Raadpleeg voor meer informatie over Microsoft-winkelcampagnes &quot;[Implementeren [!DNL Microsoft® Advertising] winkelcampagnes](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)&quot; en de [Microsoft-advertentiedocumentatie](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>Ondersteuning is niet beschikbaar voor [!DNL Google Ads] het aanbieden van groepen in prestaties maximumcampagnes, die slimme het winkelen campagnes vervangen. Als u gegevens voor aanbiedingsgroepen wilt beheren en weergeven, gebruikt u de opdracht [!DNL Google Ads] editor.

## Hiërarchie van productgroepen

Voordat u productgroepen kunt maken met specifieke kenmerken voor een advertentiegroep, moet u eerst een inclusieve productgroep maken met de naam &quot;[!UICONTROL All Products].&quot; Vanuit deze bovenliggende productgroep kunt u onderliggende productgroepen maken voor subsets van producten en kleinkinderen maken van de onderliggende productgroepen. Wanneer u de eerste onderliggende productgroep voor een advertentiegroep hebt gemaakt, wordt een andere productgroep genaamd &quot;[!UICONTROL Everything Else]&quot; wordt automatisch gemaakt op basis van het standaardbod voor advertenties. Als u meer productgroepen toevoegt, wordt &quot;[!UICONTROL Everything Else]&quot; wordt dienovereenkomstig aangepast, zodat het alle producten betreft die niet tot een andere productgroep behoren.

Binnen een advertentiegroep kunt u tot zeven niveaus van productgroepen tot stand brengen (zonder &quot;[!UICONTROL All Products]&quot;) om een of meer productgroepen die zich op hetzelfde kenmerk richten, op elk niveau op te nemen in of uit te sluiten van biedingen (bijvoorbeeld [!UICONTROL Brand]=Acme voor één productgroep en [!UICONTROL Brand]=AcmePlus voor een andere op het zelfde niveau). Bovenliggende productgroepen worden onderverdelingen genoemd en het laagste niveau van onderverdelingen wordt eenheid genoemd. Je kunt biedingen en trackingsjablonen instellen of biedingen volledig uitsluiten op het niveau van de eenheid. De volledige reeks actieve productgroepen voor een advertentiegroep wordt hiërarchisch toegepast om de in aanmerking komende producten te bepalen. Als u bijvoorbeeld subdeelt [!UICONTROL All Products] in [!UICONTROL Brand]=AcmeBasic en [!UICONTROL Brand]=AcmePlus, en dan onderverdeelt u verder elk van die productgroepen in [!UICONTROL Condition]=Nieuwe en stel biedingen in. Alleen nieuwe producten met de merken AcmeBasic en AcmePlus mogen worden geadverteerd of van advertenties worden uitgesloten.

![Voorbeeld van een productgroepset](/help/search-social-commerce/assets/product-group-list.png "Voorbeeld van een productgroepset")

![Voorbeeld van hiërarchie van productgroepen](/help/search-social-commerce/assets/product-group-tree.png "Voorbeeld van hiërarchie van productgroepen")

## De [!UICONTROL Product Groups] weergave

U kunt productgroepen en onderliggende productgroepen maken en bewerken in de [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] weergeven.

## Traceergegevens en prestatiegegevens voor winkelproductgroepen

(Rekeningen/campagnes met &quot;[!UICONTROL EF Redirect]&quot;optie voor bijhouden&quot;) Als u Zoeken, Sociale Zaken en Handel wilt toestaan om conversies voor productgroepen bij te houden, [URL&#39;s voor bijhouden genereren voor productgroepen met het gereedschap URL&#39;s bijhouden](/help/search-social-commerce/tools/click-tracking-url-generate.md)en voer vervolgens een van de volgende handelingen uit:

* (Vereist voor [!DNL Google Ads]; beste praktijken voor [!DNL Microsoft Advertising]) Voeg de URL voor bijhouden toe aan de [!DNL Tracking Template] in de account-, campagne- of productgroepinstelling. Voeg deze op het hoogst mogelijke niveau toe om het onderhoud te vereenvoudigen. Om het even welke toevoegingsparameters die voor de rekening of de campagne worden gespecificeerd zijn niet inbegrepen.

   >[!CAUTION]
   >
   >([!DNL Microsoft Advertising]Gebruik deze optie alleen als u URL&#39;s voor het bijhouden van zoekopdrachten, sociale gegevens en handel niet opneemt in een aangepaste kolom in de productfeed. Als u beide instelt, bevatten de URL&#39;s twee omleidingen die verbroken koppelingen veroorzaken.

* ([!DNL Microsoft Advertising] alleen) Voeg de URL voor bijhouden toe aan de productgegevens in het dialoogvenster [!DNL Microsoft Merchant Center] account. Hiervoor neemt u de URL voor bijhouden op, samen met de waarde in het dialoogvenster `link` of `mobile_link` in een aangepaste kolom met de naam [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) in het diervoeder. URL&#39;s die met deze methode worden gegenereerd, bevatten geen volgparameters die zijn opgegeven in de account- of campagnemontages in Zoeken, Sociaal en Handel.

U kunt gegevens over productgroepen weergeven in [de [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [Winkelproductgroepen beheren](product-group-manage.md)
>* [[!DNL Google Ads] productgroepinstellingen](product-group-settings-google.md)
>* [Implementeren [!DNL Google Ads] winkelcampagnes](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] productgroepinstellingen](product-group-settings-microsoft.md)
>* [Implementeren [!DNL Microsoft® Advertising] winkelcampagnes](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)

