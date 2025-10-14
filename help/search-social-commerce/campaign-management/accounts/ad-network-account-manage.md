---
title: Netwerkaccounts beheren
description: Leer hoe u accountdetails voor een advertentienetwerkaccount instelt en beheert.
exl-id: 4038d03b-63e2-4953-89df-37f7b5f68652
feature: Search Campaign Management
source-git-commit: cb65108fcc60c11b901e3b43c292ad5a94192b9f
workflow-type: tm+mt
source-wordcount: '2079'
ht-degree: 0%

---

# Netwerkaccounts beheren

<!-- Probably need to change the page title. If I update the filename, get B. to create a redirect to the new URL. -->

Hieronder vindt u instructies voor het maken en bewerken van gegevens van een netwerkaccount, het [!DNL oAuth] -token voor een account vernieuwen en accounts uitschakelen.

<!-- Move out info about Naver?  Then change to the following:  Following are instructions for creating and editing account details for an ad network account that Search, Social, & Commerce will sync using the ad network's API; refreshing the [!DNL oAuth] token for an account; and disabling accounts. -->

<!-- Also update Description metadata to "Learn how to set up and manage account details for an ad network account synced via the ad network API." -->

Voor details over de functionaliteit beschikbaar voor elk advertentienetwerk, zie &quot;[&#x200B; Gesteunde Inventaris &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

## Gegevens van een advertentienetwerkaccount maken {#create-account}

*de rekeningsmanager van het Agentschap, de rekeningsmanager van Adobe, en slechts de rollen van de beheerdergebruiker*

Om het synchroniseren of het volgen van een rekening toe te laten, moet u een overeenkomstig rekeningsverslag tot stand brengen dat de geloofsbrieven van de rekeningstoegang en het volgen opties en met de status *actieve* bevat.

>[!NOTE]
>
>* Ondersteuning is niet beschikbaar voor nieuwe [!DNL Baidu] -accounts.
>* Ga naar de website van het advertentienetwerk om een werkelijke account op het advertentienetwerk te maken.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]** . Klik in het submenu op **[!UICONTROL Live]** \> **[!UICONTROL Accounts]** .

