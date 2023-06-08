---
title: Over synchroniseren [!DNL Google Analytics] conversiemetingen
description: Meer informatie over synchroniseren [!DNL Google Analytics] conversiemetriek voor optimalisatie en rapportage.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Over synchroniseren [!DNL Google Analytics] conversiemetingen

Met Zoeken, Sociaal en Handel kunt u conversiemetriek synchroniseren voor een specifieke [!DNL Google Analytics] account, eigenschap en weergavecombinatie voor optimalisatie en rapportage. [Paginaweergaven](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=page_tracking&amp;jump=ga_pageviews), [Sessies](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessions), [Stuitsnelheid](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_bouncerate) (berekend als boekingen/sessies), en [Sessieduur](https://ga-dev-tools.google/dimensions-metrics-explorer/#view=detail&amp;group=session&amp;jump=ga_sessionduration) worden automatisch opgenomen. U kunt maximaal 16 extra metriek per gegevensbron omvatten.

>[!NOTE]
>
>Reclame DSP gebruikers kunnen de omzettingsmetriek als douanedoelstellingen en in rapporten gebruiken.

Alle API-toepassingen voor de gegevensoverdracht worden in het toepasselijke [!DNL Google Analytics] account. U kunt uw quota&#39;s voor dit project weergeven in [de [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). Zie [!DNL Google Analytics] documentatie voor meer informatie over [quota&#39;s en oproeplimieten voor het rapporteren van API-aanvragen](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

De volgende stappen beschrijven het proces voor het synchroniseren van conversiegegevens van [!DNL Google Analytics].

1. [Voer de vereiste taken uit](data-source-prerequisites.md)

   * Een Adobe-advertentietoken implementeren (`ef_id` parameter querytekenreeks) in de bestemmingspagina-URL&#39;s voor alle toepasselijke advertentierekeningen.

   * Leg het Adobe-advertentietoken vast (`ef_id` querytekenreeks (parameter) in een [!DNL Custom Dimension] in [!DNL Google Analytics].

1. (Accountbeheerder van het Agentschap, accountmanager van het agentschap, [!DNL Adobe] accountmanager en alleen beheerders) [Eén gegevensbron maken per [!DNL Google Analytics] account, eigenschap en weergavecombinatie](data-source-configure.md).

   Als u metriek voor meerdere eigenschappen of voor meerdere weergaven voor één eigenschap wilt integreren, stelt u voor elke eigenschap een aparte gegevensbron in.

   Zodra een gegevensbron wordt gevormd, trekt Onderzoek, Sociale, &amp; Handel gegevens dagelijks, die bij 05:00 in de tijdzone van de adverteerder beginnen. Zodra de metriek beschikbaar zijn, kunt u hen in campagne en portefeuillebeheermeningen en in rapporten omvatten, en hen gebruiken in optimaliseringsdoelstellingen, zoals nodig.

>[!MORELIKETHIS]
>
>* [Vereisten voor het configureren van een [!DNL Google Analytics] gegevensbron](data-source-prerequisites.md)
>* [Een [!DNL Google Analytics] weergeven als gegevensbron](data-source-configure.md)
>* [Een [!DNL Google Analytics] gegevensbron](data-source-edit.md)
>* [Synchronisatie van een gegevensbron pauzeren](data-source-pause.md)
>* [Een [!DNL Google Analytics] gegevensbron](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] gegevensbroninstellingen](data-source-settings.md)
>* [Bijlage - beschikbaar [!DNL Google Analytics] cijfers](data-source-ga-metrics.md)

