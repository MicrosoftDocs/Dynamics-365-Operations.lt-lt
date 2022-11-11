---
title: „Dynamics 365 Commerce“ esantys domenai
description: Šiame straipsnyje aprašoma, kaip tvarkomi domenai Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: f1a2de7984aad7d291b8a4dc68f5690d57ebe6cc
ms.sourcegitcommit: 2b654e60e2553a5835ab5790db4ccfa58828fae7
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750686"
---
# <a name="domains-in-dynamics-365-commerce"></a>„Dynamics 365 Commerce“ esantys domenai

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip tvarkomi domenai Microsoft Dynamics 365 Commerce.

Domenai yra interneto adresai, naudojami pereiti į „Dynamics 365 Commerce” svetaines žiniatinklio naršyklėje. Jūs kontroliuojate jūsų domeno valdymą su pasirinktu domenų vardų serverio (DNS) tiekėju. Domenai nurodomi „Dynamics 365 Commerce” svetainių daryklėje, kad būtų galima koordinuoti, kaip svetainė bus pasiekiama publikavus. Šiame straipsnyje peržiūrime, kaip domenai yra tvarkomi ir nurodomi per komercijos svetainės kūrimo ciklą ir paleidžiami.

> [!NOTE]
> Nuo 2022 Dynamics 365 Commerce`.dynamics365commerce.ms` metų gegužės 6 d. visos sukurtos aplinkos bus suskurtos su domenu, pakeičiant ankstesnį šabloną `.commerce.dynamics.com`. Esamos aplinkos, kurios yra su domenu `.commerce.dynamics.com`, ir toliau veiks.

## <a name="provisioning-and-supported-host-names"></a>Parengimas ir palaikomi pagrindinių kompiuterių vardai

