---
title: null
description: null
source-git-commit: f2b29c2f3a38cadc31a9b3110aa82feadd62e5cc
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Accountgegevens uploaden voor rapportage en simulaties

<!-- Move all related files into one page? -->

Als u online en netwerken gebruikt waarvoor Search, Social &amp; Commerce geen API-ondersteuning biedt, kunt u inhoud van de campagne en offline kosten uploaden, klikken en conversiegegevens voor een account voor rapportage- en prestatiesimulaties. Adverteerders met een [[!DNL Adobe Analytics for Advertising]  integratie ](/help/integrations/analytics/overview.md) kunnen gegevens voor hun rekeningen binnen Adobe Analytics ook bekijken.

Deze functie is beschikbaar voor advertentienetwerken die de standaardcampagnestructuur met drie lagen volgen (campagne, advertentiegroep of advertentieset, en biedingseenheid (ad of trefwoord)). Voor Adobe DSP is de functie beschikbaar voor pakketten en de plaatsingen die aan een pakket zijn toegewezen, maar niet voor campagnes of plaatsingen met plaatsingsniveau.

De uit-van-de-doos steun is beschikbaar voor de volgende netwerken:<!-- But what if you want to use something else? Is that possible currently? -->

<!-- * Adobe Demand Side Platform (Advertising DSP) [Is any data upload required, or just an initial setup of an S3 bucket and/or something else, and then DSP sends the data automatically? If so, then I may need to reframe this whole chapter accordingly.] -->
<!-- * [!DNL Reddit Ads] -->

* [!DNL Apple Search Ads]
* [!DNL LinkedIn Ads]
* [!DNL TikTok Ads]

Op Zoeken, Sociaal en Commerce klikken en Adobe Advertising converteren volgen worden niet ondersteund met deze functie.

## Functionaliteit beschikbaar in Zoeken, Sociaal en Commerce

* Tekstspatiëring en rapportage:

   * Alleen-lezen campagnecomponenten tot het niveau van de biedingseenheid in de campagnebeheerweergaven.

   * Prestatiegegevens tot het niveau van de advertentiegroep <!-- verify the entity level --> binnen de meningen van het campagnebeheer en douanerapporten. Adverteerders met [!DNL Adobe Analytics for Advertising]) krijgen bovendien prestatiegegevens tot het niveau van de advertentiegroep <!-- verify the entity level --> in de Adobe Analytics-rapportsuite die voor de adverteerder is opgegeven.&lt;!— Controleren of de gegevenstypen beperkt zijn — kosten, klikken, indruk weergeven, inkomsten? —>

* De simulaties van prestaties wanneer u de campagnes aan een portefeuille toevoegt.<!-- How does this even work? Do they need to be in standard or hybrid portfolios, with active or optimized status, and can you mix these campaigns with API-synced campaigns? If so, do we just ignore these campaigns and optimize the others? -->

  Zoeken, Sociaal en Commerce optimaliseren niets en plaatsen zelfs geen biedingen voor dit soort campagnes binnen een portfolio.

## Workflow voor het instellen van offlineaccounts

<!-- subtitle wording? -->

1. [ opstelling een dummy rekeningsverslag ](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md).

1. Creeer een gegevensdossier voor één enkele rekening <!--  in what file format? -->, met inbegrip van de status op het dagniveau voor campagnes, en groepen, en advertenties.

De gegevens moeten de gegevensvereisten voor het advertentienetwerk volgen, zodat kunnen de gegevensgebieden voor elke entiteit door ad netwerk variëren.

1. <!-- For all ad networks (excluding DSP), -->Upload de initiële gegevens voor één account op een van de volgende manieren:

* Upload een bestand handmatig van uw apparaat of netwerk.

* Upload de gegevens naar een door Zoeken, Sociale en Commerce toegewezen map in een [!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3]) emmertje.

  >[!PREREQUISITES]
  >
  >* Neem contact op met uw Adobe-accountteam om het uploaden van accountgegevens voor uw advertentieaccount voor Zoeken, Sociaal en Commerce in te schakelen. Het team zal de verwezenlijking van een organisatie-specifieke omslag in een [!DNL S3] emmer vergemakkelijken, en zij zullen u op de hoogte brengen wanneer het wordt voltooid.<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
  >* Haal het [!DNL S3] -pad voor cloudopslag, de toegangstoets-id en de sleutel voor geheime toegang voor uw account op. Dezelfde toegangssleutel-id en geheime toegangssleutel worden gebruikt voor alle <!-- naming convention?--> -accounts van de organisatie die gegevens uploaden.

1. Blijf dagelijks nieuwe gegevensbestanden uploaden.

1. Zodra u gegevens voor 30 dagen hebt geupload, kunt u naar keuze de campagnes aan <!--what type? how should we refer to them? --> portefeuilles toevoegen en simulaties produceren.

U kunt [ een logboek van elke gegevens bekijken uploadt ](upload-log.md) om zijn status te zien. Bovendien als u een upload in werking stelt maar uploadt niet volledig succesvol is, dan ontvangt u een foutenmelding via [ Centrum van het Bericht ](/help/search-social-commerce/notifications/notification-about.md), dat op uw berichtmontages wordt gebaseerd.

<!-- Data validation, and any troubleshooting? -->

>[!MORELIKETHIS]
>
>* [ Ongeveer het uploaden rekeningsgegevens voor het melden en simulaties ](data-upload-accounts-about.md)
>* [ uploadt rekeningsgegevens aan een  [!DNL Amazon] [!DNL S3] emmertje ](upload-data-from-s3-bucket.md)
>* [ uploadt manueel rekeningsgegevens ](upload-data-manually.md)
>* [ Mening een logboek van geüploade dossiers van rekeningsgegevens ](upload-log.md)
>* [ beheer en netwerkrekeningen voor gegevensupload ](/help/search-social-commerce/campaign-management/accounts/data-upload-account-manage.md)
