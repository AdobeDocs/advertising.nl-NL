---
title: Een [!DNL Google Analytics] weergeven als gegevensbron
description: Leer hoe te om een gegevensbron van een te vormen [!DNL Google Analytics] weergeven.
role: User, Admin
exl-id: 583cf9aa-861c-4faf-a707-1def4e983b93
feature: Search Admin, Search Data Sources
source-git-commit: f21283731d7a1830af585cec43805c54c81c72ff
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# Een [!DNL Google Analytics] weergeven als gegevensbron

*Beheerders van agentschappen, accountmanagers van het Bureau, accountmanagers van Adobe en alleen beheerders*

U kunt per [!DNL Google Analytics] account, eigenschap en weergavecombinatie.

Als u metriek voor meerdere eigenschappen of voor meerdere weergaven voor één eigenschap wilt integreren, stelt u voor elke eigenschap een aparte gegevensbron in.

1. [Voer alle vereisten uit om het [!DNL Google Analytics] account](data-source-prerequisites.md).

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Klik op de werkbalk boven de tabel met gegevens op ![Maken](/help/search-social-commerce/assets/add.png "Maken").

1. In de [!UICONTROL Deployment Prerequisites] schakelt u het selectievakje in om te bevestigen dat de vereiste aangepaste afmeting &quot;ef_id&quot; is geïmplementeerd in het dialoogvenster [!DNL Google Analytics] en klik vervolgens op **[!UICONTROL Continue]**.

   Sommige eerste vereisten kunnen door andere rollen in uw organisatie zijn uitgevoerd. Neem contact op met uw accountteam van Adobe als u vragen hebt over de voorwaarden.

1. Voer de [gegevensbroninstellingen](data-source-settings.md):

   1. In de **[!UICONTROL Connect to [!DNL Google Analytics]]** , voert u de volgende handelingen uit.

      1. Voer de numerieke id in voor de [!DNL Google Analytics] account.

      1. Voer het e-mailadres in dat u wilt gebruiken voor toegang tot gegevens voor deze gegevensbron. Het e-mailadres moet bij een [!DNL Google] -account en beschikken over &quot;Lezen en analyseren&quot;-machtigingen voor de [!DNL Google Analytics] account. Zie de [instructies voor het toewijzen van gebruikersmachtigingen in [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Alleen specifieke [!DNL Google Analytics] De eigenschappen en de meningen zijn beschikbaar binnen Adobe Advertising, login gebruikend een e-mailadres dat toegang tot slechts die eigenschappen en meningen heeft.

         >[!NOTE]
         >
         >Als u het wachtwoord voor deze e-mailaccount later wijzigt, worden alle open verbindingen met de e-mailaccount gesloten. Als u het synchroniseren van gegevens wilt hervatten, gaat u terug naar deze pagina en [opnieuw verifiëren](data-source-reauthenticate.md).

      1. Schakel het selectievakje in om Adobe Advertising toegang te geven tot gegevens voor de account.

      1. Klik op **[!UICONTROL Authenticate]**.

   1. In de [!UICONTROL Account Details] in, geeft u de eigenschap en weergave op voor de metriek die u wilt importeren. Bovendien specificeer de douaneafmeting die met de waarde van de &quot;ef_id&quot;parameter van het vraagkoord wordt bevolkt.

   1. In de [!UICONTROL Import Metrics] , geeft u de metriek op die u in de feed(s) wilt opnemen.

      U kunt niet verwijderen [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces], of [!UICONTROL Session Duration], die automatisch worden opgenomen. U kunt tot 16 extra geldige metriek of metriek zonder gegevens toevoegen.

      >[!WARNING]
      >
      >[!DNL Google Analytics] staat maximaal 10 metriek in één enkele gegevensvoer toe. Zoeken, sociale zaken en handel kunnen maximaal twee feeds met in totaal 20 metriek ondersteunen, maar door een tweede feed te gebruiken worden uw API-aanroepen verdubbeld naar [!DNL Google Analytics]. Als u veel metriek hebt, selecteer slechts de metriek die u in doelstellingen voor optimalisering wilt gebruiken. Meer informatie over [quota&#39;s en oproeplimieten voor API-aanvragen voor [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. In de [!UICONTROL Metric Tag] de naam van de tag in die u aan elke metrische waarde voor de gegevensbron wilt toevoegen.

1. Klik rechtsboven op **[!UICONTROL Post]**.

   De gegevensbron krijgt de naam &quot;AccountName > PropertyName > ViewName&quot; en wordt automatisch geactiveerd. Als u de gegevensbron wilt onderbreken, raadpleegt u &quot;[Een feed onderbreken vanuit een gegevensbron](data-source-pause.md).&quot;

   De metriek zijn beschikbaar de volgende dag na voltooiing van de dagelijkse gegevenssynchronisatie, die om 05:00 in de tijdzone van de adverteerder begint. Zodra de metriek beschikbaar zijn, zijn zij zichtbaar in [[!UICONTROL Admin] > [!UICONTROL Conversions]](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md). Elke nieuwe omzettingsmetrische waarde krijgt de naam &quot;`ga:backEndMetricName_propertyID_viewID`,&quot; waarbij &quot;backEndMetricName&quot; de metrische naam is die door de API wordt gebruikt. De weergavenaam van elke nieuwe omzettingsmetrische waarde is &quot;`friendlyMetricName_ga:MetricTag`,&quot; waarbij &quot;VriendelijkeMetricName&quot; de metrische naam is die wordt weergegeven in [!DNL Google Analytics] en &quot;MetricTag&quot; is de [!UICONTROL Metric Tag] gedefinieerd in de gegevensbroninstellingen.

   U kunt de metriek aan campagnebeheer en portefeuillebeheermeningen, rapporten, en optimaliseringsdoelstellingen direct toevoegen.

>[!MORELIKETHIS]
>
>* [Over synchroniseren [!DNL Google Analytics] conversiemetingen](data-source-about.md)
>* [Vereisten voor het configureren van een [!DNL Google Analytics] gegevensbron](data-source-prerequisites.md)
>* [Een [!DNL Google Analytics] gegevensbron](data-source-edit.md)
>* [Synchronisatie van een gegevensbron pauzeren](data-source-pause.md)
>* [Een [!DNL Google Analytics] gegevensbron](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] gegevensbroninstellingen](data-source-settings.md)
>* [Bijlage - beschikbaar [!DNL Google Analytics] cijfers](data-source-ga-metrics.md)