Suteikiant e-komercijos aplinką [„Microsoft Dynamics  Lifecycle Services“ (LCS)](https://lcs.dynamics.com/), **Palaikomi šeimininko vardai** tiek e-komercijos suteikimo ekrane yra naudojami siekiant įvesti domenus, kurie bus susieti su talpinta „Commerce“ aplinka. Šie domenai bus klientui rodomi domeno pavadinimo serverio (DNS) pavadinimai, kuriame e-komercijos interneto svetainės bus patalpintos. Įvedus domeną šiuo etapu, domeno srautas pradedamas grąžinti Dynamics 365 Commerce. Domeno srautas bus nukreiptas į „Commerce” galinį punktą, tik kai atnaujinamas DNS CNAME įrašas, kad „Commerce” galinis punktas būtų naudojamas su domenu.

> [!NOTE]
> Kelis domenus galima įvesti į langelį **Palaikomi pagrindinių kompiuterių vardai** atskiriant juos kabliataškiais.

Tolesnis paveikslėlis rodo LCS e-komercijos suteikimo ekraną su pabrėžtu **Palaikomais šeimininko pavadinimais** laukeliu. 

![LCS e-komercijos suteikimo ekranas su **Palaikomi talpinimo pavadinimai** pabrėžtas laukelis.](./media/Domains_ProvisioningeCommerceScreen_publish.png)

Galite sukurti paslaugos užklausą, norėdami įtraukti papildomus domenus į aplinką, jei parengimas jau įvyko. Norėdami sukurti paslaugos užklausą LCS, jūsų aplinkoje eikite į **Palaikymas \> Palaikymo problemos** ir pasirinkite **Pateikti incidentą**.

## <a name="commerce-generated-urls"></a>„Commerce” sugeneruoti URL

Suteikiant „Dynamics 365 Commerce“ e-komercijos aplinką, „Commerce“ sukurs URL, kuris bus veikiantis aplinkos adresas. Šis URL yra nukreiptas į e-komercijos saito nuorodą rodomą LCS suteikus aplinką. „Commerce“ sukurtas URL yra šio formato `https://<e-commerce tenant name>.dynamics365commerce.ms`, kuriame e-komercijos nuomotojo pavadinimas yra pavadinimas įvestas į LCS „Commerce“ aplinkoje.

Taip pat galite naudoti gamybos svetainės pagrindinių kompiuterių vardus smėlio dėžės aplinkoje. Ši pasirinktis geriausia, kai galėsite kopijuoti svetainę iš sandbox aplinkos į gamybą.

## <a name="site-setup"></a>Svetainės sąranka

Kai jūsų e-komercijos aplinka yra suteikta, turite nustatyti jūsų saitą „Commerce“ saito kūrimo įrankyje, kad jūsų saitas būtų susietas su veikiančiu URL.

Pirmą kartą nustačius svetainę svetainių daryklėje, bus rodomas dialogo langas **Jūsų svetainės nustatymas**.

Toliau pateiktoje iliustracijoje rodomas dialogo langas **Jūsų svetainės nustatymas** svetainei, kurios pavadinimas „numatytoji”, kai pirmą kartą pasiekiate svetainę svetainių daryklėje.

![Dialogo langas **Jūsų svetainės nustatymas**.](./media/Domains_SetupyoursiteScreen.png)

Langelis **Pasirinkti domeną** leidžia susieti vieną iš palaikomų pagrindinių kompiuterių vardų, pateiktų jūsų svetainei LCS, su svetaine, esančia svetainių daryklėje.

Langelis **Kelias** gali būti paliktas tuščias arba galima įtraukti papildomą kelio eilutę, kuri bus rodoma jūsų darbo URL. Jei langelis **Kelias** paliekamas tuščias, pagrindinis „Commerce” sugeneruotas URL susiejamas su svetaine, kuri nustatoma svetainių daryklėje. Kiekvienos svetainės / domeno poros keliai turi būti unikalūs. Pasirinkus svetainę ir domeną, tik viena aplinkos svetainė gali naudoti tuščią kelią arba būti susieta su unikalaus kelio eilute. Bet kokia eilutė, įtraukta į lauką **Kelias** atliekant svetainės nustatymą, taps papildomu pagrindinio „Commerce” sugeneruoto URL, naudojamo svetainei pasiekti žiniatinklio naršyklėje, keliu.

> [!NOTE]
> Šis kelias dar žinomas kaip **Kelio atitikmuo**, kai įtraukiamas kanalas svetainės daryklės konfigūracijos skyriuje **Svetainės parametrai \> Kanalai**.

Pavyzdžiui, jei turite saito saito kūrimo įrankyje pavadinimu „fabrikam“ e-komercijos nuomotojo pavadinime „xyz“ ir nustatėte saitą su tuščių maršrutu, tuomet prieisite prie publikuoto saito turinio žiniatinklio naršyklėje patekę tiesiogiai į pagrindinį „Commerce“ sukurtą URL:

`https://xyz.dynamics365commerce.ms`

Taip pat, jei tos pačios svetainės nustatymo metu įtraukėte „fabrikam” kelią, turėtumėte prieigą prie paskelbto svetainės turinio žiniatinklio naršyklėje naudodami toliau pateiktą URL.

`https://xyz.dynamics365commerce.ms/fabrikam`

## <a name="pages-and-urls"></a>Puslapiai ir URL

Nustačius svetainę keliu, visi URL, susieti su svetainės daryklės puslapiais, bus sukurti pagal darbo URL („Commerce” sugeneruotą URL arba „Commerce” sugeneruotą URL ir kelią), skirtą svetainei. Jei kursite naują URL svetainių daryklėje (**URL /> +Naujas**) pasirinkdami puslapį iš sąrašo, esančiame dialogo lange **Naujas URL** ir įvesdami to puslapio URL kelią, tas URL bus susietas su pasirinktu puslapiu. URL kelio reikšmė tada pridedama prie svetainės darbo URL, kad būtų galima pasiekti puslapį, ir yra pažymėta kaip `./<URL path>` svetainių daryklės puslapio **URL** URL sąraše.

Toliau pateiktame paveikslėlyje parodytas dialogo langas **Naujas URL** svetainių daryklėje ir paryškintas pavyzdinis URL kelias. 

![Dialogo langas **Naujas URL** svetainių daryklėje.](./media/Domains_PageSetup2a.png)

Toliau pateiktame paveikslėlyje parodytas puslapis **URL** svetainių daryklėje ir sąraše paryškintas pavyzdinis URL.

![Vartotojo srauto vykdymo parinktis strategijos sraute.](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>Domenai svetainių daryklėje

Palaikomų pagrindinių kompiuterių vardų reikšmės gali būti susietos kaip domenas nustatant svetainę. Pasirinkdami palaikomą pagrindinio kompiuterio pavadinimą kaip domeną, matysite pasirinktą domeną, kurį nurodo visos svetainės generatorius. Šis domenas yra tik nuoroda Komercijos aplinkoje. Tiesioginis to domeno srautas dar nebus siunčiamas Dynamics 365 Commerce.

Kai dirbate su svetainėmis svetainių daryklėje, jei turite dvi svetaines, nustatytas su dviem skirtingais domenais, galite pridėti atributą **?domain=** prie savo darbo URL, kad galėtumėte pasiekti publikuotą svetainės turinį naršyklėje.

Pvz., aplinka „xyz” buvo parengta, o svetainių daryklėje sukurtos ir susietos dvi svetainės: viena su domenu `www.fabrikam.com` ir kita su domenu `www.constoso.com`. Kiekviena svetainė buvo nustatyta naudojant tuščią kelią. Tada šios dvi svetainės gali būti pasiekiamos žiniatinklio naršyklėje naudojant atributą **?domain=**, kaip pateikta toliau.
- `https://xyz.dynamics365commerce.ms?domain=www.fabrikam.com`
- `https://xyz.dynamics365commerce.ms?domain=www.contoso.com`

Kai domeno užklausos eilutė pateikta aplinkoje, kurioje pateikti keli domenai, "Commerce" naudoja pirmąjį jūsų pateiktą domeną. Pavyzdžiui, jei kelias „fabrikam” buvo pateiktas pirmiausiai svetainės nustatymo metu, URL `https://xyz.dynamics365commerce.ms` gali būti naudojamas pasiekti publikuotos svetainės turinį `www.fabrikam.com`.

Taip pat galite pridėti pasirinktinius domenus. Norėdami tai padaryti projekto aplinkos komercijos valdymo puslapyje, **paantraštėje El** . prekyba, pasirinkite + Įtraukti **pasirinktinį domeną**. Ats., parodo esamus pasirinktinius domenus ir suteikia pasirinktį įtraukti naują pasirinktinį domeną.

## <a name="update-which-commerce-scale-unit-is-used"></a>Naujinti, kuris "Commerce Scale Unit" naudojamas

"Commerce Scale Unit" (CSU) paprastai pasirenkama iš pradžių sukūrus aplinką. Commerce leidžia pakeisti, kurį CSU egzempliorių naudoja jūsų aplinka, leidžia geriau prižiūrėti savo architektūrą savitarnos funkcijose ir sumažinti poreikį susisiekti su palaikymo tarnyba. Norėdami atnaujinti savo CSU egzempliorių, eikite į projekto aplinkos komercijos valdymo puslapį ir pasirinkite Naujinti skalės **vienetą**. Naudokite naują **komercijos skalės** vienetą norėdami pasirinkti naują CSU egzempliorių iš jūsų aplinkoje galimų CSUs sąrašo.

## <a name="traffic-forwarding-in-production"></a>Srauto perdavimas gamybos metu

Galite imituoti kelis domenus naudodami domeno užklausos eilutės parametrus, esančius commerce.dynamics.com galiniame punkte. Tačiau kai reikia įgyvendinti gamybos metu, turite persiųsti jūsų pasirinktinio domeno srautą į `<e-commerce tenant name>.dynamics365commerce.ms` galinį punktą.

Galinis `<e-commerce tenant name>.dynamics365commerce.ms` punktas nepalaiko pasirinktinio domeno saugiųjų jungčių lygmenų (SSLS), todėl turite nustatyti pasirinktinius domenus naudodami priekinių durų tarnybą arba turinio pristatymo tinklą (CDN). 

Norėdami nustatyti pasirinktinius domenus naudodami „Front Door Service“ arba CDN, turite dvi toliau pateiktas parinktis.

- Nustatykite durų tarnybą, pvz., "Azure Front Door", kad galėtumėte tvarkyti priekinį srautą ir prisijungti prie "Commerce" aplinkos, kuri labiau kontroliuoja domeno ir sertifikatų valdymą bei išsamesnes saugos strategijas.

- Naudokite "Commerce-supplied Azure Front Door" egzempliorių, kuriam reikia imtis veiksmų su komanda, Dynamics 365 Commerce skirta domeno tikrinimui ir SSL sertifikatų gavimas jūsų gamybos domenui.

> [!NOTE]
> Jei naudojate išorinę CDN arba priekinių durų tarnybą, įsitikinkite, kad užklausa yra naudojama "Commerce" platformoje su "Commerce- pateikta" pagrindinio kompiuterio pavadinimu, bet su X-Yra Yra pagrindinis kompiuteris (XFH) antrašte \<custom-domain\>. Pvz., jei yra jūsų "Commerce" `xyz.dynamics365commerce.ms``www.fabrikam.com` galinis punktas, o pasirinktinis domenas yra, `xyz.dynamics365commerce.ms` reikia perduoti užklausos pagrindinio kompiuterio antraštę, o XFH antraštę –`www.fabrikam.com`.

Informacijos apie tai, kaip nustatyti CDN paslaugą tiesiogiai, žr. [Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md).

Norėdami naudoti „Commerce” teikiamą „Azure Front Door” egzempliorių, turite sukurti paslaugos užklausą, kad gautumėte CDN nustatymo pagalbos iš „Commerce” supažindinimo komandos. 

- Jums reikės pateikti savo įmonės pavadinimą, gamybos domeną, aplinkos ID ir gamybos el. komercijos nuomininko pavadinimą. 
- Jums reikės patvirtinti, ar ši tarnybos užklausa skirta esamam domenui (naudojama šiuo metu aktyviai svetainei) ar naujam domenui. 
- Jei tai naujas domenas, domeno tikrinimas ir SSL sertifikatas gali būti pasiektas vienu veiksmu. 
- Domenui, naudojančiam esamą svetainę, būtinas kelių žingsnių procesas domeno tikrinimui ir SSL sertifikatui nustatyti. Šis procesas turi 7 darbo dienų aptarnavimo lygio sutartį (SLA), skirtą domenui, kad jis būtų įgyvendintas, nes procesas apima kelis nuoseklius veiksmus.

Norėdami sukurti paslaugos užklausą LCS, jūsų aplinkoje eikite į **Palaikymas \> Palaikymo problemos** ir pasirinkite **Pateikti incidentą**.

> [!NOTE]
> Pasirinktiniai domenai su SSL palaikomi tik gamybos aplinkose. Ne gamybos aplinkose, pvz., smėlio dėžės ir vartotojo priėmimo testavimo (UAT), naudokite „Commerce” sugeneruotą URL, kad pasiektumėte publikuotą turinį žiniatinklio naršyklėje.

## <a name="ssl-certificate-process"></a>SSL sertifikato procesas

Kai paslaugos užklausa pateikta, „Commerce” komanda su jumis derins toliau pateiktus veiksmus.

Jei domenai nauji, bus atlikti toliau pateikti veiksmai.
- „Commerce” komanda nustatys „Azure Front Door” egzempliorių („Commerce” nuomojamą).
- Tada „Commerce” komanda pateiks CNAME įrašą, kuris nurodys į jūsų pasirinktinį domeną.
- Po to, kai CNAME įrašas bus atnaujintas, „Commerce” nuomojamas „Azure Front Door” egzempliorius galės patikrinti domeno savininką ir gauti SSL sertifikatą.

Jei domenai esami / aktyvūs, bus atlikti toliau pateikti veiksmai.
- „Commerce” komanda nurodys jums, kaip įtraukti `afdverify.<custom-domain>` CNAME įrašą, kad būtų galima jį pateikti jūsų domeno DNS teikėjui.
- Baigus, „Commerce” komanda įtrauks domeną į „Azure Front Door” egzempliorių ir pateiks papildomų DNS TXT įrašų, kad jie būtų įtraukti į domeno DNS.
- Užbaigus TXT įrašus, „Commerce” komanda užbaigs „Azure Front Door” naujinimus, skirtus domenui, kuris nustatys SSL sertifikatą.

## <a name="apex-domains"></a>Viršūnės domenai

"Commerce-supplied Azure Front Door" egzempliorius nepalaiko "APex" domenų (šakniniai domenai, kuriuose nėra su padomenių). Norint naudoti "Apex" domenus reikia nustatyti IP adresą, o "Commerce Azure Front Door" egzempliorius turi tik virtualiuosius galinius punktus. Norėdami naudoti apex domeną, turite šias pasirinktis:

- **1 parinktis** – naudokite jūsų DNS teikėją, kad nukreiptumėte viršūnės domeną į „www” domeną. Pvz., fabrikam.com nukreipia į `www.fabrikam.com`, o `www.fabrikam.com` yra CNAME įrašas, nurodantis į „Commerce” nuomojamą „Azure Front Door” egzempliorių.

- **2 parinktis** – jei jūsų DNS tiekėjas palaiko ALIAS įrašus, galite nurodyti "Apex" domeną į "Azure Front Door" galinį punktą, kuris užtikrina, kad galinio punkto IP pakeitimas bus rodomas. "Azure" priekinės saugyklos egzempliorius turi būti iš jūsų pagrindinio kompiuterio.
  
- **3 parinktis** – jei jūsų DNS tiekėjas nepalaiko PSEUDONIMO įrašų, tada turite pakeisti savo DNS tiekėją į "Azure DNS" ir patiems nuo pagrindinio kompiuterio nuoduoti "Azure" DNS ir "Azure" priekinės saugyklos egzempliorių.

> [!NOTE]
> Jei naudojate „Azure Front Door”, taip pat turite nustatyti „Azure” DNS toje pačioje prenumeratoje. Viršūnės domenas, nuomojamas „Azure” DNS, gali nukreipti į jūsų „Azure Front Door” kaip į pseudonimo įrašą. Tai yra vienintelis sprendimas, nes viršūnės domenai visada turi nukreipti į IP adresą.
  
Jei turite klausimų dėl "Apex" domenų, kreipkitės į " [Microsoft" palaikymo tarnybą](https://support.microsoft.com/).

  ## <a name="additional-resources"></a>Papildomi ištekliai

  [Talpinkite naują e-komercijos nuomotoją](deploy-ecommerce-site.md)

  [Interneto parduotuvės kanalo integravimas](./channel-setup-online.md)

  [Sukurkite e-komercijos saitą](create-ecommerce-site.md)

  [Susiekite „Dynamics 365 Commerce“ saitą su interneto kanalu](associate-site-online-store.md)

  [robots.txt failų tvarkymas](manage-robots-txt-files.md)

  [Masinis URL peradresavimų nusiuntimas](upload-bulk-redirects.md)

  [B2C nuomotojo nustatymas „Commerce“ aplinkoje](set-up-B2C-tenant.md)

  [Vartotojo prisijungimo pasirinktinių puslapių sąranka](custom-pages-user-logins.md)

  [„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas](configure-multi-B2C-tenants.md)

  [Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md)

  [Parduotuvės nustatymo pagal vietą įgalinimas](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
