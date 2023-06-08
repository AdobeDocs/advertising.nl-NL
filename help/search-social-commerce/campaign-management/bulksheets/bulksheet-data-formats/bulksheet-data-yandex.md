---
title: Vereiste gegevens voor het bulkwerkblad [!DNL Yandex] rekeningen
description: Verwijs naar de vereiste kopbalgebieden en gegevensgebieden in bulksbladen voor [!DNL Yandex] rekeningen.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1857'
ht-degree: 1%

---

# Aanhangsel - Vereiste gegevens voor het informatieblad voor [!DNL Yandex] rekeningen

Om te creëren en bij te werken [!DNL Yandex] Campagne gegevens in bulk, kunt u Onderzoek, Sociale, &amp; het bulksbladdossiers van de Handel gebruiken die specifiek voor worden geformatteerd [!DNL Yandex] rekeningen. U kunt een van beide [bulkbladbestanden genereren voor bestaande accounts](../bulksheet-download.md) in de vereiste bestandsindeling of b) handmatig aanmaken (zie &quot;[Ondersteunde bestandsindelingen voor bulkbladbestanden](bulksheet-file-formats.md)&quot; voor algemene informatie over de ondersteunde bestandsindelingen).

{{$include /help/_includes/bulksheet-appendices-intro.md}}

<!-- Hiding because this is probably too long a list to be useful.

## Available header fields

Platform,Acct Name,Campaign Name,Campaign Start Date,Campaign Budget,Delivery Method,Ad Group Name,Ad Title,Ad Description,Base URL,Destination URL,SiteLink Title,SiteLink Base URL,SiteLink Destination URL,Keyword,Max CPC,Match Type,Search Network Status,Content Network Status,Negative Keywords (Yandex),Param1 (Yandex),Param2 (Yandex),Campaign Status,Ad Group Status,Ad Status,Keyword Status,SiteLink Status,Campaign ID,Ad Group ID, Ad ID,Keyword ID,AMO ID, [Advertiser-specific Label Classification],Constraints,EF Error Message

{{$include /help/_includes/bulksheet-headers-note.md}}

-->

## Beschikbare gegevensvelden

{{$include /help/_includes/bulksheet-appendices-intro-required-data.md}}

