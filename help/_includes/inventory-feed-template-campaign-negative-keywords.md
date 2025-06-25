---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---
# Tekst en sjabloon - Instellingen voor negatieve trefwoorden op campagnereniveau

**[!UICONTROL Delete negative keywords when omitted from list]:** (Alle ad netwerken behalve Yandex; facultatief) schrapt bestaande campagne-vlakke negatieve sleutelwoorden eerder gecreeerd gebruikend het malplaatje die niet in de hieronder lijsten worden gespecificeerd. **Nota:** Negatieve sleutelwoorden die worden gecreeerd gebruikend andere middelen (zoals in gewone bulksbladen, de [!UICONTROL Campaigns] meningen, of in de ad redacteur van het advertentienetwerk) worden nooit verwijderd gebruikend het malplaatje.

**[!UICONTROL Set negative keywords by campaign name condition]:** (Alle advertentienetwerken behalve Yandex; facultatief) staat u toe om negatieve sleutelwoorden voor campagnes te specificeren de waarvan naam een gespecificeerde koord omvat. Wanneer u deze optie selecteert, kunt u maximaal drie campagnenaam-tekenreeksen en bijbehorende trefwoorden toevoegen.

Klik voor elke tekenreeks op **[!UICONTROL Add (Up to 3)]** en voer de volgende informatie in:

* **[!UICONTROL If campaign name contains]:** een tekstkoord om binnen de campagnenaam overal te zoeken. De vraag is case-sensitive (bijvoorbeeld, &quot;[!DNL Car]&quot;past de campagnenaam &quot;[!DNL Car Parts]&quot;maar niet &quot;[!DNL INTERIOR CAR ACCESSORIES]&quot;) aan.

* **[!UICONTROL Apply these negatives]:** Om het even welke statische campagne-vlakke negatieve sleutelwoorden om voor campagnes toe te voegen de waarvan naam het gespecificeerde koord omvat. Als u meerdere trefwoorden of meerdere overeenkomende typen voor hetzelfde trefwoord wilt opgeven, voert u deze op aparte regels in. Gebruik de volgende syntaxis, zonder een minteken:

   * Negatieve brede overeenkomst: `keyword` (wordt niet ondersteund door [!DNL Microsoft Advertising])
   * Negatieve woordgroep komt overeen: `"keyword"`
   * Negatieve exacte overeenkomst: `[keyword]`

De gebruikelijke syntaxis voor uitdrukking en nauwkeurige gelijke types wordt gebruikt in bulksheet die wordt geproduceerd wanneer u voedergegevens door het malplaatje verspreidt. **Nota:** u kunt niet de negatieve sleutelwoorden in het [!UICONTROL Keywords] lusje of in [!UICONTROL Search, Social, & Commerce] zien > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] mening.

**[!UICONTROL All other campaigns: Apply these negatives]:** (Alle advertentienetwerken behalve [!DNL Yandex]; facultatief) Om het even welke statische op campagneniveau negatieve sleutelwoorden om voor campagnes toe te voegen de waarvan naam een gespecificeerde koord niet aanpast. Als u meerdere trefwoorden of meerdere overeenkomende typen voor hetzelfde trefwoord wilt opgeven, voert u deze op aparte regels in. Gebruik de volgende syntaxis, zonder een minteken:

* Negatieve brede overeenkomst: `keyword` (wordt niet ondersteund door [!DNL Microsoft Advertising])
* Negatieve woordgroep komt overeen: `"keyword"`
* Negatieve exacte overeenkomst: `[keyword]`

De gebruikelijke syntaxis voor uitdrukking en nauwkeurige gelijke types wordt gebruikt in bulksheet die wordt geproduceerd wanneer u voedergegevens door het malplaatje verspreidt. **Nota:** u kunt niet de negatieve sleutelwoorden in het [!UICONTROL Keywords] lusje of in [!UICONTROL Search, Social, & Commerce] zien > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] mening.
