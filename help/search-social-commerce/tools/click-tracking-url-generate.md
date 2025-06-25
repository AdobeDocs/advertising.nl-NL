---
title: Een URL voor het bijhouden van klikken genereren
description: Leer hoe u handmatig een URL voor het bijhouden van klikken in Zoeken, Sociaal en Commerce genereert.
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Een URL voor het bijhouden van klikken via Zoeken in sociale en Commerce genereren met het gereedschap URL&#39;s bijhouden

*Advertisers met slechts het volgen van de omzetting van Adobe Advertising*

Voor informatie over wanneer u moet manueel een klik-volgende URL produceren en uitvoeren, zie &quot;[ wanneer en hoe te klik-volgende URLs ](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) produceren.&quot;

>[!NOTE]
>
>Met deze functie wordt de URL voor het bijhouden van de sjabloon of de bestemming niet geïmplementeerd in het desbetreffende advertentiaccount.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]** .

1. Selecteer de netwerkaccount voor advertenties in de lijst.

   ([!DNL Google Ads] trefwoorden; tekst, installatie van mobiele apps en dynamische zoekadvertenties; plaatsingen, sitelinks en productgroepen) Er worden trackinglabels voor het sjabloonveld voor bijhouden weergegeven. Zij omvatten geen rekening-vlakke toevoegingsparameters. Ga verder met stap 4.

   Voor alle andere typen tags voert u de invoergegevens in om een tag te genereren.

1. (Indien nodig) Genereer een tag:

   1. Geef de bestemmingspagina&#39;s, met sitelinks of productnamen op verzoek, op een van de volgende manieren op:

      * Geef een bestand op dat de informatie bevat door het volledige pad en de volledige bestandsnaam in te voeren of door op **[!UICONTROL Browse]** te klikken om het bestand op uw apparaat of netwerk te zoeken. Het bestand moet een door tabs gescheiden tekstbestand zijn met één item per regel in de volgende indeling:

         * (Creative Cloud, standaardadvertenties) `**landing_page**`

           waarbij `landing_page` een geldige bestemmingspagina-URL of basis-URL is.

           Voorbeeld: http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] sitelinks) `sitelink <tab> ** <tab> landing_page`

           waarbij `sitelink` de naam van de sitelink is en `landing_page` een geldige bestemmingspagina-URL of basis-URL is.

           Voorbeeld: `Careers <tab> ** <tab> http://www.example.com/careers.html`

           Het bestand kan maximaal 10.000 regels bevatten.

         * ([!DNL Google Merchant Center] productgroepen en [!DNL Microsoft Advertising] productadvertenties) `product name <tab> ** <tab> landing_page`

           waarbij `product name` de productnaam is en `landing_page` een geldige bestemmingspagina-URL of basis-URL is.

           Voorbeeld: `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           Het bestand kan maximaal 10.000 regels bevatten.

      * Voer in het invoerveld één item per regel in de volgende notatie in:

         * (Creative Cloud, standaardadvertenties) `landing_page`

           waarbij `landing_page` een geldige bestemmingspagina-URL of basis-URL is.

           Voorbeeld: http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] sitelinks) `sitelink**landing_page`

           waarbij `sitelink` de naam van de sitelink is en `landing_page` een geldige bestemmingspagina-URL of basis-URL is.

           Voorbeeld: `Careers**http://www.example.com/careers.html`

         * ([!DNL Google Merchant Center] productgroepen en [!DNL Microsoft Advertising] productadvertenties) `product name**landing_page`

           waarbij `product name` de productnaam is en `landing_page` een geldige bestemmingspagina-URL of basis-URL is.

           Voorbeeld: Acme PR208**http://www.example.com/travel.html

   1. Klik op **[!UICONTROL Generate Tracking URLs]**.

1. (Optioneel) Kopieer de URL&#39;s (te beginnen met &quot;http&quot; of &quot;https&quot;) van het scherm of de uitvoerpagina en implementeer deze in de zoekfunctie of de sociale account.

Voor accounts met doel-URL&#39;s voert u de waarden in de desbetreffende [!UICONTROL Base URL] -velden in.

Voor accounts met uiteindelijke URL&#39;s voert u de waarde op het scherm in het desbetreffende veld [!UICONTROL Tracking Template] in. U moet een parameter voor de laatste URL toevoegen na de parameter `&url=` (zoals `{lpurl}` ). Gebruik voor [!DNL Yahoo! Japan Ads] -accounts de parameter `{lpurl}` . Voor een lijst van [!DNL Google Ads] en [!DNL Microsoft Advertising] parameters om definitieve URLs in het volgen malplaatjes te wijzen, zie de [[!DNL Google Ads]  documentatie ](https://support.google.com/google-ads/answer/6305348) (zie de &quot;het Volgen malplaatje slechts&quot;parameters in de sectie over &quot;Beschikbare [!DNL ValueTrack] Parameters&quot;) en [[!DNL Microsoft Advertising]  documentatie ](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [ Ongeveer de hulpmiddelen om het volgen markeringen tot stand te brengen en te decoderen ](tracking-tools-about.md)
>* [ wanneer en hoe te om klik-volgende URLs te produceren ](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [ decodeer een Onderzoek, Sociale, &amp; klik-volgende URL van Commerce ](click-tracking-url-decode.md)
