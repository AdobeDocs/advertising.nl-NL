---
title: Herhaal  [!DNL Google Ads]  campagnes in  [!DNL Microsoft Advertising]
description: Leer hoe te om uw gesynchroniseerde campagnes in a  [!DNL Google Ads]  rekening in een gesynchroniseerde  [!DNL Microsoft Advertising]  rekening direct uit te voeren.
exl-id: e7714d3d-4a8e-44ef-a3a7-e5198c091660
feature: Search Tools
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# [!DNL Google Ads] -campagnes herhalen in [!DNL Microsoft Advertising]

U kunt uw gesynchroniseerde campagnes in een [!DNL Google Ads] account rechtstreeks exporteren naar een gesynchroniseerde [!DNL Microsoft Advertising] -account als verbeterde CPC-campagnes (eCPC). De bestaande biedingen en campagnebudgetten worden geschaald. Bestaande tracking van zoekopdrachten, sociale en Commerce-bestanden worden niet geïmporteerd.

U kunt de volgende typen campagnes en de bijbehorende campagnestructuur repliceren:

* [!DNL Google Ads] zoek- en weergavecampagnes in [!DNL Microsoft Advertising] .

* [!DNL Google Display Network] voert campagnes, waaronder afbeeldingen, in [!DNL Microsoft Advertising] -publiekscampagnes op het Microsoft Audience Network.

  Als u boodschappencampagnes op basis van feed wilt herhalen, moet u eerst de [!DNL Google Merchant Center] -productaanbiedingen overnemen naar [!DNL Microsoft Merchant Center] . Wanneer u de campagnes dupliceert, selecteert u de [!DNL Microsoft Merchant Center] -winkel in de Importopties om de winkel te koppelen aan uw doelcampagnes op basis van de feed.

* [!DNL Google Ads] presteert max-campagnes, inclusief lokale voorraadadvertenties, in [!DNL Microsoft Advertising] maximale prestatiecampagnes.

U kunt ervoor kiezen de campagnes eenmaal bij te werken, dagelijks wekelijks of maandelijks, of volgens het door [!DNL Microsoft Advertising] aanbevolen schema. U kunt meldingen desgewenst configureren telkens wanneer een importtaak wordt uitgevoerd of wanneer er fouten of wijzigingen optreden. Nadat u uw campagnes hebt geïmporteerd in [!DNL Microsoft Advertising] , kunt u de status van uw importtaak controleren, eventuele foutmeldingen controleren, handmatig een importtaak uitvoeren en uw importschema bewerken, pauzeren, inschakelen of verwijderen.

