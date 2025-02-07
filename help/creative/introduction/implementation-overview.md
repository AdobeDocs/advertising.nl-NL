---
title: Overzicht van de uitvoering van de Adobe Advertising Creative
description: Leer over het basiswerkschema voor het uitvoeren van  [!DNL Creative].
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Overzicht van de uitvoering van de Adobe Advertising Creative

*Gesloten bèta*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

Het bewerkingsteam van [!DNL Creative] werkt met elke adverteerder aan opstelling zijn creatieve ervaringen en, of implementeert de advertentie als advertenties binnen uw DSP of verstrekt uw team van de markeringen van de derdeadvertentie om zich uit te voeren, en het bevestigen van de aanvankelijke kosten, klik, en omzettingsgegevens.

Het accountteam van de Adobe, het agententeam of de adverteerder (afhankelijk van de voorwaarden van de service level agreement) moeten voortdurend elke ervaring controleren en deze zo nodig bewerken om de doelstellingen van de adverteerder te halen.

## Eerste instellingstaken voor [!DNL Creative] campagnes <!-- Experiences? "Campaigns" may be confusing now. -->

Het implementatieteam en/of uw bureau werken met u als volgt samen:

1. Definieer uw verpersoonlijkingsdoelstellingen (zoals of u advertenties voor prospectie of het opnieuw richten zult personaliseren); alle eerste, tweede, en derdegegevens beschikbaar, met inbegrip van creatieve activa, publiekssegmenten, en de gegevens van CRM <!-- used how/where? -->; en uw strategie voor het bereiken van uw doelstellingen.

1. (Nieuwe adverteerderaccounts) Administratieve accounts instellen:

   1. Stel het account van de adverteerder in voor [!DNL Creative]<!-- and/or DSP? --> en maak ook een account in Advertising Search.

      De accountinstellingen van [!DNL Creative] bevinden zich in Advertising DSP, zelfs als de adverteerder geen DSP klant is.

      Zelfs als de adverteerder geen [!DNL Search] -klant is, wordt het [!DNL Search] -account gebruikt om conversie-tags te maken en conversiekolommen in te stellen in [!DNL Creative] .

   1. (Indien nodig) Maak gebruikersaccounts zodat de adverteerder zijn creatieve en advertentieervaringen kan bekijken en beheren en rapporten kan genereren.

1. (Optioneel) Als u de doelsegmenten van de eerste partij wilt maken om deze als doelen voor uw creatieve projecten op te nemen, kunt u de labels op een van de volgende manieren maken:

   * [ creeer het opnieuw richten pixel ](/help/creative/pixels/retargeting-pixel-manage.md) om advertenties aan bezoekers met specifieke attributen aan specifieke het landen pagina&#39;s of omzettingspagina&#39;s opnieuw te richten, en dan markeringen te produceren om in de relevante Web-pagina&#39;s op te nemen.

   * (Advertisers met DSP) binnen DSP, [ creeer de segmenten van het douanepubliek ](/help/dsp/audiences/custom-segment-create.md) om alle bezoekers aan specifieke het landen pagina&#39;s of omzettingspagina&#39;s te volgen, en dan markeringen te produceren om in de relevante Web-pagina&#39;s op te nemen.

   Beide typen labels zijn afbeeldingstags, die een transparante afbeelding (pixel) van 1 pixel x 1 pixel (onzichtbaar voor eindgebruikers) weergeven op de webpagina waarop ze worden toegevoegd. Later kunt u creatieve elementen in een advertentie configureren om specifieke doelgerichte pixels of segmenten te maken, zodat de relevante advertentie-elementen alleen worden weergegeven voor gebruikers die eerder sitepagina&#39;s hebben bezocht die zijn gekoppeld aan de pixel of het segment.

   De IT-afdeling of andere groep van de adverteerder moet mogelijk de implementatie van de tag plannen of hierover worden geïnformeerd.

   **Nota:** u kunt uw eerstepartijpubliek van Adobe Audience Manager en Adobe Analytics als creatieve doelstellingen ook gebruiken. Wanneer een bezoeker in aanmerking komt voor een publiek dat wordt gedeeld vanuit [!DNL Analytics] , kan de informatie binnen 24-48 uur in [!DNL Creative] worden uitgevoerd. <!--Still true? And what about AAM and DSP? -->

