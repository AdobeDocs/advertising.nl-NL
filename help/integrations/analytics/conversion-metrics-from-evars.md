---
title: Creeer omzettingsmetriek van Adobe Analytics  [!DNL eVars]  en steunen
description: Vorm metriek van de de gebeurtenismetriek van het douanesucces gebruikend  [!DNL eVar] - en  [!DNL prop] - vlakke gegevens.
feature: Integration with Adobe Analytics, Conversions
exl-id: 7717d10c-76ca-4ba9-9fbb-e34ad006619c
source-git-commit: 91e8435ff00feca804dfa2f4c323f88ee31813ab
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Conversiemetriek maken van Adobe Analytics [!DNL eVars] en [!DNL props]

*Advertisers met Adobe Advertising-Adobe Analytics slechts Integratie*

U kunt succesgegevens gebruiken om DSP pakketten en zoek-, sociale en Commerce-campagnes te optimaliseren op basis van Adobe Analytics-sitegegevens die het beste passen bij de doelstellingen van uw merk. U kunt de metriek van de gebeurtenis van het douanesucces vormen die op uw bestaande [[!DNL Analytics] [!DNL eVars] ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) en [[!DNL props] ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/prop.html) wordt gebaseerd door [!DNL eVar] - en [!DNL prop] - vlakke gegevens in een gebeurtenis te financieren. Andere [!DNL Analytics] metriek, met inbegrip van standaard, douane, en gereserveerde omzettingsmetriek en verkeersmetriek, zijn automatisch beschikbaar in DSP en Onderzoek, Sociale, &amp; Commerce.

{het voorbeeld van het 0} Gebruik ](/help/integrations/assets/a4adc-conversion-evar-example.jpg " Voorbeeld van het Gebruik ")![

De meeste van de volgende taken moeten door een [!DNL Analytics] beheerder of andere gebruiker worden uitgevoerd. Als u hulp nodig hebt, contacteer (DSP gebruikers) het DSP technische ondersteuningsteam bij `adcloud_support@adobe.com` of (Onderzoek, Sociale, &amp; gebruikers van Commerce) uw Team van de Rekening van de Adobe.

1. In [!DNL Analytics], [ creeer een placeholder succesgebeurtenis ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/conversion-variables/success-event).

   Gebruik de volgende aanvullende parameters:

   **Type:** `Counter`

   **Polariteit:** of `Up is Good` of `Up is Bad`

   **Zichtbaarheid:** `Visible Everywhere`

   **Unieke Gebeurtenisopname:** `Always Record Event`

   **Deelname:** `Enabled`

   U hoeft de nieuwe gebeurtenis niet te implementeren op de website van uw merk omdat er bestaande gegevens worden gebruikt die al zijn vastgelegd.

1. Een verwerkingsregel maken en valideren in [!DNL Analytics] :

   >[!NOTE]
   >
   >Alleen [!DNL Analytics] -accountbeheerders kunnen verwerkingsregels maken, tenzij ze toestemming hebben verleend aan niet-beheerders.

   1. [ creeer een verwerkingsregel ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.html?lang=en), gebruikend de volgende configuratie:

      * Geef de vereiste [!DNL eVars] of [!DNL props] op voor de voorwaarde waaraan moet worden voldaan.

        U kunt zo nodig aanvullende niveaus van granulariteit configureren om ervoor te zorgen dat de meest nauwkeurige gebeurtenissen worden gemaakt.

        >[!TIP]
        >
        >U kunt het beste slechts één [!DNL eVar] of [!DNL prop] gebruiken.

      * Voor de actie, selecteer **Vastgestelde Gebeurtenis** en selecteer de placeholder gebeurtenis.

   1. In [!DNL Analytics] [!DNL Analysis Workspace], [ creeer een project ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html) en trek de nieuwe gebeurtenis in een vrije vormlijst om ervoor te zorgen dat het gegeven voor [!DNL eVar] of [!DNL prop] metrisch bevolkt is.

1. Neem contact op met het accountteam van de Adobe om de nieuwe metrische gegevens te synchroniseren naar de Adobe Advertising.

Nadat metrisch beschikbaar is, kunt u het gebruiken om een doel tot stand te brengen, dat u aan een Onderzoek, een Sociale, &amp; portefeuille van Commerce of gebruik als a [ douanedoel ](/help/dsp/optimization/custom-goal.md) voor een DSP pakket kunt dan toewijzen.

Raadpleeg voor meer informatie over het maken van doelstellingen het hoofdstuk over &quot;Doelstellingen&quot; in de Optimalisatiegids, dat beschikbaar is in Zoeken, Sociaal, &amp; Commerce

>[!MORELIKETHIS]
>
>* [[!DNL Analytics]  Gegevens in Adobe Advertising ](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [ Mening de omzettingsmetriek die voor een adverteerder wordt gevolgd ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
