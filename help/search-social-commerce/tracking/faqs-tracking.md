---
title: Veelgestelde vragen over bijhouden
description: Leer antwoorden op algemene vragen over het volgen, met inbegrip van het oplossen van problemenkwesties.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1191'
ht-degree: 0%

---

# Veelgestelde vragen over bijhouden

## Functies voor bijhouden

+++Kan ik campagnes bijhouden die Adobe Advertising niet beheert?

Ja. Als Zoeken, Sociaal, &amp; Handel één van uw rekeningen van het advertentienetwerk synchroniseert, dan volgt het de klikgegevens van het advertentienetwerk voor allen [ondersteunde typen campagne](/help/search-social-commerce/introduction/supported-inventory.md) op die rekening. De conversiegegevens worden ook bijgehouden als u de omleiding Zoeken, Sociale Zaken en Handel hebt toegevoegd aan uw doel-URL&#39;s voor advertenties en/of trefwoorden, of als u sjablonen hebt bijgehouden en conversie-tracking hebt geïmplementeerd op uw conversiepagina&#39;s. Verbeter met uw Adobe Account Team welke campagnes u Onderzoek, Sociale, &amp; Handel eenvoudig wilt volgen en die u hen wilt beheren.
+++

+++Hoe krijg ik multievent-attributie?

Voor adverteerders die tags voor Zoeken, Sociale &amp; Handel of Adobe Analytics-conversie gebruiken, biedt Adobe Advertising meerdere opties voor het toewijzen van conversiegegevens voor een reeks gebeurtenissen die tot conversie leiden. Met een instelling op advertentieniveau wordt bepaald hoe conversiegegevens over gebeurtenissen moeten worden verdeeld, zelfs wanneer deze via meerdere advertentiekanalen plaatsvinden, op voorwaarde dat de kanalen de indruk op gebeurtenisniveau kunnen bijhouden. Standaard worden conversies toegeschreven aan de laatste (meest recente) gebeurtenis, maar de instelling kan anders worden geconfigureerd, bijvoorbeeld om conversies aan de eerste gebeurtenis toe te schrijven of om alle gebeurtenissen gelijkmatig af te wegen. Als u de toewijzingsregel wijzigt, bepaalt dat hoe toekomstige biedingen worden berekend.

Adverteerders die alle conversiegegevens in een voederbestand verstrekken, moeten de conversie aan de gerelateerde transactiegebeurtenissen zelf toeschrijven.

>[!NOTE]
>
>In de meningen, rapporten en (beschikbaar aan sommige gebruikers) douanesimulaties van het campagnebeheer en van het portefeuillebeheer, kunt u de regel veranderen die wordt gebruikt om omzettingsgegevens binnen de meningen en rapportresultaten te attributen, zonder te beïnvloeden hoe toekomstige biedingen worden berekend.

+++

+++Hoe identificeren Adobe-advertenties dubbele transacties?

Er kunnen dubbele transacties plaatsvinden wanneer een gebruiker de bevestigingspagina vernieuwt nadat een transactie is voltooid. Voor reclame Adobe wordt gebruikgemaakt van de `ev_transid` attribuut om dubbele transacties met zelfde transactieID en bezitswaarde te elimineren.

De deduplicatielogica van Adobe Advertising:

* **Wanneer een client een waarde verzendt voor de `ev_transid` kenmerk:** Volgende pixelaanvragen worden beschouwd als duplicaten van de vorige als de volgende aanvragen hetzelfde zijn: de `ev_transid`; de volgende identiteitskaart voor het zelfde sleutelwoord, en, of plaatsing; en de waarde voor een specifieke transactieeigenschap.

   Bijvoorbeeld, als de veelvoudige leningstoepassingen zelfde toepassings identiteitskaart en leningsbedrag voor het zelfde sleutelwoord op een specifiek advertentienetwerk hebben, dan worden zij beschouwd als duplicaten, en slechts wordt de eerste leningstoepassing geteld.

* **Wanneer een client geen waarde verzendt voor de `ev_transid` kenmerk:** Opeenvolgende transacties worden beschouwd als duplicaten van de vorige als ze een tracking-id delen voor hetzelfde trefwoord, dezelfde advertentie of dezelfde plaatsing. en dezelfde waarde voor een specifieke transactieeigenschap.

   Als bijvoorbeeld meerdere leningaanvragen dezelfde trefwoordid en hetzelfde bedrag voor de lening hebben, worden ze als duplicaten beschouwd en wordt alleen de eerste leningaanvraag geteld.
+++

## Typen implementatie bijhouden

+++Ik wil stoppen met het gebruik van de service Adobe Advertising tracking voor een of meer campagnes of accounts. Hoe kan ik snel de volgende code uit volgende URLs verwijderen?

Neem eerst contact op met uw Adobe-accountteam om te begrijpen wat de gevolgen zijn van het verwijderen van URL&#39;s die u bijhoudt.

Wijzig in de account of campagne de methode voor bijhouden in &quot;[!UICONTROL No EF Redirect].&quot; Maak vervolgens een werkblad met de &quot;[!UICONTROL Generate Tracking URLs]&quot; en deze naar het advertentienetwerk verzenden. Alle bestaande URL&#39;s voor reeksspatiëring of doel-URL&#39;s worden vervangen.
+++

## Gegevensvragen