1. In de toolbar boven de gegevenslijst, leidt de klik ![&#x200B; &#x200B;](/help/search-social-commerce/assets/add.png " tot ").

1. Specificeer de [&#x200B; rekeningsmontages &#x200B;](#account-settings):

   1. Klik op de naam van het advertentienetwerk en klik vervolgens op **[!UICONTROL Next]** .

   1. Voer in de sectie **[!UICONTROL Account Details]** de accountgegevens in.

      Voor advertentienetwerken die het login toestemmingstype &quot;[!UICONTROL oAuth] gebruiken,&quot;sta Onderzoek, Sociale, &amp; Commerce toe om tot de rekening toegang te hebben gebruikend het [&#x200B; OAuth vergunningsprotocol &#x200B;](https://oauth.net/2/):

      1. Voer de **[!UICONTROL Login]** -waarde voor de account in, voer desgewenst het wachtwoord in en klik op **[!UICONTROL Authenticate]** .

         De beste manier is om de aanmelding voor API-toegang tot de account te gebruiken. Voer het wachtwoord in wanneer u het wilt versleutelen en opslaan, zodat het Adobe-accountteam tokens naar wens kan vernieuwen.

      1. (Als u niet bent aangemeld bij de account van de adverteerder) Meld u aan bij de advertentieaccount. De beste manier is om de referenties te gebruiken voor API-toegang tot de account.

      1. In het verzoek om toestemming/het toegangsscherm, klik de knoop om toestemming te bevestigen.

      1. Kopieer de verificatietekenreeks in het pop-upvenster dat wordt geopend en plak de tekenreeks in het veld **[!UICONTROL oAuth Token]** .

      1. Geef de overige accountgegevens op.

   1. Klik op **[!UICONTROL Set Account Tracking]** en voer de instellingen voor bijhouden in.

1. Klik op **[!UICONTROL Post]**.

   Recente kosten en klik op gegevens voor alle campagnes in de account zijn binnen 24 uur beschikbaar in Zoeken, Sociaal en Commerce. Standaard zijn gegevens beschikbaar gedurende de laatste 5-10 dagen, afhankelijk van het advertentienetwerk. Indien nodig, echter, kan het team van de projectlancering gegevens voor maximaal de laatste 60 dagen terugwinnen.

## Gegevens van netwerkaccounts bewerken {#edit-account}

*de rekeningsmanager van het Agentschap, de rekeningsmanager van Adobe, en slechts de rollen van de beheerdergebruiker*

Als de verificatiegegevens van de account veranderen, wilt u de standaardparameters voor bijhouden van een account wijzigen. Als u activiteiten van een account wilt in- of uitschakelen, bewerkt u de accountgegevens.

>[!NOTE]
>
>Ga naar de website van het advertentienetwerk als u een werkelijke account op het advertentienetwerk wilt bewerken.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]** . Klik in het submenu op **[!UICONTROL Live]** \> **[!UICONTROL Accounts]** .

1. Houd de curseur over de rekeningsnaam, klik ![&#x200B; Meer &#x200B;](/help/search-social-commerce/assets/more-filters.png " "), en selecteer dan **[!UICONTROL Edit]**.

1. Bewerk de [&#x200B; rekeningsmontages &#x200B;](#account-settings):

   1. (Optioneel) Bewerk de accountgegevens.

   1. (Optioneel) Klik op **[!UICONTROL Set Account Tracking]** en bewerk de instellingen voor bijhouden.

1. Klik op **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >Zoeken, Sociaal en Commerce moeten de nieuwe accountgegevens synchroniseren met de gegevens op het advertentienetwerk. Dit gebeurt automatisch één keer per dag, of vaker wanneer Zoeken, Sociaal en Commerce wijzigingen op het advertentienetwerk detecteert.

## Tokens voor automatische toegang tot zoekaccounts vernieuwen {#refresh-oauth-tokens}

*de rekeningsmanager van het Agentschap, de rekeningsmanager van Adobe, en slechts de rollen van de beheerdergebruiker*

Als het Onderzoek, Sociaal, &amp; Commerce tot de rekening toegang heeft gebruikend het [&#x200B; OAuth vergunningsprotocol &#x200B;](https://oauth.net/2/) en de veranderingen van de rekeningsgeloofsbrieven, of als de extra toegang wordt vereist om nieuwe eigenschappen in Onderzoek, Sociale, &amp; Commerce te steunen, dan moet u een nieuw toegangstoken voor de rekening krijgen.

Uw Adobe-accountteam zal u informeren als voor nieuwe functies een nieuwe token nodig is.

1. (Als u bent aangemeld bij een andere account voor hetzelfde advertentienetwerk in dezelfde browsertoepassing) Afmelden bij een andere account dan die van de adverteerder.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]** . Klik in het submenu op **[!UICONTROL Live]** \> **[!UICONTROL Accounts]** .

1. Houd de curseur over de rekeningsnaam, klik ![&#x200B; Meer &#x200B;](/help/search-social-commerce/assets/more-filters.png " "), en selecteer dan **[!UICONTROL Edit]**.

1. Krijg een nieuw toegangstoken:

   1. Klik op **[!UICONTROL Get oAuth Token]**.

   1. (Als u niet bent aangemeld bij de account van de adverteerder) Meld u aan bij de advertentieaccount. De beste manier is om de referenties te gebruiken voor API-toegang tot de account.

   1. In het verzoek om toestemming/het toegangsscherm, klik de knoop om toestemming te bevestigen.

   1. Kopieer de verificatietekenreeks in het pop-upvenster dat wordt geopend en plak de tekenreeks in het veld **[!UICONTROL oAuth Token]** .

1. Klik op **[!UICONTROL Post]**.

## Enable or disable ad network accounts {#enable-disable-account}

*de rekeningsmanager van het Agentschap, de rekeningsmanager van Adobe, en slechts de rollen van de beheerdergebruiker*

Wanneer u een advertentienetwerkaccount inschakelt, synchroniseren Zoeken, Sociaal en Commerce campagnegegevens met de account (indien ondersteund) en worden geautomatiseerde biedingen en/of campagnebudgetten voor campagnes in portfolio&#39;s geactiveerd.Wanneer u een advertentienetwerkaccount uitschakelt, stopt Zoeken, Sociaal en Commerce alle activiteiten op de account. Gegevens die zijn verzameld terwijl de account actief was, worden nog opgeslagen, maar de weergaven en rapporten voor het campagnebeheer bevatten geen gegevens voor de periode waarin de account is uitgeschakeld. U kunt de account later weer inschakelen om de activiteiten met de account te hervatten.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]** . Klik in het submenu op **[!UICONTROL Live]** \> **[!UICONTROL Accounts]** .

1. Voer een van de volgende handelingen uit:

   * (Om de status voor één enkele rekening te veranderen) Houd de curseur over de rekeningsnaam, klik ![&#x200B; Meer &#x200B;](/help/search-social-commerce/assets/more-filters.png " "), en selecteer dan **[!UICONTROL Edit]**. Verander **[!UICONTROL Status]** in *Toegelaten* of *Gehandicapten*, en klik dan **[!UICONTROL Post]**.

   * (Ga als volgt te werk om de status van een of meer accounts te wijzigen:

      1. Schakel het selectievakje naast elke account in.

         Voor uiteinden bij het selecteren van veelvoudige rijen, zie &quot;[&#x200B; Uitgezochte veelvoudige rijen &#x200B;](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. In de toolbar boven de gegevenslijst, activeert de klik ![&#x200B; pictogram &#x200B;](/help/search-social-commerce/assets/activate.png " pictogram ") activeren om de rekening toe te laten of ![Pictogram uitschakelen](/help/search-social-commerce/assets/disable.png "Pictogram uitschakelen") om de rekening onbruikbaar te maken.

## Instellingen voor een netwerkaccount toevoegen {#account-settings}

>[!NOTE]
>
>Alleen accountmanager, [!DNL Adobe] accountmanager en beheerders kunnen accountinstellingen configureren.

### Accountgegevens

**[!UICONTROL SE Account ID]:** (Alle accounts behalve [!DNL Naver] - en [!DNL Yandex] -accounts; alleen bewerkbaar voor nieuwe accounts) De account-id die door het advertentienetwerk is toegewezen.

>[!NOTE]
>
>De rekeningen van de Adnetwork manager worden hier niet gesteund. Als u een beheerdersaccount wilt identificeren voor [!DNL Microsoft Advertising] of [!DNL Yandex] , gebruikt u respectievelijk het veld Hoofdaccount-id of MCC-account. Aan [&#x200B; opstellingsgeloofsbrieven voor de rekening van de a  [!DNL Google Ads]  manager &#x200B;](/help/search-social-commerce/admin/manager-accounts.md), ga [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** De naam die voor het account in Search, Social &amp; Commerce moet worden weergegeven.

>[!NOTE]
>
>Als u de integratie Zoeken, Sociaal en Commerce-Adobe Analytics hebt en de naam van de zoekaccount wijzigt, stuurt u een melding naar uw Adobe-accountteam zodat deze de toewijzing kan bijwerken.

**[!UICONTROL Login Details]: \[Login Type \]** - ([!DNL Microsoft Advertising]/ [!DNL Microsoft Merchant Center] slechts) of om logins aan de rekening toe te laten gebruikend:

* *[!UICONTROL oAuth]* (het gebrek): Om het [[!DNL OAuth]  vergunningsprotocol &#x200B;](https://oauth.net/2/) te gebruiken.

* *[!UICONTROL Password]:* om het wachtwoord van de cliënt te gebruiken.

Voor [!DNL Microsoft Advertising] -accounts kunnen alleen door [!DNL oAuth] geautoriseerde aanmeldingen worden gebruikt.

**[!UICONTROL Login Details]: [!UICONTROL Login]:** (Alle advertentienetwerken behalve [!DNL Naver]) De login naam of identiteitskaart om API toegang tot de rekening toe te laten.

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** ([!DNL Microsoft Advertising] [!DNL oAuth] - toegelaten en alle andere netwerken behalve [!DNL Meta] en [!DNL Yandex]) het teken van de rekening om logins toe te staan gebruikend het [[!DNL OAuth]  vergunningsprotocol &#x200B;](https://oauth.net/2/).

**[!UICONTROL Login Details]: [!UICONTROL Password]:** (Alle en netwerken behalve [!DNL Naver]) Het wachtwoord voor de account. Voor accounts waarvoor een wachtwoord is ingeschakeld op [!DNL Microsoft Advertising] , [!DNL Yahoo! Japan Ads] en [!DNL Yandex] , is dit veld vereist. Voor accounts waarvoor [!DNL oAuth] is ingeschakeld, is dit veld optioneel. Gebruik dit veld wanneer u het wachtwoord wilt versleutelen en opslaan, zodat accountbeheerders tokens naar behoefte kunnen vernieuwen.

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** ([!DNL Yandex] slechts rekeningen) de toegangssleutel voor de ontwikkelaarrekening die moet worden gebruikt.

**[!UICONTROL Currency]:** De afkorting van de valuta die voor de account wordt gebruikt. Dit veld kan worden bewerkt voor nieuwe [!DNL Naver] -accounts. Voor alle andere onderzoeksnetwerken, wordt de waarde automatisch gevuld met de munt die voor de rekening op het advertentienetwerk wordt gevormd zodra u sparen het verslag.

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] en [!DNL Microsoft Advertising] slechts rekeningen; facultatief) Om het even welke parameters om aan het eind van definitieve URLs aan spoorinformatie toe te voegen; omvat alle parameters die uw zaken moeten volgen.

Voorbeeld: `param1=value1&param2=value2`

Accounts die gebruikmaken van Adobe Advertising click tracking, moeten de klikidentificatie (`msclkid` for [!DNL Microsoft Advertising]; `gclid` for Google) van het advertentienetwerk in het achtervoegsel opnemen. Accounts met een Adobe Analytics-integratie moeten de parameter AMO ID gebruiken (te beginnen met `s_kwcid`). Als de account een AMO-id-implementatie aan de serverzijde heeft, wordt de parameter automatisch toegevoegd wanneer een gebruiker op een advertentie klikt; anders moet u deze hier handmatig toevoegen. Zie [&#x200B; vereiste achtervoegselformaten voor  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) en [&#x200B; vereiste achtervoegselformaten voor  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Dit veld wordt niet bijgewerkt met de instelling voor [!UICONTROL Auto Upload] bijhouden.
>* De laatste URL-achtervoegsels op lagere niveaus overschrijven het achtervoegsel op accountniveau. Gebruik voor een eenvoudiger onderhoud alleen het achtervoegsel op accountniveau, tenzij het bijhouden van wijzigingen voor afzonderlijke accountcomponenten nodig is. Om een achtervoegsel op het niveau van de advertentiegroep of lager te vormen, gebruik de redacteur van het advertentienetwerk.

**Tijdzone:** (Alle advertentienetwerken behalve [!DNL Baidu] en [!DNL Yahoo! Display Network]) de tijdzone van de adverteerder. Dit veld is bewerkbaar en optioneel voor nieuwe [!DNL Naver] -accounts. Voor alle andere zoeknetwerken wordt de waarde automatisch gevuld met de tijdzone die is geconfigureerd voor de account Zoeken, Sociaal en Commerce van de adverteerder wanneer u de record opslaat.

**Status:** de rekeningsstatus binnen Onderzoek, Sociale, &amp; Commerce:

* *Toegelaten:* Onderzoek, Sociale, &amp; Commerce synchroniseert campagnegegevens met de rekening (wanneer gesteund) en duwt geautomatiseerde biedingen en/of campagnebegrotingen voor campagnes in portefeuilles.
* *Gehandicapte:* Onderzoek, Sociale, &amp; Commerce houdt al activiteit op de rekening tegen. Gegevens die zijn verzameld terwijl de account actief was, worden nog opgeslagen, maar de weergaven en rapporten voor het campagnebeheer bevatten geen gegevens voor de periode waarin de account is gepauzeerd. U kunt het account later opnieuw activeren om de activiteiten met het account te hervatten.

**het Volgen Malplaatje** - ([!DNL Google Ads], [!DNL Microsoft Advertising], en [!DNL Yahoo! Japan Ads] slechts rekeningen; facultatief) het gebrek volgende malplaatje voor de rekening, die alle off-landing domeinomleidingen en het volgen parameters specificeert en ook definitieve/het landen pagina URL in een parameter inbedt. Voorbeeld: `{lpurl}?source={network}&id=5` of `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` om een omleiding op te nemen.

* De uiteindelijke URL insluiten:

   * ([!DNL Google Ads] en [!DNL Microsoft Advertising] slechts) voor een lijst van parameters om definitieve URLs in het volgen van malplaatjes te wijzen, zie ([!DNL Microsoft Advertising] slechts) [[!DNL Microsoft Advertising]  documentatie &#x200B;](https://help.ads.microsoft.com/#apex/3/en/56799) of ([!DNL Google Ads] slechts) de &quot;Volgend malplaatje slechts&quot;parameters in de sectie over &quot;Beschikbare [!DNL ValueTrack] Parameters&quot;in de [[!DNL Google Ads]  documentatie &#x200B;](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] slechts) gebruik de parameter `!{lpurl}` om op de het landen pagina URL te wijzen.

* U kunt optioneel URL-parameters en aangepaste parameters die voor de campagne zijn gedefinieerd, van elkaar scheiden door en-tekens (&amp;), zoals `{lpurl}?matchtype={matchtype}&device={device}` .

* U kunt desgewenst omleidingen en tekstspatiëring van derden toevoegen.

* Wanneer de campagnemontages &quot;[!UICONTROL EF Redirect]&quot;en &quot;[!UICONTROL Auto Upload] omvatten,&quot;Onderzoek, Sociale, &amp; Commerce vooraf bevestigt automatisch zijn eigen omleiding en het volgen code wanneer u sparen het verslag.

>[!NOTE]
>
>* Gebruik bij [!DNL Google Ads] geen macro&#39;s, die niet worden vervangen door klikken vanuit bronnen die parallelle tracering mogelijk maken. Als de adverteerder macro&#39;s moet gebruiken, moet het Adobe-accountteam samenwerken met Customer Support of het implementatieteam om deze toe te voegen.
>* De volgende sjabloon op het meest granulaire niveau overschrijft de waarden op alle hogere niveaus. Als zowel de accountinstellingen als de trefwoordinstellingen bijvoorbeeld een waarde bevatten, wordt de trefwoordwaarde toegepast.
>* Als u een trackingsjabloon bijwerkt op advertentie-, sitelink- of trefwoordniveau, worden de relevante advertenties opnieuw verzonden voor revisie. U kunt de trackingsjablonen op account-, campagne- of advertentieniveau bijwerken zonder uw advertenties opnieuw ter goedkeuring in te dienen.

**[!UICONTROL Master Account ID]:** ([!DNL Microsoft Advertising] slechts rekeningen) identiteitskaart voor een agentschap/beheersrekening verbonden aan de rekening.

**[!UICONTROL MCC Account]:** ([!DNL Yandex] slechts rekeningen; facultatief) een agentschap/beheersrekening verbonden aan de rekening. Om een bestaande vereniging te verwijderen, selecteer &quot;[!UICONTROL No MCC Account]&quot;.

**[!UICONTROL Application ID]:** ([!DNL Yandex] slechts rekeningen) het ontwikkelaarstoken voor de rekening te gebruiken. Voor alle [!DNL Yandex] -accounts wordt dezelfde token gebruikt.

**[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] rekeningen met Gedeelde die slechts plaatsen; facultatief) De numerieke identiteitskaart voor de campagne wordt gebruikt om voor alle advertentiecampagnes in de rekening te betalen die.

**[!UICONTROL Finance Token]:** ([!DNL Yandex] rekeningen met Gedeelde die slechts plaatst; facultatief) de ontwikkelaarstoken aan gebruik voor financiering-verwante API vraag, zoals voor het opnieuw toewijzen van geld uit de portemonnee tussen de campagnes van de adverteerder zonodig voor portefeuillestimalisatie.

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

**[!UICONTROL Track Product Group]:** (alleen voor [!UICONTROL EF Redirect] ) Niet geïmplementeerd

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **S_kwcid Formaat:** (Bestaande [!DNL Google Ads] rekeningen voor adverteerders met een integratie Adobe Advertising-Adobe Analytics en waarvoor AMO identiteitskaart (s_kwcid) niet reeds is gemigreerd)

Dit account gebruikt de oudere indeling voor de trackingcode van de AMO-id, waarmee Adobe Advertising gegevens over het account kan delen met Adobe Analytics. Het [&#x200B; recentste formaat &#x200B;](/help/integrations/analytics/ids.md#amo-id-formats) omvat parameters voor campagne identiteitskaart en identiteitskaart van de advertentiegroep, die noodzakelijk zijn om bij de campagne en ad groepsniveaus voor [!DNL Google Ads] prestaties te rapporteren maximum campagnes en concepten en experimentatiecampagnes in Analytics:

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

Als dit account op campagne- en advertentieniveau moet rapporteren, klikt u op het pictogram [!UICONTROL Edit] (potlood) en vervolgens **[!UICONTROL Migrate to new s_kwcid format]** om naar de nieuwe indeling te gaan. Voor accounts die deze typen campagnes niet bevatten, is het migreren naar de nieuwe indeling optioneel, maar aanbevolen.

Voor volledige instructies, zie &quot;[&#x200B; Update de het volgen code van identiteitskaart AMO voor a  [!DNL Google Ads]  rekening &#x200B;](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot;

**de Namen van de Reeks van het Rapport:** (voor EF richt slechts met teken; adverteerders met een integratie Adobe Advertising-Adobe Analytics; facultatief) één of meerdere Analytics- rapportsuites waaraan Onderzoek, Sociale, &amp; Commerce gegevens verzendt het van het advertentienetwerk, met inbegrip van entiteitclassificaties verzamelt en gegevens voor de rekening klikt. Deze functie is alleen beschikbaar voor ondersteunde advertentienetwerken.

Voor de gegevens om in de rapportreeksen te verschijnen, of (a) moet de server-zij eigenschap van identiteitskaart van AMO voor de rekening worden gevormd of (b) adverteerder-niveau dat aan &quot; [!UICONTROL Enable Advertising reporting in Analytics]&quot;plaatst wordt toegelaten. Daarnaast moet het account Analytics van de adverteerder zijn geconfigureerd voor het ontvangen van gegevens van Search, Social en Commerce. Neem voor meer informatie contact op met uw Adobe-accountteam.

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer ad netwerkrekeningen &#x200B;](ad-network-account-about.md)
>* [&#x200B; beheert commerciële centrumrekeningen &#x200B;](merchant-account-manage.md)
>* [&#x200B; Werk s_kwcid het volgen code voor a  [!DNL Google Ads]  rekening &#x200B;](update-amo-id-google.md) bij
