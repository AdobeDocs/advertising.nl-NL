---
title: "Conversie-metriek maken van Adobe Analytics [!DNL eVars] en props"
description: "Configureer aangepaste succesgebeurtenismetriek met [!DNL eVar]- en [!DNL prop]-level data."
feature: Integration with Adobe Analytics, Conversions
source-git-commit: f6f3e0b3cc867b817ce40c7ba06c76885948edbe
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 0%

---

# Conversie-metriek maken vanuit Adobe Analytics [!DNL eVars] en [!DNL props]

*Adverteerders met alleen Adobe Advertising-Adobe Analytics-integratie*

U kunt succesgegevens gebruiken om DSP pakketten en zoek-, sociale en handelscampagnes te optimaliseren op basis van Adobe Analytics-sitegegevens die het beste passen bij de doelstellingen van uw merk. U kunt maatstaven voor aangepaste succesgebeurtenissen configureren op basis van [uw bestaande [!DNL Analytics] [!DNL eVars]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) en [[!DNL props]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) door middel van fundering [!DNL eVar]- en [!DNL prop]-level gegevens in een gebeurtenis. Overige [!DNL Analytics] metriek, met inbegrip van standaard, douane, en gereserveerde omzettingsmetriek en verkeersmetriek, zijn automatisch beschikbaar in DSP en Onderzoek, Sociale, &amp; Handel.

![Gebruiksvoorbeeld](/help/integrations/assets/a4adc-conversion-evar-example.jpg "Gebruiksvoorbeeld")

De meeste van de volgende taken moeten worden uitgevoerd door een [!DNL Analytics] beheerder of andere gebruiker. Als u hulp nodig hebt, neemt u contact op met (DSP gebruikers) het DSP technische ondersteuningsteam op `adcloud_support@adobe.com` of (zoek gebruikers van de Sociale, &amp; Handel) uw Adobe Account Team.

1. In [!DNL Analytics], [een placeholder succesgebeurtenis maken](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-events/success-event.html?lang=en).

   Gebruik de volgende aanvullende parameters:

   **Type:** `Counter`

   **Polariteit:**  ofwel `Up is Good` of `Up is Bad`

   **Zichtbaarheid:** `Visible Everywhere`

   **Unieke gebeurtenisopname:** `Always Record Event`

   **Deelname:** `Enabled`

   U hoeft de nieuwe gebeurtenis niet te implementeren op de website van uw merk omdat er bestaande gegevens worden gebruikt die al zijn vastgelegd.

1. Een verwerkingsregel maken in [!DNL Analytics]:

   >[!NOTE]
   >
   >Alleen [!DNL Analytics] accountbeheerders kunnen verwerkingsregels maken, tenzij ze machtigingen hebben verleend aan niet-beheerders.

   1. [Een verwerkingsregel maken](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en), met de volgende configuratie:

      * Geef voor de voorwaarde waaraan moet worden voldaan, de vereiste [!DNL eVars] of [!DNL props].

        U kunt zo nodig aanvullende niveaus van granulariteit configureren om ervoor te zorgen dat de meest nauwkeurige gebeurtenissen worden gemaakt.

        >[!TIP]
        >
        >De beste manier is om slechts één [!DNL eVar] of [!DNL prop].

      * Selecteer bij de handeling **Gebeurtenis instellen** en selecteert u de gebeurtenis placeholder.

   1. In [!DNL Analytics] [!DNL Analysis Workspace], [een project maken](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) en trek de nieuwe gebeurtenis in een vrije-vormlijst om ervoor te zorgen dat de gegevens voor [!DNL eVar] of [!DNL prop] metrisch.

1. Neem contact op met het accountteam van Adobe om de nieuwe-waarde in Adobe Advertising te synchroniseren.

Nadat metrisch beschikbaar is, kan het gebruiken om een doel tot stand te brengen, dat u dan aan een portefeuille van het Onderzoek, Sociale, &amp; Handel of gebruik als [aangepast doel](/help/dsp/optimization/custom-goal-about.md) voor een DSP pakket.

Voor meer informatie over het creëren van doelstellingen, zie het hoofdstuk van de Gids van de Optimalisering over &quot;Doelstellingen,&quot;dat van binnen Onderzoek, Sociale, &amp; Handel beschikbaar is.

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Gegevens in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
<!--
>* [](/help/search-social-commerce/admin/conversion-metrics/ ????????)
-->