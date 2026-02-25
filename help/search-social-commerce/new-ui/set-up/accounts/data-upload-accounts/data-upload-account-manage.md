---
title: Netwerkaccounts configureren voor het uploaden van gegevens
description: Leer hoe u accountdetails voor een advertentienetwerkaccount instelt en beheert.
feature: Search Campaign Management
exl-id: 7e8fb475-21f9-446b-a112-e0f27a4c4172
source-git-commit: 00565a6c9e784472fab9c9d223c83b0c7cbb91b1
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Beheer en netwerkaccounts voor het uploaden van gegevens

<!-- Edit all, including title and metadata -->

Hieronder vindt u instructies voor het beheren van accountgegevens voor advertentienetwerkaccounts waarvoor u de accountgegevens uploadt.

Voor details over de functionaliteit beschikbaar voor elk advertentienetwerk, zie &quot;[ Gesteunde Inventaris ](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

>[!NOTE]
>
>Voor instructies over het beheren van rekeningsdetails voor een advertentienetwerkrekening die Onderzoek, Sociale, &amp; Commerce syncs gebruikend API van het advertentienetwerk, zie &quot;[ leiden en netwerkrekeningen via API verbinding ](../api-accounts/api-account-manage.md)&quot; in plaats daarvan.

## Accountdetails maken {#create-account}

1. Klik op **[!UICONTROL Create Account]**.

1. Klik op de naam van het advertentienetwerk en klik vervolgens op **[!UICONTROL Next]** .

1. Specificeer de [ rekeningsmontages ](#account-settings):

   1. Bewerk op het tabblad **[!UICONTROL Account Details]** de accountgegevens.

   1. (Advertisers met een [[!DNL Adobe Analytics for Advertising]  integratie ](/help/integrations/analytics/overview.md)) klik het **[!UICONTROL Set up Adobe Analytics]** lusje, en geef [!DNL Analytics] rapporteringssuites uit voor het volgen en het melden van campagneactiviteit te gebruiken.

   1. (Optioneel) Upload op het tabblad **[!UICONTROL Upload File]** gegevensbestanden voor de account.

1. Klik op **[!UICONTROL Save]**.

## Accountdetails bewerken {#edit-account}

1. Klik in het hoofdmenu op **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]** .

1. Selecteer de account op een van de volgende manieren:

   * Schakel het selectievakje naast de accountnaam in en klik op **[!UICONTROL Edit]** op de werkbalk voor bulkacties.

   * Plaats de cursor boven de accountnaam, klik op **..** en klik vervolgens op **[!UICONTROL Edit]** .

1. Bewerk de [ rekeningsmontages ](#account-settings-upload):

   1. (Optioneel) Bewerk op het tabblad **[!UICONTROL Account Details]** de accountgegevens.

   1. (Facultatief; adverteerders met een [[!DNL Adobe Analytics for Advertising]  integratie ](/help/integrations/analytics/overview.md)) klik het **[!UICONTROL Set up Adobe Analytics]** lusje, en geef [!DNL Analytics] rapporteringssuites uit voor het volgen en het melden van campagneactiviteit te gebruiken.

   1. (Optioneel) Upload op het tabblad **[!UICONTROL Upload File]** gegevensbestanden voor de account.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Klik op **[!UICONTROL Save]**.

## Enable or disable ad network accounts {#enable-disable-account}

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

## Accountinstellingen {#account-settings-upload}

### [!UICONTROL Account Details] tab

**[!UICONTROL Account Name]:** De naam die voor het account in Search, Social &amp; Commerce moet worden weergegeven.

>[!NOTE]
>
>Als u de integratie Zoeken, Sociaal en Commerce-Adobe Analytics hebt en de naam van de zoekaccount wijzigt, stuurt u een melding naar uw Adobe-accountteam zodat deze de toewijzing kan bijwerken.

**[!UICONTROL Network Account ID]:** De account-id die door het advertentienetwerk is toegewezen. Deze id wordt alleen gebruikt voor rapportage. Zoeken, Sociaal en Commerce maken geen rechtstreeks verbinding met de netwerkaccount van de advertentie.

**[!UICONTROL Currency]:** (Alleen-lezen voor bestaande accounts) De afkorting van de valuta die voor de account wordt gebruikt.

**[!UICONTROL Time Zone]:** (Alleen-lezen voor bestaande accounts) De tijdzone van de adverteerder.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Met Zoeken, Sociaal en Commerce kunnen gegevens automatisch worden opgehaald voor een opgegeven S3-emmertje.

## [!UICONTROL Setup Analytics] tab

**[!UICONTROL Adobe Analytics Report Suite]:** (Advertisers met een [[!DNL Adobe Analytics for Advertising]  integratie ](/help/integrations/analytics/overview.md); facultatief) Één of meerdere het rapportreeksen van Analytics waaraan Onderzoek, Sociale, &amp; Commerce gegevens verzendt u voor het advertentienetwerk, met inbegrip van entiteitclassificaties uploadt en gegevens voor de rekening klikt.

Voor de gegevens om in de rapportreeksen te verschijnen, of (a) moet de server-zij eigenschap van identiteitskaart van AMO voor de rekening worden gevormd of (b) adverteerder-niveau dat aan &quot; [!UICONTROL Enable Advertising reporting in Analytics]&quot;plaatst wordt toegelaten. Daarnaast moet het [!DNL Analytics] -account van de adverteerder zijn geconfigureerd voor het ontvangen van gegevens van Search, Social en Commerce. Neem voor meer informatie contact op met uw Adobe-accountteam.

### [!UICONTROL Upload File] tab

(Optioneel) Upload gegevensbestanden voor de account.<!-- For instructions, see "[Upload offline account data for reporting and simulations](upload-account-data.md)." -->
