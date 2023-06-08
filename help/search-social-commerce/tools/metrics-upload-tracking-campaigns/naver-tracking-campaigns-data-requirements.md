---
title: Gegevensvereisten voor verkeers- en conversiemetriek voor [!DNL Naver] accounts met alleen traceren
description: Verwijzing naar de vereisten voor het uploaden van gegevens voor [!DNL Naver] accounts met het kenmerk Alleen bijhouden.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# Metrische gegevensvereisten voor [!DNL Naver] accounts met alleen traceren

Hieronder worden de gegevensvereisten voor [!DNL Naver] verkeers en omzettingsmetriek voor het volgen-slechts rekeningen.

Gegevensbestanden moeten de indeling TSV, CSV of TXT hebben.

De volgende koptekstvelden zijn vereist en optioneel. Elke gegevensrij moet voor ten minste één metrisch veld een dagelijks geaggregeerde waarde bevatten.

| Koptekstveld/kolomnaam | Type | Beschrijving |
| ---- | ---- | ---- |
| Periode | DateTime | De datum waarop de gegevens van toepassing zijn, in de vorm `YYYY.MM.DD.` (zoals `2019.11.15.`, met een periode na de dag). |
| Campagne | Hoofdlettergevoelige tekenreeks | De naam van de campagne. |
| Adgroup (als één woord) | Hoofdlettergevoelige tekenreeks | De naam van de advertentiegroep. |
| Trefwoord | Hoofdlettergevoelige tekenreeks | (Trefwoordadvertenties) Het trefwoord dat de advertentie heeft gegenereerd. |
| [Metrisch] | Geheel | (Optioneel) Het aantal [wat de meting is].</br><br>Standaardmetriek zijn onder andere Impressies, Kosten en Klikken. U kunt om het even welke extra metriek omvatten u van het advertentienetwerk wilt. Neem elke metrische waarde op in een aparte kolom.<br><br><b>Opmerkingen:</b><ul><li>De kolomkop voor Kosten moet &#39;Kosten (KRW)&#39; zijn.</li><li>Als u Kostprijs (KRW) wilt opnemen voor merkadvertenties, verdeelt u de vaste maandelijkse kosten handmatig op groepsniveau.</li><li>Verwijder alle komma&#39;s uit standaardmetrische waarden. Gebruik bijvoorbeeld 1000 in plaats van 1000.</li><li>Gebruik 0 voor null-waarden.</li></ul> |

>[!MORELIKETHIS]
>
>* [Implementeren [!DNL Naver] accounts met alleen traceren](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Aanhangsel - Vereiste gegevens voor het informatieblad voor [!DNL Naver] rekeningen](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [Verkeer- en conversiemetriek uploaden voor [!DNL Naver] accounts met alleen traceren](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)

