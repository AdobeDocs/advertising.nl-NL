---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---
# Tekst en sjabloon - Instellingen voor negatieve trefwoorden op campagnereniveau

**[!UICONTROL Delete negative keywords when omitted from list]:** (Alle en netwerken behalve Yandex; (optioneel) Verwijdert bestaande negatieve trefwoorden op campagneniveau die eerder zijn gemaakt met de sjabloon die niet in de onderstaande lijsten zijn opgegeven. **Opmerking:** Negatieve trefwoorden die op andere manieren zijn gemaakt (zoals in gewone opsommingstekens, worden [!UICONTROL Campaigns] weergaven (of in de advertentienetwerkeditor) worden nooit verwijderd met de sjabloon.

**[!UICONTROL Set negative keywords by campaign name condition]:** (Alle en netwerken behalve Yandex; (optioneel) Hiermee kunt u negatieve trefwoorden opgeven voor campagnes waarvan de naam een opgegeven tekenreeks bevat. Wanneer u deze optie selecteert, kunt u maximaal drie campagnenaam-tekenreeksen en bijbehorende trefwoorden toevoegen.

Klik voor elke tekenreeks op **[!UICONTROL Add (Up to 3)]** en voert u de volgende gegevens in:

* **[!UICONTROL If campaign name contains]:**  Een tekstreeks die overal binnen de naam van de campagne moet worden gezocht. De query is hoofdlettergevoelig (bijvoorbeeld &quot;[!DNL Car]&quot; komt overeen met de naam van de campagne &quot;[!DNL Car Parts]&quot; maar niet &quot;[!DNL INTERIOR CAR ACCESSORIES]&quot;).

* **[!UICONTROL Apply these negatives]:**  Eventuele negatieve trefwoorden op campagneniveau op statisch niveau die moeten worden toegevoegd voor campagnes waarvan de naam de opgegeven tekenreeks bevat. Als u meerdere trefwoorden of meerdere overeenkomende typen voor hetzelfde trefwoord wilt opgeven, voert u deze op aparte regels in. Gebruik de volgende syntaxis, zonder een minteken:

   * Negatieve brede overeenkomst: `keyword` (wordt niet ondersteund door [!DNL Microsoft Advertising])
   * Negatieve woordovereenkomst: `"keyword"`
   * Negatieve exacte overeenkomst: `[keyword]`

De gebruikelijke syntaxis voor uitdrukking en nauwkeurige gelijke types wordt gebruikt in bulksheet die wordt geproduceerd wanneer u voedergegevens door het malplaatje verspreidt. **Opmerking:** De negatieve trefwoorden kunt u niet zien in het dialoogvenster [!UICONTROL Keywords] of in de [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] weergeven.

**[!UICONTROL All other campaigns: Apply these negatives]:** (Alle advertentienetwerken behalve [!DNL Yandex]; (optioneel) Eventuele negatieve trefwoorden op campagneniveau op statisch niveau die moeten worden toegevoegd voor campagnes waarvan de naam niet overeenkomt met een opgegeven tekenreeks. Als u meerdere trefwoorden of meerdere overeenkomende typen voor hetzelfde trefwoord wilt opgeven, voert u deze op aparte regels in. Gebruik de volgende syntaxis, zonder een minteken:

* Negatieve brede overeenkomst: `keyword` (wordt niet ondersteund door [!DNL Microsoft Advertising])
* Negatieve woordovereenkomst: `"keyword"`
* Negatieve exacte overeenkomst: `[keyword]`

De gebruikelijke syntaxis voor uitdrukking en nauwkeurige gelijke types wordt gebruikt in bulksheet die wordt geproduceerd wanneer u voedergegevens door het malplaatje verspreidt. **Opmerking:** De negatieve trefwoorden kunt u niet zien in het dialoogvenster [!UICONTROL Keywords] of in de [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] weergeven.
