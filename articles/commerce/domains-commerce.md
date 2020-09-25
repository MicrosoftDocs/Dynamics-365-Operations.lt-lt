---
title: „Dynamics 365 Commerce” domenai
description: Šioje temoje aprašoma, kaip domenai valdomi „Microsoft Dynamics 365 Commerce”.
author: BrShoo
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: BrShoo
ms.search.validFrom: ''
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 84becee12363ca38951ff13073d87d1b1f14b616
ms.sourcegitcommit: a47a4652a29fdb567a8ba67c4f914a8698e8c48c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/03/2020
ms.locfileid: "3765006"
---
# <a name="domains-in-dynamics-365-commerce"></a>„Dynamics 365 Commerce” domenai

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip domenai valdomi „Microsoft Dynamics 365 Commerce”.

Domenai yra interneto adresai, naudojami pereiti į „Dynamics 365 Commerce” svetaines žiniatinklio naršyklėje. Jūs kontroliuojate jūsų domeno valdymą su pasirinktu domenų vardų serverio (DNS) tiekėju. Domenai nurodomi „Dynamics 365 Commerce” svetainių daryklėje, kad būtų galima koordinuoti, kaip svetainė bus pasiekiama publikavus. Šioje temoje nagrinėjama, kaip domenai valdomi ir nurodomi „Commerce” svetainės kūrimo ir paleidimo ciklo metu.

## <a name="provisioning-and-supported-host-names"></a>Parengimas ir palaikomi pagrindinių kompiuterių vardai

