---
title: 'Steun van de Adobe Advertising voor de California Consumer Privacy Act: Ondersteuning van de consument'
description: Meer informatie over ondersteuning voor het vastleggen van aanvragen voor een opt-out voor consumenten.
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: 7378ea6e6907aa4067bd3e73160a8e71c925ec9d
workflow-type: tm+mt
source-wordcount: '988'
ht-degree: 0%

---

# Adobe Advertising Support for the California Consumer Privacy Act: Consumer Opt-Out of Sale Support

*Voor Demand Side Platform Adobe Advertising (DSP)*

>[!IMPORTANT]
>
>De inhoud van dit document is geen juridisch advies en is niet bedoeld ter vervanging van juridisch advies. Raadpleeg uw juridische adviseur voor advies over de California Consumer Privacy Act.

De California Consumer Privacy Act (CCPA) is de nieuwe privacywet van Californië, die op 1 januari 2020 van kracht is. CCPA verleent de inwoners van Californië nieuwe rechten met betrekking tot hun persoonlijke informatie en legt gegevensbeschermingstaken op aan bepaalde entiteiten die zaken in Californië leiden. De CCPA verleent consumenten het recht om toegang te krijgen tot hun gegevens en deze te verwijderen, alsook het recht om zich te onthouden van bepaalde activiteiten die als &quot;verkoop&quot; van persoonlijke informatie aan derden worden aangemerkt.

Als bedrijf, zult u de persoonlijke gegevens bepalen die Adobe Experience Cloud verwerkt en namens u opslaat.

Als uw dienstverlener, verleent de Adobe Advertising steun voor uw zaken om aan zijn verplichtingen in het kader van CCPA te voldoen die op het gebruik van de producten en de diensten van de Adobe Advertising van toepassing zijn, met inbegrip van het beheren van consumentenverzoeken om toegang tot en schrapping van persoonlijke informatie en het beheren van consumentenverzoeken om zich uit de verkoop van persoonlijke informatie te sluiten.

In dit document wordt beschreven hoe het Demand Side Platform van de Adobe Advertising (DSP), als dienstverlener, het recht van de consument steunt om zich te onthouden van de &quot;verkoop&quot; van &quot;persoonlijke informatie&quot;, aangezien elke term door de CCPA wordt gedefinieerd. Het omvat informatie over hoe te om opt-out van-of-verkoop verzoeken aan Adobe Advertising mee te delen en hoe te om rapporten van de opt-out van uw organisatie verzoeken terug te winnen.

