---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# Tekst en sjabloon - Feed Filter

**\[Feed-filter\]:** Welke rijen in het feed-bestand worden doorgegeven:

* *[!UICONTROL Propagate all rows found in feed:]* (De standaardinstelling) Als u gegevens voor alle rijen wilt doorgeven.

* *[!UICONTROL Propagate rows that meet certain conditions:]* Gegevens alleen doorgeven voor rijen die aan maximaal tien opgegeven voorwaarden voldoen. Geef de filters op die u wilt toepassen:

   1. Selecteer de Booleaanse bewerking die u voor alle filters wilt gebruiken:  **[!UICONTROL AND]** of **[!UICONTROL OR]**.

   1. Selecteer een kolomnaam in het eerste menu, selecteer een operator in het tweede menu en voer vervolgens de toepasselijke waarden in of laat het invoerveld leeg om gegevens voor rijen zonder voorwaarden te verspreiden.

   De kolomlijst bevat alle beschikbare kolommen in de feed.

   Beschikbare operatoren omvatten *[!UICONTROL contains]*, *[!UICONTROL does not contain]*, *[!UICONTROL =]*, *[!UICONTROL <>]* (is niet gelijk aan), *[!UICONTROL in]*, *[!UICONTROL not in]*, *[!UICONTROL less than]*, en *[!UICONTROL greater than]*. Wanneer u de operator &quot;[!UICONTROL in],&quot; kunt u een lijst met door komma&#39;s gescheiden waarden invoeren; als een record overeenkomt met een van de opgegeven waarden, worden gegevens voor die rijen doorgegeven. Voer voor alle andere operatoren slechts één waarde in. Waarden zijn niet hoofdlettergevoelig.

   Als u bijvoorbeeld de kolom &quot;product_type&quot; hebt geselecteerd en alleen rijen wilt retourneren voor productnamen die &quot;schoenen&quot; bevatten, selecteert u &quot;**[!UICONTROL contains]**&quot; en voer `shoes` in het invoerveld.

   1. (Als u maximaal negen extra filters wilt toepassen) Klik voor elk extra filter op **[!UICONTROL Add Condition]** en geeft u vervolgens het aanvullende filter op per stap 2.