1. Stel uw advertenties in op basis van uw advertentiedoelstellingen:

   * **werkschema van de Automatisering:** het [!DNL Creative] verrichtingenteam kan dynamische advertenties voor uw organisatie tot stand brengen gebruikend advertentiesjablonen en gegevensvoer.

     Neem voor meer informatie contact op met het accountteam van de Adobe.

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. -->

   * **Handmatig werkschema:** manueel opstelling en ervaart:

      1. Creatieve instellingen instellen voor gebruik in uw ervaringen:

         * Voor creatieve personen die door [!DNL Creative] worden gehost, uploadt u deze. <!-- Add x-ref and reword if necessary to cover all cases -->

         * Voor creatieve die creatieve die op een gesteunde derde en server wordt ontvangen, [ richt aan de creatieve dossiers ](/help/creative/creative-libraries/creative-third-party-manage.md).

      1. (Facultatief) [ creatieve groepen in bundels ](/help/creative/creative-libraries/bundle-manage.md) die u aan ervaringen in één stap kunt vastmaken.

      1. De schepselen van de opeenvolging en facultatieve ad doelstellingen als [ en ervaringen ](/help/creative/experiences/experience-about.md).<!-- maybe change x-ref once that chapter is done -->

     Toevoegingsdoelen kunnen het opnieuw toewijzen van pixels omvatten die u in [!DNL Creative] maakt, publiekssegmenten in Adobe Experience Cloud (inclusief in DSP, Audience Manager of [!DNL Analytics]), geografische doelen of specifieke gegevenstriggers op de webpagina (zoals SKU=01234567890123 of Cart=leeg).&lt;!— Ik zie publiekssegmenten niet beschikbaar, en ik zie straaldoelen (wat niet werkt) maar geen andere geo-doelen — controleer al deze. —>

1. Conversie bijhouden instellen voor advertenties:


Conversie bijhouden instellen. Afhankelijk van de implementatie kan dit het toevoegen van
conversietags naar de webpagina&#39;s van de adverteerder en/of het instellen van een dagelijkse
feed-drop voor conversiegegevens die de adverteerder afzonderlijk heeft verzameld.


U kunt tags voor het bijhouden van Advertising Cloud-conversies genereren in Advertising Cloud
Zoeken of in Dynamic Tag Manager voor Adobe (voorheen Dynamisch tagbeheer).
Opmerking: u moet JavaScript-conversietags gebruiken, niet afbeeldingstags.


De IT-afdeling of andere groep van de adverteerder moet mogelijk plannen of op de hoogte worden gebracht
ongeveer, de markering plaatsing.


(Optioneel) Breng in Advertising Cloud Search elke conversie aan (transactieeigenschap)
beschikbaar als een individuele kolomreeks in gegevensmeningen en rapporten.


Een conversie (transactie-eigenschap) wordt in Advertising Cloud Search weergegeven na op
Er is minstens één conversiegebeurtenis bijgehouden.


Als u geen specifieke metriek ter beschikking stelt, dan worden alle omzettingen geconsolideerd
in één kolomset &quot;Conversies&quot;.


Valideer de gegevens die worden bijgehouden.


(Optioneel) Stel levering van geplande rapporten in op opgegeven e-mailadressen.


Zie het Help-hoofdstuk over &quot;Rapporten&quot; voor instructies.


Stel advertentiecampagnes in op Advertising Cloud DSP of een andere DSP en verstrek JavaScript
of iframe-tags voor de advertentie die de adverteerder krijgt toegewezen, die deze kan implementeren als
advertenties van derden in de DSP.


Controleer de prestaties van uw voltooide advertentie-ervaringen, of het bekijken vooraf bepaald
prestatiegegevens voor individuele ervaringen of het maken van aangepaste prestatierapporten.


(Waar nodig) Werk en ervaringen bij op basis van prestaties en bijgewerkt overseinen.






>[!MORELIKETHIS]
>
>* [ Ongeveer Adobe Advertising Creative ](/help/creative/introduction/creative-about.md)
>* [ hoe het gebruikersinterface wordt georganiseerd ](/help/creative/introduction/ui.md)
