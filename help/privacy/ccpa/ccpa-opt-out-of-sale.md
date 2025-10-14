---
title: Adobe Advertising support for the California Consumer Privacy Act &#58; Consumer Opt-Out-of-Sale Support
description: Meer informatie over ondersteuning voor het vastleggen van aanvragen voor een opt-out voor consumenten.
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 0%

---

# Adobe Advertising Support for the California Consumer Privacy Act: Consumer Opt-Out of Sale Support

*voor Adobe Advertising Demand Side Platform (DSP)*

>[!IMPORTANT]
>
>De inhoud van dit document is geen juridisch advies en is niet bedoeld ter vervanging van juridisch advies. Raadpleeg uw juridische adviseur voor advies over de California Consumer Privacy Act.

De California Consumer Privacy Act (CCPA) is de nieuwe privacywet van Californië, die op 1 januari 2020 van kracht is. CCPA verleent de inwoners van Californië nieuwe rechten met betrekking tot hun persoonlijke informatie en legt gegevensbeschermingstaken op aan bepaalde entiteiten die zaken in Californië leiden. De CCPA verleent consumenten het recht om toegang te krijgen tot hun gegevens en deze te verwijderen, alsook het recht om zich te onthouden van bepaalde activiteiten die als &quot;verkoop&quot; van persoonlijke informatie aan derden worden aangemerkt.

Als bedrijf, zult u de persoonlijke gegevens bepalen die Adobe Experience Cloud verwerkt en namens u opslaat.

Als uw dienstverlener, verleent Adobe Advertising steun voor uw zaken om aan zijn verplichtingen in het kader van CCPA te voldoen die op het gebruik van de producten en de diensten van Adobe Advertising van toepassing zijn, met inbegrip van het beheren van consumentenverzoeken om toegang tot en schrapping van persoonlijke informatie en het beheren van consumentenverzoeken om zich uit de verkoop van persoonlijke informatie te sluiten.

In dit document wordt beschreven hoe Adobe Advertising Demand Side Platform (DSP) als dienstverlener het recht van de consument steunt om zich te onthouden van de &quot;verkoop&quot; van &quot;persoonlijke informatie&quot;, zoals elke term door de CCPA wordt gedefinieerd. Het bevat informatie over de manier waarop u aanvragen om te weigeren aan Adobe Advertising kunt doorgeven en over de manier waarop u rapporten kunt ophalen over de verzoeken van uw organisatie om zich af te melden.

