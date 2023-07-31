---
title: Vereiste gegevens voor het bulkwerkblad [!DNL Naver] rekeningen
description: Verwijs naar de vereiste kopbalgebieden en gegevensgebieden in bulksbladen voor [!DNL Naver] rekeningen.
exl-id: bd6e3dab-47b0-428a-825d-bd9c21494fb0
feature: Search Bulksheets
source-git-commit: 97111c6cd38098cac72b8773390afd254a017d1d
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 1%

---

# Aanhangsel - Vereiste gegevens voor het informatieblad voor [!DNL Naver] rekeningen

Vul uw [!DNL Naver] accounts in Search, Social &amp; Commerce door een bulkbladbestand te genereren in [!DNL Naver]en uploadt u deze naar Zoeken, Sociale Zaken en Handel.

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Ad Group Name,Keyword,Base URL,Destination URL,[Advertiser-specific Label Classification],Constraints,Campaign Status,Ad Group Status,Keyword Status,Campaign ID,Ad Group ID,Keyword ID,AMO ID,Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## Beschikbare gegevensvelden

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Veld | Campagne | Advertentiegroep | Trefwoord | Beschrijving |
|----|----|----|----|----|
| [!UICONTROL Platform] | nvt | nvt | nvt | (Opgenomen in gegenereerde bulksbladen ter informatie) Het advertentieplatform. Vereist, tenzij elke rij een AMO-id voor de entiteit bevat. |
| [!UICONTROL Acct Name] | Vereist/optioneel | Vereist/optioneel | Vereist/optioneel | De unieke naam die een advertentienetwerkaccount identificeert. Vereist, tenzij elke rij een AMO-id voor de entiteit bevat. |
| [!UICONTROL Campaign Name] | Vereist | Vereist | Vereist | De unieke naam die een campagne voor een account identificeert. |
| [!UICONTROL Ad Group Name] | nvt | Vereist | Vereist | De unieke naam die een advertentiegroep identificeert. |
| [!UICONTROL Keyword] | nvt | nvt | Vereist | De trefwoordtekenreeks. |
| [!UICONTROL Base URL] | nvt | nvt | Optioneel | De bestemmingspagina URL waaraan de eind - gebruikers worden genomen wanneer zij uw advertentie klikken, met inbegrip van om het even welke toevoegingsparameters die voor de campagne of de rekening worden gevormd.<br><br>Basis/definitieve URLs op het sleutelwoordniveau treedt URLs op het advertentieniveau en hoger met voeten. |
| [!UICONTROL Destination URL] | nvt | nvt | nvt | (Opgenomen in gegenereerde bulksbladen voor informatiedoeleinden; niet gepost naar het advertentienetwerk) Voor accounts met doel-URL&#39;s is deze waarde de URL die een advertentie koppelt aan een basis-URL/bestemmingspagina op de website van de adverteerder (soms via een andere site die de klik bijhoudt en de gebruiker vervolgens doorstuurt naar de bestemmingspagina). Het omvat om het even welke toevoegingsparameters die voor de Onderzoek, Sociale, &amp; de campagne of de rekening van de Handel worden gevormd. Als u URL&#39;s voor bijhouden hebt gegenereerd, is deze waarde gebaseerd op de volgende parameters in uw accountinstellingen en campagnemontages. Als u toevoegde en netwerk-specifieke parameters, kunnen zij met de gelijkwaardige parameters voor Onderzoek, Sociale, &amp; Handel worden vervangen.<br><br>Voor accounts met uiteindelijke URL&#39;s geeft deze kolom dezelfde waarde als de [!UICONTROL Base URL/Final URL column]. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel | Optioneel | Optioneel | (Benoemd voor een advertentiespecifieke labelclassificatie, zoals &quot;Kleur&quot; voor een labelclassificatie genaamd Kleur) Een waarde voor de opgegeven classificatie die aan de entiteit is gekoppeld. U kunt per entiteit slechts één waarde per classificatie opnemen (zoals &quot;rood&quot; voor de labelclassificatie &quot;Kleur&quot; voor campagne A). De maximumlengte is 100 tekens en de waarde kan ASCII- en niet-ASCII-tekens bevatten.<br><br>De classificaties van het etiket en hun etiketwaarden worden toegepast op alle kindcomponenten; de nieuwe componenten die later worden toegevoegd worden automatisch geassocieerd met het etiket. De etiketclassificaties voor productgroepen worden toegepast op het eenheidniveau (het meest korrelige).<br><br>De classificatienaam en de classificatiewaarde zijn niet hoofdlettergevoelig. |
| [!UICONTROL Constraints] | Optioneel | Optioneel | Optioneel | Een beperking die aan de entiteit is toegewezen. U kunt slechts één beperking per entiteit toewijzen.<br><br>Restricties worden overgeërfd door onderliggende entiteiten, zodat u geen waarden voor onderliggende entiteiten hoeft in te voeren, tenzij u de overgeërfde waarden wilt overschrijven. |
| [!UICONTROL Campaign Status] | Optioneel: maken of bewerken<br>Vereist: verwijderen | nvt | nvt | Weergavestatus van de campagne: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, of <i>[!UICONTROL Deleted]</i> (alleen bestaande campagnes). De standaardwaarde voor nieuwe campagnes is <i>[!UICONTROL Active]</i>. Als u een actieve of gepauzeerde campagne wilt verwijderen, voert u de waarde &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Ad Group Status] | nvt | Optioneel: maken of bewerken<br>Vereist: verwijderen | nvt | De weergavestatus van de advertentiegroep: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, of <i>[!UICONTROL Deleted]</i> (alleen bestaande advertentiegroepen). De standaardwaarde voor nieuwe advertentiegroepen is <i>[!UICONTROL Active]</i>. Als u een actieve of gepauzeerde ad-groep wilt verwijderen, voert u de waarde &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Keyword Status] | nvt | nvt | Optioneel: maken of bewerken<br>Vereist: verwijderen | De weergavestatus van het trefwoord: *[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, of <i>[!UICONTROL Deleted]</i> (alleen bestaande trefwoorden). De standaardwaarde voor nieuwe trefwoorden is <i>[!UICONTROL Active]</i>. Als u een actief of onderbroken trefwoord wilt verwijderen, voert u de waarde &quot;[!UICONTROL Deleted]&quot;. |
| [!UICONTROL Campaign ID] | n.v.t. maken<br>Vereist/optioneel: bewerken of verwijderen | Optioneel | Optioneel | De unieke id die een bestaande campagne identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Deze optie is alleen vereist wanneer u de naam van de campagne wijzigt, tenzij de rij een AMO-id voor de campagne bevat. |
| [!UICONTROL Ad Group ID] | nvt | n.v.t. maken<br>Vereist/optioneel: bewerken of verwijderen | Optioneel | De unieke id die een bestaande advertentiegroep identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Deze optie is alleen vereist wanneer u de naam van de advertentiegroep wijzigt, tenzij de rij een AMO-id voor de advertentiegroep bevat. |
| [!UICONTROL Keyword ID] | nvt | nvt | n.v.t. maken<br>Vereist/optioneel: Bewerken<br>Vereist: verwijderen | De unieke id die een bestaand trefwoord identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Vereist slechts wanneer u de sleutelwoordnaam verandert, tenzij de rij a) voldoende bezitskolommen omvat om het sleutelwoord te identificeren of b) een identiteitskaart van AMO. |
| [!UICONTROL AMO ID] | n.v.t. maken<br>Optioneel: bewerken of verwijderen | n.v.t. maken<br>Optioneel: bewerken of verwijderen | n.v.t. maken<br>Optioneel: bewerken of verwijderen | (In gegenereerde opsommingstekens) en [!DNL Adobe]-generated unique identifier for a synced entity. Voor responsieve zoekadvertenties is de AMO-id vereist om advertenties te bewerken of te verwijderen, tenzij u de [!UICONTROL Ad ID]. Als u gegevens voor alle andere entiteitstypen met een AMO-id wilt bewerken, moet de AMO-id de gegevens bewerken of verwijderen, tenzij u de id van de entiteit en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |
| [!UICONTROL EF Error Message] | nvt | nvt | nvt | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van foutberichten van Zoeken, Sociale Zaken en Handel met betrekking tot gegevens in de rij; foutberichten worden opgenomen in [!UICONTROL EF Errors] bestanden. Deze waarde wordt niet naar het advertentienetwerk gepost. |
| [!UICONTROL SE Error Message] | nvt | nvt | nvt | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van foutberichten van het advertentienetwerk met betrekking tot gegevens in de rij; foutberichten worden opgenomen in [!UICONTROL SE Errors] bestanden. Deze waarde wordt niet naar het advertentienetwerk gepost. |

[^1]: Excel zet grote aantallen in wetenschappelijke aantekening (zoals 2.12E+09 voor 2115585666) om wanneer het dossier opent. Als u cijfers in de standaardnotatie wilt weergeven, selecteert u een willekeurige cel in de kolom en klikt u in de formulebalk.

>[!MORELIKETHIS]
>
>* [Bijlage - Fouten in bladbladen](../bulksheet-errors.md)
>* [Bewerkingen die u kunt uitvoeren in bulksbladen](bulksheet-operations.md)
>* [Ondersteunde bestandsindelingen voor bulksbladen](bulksheet-file-formats.md)
>* [Een bulkbladbestand downloaden/maken](../bulksheet-download.md)
>* [Opmaak voor het bijhouden van klikken voor [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Een bulksbladbestand of gecorrigeerd foutbestand uploaden](../bulksheet-upload.md)
>* [Implementeren [!DNL Naver] accounts met alleen traceren](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
