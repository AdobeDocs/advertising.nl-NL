---
title: Aangepaste metrische instellingen
description: Verwijs naar de montages voor douanemetriek, die van standaardmetriek worden berekend.
exl-id: b9e8434d-5ea2-47cd-9d63-705a6337c34c
feature: Search Common Tasks, Search Custom Metrics
source-git-commit: a89a6513dfe468b98513b2d47c086a3107e63d47
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# Aangepaste metrische instellingen

Aangepaste metrische instellingen verschillen enigszins in verschillende delen van de interface.

## Aangepaste metrische instellingen in de meeste beheerweergaven

| Parameter/Sectie | Beschrijving |
|----|----|
| Aangepaste metrische naam | De naam van metrisch, die als kolomnaam verschijnt. <b> Uiteinde:</b> gebruik een betekenisvolle metrische naam, maar ben van mening dat de langere namen de kolom breder maken. |
| Metrisch invoegen | De wiskundige formule die wordt gebruikt om nieuwe metrisch (zoals [ Kosten ] te berekenen/ [ Registraties ]:<ul><li>Om metrisch van de lijst van verkeer en opbrengstmetriek op te nemen, plaats uw curseur waar u metrisch wilt opnemen, en dan of metrisch van de lijst selecteren of het manueel en ingesloten tussen haakjes ingaan (bijvoorbeeld, `[CPC]`).</li><li>Als u een operator wilt invoegen, plaatst u de cursor op de plaats waar u de operator wilt invoegen en klikt u op de knop of voert u het symbool handmatig in. De beschikbare wiskundige operatoren: `+ - * / ( ) ()`</li></ul><b> Nota:</b> De complexe douanemetriek neemt langer om te berekenen, en rapporten en meningen die hen omvatten — vooral wanneer zij afzonderlijke kolommen voor klik-door en mening-door omzettingen omvatten — duurt langer om te produceren. |
| Indeling | De gegevens voor deze metrische waarde weergeven: *[!UICONTROL Currency]* (een monetaire waarde), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* of *[!UICONTROL Percentage]* (een percentage met twee decimale punten).<br><br><b> Voorzichtigheid:</b> als u afgeleide metrisch met formaat [!UICONTROL Number w/out Decimal Points] creeert (die gegevens als gehelen toont) en het in een mening of een rapport omvat die een gewogen omzettingsattributieregel ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], of [!UICONTROL Even Distribution]) gebruikt, dan wordt de output getoond in gehelen, niet decimalen. Dit betekent dat afzonderlijke gegevensvelden mogelijk onjuist zijn, ook al zijn de totalen juist. Als een volgorde bijvoorbeeld gelijk is verdeeld tussen drie gebeurtenissen, wordt één volgorde (in plaats van 0,33 volgorde) toegewezen aan elk van de drie gebeurtenissen. Gebruik de metrische notatie [!UICONTROL Number to 2 Decimal Points] om het probleem te voorkomen. |

## Aangepaste metrische instellingen in rapporten en rapportsjablonen en in de verouderde [!UICONTROL Portfolios] weergaven

| Parameter/Sectie | Beschrijving |
|----|----|
| Aangepaste metrische naam | De naam van metrisch, die als kolomnaam verschijnt. <b> Uiteinde:</b> gebruik een betekenisvolle metrische naam, maar ben van mening dat de langere namen de kolom breder maken. |
| Indeling | De gegevens voor deze metrische waarde weergeven: *[!UICONTROL Currency]* (een monetaire waarde), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* of *[!UICONTROL Percentage]* (een percentage met twee decimale punten).<br><br><b> Voorzichtigheid:</b> als u afgeleide metrisch met formaat [!UICONTROL Number w/out Decimal Points] creeert (die gegevens als gehelen toont) en het in een mening of een rapport omvat die een gewogen omzettingsattributieregel ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More], of [!UICONTROL Even Distribution]) gebruikt, dan wordt de output getoond in gehelen, niet decimalen. Dit betekent dat afzonderlijke gegevensvelden mogelijk onjuist zijn, ook al zijn de totalen juist. Als een volgorde bijvoorbeeld gelijk is verdeeld tussen drie gebeurtenissen, wordt één volgorde (in plaats van 0,33 volgorde) toegewezen aan elk van de drie gebeurtenissen. Gebruik de metrische notatie [!UICONTROL Number to 2 Decimal Points] om het probleem te voorkomen. |
| Metrisch invoegen | Een lijst van bestaande metriek waarvan u een formule kunt tot stand brengen.<br><br> om metrisch op het gebied van de formulesinput op te nemen, plaats uw curseur waar u metrisch wilt opnemen, en dan of metrisch van de lijst selecteren of het manueel en ingesloten tussen haakjes ingaan (bijvoorbeeld, `[CPC]`). |
| Operator invoegen | De beschikbare wiskundige exploitanten: `+ - x / ( )`<br><br> om een exploitant op het gebied van de formulesinput op te nemen, plaats uw curseur waar u de exploitant wilt opnemen, en dan of klik de knoop of ga manueel het symbool in. |
| [ Invoergebied van de Formule voor metrisch ] | De wiskundige formule die wordt gebruikt om nieuwe metrisch te berekenen die op één of meerdere bestaande eigenschappen of standaardmetriek (zoals `[Cost]/[Registrations]` wordt gebaseerd. Het kan elke combinatie van metriek en operatoren bevatten.<br><br><b> Nota:</b> De complexe douanemetriek neemt langer om te berekenen, en rapporten en meningen die hen omvatten — vooral wanneer zij afzonderlijke kolommen voor klik-door en mening-door omzettingen omvatten — duurt langer om te produceren. |

>[!MORELIKETHIS]
>
>* [&#x200B; Ongeveer douanemetriek &#x200B;](custom-metric-about.md)
>* [&#x200B; creeer metrische douane &#x200B;](custom-metric-create.md)
>* [&#x200B; geef metrisch douane &#x200B;](custom-metric-edit.md) uit
>* [&#x200B; Schrap metrische douane &#x200B;](custom-metric-delete.md)
