---
title: (Nieuwe interface) Beheer en netwerkaccounts
description: Leer hoe u accountgegevens instelt en beheert in de nieuwe gebruikersinterface voor een advertentienetwerk dat is gesynchroniseerd via de API voor het advertentienetwerk.
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '2129'
ht-degree: 0%

---

# (Nieuwe interface) Beheer en netwerkaccounts via API-verbinding

<!-- Besides just logging into an account, do you have to make any other choices once you're logged in (such as to give speciic permissions to SSC?  And what about oAuth tokens -- do we still use them? -->

*eigenschap van Beta*

<!-- Move out info about Naver into a separate page -->

Hieronder vindt u instructies voor het beheer van advertentienetwerkaccounts waarmee Zoeken, Sociaal en Commerce worden gesynchroniseerd met de API van het advertentienetwerk.

<!-- Move out info about Naver into a separate page -->

Voor details over de functionaliteit beschikbaar voor elk advertentienetwerk, zie &quot;[ Gesteunde Inventaris ](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

## Gegevens van een advertentienetwerkaccount maken {#create-account}

Om het synchroniseren van een rekening toe te laten, moet u een overeenkomstig rekeningsverslag tot stand brengen dat de geloofsbrieven van de rekeningstoegang en het volgen opties bevat en met de status *toegelaten*.

>[!NOTE]
>
>Ga naar de website van het advertentienetwerk om een werkelijke account op het advertentienetwerk te maken.

1. Klik in het hoofdmenu op **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** .

1. Klik op **[!UICONTROL Create Account]**.

1. Klik op de naam van het advertentienetwerk en klik vervolgens op **[!UICONTROL Next]** .

1. (Alle advertentienetwerken behalve [!DNL Yandex] ) Meld u met de referenties aan bij het advertentienetwerk. Selecteer de optie Account tracking voor dit account. Klik vervolgens in de rechterbovenhoek op **[!UICONTROL Next]** .

1. Specificeer de [ rekeningsmontages ](#account-settings-api):

   1. Geef op het tabblad **[!UICONTROL Select Accounts]** de algemene accountinstellingen op. Geef voor [!DNL Yandex] -accounts de accountgegevens op.

   1. Klik op de tab **[!UICONTROL Setup Tracking]** en voer de instellingen voor bijhouden in.

   1. (Advertisers met een [[!DNL Adobe Analytics for Advertising]  integratie ](/help/integrations/analytics/overview.md)) klik het **[!UICONTROL Set up Adobe Analytics]** lusje, en selecteer alle [!DNL Analytics] rapporteringssuites voor het volgen en het melden van campagneactiviteit te gebruiken.

1. Klik op **[!UICONTROL Save]**.

   Recente kosten en klik op gegevens voor alle campagnes in de account worden per uur bijgewerkt in Zoeken, Sociaal en Commerce. Standaard zijn gegevens beschikbaar gedurende de laatste 5-10 dagen, afhankelijk van het advertentienetwerk. Indien nodig, echter, kan het team van de projectlancering gegevens voor maximaal de laatste 60 dagen terugwinnen.

## Gegevens van netwerkaccounts bewerken {#edit-account}

Als u de accountinstellingen opnieuw wilt verifiëren om de verbinding te vernieuwen of machtigingen bij te werken, activiteit op een account in- of uit te schakelen, de standaardparameters voor bijhouden in een account te wijzigen of de rapportsuites van [!DNL Analytics] te wijzigen voor het bijhouden en rapporteren, bewerkt u vervolgens de accountgegevens.

>[!NOTE]
>
>Ga naar de website van het advertentienetwerk als u een werkelijke account op het advertentienetwerk wilt bewerken.

1. Klik in het hoofdmenu op **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** .

1. Selecteer de account op een van de volgende manieren:

   * Schakel het selectievakje naast de accountnaam in en klik op **[!UICONTROL Edit]** op de werkbalk voor bulkacties.

   * Plaats de cursor boven de accountnaam, klik op **..** en klik vervolgens op **[!UICONTROL Edit]** .

1. Bewerk de [ rekeningsmontages ](#account-settings-api):

   1. (Optioneel) Bewerk op het tabblad **[!UICONTROL Account Details]** de accountgegevens.

   1. (Optioneel) Klik op het tabblad **[!UICONTROL Setup Tracking]** en bewerk de instellingen voor bijhouden.

   1. (Facultatief; adverteerders met een [[!DNL Adobe Analytics for Advertising]  integratie ](/help/integrations/analytics/overview.md)) klik het **[!UICONTROL Set up Adobe Analytics]** lusje, en geef [!DNL Analytics] rapporteringssuites uit voor het volgen en het melden van campagneactiviteit te gebruiken.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Klik op **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Zoeken, Sociaal en Commerce moeten de nieuwe accountgegevens synchroniseren met de gegevens op het advertentienetwerk. Dit gebeurt automatisch één keer per dag, of vaker wanneer Zoeken, Sociaal en Commerce wijzigingen op het advertentienetwerk detecteert.

## Een advertentienetwerkaccount opnieuw verifiëren {#reauthenticate}

Als u de netwerkverbinding voor de advertentie wilt vernieuwen of de machtigingen voor de account wilt bijwerken, moet u de account opnieuw verifiëren.

1. (Als u bent aangemeld bij een andere account voor hetzelfde advertentienetwerk in dezelfde browsertoepassing) Afmelden bij een andere account dan die van de adverteerder.

1. Klik in het hoofdmenu op **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** .

<!-- For Bing and Yandex, the right-click menu includes "Re authenticate." Clarify why just those types -->

1. Selecteer de account op een van de volgende manieren:

   * Schakel het selectievakje naast de accountnaam in en klik op **[!UICONTROL Edit]** op de werkbalk voor bulkacties.

   * Plaats de cursor boven de accountnaam, klik op **..** en klik vervolgens op **[!UICONTROL Edit]** .

1. Klik op het tabblad **[!UICONTROL Account Details]** op **[!UICONTROL Re authenticate]** en meld u met de referenties aan bij het advertentienetwerk.

1. Klik op **[!UICONTROL Save]**.

## Enable or disable ad network accounts {#enable-disable-account}

Wanneer u een advertentienetwerkaccount inschakelt, synchroniseren Zoeken, Sociaal en Commerce campagnegegevens met de account (indien ondersteund) en worden geautomatiseerde biedingen en/of campagnebudgetten voor campagnes in portfolio&#39;s geactiveerd. Wanneer u een advertentienetwerkaccount uitschakelt, stopt Search, Social en Commerce alle activiteiten op de account. Gegevens die zijn verzameld terwijl de account actief was, worden nog opgeslagen, maar de weergaven en rapporten voor het campagnebeheer bevatten geen gegevens voor de periode waarin de account is uitgeschakeld. U kunt de account later weer inschakelen om de activiteiten met de account te hervatten.

1. Klik in het hoofdmenu op **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** .

1. Voer een van de volgende handelingen uit:

   * (Vanuit de [!UICONTROL Accounts] -weergave):

      * (Als u de account wilt inschakelen) Schakel het selectievakje naast de accountnaam in en klik op **[!UICONTROL Activate]** op de werkbalk voor bulkacties.

      * (Als u de account wilt uitschakelen) Schakel het selectievakje naast de accountnaam in en klik op **[!UICONTROL Pause]** op de werkbalk voor bulkacties.

   * (Uit de accountinstellingen):

      1. Selecteer de account op een van de volgende manieren:

         * Plaats de cursor boven de accountnaam, klik op **..** en klik vervolgens op **[!UICONTROL Edit]** .

         * Schakel het selectievakje naast de accountnaam in en klik op **[!UICONTROL Edit]** op de werkbalk voor bulkacties.

      1. Schakel **[!UICONTROL Account Details]** uit op de tab **[!UICONTROL Account enabled]** .

      1. Klik op **[!UICONTROL Save]**.

## Instellingen voor een netwerkaccount toevoegen {#account-settings-api}

De accountinstellingen variëren per advertentienetwerk. Mogelijk ziet u niet alle onderstaande instellingen.

<!-- When you're creating new accounts only; not sure that you'll have anything to do here once you've authenticated

### Authenticate tab

-->

### [!UICONTROL Select Accounts]/[!UICONTROL Account Details] tab

**[!UICONTROL Account Name]:** De naam die voor het account in Search, Social &amp; Commerce moet worden weergegeven.

>[!NOTE]
>
>Als u een integratie hebt met Zoeken, Sociaal en Commerce-Adobe Analytics en de naam van de zoekaccount wilt wijzigen, vraagt u uw Adobe-accountteam om de toewijzing bij te werken.

**[!DNL [ Advertentienetwerk ] Rekeningen]:** (Zichtbaar terwijl u een rekening creeert) De rekening van het advertentienetwerk aan synchronisatie.

**[Login Details ]:** (de rekeningen van Yandex slechts) de te gebruiken rekeningsgeloofsbrieven:

* **[!UICONTROL Login]:** De aanmeldnaam of -id waarmee API-toegang tot de account wordt ingeschakeld.

* **[!UICONTROL Password]:** Het wachtwoord voor de account.

* **[!UICONTROL Access Key]:** De toegangstoets voor de ontwikkelaarsaccount die moet worden gebruikt.

* **[!UICONTROL Application ID]:** Het ontwikkelaarstoken voor de rekening te gebruiken. Voor alle [!DNL Yandex] -accounts wordt dezelfde token gebruikt.

* **[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] rekeningen met Gedeelde die slechts plaatsen; facultatief) De numerieke identiteitskaart voor de campagne wordt gebruikt om voor alle advertentiecampagnes in de rekening te betalen die.

* **[!UICONTROL Finance Token]:** ([!DNL Yandex] rekeningen met Gedeelde die slechts plaatst; facultatief) de ontwikkelaarstoken aan gebruik voor financiering-verwante API vraag, zoals voor het opnieuw toewijzen van geld uit de portemonnee tussen de campagnes van de adverteerder zonodig voor portefeuillestimalisatie.

**[!UICONTROL Network Account ID]:** (Alle advertentienetwerken behalve [!DNL Yandex] De account-id die door het advertentienetwerk wordt toegewezen.

>[!NOTE]
>
>De rekeningen van de Adnetwork manager worden hier niet gesteund. Als u een beheerdersaccount voor [!DNL Microsoft Advertising] wilt identificeren, gebruikt u respectievelijk het veld Hoofdaccount-id of MCC-account. Aan [ opstellingsgeloofsbrieven voor de rekening van de a  [!DNL Google Ads]  manager ](/help/search-social-commerce/admin/manager-accounts.md), ga [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Currency]:** (Alleen-lezen) De afkorting van de valuta die voor de account wordt gebruikt. Deze waarde wordt automatisch gevuld met de valuta die voor de account op het advertentienetwerk is geconfigureerd als u de record opslaat.

**[!UICONTROL Time Zone]:** De tijdzone van de adverteerder. Deze waarde wordt automatisch gevuld met de tijdzone die is geconfigureerd voor de account van de adverteerder Search, Social en Commerce nadat u de record hebt opgeslagen.

**[!UICONTROL Login]:** (Alleen-lezen) De gebruikersaccount die wordt gebruikt om u aan te melden bij de account.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** zoek-, sociale en Commerce synchroniseert campagnegegevens met de account (indien ondersteund) en plaatst automatische biedingen en/of campagnebudgetten voor campagnes in portfolio&#39;s.

## [!UICONTROL Setup Tracking] tab

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]:** of het bijhouden van wijzigingen moet worden ingeschakeld, gebruikt de service voor het bijhouden van Adobe Advertising-conversies. Met deze methode worden unieke id&#39;s voor het bijhouden van klikken gegenereerd en worden gebruikers doorgestuurd naar de Adobe Advertising-server voor traceringsdoeleinden voordat ze naar de landingspagina van de client worden verzonden. Deze methode heeft standaardopties voor bijhouden die u naar keuze kunt aanpassen en u kunt ook parameters opgeven die aan elke URL moeten worden toegevoegd.

Om deze eigenschap toe te laten, zet **[het Volgen]** toe.

>[!NOTE]
>
>* Als u deze instelling wijzigt, moet u de URL&#39;s voor het bijhouden van een account opnieuw genereren.
>* De opties voor bijhouden op campagnereniveau hebben voorrang op instellingen op accountniveau.

**[!UICONTROL Tracking Type]:** (Wanneer Zoeken, Sociaal, &amp; het volgen van Commerce wordt toegelaten) de methode om eind - gebruikers aan definitieve URL of bestemmingsURL om te leiden. De geselecteerde optie is van toepassing op alle biedingseenheden in de account of campagne. De standaardinstelling op accountniveau wordt overgenomen van de instellingen voor bijhouden van adverteerders en de standaardinstelling op campagneniveau wordt overgenomen van de accountinstellingen.

* *[!UICONTROL Standard]:* enkel de eindgebruiker aan gespecificeerde URL om te leiden.

* *[!UICONTROL Token]:* om de eindgebruiker aan URL om te leiden en ook onderzoek te registreren, sociaal, &amp; identiteitskaart van Commerce voor de klik (`ef_id`) als parameter van het vraagkoord, die als teken wordt gebruikt. Kies deze optie als u offlinetransacties rapporteert, Zoeken, Sociaal en Commerce gegevens wilt uitwisselen met Adobe Analytics of als u alle conversies wilt bijhouden die plaatsvinden in [!DNL Apple Safari] -browsers.

>[!NOTE]
>
>* Als u schakelt van [!UICONTROL Standard] naar [!UICONTROL Token] of vice versa, moet u URL&#39;s voor het bijhouden van een account opnieuw genereren.
>* U kunt de instelling op accountniveau op campagneniveau overschrijven.

**[!UICONTROL Auto Update]:** (Wanneer Zoeken, Sociaal, &amp; het volgen van Commerce wordt toegelaten) normaliseert uw het volgen URLs voor verenigbaarheid over browsers en servers. Met Zoeken, Sociaal en Commerce wordt het volgende automatisch naar het advertentienetwerk geüpload tijdens de volgende synchronisatie: a) parameters voor het bijhouden van sjablonen zoeken, Sociaal en Commerce en dezelfde parameters die aan de uiteindelijke URL&#39;s zijn toegevoegd, of b) nieuwe doel-URL&#39;s die zijn ingesloten met code voor het bijhouden van zoekopdrachten, sociale gegevens en Commerce. Voor adverteerders met een [ Adobe Advertising-Adobe Analytics integratie ](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) en een server-kantAMO identiteitskaart (s_kwcid) configuratie, omvat de upload ook [ parameters van identiteitskaart van AMO ](/help/integrations/analytics/ids.md#amo-id) voor uw [!DNL Google Ads] en [!DNL Microsoft Advertising] rekeningen. De standaardinstelling op accountniveau wordt overgenomen van de instellingen voor bijhouden van adverteerders. U kunt de instelling op accountniveau op campagneniveau overschrijven.

URL&#39;s bijhouden wordt dagelijks alleen bijgewerkt voor entiteiten die niet meer gesynchroniseerd zijn (dat wil zeggen nieuwe entiteiten die zijn toegevoegd en bestaande entiteiten waarvan de eigenschappen zijn gewijzigd). Als u deze instelling wijzigt van uitgeschakeld in ingeschakeld voor een bestaande adverteerder/account/campagne, worden URL&#39;s die worden bijgehouden niet bijgewerkt voor bestaande entiteiten die al gesynchroniseerd zijn. Als u de URL&#39;s van bestaande, synchrone entiteiten wilt bijhouden, neemt u contact op met uw Adobe-accountteam en vraagt u een eenmalig, handmatig synchronisatieproces. Het automatische uploadproces zal toekomstige veranderingen behandelen.

**[!UICONTROL URL Encoding]:** (Wanneer Zoeken, Sociaal en Commerce bijhouden is ingeschakeld; accounts met alleen doel-URL&#39;s) Codeert de basis-URL binnen de adresbalk van de browser van de eindgebruiker (zoals `%3D` in plaats van `=`):

**[!UICONTROL Tracking Level]:** (Wanneer Zoeken, Sociaal, &amp; het volgen van Commerce wordt toegelaten; beschikbaar op de rekening en campagnemaniveaus; niet van toepassing op advertentienetwerken die voor parallelle het volgen worden toegelaten) het niveau waarop klikken en opbrengst door een omleiding (indien relevant) toe te voegen en parameters aan relevante URLs toe te voegen:

* *[!UICONTROL Keyword]:* om gegevens op slechts het sleutelwoordniveau te volgen. Niet beschikbaar voor [!DNL Yandex].

* *[!UICONTROL Ad]:* om gegevens op slechts het advertentieniveau te volgen. Niet beschikbaar voor [!DNL Naver].

* *[!UICONTROL Keyword and Ad]:* om gegevens bij zowel het sleutelwoord als de advertentieniveaus te volgen. Niet beschikbaar voor [!DNL Naver] en [!DNL Yandex] .

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] en [!DNL Microsoft Advertising] slechts rekeningen; facultatief) Om het even welke parameters om aan het eind van definitieve URLs aan spoorinformatie toe te voegen; omvat alle parameters die uw zaken moeten volgen.

