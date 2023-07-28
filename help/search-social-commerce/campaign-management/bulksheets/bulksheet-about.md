---
title: Campagnegegevens beheren met behulp van bulksbladen
description: Meer informatie over de functionaliteit van bulksheet die beschikbaar is in het advertentienetwerk, de werkstroom van het bulksblad en foutafhandeling.
exl-id: 207cc08b-8650-4243-b9fd-1c920b81c1f9
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---

# Campagnegegevens beheren met behulp van bulksbladen

Een bulksheet is een bestand dat campagnegegevens in een specifieke indeling bevat en kan worden gebruikt om snel campagne- en groepsstructuurgegevens en tekstadvertenties te maken of te wijzigen. U kunt bulksbladen met gegevens voor één of meerdere rekeningen, voor specifieke campagnes en ad groepen, of zelfs voor specifieke tekstadvertenties, plaatsen, en productgroepen produceren (downloaden). U kunt bulksbladen gebruiken om grote gegevensreeksen te beheren of kleine veranderingen aan te brengen. Elk ad netwerk vereist verschillende kolommen van informatie.

U kunt opsommingstekens genereren met zoveel gegevens als u wilt, of u kunt deze desgewenst handmatig maken en uploaden (zie het hoofdstuk over &quot;Vereiste/Opgenomen gegevens in bulksbladen&quot;).

Wanneer u een werkblad hebt gemaakt, kunt u eventuele gebroken bestemmingspagina&#39;s identificeren die moeten worden gecorrigeerd, of aanvullende gegevens die moeten worden toegevoegd of bewerkt. U kunt het dossier dan uitgeven en het uploaden aan Onderzoek, Sociale, &amp; Handel, naar keuze plannend het om aan het relevante advertentienetwerk onmiddellijk of later worden gepost. U kunt ook direct of later een beschikbaar bulksblad plaatsen.

U kunt optioneel bulkbladbestanden uploaden naar een opgegeven FTP-account voor opvragen en automatisch posten. De directory wordt elk uur gescand en nieuwe bestanden worden naar het zoeknetwerk gepost in de volgorde waarin ze zijn ontvangen.

Alle bulksbladen, bestanden met validatiefouten van de landingspagina en andere foutbestanden worden 30 dagen nadat ze zijn gemaakt, automatisch verwijderd, tenzij u ze eerder verwijdert.

## Functionaliteit per ad-netwerk

* **Downloaden, uploaden en posten:**  [!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft® Advertising], en [!DNL Yandex] rekeningen

* **Alleen downloaden en uploaden:** [!DNL Naver] rekeningen

  U kunt uploaden [!DNL Naver] gegevens voor gebruik binnen Onderzoek, Sociale, &amp; Handel maar kan het niet aan het advertentienetwerk posten. U kunt ook de bestaande (niet-gesynchroniseerde) gegevens downloaden.

* **Alleen gegevens downloaden:**  [!DNL Pinterest], [!DNL Yahoo Native], en [!DNL Yahoo! Display Network] rekeningen

  U kunt uw bestaande (niet-gesynchroniseerde) gegevens downloaden.

## Overzicht van het gebruik van bulksbladen

De standaardstappen voor het gebruik van bulksbladen voor gesynchroniseerde accounts zijn als volgt:

<!-- insert image
  [EDIT/RECREATE FILE to replace "search engine"]
-->

1. [Gegevens downloaden voor een of meer accounts, campagnes of groepen toevoegen aan een bulkbladbestand](bulksheet-download.md). U kunt desgewenst handmatig een netwerkspecifiek blad vullen en het bestand uploaden.

1. [De openingspagina&#39;s valideren](bulksheet-validate-landing-pages.md) in de basis (uiteindelijke) URL&#39;s of doel-URL&#39;s in het bestand.

1. Wanneer u gegevens moet toevoegen of correcties moet aanbrengen:

   1. [Het bestand exporteren](bulksheet-export.md) naar uw bureaublad en bewerk het in [!DNL Microsoft® Excel].

   1. [Het bewerkte bestand handmatig uploaden](bulksheet-upload.md) om te zoeken, sociale zaken en handel, of [het bestand uploaden naar een opgegeven FTP-account](bulksheet-ftp-account.md) voor automatisch posten.

1. (Voor bestanden die handmatig worden geüpload) [Het bestand verzenden](bulksheet-post.md) naar het advertentienetwerk wanneer u het uploadt of later.

1. (Indien nodig) Download eventuele nieuwe foutbestanden, corrigeer de rijen en post het bestand opnieuw.

## Fouten beheren bij het uploaden en posten van campagnegegevens

Met Zoeken, Sociaal zoeken en Handel uploadt en plaatst u zoveel rijen gegevens als u kunt op een bulkblad voor de campagne, inclusief de URL&#39;s die zo nodig worden gegenereerd.

Wanneer er fouten optreden tijdens het bewerken van een werkblad, wordt een van de volgende twee typen foutbestanden gegenereerd:

* **[!UICONTROL EF Errors]:**  Wanneer een bestand of afzonderlijke rijen in het bestand niet kunnen worden geüpload of verwerkt, wordt een foutbestand met de naam `<uploaded file name>_ef_errors.<extension used for the bulksheet>` wordt gemaakt. Als het probleem met individuele rijen is, dan worden die rijen omvat, met een verklaring van elke fout zodat het kan worden verbeterd.

* **[!UICONTROL SE Errors]:**  Wanneer een bestand wordt gepost maar het ad-netwerk niet alle of een deel van de gegevens accepteert, wordt een foutbestand met de naam `<uploaded file name>_se_errors.<extension used for the bulksheet>` wordt gemaakt. Wanneer sommige maar niet alle rijen werden goedgekeurd, toont het foutendossier de rijen die niet werden gepost en een verklaring van elke fout zodat kan het worden verbeterd. De foutberichten worden weergegeven in de laatste drie kolommen van elke rij.

>[!NOTE]
>
>Als u [!DNL Google Ads] advertenties die in strijd zijn met het reclamebeleid van het advertentienetwerk maar in aanmerking komen voor uitzonderingen , worden die advertenties automatisch opnieuw gepost met vrijstellingsverzoeken . Als de vrijstellingsaanvraag mislukt, wordt informatie over de schending opgenomen in het foutbestand.

U kunt beide typen foutbestanden downloaden, correcties rechtstreeks in de rijen aanbrengen en het bestand vervolgens opnieuw uploaden en posten.

Foutbestanden worden na 30 dagen automatisch verwijderd, tenzij u ze eerder verwijdert.

## Informatie over elk bestand

Alle gedownloade gegevensbestanden, geüploade bestanden en foutbestanden zijn beschikbaar via [!UICONTROL Search] > [!UICONTROL Bulksheets].

De informatie voor elk dossier omvat de huidige taakstatus en het percentage van de taak die wordt voltooid, de datum het werd gecreeerd, (indien van toepassing) de datum het aan het gespecificeerde ad netwerk, de geplande schrappingsdatum, en de login naam van de gebruiker werd of zal worden gepost die de taak in werking stelde.

>[!MORELIKETHIS]
>
>* [Een bulkbladbestand downloaden/maken](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
>* [Upload een bulksheet of een gecorrigeerd foutbestand](bulksheet-upload.md)
>* [Kolommen of gecorrigeerde foutbestanden plaatsen](bulksheet-post.md)
>* [Een gegenereerd of geüpload bulksbladbestand exporteren](bulksheet-export.md)
