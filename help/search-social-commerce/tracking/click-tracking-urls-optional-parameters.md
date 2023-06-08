---
title: Optionele trackingparameters voor URL's die klikken en volgen
description: Leer over facultatieve het volgen parameters van het Onderzoek, Sociale, & van de Handel en en netwerk-specifieke het volgen parameters die u aan uw klik-volgende URLs kunt toevoegen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 0%

---

# Optionele trackingparameters voor URL&#39;s die klikken en volgen

*Google Ads, Microsoft Advertising en Yahoo! Alleen Japan-accounts*

In plaats van alleen de standaard trackingparameters te gebruiken voor een uiteindelijke URL of doel-URL, kunt u meer parameters toevoegen om specifieke gegevens voor een advertentie-netwerkaccount bij te houden. U kunt om het even welke combinatie volgende parameters in de rekeningsmontages of de campagnemontages toevoegen:

* U kunt elke statische teksttekenreeks toevoegen als een parameter in de basis-URL&#39;s voor de account/campagne.

* U kunt Adobe Advertising- en netwerkspecifieke parameters toevoegen aan de basis-URL&#39;s voor de account/campagne om meer gegevens bij te houden:

   * Adobe Reclameparameters zijn semistatisch. Bij Advertising Adobe wordt een gegevenswaarde ingevoegd wanneer de basis-URL naar het advertentienetwerk wordt geüpload. Wanneer u bijvoorbeeld `campaign={ef_campaign}` bij de basis-URL vervangt Adobe Advertising `{ef_campaign}` met de daadwerkelijke naam van de campagne (zoals &quot;Back-to-school-Campaign&quot;) wanneer de URL wordt geüpload.

      **Opmerking:** Zodra de waarden worden opgenomen, blijven zij statisch. Als u een trefwoord of advertentie naar een andere advertentiegroep verplaatst of de advertentiegroep naar een andere campagne verplaatst, wordt de parameter {ef_adgroup} of {ef_campagne} niet automatisch bijgewerkt, dus moet u handmatig een nieuwe doel-URL of basis-URL (final) genereren.

   * Netwerkspecifieke parameters zijn dynamisch en de zoekfunctie voegt een gegevenswaarde in wanneer de gebruiker op een advertentie klikt. Wanneer u bijvoorbeeld `{param1}` op de basis-URL vervangt het advertentienetwerk deze door de werkelijke URL {param1} als een eindgebruiker op de advertentie klikt.

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
| {custom_code}</code> | Gegevens uit de kolom &quot;Aangepast URL-param&quot; in een geüpload bulksbladbestand invoegen in de URL voor reeksspatiëring. {custom_code} mag alleen worden gebruikt aan het einde van de waarde van een of meer sleutel-waardeparen in de URL voor reeksspatiëring. Voorbeelden: a={custom_code}</code>; a={ef_campagne}{custom_code}</code>; a={ef_campagne}{custom_code}&amp;b={custom_code}</code><br><br><b>Opmerking:</b> Als u de aangepaste waarde uit het bulksbladbestand wilt invoegen in de URL voor bijhouden, uploadt u het bulksbladbestand met de optie URL&#39;s voor bijhouden genereren. Zie &quot;[Campagnegegevens beheren met behulp van bulksbladen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot; |
| {ef_uniqueid}</code> | De unieke id invoegen die is gemaakt door Adobe Advertising. Wordt automatisch toegevoegd wanneer de methode voor reeksspatiëring &quot;EF-omleiding&quot; is. |
| {ef_userid}</code> | Om de unieke gebruikersnaam in te voegen die door advertenties van Adobe aan de adverteerder wordt toegewezen. |
| {ef_sid}</code> | Om numerieke identiteitskaart op te nemen die Onderzoek, Sociale, &amp; Handel aan het advertentienetwerk toewijst: <i>[!UICONTROL 3]</i> for [!DNL Google Ads], <i>[!UICONTROL 10]</i> for [!DNL Microsoft® Advertising], <i>[!UICONTROL 45]</i> for [!DNL Meta], <i>[!UICONTROL 86]</i> for [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> for [!DNL Naver], <i>[!UICONTROL 88]</i> for [!DNL Baidu], <i>[!UICONTROL 90]</i> for [!DNL Yandex], <i>[!UICONTROL 94]</i> for [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> for [!DNL Yahoo Native] (afgekeurd), of <i>[!UICONTROL 106]</i> for [!DNL Pinterest] (afgekeurd). |
| {ef_searchEngine}</code> | De naam van het advertentienetwerk invoegen. |
| {ef_campagne}</code> | De naam van de campagne invoegen. |
| {ef_campagnid}</code> | De campagne-id invoegen. <b>Opmerking:</b> ID voor een nieuwe campagne wordt niet gecreeerd tot de campagne aan het advertentienetwerk wordt gepost. Als de account gebruikmaakt van de opties &quot;EF Redirect&quot; en &quot;AutoUpload&quot;, voegt Adobe-advertentie de volgende dag automatisch de campagne-id in de desbetreffende doel-URL&#39;s of de uiteindelijke URL&#39;s in. Als de account de opties &quot;EF omleiden&quot; en &quot;Automatisch uploaden&quot; niet gebruikt en u de campagne-id wilt invoegen in de relevante doel-URL&#39;s of de uiteindelijke URL&#39;s, moet u de campagne maken. Download een bulksheet-bestand voor de nieuwe campagne met de optie &quot;URL&#39;s bijhouden genereren;&quot; en post het bestand vervolgens naar het ad-netwerk. |
| {ef_adgroup}</code> | De naam van de advertentiegroep invoegen. |
| {ef_adgroupid}</code> | De id van de advertentiegroep invoegen. <b>Opmerking:</b> De id voor een nieuwe advertentiegroep wordt pas gemaakt nadat de advertentiegroep naar het advertentienetwerk is gepost. Als de account gebruikmaakt van de opties &quot;EF Redirect&quot; en &quot;AutoUpload&quot;, voegt Adobe-advertentie de volgende dag automatisch de id van de advertentiegroep in de desbetreffende doel-URL&#39;s of uiteindelijke URL&#39;s in. Als de account de opties &quot;EF omleiden&quot; en &quot;Automatisch uploaden&quot; niet gebruikt en u de id van de advertentiegroep wilt invoegen in de relevante doel-URL&#39;s of de uiteindelijke URL&#39;s, moet u de advertentiegroep maken. Download een bulksheet-bestand voor de nieuwe advertentiegroep, waarbij u de optie &quot;URL&#39;s voor bijhouden genereren&quot; gebruikt en het bestand vervolgens op het advertentienetwerk plaatst. |
| {ef_keyword}</code> | Het trefwoord invoegen. |
| {ef_keywordid}</code> | De trefwoordid invoegen. <b>Opmerking:</b> De id voor een nieuw trefwoord wordt pas gemaakt nadat het trefwoord naar het advertentienetwerk is gepost. Als de account gebruikmaakt van de opties &quot;EF omleiden&quot; en &quot;Automatisch uploaden&quot;, wordt in advertentie van Adobe de volgende dag automatisch de trefwoordid ingevoegd in de desbetreffende doel-URL&#39;s of in de uiteindelijke URL&#39;s. Als de account de opties &quot;EF omleiden&quot; en &quot;Automatisch uploaden&quot; niet gebruikt en u de trefwoordid wilt invoegen in de relevante doel-URL&#39;s of de uiteindelijke URL&#39;s, moet u het trefwoord maken. Download een bulksheet-bestand voor het nieuwe trefwoord, met de optie &quot;URL&#39;s bijhouden genereren&quot; en post het bestand vervolgens naar het advertentienetwerk. |
| {ef_matchtype}</code> | Als u het trefwoordmatrixtype wilt invoegen als &quot;Breed&quot;, &quot;Exacte&quot; of &quot;Wis&quot;. Automatisch opgenomen voor advertenties van Google Ads en Microsoft met de &quot;EF Redirect&quot;-methode. |
| {ef_adid}</code> | De advertentie-id invoegen. <b>Opmerking:</b> De id voor een nieuwe advertentie wordt pas gemaakt nadat de advertentie naar het advertentienetwerk is gepost. Als de account gebruikmaakt van de opties &quot;EF omleiden&quot; en &quot;Automatisch uploaden&quot;, voegt Adobe-advertentie de volgende dag automatisch de advertentie-id in de desbetreffende doel-URL&#39;s of uiteindelijke URL&#39;s in. Als de account de opties &quot;EF omleiden&quot; en &quot;Automatisch uploaden&quot; niet gebruikt en u de advertentie-id wilt invoegen in de relevante doel-URL&#39;s of de uiteindelijke URL&#39;s, moet u de advertentie maken. Download een bulksheet-bestand voor de nieuwe advertentie met de optie &quot;URL&#39;s voor bijhouden genereren&quot; en post het bestand vervolgens naar het advertentienetwerk. |

## Google voegt dynamische trackingparameters toe

Zie [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## Dynamische volgparameters voor Microsoft-advertentie

Zie [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## Oorspronkelijke parameters voor dynamisch bijhouden van Yahoo

Zie [https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters](https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters).

## Yahoo! Japan voegt dynamische volgende parameters toe

Zie [https://help.marketing.yahoo.co.jp/en/?p=115](https://help.marketing.yahoo.co.jp/en/?p=115).

## Dynamische volgparameters van Yandex

Zie [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [Over het bijhouden van klikken op URL-indelingen voor de service voor het bijhouden van Adobe-advertenties](/help/search-social-commerce/tracking/formats-click-tracking-about.md)

