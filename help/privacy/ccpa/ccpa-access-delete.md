---
title: Adobe Advertising support for the California Consumer Privacy Act &#58; Consumer Data Access and Delete Support
description: Leer meer over de ondersteunde typen gegevensaanvragen, de vereiste instellingen en veldwaarden en voorbeelden van API-toegangsaanvragen met oude product-id's en geretourneerde gegevensvelden.
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
source-git-commit: 97e0f562153983202a2f3641e17dd682ff3d00ea
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 0%

---

# Adobe Advertising Support for the California Consumer Privacy Act: Consumer Data Access and Delete Support

*voor [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; en Adobe Advertising DCO*

>[!IMPORTANT]
>
>De inhoud van dit document is geen juridisch advies en is niet bedoeld ter vervanging van juridisch advies. Raadpleeg uw juridische adviseur voor advies over de California Consumer Privacy Act.

De California Consumer Privacy Act (CCPA) is de nieuwe privacywet van Californië, die op 1 januari 2020 van kracht is. CCPA verleent de inwoners van Californië nieuwe rechten met betrekking tot hun persoonlijke informatie en legt gegevensbeschermingstaken op aan bepaalde entiteiten die zaken in Californië leiden. De CCPA verleent consumenten het recht om hun persoonlijke gegevens te raadplegen en te verwijderen, alsmede het recht om af te zien van bepaalde activiteiten die als &quot;verkoop&quot; van persoonlijke gegevens aan derden worden aangemerkt.

Als bedrijf, zult u de persoonlijke gegevens bepalen die Adobe Experience Cloud verwerkt en namens u opslaat.

Als uw dienstverlener, verleent Adobe Advertising steun voor uw zaken om aan zijn verplichtingen in het kader van CCPA te voldoen die op het gebruik van de producten en de diensten van Adobe Advertising van toepassing zijn, met inbegrip van het beheren van verzoeken om toegang tot en schrapping van persoonlijke informatie en het beheren van verzoeken om zich uit de verkoop van persoonlijke informatie te sluiten.

In dit document wordt beschreven hoe [!DNL Advertising Search, Social, & Commerce] , Advertising Creative, Advertising DSP (Demand Side Platform) en [!DNL Advertising DCO] (als serviceproviders) het recht van consumenten op toegang tot en verwijdering van persoonlijke gegevens met de Adobe [!DNL Experience Platform Privacy Service API] en [!DNL Privacy Service UI] ondersteunen.

Voor informatie over hoe Advertising DSP het recht van de consument steunt om van de verkoop van persoonlijke informatie te sluiten, zie [ Steun van Adobe Advertising voor de Wet van de Privacy van de consument van Californië: De Steun van de Opt-out van de consument ](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

Voor meer informatie over de diensten van de Privacy van Adobe voor CCPA, zie het [ Centrum van de Privacy van Adobe ](https://www.adobe.com/privacy/ccpa.html).

## Ondersteunde gegevenstypen voor Adobe Advertising

Adobe Experience Platform biedt bedrijven de mogelijkheid om de volgende taken uit te voeren:

* Gebruik gegevens op cookieniveau of gegevens op ID-niveau van een consument (voor advertenties in mobiele apps) in [!DNL Search, Social, & Commerce] , [!DNL Creative] , [!DNL DSP] of [!DNL DCO] .
* Verwijder gegevens op cookieniveau die zijn opgeslagen in [!DNL Search, Social, & Commerce] , [!DNL Creative] , [!DNL DSP] of [!DNL DCO] voor consumenten die een browser gebruiken, of verwijder de gegevens op ID-niveau die zijn opgeslagen in [!DNL DSP] voor consumenten die apps op mobiele apparaten gebruiken.
* Controleer de status van een of alle bestaande aanvragen.

## Vereiste installatie voor het verzenden van aanvragen voor Adobe Advertising

Om verzoeken tot toegang tot en verwijdering van persoonlijke gegevens van consumenten uit Adobe Advertising in te dienen, moet u:

1. Implementeer een JavaScript-bibliotheek om de cookies van uw klant op te halen en te verwijderen. Dezelfde bibliotheek, `AdobePrivacy.js` , wordt gebruikt voor alle Adobe Experience Cloud-oplossingen.

   >[!IMPORTANT]
   >
   >Voor aanvragen bij sommige Experience Cloud-oplossingen is de JavaScript-bibliotheek niet vereist, maar aanvragen bij Adobe Advertising vereisen deze bibliotheek.

   U zou de bibliotheek op de webpagina moeten opstellen waarvan uw klanten toegang en schrappingsverzoeken, zoals het privacyportaal van uw bedrijf kunnen voorleggen. De bibliotheek helpt u bij het ophalen van Adobe-cookies (naamruimte-id: `gsurferID` ), zodat u deze id&#39;s kunt verzenden als onderdeel van toegangs- en verwijderaanvragen via [!DNL Adobe Experience Platform Privacy Service API] .

   Wanneer de klant vraagt om persoonlijke gegevens te verwijderen, verwijdert de bibliotheek ook het cookie van de klant uit de browser van de klant.

   >[!NOTE]
   >
   >Het verwijderen van persoonlijke gegevens is anders dan het uitschakelen van gegevens, waardoor een eindgebruiker niet meer doelgericht met publiekssegmenten werkt. Wanneer een klant echter om het verwijderen van persoonlijke gegevens uit [!DNL Creative] , [!DNL DSP] of [!DNL DCO] vraagt, verzendt de bibliotheek ook een verzoek aan Adobe Advertising om de klant te weigeren zich te richten op een segment. Voor adverteerders met [!DNL Search, Social, & Commerce], adviseren wij dat u uw klanten een verbinding aan [ https://www.adobe.com/privacy/opt-out.html#customeruse ](https://www.adobe.com/privacy/opt-out.html#customeruse) verstrekt, die verklaart hoe te om uit doelgericht van het publiekssegment te kiezen.

1. Identificeer uw organisatie-id van Experience Cloud en zorg ervoor dat deze is gekoppeld aan uw Adobe Advertising-accounts.

   Een Experience Cloud-organisatie-id is een alfanumerieke tekenreeks van 24 tekens die wordt toegevoegd met &quot;@AdobeOrg&quot;. Aan de meeste Experience Cloud-klanten is een organisatie-id toegewezen. Neem contact op met uw Adobe-accountteam als uw marketingteam of de interne [!DNL Adobe] -systeembeheerder uw organisatie-id niet kent of niet zeker weet of er provisioned is geweest. U hebt de organisatie-id nodig om aanvragen naar de privacy-API te verzenden met behulp van de naamruimte `imsOrgID` .

   >[!IMPORTANT]
   >
   >Neem contact op met de Adobe Advertising-vertegenwoordiger van uw bedrijf om te bevestigen dat alle Adobe Advertising-accounts van uw organisatie, inclusief [!DNL DSP] accounts of adverteerders, [!DNL Search, Social, & Commerce] accounts en [!DNL Creative] - zijn gekoppeld aan uw Experience Cloud-organisatie-id. [!DNL DCO]

1. Gebruik of [ Adobe Experience Platform Privacy Service API ](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (voor geautomatiseerde verzoeken) of [ Privacy Service UI ](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (voor ad-hocverzoeken) om verzoeken om tot en schrapping persoonlijke informatie aan Adobe Advertising namens consumenten toegang te hebben, en de status van bestaande verzoeken te controleren.

   Voor adverteerders die een mobiele app hebben om te communiceren met klanten en campagnes te starten met [!DNL DSP] , moet u de voor privacy geschikte mobiele SDK&#39;s voor Experience Cloud downloaden. Met de Mobile SDK&#39;s kunnen bedrijven statusmarkeringen voor weigeren instellen, de apparaat-id van de consument (naamruimte-id: `deviceID` ) ophalen en aanvragen naar de Privacy Service API verzenden. Voor uw mobiele app is een SDK versie 4.15.0 of hoger vereist.

   Wanneer u een verzoek om toegang voor de consument indient, retourneert de Privacy Service API de informatie van de consument op basis van de opgegeven cookie of apparaat-id, die u vervolgens aan de consument moet retourneren.

   Wanneer u een verzoek tot verwijdering van een consument indient, worden de cookie-id of apparaat-id en alle kosten, klik en inkomstengegevens die bij het cookie horen, van de server verwijderd.

   >[!NOTE]
   >
   >Als uw bedrijf meerdere Experience Cloud-organisatie-id&#39;s heeft, moet u voor elke id een afzonderlijke API-aanvraag verzenden. U kunt echter één API-aanvraag indienen voor meerdere Adobe Advertising-suboplossingen ( [!DNL Search, Social, & Commerce] , [!DNL Creative] , [!DNL DSP] en [!DNL DCO] ) met één account per suboplossing.

Alle stappen zijn nodig om steun van Adobe Advertising te ontvangen. Voor meer informatie over deze en andere verwante taken moet u het gebruiken van Adobe Experience Platform Privacy Service uitvoeren, en waar te om de noodzakelijke punten te vinden, [ https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html ](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html) zien.

## Vereiste veldwaarden in Adobe Advertising JSON-verzoeken

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*uw organisatieidentiteitskaart van Experience Cloud*>

&quot;gebruikers&quot;:

* `"key":` &lt;*gewoonlijk de naam van de klant*>

* `"action":` either `**access**` or `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (geeft de [!DNL adCloud] cookie-ruimte aan)

   * `"value":` &lt;*de waarde van de de koekjesidentiteitskaart van de daadwerkelijke klant zoals die van`AdobePrivacy.js`* wordt teruggewonnen>

* `"include": **adCloud**` (dit is het [!DNL Adobe] -product dat van toepassing is op de aanvraag)

* `"regulation": **ccpa**` (dit is de privacyverordening die van toepassing is op het verzoek)

## Voorbeeld van een aanvraag die door een consument is ingediend met een Adobe Advertising-gebruikersnaam die is opgehaald van AdobePrivacy.js

```
{
"companyContexts":[
    {
        "namespace":"imsOrgID",
        "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
 "userIDs":[
      { 
        "namespace":"411",
        "value":"Wqersioejr-wdg",
        "type":"namespaceId",
        "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"ccpa"
}
```

## Gegevensvelden die worden geretourneerd voor toegangsverzoeken

Hieronder ziet u een voorbeeld van een reactie van Adobe Advertising op de toegang tot persoonlijke gegevens.

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"eXelate Australia Demographic - Jobs & Education - Job Seekers",
                    "segmentID":"2213789",
                    "serviceProvider":"exelate"
                }
            ]
        }
    }
}
```