Voor informatie over hoe [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; en [!DNL Advertising DCO] ondersteuning van de rechten van de consument op het gebied van toegang tot en verwijdering van persoonsgegevens , zie [Adobe Advertising Support for the California Consumer Privacy Act: Consumer Data Access and Delete Support](/help/privacy/ccpa/ccpa-access-delete.md).

Voor meer informatie over de diensten van de Privacy van de Adobe voor CCPA, zie [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Het meedelen van de Verzoeken van de Consumenten van de Opt-out van de Verkoop aan Adobe Advertising

Je kunt de aanvraag voor een opt-out bij verkoop aan de consument doorgeven met behulp van:

* een opt-out-of-sales-segment van de CCPA dat in DSP is gecreëerd
* de Adobe Experience Platform Privacy Service API

### Methode 1: Communiceer CCPA uit-van-verkoop verzoeken gebruikend een [!UICONTROL CCPA Opt-Out-of-Sale] Segment in DSP

>[!NOTE]
>
>De gebruikers blijven in opt-out van CCPA-segmenten voor onbepaalde tijd.

1. Meld u aan bij de account van de adverteerder in DSP op [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Creeer een opt-out van CCPA van verkoop segment, en voer het segmentpixel uit om de opt-out verzoeken te vangen](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Methode 2: Communiceer CCPA uit-van-verkoop verzoeken gebruikend Adobe Experience Platform Privacy Service API

*Adverteerders hebben alleen een Adobe Experience Cloud-organisatie-id toegewezen*

1. Implementeer een JavaScript-bibliotheek om de cookies van uw klant op te halen. Dezelfde bibliotheek, `AdobePrivacy.js`, wordt gebruikt voor alle Adobe Experience Cloud-oplossingen.

   >[!IMPORTANT]
   >
   >Voor aanvragen bij sommige Adobe Experience Cloud-oplossingen is de JavaScript-bibliotheek niet vereist, maar voor aanvragen bij Adobe Advertising is deze vereist.

   U moet de bibliotheek implementeren op de webpagina van waaruit uw klanten aanvragen voor een opt-out-of--verkoop kunnen indienen, zoals het privacyportaal van uw bedrijf. Met de bibliotheek kunt u Adobe cookies ophalen (naamruimte-id: `gsurferID`), zodat u deze identiteiten kunt verzenden als onderdeel van een &quot;opt-out&quot;-aanvraag via de Adobe Experience Platform Privacy Service API.

1. Identificeer uw organisatie-ID van het Experience Cloud en zorg ervoor dat het met uw rekeningen van de Adobe Advertising verbonden is.

   Een organisatie-id voor een Experience Cloud is een alfanumerieke tekenreeks van 24 tekens die wordt toegevoegd met &quot;@AdobeOrg&quot;. De meeste klanten van het Experience Cloud zijn toegewezen een organisatieidentiteitskaart Als uw marketing team of interne beheerder van het systeem van de Adobe uw organisatie identiteitskaart niet kent, of niet zeker als het provisioned is, dan contacteer uw Team van de Rekening van de Adobe. U hebt de organisatie-id nodig om aanvragen in te dienen bij de privacy-API met behulp van de `imsOrgID` naamruimte.

   >[!IMPORTANT]
   >
   >Neem contact op met de vertegenwoordiger van de Adobe Advertising van uw bedrijf om te bevestigen dat alle accounts van de Adobe Advertising van uw organisatie — inclusief [!DNL DSP] accounts of adverteerders, [!DNL Search, Social, & Commerce] rekeningen, en [!DNL Creative] of [!DNL DCO] accounts — zijn gekoppeld aan de organisatie-id van uw Experience Cloud.

1. De Adobe Experience Platform Privacy Service API gebruiken om [indiening van &quot;opt-out&quot;-verzoeken](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) Adobe Advertising namens de consument en controle op de status van bestaande verzoeken.

   Zie de bijlage hieronder voor een voorbeeld van een &quot;opt-out&quot;-verzoek.

   >[!NOTE]
   >
   >Als uw bedrijf veelvoudige Experience Cloud organisatie IDs heeft, dan moet u afzonderlijke API verzoeken voor elk verzenden. U kunt echter één API-aanvraag indienen voor meerdere Adobe Advertising-suboplossingen ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], en [!DNL DCO]), met één rekening per suboplossing.

Al deze stappen zijn nodig om steun van Adobe Advertising te ontvangen. Ga voor meer informatie over deze en andere verwante taken die u moet uitvoeren met de Adobe Experience Platform Privacy Service en waar u de benodigde items kunt vinden naar [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Rapporten ophalen van consumenten die verzoeken om niet-te verkopen hebben ingediend

Adobe Advertising genereert maandelijkse rapporten van id&#39;s die klanten hebben ingediend voor een aanvraag om niet te verkopen voor de account. Elk rapport is beschikbaar als een tekstbestand met tabs als scheidingsteken en gecomprimeerd in de GZIP-indeling. De gegevens consolideren aanvragen die zijn vastgelegd met CCPA-opt-out-of-sales-segmenten die zijn gemaakt in DSP voor advertenties en alle opmerkingen die via de Privacy Service-API zijn ingediend. In de CCPA-opt-out-of-sales-segmenten vastgelegde gebruikers-id&#39;s worden per segment en per adverteerder geïdentificeerd. Rapporten worden gegenereerd op de eerste van elke maand voor de vorige maand. De maandelijkse gebruikerslijst voor juni is bijvoorbeeld beschikbaar op 1 juli.

U kunt koppelingen opvragen naar de maandelijkse rapporten die in de afgelopen drie maanden zijn gemaakt, vanuit DSP advertentie of via de DSP [!DNL Trafficking API]. Elke koppeling is zeven dagen geldig, maar wordt telkens vernieuwd wanneer een klant probeert een koppeling op te halen.

### Methode 1: Rapporten van de verkoopcommissie van de consument in DSP ophalen

1. Meld u aan bij de account van de adverteerder in DSP op [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [De rapporten ophalen](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Methode 2: Rapporten over het niet-verkopen van consumenten ophalen met behulp van de DSP [!DNL Trafficking API]

Deze functie is beschikbaar voor organisaties die de [!DNL Trafficking API]. Zie de documentatie voor de [!DNL Trafficking API] voor meer informatie .<!-- Add link to API doc once it's published. -->

Als uw organisatie de opdracht [!DNL Trafficking API] maar u hebt meer informatie nodig. Neem contact op met het accountteam van uw Adobe.

## Bijlage: Voorbeeld [!UICONTROL CCPA Opt-Out-of-Sale] Aanvraag voor Privacy Service API-gebruikers

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
            "namespace": "adCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["adCloud"],
    "regulation": "ccpa"
}'
```

waarbij:

* `"namespace": "adCloud"` Hiermee wordt de `adCloud` koekjesruimte, en de overeenkomstige waarde is de koekjesidentiteitskaart van de klant zoals die van wordt teruggewonnen `AdobePrivacy.js`
* `"include": ["adCloud"]` geeft aan dat het verzoek van toepassing is op Adobe Advertising
