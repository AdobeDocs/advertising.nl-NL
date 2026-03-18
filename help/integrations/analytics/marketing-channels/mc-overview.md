---
title: Grondbeginselen van  [!DNL Marketing Channels]
description: Leer zeer belangrijke informatie over  [!DNL Analytics Marketing Channels]  dat  [!DNL Analytics for Advertising]  de gebruikers zouden moeten begrijpen.
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: 0b95d99a1370a047642f8d1e4bbafe35ad5187f6
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# Grondbeginselen van [!DNL Analytics Marketing Channels]

Deze pagina bevat belangrijke informatie over [!DNL Analytics Marketing Channels] die [!DNL Analytics for Advertising] -gebruikers moeten begrijpen.

Voor volledige documentatie op [!DNL Marketing Channels], zie &quot;[ Begonnen met  [!DNL Marketing Channels] ](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html).&quot;

## Overzicht van [!DNL Marketing Channels]

[!DNL Marketing Channels] zijn een belangrijke functie van Adobe Analytics. In [!DNL Marketing Channels] worden rapporten weergegeven waarin wordt aangegeven hoe klanten via het rapportagevenster naar uw website komen en hoe elk kanaal invloed heeft op de inkomsten of het gedrag op de locatie.

Neem bijvoorbeeld het volgende voorbeeld van een reis tijdens een kruisbezoek. Elk bezoek aan uw website wordt aangegeven door het marketingkanaal van waaruit de bezoeker is gekomen. Het eerste bezoek, ook wel First Touch Channel genoemd, is E-mail. Weergeven bij bezoek twee is een deelnemend kanaal en Natuurlijk zoeken wordt beschouwd als het laatste aanraakkanaal. Als u [!UICONTROL Last Touch Attribution] gebruikt binnen [!UICONTROL Attribution IQ] , ontvangt Natural Search volledige creditering voor de conversiegebeurtenis $250. Met de Experience Cloud ID Service kunt u deze individuele bezoeken aan elkaar koppelen om één reis door één enkele bezoeker te onthullen.

![ de reis van de het dwars-bezoek van het voorbeeld in de Kanalen van de Marketing ](/help/integrations/assets/a4adc-mc-sample-journey.png)

Door [!UICONTROL Marketing Channels] Regels van de Verwerking te gebruiken, kunt u reeksen logica tot stand brengen om de kanalen te bepalen die verkeer drijven en elk kanaal te volgen aangezien de gebruikers naar uw plaats komen. Het [!UICONTROL Email] -kanaal wordt bijvoorbeeld aangegeven met een unieke trackingcode die wordt gegenereerd wanneer u op dit kanaal klikt. Als u het kanaal door Adobe Analytics hebt geregistreerd, wordt het bezoek gecategoriseerd als afkomstig van een marketingcampagne voor e-mail.

## De regels van de verwerking en hoe de Kanalen van de Marketing worden geplaatst

Elke keer dat een gebruiker naar een website komt, doet hij dat via een URL waarop hij of zij heeft geklikt of die hij of zij rechtstreeks in de adresbalk heeft getypt. Wanneer de gebruiker de website betreedt, houdt [!DNL Analytics] informatie bij die kan worden gebruikt om het kanaal te bepalen dat het bezoek leidde.

Vaak voegen marketers code voor het bijhouden van querytekenreeksparameters toe aan kanaal-URL&#39;s om het effect van het kanaal op hun site te volgen. U kunt [!DNL Marketing Channels] verwerkingsregels zodanig configureren dat wordt geluisterd naar specifieke trackingparameters en -waarden om het kanaal te bepalen zonder dat er meer tekstspatiëring nodig is. Als bijvoorbeeld alle URL&#39;s van e-mailcampagnes de indeling `www.adobe.com?cid=email…` volgen (waar de URL de parameter en waarde van de queryreeks bevat `cid=email` ), kunt u een regel maken om naar deze trackingcode te luisteren en het bezoek in het [!UICONTROL Email] -kanaal te stoppen.

Andere kanalen hebben geen trackable wegen URL en hebben verdere logica voor identificatie nodig. [!UICONTROL Earned Social] , waarin een gebruiker bijvoorbeeld op een koppeling klikt die een andere gebruiker organisch op een sociaal netwerk heeft gedeeld, is een belangrijk kanaal om te volgen. Nochtans, heeft de teller geen manier om een parameter het volgen code van het vraagkoord aan URL toe te voegen die wordt gedeeld. In dit geval kunt u een verwerkingsregel maken om te luisteren naar het verwijzende domein van sociale netwerken van interesse en naar het ontbreken van betaalcodes om het kanaal te bepalen. De bezoeken die aan deze vereisten voldoen zouden dan als Verdiende Sociale binnen het rapport van de Kanalen van de Marketing worden gevolgd.

Adobe raadt u aan samen te werken met uw analyseteam om een uitgebreide set [!DNL Marketing Channels] -verwerkingsregels op te stellen om alle kanalen te volgen die relevant zijn voor uw bedrijf. Zo kunt u krachtige rapportage van toewijzingen maken.

Om te begrijpen hoe Adobe Advertising aan de signalen kan bijdragen noodzakelijk om douanegeleidende kanalen tot stand te brengen, zie &quot;[ Gebruikend Advertising IDs om  [!DNL Marketing Channels]  Regels ](mc-ids.md) tot stand te brengen.&quot;

>[!MORELIKETHIS]
>
>* [ Gebruikend Adobe Advertising IDs om  [!DNL Marketing Channels]  verwerkingsregels ](mc-ids.md) te creëren
>* [ waarom de kanaalgegevens tussen Adobe Advertising en  [!DNL Marketing Channels]](mc-data-variances.md) kunnen variëren
>* [ Gebruikend  [!DNL Analytics Marketing Channels]  met de gegevens van Adobe Advertising ](mc-ac-data.md)
>* [ Video: Gebruikend  [!DNL Marketing Channels]  voor Adobe Advertising die ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html) meldt
>* [ Overzicht van  [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
