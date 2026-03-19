---
title: Gebruikend  [!DNL Marketing Channels]  met de gegevens van Adobe Advertising
description: Leer hoe te om de gegevens van Adobe Advertising in  [!DNL Analytics Marketing Channels] te gebruiken.
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
source-git-commit: 4db751aae61eaf8abdc5e3afca3b4027f0eddf26
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# [!DNL Analytics Marketing Channels] gebruiken met Adobe Advertising-gegevens

*Advertisers met slechts een integratie Adobe Advertising-Adobe Analytics*

Door Adobe Advertising- en [!DNL Analytics Marketing Channels] -rapporten te gebruiken, kunt u waardevolle insight winnen voor de manier waarop uw digitale media van invloed is op de activiteit van de site.

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

In het volgende voorbeeld wordt getoond hoe Adobe Advertising en [!DNL Marketing Channels] de individuele bezoeken volgen die de reis van één bezoeker omvatten. Adobe Advertising-rapporten in [!DNL Analytics] zijn beperkt tot alleen betaalde reclame voor displays, zoekopdrachten, sociale media en handelskanalen die via Adobe Advertising worden verhandeld, met behulp van de AMO-id. [!DNL Marketing Channels] houdt echter alle kanalen bij die in de [!DNL Marketing Channels] -verwerkingsregels zijn geconfigureerd.

![&#x200B; hoe Adobe Advertising en [!DNL Marketing Channels] de individuele bezoeken in de reis van een bezoeker &#x200B;](/help/integrations/assets/a4adc-mc-sample-journey2.png) volgen

Tijdens het eerste bezoek heeft de gebruiker de website ingevoerd via een e-mailcampagne, tien paginaweergaven uitgevoerd en vervolgens vertrokken. Tijdens het tweede bezoek heeft de gebruiker de site ingevoerd via een advertentie, tien paginaweergaven uitgevoerd en vervolgens links. Tijdens het derde bezoek heeft de gebruiker de site betreden via een natuurlijke zoekopdracht, vijf paginaweergaven uitgevoerd, een conversie van € 250 uitgevoerd en links. Let op het verschil in reeksspatiëring tussen [!DNL Marketing Channels] en Adobe Advertising. Het enige kanaal dat Adobe Advertising in deze reis volgt, is [!UICONTROL Display]. Adobe Advertising houdt het [!UICONTROL Display] -kanaalbezoek bij en wijst de daaropvolgende betrokkenheidsgegevens (zoals paginaweergaven) en conversies terug naar de invloed van die advertentie. [!DNL Marketing Channels] daarentegen geeft een volledig beeld van alle kanalen.

Omdat de AMO-id tijdens de reis van de bezoeker blijft bestaan, kunt u met de AMO-id-gegevens zien hoe Adobe Advertising andere marketingkanalen beïnvloedt. Identiteitskaart van AMO [&#x200B; persisteert 60 dagen door gebrek &#x200B;](/help/integrations/analytics/overview.md), maar u kunt persistentie vormen zoals nodig.

## Adobe Advertising en Marketing Channel-gegevens combineren om mediaprestaties te analyseren

Binnen [!DNL Analytics] kunt u de Adobe Advertising-gegevens voor blijvend betaalde advertenties combineren met de [!DNL Marketing Channels] -gegevens voor uitgebreide bezoeken om de mediaprestaties beter te analyseren, zodat u de reis van de klant beter kunt beïnvloeden.

In de volgende analyse worden de Adobe Advertising-gegevens gebruikt om verschillende versies weer te geven van de invloed van een weergaveadvertentie op siteconversie. Alle drie de kolommen gebruiken de zelfde omzettingsmetriek, maar elke kolom vertelt een verschillend verhaal:

* In kolom 1 worden de AMO-id-gegevens weergegeven die blijvend zijn over de reis van de bezoeker. Kolom 1 geeft aan dat 641 toepassingen op één punt zijn gekoppeld aan een Adobe Advertising-advertentie, via een doorkijkgebeurtenis of via een doorklikgebeurtenis. In deze weergave wordt geen rekening gehouden met een andere [!DNL Marketing Channels] -toewijzing.

* In de gegevensset van [!DNL Marketing Channels] worden de 641 toepassingen Start echter toegewezen aan andere marketingkanalen. In de laatste twee kolommen worden de 641 toepassingen gestart en worden de gegevens beperkt tot de kanalen [!UICONTROL Display Click-Through] en [!UICONTROL Display View-Through] . Hierin worden de omzettingen weergegeven die zich voordoen in een laatste aanraakattributiemodel.

![&#x200B; voorbeeld van hoe een vertoning en plaatsomzetting beïnvloedt &#x200B;](/help/integrations/assets/a4adc-mc-display-impact.png)

U kunt deze analyse een stap verder zetten. U kunt de rij van Adobe Advertising verder door marketing kanaal verdelen om te zien waar de omzettingen van Adobe Advertising aan de 641 Beginnen van Toepassingen worden toegewezen. U weet al dat vijf van deze omzettingen worden toegeschreven aan een laatste aanraakscherm en dat er 19 worden toegewezen aan een laatste aanraakscherm. Hierdoor blijven 617 toepassingen aan andere marketingkanalen toegewezen. U kunt de afmeting Laatste aanraakkanaal boven op het Advertising DSP-regelitem slepen en neerzetten om de kanaaltoewijzing voor de rest van de toepassingen zichtbaar te maken en de kanaalinvloed van het weergavekanaal te tonen.

![&#x200B; hoe te om de Laatste dimensie van het Kanaal van de Aanraak toe te voegen &#x200B;](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Nu kunt u zien hoe de resterende Toepassingen worden toegewezen. E-mail krijgt krediet voor 357 meest recente aanraaktoepassingen Start waarvoor een AMO-id werd gebruikt. Met dit type analyse kunt u zien wat de impact was van advertenties in Adobe Advertising op alle kanalen. Met slechts één gegevensset en attributiemodel zou dit type insight niet beschikbaar zijn.

![&#x200B; voorbeeld van het kanaaleffect van de kanalen van de Vertoning &#x200B;](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

U kunt de analyse verder verbeteren door een Stapelgrafiek te gebruiken die aan &quot;100% wordt geplaatst gestapeld&quot;om trended gegevens in tijd te tonen. Dankzij deze visualisatie kunt u gemakkelijker controleren welke laatste aanraakmarketingkanalen zwaarder worden beïnvloed door uw marketingcampagnes voor beeldschermen.

![&#x200B; voorbeeld van het trended kanaaleffect van de kanalen van de Vertoning &#x200B;](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [&#x200B; Grondbeginselen van  [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [&#x200B; Gebruikend Adobe Advertising IDs om  [!DNL Marketing Channels]  verwerkingsregels &#x200B;](mc-ids.md) te creëren
>* [&#x200B; waarom de kanaalgegevens tussen Adobe Advertising en  [!DNL Marketing Channels]](mc-data-variances.md) kunnen variëren
>* [&#x200B; Video: Gebruikend  [!DNL Marketing Channels]  voor Adobe Advertising die &#x200B;](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=nl-NL) meldt
>* [&#x200B; Overzicht van  [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
