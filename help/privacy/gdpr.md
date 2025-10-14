---
title: Adobe Advertising-steun voor de algemene gegevensbeschermingsverordening
description: Meer informatie over de ondersteunde typen gegevensaanvragen, de vereiste instellingen en veldwaarden en voorbeelden van API-toegangsaanvragen met oude product-id's en geretourneerde gegevensvelden
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 8e9dac77b4f687fb175adaf27a4e726fa80ca7b4
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Adobe Advertising-steun voor de algemene gegevensbeschermingsverordening

*voor [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; en Adobe Advertising DCO*

>[!IMPORTANT]
>
>De inhoud van dit document is geen juridisch advies en is niet bedoeld ter vervanging van juridisch advies. Raadpleeg uw juridisch adviseur voor advies over de algemene verordening inzake gegevensbescherming.

De algemene gegevensbeschermingsverordening (GDPR), een wet die op 25 mei 2018 van kracht is, geeft alle personen (betrokkenen) binnen de grenzen van de Europese Unie (EU) controle op hun persoonsgegevens en vereenvoudigt het regelgevingskader voor het internationale bedrijfsleven. Deze wet is van toepassing op alle ondernemingen (voor de verwerking van persoonsgegevens verantwoordelijke personen) die goederen of diensten aanbieden, het gedrag van personen binnen de grenzen van de EU volgen of persoonsgegevens verzamelen op het tijdstip waarop hun persoonsgegevens worden verwerkt, ongeacht de bedrijfslocatie van de voor de verwerking verantwoordelijke.

Adobe Experience Cloud treedt op als een gegevensverwerker voor persoonlijke gegevens die het ontvangt en opslaat namens zijn klanten. Als gegevenscontroller bepaalt u de persoonlijke gegevens die Adobe Experience Cloud voor u verwerkt en opslaat.

In dit document wordt beschreven hoe [!DNL Advertising Search, Social, & Commerce] ; Advertising Creative; Advertising DSP (Demand Side Platform); en [!DNL Advertising DCO] de toegangsrechten tot en verwijdering van GDPR-gegevens van de betrokkenen ondersteunen met de interface van Adobe Experience Platform Privacy Service API en Privacy Service.

Voor meer informatie over wat GDPR voor uw zaken betekent, zie [&#x200B; GDPR en Uw Zaken &#x200B;](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Ondersteunde gegevenstypen voor Adobe Advertising

Adobe Experience Platform biedt bedrijven de mogelijkheid om de volgende taken uit te voeren:

* Open gegevens op cookieniveau of gegevens op id-niveau van een apparaat (voor advertenties in mobiele apps) op [!DNL Search, Social, & Commerce] , [!DNL Creative] , [!DNL DSP] of [!DNL DCO] .
* Verwijder gegevens op cookieniveau die zijn opgeslagen in [!DNL Search, Social, & Commerce] , [!DNL Creative] , [!DNL DSP] of [!DNL DCO] voor betrokkenen met behulp van een browser, of verwijder de gegevens op ID-niveau die zijn opgeslagen in [!DNL DSP] voor betrokkenen met behulp van apps op mobiele apparaten.
* Controleer de status van een of alle bestaande aanvragen.

## Vereiste installatie voor het verzenden van aanvragen voor Adobe Advertising

Als u toegang tot gegevens voor Adobe Advertising wilt aanvragen en deze wilt verwijderen, moet u:

1. Implementeer een JavaScript-bibliotheek om cookies van het gegevenssubject op te halen en te verwijderen. Dezelfde bibliotheek, `AdobePrivacy.js` , wordt gebruikt voor alle Adobe Experience Cloud-oplossingen.

   >[!IMPORTANT]
   >
   >Voor aanvragen bij sommige Experience Cloud-oplossingen is de JavaScript-bibliotheek niet vereist, maar aanvragen bij Adobe Advertising vereisen deze bibliotheek.

   U moet de bibliotheek op de webpagina plaatsen van waaruit uw betrokkenen toegang kunnen verzenden en aanvragen kunnen verwijderen, zoals het privacyportaal van uw bedrijf. De bibliotheek helpt u bij het ophalen van [!DNL Adobe] cookies (naamruimte-id: `gsurferID` ), zodat u deze id&#39;s kunt verzenden als onderdeel van toegangs- en verwijderaanvragen via de Adobe Experience Platform Privacy Service API.

   Wanneer de betrokkene om verwijdering van persoonsgegevens vraagt, verwijdert de bibliotheek ook het cookie van de betrokkene uit de browser van de betrokkene.

   >[!NOTE]
   >
   >Het schrappen van persoonlijke gegevens is verschillend dan uit Opt, die het richten van een eindgebruiker met publiekssegmenten tegenhoudt. Wanneer een gegevenssubject echter om persoonlijke gegevens uit [!DNL Creative] , [!DNL DSP] of [!DNL DCO] vraagt te verwijderen, verzendt de bibliotheek ook een verzoek aan Adobe Advertising om de betrokkene uit te schakelen van segmentgerichtheid. Voor adverteerders met [!DNL Search, Social, & Commerce], adviseren wij dat u de gegevensproefpersonen een verbinding aan [&#x200B; https://www.adobe.com/privacy/opt-out.html &#x200B;](https://www.adobe.com/privacy/opt-out.html) verstrekt, die verklaart hoe te om uit doelgericht van het publiekssegment te kiezen.

1. Identificeer uw Experience Cloud-organisatie-id en zorg ervoor dat deze is gekoppeld aan uw Adobe Advertising-accounts.

   Een Experience Cloud-organisatie-id is een alfanumerieke tekenreeks van 24 tekens die wordt toegevoegd met &quot;@AdobeOrg&quot;. Aan de meeste Experience Cloud-klanten is een organisatie-id toegewezen. Als uw marketingteam of interne [!DNL Adobe] systeembeheerder uw organisatie-id niet kent of niet zeker weet of deze is ingericht, neemt u contact op met de klantenservice van Adobe op gdprsupport@adobe.com. U hebt de organisatie-id nodig om aanvragen naar de privacy-API te verzenden met behulp van de naamruimte `imsOrgID` .

   >[!IMPORTANT]
   >
   >Neem contact op met de Adobe Advertising-vertegenwoordiger van uw bedrijf om te bevestigen dat alle Adobe Advertising-accounts van uw organisatie, inclusief [!DNL DSP] accounts of adverteerders, [!DNL Search, Social, & Commerce] accounts en [!DNL Creative] - zijn gekoppeld aan uw Experience Cloud-organisatie-id. [!DNL DCO]

1. Gebruik of [&#x200B; Adobe Experience Platform Privacy Service API &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html?lang=nl-NL) (voor geautomatiseerde verzoeken) of [&#x200B; Privacy Service UI &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=nl-NL) (voor ad-hocverzoeken) om toegang en schrappingsverzoeken aan Adobe Advertising namens de gegevensproefpersonen voor te leggen, en de status van bestaande verzoeken te controleren.

   Voor adverteerders die een mobiele app hebben om te communiceren met betrokkenen en campagnes te starten met DSP, moet u de voor privacy geschikte mobiele SDK&#39;s voor Experience Cloud downloaden. Met de Mobile SDK&#39;s kunnen gegevenscontrollers de statusmarkeringen voor weigeren instellen, de apparaat-id van de betrokkene (naamruimte-id: `deviceID` ) ophalen en aanvragen naar de Privacy Service API verzenden. Voor uw mobiele app is een SDK versie 4.15.0 of hoger vereist.

   Wanneer u het toegangsverzoek van een betrokkene verzendt, retourneert de Privacy Service API de gegevens van de betrokkene op basis van de opgegeven cookie of apparaat-id, die u vervolgens moet terugsturen naar de betrokkene.

   Wanneer u het verwijderingsverzoek van een betrokkene verzendt, worden de cookie-id of apparaat-id en alle kosten, klik en inkomstengegevens die bij het cookie horen, van de server verwijderd.

   >[!NOTE]
   >
   >Als uw bedrijf meerdere Experience Cloud-organisatie-id&#39;s heeft, moet u afzonderlijke API-aanvragen voor elke id verzenden. U kunt echter één API-aanvraag indienen voor meerdere Adobe Advertising-suboplossingen ( [!DNL Search, Social, & Commerce] , [!DNL Creative] , [!DNL DSP] en [!DNL DCO] ) met één account per suboplossing.

Alle stappen zijn nodig voor Adobe Advertising. Voor meer informatie over deze en andere verwante taken moet u het gebruiken van Adobe Experience Platform Privacy Service uitvoeren, en waar te om de noodzakelijke punten te vinden, zie &quot;[&#x200B; overzicht van Privacy Service &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=nl-NL).&quot;

## Vereiste veldwaarden in Adobe Advertising JSON-verzoeken

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*uw organisatieidentiteitskaart van Experience Cloud*>

`"users":`

* `"key":` &lt;*gewoonlijk de naam van het gegevenssubject*>

* `"action":` either `**access**` or `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (geeft de [!DNL adcloud] cookie-ruimte aan)

   * `"value":` &lt;*de waarde van de koekjesidentiteitskaart van de daadwerkelijke betrokkene zoals teruggewonnen van`AdobePrivacy.js`*>

* `"include": **adCloud**` (dit is het [!DNL Adobe] -product dat van toepassing is op de aanvraag)

* `"regulation": **gdpr**` (dit is de privacyverordening die van toepassing is op het verzoek)

## Voorbeeld van een aanvraag die is ingediend door de betrokkene met een Adobe Advertising-gebruikersnaam die is opgehaald uit `AdobePrivacy.js`

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
    "regulation":"gdpr"
}
```

## Gegevensvelden die worden geretourneerd voor toegangsverzoeken

Hieronder ziet u een voorbeeld van een toegangsreactie voor Adobe Advertising.

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

<!-- Changed example from BlueKai (no longer supported) to Exelate -->
