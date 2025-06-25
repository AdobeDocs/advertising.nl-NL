---
title: Instellingen voor voedergegevens configureren
description: Leer hoe te om de montages te vormen die controleren hoe de voedergegevens worden verwerkt.
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# Instellingen voor voedergegevens configureren

*[!DNL Google Ads], [!DNL Microsoft Advertising] , [!DNL Yahoo! Japan Ads] (alleen acties verwijderen) en [!DNL Yandex] alleen accounts*

U kunt configureren hoe ad-hocgroepen, trefwoorden en advertenties in bestanden met feed-gegevens worden verwerkt, en hoe de gegevens in FTP-bestanden worden verwerkt, met name via de feed-instellingen.

1. Klik in het hoofdmenu op **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** .

1. Klik in de werkbalk boven de gegevenstabel op **[!UICONTROL Settings]** .

1. Specificeer de [ montages van voedergegevens ](#feed-data-settings):

   1. Selecteer in de sectie [!UICONTROL Obsolete Item Auto-Processing] informatie in de velden.

   1. (Adverteerders die gegevens uploaden via FTP of via een directe koppeling naar een bedrijfscentrum account) Selecteer in de sectie [!UICONTROL FTP/GMC Account Auto-Processing] informatie in de velden.

   1. Selecteer in de sectie [!UICONTROL Miscellaneous Auto-Processing] informatie in de velden.

1. Klik op **[!UICONTROL Save]**.

## Instellingen voor Feed-gegevens {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** past alle [!UICONTROL Obsolete Item Auto-processing] instellingen toe op:

* *[!UICONTROL Ad Groups Only]:* Alleen verouderde advertentiegroepen.

* *[!UICONTROL Keywords Only]:* Alleen verouderde trefwoorden en productgroepen.

* *[!UICONTROL Ad Variations Only]* (de standaardwaarde): alleen verouderde advertenties.

* *[!UICONTROL Keywords and Ad Variations]:* Zowel verouderde trefwoorden/productdoelen/productgroepen als verouderde advertenties.

>[!NOTE]
>
>* Voor [!DNL Google Ads] winkeladvertenties heeft dit alleen invloed op de laagste productgroep.
>* Voor [!DNL Yandex] -accounts worden verouderde automatische verwerkingstaken voor items altijd uitgevoerd op en variaties, ongeacht deze instelling.

**[!UICONTROL When the Scheduled End Date is reached]:** (manueel geposte gegevens slechts) wat te doen met lijnpunten in een voederdossier dat met een gespecificeerde einddatum en een tijd wordt gepost zodra de eindtijd aankomt:

* *[!UICONTROL Delete]* (de standaardwaarde): verwijder alle relevante componenten wanneer de opgegeven eindtijd aankomt. U kunt deze bewerking niet omkeren.

* *[!UICONTROL Pause]:* pauzeer alle relevante componenten wanneer de gespecificeerde eindtijd aankomt. U kunt de componenten later desgewenst opnieuw activeren.

* *[!UICONTROL None]:* verander niet de status van de relevante componenten.

**[!UICONTROL Missing line items in a manually uploaded feed]:** wat te doen met bestaande punten wanneer zij niet inbegrepen in een nieuw voederdossier zijn dat manueel werd geupload of wanneer zij niet aan bestaande campagnes of ad groepen per de montages van de Kaart slechts in het malplaatje in kaart brengen:

* *[!UICONTROL Delete]:* schrap de bestaande componenten.

* *[!UICONTROL Pause]:* onderbreek de bestaande componenten. Ze worden opnieuw geactiveerd als een nieuw feed-bestand dezelfde lijstitems bevat en ze behouden hun historie- en kwaliteitsscores. **Nota:** als alle groepen van het kindproduct voor een groep van het ouderproduct ontbreken, dan wordt de groep van het ouderproduct geschrapt omdat u niet productgroepen kunt pauzeren.

* *[!UICONTROL None]* (de standaardwaarde): wijzig de bestaande componenten niet.

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** wat te doen met bestaande punten wanneer 1) zij niet inbegrepen a) in een nieuw voederdossier zijn dat aan een folder van FTP of b) in een bedrijfscentrum rekening werd geupload de volgende tijd dat Onderzoek, Sociale, &amp; Commerce met het synchroniseert, of 2) wanneer zij niet aan bestaande campagnes of ad groepen volgens de [!UICONTROL Map Only] montages in het malplaatje in kaart brengen.

* *[!UICONTROL Delete]:* schrap de bestaande componenten.

* *[!UICONTROL Pause]:* onderbreek de bestaande componenten. Ze worden opnieuw geactiveerd als nieuwe gegevens dezelfde lijstitems bevatten en hun geschiedenis en kwaliteitsscore behouden. **Nota:** als alle groepen van het kindproduct voor een groep van het ouderproduct ontbreken, dan wordt de groep van het ouderproduct geschrapt omdat u niet productgroepen kunt pauzeren.

* *[!UICONTROL None]* (de standaardwaarde): wijzig de bestaande componenten niet.

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** wat te doen met lijnpunten die een voorraadniveau omvatten wanneer:

* (Voor diervoeders met uitsluitend numerieke waarden in de opgegeven kolom) Het voorraadniveau is op of onder een bepaalde hoeveelheid. De standaardhoeveelheid is nul (0).

* (Voor feeds met tekstwaarden in de opgegeven kolom) De waarde voor [!UICONTROL Availability] is &quot;[!UICONTROL out of stock]&quot;; de waarde is niet hoofdlettergevoelig. **Nota:** **In voedermalplaatjes, wijs op tekst-gebaseerde kolommen van het voorraadniveau gebruikend de controledoos voor &quot;[!UICONTROL This column has non-numeric values]&quot;.

Selecteer de actie voor beide gevallen:

* *[!UICONTROL Delete]* (standaard) Verwijder de componenten.

* *[!UICONTROL Pause]:* onderbreek de componenten. Wanneer de gegevens worden bijgewerkt, worden de componenten opnieuw geactiveerd als de numerieke voorraadwaarden boven de gespecificeerde hoeveelheid gaan of als [!UICONTROL Availability] &quot; [!UICONTROL in stock]&quot;of &quot;[!UICONTROL preorder]&quot;is. De componenten behouden hun geschiedenis en kwaliteitsscore.

Het voorraadniveau voor elk lijnpunt komt uit een kolom in het voederingsdossier, zoals die in het &quot;[!UICONTROL Stock Level]&quot;gebied voor elke malplaatje wordt gespecificeerd.

>[!TIP]
>
>* Voor producten of de diensten die u verwacht om beschikbaarheid te hervoorraden of te verhogen voor, zou u ad groepen, sleutelwoorden, en advertenties eerder dan hen te schrappen en hen te ontspannen. Door te pauzeren kunnen ze hun kwaliteitsscores behouden.
>* Als u verouderde automatische verwerking voor advertentiegroepen inschakelt en nieuwe gegevens een voorraadniveau voor de advertentiegroep bevatten, is het zinvol om de advertentiegroep alleen te verwijderen of te pauzeren wanneer het opgegeven voorraadniveau zich op categorieniveau bevindt in plaats van op het merk/artikelniveau. Als u bijvoorbeeld een ad-groep &quot;convertibles&quot; hebt, moet het voorraadniveau voor de ad-groep het totaal zijn voor alle afzonderlijke converteerbare modellen die in de ad-groep worden vertegenwoordigd.

**[!UICONTROL Propagate feed data through all applicable templates]:** (Advertisers die gegevensdossiers via FTP of een bedrijfscentrum rekening uploaden) verspreidt automatisch nieuwe gegevens door de toepasselijke malplaatjes. De optie is standaard geselecteerd. Als u de optie uitschakelt, kunt u nog steeds handmatig gegevens doorgeven voor een feed-bestand of -account, of voor een sjabloon.

>[!NOTE]
>
>* Voor FTP-bestanden controleert de voederservice om de twee uur op updates in de FTP-map (even genummerde uren in de PST-tijdzone). Met deze optie verwerkt u alle bestanden die sinds de laatste controle zijn geüpload.
>* Voor zakelijke accounts synchroniseert Search, Social &amp; Commerce dagelijks met het account om ongeveer 6:00 uur in de tijdzone van de adverteerder. Met deze optie verwerkt u alle gegevens die zijn bijgewerkt sinds de laatste synchronisatie.
>* Gepagieerde gegevens zijn beschikbaar op de tabbladen [!UICONTROL Campaigns] , [!UICONTROL Ad Groups] , [!UICONTROL Keywords] en [!UICONTROL Ads] totdat de gegevens naar het advertentienetwerk of de weergave [!UICONTROL Bulksheets] worden gepost.

**[!UICONTROL Post to the SE]:** (Adverteerders die gegevensdossiers via FTP of een bedrijfscentrum rekening uploaden) creeert automatisch bulkbladdossiers in de correcte formaten voor de relevante advertentienetwerken nadat de nieuwe gegevens door de toepasselijke malplaatjes worden verspreid. Met deze optie worden ook de gegevens verwijderd van de tabbladen [!UICONTROL Campaigns] , [!UICONTROL Ad Groups] , [!UICONTROL Keywords] en [!UICONTROL Ads] , tenzij subcomponenten fouten bevatten.

Deze optie is standaard uitgeschakeld. Als u deze optie wilt inschakelen, schakelt u het selectievakje in en geeft u op of u bladbestanden met opsommingstekens wilt posten op de advertentienetwerken:

* *[!UICONTROL Immediately]* (het gebrek): Post de bulkbladdossiers aan de relevante advertentienetwerken nadat het gegeven door de malplaatjes wordt verspreid. De bulksbladbestanden blijven 30 dagen beschikbaar in de weergave [!UICONTROL Bulksheets] .

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:** Plaatst de bulksbladdossiers niet aan de relevante ad netwerken maar maakt een lijst van hen in de [!UICONTROL Bulksheets] mening, waaruit u hen kunt later posten. De bulksbladbestanden blijven 30 dagen beschikbaar in de weergave [!UICONTROL Bulksheets] . Wanneer het bulksbladbestand groter is dan 10 MB maar kleiner dan 2 GB, heeft het bestand de ZIP-indeling. U hoeft het bestand niet uit te pakken om het te posten. **Uiteinde:** als u uw het landen pagina&#39;s niet eerder hebt bevestigd, dan gebruik deze optie zodat kunt u hen van de [!UICONTROL Bulksheets] mening bevestigen alvorens u de gegevens aan het advertentienetwerk post.

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** sluit het posten van sleutelwoorduitdrukkingen met meer dan een gespecificeerd aantal woorden aan het advertentienetwerk uit. Als deze optie is geselecteerd, worden trefwoordwoordzinnen met meer dan het maximale aantal woorden doorgegeven en weergegeven op het tabblad [!UICONTROL Keywords] , maar worden ze niet gepost wanneer u de gegevens probeert te posten.

Deze optie is standaard uitgeschakeld, zodat alle trefwoorden worden gepost, ongeacht het aantal woorden dat de woordgroep bevat. Als u deze optie selecteert, selecteert u het maximumaantal woorden dat u wilt posten (van 3-10).

>[!MORELIKETHIS]
>
>* [ Ongeveer inventarisvoer ](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [ doorgeven voedergegevens door malplaatjes ](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [ Post campagnegegevens die van voer aan ad netwerken worden geproduceerd ](propagated-data-post.md)
