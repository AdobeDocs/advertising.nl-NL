---
title: Een URL voor het bijhouden van klikken genereren
description: Leer hoe u handmatig een URL voor het bijhouden van klikken in Zoeken, Sociaal en Commerce genereert.
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Een URL voor het bijhouden van klikken via Zoeken in sociale en Commerce genereren met het gereedschap URL&#39;s bijhouden

*Adverteerders die alleen de conversie van Adoben Advertising bijhouden*

Voor informatie over wanneer u een klik-volgende URL manueel moet produceren en uitvoeren, zie &quot;[Wanneer en hoe te om klik-volgende URLs te produceren](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

>[!NOTE]
>
>Met deze functie wordt de URL voor het bijhouden van de sjabloon of de bestemming niet geïmplementeerd in het desbetreffende advertentiaccount.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**.

1. Selecteer de netwerkaccount voor advertenties in de lijst.

   ([!DNL Google Ads] Trefwoorden; tekst, installatie van mobiele apps en dynamische zoekopdrachten; plaatsaanduidingen, sitelinks en productgroepen) Tags voor het trackingsjabloonveld worden weergegeven. Zij omvatten geen rekening-vlakke toevoegingsparameters. Ga verder met stap 4.

   Voor alle andere typen tags voert u de invoergegevens in om een tag te genereren.

1. (Indien nodig) Genereer een tag:

   1. Geef de bestemmingspagina&#39;s, met sitelinks of productnamen op verzoek, op een van de volgende manieren op:

      * Geef een bestand op dat de informatie bevat door het volledige pad en de volledige bestandsnaam in te voeren of door op **[!UICONTROL Browse]** om het bestand op uw apparaat of netwerk te zoeken. Het bestand moet een door tabs gescheiden tekstbestand zijn met één item per regel in de volgende indeling:

         * (Creatieve producten, standaardadvertenties) `**landing_page**`

           waar `landing_page` is een geldige bestemmingspagina URL of basis URL.

           Voorbeeld: http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] sitelinks) `sitelink <tab> ** <tab> landing_page`

           waar `sitelink` de naam van de sitelink is en `landing_page` is een geldige bestemmingspagina URL of basis URL.

           Voorbeeld: `Careers <tab> ** <tab> http://www.example.com/careers.html`

           Het bestand kan maximaal 10.000 regels bevatten.

         * ([!DNL Google Merchant Center] productgroepen en [!DNL Microsoft Advertising] productadvertenties) `product name <tab> ** <tab> landing_page`

           waar `product name` is de productnaam en `landing_page` is een geldige bestemmingspagina URL of basis URL.

           Voorbeeld: `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           Het bestand kan maximaal 10.000 regels bevatten.

      * Voer in het invoerveld één item per regel in de volgende notatie in:

         * (Creatieve producten, standaardadvertenties) `landing_page`

           waar `landing_page` is een geldige bestemmingspagina URL of basis URL.

           Voorbeeld: http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] sitelinks) `sitelink**landing_page`

           waar `sitelink` de naam van de sitelink is en `landing_page` is een geldige bestemmingspagina URL of basis URL.

           Voorbeeld: `Careers**http://www.example.com/careers.html`

         * ([!DNL Google Merchant Center] productgroepen en [!DNL Microsoft Advertising] productadvertenties) `product name**landing_page`

           waar `product name` is de productnaam en `landing_page` is een geldige bestemmingspagina URL of basis URL.

           Voorbeeld: Acme PR208**http://www.example.com/travel.html

   1. Klik op **[!UICONTROL Generate Tracking URLs]**.

1. (Optioneel) Kopieer de URL&#39;s (te beginnen met &quot;http&quot; of &quot;https&quot;) van het scherm of de uitvoerpagina en implementeer deze in de zoekfunctie of de sociale account.

Voer voor accounts met doel-URL&#39;s de waarden in het juiste [!UICONTROL Base URL] velden.

Voer voor accounts met uiteindelijke URL&#39;s de waarde op het scherm in het juiste [!UICONTROL Tracking Template] veld. U moet een parameter voor de laatste URL toevoegen na de instelling `&url=` parameter (zoals `{lpurl}`). Voor [!DNL Yahoo! Japan Ads] accounts, gebruik de parameter `{lpurl}`. Voor een lijst met [!DNL Google Ads] en [!DNL Microsoft Advertising] parameters die de uiteindelijke URL&#39;s aangeven in trackingsjablonen, raadpleegt u de [[!DNL Google Ads] documentatie](https://support.google.com/google-ads/answer/6305348) (Zie de parameters &quot;Volgsjabloon alleen&quot; in het gedeelte over &quot;Beschikbaar&quot; [!DNL ValueTrack] Parameters&quot;) en de [[!DNL Microsoft Advertising] documentatie](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [Over de gereedschappen voor het maken en decoderen van trackingcodes](tracking-tools-about.md)
>* [Wanneer en hoe te om klik-volgende URLs te produceren](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [Een URL voor het bijhouden van klikken in een zoekopdracht, sociaal profiel en Commerce decoderen](click-tracking-url-decode.md)
