---
title: Optionele trackingparameters voor URL's die klikken en volgen
description: Leer over facultatieve het volgen parameters van het Onderzoek, Sociale, & van de Handel en en netwerk-specifieke het volgen parameters die u aan uw klik-volgende URLs kunt toevoegen.
exl-id: df53bb8c-63ad-47f9-af44-57bd4bd58d71
feature: Search Tracking
source-git-commit: c743e0dec75578d739a704ef94f96dd7be4f982e
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# Optionele trackingparameters voor URL&#39;s die klikken en volgen

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan], en [!DNL Yandex] alleen accounts*

In plaats van alleen de standaard trackingparameters te gebruiken voor een uiteindelijke URL of doel-URL, kunt u meer parameters toevoegen om specifieke gegevens voor een advertentie-netwerkaccount bij te houden. U kunt om het even welke combinatie volgende parameters in de rekeningsmontages of de campagnemontages toevoegen:

* U kunt elke statische teksttekenreeks toevoegen als een parameter in de basis-URL&#39;s voor de account/campagne.

* U kunt Adobe Advertising- en netwerkspecifieke parameters toevoegen aan de basis-URL&#39;s voor de account/campagne om meer gegevens bij te houden:

   * Adobe Advertising parameters zijn semistatisch. Adobe Advertising voegt een gegevenswaarde in wanneer de basis-URL naar het advertentienetwerk wordt geüpload. Wanneer u bijvoorbeeld `campaign={ef_campaign}` naar de basis-URL; Adobe Advertising vervangt `{ef_campaign}` met de daadwerkelijke naam van de campagne (zoals &quot;Terug naar school-Campagne&quot;) wanneer het uploadt URL.

     **Opmerking:** Nadat de waarden zijn ingevoegd, blijven ze statisch. Als u een trefwoord of advertentie naar een andere advertentiegroep verplaatst of de advertentiegroep naar een andere campagne verplaatst, wordt de  {ef_adgroup} of {ef_campaign} parameter niet automatisch wordt bijgewerkt, zodat moet u een nieuwe bestemmingsURL of basis (definitieve) URL manueel produceren.

   * Netwerkspecifieke parameters zijn dynamisch en de zoekfunctie voegt een gegevenswaarde in wanneer de gebruiker op een advertentie klikt. Wanneer u bijvoorbeeld `{param1}` op de basis-URL vervangt het advertentienetwerk deze door de werkelijke URL {param1} waarde wanneer een eindgebruiker op de advertentie klikt.

>[!NOTE]
>
>* Meerdere parameters scheiden met komma&#39;s of ampersands (`&`).
>* De volgende parameters zijn niet hoofdlettergevoelig.
>* Speciale tekens in de toegevoegde parameters worden als volgt vervangen in de gegenereerde doel-URL of basis-URL (definitieve) URL:
>  * `=` vervangen door `%3D`
>  * `?` vervangen door `%26`
>  * een lege spatie wordt vervangen door `%2B`
>  Wanneer u bijvoorbeeld de parameter toevoegt `campaign={ef_campaign}` naar de basis-URL http://www.example.com voor een trefwoord, wordt de basis-URL voor dat trefwoord gegenereerd als `http://www.example.com/campaign%3D{ef_campaign}`.

## Parameters voor statische tracking voor zoeken, sociale zaken en handel

U kunt de volgende parameters voor rekeningen op om het even welk advertentienetwerk gebruiken en hen combineren met parameters voor een specifiek advertentienetwerk zoals nodig. Sommige van deze parameters dupliceren de parameters die automatisch voor specifieke advertentienetwerken worden toegevoegd wanneer de volgende methode van de rekening &quot;[!UICONTROL EF Direct].&quot;

