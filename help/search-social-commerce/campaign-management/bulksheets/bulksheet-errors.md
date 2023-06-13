---
title: Fouten in werkbladen
description: Verwijzing naar mogelijke redenen voor elke fout in het werkblad.
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '1141'
ht-degree: 0%

---

# Fouten in werkbladen

Met Zoeken, Sociaal en Handel worden twee typen foutbestanden gegenereerd tijdens bewerkingen in bulksheet:

* **SE-fouten:** Wanneer een bestand wordt gepost maar het ad-netwerk niet alle gegevens accepteert, wordt een foutbestand met de naam `<uploaded file name>_se_errors.<extension used for the bulksheet>` wordt gemaakt. Wanneer sommige maar niet alle rijen werden goedgekeurd, toont het foutendossier de rijen die niet werden gepost en een verklaring van elke fout zodat kunt u het verbeteren. De fouten worden opgenomen in het gedeelte &quot;[!UICONTROL SE Error Message]&quot; kolom.

>[!NOTE]
>
>Als u [!DNL Google Ads] advertenties die in strijd zijn met het reclamebeleid van het advertentienetwerk maar in aanmerking komen voor uitzonderingen , worden die advertenties automatisch opnieuw gepost met vrijstellingsverzoeken . Als de vrijstellingsaanvraag mislukt, wordt informatie over de schending opgenomen in het foutbestand.

* **EF-fouten:** Wanneer een bestand of afzonderlijke rijen in het bestand niet kunnen worden geüpload of verwerkt met de bulkspaginabewerking, wordt een foutbestand met de naam `<uploaded file name>_ef_errors.<extension used for the bulksheet>`. Als het probleem zich bij afzonderlijke rijen voordoet, worden deze rijen opgenomen met een uitleg van elke fout, zodat u deze kunt corrigeren. De fouten worden opgenomen in het gedeelte &quot;[!UICONTROL EF Error Message]&quot; kolom.

## [!UICONTROL SE Error] berichten

Fouten in de [!UICONTROL SE Error] de kolom komt direct van het advertentienetwerk.

## [!UICONTROL EF Error] berichten

De volgende fouten kunnen in de [!UICONTROL EF Error] kolom in [!UICONTROL EF Errors] bestanden.

### Downloaden/fouten maken

