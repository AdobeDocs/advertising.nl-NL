---
title: Netwerkaccounts beheren
description: Leer hoe u accountdetails voor een advertentienetwerkaccount instelt en beheert.
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Netwerkaccounts beheren

Hieronder vindt u instructies voor het maken en bewerken van gegevens van een netwerkaccount en het vernieuwen van de [!DNL oAuth] token voor een account en accounts uitschakelen.

## Gegevens van een advertentienetwerkaccount maken {#create-account}

*Accountmanager, accountmanager en alleen gebruikersrollen voor beheerders van Adobe*

Als u het synchroniseren of bijhouden van een account wilt inschakelen, moet u een corresponderend accountrecord maken met de toegangsgegevens van de account en de opties voor het bijhouden van de account en met de status *actief*. Voor details over de functionaliteit beschikbaar voor elk advertentienetwerk, zie &quot;[Ondersteunde voorraad](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

>[!NOTE]
>
>Ga naar de website van het advertentienetwerk om een werkelijke account op het advertentienetwerk te maken.

1. Klik in het hoofdmenu op **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klik in het submenu op **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Klik op de werkbalk boven de tabel met gegevens op ![Maken](/help/search-social-commerce/assets/add.png "Maken").

1. Geef de [accountinstellingen](#account-settings):

   1. Klik op de naam van het advertentienetwerk en klik vervolgens op **[!UICONTROL Next]**.

   1. In de **[!UICONTROL Account Details]** Voer de accountgegevens in.

      Voor advertentienetwerken die het type van login vergunning gebruiken &quot;[!UICONTROL oAuth],&quot; staat Search, Social &amp; Commerce toe om toegang te krijgen tot de account via de [OAuth-autorisatieprotocol](https://oauth.net/2/):

      1. Voer de **[!UICONTROL Login]** waarde voor de account, voert u desgewenst het wachtwoord in en klikt u op **[!UICONTROL Authenticate]**.

         De beste manier is om de aanmelding voor API-toegang tot de account te gebruiken. Voer het wachtwoord in wanneer u het wilt versleutelen en opslaan, zodat het accountteam van Adobe tokens naar wens kan vernieuwen.

      1. (Als u niet bent aangemeld bij de account van de adverteerder) Meld u aan bij de advertentieaccount van de adverteerder. De beste manier is om de referenties te gebruiken voor API-toegang tot de account.

      1. In het verzoek om toestemming/het toegangsscherm, klik de knoop om toestemming te bevestigen.

      1. Kopieer de verificatietekenreeks in het pop-upvenster dat wordt geopend, en plak de tekenreeks in de **[!UICONTROL oAuth Token]** veld.

      1. Geef de overige accountgegevens op.

   1. Klikken **[!UICONTROL Set Account Tracking]** en voer de instellingen voor bijhouden in.

1. Klik op **[!UICONTROL Post]**.

   Recente kosten en klik op gegevens voor alle campagnes in de account zijn binnen 24 uur beschikbaar in Zoeken, Sociale Zaken en Handel. Standaard zijn gegevens beschikbaar gedurende de laatste 5-10 dagen, afhankelijk van het advertentienetwerk. Indien nodig, echter, kan het team van de projectlancering gegevens voor maximaal de laatste 60 dagen terugwinnen.

## Gegevens van netwerkaccounts bewerken {#edit-account}

*Accountmanager, accountmanager en alleen gebruikersrollen voor beheerders van Adobe*

Als de verificatiegegevens van de account veranderen, wilt u de standaardparameters voor bijhouden van een account wijzigen. Als u activiteiten van een account wilt in- of uitschakelen, bewerkt u de accountgegevens.

>[!NOTE]
>
>Ga naar de website van het advertentienetwerk als u een werkelijke account op het advertentienetwerk wilt bewerken.

1. Klik in het hoofdmenu op **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klik in het submenu op **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Houd de cursor boven de accountnaam en klik op ![Meer](/help/search-social-commerce/assets/more-filters.png "Meer")en selecteer vervolgens **[!UICONTROL Edit]**.

1. Bewerk de [accountinstellingen](#account-settings):

   1. (Optioneel) Bewerk de accountgegevens.

   1. (Optioneel) Klik op **[!UICONTROL Set Account Tracking]** en bewerk de instellingen voor bijhouden.

1. Klik op **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >Zoek, Sociaal, &amp; Handel moet de nieuwe rekeningsgegevens met die op het advertentienetwerk synchroniseren. Dit gebeurt automatisch één keer per dag, of vaker wanneer Onderzoek, Sociale, &amp; Handel veranderingen op het advertentienetwerk ontdekt.

## Tokens voor automatische toegang tot zoekaccounts vernieuwen {#refresh-oauth-tokens}

*Accountmanager, accountmanager en alleen gebruikersrollen voor beheerders van Adobe*

Als Zoeken, Sociaal en Handel toegang heeft tot de account met de [OAuth-autorisatieprotocol](https://oauth.net/2/) en de geloofsbrieven van de rekening veranderen, of als extra toegang wordt vereist om nieuwe eigenschappen in Onderzoek, Sociale, &amp; Handel te steunen, dan moet u een nieuw toegangstoken voor de rekening krijgen.

Uw Adobe Account Team zal u informeren als de nieuwe eigenschappen een nieuw teken vereisen.

1. (Als u bent aangemeld bij een andere account voor hetzelfde advertentienetwerk in dezelfde browsertoepassing) Afmelden bij een andere account dan die van de adverteerder.

1. Klik in het hoofdmenu op **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klik in het submenu op **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Houd de cursor boven de accountnaam en klik op ![Meer](/help/search-social-commerce/assets/more-filters.png "Meer")en selecteer vervolgens **[!UICONTROL Edit]**.

1. Krijg een nieuw toegangstoken:

   1. Klik op **[!UICONTROL Get oAuth Token]**.

   1. (Als u niet bent aangemeld bij de account van de adverteerder) Meld u aan bij de advertentieaccount van de adverteerder. De beste manier is om de referenties te gebruiken voor API-toegang tot de account.

   1. In het verzoek om toestemming/het toegangsscherm, klik de knoop om toestemming te bevestigen.

   1. Kopieer de verificatietekenreeks in het pop-upvenster dat wordt geopend, en plak de tekenreeks in de **[!UICONTROL oAuth Token]** veld.

1. Klik op **[!UICONTROL Post]**.

## Enable or disable ad network accounts {#enable-disable-account}

*Accountmanager, accountmanager en alleen gebruikersrollen voor beheerders van Adobe*

Wanneer u een advertentienetwerkaccount inschakelt, synchroniseert u met Zoeken, Sociale Zaken en Handel campagnegegevens met de account (indien ondersteund) en voert u geautomatiseerde biedingen en/of campagnebudgetten voor campagnes in portfolio&#39;s uit.Wanneer u een advertentienetwerkaccount uitschakelt, stopt u met Zoeken, Sociaal en Handel alle activiteiten op de account. Gegevens die zijn verzameld terwijl de account actief was, worden nog opgeslagen, maar de weergaven en rapporten voor het campagnebeheer bevatten geen gegevens voor de periode waarin de account is uitgeschakeld. U kunt de account later weer inschakelen om de activiteiten met de account te hervatten.

1. Klik in het hoofdmenu op **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Klik in het submenu op **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Voer een van de volgende handelingen uit:

   * (Als u de status voor één account wilt wijzigen) Houd de cursor boven de accountnaam. Klik op ![Meer](/help/search-social-commerce/assets/more-filters.png "Meer")en selecteer vervolgens **[!UICONTROL Edit]**. Wijzig de **[!UICONTROL Status]** tot *Ingeschakeld* of *Uitgeschakeld* en klik vervolgens op **[!UICONTROL Post]**.

   * (Ga als volgt te werk om de status van een of meer accounts te wijzigen:

      1. Schakel het selectievakje naast elke account in.

         Voor tips over het selecteren van meerdere rijen raadpleegt u &quot;[Meerdere rijen selecteren](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Klik op de werkbalk boven de tabel met gegevens op ![Pictogram Activeren](/help/search-social-commerce/assets/activate.png "Pictogram Activeren") om de rekening of ![Pictogram uitschakelen](/help/search-social-commerce/assets/disable.png "Pictogram uitschakelen") om de account uit te schakelen.

## Instellingen voor netwerkaccounts toevoegen {#account-settings}

>[!NOTE]
>
>Alleen accountmanager van een agentschap [!DNL Adobe] accountbeheer en beheerders kunnen accountinstellingen configureren.

### Accountgegevens

**[!UICONTROL SE Account ID]:** (Alle rekeningen behalve [!DNL Naver] en [!DNL Yandex] rekeningen; (alleen bewerkbaar voor nieuwe accounts) De account-id die is toegewezen door het advertentienetwerk.

>[!NOTE]
>
>De rekeningen van de Adnetwork manager worden hier niet gesteund. Een beheerdersaccount identificeren voor [!DNL Microsoft Advertising] of [!DNL Yandex], gebruikt u het veld Master account-id of MCC-account. Naar [aanmeldingsgegevens instellen voor een [!DNL Google Ads] beheeraccount](/help/search-social-commerce/admin/manager-accounts.md), ga naar [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** De naam die moet worden weergegeven voor het account in Zoeken, Sociale media en Handel.

>[!NOTE]
>
>Als u de integratie Search, Social &amp; Commerce-Adobe Analytics hebt en de naam van de zoekaccount wijzigt, stuurt u een melding naar uw Adobe-accountteam zodat deze de toewijzing kan bijwerken.

**[!UICONTROL Login Details]: \[Aanmeldingstype\]** - ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] alleen) Of u aanmeldingsgegevens voor de account wilt autoriseren met:

* *[!UICONTROL oAuth]* (de standaardinstelling): Als u de opdracht [[!DNL OAuth] machtigingsprotocol](https://oauth.net/2/).

* *[!UICONTROL Password]:* Het wachtwoord van de client gebruiken.

Voor [!DNL Microsoft Advertising] alleen accounts [!DNL oAuth]-authorised logins kan worden gebruikt.

**[!UICONTROL Login Details]: [!UICONTROL Login]:** (Alle advertentienetwerken behalve [!DNL Naver]) De aanmeldnaam of -id om API-toegang tot het account in te schakelen.

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** ([!DNL Microsoft Advertising] [!DNL oAuth]-enabled en alle andere netwerken behalve [!DNL Baidu], [!DNL Meta], en [!DNL Yandex]) De token van de account voor het autoriseren van aanmeldingen met de [[!DNL OAuth] machtigingsprotocol](https://oauth.net/2/).

**[!UICONTROL Login Details]: [!UICONTROL Password]:** (Alle advertentienetwerken behalve [!DNL Naver]) Het wachtwoord voor de account. Voor accounts waarvoor wachtwoorden zijn ingeschakeld: [!DNL Baidu], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], en [!DNL Yandex]is dit veld vereist. Voor [!DNL oAuth]-enabled accounts, is dit veld optioneel; gebruik dit wanneer u het wachtwoord wilt coderen en opslaan, zodat accountmanager tokens naar wens kan vernieuwen.

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** ([!DNL Baidu] en [!DNL Yandex] alleen accounts) De toegangstoets voor de ontwikkelaarsaccount die moet worden gebruikt.

**[!UICONTROL Currency]:** De afkorting van de voor de rekening gebruikte valuta. Dit veld kan worden bewerkt voor nieuwe [!DNL Naver] rekeningen. Voor alle andere onderzoeksnetwerken, wordt de waarde automatisch gevuld met de munt die voor de rekening op het advertentienetwerk wordt gevormd zodra u sparen het verslag.

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] en [!DNL Microsoft Advertising] alleen rekeningen; (facultatief) om het even welke parameters om aan het eind van definitieve URLs aan spoorinformatie toe te voegen; omvat alle parameters die uw zaken moeten volgen.

Voorbeeld: `param1=value1&param2=value2`

Accounts die Adobe Advertising Click tracking gebruiken, moeten de klikidentificatie van het advertentienetwerk bevatten (`msclkid` for [!DNL Microsoft Advertising]; `gclid` voor Google) in het achtervoegsel. Accounts met een Adobe Analytics-integratie moeten de `s_kwcid` parameter. Als de account een s\_kwcid-implementatie aan de serverzijde heeft, wordt de parameter automatisch toegevoegd wanneer een gebruiker op een advertentie klikt; anders, moet u het hier manueel toevoegen. Zie de [vereiste achtervoegselformaten voor [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) en [vereiste achtervoegselformaten voor [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Dit veld wordt niet bijgewerkt door de [!UICONTROL Auto Upload] instelling voor tekstspatiëring.
>* De laatste URL-achtervoegsels op lagere niveaus overschrijven het achtervoegsel op accountniveau. Gebruik voor een eenvoudiger onderhoud alleen het achtervoegsel op accountniveau, tenzij het bijhouden van wijzigingen voor afzonderlijke accountcomponenten nodig is. Om een achtervoegsel op het niveau van de advertentiegroep of lager te vormen, gebruik de redacteur van het ad netwerk.

**Tijdzone:** (Alle advertentienetwerken behalve [!DNL Baidu] en [!DNL Yahoo! Display Network]) De tijdzone van de adverteerder. Dit veld kan worden bewerkt en optioneel voor nieuwe [!DNL Naver] rekeningen. Voor alle andere onderzoeksnetwerken, wordt de waarde automatisch gevuld met de tijdzone die voor de rekening van het Onderzoek, Sociale, &amp; van de Handel van de adverteerder wordt gevormd zodra u het verslag opslaat.

**Status:** De rekeningstatus in Zoeken, Sociale &amp; Handel:

* *Ingeschakeld:* Met Zoeken, Sociale media en Handel worden campagnegegevens gesynchroniseerd met de account (indien ondersteund) en worden geautomatiseerde biedingen en/of campagnebudgetten voor campagnes in portfolio&#39;s onder de aandacht gebracht.
* *Uitgeschakeld:* Met Zoeken, Sociaal en Handel stopt u alle activiteiten op de account. Gegevens die zijn verzameld terwijl de account actief was, worden nog opgeslagen, maar de weergaven en rapporten voor het campagnebeheer bevatten geen gegevens voor de periode waarin de account is gepauzeerd. U kunt het account later opnieuw activeren om de activiteiten met het account te hervatten.

**Sjabloon voor bijhouden** - ([!DNL Google Ads], [!DNL Microsoft Advertising], en [!DNL Yahoo! Japan Ads] alleen rekeningen; (optioneel) De standaard volgsjabloon voor de account, die alle omleidingen en volgparameters van het niet-landende domein opgeeft en ook de URL van de laatste/bestemmingspagina in een parameter insluit. Voorbeeld: `{lpurl}?source={network}&id=5` of `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` om een omleiding op te nemen.

* De uiteindelijke URL insluiten:

   * ([!DNL Google Ads] en [!DNL Microsoft Advertising] alleen) Voor een lijst met parameters die de uiteindelijke URL&#39;s aangeven in trackingsjablonen, raadpleegt u ([!DNL Microsoft Advertising] alleen) [[!DNL Microsoft Advertising] documentatie](https://help.ads.microsoft.com/#apex/3/en/56799) of ([!DNL Google Ads] alleen) de &quot;Volgsjabloon alleen&quot;-parameters in de sectie &quot;Beschikbaar [!DNL ValueTrack] Parameters&quot; in de [[!DNL Google Ads] documentatie](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] alleen) De parameter gebruiken `!{lpurl}` om de URL van de landingspagina aan te geven.

* U kunt optioneel URL-parameters en aangepaste parameters die zijn gedefinieerd voor de campagne opnemen, gescheiden door en-tekens (&amp;), zoals `{lpurl}?matchtype={matchtype}&device={device}`.

* U kunt desgewenst omleidingen en tekstspatiëring van derden toevoegen.

* Wanneer de campagne-instellingen &quot;[!UICONTROL EF Redirect]&quot; en &quot;[!UICONTROL Auto Upload],&quot; Onderzoek, Sociale, &amp; Handel vooraf fixeert automatisch zijn eigen omleiding en het volgen code wanneer u sparen het verslag.

>[!NOTE]
>
>* Voor [!DNL Google Ads], vermijd het gebruiken van macro&#39;s, die niet voor kliks van bronnen substitueren die parallel volgen toelaten. Als de adverteerder macro&#39;s moet gebruiken, moet het Adobe Account Team met de Klantenondersteuning of het implementatieteam samenwerken om deze toe te voegen.
>* De het volgen malplaatje op het meest korrelige niveau treedt de waarden op alle hogere niveaus met voeten. Als zowel de accountinstellingen als de trefwoordinstellingen bijvoorbeeld een waarde bevatten, wordt de trefwoordwaarde toegepast.
>* Als u een trackingsjabloon bijwerkt op advertentie-, sitelink- of trefwoordniveau, worden de relevante advertenties opnieuw verzonden voor revisie. U kunt de trackingsjablonen op account-, campagne- of advertentieniveau bijwerken zonder uw advertenties opnieuw ter goedkeuring in te dienen.

**[!UICONTROL Master Account ID]:** ([!DNL Microsoft Advertising] (alleen accounts) De ID voor een agentschap/beheeraccount die bij de account hoort.

**[!UICONTROL MCC Account]:** ([!DNL Yandex] alleen rekeningen; (facultatief) een agentschap/beheersrekening verbonden aan de rekening. Als u een bestaande koppeling wilt verwijderen, selecteert u &quot;[!UICONTROL No MCC Account].&quot;

**[!UICONTROL Application ID]:** ([!DNL Yandex] alleen accounts) De ontwikkelaarstoken die voor de account moet worden gebruikt. Hetzelfde token wordt gebruikt voor alles [!DNL Yandex] rekeningen.

**[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] accounts met de instelling Gedeelde account alleen uitgeschakeld; (optioneel) De numerieke id van de campagne die wordt gebruikt voor alle advertentiecampagnes in de account.

**[!UICONTROL Finance Token]:** ([!DNL Yandex] accounts met de instelling Gedeelde account alleen uitgeschakeld; (optioneel) De ontwikkelaarstoken die moet worden gebruikt voor API-aanroepen die betrekking hebben op financiering, bijvoorbeeld voor het opnieuw toewijzen van geld uit de portemonnee tussen de campagnes van de adverteerder, indien nodig voor het optimaliseren van het portfolio.

### Account bijhouden

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (Voor [!UICONTROL EF Redirect] alleen) Niet geïmplementeerd

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **S\_kwcid-indeling** - (Bestaande [!DNL Google Ads] accounts voor adverteerders met een Adobe Advertising-Adobe Analytics-integratie en waarvoor de s\_kwcid nog niet is gemigreerd)

Dit account gebruikt de oudere indeling voor de s\_kwcid-trackingcode, waarmee Adobe-advertenties gegevens over het account kunnen delen met Adobe Analytics. De [nieuwste indeling](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md) bevat parameters voor campagne-id en groep-id, die nodig zijn om nauwkeurig te rapporteren op campagne- en advertentieniveau voor [!DNL Google Ads] maximaal presterende campagnes en concepten en experimentatiecampagnes in Analytics:

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

Als dit account op campagne- en advertentieniveau moet rapporteren, klikt u op de knop [!UICONTROL Edit] (potlood) en vervolgens **[!UICONTROL Migrate to new s\_kwcid format]** wijzigen in de nieuwe indeling. Voor accounts die deze typen campagnes niet bevatten, is het migreren naar de nieuwe indeling optioneel, maar aanbevolen.

Voor volledige instructies raadpleegt u &quot;[De s\_kwcid volgcode voor een bijwerken [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-skwcid-google.md).&quot;

**Namen van rapportsuite** - (alleen voor EF-omleiding met token; adverteerders met Adobe Advertising-Adobe Analytics-integratie; (optioneel) Een of meer Analytics-rapportreeksen waarnaar Search, Social &amp; Commerce gegevens verzendt die deze verzamelt via het advertentienetwerk, inclusief entiteitsclassificaties en klik op gegevens voor de account. Deze functie is alleen beschikbaar voor ondersteunde advertentienetwerken.

Om de gegevens in de rapportreeksen te verschijnen, of a) moet de server-kant s\_kwcid voor de rekening worden gevormd of b) het adverteerder-niveau plaatsen aan &quot;[!UICONTROL Enable tracking for SAINT feeds]&quot; moet zijn ingeschakeld. Daarnaast moet de account Analytics van de adverteerder zo zijn geconfigureerd dat gegevens van Search, Social &amp; Commerce worden ontvangen. Neem voor meer informatie contact op met uw Adobe-accountmanager.

>[!MORELIKETHIS]
>
>* [Informatie over netwerkaccounts](ad-network-account-about.md)
>* [Zakelijke accounts beheren](merchant-account-manage.md)
>* [De s\_kwcid volgcode voor een bijwerken [!DNL Google Ads] account](update-skwcid-google.md)
