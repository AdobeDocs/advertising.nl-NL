---
title: Grondbeginselen van [!DNL Marketing Channels]
description: Belangrijke informatie over [!DNL Analytics Marketing Channels] dat [!DNL Analytics for Advertising] gebruikers moeten dit begrijpen.
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: 29b49e8fa54580d7cdd62f9a10fd2616def4694b
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# Grondbeginselen van [!DNL Analytics Marketing Channels]

Deze pagina bevat belangrijke informatie over [!DNL Analytics Marketing Channels] dat [!DNL Analytics for Advertising] gebruikers moeten dit begrijpen .

Voor volledige documentatie over [!DNL Marketing Channels], zie &quot;[Aan de slag met [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html?lang=nl-NL).&quot;

## Overzicht van [!DNL Marketing Channels]

[!DNL Marketing Channels] zijn een belangrijke functie van Adobe Analytics. [!DNL Marketing Channels] In rapporten ziet u hoe klanten via het rapportagevenster naar uw website komen en hoe elk kanaal invloed heeft op de inkomsten of het gedrag op de locatie.

Neem bijvoorbeeld het volgende voorbeeld van een reis tijdens een kruisbezoek. Elk bezoek aan uw website wordt aangegeven door het marketingkanaal van waaruit de bezoeker is gekomen. Het eerste bezoek, ook wel First Touch Channel genoemd, is E-mail. Weergeven bij bezoek twee is een deelnemend kanaal en Natuurlijk zoeken wordt beschouwd als het laatste aanraakkanaal. Als u [!UICONTROL Last Touch Attribution] binnen [!UICONTROL Attribution IQ]Natuurlijk zoeken zou volledige krediet ontvangen voor de conversiegebeurtenis $250. Met de Experience Cloud-id-service kunt u deze afzonderlijke bezoeken aan elkaar koppelen om één reis van één bezoeker te onthullen.

![Voorbeeld van een reis naar conversie tussen bezoeken in marketingkanalen](/help/integrations/assets/a4adc-mc-sample-journey.png)

Met [!UICONTROL Marketing Channels] Bij de verwerking van Regels kunt u logische sets maken om te bepalen welke kanalen het verkeer sturen en om elk kanaal bij te houden wanneer gebruikers naar uw site komen. Bijvoorbeeld de [!UICONTROL Email] het kanaal zou worden aangegeven met een unieke code voor het bijhouden van de gegevens die wordt gegenereerd wanneer Adobe Analytics een aanmelding indient en die het bezoek zou aanmerken als afkomstig van een e-mailmarketingcampagne.

## De Regels van de verwerking en hoe de Kanalen van de Marketing worden geplaatst

Elke keer dat een gebruiker naar een website komt, doet hij dat via een URL waarop hij of zij heeft geklikt of die hij of zij rechtstreeks in de adresbalk heeft getypt. Wanneer de gebruiker de website betreedt, [!DNL Analytics] volgt informatie die kan worden gebruikt om het kanaal te bepalen dat het bezoek leidde.

Vaak voegen marketers code voor het bijhouden van querytekenreeksparameters toe aan kanaal-URL&#39;s om het effect van het kanaal op hun site te volgen. U kunt [!DNL Marketing Channels] verwerkingsregels om te luisteren naar specifieke volgende parameters en waarden om het kanaal te bepalen zonder extra tracking. Als bijvoorbeeld alle URL&#39;s van de e-mailcampagne de indeling volgen `www.adobe.com?cid=email…` (wanneer de URL de parameter en waarde van de querytekenreeks bevat `cid=email`), dan kunt u een regel tot stand brengen om naar deze volgende code te luisteren en het bezoek in te sluiten [!UICONTROL Email] kanaal.

Andere kanalen hebben geen trackable wegen URL en hebben verdere logica voor identificatie nodig. Bijvoorbeeld: [!UICONTROL Earned Social], waarin een gebruiker op een koppeling klikt die een andere gebruiker organisch op een sociaal netwerk heeft gedeeld, is een belangrijk kanaal om te volgen. Nochtans, heeft de teller geen manier om een parameter het volgen code van het vraagkoord aan URL toe te voegen die wordt gedeeld. In dit geval kunt u een verwerkingsregel maken om te luisteren naar het verwijzende domein van sociale netwerken van interesse en naar het ontbreken van betaalcodes om het kanaal te bepalen. De bezoeken die aan deze vereisten voldoen zouden dan als Verdiende Sociale binnen het rapport van de Kanalen van de Marketing worden gevolgd.

Adobe raadt u aan samen te werken met uw analyseteam om een uitgebreide set [!DNL Marketing Channels] verwerkingsregels om alle kanalen te volgen die voor uw zaken relevant zijn. Zo kunt u krachtige rapportage van toewijzingen maken.

Als u wilt begrijpen hoe Adobe Advertising kan bijdragen aan de signalen die nodig zijn om aangepaste marketingkanalen te maken, raadpleegt u &quot;[Adverteren-id&#39;s gebruiken om te maken [!DNL Marketing Channels] Regels](mc-ids.md).&quot;

>[!MORELIKETHIS]
>
>* [Adobe Advertising-id&#39;s gebruiken om te maken [!DNL Marketing Channels] Verwerkingsregels](mc-ids.md)
>* [Waarom kanaalgegevens kunnen variëren tussen Adobe Advertising en [!DNL Marketing Channels]](mc-data-variances.md)
>* [Gebruiken [!DNL Analytics Marketing Channels] met Adobe Advertising-gegevens](mc-ac-data.md)
>* [Video: gebruiken [!DNL Marketing Channels] voor rapportage van Adoben Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=nl-NL)
>* [Overzicht van [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
