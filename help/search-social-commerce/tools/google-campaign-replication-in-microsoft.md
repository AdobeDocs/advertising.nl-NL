---
title: Repliceren [!DNL Google Ads] campagnes in [!DNL Microsoft® Advertising]
description: Leer hoe u uw gesynchroniseerde campagnes exporteert in een [!DNL Google Ads] account direct in een gesynchroniseerd account [!DNL Microsoft® Advertising] account.
exl-id: 1bb0d915-bf33-4c50-88a5-268d4de5ccff
feature: Search Tools
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 0%

---

# Repliceren [!DNL Google Ads] campagnes in [!DNL Microsoft® Advertising]

U kunt uw gesynchroniseerde campagnes exporteren in een [!DNL Google Ads] account direct in een gesynchroniseerd account [!DNL Microsoft® Advertising] als verbeterde CPC-campagnes (eCPC). De bestaande biedingen en campagnebudgetten worden geschaald. Bestaande tracering van zoekopdrachten, sociale gegevens en handel wordt niet geïmporteerd.

U kunt de volgende typen campagnes en de bijbehorende campagnestructuur repliceren:

* [!DNL Google Ads] zoeken en campagnes weergeven in [!DNL Microsoft® Advertising] zoek- en weergavecampagnes.

* [!DNL Google Display Network] campagnes, waaronder afbeeldingen, in [!DNL Microsoft® Advertising] publiekscampagnes over het Microsoft® Audience Network.

  Als u boodschappencampagnes op basis van feed wilt herhalen, moet u eerst uw [!DNL Google Merchant Center] productaanbiedingen voor [!DNL Microsoft® Merchant Center]. Wanneer u de campagnes kopieert, selecteert u de [!DNL Microsoft® Merchant Center] in Importopties opslaan om de winkel te koppelen aan uw doelgerichte campagnes.

* [!DNL Google Ads] maximale prestatiecampagnes, inclusief lokale voorraadadvertenties, in [!DNL Microsoft® Advertising] slimme winkelcampagnes.

U kunt ervoor kiezen de campagnes eenmaal bij te werken, dagelijks wekelijks of maandelijks, of volgens [!DNL Microsoft® Advertising]aanbevolen schema. U kunt meldingen desgewenst configureren telkens wanneer een importtaak wordt uitgevoerd of wanneer er fouten of wijzigingen optreden. Nadat u uw campagnes hebt geïmporteerd in [!DNL Microsoft® Advertising]kunt u de status van de importtaak controleren, eventuele foutlogboeken controleren, een importtaak handmatig uitvoeren en uw importschema bewerken, pauzeren, inschakelen of verwijderen.

