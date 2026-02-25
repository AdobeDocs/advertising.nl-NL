---
title: (Nieuwe UI) beheert  [!DNL Naver]  rekeningen slechts voor het volgen
description: Leer hoe te opstelling en rekeningsdetails in nieuwe UI voor a  [!DNL Naver]  rekening te beheren.
feature: Search Campaign Management
source-git-commit: 0de2a01905727314ca6c0792c5efaf6450548293
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# (Nieuwe gebruikersinterface) [!DNL Naver] Alleen accounts beheren voor tracering

*eigenschap van Beta*

Na zijn instructies voor het beheren van [[!DNL Naver]  rekeningen ](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md) om prestaties voor de advertenties te volgen, te rapporteren en te visualiseren die u direct van het advertentienetwerk koopt. Zoeken, sociale media en Commerce synchroniseren geen gegevens met het advertentienetwerk, bieden geen geautomatiseerde biedingen en bieden geen optimalisatie of simulaties.

Voor details over de beschikbare functionaliteit, zie &quot;[ Gesteunde Inventaris ](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

## Gegevens van een advertentienetwerkaccount maken {#create-account}

Om het volgen van een rekening toe te laten, moet u een overeenkomstig rekeningsverslag tot stand brengen dat de geloofsbrieven van de rekeningstoegang bevat en met de status *toegelaten*.

>[!NOTE]
>
>Ga naar de website van het advertentienetwerk om een werkelijke account op het advertentienetwerk te maken.

1. Klik in het hoofdmenu op **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** .

1. Klik op **[!UICONTROL Create Account]**.

1. Klik op de naam van het advertentienetwerk en klik vervolgens op **[!UICONTROL Next]** .

1. Specificeer de [ rekeningsmontages ](#account-settings-naver):

   1. Geef op het tabblad **[!UICONTROL Enter Account Details]** de algemene accountinstellingen op.

   1. (Advertisers met een [[!DNL Adobe Analytics for Advertising]  integratie ](/help/integrations/analytics/overview.md)) klik het **[!UICONTROL Set up Adobe Analytics]** lusje, en selecteer alle [!DNL Analytics] rapporteringssuites voor het volgen en het melden van campagneactiviteit te gebruiken.

1. Klik op **[!UICONTROL Save]**.

## Gegevens van netwerkaccounts bewerken {#edit-account}

Als u de accountnaam wilt wijzigen, de accountstatus wilt wijzigen of de [!DNL Analytics] -rapportsuites wilt wijzigen voor het bijhouden en rapporteren, bewerkt u de accountgegevens.

>[!NOTE]
>
>Ga naar de website van het advertentienetwerk als u een werkelijke account op het advertentienetwerk wilt bewerken.

1. Klik in het hoofdmenu op **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** .

1. Selecteer de account op een van de volgende manieren:

   * Schakel het selectievakje naast de accountnaam in en klik op **[!UICONTROL Edit]** op de werkbalk voor bulkacties.

   * Plaats de cursor boven de accountnaam, klik op **..** en klik vervolgens op **[!UICONTROL Edit]** .

1. Bewerk de [ rekeningsmontages ](#account-settings-api):

   1. (Optioneel) Bewerk op het tabblad **[!UICONTROL Account Details]** de accountgegevens.

   1. (Facultatief; adverteerders met een [[!DNL Adobe Analytics for Advertising]  integratie ](/help/integrations/analytics/overview.md)) klik het **[!UICONTROL Set up Adobe Analytics]** lusje, en geef [!DNL Analytics] rapporteringssuites uit voor het volgen en het melden van campagneactiviteit te gebruiken.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Klik op **[!UICONTROL Save]**.

<!-- What does this do?

## Enable or disable ad network accounts {#enable-disable-account}

When you enable an ad network account, Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios. When you disable an ad network account, Search, Social, & Commerce stops all activity on the account. Data collected while the account was active is still stored, but the campaign management views and reports don't include data for the time period in which the account is disabled. You can later re-enable the account to resume activity with the account.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Do either of the following:

   * (From the [!UICONTROL Accounts] view):

     * (To enable the account) Select the check box next to the account name, and then click **[!UICONTROL Activate]** in the bulk actions toolbar.

     * (To disable the account) Select the check box next to the account name, and then click **[!UICONTROL Pause]** in the bulk actions toolbar.

   * (From the account settings):
   
     1. Select the account in either of the following ways:
     
        * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.
        
        * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.
        
     1. On the **[!UICONTROL Account Details]** tab, turn off **[!UICONTROL Account enabled]**.

     1. Click **[!UICONTROL Save]**.

-->

## Instellingen voor een netwerkaccount toevoegen {#account-settings-api}

### [!UICONTROL Account Details] tab

#### [!UICONTROL Enter Account Details]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** De naam die voor het account in Search, Social &amp; Commerce moet worden weergegeven.

>[!NOTE]
>
>Als u een integratie hebt met Zoeken, Sociaal en Commerce-Adobe Analytics en de naam van de zoekaccount wilt wijzigen, vraagt u uw Adobe-accountteam om de toewijzing bij te werken.

**[!UICONTROL Network Account ID]:** De account-id die door het advertentienetwerk is toegewezen.

**[!UICONTROL Currency]:** De afkorting van de valuta die voor de account wordt gebruikt.

**[!UICONTROL Time Zone]:** De tijdzone van de adverteerder.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** zoek-, sociale en Commerce synchroniseert campagnegegevens met de account (indien ondersteund) en plaatst automatische biedingen en/of campagnebudgetten voor campagnes in portfolio&#39;s.

## [!UICONTROL Setup Analytics] tab

**[!UICONTROL Adobe Analytics Report Suite]:** (Advertisers met een [[!DNL Adobe Analytics for Advertising]  integratie ](/help/integrations/analytics/overview.md); facultatief) Één of meerdere het rapportreeksen van Analytics waaraan Onderzoek, Sociale, &amp; Commerce gegevens verzendt u voor het advertentienetwerk, met inbegrip van entiteitclassificaties uploadt en gegevens voor de rekening klikt.

Voor de gegevens om in de rapportreeksen te verschijnen, of (a) moet de server-zij eigenschap van identiteitskaart van AMO voor de rekening worden gevormd of (b) adverteerder-niveau dat aan &quot; [!UICONTROL Enable Advertising reporting in Analytics]&quot;plaatst wordt toegelaten. Daarnaast moet het [!DNL Analytics] -account van de adverteerder zijn geconfigureerd voor het ontvangen van gegevens van Search, Social en Commerce. Neem voor meer informatie contact op met uw Adobe-accountteam.

>[!MORELIKETHIS]
>
>* [ voert  [!DNL Naver]  het volgen-slechts rekeningen ](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md) uit
>* [ Ongeveer ad netwerkrekeningen ](/help/search-social-commerce/new-ui/set-up/accounts/ad-network-account-about.md)