Alle volgende parameters moeten als sleutel-waarde paar worden gespecificeerd; u kunt veelvoudige parameters voor één waardepaar omvatten. Als u bijvoorbeeld de naam van de campagne wilt invoegen, gebruikt u `<your_parameter_name>={ef_campaign}`, zoals `campaign={ef_campaign}`. Als u het type overeenkomst wilt invoegen met de opgegeven overeenkomende typenamen, gebruikt u `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`, zoals `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. De niet-toepasselijke overeenkomende typen worden niet weergegeven in de resulterende URL.

| Parameter | Beschrijving |
| ---- | ---- |
| <code>{custom_code}</code> | Gegevens uit de kolom &quot;Aangepast URL-param&quot; in een geüpload bulksbladbestand invoegen in de URL voor reeksspatiëring. {custom_code} mag alleen worden gebruikt aan het einde van de waarde van een of meer sleutel-waardeparen in de URL voor reeksspatiëring. Voorbeelden:  <code>a={custom_code}</code>; <code>a={ef_campaignid}{custom_code}</code>; <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>Opmerking:</b> Als u de aangepaste waarde uit het bulksbladbestand wilt invoegen in de URL voor bijhouden, uploadt u het bulksbladbestand met de optie URL&#39;s voor reeksspatiëring genereren. Zie &quot;[Campagnegegevens beheren met behulp van bulksbladen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot; |
| <code>{ef_uniqueid}</code> | De unieke id invoegen die door de Adobe Advertising is gemaakt. Wordt automatisch toegevoegd wanneer de methode voor reeksspatiëring &quot;EF-omleiding&quot; is. |
| <code>{ef_userid}</code> | Om de unieke gebruikersnaam in te voegen die de Adobe Advertising aan de adverteerder toewijst. |
| <code>{ef_sid}</code> | Om numerieke identiteitskaart op te nemen die Onderzoek, Sociale, &amp; Handel aan het advertentienetwerk toewijst: <i>[!UICONTROL 3]</i> for [!DNL Google Ads], <i>[!UICONTROL 10]</i> for [!DNL Microsoft®® Advertising], <i>[!UICONTROL 45]</i> for [!DNL Meta], <i>[!UICONTROL 86]</i> for [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> for [!DNL Naver], <i>[!UICONTROL 88]</i> for [!DNL Baidu], <i>[!UICONTROL 90]</i> for [!DNL Yandex], <i>[!UICONTROL 94]</i> for [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> for [!DNL Yahoo Native] (afgekeurd), of <i>[!UICONTROL 106]</i> for [!DNL Pinterest] (vervangen). |
| <code>{ef_searchengine}</code> | De naam van het advertentienetwerk invoegen. |
| <code>{ef_campaign}</code> | De naam van de campagne invoegen. |
| <code>{ef_campaignid}</code> | De campagne-id invoegen. <b>Opmerking:</b> ID voor een nieuwe campagne wordt niet gecreeerd tot de campagne aan het advertentienetwerk wordt gepost. Als de account de optie &quot;[!UICONTROL EF Redirect]De opties &quot; en &quot;AutoUpload&quot;, dan voegt de Adobe Advertising automatisch campagne-id in relevante bestemmings-URLs of definitieve URLs de volgende dag in. Als de account de optie &quot;[!UICONTROL EF Redirect]&quot; en [!UICONTROL Auto Upload]&quot; en u wilt de campagne-id invoegen in de relevante doel-URL&#39;s of uiteindelijke URL&#39;s, moet u de campagne maken, een bulksbladbestand voor de nieuwe campagne downloaden met de optie &quot;URL&#39;s bijhouden genereren&quot; en het bestand vervolgens naar het advertentienetwerk posten. |
| <code>{ef_adgroup}</code> | De naam van de advertentiegroep invoegen. |
| <code>{ef_adgroupid}</code> | De advertentie-ID invoegen. <b>Opmerking:</b> De id voor een nieuwe advertentiegroep wordt pas gemaakt nadat de advertentiegroep naar het advertentienetwerk is gepost. Als de account de optie &quot;[!UICONTROL EF Redirect]&quot;- en &quot;AutoUpload&quot;-opties, voegt Adobe Advertising de id van de advertentiegroep automatisch in in de relevante doel-URL&#39;s of uiteindelijke URL&#39;s de volgende dag. Als de account het[!UICONTROL EF Redirect]&quot; en [!UICONTROL Auto Upload]&quot; en u wilt de id van de advertentiegroep invoegen in de relevante doel-URL&#39;s of uiteindelijke URL&#39;s, dan moet u de advertentiegroep maken; een bulksbladbestand voor de nieuwe advertentiegroep downloaden met de optie &quot;URL&#39;s van het bijhouden genereren&quot; en het bestand vervolgens naar het advertentienetwerk posten. |
| <code>{ef_keyword}</code> | Het trefwoord invoegen. |
| <code>{ef_keywordid}</code> | De trefwoordid invoegen. <b>Opmerking:</b> De id voor een nieuw trefwoord wordt pas gemaakt nadat het trefwoord naar het advertentienetwerk is gepost. Als de account de optie &quot;[!UICONTROL EF Redirect]&quot; en [!UICONTROL Auto Upload]&quot;-opties, voegt de Adobe Advertising de trefwoordid de volgende dag automatisch in de desbetreffende doel-URL&#39;s of uiteindelijke URL&#39;s in. Als de account de optie &quot;[!UICONTROL EF Redirect]&quot; en [!UICONTROL Auto Upload]&quot; en u wilt de sleutelwoordidentiteitskaart in relevante bestemmingsURLs of definitieve URLs opnemen, dan moet u het sleutelwoord tot stand brengen; een bulksbladdossier voor het nieuwe sleutelwoord downloaden, gebruikend de optie &quot;het Volgen URLs van het Terugwinnen;&quot;en dan het dossier aan het ad netwerk posten. |
| <code>{ef_matchtype}</code> | Als u het trefwoordmatrixtype wilt invoegen als &quot;Breed&quot;, &quot;Exacte&quot; of &quot;Wis&quot;. Automatisch opgenomen voor [!DNL Google Ads] en [!DNL Microsoft® Advertising] met &quot;[!UICONTROL EF Redirect]&quot;. |
| <code>{ef_adid}</code> | De advertentie-id invoegen. <b>Opmerking:</b> De id voor een nieuwe advertentie wordt pas gemaakt nadat de advertentie naar het advertentienetwerk is gepost. Als de account de optie &quot;[!UICONTROL EF Redirect]&quot; en [!UICONTROL Auto Upload]&quot;-opties, voegt de Adobe Advertising de advertentie-id de volgende dag automatisch in de relevante doel-URL&#39;s of uiteindelijke URL&#39;s in. Als de account de optie &quot;[!UICONTROL EF Redirect]&quot; en [!UICONTROL Auto Upload]&quot; en u wilt de advertentie-id invoegen in de relevante doel-URL&#39;s of uiteindelijke URL&#39;s, dan moet u de advertentie maken, een bulksbladbestand voor de nieuwe advertentie downloaden met de optie &quot;URL&#39;s van het bijhouden genereren&quot; en het bestand vervolgens naar het advertentienetwerk posten. |

## [!DNL Google Ads] dynamische tracking-parameters

Zie [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## [!DNL Microsoft® Advertising] dynamische tracking-parameters

Zie [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## Yahoo! Japan voegt dynamische volgende parameters toe

Zie [https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US).

## [!DNL Yandex] dynamische tracking-parameters

Zie [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [Over URL-indelingen voor het bijhouden van klikken voor de service Adobe Advertising converteren](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
