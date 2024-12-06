---
title: Adobe Analytics-conversie bijhouden
description: Meer informatie over het bijhouden van Adobe Analytics-conversies voor je campagnes in Adobe Advertising.
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
source-git-commit: 8deabf2c98901d706acdd035221e8c24e4a1d20d
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Adobe Analytics-conversie bijhouden

*Advertisers met slechts Adobe Advertising-Adobe Analytics integratie*

Voor adverteerders met een Adobe Advertising-Adobe Analytics integratie, kan Advertising Cloud uw advertenties en indrukkingen met de plaatsovereenkomst en omzettingsmetriek verbinden die door [!DNL Analytics] wordt gevolgd wanneer u een omleiding met teken (`ef_id` parameter) in uw klik-volgende URLs voor uw [ biedingseenheden ](/help/search-social-commerce/glossary.md#a-b) gebruikt. De [!DNL Analytics] -gegevens worden automatisch naar Advertising Cloud verzonden via een dagelijks feed-bestand.

Zie &quot;[ Overzicht van  [!DNL Analytics for Advertising] ](https://experienceleague.adobe.com/docs/advertising/dsp/integrations/analytics/overview.html) {target="_blank"}&quot;voor meer informatie over de integratie.

>[!PREREQUISITES]
>
> Tijdzones in de adverteerderaccount Zoeken, Sociaal en Commerce, de [!DNL Analytics] -rapportreeksen en de netwerkaccounts van de advertentie moeten overeenkomen. Als zij niet aanpassen, komen de gegevensvariaties over de systemen voor.

## Overzicht van implementatie

1. In [!DNL Analytics] wijzigt uw implementatieteam Search, Social en Commerce de volgende configuratie-instellingen voor elke rapportsuite:

   * De vervaldatum voor `ef_id` [!DNL eVar] wordt gewijzigd zodat deze overeenkomt met het klikvenster van de adverteerder voor Adobe Advertising.

   * De gebruikers-id van de Adobe Advertising.

   * Standaard- en aangepaste gebeurtenissen die moeten worden gebruikt voor optimalisatie.

1. In Search, Social &amp; Commerce, uw implementatieteam:

   1. Synchroniseert de bestaande hiërarchie van de advertentienetwerkrekeningen in Onderzoek, Sociale, &amp; Commerce.

   1. Voegt omleidingen met &quot;`ef_id`&quot;token toe die tot volgende URLs overgaan en hen aan het advertentienetwerk posten.

   Met deze stap wordt een omleiding naar de Adobe Advertising tracking-server (behalve voor [!DNL Google Ads] - en [!DNL Microsoft Advertising] -advertenties in browsers die parallelle tracering ondersteunen) voorbereid en wordt een dynamisch gevulde &quot;ef_id&quot;-parameter toegevoegd aan de URL op het moment van de advertentie. Wanneer parallelle tracering van toepassing is, worden eindgebruikers rechtstreeks van uw advertentie naar de uiteindelijke URL verzonden en wordt de URL van uw volgsjabloon (met klikmeting) op de achtergrond geladen.

Zodra de integratie is voltooid, ontvangen Search, Social, &amp; Commerce automatisch alle gebeurtenisgegevens op pagina die in [!DNL Analytics] voor de rapportreeksen worden gevolgd die werden gevormd.

>[!MORELIKETHIS]
>
>* [ het volgen van de Omzetting opties ](conversion-tracking-about.md)
