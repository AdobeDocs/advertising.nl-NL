---
title: Adobe Analytics-conversie bijhouden
description: Meer informatie over het bijhouden van Adobe Analytics-conversies voor je campagnes in Adobe Advertising.
exl-id: 0ed1d059-829a-4090-950d-41cbcc27b3ac
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Adobe Analytics-conversie bijhouden

*Adverteerders die alleen Adobe Advertising-Adobe Analytics-integratie hebben*

Voor adverteerders met een Adobe Advertising-Adobe Analytics-integratie kan Advertising Cloud uw advertenties en indrukkingen verbinden met de betrokkenheids- en conversiemetriek van de site die worden bijgehouden door [!DNL Analytics] wanneer u een omleiding gebruikt met een token (`ef_id` parameter) in uw klik-volgende URLs voor uw klik [biedingseenheden](/help/search-social-commerce/glossary.md#a-b). De [!DNL Analytics] gegevens worden automatisch naar Advertising Cloud verzonden via een dagelijks feed-bestand.

Zie &quot;[Overzicht van [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html){target="_blank"}&quot; voor meer informatie over de integratie .

>[!PREREQUISITES]
>
> Tijdzones in het adverteerderaccount Zoeken, Sociaal en Handel, het [!DNL Analytics] rapporteer suites, en de rekeningen van het advertentienetwerk moeten aanpassen. Als zij niet aanpassen, zullen de gegevensvariaties over systemen bestaan.

## Overzicht van implementatie

1. In [!DNL Analytics], wijzigt uw de implementatieteam van het Onderzoek, Sociale, &amp; van de Handel de volgende configuratiemontages voor elke rapportreeks:

   * De vervaldatum voor de `ef_id` De eVar wordt gewijzigd zodat deze overeenkomt met het venster voor het terugzoeken van adverteerders naar de Adobe Advertising.

   * De gebruikers-id van de Adobe Advertising.

   * Standaard- en aangepaste gebeurtenissen die moeten worden gebruikt voor optimalisatie.

1. In Search, Social, &amp; Commerce, uw implementatieteam:

   1. Synchroniseert de bestaande hiërarchie van de advertentienetwerkrekeningen in Onderzoek, Sociale, &amp; Handel.

   1. Hiermee voegt u omleidingen toe met &quot;`ef_id`&quot;-token dat wordt doorgegeven aan URL&#39;s die de URL bijhouden en dat wordt gepost naar het advertentienetwerk.

   Deze stap gaat een omleiding aan de Adobe Advertising volgende server (behalve voor [!DNL Google Ads] en [!DNL Microsoft Advertising] advertenties in browsers die parallelle tracering ondersteunen) en voegt een dynamisch gevulde &quot;ef_id&quot;-parameter toe aan de URL op het moment van de advertentie-klik. Wanneer parallelle tracering van toepassing is, worden eindgebruikers rechtstreeks van uw advertentie naar de uiteindelijke URL verzonden en wordt de URL van uw volgsjabloon (met klikmeting) op de achtergrond geladen.

Zodra de integratie is voltooid, ontvangt Search, Social &amp; Commerce automatisch alle gebeurtenisgegevens op de pagina die worden bijgehouden in [!DNL Analytics] voor de rapportsuites die werden gevormd.

>[!MORELIKETHIS]
>
>* [Opties voor bijhouden van conversie](conversion-tracking-about.md)
