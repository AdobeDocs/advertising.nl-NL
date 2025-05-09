---
title: Vorm a [!DNL Google Analytics]  mening als gegevensbron
description: Leer hoe te om een gegevensbron van a  [!DNL Google Analytics]  mening te vormen.
role: User, Admin
exl-id: 9e299e42-4971-49ea-a515-54a97eb13e0d
feature: Search Admin, Search Data Sources
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# Een weergave [!DNL Google Analytics] configureren als gegevensbron

*de Beheerders van het Agentschap, de Managers van de Rekening van het Agentschap, de Managers van de Rekening van Adobe, en slechts Beheerders*

U kunt één gegevensbron per [!DNL Google Analytics] account, eigenschap en weergavecombinatie maken.

Als u metriek voor meerdere eigenschappen of voor meerdere weergaven voor één eigenschap wilt integreren, stelt u voor elke eigenschap een aparte gegevensbron in.

1. [ voer alle eerste vereisten aan het integreren van de  [!DNL Google Analytics]  rekening ](data-source-prerequisites.md) uit.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]** .

1. In de toolbar boven de gegevenslijst, leidt de klik ![ ](/help/search-social-commerce/assets/add.png " tot ").

1. Schakel in het dialoogvenster [!UICONTROL Deployment Prerequisites] het selectievakje in om te bevestigen dat de vereiste aangepaste afmeting &quot;ef_id&quot; is geïmplementeerd in de [!DNL Google Analytics] -account en klik vervolgens op **[!UICONTROL Continue]** .

   Sommige eerste vereisten kunnen door andere rollen in uw organisatie zijn uitgevoerd. Neem contact op met uw Adobe-accountteam als u vragen hebt over de voorwaarden.

1. Ga de [ montages van de gegevensbron ](data-source-settings.md) in:

   1. Ga als volgt te werk in de sectie **[!UICONTROL Connect to [!DNL Google Analytics]]** .

      1. Voer de numerieke id voor het [!DNL Google Analytics] -account in.

      1. Voer het e-mailadres in dat u wilt gebruiken voor toegang tot gegevens voor deze gegevensbron. Het e-mailadres moet zijn geregistreerd bij een [!DNL Google] -account en de machtiging &quot;Lezen en analyseren&quot; hebben voor de [!DNL Google Analytics] -account. Zie de [ instructies voor het toewijzen van gebruikerstoestemmingen in  [!DNL Google Analytics] ](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Meld u aan met een e-mailadres dat alleen toegang heeft tot die eigenschappen en weergaven, om ervoor te zorgen dat in Adobe Advertising alleen specifieke [!DNL Google Analytics] -eigenschappen en -weergaven beschikbaar zijn.

         >[!NOTE]
         >
         >Als u het wachtwoord voor deze e-mailaccount later wijzigt, worden alle open verbindingen met de e-mailaccount gesloten. Om synchroniserende gegevens te hervatten, terugkeer aan deze pagina en [ opnieuw voor authentiek verklaren ](data-source-reauthenticate.md).

      1. Schakel het selectievakje in om Adobe Advertising toegang te geven tot gegevens voor het account.

      1. Klik op **[!UICONTROL Authenticate]**.

   1. Geef in de sectie [!UICONTROL Account Details] de eigenschap en weergave op voor de metriek die u wilt importeren. Bovendien specificeer de douaneafmeting die met de waarde van de &quot;ef_id&quot;parameter van het vraagkoord wordt bevolkt.

   1. Geef in de sectie [!UICONTROL Import Metrics] de metriek op die u in de feed(s) wilt opnemen.

      U kunt [!UICONTROL Pageviews] , [!UICONTROL Sessions] , [!UICONTROL Bounces] of [!UICONTROL Session Duration] niet verwijderen. Deze worden automatisch opgenomen. U kunt tot 16 extra geldige metriek of metriek zonder gegevens toevoegen.

      >[!WARNING]
      >
      >[!DNL Google Analytics] staat maximaal 10 metriek toe in één gegevensfeed. Zoeken, Sociaal en Commerce kunnen maximaal twee feeds met een totaal van 20 metriek ondersteunen, maar met een tweede feed worden uw API-aanroepen verdubbeld tot [!DNL Google Analytics] . Als u veel metriek hebt, selecteer slechts de metriek die u in doelstellingen voor optimalisering wilt gebruiken. Zie meer over [ quota en vraaggrenzen voor API verzoeken aan  [!DNL Google Analytics] ](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. Voer in de sectie [!UICONTROL Metric Tag] de naam in van de tag die aan elke metrische waarde voor de gegevensbron moet worden toegevoegd.

1. Klik in de rechterbovenhoek op **[!UICONTROL Post]** .

   De gegevensbron krijgt de naam &quot;AccountName > PropertyName > ViewName&quot; en wordt automatisch geactiveerd. Om de gegevensbron te pauzeren, zie &quot;[ een voer van een Gegevens Source ](data-source-pause.md) pauzeren.&quot;

   De metriek zijn beschikbaar de volgende dag na voltooiing van de dagelijkse gegevenssynchronisatie, die om 05:00 in de tijdzone van de adverteerder begint. Zodra de metriek beschikbaar zijn, zijn zij zichtbaar in [[!UICONTROL Admin] > [!UICONTROL Conversions]](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md). Elke nieuwe metrische conversie wordt genoemd &quot;`ga:backEndMetricName_propertyID_viewID`,&quot;waar &quot;backEndMetricName&quot;de metrische naam is die door API wordt gebruikt. De weergavenaam voor elke nieuwe omzettingsmetrische waarde is &quot;`friendlyMetricName_ga:MetricTag`&quot;, waarbij &quot;FriedmetricName&quot; de metrische naam is die wordt weergegeven in [!DNL Google Analytics] en &quot;MetricTag&quot; is de [!UICONTROL Metric Tag] die is gedefinieerd in de gegevensbroninstellingen.

   U kunt de metriek aan campagnebeheer en portefeuillebeheermeningen, rapporten, en optimaliseringsdoelstellingen direct toevoegen.

>[!MORELIKETHIS]
>
>* [ Ongeveer synchroniserend  [!DNL Google Analytics]  omzettingsmetriek ](data-source-about.md)
>* [ Vereisten om a  [!DNL Google Analytics]  gegevensbron ](data-source-prerequisites.md) te vormen
>* [ geef a  [!DNL Google Analytics]  gegevensbron ](data-source-edit.md) uit
>* [ de synchronisatie van de pauze van een gegevensbron ](data-source-pause.md)
>* [ verklaart a  [!DNL Google Analytics]  gegevensbron ](data-source-reauthenticate.md) opnieuw voor authentiek
>* [[!DNL Google Analytics]  gegevensbronmontages ](data-source-settings.md)
>* [ Bijlage - Beschikbare  [!DNL Google Analytics]  metriek ](data-source-ga-metrics.md)
