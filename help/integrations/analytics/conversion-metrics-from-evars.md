---
title: Conversiemetriek maken van Adobe Analytics Vars en props
description: Configureer aangepaste succesgebeurtenismetriek met behulp van gegevens op eVar- en prop-niveau.
feature: Integration with Adobe Analytics, Conversions
source-git-commit: d4f439ad23fc386bc85d95cc1291ec668ecf1cd2
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Conversiemetriek maken van Adobe Analytics Vars en props

*Adverteerders met alleen Adobe Advertising-Adobe Analytics-integratie*

U kunt succesgegevens gebruiken om DSP pakketten en zoek-, sociale en handelscampagnes te optimaliseren op basis van Adobe Analytics-sitegegevens die het beste passen bij de doelstellingen van uw merk. U kunt de metriek van de gebeurtenis van het douanesucces vormen gebaseerd op uw bestaand [!DNL Analytics] [eVars](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) en [props](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) door gegevens op eVar- en propniveau in een gebeurtenis te fungeren. Overige [!DNL Analytics] metriek, met inbegrip van standaard, douane, en gereserveerde omzettingsmetriek en verkeersmetriek, zijn automatisch beschikbaar in DSP en Onderzoek, Sociale, &amp; Handel.

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

      * Geef voor de voorwaarde waaraan moet worden voldaan, de vereiste eVars of props op.

        U kunt zo nodig aanvullende niveaus van granulariteit configureren om ervoor te zorgen dat de meest nauwkeurige gebeurtenissen worden gemaakt.

        >[!TIP]
        >
        >De beste manier is om slechts één eVar of rekwisiet te gebruiken.

      * Selecteer bij de handeling **Gebeurtenis instellen** en selecteert u de gebeurtenis placeholder.

   1. In [!DNL Analytics] [!DNL Analysis Workspace], [een project maken](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) en trek de nieuwe gebeurtenis in een vrije vormlijst om ervoor te zorgen dat de gegevens voor eVar of pro metrisch bevolken.

1. Neem contact op met het accountteam van Adobe om de nieuwe-waarde in Adobe Advertising te synchroniseren.

Nadat metrisch beschikbaar is, kan het gebruiken om een doel tot stand te brengen, dat u dan aan een portefeuille van het Onderzoek, Sociale, &amp; Handel of gebruik als [aangepast doel](/help/dsp/optimization/custom-goal-about.md) voor een DSP pakket.

Voor meer informatie over het creëren van doelstellingen, zie het hoofdstuk van de Gids van de Optimalisering over &quot;Doelstellingen,&quot;dat van binnen Onderzoek, Sociale, &amp; Handel beschikbaar is.

>[!MORELIKETHIS]
>
>* [[!DNL Analytics] Gegevens in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
<!--
>* [](/help/search-social-commerce/admin/conversion-metrics/ ????????)
-->