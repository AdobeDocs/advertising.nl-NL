---
title: Vereiste bulkbladgegevens voor  [!DNL Naver]  rekeningen
description: Verwijzing de vereiste kopbalgebieden en gegevensgebieden in bulksbladen voor  [!DNL Naver]  rekeningen.
exl-id: 1bfcdbb6-8026-4230-ab6b-b7c79b0d185a
feature: Search Bulksheets
source-git-commit: 7945887cf34c5ff390a35f1b9a6ede2888254c65
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 0%

---

# Bijlage - Vereiste bulksbladgegevens voor [!DNL Naver] -accounts

Vul uw [!DNL Naver] -accounts in Zoeken, Sociaal en Commerce door een bulksbladbestand te genereren in [!DNL Naver] en dit vervolgens te uploaden naar Zoeken, Sociaal en Commerce.

{{$include /help/_includes/bulksheet-appendices-intro.md}}

## Beschikbare gegevensvelden

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Veld | Campagne | Advertentiegroep | Trefwoord | Beschrijving |
|----|----|----|----|----|
| [!UICONTROL Platform] | nvt | nvt | nvt | (Opgenomen in gegenereerde bulksbladen ter informatie) Het advertentieplatform. Vereist, tenzij elke rij een AMO-id voor de entiteit bevat. |
| [!UICONTROL Acct Name] | Vereist/optioneel | Vereist/optioneel | Vereist/optioneel | De unieke naam die een advertentienetwerkaccount identificeert. Vereist, tenzij elke rij een AMO-id voor de entiteit bevat. |
| [!UICONTROL Campaign Name] | Vereist | Vereist | Vereist | De unieke naam die een campagne voor een account identificeert. |
| [!UICONTROL Ad Group Name] | nvt | Vereist | Vereist | De unieke naam die een advertentiegroep identificeert. |
| [!UICONTROL Keyword] | nvt | nvt | Vereist | De trefwoordtekenreeks. |
| [!UICONTROL Base URL] | nvt | nvt | Optioneel | De bestemmingspagina URL waaraan de eind - gebruikers worden genomen wanneer zij uw advertentie klikken, met inbegrip van om het even welke toevoegingsparameters die voor de campagne of de rekening worden gevormd.<br><br> Basis/definitieve URLs op het sleutelwoordniveau treedt URLs op het advertentieniveau en hoger met voeten. |
| [!UICONTROL Destination URL] | nvt | nvt | nvt | (Opgenomen in gegenereerde bulksbladen voor informatiedoeleinden; niet gepost naar het advertentienetwerk) Voor accounts met doel-URL&#39;s is deze waarde de URL die een advertentie koppelt aan een basis-URL/bestemmingspagina op de website van de adverteerder (soms via een andere site die de klik bijhoudt en de gebruiker vervolgens doorstuurt naar de bestemmingspagina). Het bevat alle toevoegingsparameters die zijn geconfigureerd voor de campagne of account voor Zoeken, Sociaal zoeken en Commerce. Als u URL&#39;s voor bijhouden hebt gegenereerd, is deze waarde gebaseerd op de volgende parameters in uw accountinstellingen en campagnemontages. Als u netwerkspecifieke parameters toevoegt, kunnen deze worden vervangen door de equivalente parameters voor Zoeken, Sociale en Commerce.<br><br> voor rekeningen met definitieve URLs, toont deze kolom de zelfde waarde zoals [!UICONTROL Base URL/Final URL column]. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel | Optioneel | Optioneel | (Benoemd voor een advertentiespecifieke labelclassificatie, zoals &quot;Kleur&quot; voor een labelclassificatie genaamd Kleur) Een waarde voor de opgegeven classificatie die aan de entiteit is gekoppeld. U kunt per entiteit slechts één waarde per classificatie opnemen (zoals &quot;rood&quot; voor de labelclassificatie &quot;Kleur&quot; voor campagne A). De maximumlengte is 100 tekens en de waarde kan ASCII- en niet-ASCII-tekens bevatten.<br><br> de classificaties van het Etiket en hun etiketwaarden worden toegepast op alle kindcomponenten; de nieuwe componenten die later worden toegevoegd worden automatisch geassocieerd met het etiket. De etiketclassificaties voor productgroepen worden toegepast op het eenheidniveau (het meest korrelige).<br><br> de classificatienaam en de classificatiewaarde zijn niet case-sensitive. |
| [!UICONTROL Constraints] | Optioneel | Optioneel | Optioneel | Een beperking die aan de entiteit is toegewezen. U kunt slechts één beperking per entiteit toewijzen.<br><br> Beperkingen worden geërft door kindentiteiten, zodat te hoeven u geen waarden voor kindentiteiten in te gaan tenzij u de geërfte waarden wilt met voeten treden. |
| [!UICONTROL Campaign Status] | Optioneel: maak of bewerk <br> Vereist: Verwijderen | nvt | nvt | De weergavestatus van de campagne: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande campagnes). De standaardwaarde voor nieuwe campagnes is <i>[!UICONTROL Active]</i>. Om een actieve of gepauzeerde campagne te schrappen, ga de waarde &quot;[!UICONTROL Deleted]&quot; in. |
| [!UICONTROL Ad Group Status] | nvt | Optioneel: maak of bewerk <br> Vereist: Verwijderen | nvt | De weergavestatus van de advertentiegroep: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande advertentiegroepen). De standaardwaarde voor nieuwe advertentiegroepen is <i>[!UICONTROL Active]</i> . Om een actieve of gepauzeerde ad groep te schrappen, ga de waarde &quot;[!UICONTROL Deleted]&quot; in. |
| [!UICONTROL Keyword Status] | nvt | nvt | Optioneel: maak of bewerk <br> Vereist: Verwijderen | De weergavestatus van het trefwoord: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i> of <i>[!UICONTROL Deleted]</i> (alleen bestaande trefwoorden). De standaardwaarde voor nieuwe trefwoorden is <i>[!UICONTROL Active]</i> . Om een actief of gepauzeerd sleutelwoord te schrappen, ga de waarde &quot;[!UICONTROL Deleted]&quot; in. |
| [!UICONTROL Campaign ID] | n.v.t.: creeer <br> Vereist/Facultatief: geef uit of schrap | Optioneel | Optioneel | De unieke id die een bestaande campagne identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Vereist slechts wanneer u de campagnenaam verandert, tenzij de rij een identiteitskaart van AMO voor de campagne omvat. |
| [!UICONTROL Ad Group ID] | nvt | n.v.t.: creeer <br> Vereist/Facultatief: geef uit of schrap | Optioneel | De unieke id die een bestaande advertentiegroep identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Vereist slechts wanneer u de naam van de advertentiegroep verandert, tenzij de rij een AMO-id voor de advertentiegroep omvat. |
| [!UICONTROL Keyword ID] | nvt | nvt | n/a: Creeer <br> Vereist/Optioneel: geef <br> Vereist uit: Schrapping | De unieke id die een bestaand trefwoord identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1 ] Vereist slechts wanneer u de sleutelwoordnaam verandert, tenzij de rij a) voldoende bezitskolommen omvat om het sleutelwoord te identificeren of b) een identiteitskaart van AMO. |
| [!UICONTROL AMO ID] | n.v.t.: creeer <br> Facultatief: geef uit of schrap | n.v.t.: creeer <br> Facultatief: geef uit of schrap | n.v.t.: creeer <br> Facultatief: geef uit of schrap | (In gegenereerde bulksbladen) Een door [!DNL Adobe] gegenereerde unieke id voor een gesynchroniseerde entiteit. Voor responsieve zoekadvertenties is de AMO-id vereist om advertenties te bewerken of te verwijderen, tenzij u de [!UICONTROL Ad ID] opneemt. Als u gegevens voor alle andere entiteitstypen met een AMO-id wilt bewerken, moet de AMO-id de gegevens bewerken of verwijderen, tenzij u de id van de entiteit en de bovenliggende entiteit-id opneemt.<br><br> Onderzoek, Sociale, &amp; Commerce gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |
| [!UICONTROL EF Error Message] | nvt | nvt | nvt | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van foutberichten van Zoeken, Sociaal en Commerce over gegevens in de rij; foutberichten worden opgenomen in [!UICONTROL EF Errors] -bestanden. Deze waarde wordt niet naar het advertentienetwerk gepost. |
| [!UICONTROL SE Error Message] | nvt | nvt | nvt | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van foutberichten van het advertentienetwerk met betrekking tot gegevens in de rij; foutberichten worden opgenomen in [!UICONTROL SE Errors] -bestanden. Deze waarde wordt niet naar het advertentienetwerk gepost. |

[^1 ]: Excel zet grote aantallen in wetenschappelijke aantekening (zoals 2.12E+09 voor 2115585666) om wanneer het dossier opent. Als u cijfers in de standaardnotatie wilt weergeven, selecteert u een willekeurige cel in de kolom en klikt u in de formulebalk.

>[!MORELIKETHIS]
>
>* [ Bijlage - de fouten van het Bulksheet ](../bulksheet-errors.md)
>* [ Verrichtingen u in bulksbladen kunt uitvoeren ](bulksheet-operations.md)
>* [ Ondersteunde formaten van het bulkbladdossier ](bulksheet-file-formats.md)
>* [ Download/creeer een bulksheet- dossier ](../bulksheet-download.md)
>* [ klik-volgende formaten voor  [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [ upload een bulksheet- dossier of verbeterd foutendossier ](../bulksheet-upload.md)
>* [ voert  [!DNL Naver]  het volgen-slechts rekeningen ](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md) uit
