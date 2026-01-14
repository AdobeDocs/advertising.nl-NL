---
title: Hoe DSP uw campagnes optimaliseert
description: Leer hoe DSP de pakketten optimaliseert in uw campagnes.
feature: DSP Optimization
exl-id: 92d411cf-4307-4449-97b4-da3817f2a0b4
source-git-commit: de2a2a097802cc4a7b5ac63bee2eb326895e70f1
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 0%

---

# Hoe Advertising DSP uw campagnes optimaliseert

Deze pagina beschrijft hoe de DSP optimization engine, die wordt aangedreven door [!DNL Adobe AI], de pakketten in uw campagnes optimaliseert. Neem voor tips en trucs voor het handmatig optimaliseren van uw campagnes contact op met uw Adobe-accountteam. <!-- add link to trading playbook if we add it to help -->

De optimalisatiedoelstellingen van het pakket werken op twee niveaus:

* Voor elk pakket: DSP wijst budget toe aan elke plaatsing binnen het pakket op basis van de prestaties van de plaatsing ten opzichte van de geselecteerde PKI.

* Voor elke plaatsing/veiling in het pakket: DSP berekent de real-time economische PKI-waarde voor elke veiling per plaatsing en gebruikt deze waarde vervolgens om het bod te bepalen.

  >[!NOTE]
  >
  >De economische waarde kan zwaar worden gewogen op basis van hoe goed een plaatsing uitgaven. Als een plaatsing achter zijn uitgavendoel ligt, dan is het toegestaan veilingen van lagere kwaliteit te kopen. Als een plaatsing gemakkelijk zijn uitgavendoel bereikt, dan verschuift de nadruk naar hogere kwaliteit veilingen.

## Pakketoptimalisatie

DSP kan uw levering op twee fundamentele manieren optimaliseren, waarbij 20 variaties beschikbaar zijn om u aan te passen aan uw specifieke prestatiedoel. U kunt kiezen:

* Prioriteit geven aan de prestatiessnelheid

* Prioriteit geven aan kostenefficiëntie voor balancering met prestatiesnelheid

Zie [ Doelstellingen van de Optimalisering en hoe te om hen ](optimization-goals.md) te gebruiken om te bepalen welk optimalisatiedoel u kunt helpen uw KPI(s) bereiken.

### Pakketten die de Tarief van Prestaties voorrang geven

Voor optimalisatiedoelen die voorrang geven aan de prestatiesnelheid, voorspelt DSP de prestaties van elke veiling en biedt altijd een bod uit op Maximumbod. Voorbeelden van toepasselijke optimalisatiedoelen zijn [!UICONTROL Highest Viewability Rate] , [!UICONTROL Highest Clickthrough Rate] , enzovoort.

Deze optimalisatiemodus werkt goed als:

* U kent al het effectieve/acceptabele CPM-niveau (bijvoorbeeld een historische benchmark).

* U bent bereid om [!UICONTROL Max Bid] voor elke plaatsing manueel aan te passen als u uitdagingen met het schrapen ervaart.

* U geeft prioriteit aan schaal boven efficiëntie.

#### Logica voor spatiëring {#pacing-logic-performance}

* Als de uitgaven op tijd zijn, wordt het bieden selectiever, zodat je alleen op veilingen biedt die hoge prestatietarieven zullen hebben.

* Als de bestedingen achterblijven, wordt het bieden minder selectief, zodat je op veilingen biedt waarvan wordt verwacht dat ze lagere prestatietarieven zullen hebben om de pakketdoelstelling te halen.

#### Prijs/biedarcering wissen {#clearing-price-performance}

Nadat DSP de prijsbepalingslogica heeft uitgevoerd, voert het voorgestelde bod uit via een prijsvoorspellingsmodel voor clearing. Als de voorspelling aangeeft dat het bod kan worden verlaagd met een minimale verlaging van de win-rente, wordt het bod verlaagd volgens de voorspelling.

### Pakketten die prioriteit geven aan het in evenwicht brengen van kostenefficiëntie met prestatiesnelheid

Voor sommige optimalisatiedoelstellingen voorspelt DSP de prestaties van elke veiling en past het de biedprijzen automatisch aan, nooit hoger dan de plaatsingskosten [!UICONTROL Max Bid]. Voorbeelden van toepasselijke optimalisatiedoelen zijn [!UICONTROL Lowest CPM] , [!UICONTROL Lowest CPA] , [!UICONTROL Lowest Cost per View] , [!UICONTROL Lowest Cost per Click] , enzovoort.

#### Pacing Logic {#pacing-logic-balanced}

* Als de bestedingen in een tempo verlopen, wordt DSP prijsgevoeliger en biedt het land lagere bedragen aan om de win-winrente te verhandelen met behulp van het pacing plan.

* Als een prestatiemetrisch ook (alle doelstellingen behalve [!UICONTROL Lowest CPM]) in evenwicht wordt gebracht, dan overvloeit voorspelde KPI in het bedrag dat wordt geboden. Je biedt dus een hogere biedprijs voor veilingen waarvan wordt verwacht dat ze beter presteren op basis van de kosten per.

* Als de uitgaven achter het tempo liggen, wordt DSP minder prijsgevoelig en biedt het hogere bedragen, tot aan de [!UICONTROL Max Bid] , om de win rate af te zetten met het pacing plan.

#### Prijs/biedarcering wissen {#clearing-price-balanced}

Nadat DSP de prijsbepalingslogica heeft uitgevoerd, voert het voorgestelde bod uit via een prijsvoorspellingsmodel voor clearing. Als de voorspelling aangeeft dat het bod kan worden verlaagd met een minimale verlaging van de win-rente, wordt het bod verlaagd volgens de voorspelling.

## Plaatsing optimaliseren

Plaatsingsfilters voor voorbiedingen zijn de strengste manier om goede prestaties te garanderen. DSP gebruikt voorbiedingsfilters strategisch voor verschillende advertentietypen om prestatiedoelen te bereiken voor verschillende plaatsen binnen elk pakket. U kunt voorbiedingsfilters tegelijk met optimalisatie op pakketniveau of onafhankelijk gebruiken.

>[!NOTE]
>
>De beschikbare filters voor voorbiedingen variëren per advertentietype. Voor een standaardplaatsing van het beeldscherm kunt u bijvoorbeeld filteren op doorklikfrequentie en gezichtsvermogen, maar niet op voltooiingsfrequentie.

Zie [ plaatsing-vlakke pre-Bodende Filters en hoe te om hen ](optimization-pre-bid-filters.md) te gebruiken om te bepalen welke pre-biederfilter u kan helpen uw KPI(s) bereiken.

>[!MORELIKETHIS]
>
>* [ de Montages van het Pakket ](/help/dsp/campaign-management/packages/package-settings.md)
>* [ Montages van de Plaatsing ](/help/dsp/campaign-management/placements/placement-settings.md)
>* [ Doelstellingen van de optimalisering en hoe te om hen te gebruiken ](optimization-goals.md)
>* [ plaatsing-vlakke pre-Bodende Filters en hoe te om hen te gebruiken ](optimization-pre-bid-filters.md)
>* [ Prestaties van het oplossen van problemen ](/help/dsp/optimization/troubleshooting-performance.md)
