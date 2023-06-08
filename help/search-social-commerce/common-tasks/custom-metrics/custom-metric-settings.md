---
title: Aangepaste metrische instellingen
description: Verwijs naar de montages voor douanemetriek, die van standaardmetriek worden berekend.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 0%

---

# Aangepaste metrische instellingen

Aangepaste metrische instellingen verschillen enigszins in verschillende delen van de interface.

## Aangepaste metrische instellingen in weergaven voor campagnebeheer

| Parameter/Sectie | Beschrijving |
|----|----|
| Aangepaste metrische naam | De naam van metrisch, die als kolomnaam verschijnt. <b>Tip:</b> Gebruik een betekenisvolle metrische naam, maar houd er rekening mee dat langere namen de kolom breder maken. |
| Metrisch invoegen | De wiskundige formule die wordt gebruikt om de nieuwe metrische waarde te berekenen (zoals [Kosten]/[Registraties]:<ul><li>Om metrisch van de lijst van verkeer en opbrengstmetriek op te nemen, plaats uw curseur waar u metrisch wilt opnemen, en dan of metrisch van de lijst selecteren of het manueel ingaan en ingesloten tussen haakjes (bijvoorbeeld, `[CPC]`).</li><li>Als u een operator wilt invoegen, plaatst u de cursor op de plaats waar u de operator wilt invoegen en klikt u op de knop of voert u het symbool handmatig in. De beschikbare wiskundige operatoren: `+ - * / ( ) ()`</li></ul><b>Opmerking:</b> Complexe aangepaste metriek duurt langer om te berekenen en rapporten en weergaven die ze bevatten, vooral wanneer ze aparte kolommen voor doorklikken en doorkijkconversies bevatten, duurt het langer om te genereren. |
| Indeling | Hoe te om de gegevens voor dit metrisch voor te stellen: *[!UICONTROL Currency]* (een monetaire waarde), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]*, of *[!UICONTROL Percentage]* (een percentage met twee decimalen).<br><br><b>Let op:</b> Als u een afgeleide metrische waarde met het formaat creeert [!UICONTROL Number w/out Decimal Points] (waarin gegevens als gehele getallen worden weergegeven) en deze opnemen in een weergave of rapport waarin een gewogen toewijzingsregel voor conversie wordt gebruikt ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], of [!UICONTROL Even Distribution]), wordt de uitvoer weergegeven in gehele getallen, niet in decimalen. Dit betekent dat afzonderlijke gegevensvelden mogelijk onjuist zijn, ook al zijn de totalen juist. Als een volgorde bijvoorbeeld gelijk is verdeeld tussen drie gebeurtenissen, wordt één volgorde (in plaats van 0,33 volgorde) toegewezen aan elk van de drie gebeurtenissen. Om de kwestie te verhinderen, gebruik metrisch formaat [!UICONTROL Number to 2 Decimal Points]. |

## De metrische montages van de douane in rapporten en rapportmalplaatjes en in [!UICONTROL Portfolios] views

| Parameter/Sectie | Beschrijving |
|----|----|
| Aangepaste metrische naam | De naam van metrisch, die als kolomnaam verschijnt. <b>Tip:</b> Gebruik een betekenisvolle metrische naam, maar houd er rekening mee dat langere namen de kolom breder maken. |
| Indeling | Hoe te om de gegevens voor dit metrisch voor te stellen: *[!UICONTROL Currency]* (een monetaire waarde), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]*, of *[!UICONTROL Percentage]* (een percentage met twee decimalen).<br><br><b>Let op:</b> Als u een afgeleide metrische waarde met het formaat creeert [!UICONTROL Number w/out Decimal Points] (waarin gegevens als gehele getallen worden weergegeven) en deze opnemen in een weergave of rapport waarin een gewogen toewijzingsregel voor conversie wordt gebruikt ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], of [!UICONTROL Even Distribution]), wordt de uitvoer weergegeven in gehele getallen, niet in decimalen. Dit betekent dat afzonderlijke gegevensvelden mogelijk onjuist zijn, ook al zijn de totalen juist. Als een volgorde bijvoorbeeld gelijk is verdeeld tussen drie gebeurtenissen, wordt één volgorde (in plaats van 0,33 volgorde) toegewezen aan elk van de drie gebeurtenissen. Om de kwestie te verhinderen, gebruik metrisch formaat [!UICONTROL Number to 2 Decimal Points]. |
| Metrisch invoegen | Een lijst van bestaande metriek waarvan u een formule kunt tot stand brengen.<br><br>Als u metrisch wilt invoegen in het veld voor de invoer van de formule, plaatst u de cursor op de plaats waar u de metrische waarde wilt invoegen en selecteert u de metrische waarde in de lijst of voert u deze handmatig in en tussen haakjes (bijvoorbeeld `[CPC]`). |
| Operator invoegen | De beschikbare wiskundige operatoren: `+ - x / ( )`<br><br>Als u een operator wilt invoegen in het invoerveld voor de formule, plaatst u de cursor op de plaats waar u de operator wilt invoegen en klikt u op de knop of voert u het symbool handmatig in. |
| [Formule-invoerveld voor de metrische waarde] | De wiskundige formule die wordt gebruikt om nieuwe metrisch te berekenen die op één of meerdere bestaande eigenschappen of standaardmetriek wordt gebaseerd (zoals `[Cost]/[Registrations]`. Het kan elke combinatie van metriek en operatoren bevatten.<br><br><b>Opmerking:</b> Complexe aangepaste metriek duurt langer om te berekenen en rapporten en weergaven die ze bevatten, vooral wanneer ze aparte kolommen voor doorklikken en doorkijkconversies bevatten, duurt het langer om te genereren. |

>[!MORELIKETHIS]
>
>* [Informatie over aangepaste metriek](custom-metric-about.md)
>* [Een aangepaste metrische waarde maken](custom-metric-create.md)
>* [Een aangepaste metrische waarde bewerken](custom-metric-edit.md)
>* [Een aangepaste metrische waarde verwijderen](custom-metric-delete.md)