Niet alle campagnegegevens worden gerepliceerd en u moet mogelijk informatie toevoegen aan uw [!DNL Microsoft® Advertising] campagnes. Voor meer informatie over welke gegevens worden ingevoerd, zie [!DNL Microsoft® Advertising] help over &quot;[Wat wordt geïmporteerd uit [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851).&quot; Omdat het zoeken, Sociale, &amp; het volgen van de Handel niet wordt ingevoerd, zou u het volgen binnen moeten ook toevoegen [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [ad-groep](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md), of [advertentie](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) instellingen.

## Repliceren [!DNL Google Ads] campagnes

>[!NOTE]
>
>Als u winkelende, op feed gebaseerde weergavecampagnes wilt herhalen, moet u eerst [repliceer uw [!DNL Google Merchant Center] productaanbiedingen in [!DNL Microsoft® Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). Wanneer u de campagnes kopieert, selecteert u de [!DNL Microsoft® Merchant Center] in de importopties opslaan om de winkel aan uw doelcampagnes te koppelen.

Zie [waaruit wordt geïmporteerd [!DNL Google Ads] campagnes](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Klik in het hoofdmenu Zoeken, Sociaal en Handel op **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Klik op **[!UICONTROL +Import]**.

1. Geef de [importinstellingen](#campaign-import-settings):

   1. In de **[!UICONTROL Select accounts]** sectie:

      1. Selecteer de bron- en doelaccounts.

      1. Klik op **[!UICONTROL Get Credential Id from MSA]**.

      1. Aanmelden bij de bestemming [!DNL Microsoft Advertising] account, kopieert u de referentie-id die wordt weergegeven en plakt u de waarde in de **[!UICONTROL Credential ID]** veld.

   1. In de **[!UICONTROL Select campaigns & ad groups]** , geeft u op welke campagnes en advertentiegroepen u wilt importeren.

   1. In de **[!UICONTROL Customize your import]** , geeft u de itemtypen op die u wilt importeren.

   1. In de **[!UICONTROL Set schedule]** , geeft u op wanneer de importtaak moet worden uitgevoerd.

1. Klik op **[!UICONTROL Post]**.

1. (Optioneel) Zoek-, sociale en handelstracering toevoegen in het dialoogvenster [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [ad-groep](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md), of [advertentie](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) instellingen.

## Planningsinstellingen voor een importtaak voor een campagne bewerken

Zie [waaruit wordt geïmporteerd [!DNL Google Ads] campagnes](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Schakel het selectievakje naast de importtaak in en klik op ![Bewerken](/help/search-social-commerce/assets/edit.png "Bewerken").

1. In de **[!UICONTROL Set schedule]** in, geeft u de [planningsinstellingen](#campaign-import-settings).

1. Klik op **[!UICONTROL Post]**.

## Uw campagne-importtaken weergeven

U kunt alle importtaken weergeven, inclusief de bron [!DNL Google Ads] account, het doel [!DNL Microsoft® Advertising] -account, de importtijd of het -schema en de gebruiker die de taak heeft gemaakt. Wanneer u een importtaak meerdere keren uitvoert, ook tijdens regelmatig geplande importbewerkingen, wordt elk exemplaar weergegeven als een afzonderlijke taak.

* Voer een van de volgende handelingen uit:

   * Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

     Standaard wordt de weergave geopend voor de [!UICONTROL List of Import Jobs] tab.

   * Van de [[!UICONTROL Import Logs] tab](#campaign-import-log)klikt u op de knop **[!UICONTROL List of Import Jobs]** tab.

## Een importtaak voor de campagne uitvoeren

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Schakel het selectievakje naast de importtaak in.

1. Klikken ![Nu uitvoeren](/help/search-social-commerce/assets/run.png "Nu uitvoeren").

## Logboeken weergeven voor importtaken voor uw campagne {#campaign-import-log}

U kunt alle voltooide of mislukte importtaken weergeven, inclusief de begintijd, de bron [!DNL Google Ads] account, het doel [!DNL Microsoft® Advertising] -account, de gebruiker die de taak heeft gemaakt, het aantal geslaagde en mislukte bewerkingen en alle e-mailadressen die meldingen voor elke taak hebben ontvangen. U kunt meer details over de veranderingen van het doel bekijken [!DNL Microsoft® Advertising] de account die voor elke taak is opgetreden, inclusief het aantal toegevoegde, gesynchroniseerde, verwijderde items en de items die fouten op elk entiteitsniveau (zoals campagne of trefwoord) in de account hebben veroorzaakt.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Klik op de knop **[!UICONTROL Import Logs]** tab.

1. (Optioneel) Klik op de waarde in het dialoogvenster [!UICONTROL Summary] kolom.

## Instellingen voor het importeren van campagnes {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** De gesynchroniseerde [!DNL Google Ads] account waaruit campagnegegevens worden geëxporteerd.

**[!UICONTROL Credential ID]:** Een id die [!DNL Microsoft® Advertising] gebruikers om uw te vertegenwoordigen [!DNL Google Ads] referenties.

Automatisch genereren van [!DNL Microsoft® Advertising] referenties voor importeren zijn niet beschikbaar vanwege [!DNL Microsoft® Advertising] beperkingen. Neem contact op met de technische ondersteuning van de Adobe of met uw Adobe-accountteam. Deze medewerkers genereren de gegevens en geven u de id.

**[!UICONTROL Target Microsoft® Ads account]:** De gesynchroniseerde [!DNL Microsoft® Advertising] rekening waarin campagnegegevens worden ingevoerd.

### [!UICONTROL Select campaigns & ad groups]

**\[Te importeren gegevens\]:** Geef de te importeren gegevens op:

* *[!UICONTROL Import all new and existing campaigns]:* Gegevens importeren voor alle campagnes die al bestaan en campagnes die niet bestaan in [!DNL Microsoft® Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* Om specifieke campagnes en ad groepen te selecteren.

   * Als u een campagne wilt uitbreiden naar onderliggende en onderliggende groepen, klikt u op **[!UICONTROL >]** na de naam van de campagne.

   * Als u een campagne of advertentiegroep wilt selecteren, selecteert u het item zodat er een vinkje verschijnt.

   * Een campagne of advertentiegroep verwijderen:

      * In de [!UICONTROL Campaigns] of [!UICONTROL Adgroups] deselecteert u de campagne of de ad-groep zodat het vinkje verdwijnt.

      * In de [!UICONTROL Selected] kolom, klik ![Verwijderen](/help/search-social-commerce/assets/delete.png "Verwijderen").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Hiermee kunt u opgeven wat u wilt importeren, bieden en budgetten en andere opties.

**[!UICONTROL What to import]:** Definieert de items die moeten worden geïmporteerd. Opties voor het importeren van itemcategorieën zijn standaard geselecteerd, waarbij alle itemtypen zijn geselecteerd. Als u alleen bepaalde itemtypen wilt opnemen, klikt u op **[!UICONTROL Show advanced options]** en wijzig de itemtypen die u wilt opnemen.

**[!UICONTROL Bids and budgets]:** Hiermee definieert u welke bied- en begrotingsinstellingen moeten worden geïmporteerd, bijgewerkt en aangepast.

**[!UICONTROL Other options]:** Hiermee definieert u hoe geïmporteerde bestemmingspagina-URL&#39;s, trackingsjablonen en andere campagne-, advertentie- en doelopties moeten worden afgehandeld.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** De naam van de importtaak.

**[!UICONTROL When]:** Wanneer importeert u de opgegeven campagnes: *Automatisch* (aan [!DNL Microsoft® Advertising] een schema instellen om uw campagnes zo goed mogelijk te optimaliseren); *[!UICONTROL Now]* (om de taak uit te voeren wanneer u de taakinstellingen plaatst), *[!UICONTROL Once]* op een bepaald tijdstip *[!UICONTROL Daily]* op een bepaald tijdstip *[!UICONTROL Weekly]* op een bepaald tijdstip, of *[!UICONTROL Monthly]* op een opgegeven tijdstip.

**[!UICONTROL Receive email notifications]:** Als en wanneer u e-mailmeldingen over importtaken wilt verzenden naar de e-mailadressen in het veld Rapporten verzenden naar.

**[!UICONTROL Send reports to]:** E-mailadressen waarop meldingen over importtaken kunnen worden ontvangen. Scheid veelvoudige adressen met komma&#39;s (`,`).
