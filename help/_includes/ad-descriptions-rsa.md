---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---
# Het veld Beschrijvingen toevoegen in de RSA-advertentie-instellingen

**[!UICONTROL Ad Descriptions]:** Minimaal twee en maximaal vier advertentiereferenties met optionele positiepunten. Het advertentienetwerk toont advertenties met maximaal twee beschrijvingen; Voer ten minste twee in. De maximale lengte voor elke beschrijving is 90 tekens, inclusief alle dynamische tekst (zoals de waarden van trefwoorden en adverteerders).

Als u een advertentieklanter wilt invoegen, gebruikt u de volgende indelingen, waarbij `Default text` is een optionele waarde die moet worden ingevoegd wanneer uw feed geen geldige waarde bevat:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Als u een beschrijving wilt vastzetten op een bepaalde positie, selecteert u de optie voor het vastzetten (bijvoorbeeld &quot;[!UICONTROL Pinned at position 1]&quot;). Voor elke positie moet ten minste één beschrijving beschikbaar zijn. Als u meerdere beschrijvingen op dezelfde positie vastzet, wordt in de laatste en altijd een van deze beschrijvingen op de opgegeven positie geplaatst. Beschrijvingen die op positie 2 zijn vastgezet, mogen niet met de advertentie worden getoond.

Als u een aanvullende beschrijving wilt toevoegen, klikt u op **[!UICONTROL + Add]**.
