---
source-git-commit: bef353542ee73d32b8ac53e6abd3265528be154f
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---
# Veld automatisch uploaden in account- en campagne-instellingen

**[!UICONTROL Auto Upload]:** (Voor gesynchroniseerde campagnes met [!UICONTROL EF Redirect] alleen) De volgende keer dat Search, Social &amp; Commerce hiermee synchroniseert, wordt automatisch het volgende naar het advertentienetwerk geüpload: a) parameters voor het bijhouden van zoekopdrachten, sociale zaken en handel voor het bijhouden van sjablonen en dezelfde parameters die aan de uiteindelijke URL&#39;s zijn toegevoegd, of b) nieuwe doel-URL&#39;s die zijn ingesloten met de trackingcode Zoeken, Sociale Zaken en Handel. Voor adverteerders met een [Integratie Adobe Advertising-Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=nl-NL) en een server-side AMO ID (s_kwcid) configuratie, omvat de upload ook [AMO ID-parameters](/help/integrations/analytics/ids.md#amo-id) voor uw [!DNL Google Ads] en [!DNL Microsoft Advertising] rekeningen. De standaardinstelling op accountniveau wordt overgenomen van de instellingen voor bijhouden van adverteerders. U kunt de instelling op accountniveau op campagneniveau overschrijven.

**Opmerking:** URL&#39;s bijhouden wordt dagelijks alleen bijgewerkt voor entiteiten die niet meer gesynchroniseerd zijn (dat wil zeggen nieuwe entiteiten die zijn toegevoegd en bestaande entiteiten waarvan de eigenschappen zijn gewijzigd). Als u deze instelling wijzigt van uitgeschakeld in ingeschakeld voor een bestaande adverteerder/account/campagne, worden URL&#39;s die worden bijgehouden niet bijgewerkt voor bestaande entiteiten die al gesynchroniseerd zijn. Neem contact op met het accountteam van de Adobe en vraag een eenmalig, handmatig synchronisatieproces aan als u de URL&#39;s van bestaande, niet-gesynchroniseerde entiteiten wilt bijhouden. Het automatische uploadproces zal toekomstige veranderingen behandelen.
