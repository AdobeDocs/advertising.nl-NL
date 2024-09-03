---
title: Voer  [!DNL Google Ads]  verbeterde omzettingen voor lood uit
description: Leer over het werkschema voor vestiging  [!DNL Google Ads]  verbeterde omzettingen voor lood.
feature: Search Campaign Management, Conversions
source-git-commit: 60a67c8668df13afc08e14b0a495a37ded24bc0c
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Uitvoeren van [!DNL Google Ads] verbeterde omzettingen voor leads

*[!DNL Google Ads]alleen accounts*

[[!DNL Google Ads]  verbeterde omzettingen voor lood ](https://support.google.com/google-ads/answer/9888656) staat u toe om gebruikers aan off-line omzettingen in kaart te brengen gebruikend uw gegevens van de eerste-partijomzetting. Gebruik uitgebreide conversies voor leads in omgevingen waarin klik-id&#39;s niet beschikbaar zijn, zoals voor het bijhouden van de verkoop via telefoon of e-mail die het resultaat is van websiteleads.

Binnen Zoeken, Sociaal, &amp; Commerce kunt u uw verbeterde omzettingen voor leads opnemen als meetgegevens in rapporten en als gewogen meetgegevens binnen doelstellingen voor optimalisatie. Search, Social &amp; Commerce synchroniseert uw bestaande verbeterde conversies naar leads dagelijks om 5:00 in de tijdzone van de adverteerder.

Voer de volgende stappen uit om deze functie te gebruiken. De stappen voor het maken van codes voor het bijhouden van conversies en het maken van conversieacties kunnen optioneel worden omgekeerd.

1. Kies in [!DNL Google Ads] de optie voor het aanmelden bij verbeterde conversies voor leads:

   1. Open de conversie-instellingen van de account.

   1. Selecteer de optie voor verbeterde conversies voor leads en accepteer de servicevoorwaarden.

   1. Selecteer of u een [!DNL Google] -tag of [!DNL Google Tag Manager] wilt gebruiken om de conversietag te maken.


1. Configureer en implementeer een [!DNL Google] -tag voor de conversieactie.

   Voor instructies, zie de [!DNL Google Ads] hulp om markeringen voor verbeterde omzettingen voor lood [ tot stand te brengen gebruikend a  [!DNL Google]  markering ](https://support.google.com/google-ads/answer/11021502) of [ gebruikend  [!DNL Google Tag Manager] ](https://support.google.com/google-ads/answer/11347292).

1. Creeer een omzettingsactie voor de verbeterde omzetting voor lood binnen of [ Onderzoek, Sociale, &amp; Commerce ](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) of [ Advertenties van Google ](https://support.google.com/google-ads/answer/12216226).

   Voor het **Type van Omzetting,** uitgezochte *Omzetting van de Invoer* of *Invoer.*

1. Upload zo vaak als nodig gegevens van de eerste partij, inclusief gehashte e-mailadressen of telefoonnummers, om deze aan de conversie voor een opgegeven account toe te wijzen. U kunt deze stap van binnen of [ Onderzoek voltooien, Sociale, &amp; Commerce ](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) of het gebruiken [!DNL Google Data Manager].

   * In Zoeken, Sociaal en Commerce kunt u een sjabloon in [!DNL Microsoft Excel] -indeling downloaden, conversiegegevens invoeren en het bestand lokaal opslaan en het bewerkte bestand vervolgens uploaden. De sjabloon bevat kolommen die aangeven of de gebruiker toestemming heeft gegeven om gegevens te uploaden naar [!DNL Google] voor advertenties en voor persoonlijke doeleinden.

     Alle geüploade gegevens worden in realtime gesynchroniseerd met [!DNL Google Ads] .

   * Voor meer informatie over het uploaden van gegevens die [!DNL Google Data Manager] gebruiken, zie &quot;[ Ongeveer de manager van Gegevens ](https://support.google.com/google-ads/answer/14639041).&quot;

>[!MORELIKETHIS]
>
>* [ creeer een omzettingsactie voor a  [!DNL Google Ads]  verbeterde omzetting voor lood ](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [ upload off-line omzettingsgegevens voor verbeterde omzettingen ](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
