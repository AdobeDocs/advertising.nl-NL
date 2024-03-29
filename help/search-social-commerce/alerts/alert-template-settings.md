---
title: Aangepaste sjablooninstellingen voor waarschuwingen
description: Meer informatie over de instellingen voor aangepaste waarschuwingssjablonen.
exl-id: 5ba98f48-c396-4b20-91dc-d45164097f9c
feature: Search Alerts
source-git-commit: f21283731d7a1830af585cec43805c54c81c72ff
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# Aangepaste sjablooninstellingen voor waarschuwingen

| Tab | Parameter | Beschrijving |
|--- |--- |--- |
| [!UICONTROL Date Range] | [!UICONTROL Date] | Het datumbereik waarvoor de voorwaarden voor de signalering moeten worden geëvalueerd. Metriek worden geaggregeerd over het datumbereik geëvalueerd. De opties variëren van *[!UICONTROL Yesterday]* tot *[!UICONTROL Last 180 Days]*. |
| [!UICONTROL Filters] |  | De voorwaarden voor het in werking stellen van de signalering op het in de [!UICONTROL Scheduling and Delivery] tab. De beschikbare kolommen variëren per eenheidstype (zoals campagne of sleutelwoord). Alle filters worden verbonden gebruikend de functie VAN Boolean EN, wat betekent dat aan alle gespecificeerde voorwaarden moet worden voldaan.<ul><li><p>Klik op ![Pijl-omlaag](/help/search-social-commerce/assets/arrow-down-expand.png "Pijl-omlaag") naast ![Toevoegen](/help/search-social-commerce/assets/add.png "Toevoegen") **[!UICONTROL ADD FILTER]** en voer vervolgens de volgende handelingen uit:</p></li><ol><li><p>(Optioneel) Als u de kolomnamen wilt filteren op een tekenreeks, voert u de zoektekenreeks in het dialoogvenster **[!UICONTROL ADD FILTER]** invoerveld.</p></li><li><p>Selecteer een kolomnaam in het kolommenu.</p></li><li><p>Definieer het filter op de kolom:</p></li><ul><li><p>(Filters zonder invoervelden) Klik op ![Pijl-omlaag](/help/search-social-commerce/assets/arrow-down-expand.png "Pijl-omlaag") naast het tweede menu en selecteer vervolgens de selectievakjes naast elke waarde die u wilt opnemen.</p></li><li><p>(Metrische kolommen waarvoor u waardeverhogingen of -verlagingen tussen het opgegeven datumbereik en de vorige periode wilt bijhouden) Selecteer voor de operator *verhogingen door* of *vermindert met* en voer vervolgens de drempelwaarde in.</p><p>Als u bijvoorbeeld &quot;[!UICONTROL Cost]&quot; kolom en wilt worden gewaarschuwd wanneer de kosten van een campagne met 21% stijgen, en selecteer vervolgens &quot;[!UICONTROL increases by]&quot; en voer in het invoerveld 21 in. In de [!UICONTROL Date Comparison Format] geeft aan dat u geïnteresseerd bent in een wijziging in percentage (in plaats van een wijziging in valuta-eenheden).</p><p>Wanneer u deze optie selecteert, worden er twee extra kolommen toegevoegd voor elke gewone gegevenskolom. Bijvoorbeeld, in plaats van het omvatten van enkel één kolom voor &quot;Kliks,&quot;omvat het rapport kolommen voor &quot;Klik R1&quot;(voor Waaier 1) &quot;klikt R2&quot;(voor Waaier 2), en of &quot;klikt Diff&quot;of &quot;kliktDiff (%),&quot;afhankelijk van gespecificeerde [!UICONTROL Date Comparison Format] (zie hieronder).</p><p>**Opmerkingen:**</p><ul><li><p>De verschilkolom wordt niet bevolkt voor afgeleide metriek.<p></li><li><p>Deze eigenschap is niet beschikbaar voor metrische omzetting, identiteitskaart, of kolommen van de etiketclassificatie.</p></li><li><p>Rapporten die grote datumbereiken vergelijken, kunnen langer duren om te genereren.</p></li></ul></ul><li><p>(Alle andere filters met invoervelden) Selecteer een operator in het tweede menu en voer vervolgens de toepasselijke waarde in.</p><p>Als u bijvoorbeeld de kolom &quot;Klikken&quot; hebt geselecteerd en alleen rijen met meer dan 100 klikken wilt retourneren, selecteert u &quot;Groter dan&quot; en voert u 100 in het invoerveld in.</p><p>Afhankelijk van het gegevenstype kunnen de beschikbare operatoren <i>groter dan</i>, <i>minder dan</i>, <i>equals</i>, <i>contains</i>, <i>bevat niet</i>, <i>begint met</i>, <i>eindigt met</i>, <i>geen waarde</i>, <i>has value</i>, <i>voor</i>, <i>na</i>, of <i>geen datum</i>.</p><p>**Opmerking:** Tekstwaarden zijn niet hoofdlettergevoelig. Als u bijvoorbeeld filtert door campagnes met &quot;lening&quot; in de naam, kunnen de resultaten &quot;Consumentenleningen&quot; en &quot;kredietaanvragen&quot; omvatten.</p></li></ol><li><p>Klik op ![Verwijderen](/help/search-social-commerce/assets/delete.png "Verwijderen") naast de filterdefinitie.</p></li></ul> |
|  | [!UICONTROL Comparing] | (Beschikbaar wanneer de waakzame sporen in één of meerdere metrische kolommen stijgen of verminderen; read-only) De twee datumwaaiers waarvoor de gegevens worden vergeleken. |
|  | [!UICONTROL Date Comparison Format] | (Beschikbaar wanneer de waakzame sporen in één of meerdere metrische kolommen stijgt of vermindert) hoe te om het verschil tussen gegevens in de twee datumwaaiers uit te drukken:<ul><li><p><i>[!UICONTROL Variance]</i> (standaard) — Geeft het verschil weer als een numerieke waarde.</p></li><li><p><i>[!UICONTROL % Change]</i> — Geeft het verschil weer als een percentage.</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Name] | De naam van de waarschuwing. Het moet ten minste vijf tekens bevatten. |
|  | [!UICONTROL Trigger this Alert] [wanneer] | Hoe vaak controleert de waarschuwing op de gespecificeerde voorwaardelefilters en, wanneer aan alle voorwaarden wordt voldaan, verzendt e-mailberichten:<ul><li><p>[!UICONTROL Daily at <*NN*> [AM|PM]]</p></li><li><p>[!UICONTROL Weekly on <*Day of Week*> at <*NN*> [AM|PM]]</p></li><li><p>[!UICONTROL Every month on <*Day NN*> at <*NN*> [AM|PM]]</p></li></ul>**Opmerking:** Deze waarde heeft geen invloed op de evaluatieperiode. |
|  | [!UICONTROL Email Recipients] | (Alleen bewerkbaar door de maker van de waarschuwingssjabloon; alleen-lezen voor alle anderen) E-mailadressen waar berichten moeten worden verzonden wanneer een waarschuwing wordt gegenereerd. Standaard wordt het adres van de sjabloonmaker ingevoerd.<br><br>Om een adres toe te voegen, ga het adres in, en klik dan **[!UICONTROL Add]**. Als u meerdere adressen wilt opgeven, scheidt u deze met komma&#39;s of spaties of voegt u ze afzonderlijk toe.<br><br>Als de waarschuwing maximaal 1000 records bevat, wordt een CSV-versie van de waarschuwing aan het e-mailbericht toegevoegd. |

>[!MORELIKETHIS]
>
>* [Aangepaste waarschuwingen](alert-about.md)
>* [Een aangepaste waarschuwingssjabloon maken](alert-template-create.md)
>* [Een aangepaste waarschuwingssjabloon bewerken](alert-template-edit.md)
>* [Een aangepaste waarschuwingssjabloon onderbreken](alert-template-pause.md)
>* [Een aangepaste waarschuwingssjabloon activeren](alert-template-activate.md)
>* [Een aangepaste waarschuwingssjabloon verwijderen](alert-template-delete.md)
>* [Aangepaste waarschuwingen weergeven](alert-view.md)
>* [Gegevens exporteren voor aangepaste waarschuwingen](alert-export-data.md)
