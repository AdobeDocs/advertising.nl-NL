---
title: Overzicht van de implementatie van Adobe Advertising Creative
description: Leer over het basiswerkschema voor het uitvoeren van  [!DNL Creative].
feature: Creative Introduction
source-git-commit: fbd85ce99ab177c70b95bae42166265ef9053034
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 0%

---

# Overzicht van de implementatie van Adobe Advertising Creative

*Gesloten bèta*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

Het bewerkingsteam van [!DNL Creative] werkt met elke adverteerder aan het opzetten van zijn creatieve en creatieve ervaringen, ofwel het implementeren van de advertentie als advertenties binnen uw DSP, ofwel het voorzien van de advertentietags van derden om zichzelf te implementeren, en het valideren van de initiële kosten, klik en conversiegegevens.

Het Adobe-accountteam, het agententeam of de adverteerder (afhankelijk van de voorwaarden van de service level agreement) moeten voortdurend toezicht houden op elke ervaring en deze zo nodig bewerken om aan de doelstellingen van de adverteerder te voldoen.

## De eerste Taken van de Opstelling voor [!DNL Creative] Ervaringen

Het implementatieteam en/of uw bureau werken met u als volgt samen:

1. Bepaal uw verpersoonlijkingsdoelstellingen (zoals of u advertenties voor het prospecteren of het opnieuw richten zult personaliseren); alle eerste, tweede, en derdegegevens die, met inbegrip van creatieve activa en publiekssegmenten beschikbaar zijn; en uw strategie om uw doelstellingen te bereiken.<!-- and CRM data? used how/where? -->

1. (Nieuwe adverteerderaccounts) Administratieve accounts instellen:

   1. Stel de account van de adverteerder voor [!DNL Creative] in en maak ook een account in Advertising Search, Social &amp; Commerce.

      De accountinstellingen van [!DNL Creative] bevinden zich in Advertising DSP, zelfs als de adverteerder de rest van DSP niet gebruikt.

      Zelfs als de adverteerder geen [!DNL Search, Social, & Commerce] -klant is, wordt het [!DNL Search, Social, & Commerce] -account gebruikt om conversie-tags te maken en conversiekolommen in te stellen in [!DNL Creative] .

   1. (Indien nodig) Maak gebruikersaccounts zodat de adverteerder zijn creatieve en advertentieervaringen kan bekijken en beheren en rapporten kan genereren.

1. (Optioneel) Als u de doelsegmenten van de eerste partij wilt maken om deze als doelen voor uw creatieve projecten op te nemen, kunt u de labels op een van de volgende manieren maken:

   * [ creeer het opnieuw richten pixel ](/help/creative/pixels/retargeting-pixel-manage.md) om advertenties aan bezoekers met specifieke attributen aan specifieke het landen pagina&#39;s of omzettingspagina&#39;s opnieuw te richten, en dan markeringen te produceren om in de relevante Web-pagina&#39;s op te nemen.

   * (Advertisers met DSP) binnen DSP, [ creeer de segmenten van het douanepubliek ](/help/dsp/audiences/custom-segment-create.md) om alle bezoekers aan specifieke landende pagina&#39;s of omzettingspagina&#39;s te volgen, en dan markeringen te produceren om in de relevante Web-pagina&#39;s op te nemen.

   Beide typen labels zijn afbeeldingstags, die een transparante afbeelding (pixel) van 1 pixel x 1 pixel (onzichtbaar voor eindgebruikers) weergeven op de webpagina waarop ze worden toegevoegd. Later kunt u creatieve elementen in een advertentie configureren om specifieke doelgerichte pixels of segmenten te maken, zodat de relevante advertentie-elementen alleen worden weergegeven voor gebruikers die eerder sitepagina&#39;s hebben bezocht die zijn gekoppeld aan de pixel of het segment.

   De IT-afdeling of andere groep van de adverteerder moet mogelijk de implementatie van de tag plannen of hierover worden geïnformeerd.

   **Nota:** u kunt uw eerstepartijpubliek van Adobe Audience Manager en Adobe Analytics als creatieve doelstellingen ook gebruiken. Wanneer een bezoeker in aanmerking komt voor een publiek dat wordt gedeeld vanuit [!DNL Analytics] , kan de informatie binnen 24-48 uur in [!DNL Creative] worden uitgevoerd. <!--Are times still true? -->

1. De campagnehiërarchie van de opstelling binnen DSPs waarin u uw advertentieervaringen zult uitvoeren. Gebruik het richten dat met het richten in de advertentiervaringen compatibel is die u binnen de campagnes zult uitvoeren.

   Het gedrag voor hiërarchische activering kan per DSP variëren. Advertising DSP past een ad-level gerichte aanpak toe boven op (niet in plaats van) plaatsing-niveau gerichte doelframes. Bijvoorbeeld, als een plaatsing gebruikers in Australië richt en een advertentie gebruikers in Japan richt, dan zal de advertentie de &quot;Iedereen anders&quot;tak voor de ervaring richten. Zorg ervoor dat u door de volledige campagnestructuur denkt.