Voor informatie over hoe [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; en [!DNL Advertising DCO] de toegang en de schrappingsrechten van de persoonlijke informatie van consumenten steunen, zie [&#x200B; Steun van Adobe Advertising voor de Wet van de Privacy van de consument van Californië: De Toegang van de Gegevens van de consument en de Steun van de Schrapping &#x200B;](/help/privacy/ccpa/ccpa-access-delete.md).

Voor meer informatie over de diensten van de Privacy van Adobe voor CCPA, zie het [&#x200B; Centrum van de Privacy van Adobe &#x200B;](https://www.adobe.com/privacy/ccpa.html).

## Communiceren van consumentenverzoeken om niet langer te verkopen aan Adobe Advertising

Je kunt de aanvraag voor een opt-out bij verkoop aan de consument doorgeven met behulp van:

* een in Advertising DSP tot stand gekomen opt-out-of-sales-segment van de CCPA
* de Adobe Experience Platform Privacy Service API

### Methode 1: Communiceer CCPA uit-van-verkoop verzoeken gebruikend een [!UICONTROL CCPA Opt-Out-of-Sale] Segment in Advertising DSP

>[!NOTE]
>
>De gebruikers blijven in opt-out van CCPA-segmenten voor onbepaalde tijd.

1. Teken binnen aan de rekening van adverteerder in Advertising DSP in [&#x200B; https://advertising.adobe.com/ &#x200B;](https://advertising.adobe.com/).

1. [&#x200B; creeer een opt-out-of-verkoop CCPA segment, en voer het segmentpixel uit om de opt-out verzoeken &#x200B;](/help/dsp/audiences/ccpa-opt-out-segment-create.md) te vangen.

### Methode 2: Communiceer CCPA uit-van-verkoop verzoeken gebruikend Adobe Experience Platform Privacy Service API

*Advertisers toegewezen slechts een organisatieidentiteitskaart van Adobe Experience Cloud*

1. Implementeer een JavaScript-bibliotheek om de cookies van uw klant op te halen. Dezelfde bibliotheek, `AdobePrivacy.js` , wordt gebruikt voor alle Adobe Experience Cloud-oplossingen.

   >[!IMPORTANT]
   >
   >Voor aanvragen bij sommige Adobe Experience Cloud-oplossingen is de JavaScript-bibliotheek niet vereist, maar aanvragen bij Adobe Advertising vereisen deze bibliotheek.

   U moet de bibliotheek implementeren op de webpagina van waaruit uw klanten aanvragen voor een opt-out-of--verkoop kunnen indienen, zoals het privacyportaal van uw bedrijf. De bibliotheek helpt u bij het ophalen van Adobe-cookies (naamruimte-id: `gsurferID` ), zodat u deze id&#39;s kunt verzenden als onderdeel van een aanvraag voor een opt-out of-sale via de Adobe Experience Platform Privacy Service API.

1. Identificeer uw organisatie-id van Experience Cloud en zorg ervoor dat deze is gekoppeld aan uw Adobe Advertising-accounts.

   Een Experience Cloud-organisatie-id is een alfanumerieke tekenreeks van 24 tekens die wordt toegevoegd met &quot;@AdobeOrg&quot;. Aan de meeste Experience Cloud-klanten is een organisatie-id toegewezen. Neem contact op met uw Adobe-accountteam als uw marketingteam of de interne Adobe-systeembeheerder uw organisatie-id niet kent of niet zeker weet of deze is ingericht. U hebt de organisatie-id nodig om aanvragen naar de privacy-API te verzenden met behulp van de naamruimte `imsOrgID` .

   >[!IMPORTANT]
   >
   >Neem contact op met de Adobe Advertising-vertegenwoordiger van uw bedrijf om te bevestigen dat alle Adobe Advertising-accounts van uw organisatie, inclusief [!DNL DSP] accounts of adverteerders, [!DNL Search, Social, & Commerce] accounts en [!DNL Creative] - zijn gekoppeld aan uw Experience Cloud-organisatie-id. [!DNL DCO]

1. Gebruik Adobe Experience Platform Privacy Service API om opt-out van-verkoop verzoeken [&#128279;](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html?lang=nl-NL) aan Adobe Advertising namens consumenten voor te leggen, en de status van bestaande verzoeken te controleren.

   Zie de bijlage hieronder voor een voorbeeld van een &quot;opt-out&quot;-verzoek.

   >[!NOTE]
   >
   >Als uw bedrijf meerdere Experience Cloud-organisatie-id&#39;s heeft, moet u voor elke id een afzonderlijke API-aanvraag verzenden. U kunt echter één API-aanvraag indienen voor meerdere Adobe Advertising-suboplossingen ( [!DNL Search, Social, & Commerce] , [!DNL Creative] , [!DNL DSP] en [!DNL DCO] ) met één account per suboplossing.

Al deze stappen zijn nodig om steun van Adobe Advertising te ontvangen. Voor meer informatie over deze en andere verwante taken moet u het gebruiken van Adobe Experience Platform Privacy Service uitvoeren, en waar te om de noodzakelijke punten te vinden, [&#x200B; https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=nl-NL &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=nl-NL) zien.

## Rapporten ophalen van consumenten die verzoeken om niet-te verkopen hebben ingediend

Adobe Advertising genereert maandelijkse rapporten met id&#39;s die klanten hebben ingediend voor een aanvraag om te weigeren te verkopen voor de account. Elk rapport is beschikbaar als een tekstbestand met tabs als scheidingsteken en gecomprimeerd in de GZIP-indeling. De gegevens consolideren aanvragen die zijn vastgelegd met CCPA-opt-out-of-sales-segmenten die in Advertising DSP zijn gemaakt en alle aanvragen die via de Privacy Service API zijn ingediend. In de CCPA-opt-out-of-sales-segmenten vastgelegde gebruikers-id&#39;s worden per segment en per adverteerder geïdentificeerd. Rapporten worden gegenereerd op de eerste van elke maand voor de vorige maand. De maandelijkse gebruikerslijst voor juni is bijvoorbeeld beschikbaar op 1 juli.

U kunt koppelingen ophalen naar de maandelijkse rapporten die in de afgelopen drie maanden zijn gemaakt, vanuit Advertising DSP of met de Advertising DSP [!DNL Trafficking API] . Elke koppeling is zeven dagen geldig, maar wordt telkens vernieuwd wanneer een klant probeert een koppeling op te halen.

### Methode 1: Rapporten van de verkoopoptie voor consumenten in Advertising DSP ophalen

1. Teken binnen aan de rekening van adverteerder in Advertising DSP in [&#x200B; https://advertising.adobe.com/ &#x200B;](https://advertising.adobe.com/).

1. [&#x200B; wint de rapporten &#x200B;](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md) terug.

### Methode 2: Rapporten met de Advertising DSP ophalen voor uitverkoop aan de consument [!DNL Trafficking API]

Deze functie is beschikbaar voor organisaties die de [!DNL Trafficking API] gebruiken. Zie de documentatie voor [!DNL Trafficking API] voor meer informatie.<!-- Add link to API doc once it's published. -->

Neem contact op met uw Adobe-accountteam als uw organisatie de [!DNL Trafficking API] niet gebruikt, maar meer informatie wenst.

## Bijlage: Voorbeeld [!UICONTROL CCPA Opt-Out-of-Sale] Verzoek voor Privacy Service API-gebruikers

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["adCloud"],
    "regulation": "ccpa"
}'
```

waar, per de [&#x200B; specificaties van Privacy Service API &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-platform/privacy/api/appendix):

* `"namespace": "AdCloud"` geeft de `AdCloud` cookie-ruimte aan en de bijbehorende waarde is de cookie-id van de klant zoals opgehaald van `AdobePrivacy.js`
* `"include": ["adCloud"]` geeft aan dat de aanvraag van toepassing is op het product Adobe Advertising
