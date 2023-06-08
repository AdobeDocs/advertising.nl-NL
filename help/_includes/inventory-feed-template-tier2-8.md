---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---
# Niveau 2 - Niveau 8 velden in winkelen en sjablonen

**[!UICONTROL Tier  2 - Tier 8]:** (Wanneer u lagen van productgroepen toevoegt) Een type van productattribuut waardoor om producten, en de kwalificerende criteria voor het geselecteerde attributentype (bijvoorbeeld, Brand=Acme of Condition=New) te richten. De waarden worden hiërarchisch toegepast om de in aanmerking komende producten te bepalen. Selecteer een kenmerktype en voer de kwalificatiecriteria in. De volgende tekens zijn niet toegestaan: `[ ] < > >>` (twee opeenvolgende &#39;groter dan&#39;-tekens), die worden gebruikt om kolomnamen in de sjabloon aan te wijzen, wijzigingsnamen in de sjabloon en lijnscheidingstekens in de sjabloon [!UICONTROL Parent Product Grouping] kolom in bulksbladen.

U kunt maximaal acht niveaus (niveaus) van productgroepen opnemen, waaronder &quot;[!UICONTROL All Products]&quot; (Tier 1). Elke laag kan meerdere productgroepen bevatten, maar ze moeten hetzelfde kenmerktype hebben (zoals &quot;Voorwaarde&quot;).

>[!NOTE]
>
>* ([!DNL Google Ads] Alleen) De mogelijke waarden voor [!UICONTROL Channel] zijn &quot;[!UICONTROL Local]&quot; of &quot;[!UICONTROL Online],&quot; en de mogelijke waarden voor [!UICONTROL ChannelExclusivity] zijn &quot;[!UICONTROL SingleChannel]&quot; en &quot;[!UICONTROL MultiChannel].&quot;
>* Wanneer u een tweede niveau (onderliggende) productgroep voor een advertentiegroep maakt vanuit de [!UICONTROL Product Groups] in de [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] bekijken, een andere productgroep genoemd &quot;[!UICONTROL Everything Else],&quot; wordt automatisch gemaakt op basis van het standaardbod voor advertenties. Het gebruiken van voorraadvoedermalplaatjes, echter, &quot;[!UICONTROL Everything Else]&quot; productgroepen zijn uitgesloten.
>* Als u meerdere lagen opneemt en er geen waarde beschikbaar is voor de uiteindelijke (hoogste) laag, wordt de op één na hoogste laag gebruikt als de productgroep die kan worden geboden. Als u bijvoorbeeld vijf lagen opneemt en er geen waarde beschikbaar is voor Tier 5, wordt Tier 4 gebruikt als de te bieden productgroep (eenheid). Als er echter geen waarde beschikbaar is voor een middelste laag, wordt de rij genegeerd. Bijvoorbeeld, als u vijf lagen omvat, en Reeks 5 heeft een waarde maar Reeks 4 niet, dan wordt Rij 4 genegeerd.

