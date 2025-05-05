---
title: Instellingen voor voedergegevens configureren
description: Leer hoe te om de montages te vormen die controleren hoe de voedergegevens worden verwerkt.
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# Instellingen voor voedergegevens configureren

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (alleen handelingen verwijderen), en [!DNL Yandex] alleen accounts*

U kunt configureren hoe ad-hocgroepen, trefwoorden en advertenties in bestanden met feed-gegevens worden verwerkt, en hoe de gegevens in FTP-bestanden worden verwerkt, met name via de feed-instellingen.

1. Klik in het hoofdmenu op **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Klik op de werkbalk boven de tabel met gegevens op **[!UICONTROL Settings]**.

1. Geef de [gegevensinstellingen van feed](#feed-data-settings):

   1. In de [!UICONTROL Obsolete Item Auto-Processing] selecteert u informatie in de velden.

   1. (Adverteerders die gegevens uploaden via FTP of via een directe koppeling naar een bedrijfscentrum account) [!UICONTROL FTP/GMC Account Auto-Processing] selecteert u informatie in de velden.

   1. In de [!UICONTROL Miscellaneous Auto-Processing] selecteert u informatie in de velden.

1. Klik op **[!UICONTROL Save]**.

## Instellingen voor Feed-gegevens {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** Hiermee past u alle [!UICONTROL Obsolete Item Auto-processing] instellingen voor:

* *[!UICONTROL Ad Groups Only]:* Alleen verouderde advertentiegroepen.

* *[!UICONTROL Keywords Only]:* Alleen verouderde trefwoorden en productgroepen.

* *[!UICONTROL Ad Variations Only]* (de standaardwaarde): alleen verouderde advertenties.

* *[!UICONTROL Keywords and Ad Variations]:* Zowel verouderde trefwoorden/productdoelen/productgroepen als verouderde advertenties.

>[!NOTE]
>
>* Voor [!DNL Google Ads] advertentiespots, alleen de laagste productgroep wordt beïnvloed.
>* Voor [!DNL Yandex] accounts, verouderde automatische verwerkingstaken voor items worden altijd uitgevoerd op en variaties, ongeacht deze instelling.

**[!UICONTROL When the Scheduled End Date is reached]:** (Alleen handmatig geposte gegevens) Wat moet u doen met regelitems in een feed-bestand die met een opgegeven einddatum en tijd worden gepost zodra de eindtijd aankomt:

* *[!UICONTROL Delete]* (de standaardwaarde): verwijder alle relevante componenten wanneer de opgegeven eindtijd aankomt. U kunt deze bewerking niet omkeren.

* *[!UICONTROL Pause]:* Pauzeren alle relevante componenten wanneer de gespecificeerde eindtijd aankomt. U kunt de componenten later desgewenst opnieuw activeren.

* *[!UICONTROL None]:* Wijzig de status van de relevante componenten niet.

**[!UICONTROL Missing line items in a manually uploaded feed]:** Wat te doen met bestaande punten wanneer zij niet inbegrepen in een nieuw voederdossier zijn dat manueel werd geupload of wanneer zij niet aan bestaande campagnes of ad groepen per de montages van de Kaart slechts in het malplaatje in kaart brengen:

* *[!UICONTROL Delete]:* Verwijder de bestaande componenten.

* *[!UICONTROL Pause]:* Onderbreek de bestaande componenten. Ze worden opnieuw geactiveerd als een nieuw feed-bestand dezelfde lijstitems bevat en ze behouden hun historie- en kwaliteitsscores. **Opmerking:** Als alle onderliggende productgroepen voor een bovenliggende productgroep ontbreken, wordt de bovenliggende productgroep verwijderd omdat u de productgroepen niet kunt onderbreken.

* *[!UICONTROL None]* (de standaardwaarde): wijzig de bestaande componenten niet.

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** Wat te doen met bestaande punten wanneer 1) zij niet inbegrepen a) in een nieuw voederdossier zijn dat aan een folder van FTP of b) in een handelscentrum rekening werd geupload de volgende keer dat Onderzoek, Sociale, &amp; Commerce met het synchroniseert, of 2) wanneer zij niet aan bestaande campagnes of advertentiegroepen per [!UICONTROL Map Only] instellingen in de sjabloon.

* *[!UICONTROL Delete]:* Verwijder de bestaande componenten.

* *[!UICONTROL Pause]:* Onderbreek de bestaande componenten. Ze worden opnieuw geactiveerd als nieuwe gegevens dezelfde lijstitems bevatten en hun geschiedenis en kwaliteitsscore behouden. **Opmerking:** Als alle onderliggende productgroepen voor een bovenliggende productgroep ontbreken, wordt de bovenliggende productgroep verwijderd omdat u de productgroepen niet kunt onderbreken.

* *[!UICONTROL None]* (de standaardwaarde): wijzig de bestaande componenten niet.

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** Wat te doen met lijnpunten die een voorraadniveau omvatten wanneer:

* (Voor diervoeders met uitsluitend numerieke waarden in de opgegeven kolom) Het voorraadniveau is op of onder een bepaalde hoeveelheid. De standaardhoeveelheid is nul (0).

* (Voor feeds met tekstwaarden in de opgegeven kolom) De waarde voor [!UICONTROL Availability] is &quot;[!UICONTROL out of stock]&quot;; de waarde is niet hoofdlettergevoelig. **Opmerking:** **Geef in voedersjablonen op welk voorraadniveau op basis van tekst wordt gebruikt het selectievakje voor &quot;[!UICONTROL This column has non-numeric values].&quot;

Selecteer de actie voor beide gevallen:

* *[!UICONTROL Delete]* (standaard) Verwijder de componenten.

* *[!UICONTROL Pause]:* Pauzeer de componenten. Wanneer de gegevens worden bijgewerkt, worden de componenten opnieuw geactiveerd als de numerieke voorraadwaarden boven de opgegeven hoeveelheid komen of als de [!UICONTROL Availability] is &quot;[!UICONTROL in stock]&quot; of &quot;[!UICONTROL preorder]&quot;. De componenten behouden hun geschiedenis en kwaliteitsscore.

Het voorraadniveau voor elk lijnitem komt uit een kolom in het voederbestand, zoals gespecificeerd in &quot;[!UICONTROL Stock Level]&quot; veld voor elke sjabloon.

>[!TIP]
>
>* Voor producten of de diensten die u verwacht om beschikbaarheid te hervoorraden of te verhogen voor, zou u ad groepen, sleutelwoorden, en advertenties eerder dan hen te schrappen en hen te ontspannen. Door te pauzeren kunnen ze hun kwaliteitsscores behouden.
>* Als u verouderde automatische verwerking voor advertentiegroepen inschakelt en nieuwe gegevens een voorraadniveau voor de advertentiegroep bevatten, is het zinvol om de advertentiegroep alleen te verwijderen of te pauzeren wanneer het opgegeven voorraadniveau zich op categorieniveau bevindt in plaats van op het merk/artikelniveau. Als u bijvoorbeeld een ad-groep &quot;convertibles&quot; hebt, moet het voorraadniveau voor de ad-groep het totaal zijn voor alle afzonderlijke converteerbare modellen die in de ad-groep worden vertegenwoordigd.

**[!UICONTROL Propagate feed data through all applicable templates]:** (Adverteerders die gegevensbestanden uploaden via FTP of een bedrijfscentrum account) verspreiden automatisch nieuwe gegevens via de toepasselijke sjablonen. De optie is standaard geselecteerd. Als u de optie uitschakelt, kunt u nog steeds handmatig gegevens doorgeven voor een feed-bestand of -account, of voor een sjabloon.

>[!NOTE]
>
>* Voor FTP-bestanden controleert de voederservice om de twee uur op updates in de FTP-map (even genummerde uren in de PST-tijdzone). Met deze optie verwerkt u alle bestanden die sinds de laatste controle zijn geüpload.
>* Voor zakelijke accounts synchroniseert Search, Social &amp; Commerce dagelijks met het account om ongeveer 6:00 uur in de tijdzone van de adverteerder. Met deze optie verwerkt u alle gegevens die zijn bijgewerkt sinds de laatste synchronisatie.
>* Doorgeven gegevens zijn beschikbaar via de [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] tabs totdat de gegevens naar het advertentienetwerk of naar het [!UICONTROL Bulksheets] weergeven.

**[!UICONTROL Post to the SE]:** (Adverteerders die gegevensbestanden uploaden via FTP of een bedrijfscentrum-account) maken automatisch bulksbladbestanden in de juiste indelingen voor de relevante advertentienetwerken nadat nieuwe gegevens zijn doorgegeven via de toepasselijke sjablonen. Met deze optie verwijdert u ook de gegevens uit het dialoogvenster [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], en [!UICONTROL Ads] tabs, tenzij subcomponenten fouten bevatten.

Deze optie is standaard uitgeschakeld. Als u deze optie wilt inschakelen, schakelt u het selectievakje in en geeft u op of u bladbestanden met opsommingstekens wilt posten op de advertentienetwerken:

* *[!UICONTROL Immediately]* (het gebrek): Post de bulkbladdossiers aan de relevante advertentienetwerken nadat het gegeven door de malplaatjes wordt verspreid. De bulksbladbestanden blijven beschikbaar in het dialoogvenster [!UICONTROL Bulksheets] weergegeven gedurende 30 dagen.

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:**&#x200B; Plaatst de bulkbladbestanden niet op de relevante advertentienetwerken, maar vermeldt deze in het dialoogvenster [!UICONTROL Bulksheets] bekijken, waaruit u ze later kunt posten. De bulksbladbestanden blijven beschikbaar in het dialoogvenster [!UICONTROL Bulksheets] weergegeven gedurende 30 dagen. Wanneer het bulksbladbestand groter is dan 10 MB maar kleiner dan 2 GB, heeft het bestand de ZIP-indeling. U hoeft het bestand niet uit te pakken om het te posten. &#x200B;** Tip:** Als u uw bestemmingspagina&#39;s niet eerder hebt bevestigd, dan gebruik deze optie zodat kunt u hen van bevestigen [!UICONTROL Bulksheets] bekijk alvorens u de gegevens aan het ad netwerk post.

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** Voorkomt het posten van sleutelwoorduitdrukkingen met meer dan een gespecificeerd aantal woorden aan het advertentienetwerk. Als deze optie is geselecteerd, worden trefwoordwoordwoordgroepen met meer dan het maximale aantal woorden doorgegeven en weergegeven op de [!UICONTROL Keywords] , maar deze worden niet gepost wanneer u de gegevens probeert te posten.

Deze optie is standaard uitgeschakeld, zodat alle trefwoorden worden gepost, ongeacht het aantal woorden dat de woordgroep bevat. Als u deze optie selecteert, selecteert u het maximumaantal woorden dat u wilt posten (van 3-10).

>[!MORELIKETHIS]
>
>* [Informatie over voorraadfeeds](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Doorvoergegevens doorgeven via sjablonen](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [Gegevens van de post campagne die van voer aan advertentienetwerken worden geproduceerd](propagated-data-post.md)