1. Stel uw advertenties in op basis van uw advertentiedoelstellingen:

   * **werkschema van de Automatisering:** het [!DNL Creative] verrichtingenteam kan dynamische advertenties voor uw organisatie tot stand brengen gebruikend advertentiesjablonen en gegevensvoer.

     Neem contact op met uw Adobe-accountteam voor meer informatie.

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. --><!-- I think this will be automatic based on their IMS organization. But I'm not sure if they need to be logged in via SSO using their Adobe login or if it will also work using their legacy DSP login. -->

   * **Handmatig werkschema:** manueel opstelling en ervaart:

      1. [ de standaardcreatieven van de opstelling in uw ervaringen ](/help/creative/creative-libraries/creative-add-standard.md) te gebruiken:

         * Upload deze naar Creative Cloud die [!DNL Creative] host. Dit kan afbeeldingselementen in een Adobe Experience Manager-account opnemen.

         * Voor creatieve bestanden die worden gehost op een ondersteunde externe advertentieserver, verwijst u naar de creatieve bestanden.

      1. (Facultatief) [ creatieve groepen in bundels ](/help/creative/creative-libraries/bundle-manage.md) die u aan gerichte ervaringen in één stap kunt vastmaken.

      1. Opstelling [ en ervaringen ](/help/creative/experiences/experience-about.md):

         * Voor [ gerichte en ervaringen ](/help/creative/experiences/experience-create-targeting.md), opeenvolgingscreatieven en facultatieve ad doelstellingen.

           Toevoegingsdoelen kunnen het opnieuw toewijzen van pixels omvatten die u maakt in [!DNL Creative] , publiekssegmenten in Adobe Experience Cloud (inclusief in DSP, Audience Manager of [!DNL Analytics] ), geografische doelen of specifieke gegevenstriggers op de webpagina (zoals SKU=01234567890123 of Cart=leeg).

         * Voor [ niet-gerichte en ervaringen ](/help/creative/experiences/experience-create-no-targeting.md), creeer algemene ervaringsmontages.

           Toevoegingsdoelen kunnen het opnieuw toewijzen van pixels omvatten die u maakt in [!DNL Creative] , publiekssegmenten in Adobe Experience Cloud (inclusief in DSP, Audience Manager of [!DNL Analytics] ), geografische doelen of specifieke gegevenstriggers op de webpagina (zoals SKU=01234567890123 of Cart=leeg).













1. Conversie bijhouden instellen voor advertenties:


Conversie bijhouden instellen. Afhankelijk van de implementatie kan dit het toevoegen van
conversietags naar de webpagina&#39;s van de adverteerder en/of het instellen van een dagelijkse
feed-drop voor conversiegegevens die de adverteerder afzonderlijk heeft verzameld.


U kunt tags voor het bijhouden van Adobe Advertising-conversies genereren via Zoeken, Sociaal en Commerce in Advertising of via Adobe Dynamic Tag Manager (voorheen Dynamic Tag Manager genoemd).
Opmerking: u moet JavaScript-conversietags gebruiken, niet afbeeldingstags.


De IT-afdeling of andere groep van de adverteerder moet mogelijk plannen of op de hoogte worden gebracht
ongeveer, de markering plaatsing.


(Optioneel) Breng in Zoeken, Sociaal en Commerce elke conversie aan (transactieeigenschap)
beschikbaar als een individuele kolomreeks in gegevensmeningen en rapporten.


Een conversie (transactie-eigenschap) wordt na op
Er is minstens één conversiegebeurtenis bijgehouden.


Als u geen specifieke metriek ter beschikking stelt, dan worden alle omzettingen geconsolideerd
in één kolomset &quot;Conversies&quot;.


Valideer de gegevens die worden bijgehouden.


(Optioneel) Stel levering van geplande rapporten in op opgegeven e-mailadressen.


Zie het Help-hoofdstuk over &quot;Rapporten&quot; voor instructies.


Stel advertentiecampagnes in op Advertising DSP of een andere DSP en verschaf JavaScript
of iframe-tags voor de advertentie die de adverteerder krijgt toegewezen, die deze kan implementeren als
advertenties van derden in de DSP.


Controleer de prestaties van uw voltooide advertentie-ervaringen, of het bekijken vooraf bepaald
prestatiegegevens voor individuele ervaringen of het maken van aangepaste prestatierapporten.


(Waar nodig) Werk en ervaringen bij op basis van prestaties en bijgewerkt overseinen.






>[!MORELIKETHIS]
>
>* [ Ongeveer Adobe Advertising Creative ](/help/creative/introduction/creative-about.md)
>* [ hoe het gebruikersinterface wordt georganiseerd ](/help/creative/introduction/ui.md)
