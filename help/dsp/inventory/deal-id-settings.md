---
title: Instellingen voor handmatige deal-id
description: Zie beschrijvingen van de montages voor manueel-binnengegaane overeenkomst IDs.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 9d3417cb-8b44-4f1c-afc4-eea6a2e5b9d7
source-git-commit: 21ed5558a39ea9b097be8e70ef81bcf8e59c14b4
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Instellingen voor handmatige deal-id

| Sectie | Parameter | Beschrijving | Vereist | Bewerkbaar |
|---------|-----------|-------------|----------|----------|
| [ Details van de Overeenkomst ] | [!UICONTROL Deal name] | De naam die uw [!UICONTROL Deal ID] in Advertising DSP moet identificeren. Voer een naam in of selecteer **[!UICONTROL Auto-name]** om DSP een naam te laten genereren op basis van de details van de deal.<br><br> Voorbeeld van een automatisch gegenereerde naam: `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | Ja | Ja |
| | [!UICONTROL External deal ID] | Identiteitskaart die door uw uitgever en SSP wordt gebruikt om deze overeenkomst te identificeren. | Ja | Nee |
| | [!UICONTROL Publisher] | De naam van de uitgever die deze voorraad verkoopt. | Ja | Nee |
| | [!UICONTROL SSP] | Het platform aan de aanbodzijde (SSP) waardoor deze overeenkomst loopt. | Ja | Nee |
| | [!UICONTROL Media type] | Het type media dat door deze deal wordt gekocht: *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]*, *[!UICONTROL Audio]* of *[!UICONTROL Publisher Managed]*. De opties variëren door SSP.<br><br> als de overeenkomst veelvoudige media types toestaat, selecteer het media type voor de standaardplaatsing wanneer u de overeenkomst creeert. Later, kunt u de waarde veranderen, of u kunt [ een nieuwe plaatsing met het extra media type ](deal-id-attach-placements.md) enkel vastmaken.<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Ja | Nee |
| | [!UICONTROL Deal type] | De overeenkomst verplichting en het tarief structuur:<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: U en de uitgever hebben zich niet verbonden aan een vast aantal impliciete afleveringen. De transactie specificeert de minimumprijs voor de voorraad, hoewel de CPM kan fluctueren en stijgen afhankelijk van de marktomstandigheden.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: U en de uitgever hebben zich niet verbonden aan een vast aantal impliciete afleveringen. Prijzen worden vastgesteld tegen een door onderhandelingen bepaalde vaste koers.</li><li>*[!UICONTROL Guaranteed (fixed)]*: U en de uitgever zijn het eens geworden over een vooraf gedefinieerd aantal indrukken, doelen, vluchtdatums en vaste prijs.<br><br><b> Nota:</b> de gewaarborgde overeenkomsten vereisen vluchtdata en een gespecificeerd aantal beelden in de [!UICONTROL Tracking] sectie. U moet ook een standaard programmatic gegarandeerde plaatsing (PG) voor de overeenkomst tot stand brengen, en u kunt naar keuze de overeenkomst voor andere plaatsen in plaats daarvan gebruiken.</li></ul> | Ja | Nee |
| | [!UICONTROL CPM] | De overeengekomen kosten per 1000 beelden (CPM). | Ja | Ja |
| | [ Valuta ] | De valuta voor de deal.<br><br> Alle SSPs keurt overeenkomsten in USD goed. Als het SSP de valuta voor je DSP-account accepteert, is die valuta ook beschikbaar. | Ja | Nee |
| | [!UICONTROL Billing method] | Alle deal-IDs wordt [!DNL Adobe]-gefinancierd en-gefactureerd. DSP betaalt alle beschikbare mediafabrikanten op basis van gebruik, beheert discrepanties met de leveranciers en stuurt één geconsolideerde factuur naar de account. Voor deze optie worden extra kosten in rekening gebracht zoals aangegeven op de betaalkaart van de account. | Ja | Nee |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | Het e-mailadres voor de gebruikersrekening die tot de overeenkomst kan toegang hebben. | Nee | Ja |
| | [!UICONTROL Advertisers that can access this deal] | De specifieke adverteerders in de rekening die tot deze overeenkomst kunnen toegang hebben.<br><br><b> Nota:</b> U kunt de overeenkomst met adverteerders in extra rekeningen van de [!UICONTROL Deals] mening delen. In de overeenkomstenrij, klik **[!UICONTROL #]**, klik **[!UICONTROL share]**, en deel dan de overeenkomst met een e-mailadres. | Ja | Ja |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | De begin en einddata voor verkeer die deze overeenkomst gebruiken. Deze datums zijn alleen bedoeld voor traceringsdoeleinden en hebben geen invloed op de levering.<br><br><b> Uiteinde:</b> in [!UICONTROL Inventory] > [!UICONTROL Deals] mening, toont de [!UICONTROL Pacing & Budget] kolom hoe de overeenkomst aan de gespecificeerde vluchtdatum en imperiatiedoel overgaat. Als de levering onderaan of overpakking is, contacteer uw uitgever om aan te passen hoeveel volume het door de overeenkomst verzendt. | Gegarandeerde overeenkomsten: Ja <br> niet-gegarandeerde overeenkomsten: Neen | Ja |
| | [!UICONTROL Impressions] | (Optioneel voor niet-gegarandeerde deals) Het geschatte aantal indrukkingen dat u verwacht te kunnen uitvoeren met deze deal. Deze waarde is alleen voor traceringsdoeleinden; de uitgever bestuurt en levert de gegevens. | Gegarandeerde overeenkomsten: Ja <br> niet-gegarandeerde overeenkomsten: Neen | Ja |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [ creeer manueel Deal ID Details ](deal-id-create.md)
>* [ SSP Partners ](ssp-partners.md)
>* [ Ongeveer Privé Inventaris ](private-inventory-about.md)
