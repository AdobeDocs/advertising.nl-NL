---
title: '[!DNL Google Ads] alleen-aanroepen en ad-instellingen'
description: Verwijzing de montages voor  [!DNL Google Ads]  vraag-slechts advertenties.
exl-id: 10672771-53fd-4ce9-9d67-6b1f8f5a41b8
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# [!DNL Google Ads] alleen-aanroepen en ad-instellingen

U kunt vraag-slechts tekstadvertenties voor campagnes tot stand brengen die het onderzoeksnetwerk gebruiken.

Zoek, sociale zaken en Commerce houdt alleen contact met advertenties via het achtervoegsel van de landingspagina op accountniveau en de sjabloon voor bijhouden, maar u kunt optioneel de opvolging op accountniveau op advertentieniveau in [!DNL Google Ads] Manager overschrijven.

Zie [!DNL Google Ads] hulp voor [ en grenzen per rekening ](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** De naam van de onderneming. De maximumlengte is 25 tekens of 12 double-byte tekens.

**[!UICONTROL Country]:** (Facultatief) het land waarin de zaken worden gevestigd.

**[!UICONTROL Phone Number]:** Het telefoonnummer voor het bedrijf. Voorbeelden: (124) 123-4567, 12345678901, +441234567890.

**[!UICONTROL Description 1], [!UICONTROL Description 2]:** De eerste en tweede lijn van het lichaam van de advertentie. De maximumlengte voor elke regel is 35 tekens of 17 double-byte tekens.

De syntaxis voor het vervangen van trefwoorden telt niet mee voor de maximale lengte. Bijvoorbeeld, &quot;`{Description1: Free Account Analysis!}`&quot;wordt behandeld als 22 karakters (slechts het gedeelte &quot;Vrije Analyse van de Rekening\!&quot;).

>[!NOTE]
>
>De beschrijvingsvelden mogen geen telefoonnummers bevatten.

**[!UICONTROL Display URL]:** URL die in de advertentie wordt getoond. De weergave-URL moet overeenkomen met een domein dat aan uw bedrijf is gekoppeld, maar de advertentie verzendt geen personen naar een bestemmingspagina.

De maximumlengte is 35 single-byte of 17 double-byte tekens. De syntaxis voor het vervangen van trefwoorden telt niet mee voor de maximale lengte. Bijvoorbeeld, &quot;`{DisplayURL: example.com}`&quot;wordt behandeld als 11 karakters (slechts het gedeelte &quot;example.com&quot;).

**[!UICONTROL Verification URL]:** (Facultatief) een webpagina waarop het telefoonaantal voor uw advertentie als tekst verschijnt, zodat [!DNL Google Ads] kan verifiëren dat het telefoonaantal geldig is. De URL moet hetzelfde domein hebben als de URL van de weergave van de advertentie.

**[!UICONTROL Is Tracked]:** laat vraag het volgen en vraag-slechts omzettingen toe.

**[!UICONTROL Count calls as phone call conversions]:** (Wanneer &quot;[!UICONTROL Is Tracked]&quot;wordt geselecteerd; facultatief) kenmerkt alle vraag die uit de advertentie aan een specifiek type van telefoongesprekomzetting voortvloeit, wanneer wordt gespecificeerd. Anders, leidt [!DNL Google Ads] tot een standaardomzettingsactie genoemd &quot;[!UICONTROL Calls from ads]&quot;zodra het minstens één omzetting van uw het door:sturen aantallen registreert, en dan attributen roept aan het.

**[!UICONTROL Count Action]:** (Wanneer &quot;[!UICONTROL Count calls as phone call conversions]&quot;wordt geselecteerd; facultatief) de bestaande omzettingsactie waaraan de vraag wordt toegeschreven.

U kunt conversieacties maken en beheren binnen [!DNL Google Ads] .

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [ Ongeveer advertenties ](ad-about.md)
>* [ beheert advertenties ](ad-manage.md)
>* [[!DNL Google Ads]  uitgevouwen dynamisch onderzoek en montages ](ad-settings-google-dsa.md)
>* [[!DNL Google Ads]  ontvankelijke onderzoek en montages ](ad-settings-google-rsa.md)
