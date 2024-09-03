---
title: Over winkelproductgroepen
description: Meer informatie over het winkelen van productgroepen tijdens winkelcampagnes.
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# Over winkelproductgroepen

*[!DNL Google Ads]en [!DNL Microsoft Advertising] alleen winkelcampagnes*

Bij winkelcampagnes bepalen de productgroepen — en niet de trefwoorden — de producten in uw winkelcentrum-account waarvoor winkeladvertenties worden weergegeven. Elke productgroep is gebaseerd op één enkel productkenmerk (zoals categorie, producttype, merk, voorwaarde, product-id of aangepaste labels) en gebruikt hetzelfde bod voor alle overeenkomende producten. U kunt biedingen voor de producten in elke groep opnemen of uitsluiten.

U vormt productgroepen op het niveau van de advertentiegroep om te bepalen welke producten in uw bedrijfscentra rekeningen in de het winkelen advertenties voor de advertentiegroep verschijnen. Zelfs als de advertentiegroep geen ad entiteiten omvat, toont het advertentienetwerk nog advertenties voor de producten.

Wanneer hetzelfde product in meer dan één campagne is opgenomen, gebruikt het advertentienetwerk eerst de campagneprioriteit om te bepalen welke campagne (en het bijbehorende bod) in aanmerking komt voor de advertentieveiling. Wanneer alle campagnes dezelfde prioriteit hebben, is de campagne met het hoogste bod subsidiabel.

Voor meer informatie over [!DNL Google] het winkelen campagnes en advertenties, zie &quot;[ voeren  [!DNL Google Ads]  het winkelen campagnes ](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)&quot;en [ Google Advertentie documentatie ](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1) uit. Voor meer informatie over [!DNL Microsoft] het winkelen campagnes, zie [  [!DNL Microsoft Advertising]  het winkelen campagnes ](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)&quot;en de [[!DNL Microsoft Advertising]  documentatie ](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500) uitvoeren.

>[!NOTE]
>
>Ondersteuning is niet beschikbaar voor [!DNL Google Ads] -aanbiedingsgroepen in maximale prestatiecampagnes, die slimme winkelcampagnes vervangen. Met de [!DNL Google Ads] editor kunt u gegevens voor lijstgroepen beheren en weergeven.

## Hiërarchie van productgroepen

Alvorens u productgroepen met specifieke attributen voor een advertentiegroep kunt tot stand brengen, moet u eerst een alle-inclusieve productgroep creëren genoemd &quot;[!UICONTROL All Products]&quot;. Vanuit deze bovenliggende productgroep kunt u onderliggende productgroepen maken voor subsets van producten en kleinkinderen maken van de onderliggende productgroepen. Nadat u de eerste onderliggende productgroep voor een advertentiegroep hebt gemaakt, wordt automatisch een andere productgroep met de naam &quot;[!UICONTROL Everything Else]&quot; gemaakt met het standaard advertentiebod. Aangezien u meer productgroepen toevoegt, wordt de &quot;[!UICONTROL Everything Else]&quot;groep dienovereenkomstig aangepast zodat het alle producten vormt die niet in een andere productgroep zijn.

Binnen een advertentiegroep kunt u tot zeven niveaus van productgroepen (exclusief &quot;[!UICONTROL All Products]&quot;) tot stand brengen om of van het bieden uit te sluiten, met één of meerdere productgroepen gericht op het zelfde attribuut in elk niveau (bijvoorbeeld, [!UICONTROL Brand]=Acme voor één productgroep en [!UICONTROL Brand]=AcmePlus voor een andere op het zelfde niveau). Bovenliggende productgroepen worden onderverdelingen genoemd en het laagste niveau van onderverdelingen wordt eenheid genoemd. Je kunt biedingen en trackingsjablonen instellen of biedingen volledig uitsluiten op het niveau van de eenheid. De volledige reeks actieve productgroepen voor een advertentiegroep wordt hiërarchisch toegepast om de in aanmerking komende producten te bepalen. Als u bijvoorbeeld [!UICONTROL All Products] onderverdeelt in [!UICONTROL Brand]=AcmeBasic en [!UICONTROL Brand]=AcmePlus, en vervolgens elk van deze productgroepen onderverdeelt in [!UICONTROL Condition]=New en biedingen instelt, kunnen alleen nieuwe producten met de merken AcmeBasic en AcmePlus worden geadverteerd of van advertenties worden uitgesloten.

![ Voorbeeld van een reeks van de productgroep ](/help/search-social-commerce/assets/product-group-list.png " Voorbeeld van een reeks van de productgroep ")

![ de hiërarchie van de productgroep van het Voorbeeld ](/help/search-social-commerce/assets/product-group-tree.png " de hiërarchie van de productgroep van het Voorbeeld ")

## De weergave [!UICONTROL Product Groups]

U kunt productgroepen en onderliggende productgroepen maken en bewerken en deze verwijderen in de weergave [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] .

## Traceergegevens en prestatiegegevens voor winkelproductgroepen

(Rekeningen/campagnes met de &quot;[!UICONTROL EF Redirect]&quot;het volgen optie) om Onderzoek, Sociaal toe te staan, &amp; Commerce om omzettingen voor productgroepen te volgen, [ het volgen URLs voor productgroepen produceren gebruikend het Volgen URLs hulpmiddel ](/help/search-social-commerce/tools/click-tracking-url-generate.md), en dan één van het volgende te doen:

* (Vereist voor [!DNL Google Ads]; aanbevolen procedure voor [!DNL Microsoft Advertising] ) Voeg de URL voor bijhouden toe aan het veld [!DNL Tracking Template] in de instelling voor account, campagne of productgroep. Voeg deze op het hoogst mogelijke niveau toe om het onderhoud te vereenvoudigen. Om het even welke toevoegingsparameters die voor de rekening of de campagne worden gespecificeerd zijn niet inbegrepen.

  >[!CAUTION]
  >
  >([!DNL Microsoft Advertising]) Gebruik deze optie slechts wanneer u Onderzoek, Sociale, &amp; het volgen URLs van Commerce niet in een douanekolom binnen de productvoer omvat. Als u beide doet, bevatten de URL&#39;s twee omleidingen en worden koppelingen verbroken.

* ([!DNL Microsoft Advertising] slechts) voeg het volgen URL aan de productgegevens binnen de [!DNL Microsoft Merchant Center] rekening toe. Daartoe neemt u de URL voor het bijhouden van de gegevens samen met de waarde in het veld `link` of `mobile_link` op, al naar het geval, in een aangepaste kolom met de naam [`bingads_redirect` ](https://help.ads.microsoft.com/#apex/3/en/51084/0) in de productfeed. URL&#39;s die met deze methode worden gegenereerd, bevatten geen volgparameters die zijn opgegeven in de account- of campagne-instellingen in Zoeken, Sociaal en Commerce.

U kunt gegevens over productgroepen bekijken in [ [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [ beheer het winkelen productgroepen ](product-group-manage.md)
>* [[!DNL Google Ads]  de montages van de productgroep ](product-group-settings-google.md)
>* [ voert  [!DNL Google Ads]  het winkelen campagnes ](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md) uit
>* [[!DNL Microsoft Advertising]  de montages van de productgroep ](product-group-settings-microsoft.md)
>* [ voert  [!DNL Microsoft Advertising]  het winkelen campagnes ](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md) uit