Niet alle campagnegegevens worden gerepliceerd en u moet mogelijk informatie toevoegen aan uw [!DNL Microsoft Advertising] -campagnes. Voor meer informatie over welke gegevens worden ingevoerd, zie [!DNL Microsoft Advertising] hulp op &quot;[ wat wordt ingevoerd van  [!DNL Google Ads] ](https://help.ads.microsoft.com/#apex/ads/en/50851).&quot; Omdat het Onderzoek, Sociaal, &amp; het volgen van Commerce niet wordt ingevoerd, zou u het volgen binnen de [ rekening ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [ campagne ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [ en groep ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md), of [ en ](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) montages ook moeten toevoegen.

## [!DNL Google Ads] campagnes herhalen

>[!NOTE]
>
>Als u het winkelen op diervoeder-gebaseerde vertoningscampagnes wilt herhalen, eerst [ repliceer uw  [!DNL Google Merchant Center]  productaanbiedingen in  [!DNL Microsoft Merchant Center] ](https://help.ads.microsoft.com/apex/index/3/en/56870). Wanneer u de campagnes dupliceert, selecteert u de [!DNL Microsoft Merchant Center] -winkel in de importopties om de winkel te koppelen aan uw doelcampagnes op basis van de feed.

Zie [ wat van  [!DNL Google Ads]  campagnes ](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500) wordt ingevoerd.

1. Klik in het hoofdmenu Zoeken, Sociaal en Commerce op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]** .

1. Klik op **[!UICONTROL +Import]**.

1. Specificeer de [ invoermontages ](#campaign-import-settings):

   1. In de sectie **[!UICONTROL Select accounts]** :

      1. Selecteer de bron- en doelaccounts.

      1. Klik op **[!UICONTROL Get Credential Id from MSA]**.

      1. Meld u aan bij de doelaccount [!DNL Microsoft Advertising] , kopieer de referentie-id die wordt weergegeven en plak de waarde in het veld **[!UICONTROL Credential ID]** .

   1. Geef in de sectie **[!UICONTROL Select campaigns & ad groups]** op welke campagnes en groepen toevoegen u wilt importeren.

   1. Geef in de sectie **[!UICONTROL Customize your import]** de itemtypen op die u wilt importeren.

   1. Geef in de sectie **[!UICONTROL Set schedule]** op wanneer de importtaak moet worden uitgevoerd.

1. Klik op **[!UICONTROL Post]**.

1. (Facultatief) voeg Onderzoek, Sociale, &amp; het volgen van Commerce binnen de [ rekening ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) toe, [ campagne ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [ en groep ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md), of [ en ](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) montages.

## Planningsinstellingen voor een importtaak voor een campagne bewerken

Zie [ wat van  [!DNL Google Ads]  campagnes ](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500) wordt ingevoerd.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]** .

1. Selecteer de controledoos naast de de invoerbaan, en klik dan ![ uitgeven ](/help/search-social-commerce/assets/edit.png " ").

1. In de **[!UICONTROL Set schedule]** sectie, specificeer de [ planningsmontages ](#campaign-import-settings).

1. Klik op **[!UICONTROL Post]**.

## Uw campagne-importtaken weergeven

U kunt alle importtaken weergeven, inclusief de bronaccount [!DNL Google Ads] , de doelaccount [!DNL Microsoft Advertising] , de importtijd of -planning en de gebruiker die de taak heeft gemaakt. Wanneer u een importtaak meerdere keren uitvoert, ook tijdens regelmatig geplande importbewerkingen, wordt elk exemplaar weergegeven als een afzonderlijke taak.

* Voer een van de volgende handelingen uit:

   * Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]** .

     Standaard wordt de weergave geopend op de tab [!UICONTROL List of Import Jobs] .

   * Klik op de tab [[!UICONTROL Import Logs] ](#campaign-import-log) op de tab **[!UICONTROL List of Import Jobs]** .

## Een importtaak voor de campagne uitvoeren

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]** .

1. Schakel het selectievakje naast de importtaak in.

1. Klik ![ Looppas nu ](/help/search-social-commerce/assets/run.png " ").

## Logboeken weergeven voor importtaken voor uw campagne {#campaign-import-log}

U kunt alle voltooide of mislukte importtaken weergeven, zoals de begintijd, de bron- [!DNL Google Ads] account, de doel- [!DNL Microsoft Advertising] account, de gebruiker die de taak heeft gemaakt, het aantal geslaagde en mislukte bewerkingen en alle e-mailadressen die meldingen voor elke taak hebben ontvangen. U kunt meer informatie bekijken over de wijzigingen in de doel [!DNL Microsoft Advertising] -account die voor elke taak zijn opgetreden, inclusief het aantal toegevoegde, gesynchroniseerde, verwijderde items en de wijzigingen die fouten hebben opgeleverd voor elk entiteitsniveau (zoals campagne of trefwoord) in de account.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]** .

1. Klik op de tab **[!UICONTROL Import Logs]** .

1. (Optioneel) Klik op de waarde in de kolom [!UICONTROL Summary] om details voor een importtaak weer te geven.

## Instellingen voor het importeren van campagnes {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** De gesynchroniseerde [!DNL Google Ads] account waaruit campagnegegevens worden geëxporteerd.

**[!UICONTROL Credential ID]:** Een id die [!DNL Microsoft Advertising] gebruikt om uw [!DNL Google Ads] referenties weer te geven.

Automatisch genereren van [!DNL Microsoft Advertising] -gegevens voor importeren is niet beschikbaar vanwege [!DNL Microsoft Advertising] -beperkingen. Neem contact op met uw Adobe-accountteam. Vervolgens worden de gegevens gegenereerd en krijgt u de id.

**[!UICONTROL Target Microsoft Ads account]:** De gesynchroniseerde [!DNL Microsoft Advertising] account waarin campagnegegevens worden geïmporteerd.

### [!UICONTROL Select campaigns & ad groups]

**\[Te importeren gegevens\]:** Geef de te importeren gegevens op:

* *[!UICONTROL Import all new and existing campaigns]:* Gegevens importeren voor alle campagnes die al bestaan en voor campagnes die niet in [!DNL Microsoft Advertising] voorkomen.

* *[!UICONTROL Import specific campaigns and adgroups]:* specifieke campagnes en ad groepen selecteren.

   * Als u een campagne wilt uitbreiden naar onderliggende en onderliggende groepen, klikt u op **[!UICONTROL >]** achter de naam van de campagne.

   * Als u een campagne of advertentiegroep wilt selecteren, selecteert u het item zodat er een vinkje verschijnt.

   * Een campagne of advertentiegroep verwijderen:

      * Schakel in de kolom [!UICONTROL Campaigns] of [!UICONTROL Adgroups] de campagne of de ad-groep uit, zodat het vinkje verdwijnt.

      * In de [!UICONTROL Selected] kolom, klik ![ Schrapping ](/help/search-social-commerce/assets/delete.png " ").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Hiermee kunt u opgeven wat u wilt importeren, biedingen en budgetten en andere opties.

**[!UICONTROL What to import]:** bepaalt de punten om in te voeren. Opties voor het importeren van itemcategorieën zijn standaard geselecteerd, waarbij alle itemtypen zijn geselecteerd. Als u alleen bepaalde itemtypen wilt opnemen, klikt u op **[!UICONTROL Show advanced options]** en wijzigt u de itemtypen die u wilt opnemen.

**[!UICONTROL Bids and budgets]:** bepaalt welke bied- en begrotingsinstellingen moeten worden geïmporteerd, bijgewerkt en aangepast.

**[!UICONTROL Other options]:** bepaalt hoe te om ingevoerde het landen pagina URLs, het volgen malplaatjes, en andere campagne, en, en het richten opties te behandelen.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** De naam van de importtaak.

**[!UICONTROL When]:** Wanneer om de gespecificeerde campagnes in te voeren: *Auto* (om [!DNL Microsoft Advertising] een programma te laten plaatsen om uw campagnes het best te optimaliseren), *[!UICONTROL Now]* (om de baan in werking te stellen wanneer u de baanmontages) plaatst, *[!UICONTROL Once]* op een gespecificeerde tijd, *[!UICONTROL Daily]* op een gespecificeerde tijd, *[!UICONTROL Weekly]* op een gespecificeerde tijd, of *[!UICONTROL Monthly]* op een gespecificeerde tijd.

**[!UICONTROL Receive email notifications]:** Als en wanneer e-mailmeldingen over importtaken moeten worden verzonden naar de e-mailadressen in het veld Rapporten verzenden naar.

**[!UICONTROL Send reports to]:** E-mailadressen voor het ontvangen van meldingen over importtaken. Scheid veelvoudige adressen met komma&#39;s (`,`).
