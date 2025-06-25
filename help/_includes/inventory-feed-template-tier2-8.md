---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---
# Niveau 2 - Niveau 8 velden in winkelen en sjablonen

**[!UICONTROL Tier  2 - Tier 8]:** (Wanneer u rijen van productgroepen toevoegt) een type van productattribuut waardoor om producten, en de kwalificerende criteria voor het geselecteerde attribuuttype (bijvoorbeeld, merk=Acme of Voorwaarde=Nieuw) te richten. De waarden worden hiërarchisch toegepast om de in aanmerking komende producten te bepalen. Selecteer een kenmerktype en voer de kwalificatiecriteria in. Verboden tekens zijn onder andere: `[ ] < > >>` (twee opeenvolgende &#39;groter dan&#39;-tekens), die worden gebruikt om kolomnamen in de sjabloon, wijzigingnamen in de sjabloon en lijnscheidingstekens in de kolom [!UICONTROL Parent Product Grouping] in de bulksbladen aan te duiden.

U kunt tot acht niveaus (niveaus) van productgroepen, met inbegrip van &quot;[!UICONTROL All Products]&quot;omvatten (Rij 1). Elke laag kan meerdere productgroepen bevatten, maar ze moeten hetzelfde kenmerktype hebben (zoals &quot;Voorwaarde&quot;).

>[!NOTE]
>
>* ([!DNL Google Ads] slechts) de mogelijke waarden voor [!UICONTROL Channel] zijn &quot;[!UICONTROL Local]&quot; of &quot;[!UICONTROL Online],&quot;en de mogelijke waarden voor [!UICONTROL ChannelExclusivity] zijn &quot;[!UICONTROL SingleChannel]&quot; en &quot;[!UICONTROL MultiChannel]&quot;.
>* Wanneer u op het tabblad [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] in de weergave een tweede niveau (onderliggende) productgroep voor een advertentiegroep maakt, wordt automatisch een andere productgroep met de naam &quot;[!UICONTROL Everything Else]&quot; gemaakt met het standaardbod en het standaardbod voor een groep. [!UICONTROL Product Groups] Het gebruiken van de malplaatjes van de voorraadvoer, echter, &quot;[!UICONTROL Everything Else]&quot;productgroepen zijn uitgesloten.
>* Als u meerdere lagen opneemt en er geen waarde beschikbaar is voor de uiteindelijke (hoogste) laag, wordt de op één na hoogste laag gebruikt als de productgroep die kan worden geboden. Als u bijvoorbeeld vijf lagen opneemt en er geen waarde beschikbaar is voor Tier 5, wordt Tier 4 gebruikt als de te bieden productgroep (eenheid). Als er echter geen waarde beschikbaar is voor een middelste laag, wordt de rij genegeerd. Bijvoorbeeld, als u vijf lagen omvat, en Reeks 5 heeft een waarde maar Reeks 4 niet, dan wordt Rij 4 genegeerd.
