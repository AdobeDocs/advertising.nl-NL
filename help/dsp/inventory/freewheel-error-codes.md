---
title: De codes van de fout voor  [!DNL FreeWheel]  plaatsen
description: Verwijs naar de foutencodes die voor advertentie aan  [!DNL FreeWheel] zijn teruggekeerd.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: e48937c2-ced9-4107-9e1d-65a3bac51fff
source-git-commit: a5be425ee34960cf58642cb850ae817998652f53
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 3%

---

# Foutcodes voor [!DNL FreeWheel] ad-hocreacties

De foutberichten voor mislukte advertenties kunnen afkomstig zijn van Advertising DSP of van [!DNL FreeWheel] . Foutberichten worden weergegeven in de kolom [!UICONTROL API Response] in het [[!UICONTROL Freewheel Status] dialoogvenster &#x200B;](freewheel-check-status.md) .

## Interne Advertising DSP-fouten

| Foutbericht | Beschrijving | Volgende stappen |
|--- |--- |--- |
| [!DNL Awaiting status response from [!DNL FreeWheel]] | [!DNL FreeWheel] heeft nog niet gereageerd dat het verzenden is gelukt of mislukt. | Controleer de status over 10 minuten opnieuw. |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] accepteert geen Britse advertenties zonder toegewezen kloknummers. | Wijs een kloknummer toe aan de advertentie en verzend de advertentie opnieuw. |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | De transcoder had het transcoderen van de advertentie niet gebeëindigd toen u probeerde om de advertentie voor te leggen. | Wacht tien minuten en verzend de advertentie opnieuw. |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | De voorgelegde overeenkomst wordt niet opgezet als programmatic gewaarborgde overeenkomst. [!DNL FreeWheel] accepteert alleen gegarandeerde deals. | Opstelling overeenkomstenidentiteitskaart als programmatic gewaarborgde overeenkomst. De advertentie wordt automatisch voorgelegd aan [!DNL FreeWheel] wanneer u sparen programmatic gewaarborgde standaardplaatsing aan het eind van het werkschema van identiteitskaart van de overeenkomst. |
| [!DNL Invalid external_deal_id:] \&lt;deal_id\> | De voorgelegde deal-id bestaat niet of is niet actief op het Adobe-einde. | Zorg ervoor dat de overeenkomst actief is, en verzend dan de advertentie opnieuw. |
| [!DNL \[public_id=]\&lt;deal\>] bestaat niet | De verzonden deal-id bestaat niet op het [!DNL FreeWheel] eind. | Neem contact op met uw [!DNL FreeWheel] -vertegenwoordiger om de deal-id te bevestigen. |
| [!DNL Ad with identifier] \&lt;*ad name*\> [!DNL was not found.] | De verzonden ad-toets bestaat niet of is niet actief aan de Adobe-zijde. | Zoek de juiste advertentiecode en verzend de advertentie opnieuw. |
| [!DNL Pending Submission] | De indiening is nog in behandeling. | Vernieuw de pagina. |

{style="table-layout:auto"}

## [!DNL Freewheel] API-fouten

| Code | Betekenis | Beschrijving | Volgende stappen |
|--- |--- |--- |--- |
| 401 | Ongeautoriseerd | Onjuiste, ontbrekende of ongeldige toegangsreferenties. | Neem contact op met uw Adobe-accountteam. |
| 403 | Verboden | De server begreep het verzoek maar weigert het te autoriseren. | Neem contact op met uw Adobe-accountteam. |
| 404 | Niet gevonden | De bron die u hebt aangevraagd, is niet beschikbaar. Als de Creative-id niet wordt gevonden in de PUT-bewerking, wordt een 404 geretourneerd. | Neem contact op met uw Adobe-accountteam. |
| 405 | Methode niet toegestaan | Er is een aanvraag ingediend voor een bron met behulp van een aanvraagmethode die niet door die bron wordt ondersteund (bijvoorbeeld GET gebruiken voor een methode waarbij gegevens moeten worden verzonden door POST of PUT gebruiken voor een alleen-lezen bron). | Neem contact op met uw Adobe-accountteam. |
| 408 | Tijdslimiet aanvraag | Er is een time-out opgetreden tijdens de verwerking van dit verzoek. De onderbrekingen worden gewoonlijk veroorzaakt door gezamenlijke verzoeken van exclusieve toegang tot bepaalde middelen. | Verzend het verzoek opnieuw wanneer u deze status ontvangt. Neem contact op met uw Adobe-accountteam als het probleem zich blijft voordoen. |
| 422 | Onbewerkbare entiteit | Ongeldige bron. Deze fout gebeurt wanneer het verzoeklichaam ongeldig is of het gecreeerde/bijgewerkte middel ongeldig is (bijvoorbeeld, als overeenkomst identiteitskaart niet werd gevonden). Zie [&#x200B; FreeWheel API 422 Fouten &#x200B;](#freewheel-422-errors) voor meer informatie. | Neem contact op met uw Adobe-accountteam. |
| 500 | Interne serverfout | API-systeemfout. | Neem contact op met uw Adobe-accountteam. |

{style="table-layout:auto"}

## [!DNL Freewheel] API 422-fouten {#freewheel-422-errors}

| Code | HTTP-code | Beschrijving |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | De aanvraaggegevens hebben een ongeldige JSON-indeling. Controleer het foutbericht voor meer informatie. |
| DATA_VALIDATION_FAILURE | 422 | De aanvraaggegevens ontbreken in de vereiste velden of hebben een ongeldig gegevenstype. Controleer het foutbericht voor meer informatie. |
| DATA_DEAL_INVALID | 422 | De overeenkomst wordt gevormd verkeerd of bestaat niet. Controleer het foutbericht voor meer informatie. |
| DATA_DEAL_GET_FAILURE | 422 | De overeenkomst werd niet gevonden of zijn configuratie heeft een kwestie. Controleer het foutbericht voor meer informatie. |
| DATA_CREATIVE_INGEST_FAILURE | 422 | De creatieve URL is ongeldig. Controleer het foutbericht voor meer informatie. |
| DATA_CREATIVE_LINK_FAILURE | 422 | De creatieve was niet verbonden met de knooppunten van de advertentie-eenheid van de deal. Controleer het foutbericht voor meer informatie. |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | De creatieve functie is niet bijgewerkt. Controleer het foutbericht voor meer informatie. |
| DATA_DSP_GET_FAILURE | 422 | De DSP bestaat niet binnen het systeem. |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | De creatieve objecten zijn niet losgekoppeld van advertentie-eenheden. |
| DATA_CREATIVE_DELETE_FAILURE | 422 | De creatieve functie is niet verwijderd. |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | De URL is niet gedetecteerd. |
| DATA_ENTITY_NOT_FOUND | 422 | De creatieve bestaat niet. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [&#x200B; Overzicht van vestiging programmatic gewaarborgde overeenkomsten in  [!DNL Freewheel]](/help/dsp/inventory/freewheel-overview.md)
>* [&#x200B; keur een overeenkomst in [!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md) goed
>* [&#x200B; voorlegt een advertentie voor een programmatic gewaarborgde overeenkomst aan  [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)
>* [&#x200B; Controle het statuut van advertenties voor de overeenkomst van a [!DNL FreeWheel]  PG &#x200B;](/help/dsp/inventory/freewheel-check-status.md)
