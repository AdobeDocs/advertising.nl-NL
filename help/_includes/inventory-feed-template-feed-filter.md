---
source-git-commit: 73c9cc7134360e073fc466dda3733cfc9bac8786
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---
# Tekst en sjabloon - Feed Filter

**\[filter van de Diervoed \]:** Welke rijen in het voederdossier om te verspreiden:

* *[!UICONTROL Propagate all rows found in feed:]* (De standaardinstelling) Gegevens doorgeven voor alle rijen.

* *[!UICONTROL Propagate rows that meet certain conditions:]* Gegevens alleen doorgeven voor rijen die aan maximaal tien opgegeven voorwaarden voldoen. Geef de filters op die u wilt toepassen:

   1. Selecteer de Booleaanse bewerking die u voor alle filters wilt gebruiken: **[!UICONTROL AND]** of **[!UICONTROL OR]** .

   1. Selecteer een kolomnaam in het eerste menu, selecteer een operator in het tweede menu en voer vervolgens de toepasselijke waarden in of laat het invoerveld leeg om gegevens voor rijen zonder voorwaarden te verspreiden.

  De kolomlijst bevat alle beschikbare kolommen in de feed.

  Beschikbare operatoren zijn onder andere *[!UICONTROL contains]*, *[!UICONTROL does not contain]*, *[!UICONTROL =]*, *[!UICONTROL <>]* (is niet gelijk aan), *[!UICONTROL in]*, *[!UICONTROL not in]*, *[!UICONTROL less than]* en *[!UICONTROL greater than]* . Wanneer u de exploitant &quot; [!UICONTROL in] selecteert,&quot;kunt u een komma-gescheiden lijst van waarden ingaan; als een verslag om het even welke gespecificeerde waarden aanpast, dan worden de gegevens verspreid voor die rijen. Voer voor alle andere operatoren slechts één waarde in. Waarden zijn niet hoofdlettergevoelig.

  Als u bijvoorbeeld de kolom &quot;product_type&quot; selecteert en alleen rijen wilt retourneren voor productnamen die &quot;schoenen&quot; bevatten, selecteert u &quot;**[!UICONTROL contains]**&quot; en voert u `shoes` in het invoerveld in.

   1. (Als u maximaal negen extra filters wilt toepassen) Klik op **[!UICONTROL Add Condition]** voor elk extra filter en geef vervolgens het aanvullende filter op per stap 2.