| Categorie | Bericht | Beschrijving |
|----|----|----|
| Algemeen | [!UICONTROL Internal Error: Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | De bewerking is volledig mislukt als gevolg van een niet-gecategoriseerde of niet-afgehandelde fout. Neem contact op met uw Adobe-accountteam als het probleem zich blijft voordoen. |
| | [!UICONTROL Pre-Sync Failed. Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | Search, Social &amp; Commerce kon niet synchroniseren met het advertentienetwerk voordat het bulksheet werd gemaakt. Er is dus geen bulksheet gemaakt. Neem contact op met uw Adobe-accountteam als het probleem zich blijft voordoen. |

### Uploadfouten

| Categorie | Bericht | Beschrijving |
|----|----|----|
| Algemeen | [!UICONTROL Internal Error: Please Try Uploading the bulksheet Again. If Problem Persists Contact Customer Care] | De bewerking is mislukt. Neem contact op met uw Adobe-accountteam als het probleem zich blijft voordoen. |
| Alle entiteiten | [!UICONTROL Invalid Fields.] \[ongeldige velden en fout\] | De opgegeven gegevens ontbreken of zijn ongeldig. |
|  | [!UICONTROL Invalid Reference Given] | De id van de entiteit op het advertentienetwerk of de id van een bovenliggende entiteit (zoals de account-id) komt niet overeen met een entiteit in Zoeken, Sociale Zaken en Handel. Dit kan voorkomen wanneer u identiteitskaart in het bulksblad uitgeeft. |
|  | [!UICONTROL &lt;Entity> is deleted or expired] | De entiteit is verlopen of verwijderd en u kunt de eigenschappen ervan niet wijzigen. De entiteit kan worden verwijderd wanneer iemand de status handmatig heeft bewerkt. |
|  | [!UICONTROL &lt;Entity> status should be Active or Paused] | (Nieuwe entiteiten) Een nieuwe entiteit kan alleen &quot;Actief&quot; of &quot;Gepauzeerd&quot; zijn. |
|  | [!UICONTROL Duplicate Entries are present] | Voor dezelfde entiteit worden meerdere rijen opgenomen, met verschillende kenmerken in elke rij. U kunt de wijzigingen in één rij samenvoegen. |
|  | [!UICONTROL Invalid AMO ID given] | De AMO-id voor de rij bestaat niet. Dit kan voorkomen als u identiteitskaart in het bulksblad uitgeeft. |
|  | [!UICONTROL Invalid row given] | De rij bevat niet genoeg informatie om het entiteitstype te bepalen. Bewerk de rij om alle vereiste velden voor het eenheidstype op te nemen. |
| Accounts | [!UICONTROL Provide Valid Account Details] | (Opsommingstekens voor meerdere accounts) Account-id&#39;s worden niet in alle rijen opgenomen. Voer waarden in voor een van de volgende combinaties van kolommen voor elke rij: a) &quot;[!UICONTROL AMO ID]&quot; of b) &quot;[!UICONTROL Account Name]&quot; en &quot;[!UICONTROL Platform].&quot; |
|  | [!UICONTROL Account is disabled. Disabled Accounts cannot be processed] | Zoekopdrachten, sociale zaken en handel hebben geen toegang tot de advertentienetwerkaccount, zodat u geen campagnegegevens kunt maken of bewerken. Controleer of de gegevens voor de zoekaccount correct zijn en of de account is ingeschakeld. |
| Campagne | [!UICONTROL Invalid Shopping Country specified] | (Winkelcampagnes) De waarde in &quot;[!UICONTROL Sales Country]&quot; veld is ongeldig. Een lijst met geldige landen bekijken [for [!DNL Google Ads]](https://support.google.com/merchants/answer/160637#countrytable) en [for [!DNL Microsoft® Advertising]](https://help.ads.microsoft.com/#apex/3/en/51083). |
| Alle campagnecomponenten | [!UICONTROL Campaign creation failed] | De bovenliggende campagne is niet gemaakt, dus deze entiteit is niet gemaakt. Zorg ervoor dat alle bovenliggende entiteiten alle vereiste velden bevatten. |
| Advertentiegroep | [!UICONTROL Campaign Row missing] | De opgegeven bovenliggende campagne bestaat niet, dus de ad-groep is niet gemaakt. Maak de bovenliggende campagne in een nieuwe rij. |
|  | [!UICONTROL New adgroup has both keywords and placement] | Een advertentiegroep kan trefwoorden of plaatsingen bevatten, maar niet beide. Maak aparte ad-hocgroepen voor trefwoorden en plaatsingen. |
|  | [!UICONTROL No corresponding keyword for Adgroup] | ([!DNL Yandex]) De advertentiegroep is niet gemaakt omdat deze niet minstens één trefwoord bevat. |
|  | [!UICONTROL No corresponding creative for Adgroup] | ([!DNL Yandex]) De advertentiegroep is niet gemaakt omdat deze niet ten minste één advertentie bevat. |
|  | [!UICONTROL Creative Row Missing] | ([!DNL Yandex]) De advertentiegroep is niet gemaakt omdat deze niet ten minste één advertentie bevat. |
| Alle componenten van de advertentiegroep | [!UICONTROL Adgroup creation failed] | De bovenliggende ad-groep is niet gemaakt, dus deze entiteit kan niet worden gemaakt. Dit kan komen door een fout in de velden van de advertentiegroep of omdat de bovenliggende campagne is mislukt. Zorg ervoor dat alle bovenliggende entiteiten alle vereiste velden bevatten. |
|  | [!UICONTROL Adgroup Row Missing] | De opgegeven bovenliggende en bovenliggende groep bestaat niet, zodat de entiteit niet kan worden gemaakt. Maak de bovenliggende ad-groep in een nieuwe rij. |
|  | [!UICONTROL Cannot modify Tracking Template at Keyword / Creative / Site Link level until Account has been migrated to use Upgraded URLs. Please retry after migration] | De &quot;[!UICONTROL Tracking Template]&quot; veld is alleen voor accounts die gebruikmaken van uiteindelijke/geavanceerde URL&#39;s. Verwijder de waarde totdat u de account hebt gemigreerd voor het gebruik van de uiteindelijke/geavanceerde URL&#39;s. |
| Advertentie | [!UICONTROL Cannot modify attributes other than status code and url for &lt;ad type>] | (Andere typen toevoegen dan tekst, uitgevouwen tekst, product, installatie van de app en dynamisch zoeken) U kunt alleen de status en URL voor dit advertentietype bewerken. |
|  | [!UICONTROL The number of creatives under an AdGroup should not exceed 50] | Elke advertentiegroep kan maximaal 50 advertenties bevatten, en dit bulksblad bevat meer dan 50. Verminder het aantal advertenties. |
|  | [!UICONTROL Cannot modify an ad which is either deleted/expired or under an deleted/expired campaign] | De advertentie bevindt zich in een verlopen of verwijderde bovenliggende entiteit, zodat u deze niet kunt bewerken. |
| Trefwoord | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | De bovenliggende campagne of advertentiegroep is verwijderd of verlopen, zodat u de entiteit niet kunt wijzigen. |
| Plaatsing | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | De bovenliggende campagne of advertentiegroep is verwijderd of verlopen, zodat u de entiteit niet kunt wijzigen. |
|  | [!UICONTROL Cannot specify placement bids for websites under Display Select enabled Campaign with Search and Display Networks] | (Google Ads) U kunt alleen op plaatsen bieden in campagnes op het zoeknetwerk of alleen op het netwerk van inhoud, maar niet op campagnes die zich richten op zowel zoek- als inhoudsnetwerken. |
| Winkelproductgroep | [!UICONTROL Cannot delete Everything Else manually. It will be deleted automatically when all Product Group Conditions under the same parent are removed] | Elke productgroep moet een &quot;[!UICONTROL Everything Else]&quot;. U kunt niet handmatig een &quot;[!UICONTROL Everything Else]&quot;groep; deze wordt automatisch verwijderd wanneer u alle andere productgroepen op hetzelfde niveau verwijdert. |
|  | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | De bovenliggende campagne of advertentiegroep is verwijderd of verlopen, zodat u de entiteit niet kunt wijzigen. |
| Sitelink | [!UICONTROL Sitelinks Cannot update more than 10 site links per campaign] | ([!DNL Yandex] alleen) Het bericht is onjuist; elke campagne kan maximaal vier ( niet 10 ) sitelinks bevatten , en dit bulksblad bevat meer dan vier . Verwijder enkele sitelinks. |
|  | [!UICONTROL Cannot update sitelinks under deleted/expired campaign] | De bovenliggende campagne is verlopen of verwijderd, zodat u de sitelink niet kunt bewerken. |
|  | [!UICONTROL Creative creation failed] | ([!DNL Yandex]) De sitelink kan niet worden gemaakt omdat de advertentie niet is gemaakt. |
| Locatiedoel | [!UICONTROL Cannot modify locations under deleted campaigns or adgroups] | De bovenliggende campagne of advertentiegroep is verwijderd of verlopen, zodat u de locatiedoelen niet kunt bewerken. |
| Uitsluitingen | [!UICONTROL Other than status is modified] | U kunt alleen de status van een uitsluiting bewerken (&quot;[!UICONTROL Active]&quot; of &quot;[!UICONTROL Deleted]&quot;). |
| Doelstellingen/publiek van de Google-lijst voor hermarketing | [!UICONTROL Invalid Audience given] | ([!DNL Google Ads] (alleen campagnes) Het doel RLSA komt niet overeen met een bestaande RLSA (publiek). Corrigeer de waarden in het veld &quot;[!UICONTROL Audience]&quot; en &quot;[!UICONTROL RLSA Target]&quot; kolommen. |

### Post-fouten

De volgende fouten treden op in [!UICONTROL EF Errors] alleen bestanden. De meeste postingsfouten komen van het advertentienetwerk en zijn inbegrepen in een dossier van de Fouten van SE.

| Categorie | Bericht | Beschrijving |
|----|----|----|
| Algemeen | [!UICONTROL Internal Error: Please Try Posting the bulksheet Again. If Problem Persists Contact Customer Care] | De bewerking is mislukt. Neem contact op met uw Adobe-accountteam als het probleem zich blijft voordoen. |
| Alle entiteiten | [!UICONTROL Entity] is gepost aan advertentienetwerk | De entiteit werd gepost aan het advertentienetwerk, maar het werd niet tegelijkertijd gesynchroniseerd aan Onderzoek, Sociale, &amp; Handel, zodat zijn de entiteitgegevens niet onmiddellijk beschikbaar in Onderzoek, Sociale, &amp; Handel. Het synchronisatieproces wordt nu automatisch geactiveerd.<br><br>Wanneer grote hoeveelheden gegevens worden gesynchroniseerd, zijn de gegevens mogelijk enkele uren of langer niet beschikbaar in Zoeken, Sociale Zaken en Handel. |
| | [!UICONTROL Skipping &lt;ENTITY> creation since &lt;PARENT ENTITY> creation failed.] | De bovenliggende entiteit kon niet worden gemaakt, dus deze onderliggende entiteit is niet gemaakt. |

>[!MORELIKETHIS]
>
>* [Campagnegegevens beheren met behulp van bulksbladen](bulksheet-about.md)
>* [Een bulkbladbestand downloaden/maken](bulksheet-download.md)
>* [Openingspagina&#39;s in bulkbladbestanden valideren](bulksheet-validate-landing-pages.md)
>* [Een bulksbladbestand of gecorrigeerd foutbestand uploaden](bulksheet-upload.md)
>* [Kolommen of gecorrigeerde foutbestanden plaatsen](bulksheet-post.md)