Kuriant „e-Commerce” aplinką [„Microsoft Dynamics Lifecycle Services” (LCS)](https://lcs.dynamics.com/), „e-Commerce” parengimo ekrane rodomas laukas **Palaikomi pagrindinių kompiuterių vardai** naudojamas domenams, kurie bus susieti su įdiegta „Commerce” aplinka, įvesti. Šie domenai bus kliento domenų vardų serverio (DNS) vardai, kur bus nuomojamos „e-Commerce” svetainės. Šio etapo metu įvedus domeną nepradedama nukreipti domeno srauto į „Dynamics 365 Commerce”. Domeno srautas bus nukreiptas į „Commerce” galinį punktą, tik kai atnaujinamas DNS CNAME įrašas, kad „Commerce” galinis punktas būtų naudojamas su domenu.

> [!NOTE]
> Kelis domenus galima įvesti į langelį **Palaikomi pagrindinių kompiuterių vardai** atskiriant juos kabliataškiais.

Toliau pateiktoje iliustracijoje parodytas LCS „e-Commerce” parengimo ekranas, kuriame paryškintas langelis **Palaikomi pagrindinių kompiuterių vardai**. 

![LCS „e-Commerce” parengimo ekranas, kuriame paryškintas langelis **Palaikomi pagrindinių kompiuterių vardai**](./media/Domains_ProvisioningeCommerceScreen.png)

Galite sukurti paslaugos užklausą, norėdami įtraukti papildomus domenus į aplinką, jei parengimas jau įvyko. Norėdami sukurti paslaugos užklausą LCS, jūsų aplinkoje eikite į **Palaikymas \> Palaikymo problemos** ir pasirinkite **Pateikti incidentą**.

## <a name="commerce-generated-urls"></a>„Commerce” sugeneruoti URL

Rengiant „e-Commerce” aplinką, „Commerce” sugeneruos URL, kuris bus aplinkos darbo adresas. Šis URL nurodomas „e-Commerce” svetainės saite, kuris rodomas LCS po to, kai aplinka sukonfigūruota. „Commerce” sugeneruoto URL formatas yra `https://<e-Commerce tenant name>.commerce.dynamics.com`, kuriame „e-Commerce” nuomotojo pavadinimas yra LCS įvestas „Commerce” aplinkos pavadinimas.

Taip pat galite naudoti gamybos svetainės pagrindinių kompiuterių vardus smėlio dėžės aplinkoje. Ši parinktis puikiai tinka, kai kopijuojate svetainę iš smėlio dėžės aplinkos į gamybos aplinką.

## <a name="site-setup"></a>Svetainės sąranka

Kai parengta jūsų „e-Commerce” aplinka, turite nustatyti jūsų svetainę „Commerce” svetainių daryklėje ir susieti jūsų svetainę su darbo URL.

Pirmą kartą nustačius svetainę svetainių daryklėje, bus rodomas dialogo langas **Jūsų svetainės nustatymas**.

Toliau pateiktoje iliustracijoje rodomas dialogo langas **Jūsų svetainės nustatymas** svetainei, kurios pavadinimas „numatytoji”, kai pirmą kartą pasiekiate svetainę svetainių daryklėje.

![Dialogo langas **Jūsų svetainės nustatymas**](./media/Domains_SetupyoursiteScreen.png)

Langelis **Pasirinkti domeną** leidžia susieti vieną iš palaikomų pagrindinių kompiuterių vardų, pateiktų jūsų svetainei LCS, su svetaine, esančia svetainių daryklėje.

Langelis **Kelias** gali būti paliktas tuščias arba galima įtraukti papildomą kelio eilutę, kuri bus rodoma jūsų darbo URL. Jei langelis **Kelias** paliekamas tuščias, pagrindinis „Commerce” sugeneruotas URL susiejamas su svetaine, kuri nustatoma svetainių daryklėje. Kiekvienos svetainės / domeno poros keliai turi būti unikalūs. Pasirinkus svetainę ir domeną, tik viena aplinkos svetainė gali naudoti tuščią kelią arba būti susieta su unikalaus kelio eilute. Bet kokia eilutė, įtraukta į lauką **Kelias** atliekant svetainės nustatymą, taps papildomu pagrindinio „Commerce” sugeneruoto URL, naudojamo svetainei pasiekti žiniatinklio naršyklėje, keliu.

> [!NOTE]
> Šis kelias dar žinomas kaip **Kelio atitikmuo**, kai įtraukiamas kanalas svetainės daryklės konfigūracijos skyriuje **Svetainės parametrai \> Kanalai**.

Pvz., jei svetainių daryklės „e-Commerce” nuomotojuje pavadinimu „xyz“ turite svetainę pavadinimu „fabrikam“ ir nustatėte svetainę tuščiu keliu, tada turėtumėte prieigą prie paskelbto svetainės turinio žiniatinklio naršyklėje eidami tiesiai į pagrindinį „Commerce” sugeneruotą URL.

`https://xyz.commerce.dynamics.com`

Taip pat, jei tos pačios svetainės nustatymo metu įtraukėte „fabrikam” kelią, turėtumėte prieigą prie paskelbto svetainės turinio žiniatinklio naršyklėje naudodami toliau pateiktą URL.

`https://xyz.commerce.dynamics.com/fabrikam`

## <a name="pages-and-urls"></a>Puslapiai ir URL

Nustačius svetainę keliu, visi URL, susieti su svetainės daryklės puslapiais, bus sukurti pagal darbo URL („Commerce” sugeneruotą URL arba „Commerce” sugeneruotą URL ir kelią), skirtą svetainei. Jei kursite naują URL svetainių daryklėje (**URL /> +Naujas**) pasirinkdami puslapį iš sąrašo, esančiame dialogo lange **Naujas URL** ir įvesdami to puslapio URL kelią, tas URL bus susietas su pasirinktu puslapiu. URL kelio reikšmė tada pridedama prie svetainės darbo URL, kad būtų galima pasiekti puslapį, ir yra pažymėta kaip `./<URL path>` svetainių daryklės puslapio **URL** URL sąraše.

Toliau pateiktame paveikslėlyje parodytas dialogo langas **Naujas URL** svetainių daryklėje ir paryškintas pavyzdinis URL kelias. 

![Dialogo langas **Naujas URL** svetainių daryklėje](./media/Domains_PageSetup2a.png)

Toliau pateiktame paveikslėlyje parodytas puslapis **URL** svetainių daryklėje ir sąraše paryškintas pavyzdinis URL.

![Vartotojo srauto vykdymo parinktis strategijos sraute](./media/Domains_URLsInSiteBuilder2a.png)

## <a name="domains-in-site-builder"></a>Domenai svetainių daryklėje

Palaikomų pagrindinių kompiuterių vardų reikšmės gali būti susietos kaip domenas nustatant svetainę. Renkantis palaikomą pagrindinio kompiuterio vardo reikšmę kaip domeną, pasirinktas domenas bus nurodytas svetainės daryklėje. Šis domenas „Commerce” aplinkoje yra tik nuoroda, o to domeno tiesioginis srautas nebus perduotas į „Dynamics 365 Commerce”.

Kai dirbate su svetainėmis svetainių daryklėje, jei turite dvi svetaines, nustatytas su dviem skirtingais domenais, galite pridėti atributą **?domain=** prie savo darbo URL, kad galėtumėte pasiekti publikuotą svetainės turinį naršyklėje.

Pvz., aplinka „xyz” buvo parengta, o svetainių daryklėje sukurtos ir susietos dvi svetainės: viena su domenu `www.fabrikam.com` ir kita su domenu `www.constoso.com`. Kiekviena svetainė buvo nustatyta naudojant tuščią kelią. Tada šios dvi svetainės gali būti pasiekiamos žiniatinklio naršyklėje naudojant atributą **?domain=**, kaip pateikta toliau.
- `https://xyz.commerce.dynamics.com?domain=www.fabrikam.com`
- `https://xyz.commerce.dynamics.com?domain=www.contoso.com`

Kai domeno užklausos eilutė nenurodyta aplinkoje su keliais domenais, „Commerce” naudoja pirmą domeną, kurį nurodėte. Pavyzdžiui, jei kelias „fabrikam” buvo pateiktas pirmiausiai svetainės nustatymo metu, URL `https://xyz.commerce.dynamics.com` gali būti naudojamas pasiekti publikuotos svetainės turinį `www.fabrikam.com`.

## <a name="traffic-forwarding-in-production"></a>Srauto perdavimas gamybos metu

Galite imituoti kelis domenus naudodami domeno užklausos eilutės parametrus, esančius commerce.dynamics.com galiniame punkte. Tačiau kai reikia įgyvendinti gamybos metu, turite persiųsti jūsų pasirinktinio domeno srautą į `<e-Commerce tenant name>.commerce.dynamics.com` galinį punktą.

`<e-Commerce tenant name>.commerce.dynamics.com` galinis punktas nepalaiko pasirinktinio domeno saugiųjų jungčių lygmenų (SSL), todėl reikia nustatyti pasirinktinius domenus naudojant „Front Door Service“ arba turinio pristatymo tinklą (CDN). 

Norėdami nustatyti pasirinktinius domenus naudodami „Front Door Service“ arba CDN, turite dvi toliau pateiktas parinktis.

- Nustatykite „Azure Front Door”, kad būtų galima valdyti sąsajos serverio srautą ir prisijungti prie savo „Commerce” aplinkos. Tai suteikia galimybę labiau kontroliuoti domenus ir sertifikatus bei išsamesnes saugos strategijas.
- Naudokite „Commerce” pateiktą „Azure Front Door” egzempliorių. Tam reikia koordinuoti veiksmus su „Dynamics 365 Commerce” komanda, kad būtų galima atlikti domeno tikrinimą ir gauti SSL sertifikatus savo gamybos domenui.

Informacijos apie tai, kaip nustatyti CDN paslaugą tiesiogiai, žr. [Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md).

Norėdami naudoti „Commerce” teikiamą „Azure Front Door” egzempliorių, turite sukurti paslaugos užklausą, kad gautumėte CDN nustatymo pagalbos iš „Commerce” supažindinimo komandos. 

- Jums reikės nurodyti jūsų įmonės pavadinimą, gamybos domeną, aplinkos ID ir gamybos „e-Commerce” nuomotojo pavadinimą. 
- Jums reikės patvirtinti, ar tai esamas domenas (naudojamas šiuo metu aktyvioje svetainėje), ar naujas domenas. 
- Jei tai naujas domenas, domeno tikrinimas ir SSL sertifikatas gali būti pasiektas vienu veiksmu. 
- Jei tai esamos svetainės domenas, yra kelių veiksmų procesas, kurio reikia norint nustatyti domeno tikrinimą ir SSL sertifikatą. Šis procesas turi 7 darbo dienų aptarnavimo lygio sutartį (SLA), skirtą domenui, kad jis būtų įgyvendintas, nes procesas apima kelis nuoseklius veiksmus.

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

„Commerce” teikiamas „Azure Front Door” egzempliorius nepalaiko viršūnės domenų (šakninių domenų, kuriuose nėra antrinių domenų). Viršūnės domenams išspręsti reikalingas IP adresas, o „Commerce Azure Front Door” egzempliorius egzistuoja tik su virtualiaisiais galiniais punktais. Norėdami naudoti viršūnės domeną, turite dvi toliau pateiktas parinktis.

- **1 parinktis** – naudokite jūsų DNS teikėją, kad nukreiptumėte viršūnės domeną į „www” domeną. Pvz., fabrikam.com nukreipia į `www.fabrikam.com`, o `www.fabrikam.com` yra CNAME įrašas, nurodantis į „Commerce” nuomojamą „Azure Front Door” egzempliorių.

- **2 parinktis** – nustatykite CDN / „Front Door” egzempliorių, kad būtų galima nuomoti viršūnės domeną.

> [!NOTE]
> Jei naudojate „Azure Front Door”, taip pat turite nustatyti „Azure” DNS toje pačioje prenumeratoje. Viršūnės domenas, nuomojamas „Azure” DNS, gali nukreipti į jūsų „Azure Front Door” kaip į pseudonimo įrašą. Tai yra vienintelis sprendimas, nes viršūnės domenai visada turi nukreipti į IP adresą.

  ## <a name="additional-resources"></a>Papildomi ištekliai

  [Naujos e. prekybos svetainės visuotinis diegimas](deploy-ecommerce-site.md)

  [Interneto parduotuvės kanalo integravimas](online-stores.md)

  [El. prekybos svetainės kūrimas](create-ecommerce-site.md)

  [Interneto svetainės susiejimas su kanalu](associate-site-online-store.md)

  [„Robots.txt” failų tvarkymas](manage-robots-txt-files.md)

  [Masinis URL peradresavimų nusiuntimas](upload-bulk-redirects.md)

  [B2C nuomotojo nustatymas „Commerce“ aplinkoje](set-up-B2C-tenant.md)

  [Vartotojo prisijungimo pasirinktinių puslapių sąranka](custom-pages-user-logins.md)

  [„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas](configure-multi-B2C-tenants.md)

  [Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md)

  [Parduotuvės nustatymo pagal vietą įgalinimas](enable-store-detection.md)