+++Hoe weet ik welke transactieeigenschap afkomstig is van een gegevensfeed of wordt bijgehouden door de tag voor het bijhouden van advertenties van Adobe?

In een [!UICONTROL Transaction Report], kunt u zien of een ingesloten transactieeigenschap is bijgehouden door de Adobe-pixel voor conversie van advertenties als u de aangepaste kolom &quot;[!UICONTROL Tracking URL].&quot; URL&#39;s bijhouden met de Adobe-pixel voor reclame bijhouden begint met `http://pixel.everesttech.net`.
+++

+++Wat zijn verweesde transacties?

Orphan-transacties zijn transactiegebeurtenissen die niet aan een specifiek trefwoord of een specifieke advertentie kunnen worden gekoppeld. Adobe Advertising kenmerkt transactie/opbrengst aan een trefwoord of advertentie door de ontvangen tracking-id&#39;s met de inkomstengebeurtenis te koppelen aan de unieke tracking-id in de URL van het trefwoord of de advertentie.

Wanneer een Adobe Account Team vermoedt dat verweesde transacties de oorzaak zijn van een daling van de inkomsten, controleert het team van de Zorg van de Klant op wezen en, als het er om het even welk vindt, onderzoekt de kwestie.

In de volgende situaties doen zich orfanen voor.

## Pixelimplementaties

Orphan-transacties komen bijna nooit voor bij pixelimplementaties. Er zijn echter pixelwezen opgetreden wanneer:

* De klikgegevens zijn niet beschikbaar voor de de klikdatum van omzetting. In dit geval worden de gegevens teruggekoppeld wanneer Search, Social &amp; Commerce de klikgegevens van het advertentienetwerk krijgt.

* De kliklogboeken worden niet verwerkt vóór de omzettingslogboeken.

## Implementaties van diervoeders

* De id voor bijhouden die in de feed is verzonden, is afkomstig van een account waarvan u niet op de hoogte bent van Zoeken, Sociale media en Handel.

* De account is niet gesynchroniseerd of er zijn fouten opgetreden tijdens het synchronisatieproces.

* De tracking-id is toegevoegd aan en verwijderd van het advertentienetwerk, terwijl Zoeken, Sociaal en Handel niet synchroon was met het advertentienetwerk. Zoekopdracht, sociale zaken en handel hebben dus geen informatie over de id. Deze kwestie blijft weesopbrengsten veroorzaken als er een vertraging is bij het ontvangen van inkomsten.

* De client heeft een id voor bijhouden verzonden die onjuist is opgemaakt in de feed en niet overeenkomt met de id voor bijhouden in de URL. Dit gebeurt gewoonlijk vanwege een opmaakprobleem of wanneer id&#39;s bijhouden in de feed worden afgekort.

* In het configuratiebestand is de reguliere expressie die wordt gebruikt om de volgende-id uit de URL&#39;s te extraheren, onjuist of verouderd. Soms wijzigt de adverteerder de tracking-id in de URL of past hij een geheel nieuw tracingsysteem toe. Hiervoor moet het implementatieteam Zoeken, Sociale Zaken en Handel de reguliere expressie bijwerken. In dergelijke gevallen is een groot deel van de inkomsten weeshuis.

## Implementaties doorvoeren met een transactie-id

Er zijn geen online transacties beschikbaar vóór de datums waarvoor gegevens beschikbaar zijn in de offlinefeed.

## Implementaties van feed met een token (ef_id)

Zoek, Sociaal, &amp; Handel kan geen overeenkomstige klik op zijn server of op het advertentienetwerk vinden. Dit kan zijn omdat de klikgegevens niet beschikbaar voor de de klikdatum van de omzetting of (zelden) zijn omdat de kliklogboeken niet vóór de omzettingslogboeken werden verwerkt. Wanneer de Onderzoek, Sociale, &amp; Handel de klikgegevens van het advertentienetwerk ontvangt of de kliklogboeken worden verwerkt, worden de gegevens in kaart gebracht aan de omzetting.
+++

## Problemen met het bijhouden van inkomsten

+++Hoe los ik oude/onjuiste gegevens van een voederdossier op?

Neem contact op met de klantenservice met het gecorrigeerde gegevensbestand.
+++

+++Meerdere trefwoorden hebben dezelfde URL voor reeksspatiëring.

**Implicaties**

Voor voederimplementaties met veelvoudige het volgen IDs, wordt het gegeven gemeld tegen veelvoudige sleutelwoorden. Voor andere implementaties, kunnen de omzettingen aan het verkeerde sleutelwoord worden toegeschreven omdat het systeem een omzetting willekeurig aan één van de sleutelwoorden toewijst.

**Mogelijke oorzaak**

De URL voor een nieuw trefwoord of een nieuwe advertentie is gekopieerd van een ander trefwoord of een andere advertentie.

Dit zou niet met vertoning of sociale advertenties moeten gebeuren.

**Mogelijke oplossing of oplossing**

* Als u uw eigen trefwoorden en advertenties beheert, maakt u een bulksheet-bestand met de juiste URL&#39;s voor de dubbele URL&#39;s en plaatst u dit op de juiste account via de **[!UICONTROL Generate Tracking URLs]** , waarmee URL&#39;s voor alle trefwoorden en advertenties opnieuw worden gegenereerd.

* Als een Adobe Account Team uw trefwoorden beheert, vraagt u hen om nieuwe URL&#39;s voor de dubbele URL&#39;s te maken.
+++
