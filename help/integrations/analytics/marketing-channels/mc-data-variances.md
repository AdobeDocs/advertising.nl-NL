---
title: Waarom kanaalgegevens kunnen variëren tussen Adobe Advertising en  [!DNL Marketing Channels]
description: Leer waarom de kanaalgegevens die door identiteitskaart van AMO worden gevolgd van kanaalgegevens kunnen variëren die door  [!DNL Analytics Marketing Channels] worden gevolgd.
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: de2a2a097802cc4a7b5ac63bee2eb326895e70f1
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Waarom kanaalgegevens kunnen variëren tussen Adobe Advertising en [!DNL Marketing Channels]

*Advertisers met slechts een integratie Adobe Advertising-Adobe Analytics*

Een algemene vraag van gebruikers die leren over de integratie van de Adobe Advertising en [!DNL Marketing Channels] gegevenssets is: &quot;Wat veroorzaakt de variatie in gegevens tussen de AMO-id en [!DNL Marketing Channels]?&quot; Of soms: &quot;Waarom worden de gegevens gebroken? Ik heb alle metriek nodig om over de rapporten te passen.&quot; Gelukkig geven discrepanties niet aan dat de gegevens &quot;gebroken&quot; zijn, en worden discrepanties verwacht en zelfs gewenst. Laten we eens kijken waarom de integratie zo is ontworpen.

De twee gegevenssets hebben verschillende hoofdgebruikscenario&#39;s:

* [!DNL Marketing Channels]: Het belangrijkste gebruik van [!DNL Marketing Channels] is het vergelijken van gegevens over meerdere kanalen met een gemeenschappelijk attributiemodel. Analysten kunnen de [!UICONTROL Marketing Channel] -dimensie gebruiken om meer inzicht te krijgen in de manier waarop kanalen met elkaar communiceren. Deze insight kan helpen bij het nemen van beslissingen op macroniveau over hoe in elk kanaal moet worden geïnvesteerd en kan leiden tot inzichten in de interactie tussen bezoekers van elk kanaal en de website.

  De [!DNL Analytics] [!UICONTROL Marketing Channel] -dimensie is daarom geconfigureerd om alle kanalen vast te leggen en te volgen. [!DNL Marketing Channels] kan ook worden geconfigureerd om Advertising DSP-weergaven en doorklikbewerkingen vast te leggen. Dit gebeurt voor de andere marketingkanalen.

* Adobe Advertising AMO-id: de Adobe Advertising AMO-id-gegevens worden voornamelijk gebruikt voor het doorvoeren van geavanceerde [!DNL Adobe AI]-georiënteerde biedingsalgoritmen. De algoritmen maken automatisch duizenden biedingsbesluiten op microniveau die dagelijks worden genomen om de advertentie-uitgaven te maximaliseren en de doelstellingen van de [!DNL DSP] campagne of de [!DNL Search, Social, & Commerce] portefeuille te bereiken. Hoe meer conversiegegevens de algoritmen kunnen verbinden met campagnes, hoe beter de algoritmen deze biedbeslissingen kunnen nemen.

  Om deze gegevens te verzamelen, gaat de [!DNL Analytics for Advertising] integratie ruwe AMO IDs over die als klikthrough en mening-door het volgen codes in de dimensie van identiteitskaart AMO van Adobe Analytics kunnen worden vertaald — die of als douanevariabele (eVar) of een gereserveerde variabele (rVar) wordt opgeslagen. Doorklikken voor andere kanalen wordt niet ingesteld in de AMO ID-dimensie, zodat de AMO ID-dimensie de invoer van deze andere kanalen niet kan bijhouden. Het resultaat is dat de AMO-id doorloopt via [!DNL Marketing Channels] -ingangspunten.

Voor meer informatie over mogelijke gegevensvariaties tussen Adobe Advertising-Getraceerde gegevens en [!DNL Analytics] - getraceerde gegevens, zie &quot;[&#x200B; Verwachte Variaties van Gegevens tussen  [!DNL Analytics]  en Adobe Advertising &#x200B;](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [&#x200B; Verwachte Variaties van Gegevens tussen  [!DNL Analytics]  en Adobe Advertising &#x200B;](/help/integrations/analytics/data-variances.md)
>* [&#x200B; Grondbeginselen van  [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [&#x200B; Gebruikend Adobe Advertising IDs om  [!DNL Marketing Channels]  Regels van de Verwerking &#x200B;](mc-ids.md) te creëren
>* [&#x200B; Gebruikend  [!DNL Analytics Marketing Channels]  met de Gegevens van Adobe Advertising &#x200B;](mc-ac-data.md)
>* [&#x200B; Video: Gebruikend  [!DNL Marketing Channels]  voor Adobe Advertising die &#x200B;](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=nl-NL) meldt
