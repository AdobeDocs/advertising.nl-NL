---
title: Campagnegegevens beheren met behulp van bulksbladen
description: Meer informatie over de functionaliteit van bulksheet die beschikbaar is in het advertentienetwerk, de werkstroom van het bulksblad en foutafhandeling.
exl-id: 34a16ee3-9eba-4b8b-a5ca-65318f4ee6c5
feature: Search Bulksheets
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '774'
ht-degree: 0%

---

# Campagnegegevens beheren met behulp van bulksbladen

Een bulksheet is een bestand dat campagnegegevens in een specifieke indeling bevat en kan worden gebruikt om snel campagne- en groepsstructuurgegevens en tekstadvertenties te maken of te wijzigen. U kunt bulksbladen met gegevens voor één of meerdere rekeningen, voor specifieke campagnes en ad groepen, of zelfs voor specifieke tekstadvertenties, plaatsen, en productgroepen produceren (downloaden). U kunt bulksbladen gebruiken om grote gegevensreeksen te beheren of kleine veranderingen aan te brengen. Elk ad netwerk vereist verschillende kolommen van informatie.

U kunt opsommingstekens genereren met zoveel gegevens als u wilt, of u kunt deze desgewenst handmatig maken en uploaden (zie het hoofdstuk over &quot;Vereiste/Opgenomen gegevens in bulksbladen&quot;).

Wanneer u een werkblad hebt gemaakt, kunt u eventuele gebroken bestemmingspagina&#39;s identificeren die moeten worden gecorrigeerd, of aanvullende gegevens die moeten worden toegevoegd of bewerkt. U kunt het bestand vervolgens bewerken en uploaden naar Zoeken, Sociaal zoeken en Commerce. U kunt desgewenst plannen dat het bestand direct of later naar het relevante advertentienetwerk wordt gepost. U kunt ook direct of later een beschikbaar bulksblad plaatsen.

U kunt optioneel bulkbladbestanden uploaden naar een opgegeven FTP-account voor opvragen en automatisch posten. De directory wordt elk uur gescand en nieuwe bestanden worden naar het zoeknetwerk gepost in de volgorde waarin ze zijn ontvangen.

Alle bulksbladen, bestanden met validatiefouten van de landingspagina en andere foutbestanden worden 30 dagen nadat ze zijn gemaakt, automatisch verwijderd, tenzij u ze eerder verwijdert.

## Functionaliteit per ad-netwerk

* **Download, upload, en post:** [!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising], en [!DNL Yandex] rekeningen

* **slechts Download en upload:** [!DNL Naver] rekeningen

  U kunt [!DNL Naver] -gegevens uploaden voor gebruik in Zoeken, Sociaal en Commerce, maar u kunt deze niet naar het advertentienetwerk posten. U kunt ook de bestaande (niet-gesynchroniseerde) gegevens downloaden.

* **slechts gegevens van de Download:** [!DNL Pinterest], [!DNL Yahoo Native], en [!DNL Yahoo! Display Network] rekeningen

  U kunt uw bestaande (niet-gesynchroniseerde) gegevens downloaden.

## Overzicht van het gebruik van bulksbladen

De standaardstappen voor het gebruik van bulksbladen voor gesynchroniseerde accounts zijn als volgt:

<!-- insert image
  [EDIT/RECREATE FILE to replace "search engine"]
-->

1. [ gegevens van de Download voor één of meerdere rekeningen, campagnes, of ad groepen in een bulksheet dossier ](bulksheet-download.md). U kunt desgewenst handmatig een netwerkspecifiek blad vullen en het bestand uploaden.

1. [ bevestigt de het landen pagina&#39;s ](bulksheet-validate-landing-pages.md) in de basis (definitieve) URLs of bestemmings URLs in het dossier.

1. Wanneer u gegevens moet toevoegen of correcties moet aanbrengen:

   1. [ Uitvoer het dossier ](bulksheet-export.md) aan uw Desktop en geef het in [!DNL Microsoft Excel] uit.

   1. [ uploadt manueel het uitgegeven dossier ](bulksheet-upload.md) aan Onderzoek, Sociaal, &amp; Commerce, of [ uploadt het dossier aan een gespecificeerde rekening van FTP ](bulksheet-ftp-account.md) voor automatisch posten.

1. (Voor manueel geupload dossiers) [ post het dossier ](bulksheet-post.md) aan het advertentienetwerk of aangezien u het of later uploadt.

1. (Indien nodig) Download eventuele nieuwe foutbestanden, corrigeer de rijen en post het bestand opnieuw.

## Fouten beheren bij het uploaden en posten van campagnegegevens

Met Zoeken, Sociaal zoeken en Commerce uploadt en plaatst u zoveel rijen gegevens als u maar kunt op een bulkpagina voor campagnes, inclusief de URL&#39;s die worden gegenereerd wanneer dat nodig is.

Wanneer er fouten optreden tijdens het bewerken van een werkblad, wordt een van de volgende twee typen foutbestanden gegenereerd:

* **[!UICONTROL EF Errors]:** wanneer een bestand of afzonderlijke rijen in het bestand niet kunnen worden geüpload of verwerkt, wordt een foutbestand met de naam `<uploaded file name>_ef_errors.<extension used for the bulksheet>` gemaakt. Als het probleem met individuele rijen is, dan worden die rijen omvat, met een verklaring van elke fout zodat het kan worden verbeterd.

* **[!UICONTROL SE Errors]:** wanneer een bestand wordt gepost maar het advertentienetwerk sommige of alle gegevens niet accepteert, wordt een foutbestand met de naam `<uploaded file name>_se_errors.<extension used for the bulksheet>` gemaakt. Wanneer sommige maar niet alle rijen werden goedgekeurd, toont het foutendossier de rijen die niet werden gepost en een verklaring van elke fout zodat kan het worden verbeterd. De foutberichten worden weergegeven in de laatste drie kolommen van elke rij.

>[!NOTE]
>
>Als u [!DNL Google Ads] -advertenties plaatst die het advertentiebeleid van het advertentienetwerk overtreden maar in aanmerking komen voor uitzonderingen, worden deze advertenties automatisch opnieuw gepost met vrijstellingsaanvragen. Als de vrijstellingsaanvraag mislukt, wordt informatie over de schending opgenomen in het foutbestand.

U kunt beide typen foutbestanden downloaden, correcties rechtstreeks in de rijen aanbrengen en het bestand vervolgens opnieuw uploaden en posten.

Foutbestanden worden na 30 dagen automatisch verwijderd, tenzij u ze eerder verwijdert.

## Informatie over elk bestand

Alle gedownloade gegevensbestanden, geüploade bestanden en foutbestanden zijn beschikbaar via [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Bulksheets] .

De informatie voor elk dossier omvat de huidige taakstatus en het percentage van de taak die wordt voltooid, de datum het werd gecreeerd, (indien van toepassing) de datum het aan het gespecificeerde ad netwerk, de geplande schrappingsdatum, en de login naam van de gebruiker werd of zal worden gepost die de taak in werking stelde.

>[!MORELIKETHIS]
>
>* [ Download/creeer een bulksheet- dossier ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
>* [ upload een bulksheet of verbeterd foutendossier ](bulksheet-upload.md)
>* [ Post bulksbladen of gecorrigeerde foutendossiers ](bulksheet-post.md)
>* [ de Uitvoer een geproduceerd of geupload bulksbladdossier ](bulksheet-export.md)
