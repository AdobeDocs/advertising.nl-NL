---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# Tekst en sjabloon - Negatieve trefwoordinstellingen op groepsniveau toevoegen

**[!UICONTROL Delete negative keywords when omitted from list]:** (Alle ad netwerken behalve Yandex; facultatief) schrapt bestaande en groep-vlakke negatieve sleutelwoorden eerder gecreeerd gebruikend het malplaatje die niet in de hieronder lijsten worden gespecificeerd. **Nota:** Negatieve sleutelwoorden die worden gecreeerd gebruikend andere middelen (zoals in gewone bulksbladen, de [!UICONTROL Campaigns] meningen, of in de ad redacteur van het advertentienetwerk) worden nooit verwijderd gebruikend het malplaatje.

**[!UICONTROL Apply these negatives]:** (Alle en netwerken behalve [!DNL Yandex]; optioneel) Alle negatieve trefwoorden op statisch en groepsniveau die moeten worden toegevoegd. Als u meerdere trefwoorden of meerdere overeenkomende typen voor hetzelfde trefwoord wilt opgeven, voert u deze op aparte regels in. Gebruik de volgende syntaxis, zonder een minteken:

* Negatieve brede overeenkomst: `keyword` (wordt niet ondersteund door [!DNL Microsoft Advertising])
* Negatieve woordgroep komt overeen: `"keyword"`
* Negatieve exacte overeenkomst: `[keyword]`

De gebruikelijke syntaxis voor uitdrukking en nauwkeurige gelijke types wordt gebruikt in bulksheet die wordt geproduceerd wanneer u voedergegevens door het malplaatje verspreidt. **Nota:** u kunt niet de negatieve sleutelwoorden in het [!UICONTROL Keywords] lusje of in [!UICONTROL Search, Social, & Commerce] zien > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] mening.
