---
title: Wanneer worden accountcomponenten gemaakt of verwijderd door voorraadfeeds?
description: Leer welke situaties accountcomponenten maken en verwijderen wanneer u voorraadfeeds plaatst.
exl-id: 39a3cc2c-f956-4a89-a69d-687a27a38a1e
feature: Search Inventory Feeds
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 0%

---

# Wanneer worden accountcomponenten gemaakt of verwijderd door voorraadfeeds?

*[!DNL Google Ads], [!DNL Microsoft Advertising] , [!DNL Yahoo! Japan Ads] (alleen acties verwijderen) en [!DNL Yandex] alleen accounts*

Wanneer een dossier van de inventarisvoer door een malplaatje wordt verspreid, worden de rekeningscomponenten gecreeerd en als volgt geschrapt.

>[!NOTE]
>
>Er worden nooit dubbele advertenties gemaakt in een advertentiegroep.

| Scenario | Voorbeeld | Handeling |
|----|----|----|
| De gegevens van het voer omvatten een nieuwe waarde voor een kolom die in een campagnenaam, een groepsnaam, een sleutelwoord, of een productgroep wordt gebruikt. | Vorige dossiers:<br> Campaign=Hats <br> Campaign=Ghandschoenen <br><br> Nieuw dossier:<br> Campaign=Shoes | Er wordt een nieuwe campagne, advertentiegroep, trefwoord of productgroep gemaakt als deze niet bestaat op het advertentienetwerk. |
| Diervoedergegevens bevatten een nieuwe waarde voor een kolom die in een advertentie wordt gebruikt. | Vorig dossier: Een advertentie omvatte price=20 <br><br> Nieuw dossier: Voor de zelfde advertentie, price=10 | Wanneer de advertentie voor [!DNL Microsoft Advertising] uitgevouwen tekstadvertenties, [!DNL Yahoo! Japan ads] - of [!DNL Yandex] -advertenties wordt gewijzigd, wordt de bestaande advertentie verwijderd en wordt een nieuwe advertentie gemaakt.<br><br> wanneer het advertentiekopie voor andere advertentietypes of wanneer de toepasselijke kolom voor een [!DNL Google Ads] advertentieparameter ({param1} of {param2}) in een advertentie wordt veranderd, dan wordt de bestaande advertentie bijgewerkt. |
| De malplaatjemontages voor de campagne, en de groep, het sleutelwoord, of de productgroep veranderden sinds de laatste propagatie. | Vorig plaatsen :Keyword= [ Trefwoord ]<br><br> Nieuwe het plaatsen: Trefword=&lt;Color> [ Trefwoord ] | Er wordt een nieuwe campagne, advertentiegroep, trefwoord of productgroep gemaakt als deze niet bestaat op het advertentienetwerk. |
| De malplaatjemontages voor een advertentie veranderden sinds de laatste propagatie. | Vorige het plaatsen: Addescription= &quot;koop [ categorie ] nu.&quot;<br><br> Nieuwe het plaatsen: Ad description= &quot;koop [ merk ] nu.&quot; | Wanneer de advertentie voor [!DNL Microsoft Advertising] uitgevouwen tekstadvertenties, [!DNL Yahoo! Japan ads] - of [!DNL Yandex] -advertenties wordt gewijzigd, wordt de bestaande advertentie verwijderd en wordt een nieuwe advertentie gemaakt.<br><br> wanneer het ad exemplaar voor andere advertentietypes wordt veranderd of wanneer de verandering op een verandering in de kolom wijst die voor één enkele [!DNL Google Ads] wordt gebruikt ad parameter ({param1} of {param2}) in een advertentie, dan wordt de bestaande advertentie bijgewerkt. |
| Nieuwe voedergegevens omvatten geen rij voor een bestaande campagne of een advertentiegroep. | nvt | De bestaande campagnes en advertentiegroepen blijven ongewijzigd. |
| Nieuwe feed-gegevens bevatten geen rij voor een bestaande advertentiegroep, advertentie, trefwoord of productgroep. | nvt | De bestaande advertentiegroep, de advertentie, het sleutelwoord, of de productgroep blijft zoals-is, wordt gepauzeerd, of wordt geschrapt, volgens de [ montages van de voedergegevens ](feed-settings-manage.md#feed-data-settings). |
| Nieuwe voedergegevens voor een bestaande ouderproductgroep omvatten geen rijen voor zijn bestaande kindproductgroepen. | nvt | De bestaande groep van het ouderproduct blijft zoals-is of geschrapt, volgens de [ montages van de voedergegevens ](feed-settings-manage.md#feed-data-settings). <b> Nota:</b> als de montages van voedergegevens worden gevormd om ontbrekende lijnpunten te pauzeren, dan wordt de groep van het ouderproduct nog geschrapt omdat u niet productgroepen kunt pauzeren. |
| De nieuwe voedergegevens omvatten een rij voor een advertentiegroep, een advertentie, een sleutelwoord, of een productgroep die a) in vorige gegevens was maar b) werd weggelaten sindsdien en volgens de [ montages van voedergegevens ](feed-settings-manage.md#feed-data-settings) gepauzeerd. | nvt | De bestaande advertentiegroep, advertentie, trefwoord of productgroep wordt opnieuw geactiveerd, zonder dat er geschiedenis of kwaliteitsscore verloren gaat. |
| De nieuwe voedergegevens omvatten een rij voor een advertentiegroep, een advertentie, een sleutelwoord, of een productgroep die a) in vorige gegevens was maar b) werd weggelaten sindsdien en werd geschrapt volgens de [ montages van voedergegevens ](feed-settings-manage.md#feed-data-settings). | nvt | Er wordt een nieuwe advertentiegroep, advertentie, trefwoord of productgroep gemaakt. |
| U hebt de campagne- of groep-vlakke optie aan &quot;[!UICONTROL Delete negative keywords when omitted from list]&quot;onbruikbaar gemaakt. | De negatieve trefwoordenlijst bevat &quot;coupe&quot; en &quot;sport car&quot;.<br><br> de ad groep omvat reeds het negatieve sleutelwoord &quot;SUV.&quot; | Eventuele negatieve trefwoorden die niet in de lijst staan, blijven ongewijzigd. |
| U hebt de campagne- of groep-vlakke optie aan &quot;[!UICONTROL Delete negative keywords when omitted from list] toegelaten,&quot;en negatieve sleutelwoorden die niet op de lijst zijn bestaan. | De negatieve trefwoordenlijst bevat &quot;coupe&quot; en &quot;sport car&quot;.<br><br> de ad groep omvat reeds het negatieve sleutelwoord &quot;SUV.&quot; | Eventuele niet-opgegeven negatieve trefwoorden die eerder met de sjabloon zijn gemaakt, worden verwijderd wanneer een feed-bestand via de sjabloon wordt doorgegeven. Niet-opgegeven negatieve trefwoorden die op andere manieren zijn gemaakt (zoals in normale bulksbladen, de [!UICONTROL Campaigns] -weergaven of in de ad-editor van het advertentienetwerk), blijven echter ongewijzigd. |
| De geplande einddatum voor de componenten van een gepost voederdossier komt voor. | nvt | De bestaande campagnes blijven ongewijzigd. De bestaande ad groepen, de advertenties, en de sleutelwoorden blijven zoals-is, worden gepauzeerd, of, volgens de [ montages van de voedergegevens ](feed-settings-manage.md#feed-data-settings) geschrapt. |
| Het voorraadniveau van een punt daalt onder een minimum dat in de [ montages van voedergegevens ](feed-settings-manage.md#feed-data-settings) wordt gespecificeerd. | Vorig dossier: stock=10 <br><br> Nieuw dossier: stock=0 | De bestaande campagnes blijven ongewijzigd. De bestaande ad groepen, de advertenties, de sleutelwoorden, en de productgroepen worden of gepauzeerd of geschrapt, volgens de [ montages van voedergegevens ](feed-settings-manage.md#feed-data-settings). |
| Het voorraadniveau van een punt gaat terug boven een minimum dat in de [ montages van voedergegevens ](feed-settings-manage.md#feed-data-settings) wordt gespecificeerd. | Vorig bestand: stock=0 <br><br> Nieuw bestand: stock=10 | Wanneer de bestaande advertenties, trefwoorden of productgroepen zijn gepauzeerd, worden ze opnieuw geactiveerd, zonder dat er geschiedenis of kwaliteitsscore verloren gaat. Als er geen advertenties, trefwoorden of productgroepen bestaan (bijvoorbeeld als deze eerder zijn verwijderd omdat het voorraadniveau onder het minimum lag), worden er nieuwe gemaakt. |

>[!MORELIKETHIS]
>
>* [ Ongeveer automatiserend en beheer gebruikend inventarisvoer ](inventory-feeds-about.md)
