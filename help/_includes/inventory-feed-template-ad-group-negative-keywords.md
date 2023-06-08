---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# Tekst en sjabloon - Negatieve trefwoordinstellingen op groepsniveau toevoegen

**[!UICONTROL Delete negative keywords when omitted from list]:** (Alle en netwerken behalve Yandex; (optioneel) Hiermee verwijdert u bestaande negatieve trefwoorden op ad-hocniveau die eerder zijn gemaakt met de sjabloon die niet in de onderstaande lijsten zijn opgegeven. **Opmerking:** Negatieve trefwoorden die op andere manieren zijn gemaakt (zoals in gewone opsommingstekens, worden [!UICONTROL Campaigns] weergaven (of in de advertentienetwerkeditor) worden nooit verwijderd met de sjabloon.

**[!UICONTROL Apply these negatives]:** (Alle advertentienetwerken behalve [!DNL Yandex]; (optioneel) Eventuele negatieve trefwoorden op statisch en groepsniveau die moeten worden toegevoegd. Als u meerdere trefwoorden of meerdere overeenkomende typen voor hetzelfde trefwoord wilt opgeven, voert u deze op aparte regels in. Gebruik de volgende syntaxis, zonder een minteken:

* Negatieve brede overeenkomst: `keyword` (wordt niet ondersteund door [!DNL Microsoft Advertising])
* Negatieve woordovereenkomst: `"keyword"`
* Negatieve exacte overeenkomst: `[keyword]`

De gebruikelijke syntaxis voor uitdrukking en nauwkeurige gelijke types wordt gebruikt in bulksheet die wordt geproduceerd wanneer u voedergegevens door het malplaatje verspreidt. **Opmerking:** De negatieve trefwoorden kunt u niet zien in het dialoogvenster [!UICONTROL Keywords] of in de [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] weergeven.
