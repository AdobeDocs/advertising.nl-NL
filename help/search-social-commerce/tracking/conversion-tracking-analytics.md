---
title: Adobe Analytics-conversie bijhouden
description: Meer informatie over het bijhouden van Adobe Analytics-conversies voor je campagnes in Adobe Advertising.
exl-id: c72cc988-5b51-4e1a-8cb6-6c3ca2a0226b
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# Adobe Analytics-conversie bijhouden

*Adverteerders die alleen Adobe Advertising-Adobe Analytics-integratie hebben*

Voor adverteerders met een Adobe Advertising-Adobe Analytics-integratie kan Advertising Cloud uw advertenties en indrukkingen verbinden met de betrokkenheids- en conversiemetriek van de site die worden bijgehouden door [!DNL Analytics] wanneer u een omleiding gebruikt met een token (`ef_id` parameter) in uw klik-volgende URLs voor uw klik [biedingseenheden](/help/search-social-commerce/glossary.md#a-b). De [!DNL Analytics] gegevens worden automatisch naar Advertising Cloud verzonden via een dagelijks feed-bestand.

Zie &quot;[Overzicht van [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud/dsp/integrations/analytics/overview.html){target="_blank"}&quot; voor meer informatie over de integratie .

>[!PREREQUISITES]
>
> Tijdzones in het advertentieaccount van Search, Social &amp; Commerce, de [!DNL Analytics] rapporteer suites, en de rekeningen van het advertentienetwerk moeten aanpassen. Als zij niet aanpassen, komen de gegevensvariaties over de systemen voor.

## Overzicht van implementatie

1. In [!DNL Analytics]En uw implementatieteam voor Zoeken, Sociaal zoeken en Commerce wijzigt de volgende configuratie-instellingen voor elke rapportsuite:

   * De vervaldatum voor de `ef_id` [!DNL eVar] wordt gewijzigd zodat deze overeenkomt met het venster voor terugzoeken van adverteerders voor Adobe Advertising.

   * De gebruikers-id van de Adobe Advertising.

   * Standaard- en aangepaste gebeurtenissen die moeten worden gebruikt voor optimalisatie.

1. In Search, Social &amp; Commerce, uw implementatieteam:

   1. Synchroniseert de bestaande hiërarchie van de advertentienetwerkrekeningen in Onderzoek, Sociale, &amp; Commerce.

   1. Hiermee voegt u omleidingen toe met &quot;`ef_id`&quot;-token dat wordt doorgegeven aan URL&#39;s die de URL bijhouden en dat wordt gepost naar het advertentienetwerk.

   Deze stap gaat een omleiding aan de Adobe Advertising volgende server (behalve voor [!DNL Google Ads] en [!DNL Microsoft Advertising] advertenties in browsers die parallelle tracering ondersteunen) en voegt een dynamisch gevulde &quot;ef_id&quot;-parameter toe aan de URL op het moment van de advertentie-klik. Wanneer parallelle tracering van toepassing is, worden eindgebruikers rechtstreeks van uw advertentie naar de uiteindelijke URL verzonden en wordt de URL van uw volgsjabloon (met klikmeting) op de achtergrond geladen.

Zodra de integratie is voltooid, ontvangen Search, Social &amp; Commerce automatisch alle gebeurtenisgegevens op de pagina die worden bijgehouden in [!DNL Analytics] voor de rapportsuites die werden gevormd.

>[!MORELIKETHIS]
>
>* [Opties voor bijhouden van conversie](conversion-tracking-about.md)
