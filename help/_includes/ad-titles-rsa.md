---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---
# Het veld Titels toevoegen in de RSA-advertentie-instellingen

**[!UICONTROL Ad Titles]:** Ten minste drie, tot en met vijftien, en titels (koppen), met optionele positiepunten. Het advertentienetwerk toont advertenties met maximaal drie koppen; Voer ten minste drie in. De maximumlengte voor elke titel is 30 tekens, inclusief alle dynamische tekst (zoals de waarden van trefwoorden en adverteerders).

Als u een advertentieklanter wilt invoegen, gebruikt u de volgende indelingen, waarbij `Default text` is een optionele waarde die moet worden ingevoegd wanneer uw feed geen geldige waarde bevat:

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Als u een titel op een bepaalde positie wilt vastzetten, selecteert u de optie voor het vastzetten (bijvoorbeeld &quot;[!UICONTROL Pinned at position 1]&quot;). Voor elke positie moet ten minste één titel beschikbaar zijn. Als u meerdere titels vastzet op dezelfde positie, bevat de laatste en altijd een van deze titels op de opgegeven positie. Titels die op positie 3 zijn vastgezet, worden mogelijk niet met de advertentie weergegeven.

Als u een extra titel wilt toevoegen, klikt u op **[!UICONTROL + Add]**.
