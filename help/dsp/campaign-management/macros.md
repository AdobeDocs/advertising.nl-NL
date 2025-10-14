---
title: Advertising DSP Macros
description: Verwijs naar de beschikbare macro's voor het algemene volgen en om kliks op derdevertoningsadvertenties te volgen.
feature: DSP Ads
exl-id: 7058c988-c544-4a61-84dd-eec4ce88ceba
source-git-commit: 195e75386e64c3659d3f4db3c2508ac903e9e311
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# Advertising DSP Macros

Een macro is een korte opdracht of korte opdracht voor een instructie en volgt doorgaans de indeling `${MACRO_NAME}` . Macro&#39;s die zijn opgenomen in creatieve code of doorklikken-URL&#39;s, worden uitgebreid naar een langere codereeks die de advertentieserver kan begrijpen. De DSP en de server voeren macro&#39;s uit wanneer de advertentie wordt bediend of geklikt.

Servermacro&#39;s zijn handig om belangrijke informatie door te geven aan DSP of aan externe ad-hocservers. Macro&#39;s worden het meest gebruikt tijdens de handel in creatieve code of meta-gegevens van derden en douane (zoals derdepixel).

U kunt een macro overal, zoals in een markering VAST, in om het even welke URL, of in een DSP of derdegebeurtenispixel manueel opnemen. Elke DSP-client en -partner heeft echter een andere indeling voor een advertentietag en de macro&#39;s moeten dienovereenkomstig op verschillende plaatsen in de tag worden ingevoegd. Elke keer dat u met een nieuwe klant of partner werkt, vraagt u hen om documentatie over waar u de macro&#39;s in hun advertentietags moet invoegen die door DSP worden verhandeld.

## Algemene trackingsmacro&#39;s

Gebruik algemene &#39;tracking&#39;-macro&#39;s voor alle advertentietypen en tagtypen om zo nodig specifieke gegevens door te geven.

| Macro | Beschrijving van vervanging | Type |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | De account-id. | integer |
| `${TM_AD_ID}` | De ad-toets (adKey). | string |
| `${TM_AD_ID_NUM}` | De advertentie-id. | integer |
| `${TM_ADVERTISER_ID}` | De adverteerder-id. | integer |
| `${TM_CAMPAIGN_ID}` | De campagnesleutel. | string |
| `${TM_CAMPAIGN_ID_NUM}` | De campagne-id. | integer |
| ` ${TM_CLICK_URL}` | De omleidings-URL, waarmee advertentieservers kunnen bijhouden en tellen en klikken. Wanneer de advertentie wordt aangeboden en de gebruiker erop klikt, wordt de macro geactiveerd en wordt de klik geregistreerd en geteld voor rapportagedoeleinden. | string |
| ` ${TM_CLICK_URL_URLENC}` | De gecodeerde omleidings-URL, waarmee ad-servers kunnen bijhouden en tellen en klikken. Wanneer de advertentie wordt aangeboden en de gebruiker erop klikt, wordt de macro geactiveerd en wordt de klik geregistreerd en geteld voor rapportagedoeleinden. Gebruik deze macro alleen als u advertenties van derden maakt en uw leverancier URL-codering vereist. | string |
| `${TM_FEED_ID}` | De sleutel voor de mediaplaatsing (feedKey). | string |
| `${TM_FEED_ID_NUM}` | De id voor de plaatsing van het medium. | integer |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | De sitecode voor de plaatsing. Vereist voor [!DNL AppsFlyer] klik op Trackers voor mobiele apps om advertenties te installeren. <!-- should map to placement_site_key column of placement_site table --> | string |
| `${TM_PLACEMENT_ID}` | De plaatsingssleutel (cpKey). | string |
| `${TM_PLACEMENT_ID_NUM}` | De plaatsing-id. | integer |
| `${TM_RANDOM}` | Cachebuster: een willekeurig getal tussen 1 en 1000000. | lang |
| `${TM_SESSION_ID}` | De id van de sessie, die overeenkomt met één ophaalbewerking van de advertentietag. | string |
| `${TM_SITE_DOMAIN_URLENC}` | Het subdomein van de pagina dat vanuit de URL in de biedaanvraag is geparseerd; URL-gecodeerd. Niet ondersteund voor in-banner, klik-aan-spel advertenties. | string |
| ` ${TM_SITE_NAME}` | De sitenaam voor de plaatsing. | string |
| `${TM_SITE_URL_URLENC}` | De URL die in de biedaanvraag is doorgegeven; URL-gecodeerd. Niet ondersteund voor in-banner, klik-aan-spel advertenties. | string |
| `${TM_SITE_ID_NUM}` | De site-id voor de plaatsing. | integer |
| `${TM_TIMESTAMP}` | De Unix-tijdstempel die aangeeft hoeveel seconden zijn verstreken sinds middernacht (00:00 UTC) op 1 januari 1970. | lang |
| ` ${TM_VIDEO_DURATION}` | De duur van de advertentievideo in seconden. | integer |

{style="table-layout:auto"}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## Mobiele macro&#39;s

