---
title: Overzicht van het verzenden van DSP-media-belichtingsgegevens naar Adobe Audience Manager
description: Leer hoe u Audience Manager-gebeurtenispixels kunt gebruiken voor het vastleggen van gegevens op beeldniveau en het klikken op niveau in Advertising DSP-campagnes
feature: Integration with Adobe Audience Manager
exl-id: c299cdf0-a83e-4026-8b8b-22ce08af0cc4
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Overzicht van het verzenden van DSP-media-belichtingsgegevens naar Adobe Audience Manager

*Advertisers met slechts Advertising DSP*

*Advertisers met slechts een integratie Adobe Advertising-Adobe Audience Manager*

Advertising DSP-klanten met Adobe Audience Manager kunnen Audience Manager-gebeurtenispixels gebruiken om gegevens op beeldniveau vast te leggen en om gegevens op klikniveau van DSP-campagnes vast te leggen. De gebeurtenispixels verzenden de gegevens als activeerbare signalen naar Audience Manager. Deze signalen maken verschillende DSP-gebruiksgevallen mogelijk, zoals geavanceerdere segmentering, frequentiebeheer, marketinganalyses en rapportageinzichten.

DSP vraagt je niet om deze signalen naar Audience Manager te sturen. U betaalt echter standaard Audience Manager-innamekosten op basis van serveroproepen, volgens uw Audience Manager-contract. Audience Manager verwijdert dubbele gebeurtenissen die op twee verschillende manieren worden bijgehouden, zodat elke gebeurtenis slechts eenmaal wordt geladen.

>[!NOTE]
>
> Audience Manager biedt ook ondersteuning voor het vastleggen van gegevens uit logbestanden van advertenties, wat minder flexibiliteit biedt. Dat proces wordt niet behandeld in deze documentatie.

## Primaire voordelen

* De campagnegegevens van DSP stromen in Audience Manager in echt - tijd, en u kunt het gebruiken om op regel-gebaseerde eigenschappen te bouwen die u gebruikt om segmenten te bepalen.

* De segmenten zijn beschikbaar voor het richten onmiddellijk na gebruikerseigenschap en segmentkwalificatie, die in real time het richten inspanningen verstevigen.

* U kunt de campagnegegevens voor dergelijke gebruiksgevallen gebruiken, zoals het aftappen van de frequentie over creatieve personen, het herrichten van gebruikers die aan vorige campagnes werden blootgesteld, en het analyseren van stroomafwaarts plaatsgedrag en ingangspunten.

* De bijeengevoegde gegevens verstrekken een verenigde mening van campagneprestaties, hulp identificeert de wegen van de douaneomzetting, en kunnen worden gebruikt om de opeenvolging van gebeurtenissen te verbeteren die tot omzettingen door Audience Manager [!DNL Audience Optimization Reports] of door een [[!DNL Audience Analytics]  integratie met Adobe Analytics &#x200B;](/help/integrations/audience-manager/audience-analytics.md) leiden.

## Hoe de gegevens worden bijgehouden

De Audience Manager-indruk en klik op gebeurtenispixels zijn gebaseerd op cookies. De pixel vangen geen gebeurtenissen vast die in milieu&#39;s zonder koekjes, zoals mobiele apps en aangesloten TV (CTV) voorkomen.<!-- 6/24: CTV inventory isn't clickable, and impression tracking would be lost when we convert users from IP to cookies. -->

### Pixels voor het bijhouden van indrukken

Audience Manager houdt de gegevens bij van de indruk van een advertentie wanneer u een pixel van 1 pixel transparante gebeurtenis aan de advertentie vastmaakt. De gebeurtenispixel wordt geladen telkens wanneer de advertentie aan een gebruiker wordt gediend en door Webbrowser wordt geladen. De pixel wordt geladen van een cliënt-specifiek subdomain van [`demdex.net` &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), dat een erfenisdomein voor Audience Manager is, en parameters als zeer belangrijk-waardeparen bevat. Met de gebeurtenisaanroep worden indruk- en conversiegegevens verzameld en naar de Audience Manager-servers voor gegevensverzameling verzonden.

### Klikken en pixels bijhouden

Audience Manager houdt kliks op dezelfde manier als indrukken, behalve dat het niet de transparante gebeurtenispixel laadt telkens als de advertentie wordt gediend. In plaats daarvan worden de klikgegevens bijgehouden in de doorklikURL van de advertentie. De advertentie wijst naar een cliënt-specifiek subdomain van [`demdex.net` &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), dat een erfenisdomein voor Audience Manager, voor verwerking door de servers van de de gegevensinzameling van Audience Manager is. De server leidt de gebruiker vervolgens om naar de bedoelde bestemmingspagina. De URL bevat parameters als sleutel-waardeparen.

>[!NOTE]
>
>Als uw organisatie [!DNL Analytics] tracking gebruikt, is het mogelijk dat u geen Audience Manager-functie voor bijhouden van klikken nodig hebt. Adobe Analytics vangt signalen vast en kan hen naar Audience Manager door [&#x200B; server-kant door:sturen &#x200B;](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html) verzenden.

>[!MORELIKETHIS]
>
>* [&#x200B; verzamel klik en indruk gegevens van de campagnes van Advertising DSP &#x200B;](collect.md)
>* [&#x200B; Gevallen van het Gebruik &#x200B;](use-cases.md)
