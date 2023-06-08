---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---
# Het veld Type omleiden in account- en campagne-instellingen

**[!UICONTROL Redirect Type]:** (Voor [!UICONTROL EF Redirect] (alleen) De methode waarmee eindgebruikers worden omgeleid naar de uiteindelijke URL of doel-URL. De geselecteerde optie is van toepassing op alle advertenties, trefwoorden en plaatsingen in de account of campagne. De standaardinstelling op accountniveau wordt overgenomen van de instellingen voor bijhouden van adverteerders en de standaardinstelling op campagneniveau wordt overgenomen van de accountinstellingen.

* *[!UICONTROL Standard]:* Alleen de eindgebruiker omleiden naar de opgegeven URL.

* *[!UICONTROL Token]:* Als u de eindgebruiker wilt omleiden naar de URL en ook de zoek-, sociale en commerciële id voor de klik wilt opnemen (`ef_id`) als een parameter van het vraagkoord, die als teken wordt gebruikt. Kies deze optie als u offlinetransacties wilt rapporteren, u wilt zoeken, sociaal en commercieel gegevens uitwisselen met Adobe Analytics of als u alle conversies wilt bijhouden die plaatsvinden binnen [!DNL Apple Safari] browsers.

**Opmerkingen:**

* Als u van [!UICONTROL Standard] tot [!UICONTROL Token], of vice versa, dan moet u het volgen URLs voor de rekening opnieuw produceren.
* U kunt de instelling op accountniveau op campagneniveau overschrijven.