| Veld | Campagne | Advertentiegroep | Trefwoord | Tekst toevoegen | Sitelink | Beschrijving |
|----|----|-----|-----|----|----|----|
| [!UICONTROL Platform] | n.v.t. | n.v.t. | n.v.t. | n.v.t. | n.v.t. | (Opgenomen in gegenereerde bulksbladen ter informatie) Het advertentieplatform. Vereist, tenzij elke rij een AMO-id voor de entiteit bevat. |
| [!UICONTROL Acct Name] | Vereist/optioneel | Vereist/optioneel | Vereist/optioneel | Vereist/optioneel | Vereist/optioneel | (Opgenomen in gegenereerde bulksbladen ter informatie) Het advertentieplatform. Vereist, tenzij elke rij een AMO-id voor de entiteit bevat. |
| [!UICONTROL Campaign Name] | Vereist | Vereist | Vereist | Vereist | Vereist | De unieke naam die een campagne voor een account identificeert. |
| [!UICONTROL Campaign Start Date] | Vereist: Maken<br>Optioneel: Bewerken of verwijderen | n.v.t. | n.v.t. | n.v.t. | n.v.t. | De eerste datum waarop een bod voor een campagne mag worden uitgebracht, in de tijdzone van de adverteerder en in een van de volgende formaten: d/m/yyyy, m/d/jj, m-d-jjjj of m-d-jj. Het gebrek voor nieuwe campagnes is de huidige dag. |
| [!UICONTROL Campaign Budget] | Vereist: Maken<br>Optioneel: Bewerken of verwijderen | n.v.t. | n.v.t. | n.v.t. | n.v.t. | Een levenslange uitgavenlimiet voor de campagne, met of zonder monetaire symbolen en leestekens. |
| [!UICONTROL Delivery Method] | Vereist: Maken<br>Optioneel: Bewerken of verwijderen | n.v.t. | n.v.t. | n.v.t. | n.v.t. | Hoe snel om advertenties voor de campagne elke dag te tonen:<ul><li><i>[!UICONTROL Standard (Distributed)]</i> (de standaardinstelling voor nieuwe campagnes): Om uw advertenties over de dag te verspreiden.</li><li><i>[!UICONTROL Accelerated]:</i> Zo vaak mogelijk advertenties weergeven totdat uw budget is bereikt. Hierdoor worden uw advertenties mogelijk niet later op de dag weergegeven.</li></ul> |
| [!UICONTROL Ad Group Name] | n.v.t. | Vereist | Vereist | Vereist | n.v.t. | De advertentiegroep. |
| [!UICONTROL Ad Title] | n.v.t. | n.v.t. | n.v.t. | Vereist | n.v.t. | De kop van de banner (advertentie). De maximumlengte is 33 tekens en een enkel woord mag niet meer dan 23 tekens bevatten.<br><br><b>Opmerking:</b> Als u de kopie van de advertentie wijzigt, verwijdert u de bestaande advertentie en maakt u een nieuwe advertentie. |
| [!UICONTROL Ad Description] | n.v.t. | n.v.t. | n.v.t. | Vereist | n.v.t. | De hoofdtekst van de banner (advertentie). De maximumlengte is 75 tekens en een enkel woord mag niet meer dan 22 tekens bevatten.<br><br><b>Opmerking:</b> Als u de kopie van de advertentie wijzigt, verwijdert u de bestaande advertentie en maakt u een nieuwe advertentie. |
| [!UICONTROL Base URL] | n.v.t. | n.v.t. | Optioneel | Vereist | n.v.t. | De bestemmingspagina URL waaraan de eind - gebruikers worden genomen wanneer zij uw advertentie klikken, met inbegrip van om het even welke toevoegingsparameters die voor de campagne of de rekening worden gevormd. De maximumlengte is 1024 tekens, inclusief het protocol.<br><br>Basis/definitieve URLs op het sleutelwoordniveau treedt URLs op het advertentieniveau en hoger met voeten. |
| [!UICONTROL Destination URL] | n.v.t. | n.v.t. | n.v.t. | n.v.t. | n.v.t. | (Ter informatie opgenomen in gegenereerde bulksbladen; niet gepost aan het advertentienetwerk) Voor accounts met doel-URL&#39;s is deze waarde de URL die een advertentie koppelt aan een basis-URL/bestemmingspagina op de website van de adverteerder (soms via een andere site die de klik bijhoudt en de gebruiker vervolgens doorstuurt naar de bestemmingspagina). Het omvat om het even welke toevoegingsparameters die voor de Onderzoek, Sociale, &amp; de campagne of de rekening van de Handel worden gevormd. Als u URL&#39;s voor bijhouden hebt gegenereerd, is deze waarde gebaseerd op de volgende parameters in uw accountinstellingen en campagnemontages. Als u toevoegde en netwerk-specifieke parameters, kunnen zij met de gelijkwaardige parameters voor Onderzoek, Sociale, &amp; Handel worden vervangen. |
| [!UICONTROL SiteLink Title] | n.v.t. | n.v.t. | n.v.t. | n.v.t. | Vereist | De sitelink-tekst. Voor nieuwe sitelinks neemt u de naam van de campagne op in de sitelink-rij. Voor sitelinks op ad-groepsniveau of op ad-niveauniveau neemt u ook de naam van de advertentiegroep of de titel en tekst van de advertentie op.<br><br><b>Opmerking:</b> U kunt maximaal vier sitelinks hebben. |
| [!UICONTROL SiteLink Base URL] | n.v.t. | n.v.t. | n.v.t. | n.v.t. | Vereist | De basis-URL voor een sitelink; moet de basis-URL voor de banner zijn. Zie &quot;[!UICONTROL Base URL].&quot; |
| [!UICONTROL SiteLink Destination URL] | n.v.t. | n.v.t. | n.v.t. | n.v.t. | n.v.t. | De doel-URL voor een sitelink; moet dit de doel-URL voor de banner zijn. Zie &quot;[!UICONTROL Destination URL].&quot; |
| [!UICONTROL Keyword] | Optioneel / n.v.t. | n.v.t. | Vereist | n.v.t. | n.v.t. | De woordgroep (trefwoordtekenreeks). Een advertentie moet minstens één zin hebben. Elk trefwoord mag maximaal zeven woorden bevatten, met uitzondering van stopwoorden.<br><br><b>Opmerkingen:</b><ul><li>Als u een uitdrukking op campagnereniveau wilt uitsluiten, stelt u de optie [!UICONTROL Match Type] tot [!UICONTROL Negative].</li><li>Als u een woordgroep wijzigt, verwijdert u de bestaande woordgroep en maakt u een nieuwe woordgroep.</li><li>Een [!DNL Yandex] trefwoordgroep of type overeenkomst verwijdert de bestaande trefwoorduitdrukking en maakt een nieuwe trefwoordgroep.</li></ul> |
| [!UICONTROL Max CPC] | n.v.t. | Vereist: Maken<br>Optioneel: Bewerken of verwijderen | Optioneel | n.v.t. | n.v.t. | De maximumkosten per klik (CPC), die het hoogste bedrag is om voor een banner (advertentie) te betalen klikt op het onderzoeksnetwerk, met of zonder monetaire symbolen en interpunctie. U kunt waarden instellen voor advertentiegroepen en trefwoorden. De standaardinstelling voor een nieuw trefwoord wordt overgenomen van het niveau van de advertentiegroep. |
| [!UICONTROL Match Type] | Optioneel / n.v.t. | n.v.t. | Optioneel: Maken<br>Vereist/optioneel: Bewerken of verwijderen | n.v.t. | n.v.t. | De optie voor trefwoordafstemming voor de woordgroep: <i>[!UICONTROL Content]</i> of <i>[!UICONTROL Search]</i>. Definieer negatieve trefwoorden met &quot;[!UICONTROL Negative Keywords]&quot; kolom.<br><br><b>Opmerking:</b> Een [!DNL Yandex] trefwoordgroep of type overeenkomst verwijdert de bestaande trefwoorduitdrukking en maakt een nieuwe trefwoordgroep. |
| [!UICONTROL Search Network Status] | Optioneel | n.v.t. | n.v.t. | n.v.t. | n.v.t. | Of advertenties op het zoeknetwerk moeten worden geplaatst: <i>[!UICONTROL Yes]</i> (de standaardwaarde) of <i>[!UICONTROL No]</i>. |
| Inhoudsnetwerkstatus | Optioneel | n.v.t. | n.v.t. | n.v.t. | n.v.t. | Of advertenties al dan niet op de [!DNL Yandex] advertentienetwerk (display): <i>[!UICONTROL Yes]</i> (de standaardwaarde) of <i>[!UICONTROL No]</i>. |
| [!UICONTROL Negative Keywords (Yandex)] | n.v.t. | n.v.t. | Optioneel | n.v.t. | n.v.t. | Negatieve trefwoorden (woordgroepen) die door alle woordgroepen in een advertentiegroep worden gedeeld, voorafgegaan door een minteken (zoals `-mykeyword`). Als een negatief trefwoord overeenkomt met een trefwoord in een woordgroep, wordt het negatieve trefwoord niet toegepast op de woordgroep. |
| [!UICONTROL Param1 (Yandex)] | n.v.t. | n.v.t. | Optioneel | n.v.t. | n.v.t. | Waarde van de `{param1}` substitutievariabele. Het kan maximaal 255 bytes bevatten. Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| [!UICONTROL Param2 (Yandex)] | n.v.t. | n.v.t. | Optioneel | n.v.t. | n.v.t. | Waarde van de  `{param2}` substitutievariabele. Het kan maximaal 255 bytes bevatten. Als u de bestaande waarde wilt verwijderen, gebruikt u de waarde `[delete]` (met inbegrip van de haakjes). |
| [!UICONTROL Campaign Status] | Optioneel: Maken of bewerken<br>Vereist: Verwijderen | n.v.t. | n.v.t. | n.v.t. | n.v.t. | De weergavestatus van de campagne: <i>[!UICONTROL active]</i>, <i>[!UICONTROL archived]</i>, <i>[!UICONTROL deleted]</i>, <i>[!UICONTROL disapproved]</i>, <i>[!UICONTROL pending]</i>, of <i>[!UICONTROL stop]</i> (gepauzeerd). De standaardinstelling voor nieuwe campagnes is <i>[!UICONTROL active]</i>.<br><br><b>Opmerkingen:</b><ul></li>Als een campagne ooit actief is geweest, kunt u het niet schrappen. archiveer het.</li><li>Campagnes kunnen in sommige situaties automatisch worden gearchiveerd of verwijderd.</li><li>U kunt de status niet handmatig instellen op <i>[!UICONTROL disapproved]</i> of <i>[!UICONTROL pending]</i>en deze statussen niet wijzigen.</li></ul> |
| [!UICONTROL Ad Group Status] | n.v.t. | Optioneel: Maken of bewerken<br>Vereist: Verwijderen | n.v.t. | n.v.t. | n.v.t. | De weergavestatus van de advertentiegroep: <i>[!UICONTROL active]</i>, <i>[!UICONTROL archived]</i>, <i>[!UICONTROL deleted]</i>, <i>[!UICONTROL disapproved]</i>, <i>[!UICONTROL pending]</i>, of <i>[!UICONTROL stop]</i> (gepauzeerd). De standaardinstelling voor nieuwe advertentiegroepen is <i>[!UICONTROL active]</i>.<br><br><b>Opmerkingen:</b><ul></li>Als een advertentiegroep ooit actief is geweest, kunt u het niet schrappen. archiveer het.</li><li>U kunt de status niet handmatig instellen op <i>[!UICONTROL disapproved]</i> of <i>[!UICONTROL pending]</i>en deze statussen niet wijzigen.</li></ul> |
| [!UICONTROL Ad Status] | n.v.t. | n.v.t. | n.v.t. | Optioneel: Maken of bewerken<br>Vereist: Verwijderen | n.v.t. | De weergavestatus van de banner (advertentie): <i>[!UICONTROL active]</i>, <i>[!UICONTROL archived]</i>, <i>[!UICONTROL deleted]</i>, <i>[!UICONTROL disapproved]</i>, <i>[!UICONTROL pending]</i>, of <i>[!UICONTROL stop]</i> (gepauzeerd). De standaardinstelling voor nieuwe banners is <i>[!UICONTROL active]</i>.<br><br><b>Opmerking: U kunt de status niet handmatig instellen op <i>[!UICONTROL disapproved]</i> of <i>[!UICONTROL pending]</i>en deze statussen niet wijzigen. |
| [!UICONTROL Keyword Status] | n.v.t. | n.v.t. | Optioneel: Maken of bewerken<br>Vereist: Verwijderen | n.v.t. | n.v.t. | De weergavestatus van de woordgroep (trefwoord): <i>[!UICONTROL active]</i>. De standaardinstelling voor nieuwe woordgroepen is <i>[!UICONTROL active]</i>.<br><br><b>Opmerking: U kunt de status niet handmatig instellen op <i>[!UICONTROL disapproved]</i> of <i>[!UICONTROL pending]</i>en deze statussen niet wijzigen. |
| [!UICONTROL SiteLink Status] | n.v.t. | n.v.t. | n.v.t. | n.v.t. | Optioneel: Maken of bewerken<br>Vereist: Verwijderen | De weergavestatus van de sitelink: <i>[*UICONTROL actief]</i> of <i>[*UICONTROL gepauzeerd]</i>. De standaardinstelling voor nieuwe sitelinks is <i>[*UICONTROL actief]</i>. |
| [!UICONTROL Campaign ID] | n.v.t.: Maken<br>Vereist/optioneel: Bewerken<br>Optioneel: Verwijderen | Optioneel | Optioneel | Optioneel | Optioneel | De unieke id die een bestaande campagne identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Deze optie is alleen vereist wanneer u de naam van de campagne wijzigt, tenzij de rij een AMO-id voor de campagne bevat. |
| [!UICONTROL Ad Group ID] | n.v.t. | n.v.t.: Maken<br>Vereist/optioneel: Bewerken<br>Optioneel: Verwijderen | Optioneel | Optioneel | n.v.t. | De unieke id die een bestaande advertentiegroep identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Deze optie is alleen vereist wanneer u de naam van de advertentiegroep wijzigt, tenzij de rij een AMO-id voor de advertentiegroep bevat. |
| [!UICONTROL Ad ID] | n.v.t. | n.v.t. | n.v.t. | n.v.t.: Maken<br>Vereist/optioneel: Bewerken of verwijderen | n.v.t. | De unieke id die een bestaand trefwoord identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Vereist slechts wanneer u de sleutelwoordnaam verandert, tenzij de rij a) voldoende bezitskolommen omvat om het sleutelwoord te identificeren of b) een identiteitskaart van AMO. |
| [!UICONTROL Keyword ID] | n.v.t. | n.v.t. | n.v.t.: Maken<br>Vereist/optioneel: Bewerken<br>Vereist: Verwijderen | n.v.t. | n.v.t. | De unieke id die een bestaand trefwoord identificeert. In CSV- en TSV-bestanden moet dit worden voorafgegaan door één aanhalingsteken (&#39;).[^1] Vereist slechts wanneer u de sleutelwoordnaam verandert, tenzij de rij a) voldoende bezitskolommen omvat om het sleutelwoord te identificeren of b) een identiteitskaart van AMO. |
| [!UICONTROL AMO ID] | n.v.t. | n.v.t. | n.v.t. | n.v.t. | n.v.t. | (In gegenereerde opsommingstekens) en [!DNL Adobe]-generated unique identifier for a synced entity. Voor responsieve zoekadvertenties is de AMO-id vereist om advertenties te bewerken of te verwijderen, tenzij u de [!UICONTROL Ad ID]. Als u gegevens voor alle andere entiteitstypen met een AMO-id wilt bewerken, moet de AMO-id de gegevens bewerken of verwijderen, tenzij u de id van de entiteit en de bovenliggende entiteit-id opneemt.<br><br>Zoek, Sociaal, &amp; Handel gebruikt de waarde om de correcte identiteit te bepalen uit te geven maar post identiteitskaart niet aan het advertentienetwerk. |
| \[Advertiserspecifieke labelclassificatie\] | Optioneel | Optioneel | Optioneel | Optioneel | n.v.t. | (Benoemd voor een advertentiespecifieke labelclassificatie, zoals &quot;Kleur&quot; voor een labelclassificatie genaamd Kleur) Een waarde voor de opgegeven classificatie die aan de entiteit is gekoppeld. U kunt per entiteit slechts één waarde per classificatie opnemen (zoals &quot;rood&quot; voor de labelclassificatie &quot;Kleur&quot; voor campagne A). De maximumlengte is 100 tekens en de waarde kan ASCII- en niet-ASCII-tekens bevatten.<br><br>De classificaties van het etiket en hun etiketwaarden worden toegepast op alle kindcomponenten; nieuwe componenten die later worden toegevoegd, worden automatisch aan het label gekoppeld. De etiketclassificaties voor productgroepen worden toegepast op het eenheidniveau (het meest korrelige).<br><br>De classificatienaam en de classificatiewaarde zijn niet hoofdlettergevoelig. |
| [!UICONTROL Constraints] | Optioneel | Optioneel | Optioneel | n.v.t. | n.v.t. | Een beperking die aan de entiteit is toegewezen. U kunt slechts één beperking per entiteit toewijzen.<br><br>Restricties worden overgeërfd door onderliggende entiteiten, zodat u geen waarden voor onderliggende entiteiten hoeft in te voeren, tenzij u de overgeërfde waarden wilt overschrijven. |
| [!UICONTROL EF Error Message] | n.v.t. | n.v.t. | n.v.t. | n.v.t. | n.v.t. | (Opgenomen in gegenereerde bulksbladen ter informatie) Tijdelijke aanduiding voor het weergeven van foutberichten van Zoeken, Sociale Zaken en Handel met betrekking tot gegevens in de rij. foutberichten worden opgenomen in [!UICONTROL EF Errors] bestanden. Deze waarde wordt niet naar het advertentienetwerk gepost. |

<table style="table-layout:auto">

[^1]: Excel zet grote aantallen in wetenschappelijke aantekening (zoals 2.12E+09 voor 2115585666) om wanneer het dossier opent. Als u cijfers in de standaardnotatie wilt weergeven, selecteert u een willekeurige cel in de kolom en klikt u in de formulebalk.

>[!MORELIKETHIS]
>
>* [Bijlage - Fouten in bladbladen](../bulksheet-errors.md)
>* [Bewerkingen die u kunt uitvoeren in bulksbladen](bulksheet-operations.md)
>* [Ondersteunde bestandsindelingen voor bulksbladen](bulksheet-file-formats.md)
>* [Een bulkbladbestand downloaden/maken](../bulksheet-download.md)
>* [Opmaak voor het bijhouden van klikken voor [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [Een bulksbladbestand of gecorrigeerd foutbestand uploaden](../bulksheet-upload.md)