| Macro | Beschrijving van vervanging | Type |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore]) De platform-id, die overeenkomt met het besturingssysteem van het apparaat:<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` wanneer het platform geen van de bovenstaande items is</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore]) De naam van het apparatenmodel, URL-Gecodeerd. | string |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore]) Het milieu waarin de advertentie werd gediend:<ul><li>`a` = mobiele toepassing</li><li>`b` = mobiele website</li></ul> | tekenreeks (`a` of `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen]) De platform-id, die overeenkomt met het besturingssysteem van het apparaat:<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` wanneer het platform geen van de bovenstaande items is</li></ul> | string |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen]) Het apparaattype waarop de advertentie viewer was:<ul><li>`TAB` = tablet</li><li>`PHN` = mobiel</li><li>`computer` = computer</li></ul> | string |
| `${UOO}` | ([!DNL Nielsen]) Of de gebruiker het volgen van advertenties al dan niet heeft uitgeschakeld:<ul><li>`1` (DNT-markering = 1) = de gebruiker heeft de advertentie niet bijgehouden</li><li>`0` (DNT-markering = 0) = de gebruiker heeft zich aangemeld voor advertentie-tracking</li></ul> | integer (`0` of `1`) |
| `${TM_BUNDLE}` | De bundel-id voor de [!DNL iOS] - of [!DNL Android] -app-store. Voorbeelden: com.zynga.wwf2.free of id804379658 | string |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` geeft aan of de bieder bepaalt dat het bod afkomstig is uit de Europese Unie en dat GDPR-handhaving vereist:<ul><li>`1` = GDPR moet worden afgedwongen</li><li>`0` = GDPR mag niet worden afgedwongen</li></ul>`gdpr_consent=${GDPR_CONSENT}` is de waarde van de toestemming die door de leverancier is doorgegeven in de binnenkomende biedaanvraag:<ul><li>In de meeste gevallen is dit een basis64url-gecodeerde toestemmingskoord, of madeliefje (voorbeeld: BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMBkIDIgM0AgOJxAnQA)</li><li>`0` = geen toestemming</li><li>`1` = toestemming</li></ul> | desybit of integer |

{style="table-layout:auto"}

## Klik op Macro&#39;s voor externe weergaveadvertenties

DSP vereist een klikmacro voor de weergave om op nauwkeurige wijze te kunnen bijhouden voor advertenties die gebruikmaken van externe weergavetags. Er is slechts één versie van de macro vereist; de relevante macro is afhankelijk van het type code.

| Macro | Beschrijving van vervanging | Type |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | De omleidings-URL waarmee advertentieservers het platform kunnen bijhouden, tellen en klikken. | string |
| `${TM_CLICK_URL_URLENC}` | De omleidings-URL waarmee advertentieservers die URL-codering nodig hebben, kunnen worden bijgehouden en geteld en op het platform kunnen worden geklikt. | string |

{style="table-layout:auto"}

DSP voegt automatisch klikmacro&#39;s in een weergavetag van derden in wanneer u:

* Advertentietags exporteren van een advertentieserverpartner <!-- [Needs PM confirmation.] -->
* Bulkupload [!DNL Flashtalking] of [!DNL Google DoubleClick for Advertisers] advertentietags direct in DSP

Als een klikmacro ontbreekt wanneer u een vertoningsadvertentie bouwt, toont DSP een waarschuwingsbericht, dat u ertoe aanzet om de aangewezen vertoning manueel op te nemen klikt macro in het correcte gebied van de markering.

## [!DNL Analytics for Advertising] Macro&#39;s

Voor extra macro&#39;s beschikbaar specifiek voor [[!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) klanten, zie &quot;[&#x200B;  [!DNL Analytics for Advertising]  Macro&#39;s aan  [!DNL Flashtalking]  Advertentietags &#x200B;](/help/integrations/analytics/macros-flashtalking.md)&quot;toevoegen en &quot;[&#x200B; voegt  [!DNL Analytics for Advertising]  Macro&#39;s aan  [!DNL Google Campaign Manager 360]  toe - Markeringen &#x200B;](/help/integrations/analytics/macros-google-campaign-manager.md).&quot;

## Problemen met macrofouten oplossen

Wanneer u macro&#39;s aan uw code toevoegt, zorg ervoor u de nauwkeurige syntaxis van de macro gebruikt. Bij het valideren van de macro&#39;s controleert DSP of de macro precies overeenkomt met een van de geldige macro&#39;s.

Er worden fouten gegenereerd als er tekens ontbreken aan het begin of einde van de macronaam. Er wordt bijvoorbeeld een foutbericht weergegeven als:

* U vergeet een of meer tekens aan het begin van de macronaam, zoals `${` . Als u de volledige syntaxis niet opneemt, wordt het item niet herkend als een geldige macro.
* De macro eindigt niet met een geldige set tekens, zoals `}` .

>[!MORELIKETHIS]
>
>* [&#x200B; Audio Advertentie Montages &#x200B;](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [&#x200B; Verbonden TV en Montages &#x200B;](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [&#x200B; Vertoning en Montages &#x200B;](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [&#x200B; Mobiele Advertentie Montages &#x200B;](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [&#x200B; Inheemse Montages &#x200B;](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [&#x200B; pre-rol en Montages &#x200B;](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [&#x200B; Universele Video en Montages &#x200B;](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
