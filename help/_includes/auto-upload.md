---
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---
# Veld automatisch uploaden in account- en campagne-instellingen

**[!UICONTROL Auto Upload]:** (Voor gesynchroniseerde campagnes met [!UICONTROL EF Redirect] alleen) De volgende keer dat Search, Social &amp; Commerce hiermee synchroniseert, wordt automatisch het volgende naar het advertentienetwerk geüpload: a) parameters voor het bijhouden van zoekopdrachten, sociale zaken en handel voor het bijhouden van sjablonen en dezelfde parameters die aan de uiteindelijke URL&#39;s zijn toegevoegd, of b) nieuwe doel-URL&#39;s die zijn ingesloten met de trackingcode Zoeken, Sociale Zaken en Handel. Voor adverteerders met een [Integratie Adobe Advertising-Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) en een server-side AMO ID-configuratie (s_kwcid), bevat de upload ook AMO ID-parameters voor uw [!DNL Google Ads] en [!DNL Microsoft Advertising] rekeningen. De standaardinstelling op accountniveau wordt overgenomen van de instellingen voor bijhouden van adverteerders. U kunt de instelling op accountniveau op campagneniveau overschrijven.

**Opmerking:** URL&#39;s bijhouden wordt dagelijks alleen bijgewerkt voor entiteiten die niet meer gesynchroniseerd zijn (dat wil zeggen nieuwe entiteiten die zijn toegevoegd en bestaande entiteiten waarvan de eigenschappen zijn gewijzigd). Als u deze instelling wijzigt van uitgeschakeld in ingeschakeld voor een bestaande adverteerder/account/campagne, worden URL&#39;s die worden bijgehouden niet bijgewerkt voor bestaande entiteiten die al gesynchroniseerd zijn. Als u de URL&#39;s van bestaande, synchrone entiteiten wilt bijhouden, neemt u contact op met uw Adobe-accountteam en vraagt u een eenmalig, handmatig synchronisatieproces. Het automatische uploadproces zal toekomstige veranderingen behandelen.
