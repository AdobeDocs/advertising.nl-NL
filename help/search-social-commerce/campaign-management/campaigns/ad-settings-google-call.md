---
title: '[!DNL Google Ads] alleen-aanroepen advertentie-instellingen'
description: Verwijs naar de instellingen voor [!DNL Google Ads] alleen-aanroepadvertenties.
exl-id: 1f810c2b-9c30-43c6-bda6-07609423ef79
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# [!DNL Google Ads] alleen-aanroepbare advertentie-instellingen

U kunt vraag-slechts tekstadvertenties voor campagnes tot stand brengen die het onderzoeksnetwerk gebruiken.

Zoek, Sociale, &amp; Handel volgt vraag-slechts advertenties gebruikend het account-vlakke het landen paginaachtervoegsel en het volgen malplaatje, maar u kunt naar keuze het rekening-vlakke volgen op het advertentieniveau binnen met voeten treden [!DNL Google Ads] Manager.

Zie de [!DNL Google Ads] hulp voor [advertentiegrenzen per account](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** De naam van het bedrijf. De maximumlengte is 25 tekens of 12 double-byte tekens.

**[!UICONTROL Country]:** (Optioneel) Het land waar het bedrijf is gevestigd.

**[!UICONTROL Phone Number]:** Het telefoonnummer voor het bedrijf. Voorbeelden: (124) 123-4567, 12345678901, +441234567890.

**[!UICONTROL Description 1], [!UICONTROL Description 2]:** De eerste en tweede regel van de advertentie. De maximumlengte voor elke regel is 35 tekens of 17 double-byte tekens.

De syntaxis voor het vervangen van trefwoorden telt niet mee voor de maximale lengte. Bijvoorbeeld &quot;`{Description1: Free Account Analysis!}`&quot; wordt behandeld als 22 tekens (alleen het gedeelte &quot;Free Account Analysis\!&quot;).

>[!NOTE]
>
>De beschrijvingsvelden mogen geen telefoonnummers bevatten.

**[!UICONTROL Display URL]:** De URL die wordt weergegeven in de advertentie. De weergave-URL moet overeenkomen met een domein dat aan uw bedrijf is gekoppeld, maar de advertentie verzendt geen personen naar een bestemmingspagina.

De maximumlengte is 35 single-byte of 17 double-byte tekens. De syntaxis voor het vervangen van trefwoorden telt niet mee voor de maximale lengte. Bijvoorbeeld &quot;`{DisplayURL: example.com}`&quot; wordt behandeld als 11 tekens (alleen het gedeelte &quot;example.com&quot;).

**[!UICONTROL Verification URL]:** (Optioneel) Een webpagina waarop het telefoonnummer van de advertentie als tekst wordt weergegeven, zodat [!DNL Google Ads] kan verifiëren dat het telefoonaantal geldig is. De URL moet hetzelfde domein hebben als de URL van de weergave van de advertentie.

**[!UICONTROL Is Tracked]:** Laat vraag het volgen en vraag-slechts omzettingen toe.

**[!UICONTROL Count calls as phone call conversions]:** (Wanneer &quot;[!UICONTROL Is Tracked]&quot; wordt geselecteerd; facultatief) kenmerkt alle vraag die uit de advertentie aan een specifiek type van telefoonomzetting voortvloeit, wanneer één wordt gespecificeerd. Anders, [!DNL Google Ads] Hiermee wordt een standaardconversieactie gemaakt met de naam &quot;[!UICONTROL Calls from ads]&quot; zodra het minstens één omzetting van uw het door:sturen aantallen registreert, en dan attributen roept aan het.

**[!UICONTROL Count Action]:** (Wanneer &quot;[!UICONTROL Count calls as phone call conversions]&quot; is geselecteerd; optioneel) De bestaande conversieactie waaraan aanroepen worden toegewezen.

U kunt conversieacties maken en beheren binnen [!DNL Google Ads].

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [Over advertenties](ad-about.md)
>* [Advertenties beheren](ad-manage.md)
>* [[!DNL Google Ads] uitgebreide dynamische zoekopdrachten en instellingen](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] responsieve zoekopdrachten en instellingen](ad-settings-google-rsa.md)