Voorbeeld: `param1=value1&param2=value2`

Accounts die gebruikmaken van Adobe Advertising click tracking, moeten de klikidentificatie (`msclkid` for [!DNL Microsoft Advertising]; `gclid` for Google) van het advertentienetwerk in het achtervoegsel opnemen. Accounts met een Adobe Analytics-integratie moeten de parameter AMO ID gebruiken (te beginnen met `s_kwcid`). Als de account een AMO-id-implementatie aan de serverzijde heeft, wordt de parameter automatisch toegevoegd wanneer een gebruiker op een advertentie klikt; anders moet u deze hier handmatig toevoegen. Zie [ vereiste achtervoegselformaten voor  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) en [ vereiste achtervoegselformaten voor  [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Dit veld wordt niet bijgewerkt met de instelling voor [!UICONTROL Auto Update] bijhouden.
>* De laatste URL-achtervoegsels op lagere niveaus overschrijven het achtervoegsel op accountniveau. Gebruik voor een eenvoudiger onderhoud alleen het achtervoegsel op accountniveau, tenzij het bijhouden van wijzigingen voor afzonderlijke accountcomponenten nodig is. Om een achtervoegsel op het niveau van de advertentiegroep of lager te vormen, gebruik de redacteur van het advertentienetwerk.

**het Volgen van de Rekening URL**: ([!DNL Google Ads], [!DNL Microsoft Advertising], en [!DNL Yahoo! Japan Ads] slechts rekeningen; facultatief) het gebrek volgende malplaatje voor de rekening, die alle off-landing domein herleidt en het volgen parameters specificeert en ook definitieve/het landen pagina URL in een parameter inbedt. Voorbeeld: `{lpurl}?source={network}&id=5` of `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` om een omleiding op te nemen.

* De uiteindelijke URL insluiten:

   * ([!DNL Google Ads] en [!DNL Microsoft Advertising] slechts) voor een lijst van parameters om definitieve URLs in het volgen van malplaatjes te wijzen, zie ([!DNL Microsoft Advertising] slechts) [[!DNL Microsoft Advertising]  documentatie ](https://help.ads.microsoft.com/#apex/3/en/56799) of ([!DNL Google Ads] slechts) de &quot;Volgend malplaatje slechts&quot;parameters in de sectie over &quot;Beschikbare [!DNL ValueTrack] Parameters&quot;in de [[!DNL Google Ads]  documentatie ](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] slechts) gebruik de parameter `!{lpurl}` om op de het landen pagina URL te wijzen.

* U kunt optioneel URL-parameters en aangepaste parameters die voor de campagne zijn gedefinieerd, van elkaar scheiden door en-tekens (&amp;), zoals `{lpurl}?matchtype={matchtype}&device={device}` .

* U kunt desgewenst omleidingen en tekstspatiëring van derden toevoegen.

* Wanneer de campagnemontages &quot;[!UICONTROL EF Redirect]&quot;en &quot;[!UICONTROL Auto Upload] omvatten,&quot;Onderzoek, Sociale, &amp; Commerce vooraf bevestigt automatisch zijn eigen omleiding en het volgen code wanneer u sparen het verslag.

>[!NOTE]
>
>* Gebruik bij [!DNL Google Ads] geen macro&#39;s, die niet worden vervangen door klikken vanuit bronnen die parallelle tracering mogelijk maken. Als de adverteerder macro&#39;s moet gebruiken, moet het Adobe-accountteam samenwerken met Customer Support of het implementatieteam om deze toe te voegen.
>* De volgende sjabloon op het meest granulaire niveau overschrijft de waarden op alle hogere niveaus. Als zowel de accountinstellingen als de trefwoordinstellingen bijvoorbeeld een waarde bevatten, wordt de trefwoordwaarde toegepast.
>* Als u een trackingsjabloon bijwerkt op advertentie-, sitelink- of trefwoordniveau, worden de relevante advertenties opnieuw verzonden voor revisie. U kunt de trackingsjablonen op account-, campagne- of advertentieniveau bijwerken zonder uw advertenties opnieuw ter goedkeuring in te dienen.

## [!UICONTROL Setup Analytics] tab

**[!UICONTROL Adobe Analytics Report Suite]:** (Advertisers met een [[!DNL Adobe Analytics for Advertising]  integratie ](/help/integrations/analytics/overview.md); facultatief) één of meerdere het rapportreeksen van Analytics waaraan Onderzoek, Sociale, &amp; Commerce gegevens verzendt het van het advertentienetwerk, met inbegrip van entiteitclassificaties en gegevens voor de rekening klikt. Deze functie is alleen beschikbaar voor ondersteunde advertentienetwerken.

Voor de gegevens om in de rapportreeksen te verschijnen, of (a) moet de server-zij eigenschap van identiteitskaart van AMO voor de rekening worden gevormd of (b) adverteerder-niveau dat aan &quot; [!UICONTROL Enable Advertising reporting in Analytics]&quot;plaatst wordt toegelaten. Daarnaast moet het [!DNL Analytics] -account van de adverteerder zijn geconfigureerd voor het ontvangen van gegevens van Search, Social en Commerce. Neem voor meer informatie contact op met uw Adobe-accountteam.

>[!MORELIKETHIS]
>
>* [ Ongeveer ad netwerkrekeningen ](../ad-network-account-about.md)
>* [ beheert commerciële centrumrekeningen ](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
>* [ Werk s_kwcid het volgen code voor a  [!DNL Google Ads]  rekening ](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md) bij
