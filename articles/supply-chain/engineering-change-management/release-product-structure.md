---
title: Išleidžiamo produkto struktūros
description: Šiame straipsnyje paaiškinama, kaip galima paleisti visas produktų struktūras ir paleisti produktus kartu su jų inžinerijos versijomis. Tokiu būdu, galite užtikrinti, kad inžinerijos produkto duomenys gali būti nesunkiai panaudojami kituose juridiniuose asmenyse.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductReleaseSiteBulkEdit, EngChgProductReleaseSendListPage, EngChgProductReleaseSendDetails,EngChgProductReleaseSelection,EngChgProductReleaseReceiveListPage, EngChgProductReleaseReceiveDetails, EngChgProductReleasePreviewPane, EngChgProductReleasePolicy, EngChgProductReleasePart, EngChgProductReleaseNote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c8359f86e5123ee40e9673971de626e1b327ac95
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875487"
---
# <a name="release-product-structures"></a>Išleidžiamo produkto struktūros

[!include [banner](../includes/banner.md)]

Siekiant užtikrinti, kad su inžinerija susiję produkto duomenys galėtų būti nesunkiai panaudoti kituose juridiniuose asmenyse, galite išleisti užbaigtas produkto struktūras kartu su išleidžiamais produktais ir jų inžinerinėmis versijomis. Dėl to, galite išleisti keletą medžiagų aprašų (KS) struktūrų kartu su valdančiu vieno išleidimo veiksmu. Tokiu atveju, KS ir žemesnio lygio produktai taip pat išleidžiami.

Inžinerijos produktai sukuriami ir prižiūrimi jų inžinerijos bendrovės taip, kad jie atitiktų kokybės reikalavimus jų sukūrimo metu. Kiekviena veikianti bendrovė ir gaminanti produktą turi turėti tą produktą ir jį paremiantį KS. Priklausomai nuo gamybos patalpų, maršrutą galima sukurti lokaliai. Tokiu atveju, jūs neišleisite maršruto kartu su produktu. Juridiniams asmenims, kurie parduos produktus, bet jų negamins, KS gali nereikėti.

Norėdami padaryti procesą efektyvesnį, visi su inžinerija susiję duomenys gali būti išleisti į kitas veikiančias įmones tuo pat metu. Šie duomenys apima produkto struktūrą. Išleidimo proceso metu galite pasirinkti, kuri produkto duomenų dalis turi būti išleista.

Dėl išsamesnės informacijos apie inžinerijos įmones ir veikiančias įmones, žr. [Inžinerijos įmonės ir duomenų turėjimo taisyklės](engineering-org-data-ownership-rules.md).

Atkreipkite dėmesį, kad galite išleisti tiek standartinius produktus, tiek inžinerinius kartu su išleidžiamo produkto struktūra. Šio proceso metu visa produkto struktūrą bus išleista net jei KS ir maršrutas bendrovei, kurios produktai yra išleidžiami.

Dėl pavyzdžio, kaip išleisti produktą, žr. [Išleisti inžinerijos produktą vietinei bendrovei](engineering-scenarios.md#release)

## <a name="released-data-for-a-product-when-the-release-product-structure-is-used"></a>Išleisti duomenys produktui, kai išleidžiamo produkto struktūra yra naudojama

Tolesni duomenys apima išleidžiamus inžinerinius produktus:

- **Produkto duomenys** – Sukuriamas naujas išleistas produktas.
- **Inžinerijos versijos data** – Inžinerijos versija ir jos duomenys yra sukuriami ir atnaujinami. Atkreipkite dėmesį, kad jei išleidžiate tą pačią inžinerijos versiją dar kartą į veikiančią įmonę, inžinerijos duomenys bus užrašyti.
- **Inžinerijos atributai** – Inžinerijos atributai ir jų versijos yra sukuriami ir atnaujinami.
- **Inžinerijos medžiagų aprašas** – Inžinerijos KS ir jos eilutės gali būti sukurtos ir atnaujintos. Išsamesnės informacijos apie duomenų turėjimą rasite [Produkto savininkai](product-owner.md).
- **Inžinerijos maršrutai** – Inžinerijos maršrutai ir jų veiksmai gali būti sukurti ir atnaujinti. Išsamesnės informacijos apie duomenų turėjimą rasite[Produkto savininkai](product-owner.md).
- **Inžinerijos dokumentai** – Su inžinerijos versija susieti inžinerijos dokumentai yra sukurti ar atnaujinti.

Jums įjungus inžinerijos keitimo valdymą jūsų sistemoje, išleidžiama produkto struktūra yra prieinama. Taip pat, standartiniai produktai apimantys savo KSs ir maršrutus jų išleidimo metu.

## <a name="product-acceptance"></a>Produkto priėmimas

**Produkto priėmimas** yra pagrindinis parametras veikiantis išleidimo procesą. Galite nustatyti šį parametrą kiekvienai bendrovei patekę į **Inžinerijos keitimo valdymas \> Nustatymai \> Inžinerijos keitimo valdymo parametrai**. Dėl daugiau informacijos, žr. [Inžinerijos keitimo valdymo parametrai](engineering-parameters.md).

### <a name="automatic-product-acceptance"></a>Automatinis produkto priėmimas

Kiekvienas produktų inžinerijos išleidimas prasideda, kai kas nors iš inžinerijos bendrovės pasirenka išleidžiamą produktą. Kai parametras **Produkto priėmimas** yra nustatytas į *Automatinis*, vartotojas inžinerijos bendrovėje nusprendžia, kurie produkto duomenys turi būti automatiškai paleidžiami į veikiančias bendroves. Produktas tuomet yra automatiškai išleidžiamas į įmones, pasirinktas išleidimo vedlyje.

### <a name="manual-product-acceptance"></a>Rankinis produkto priėmimas

Kiekvienas produktų inžinerijos išleidimas prasideda, kai kas nors iš inžinerijos bendrovės pasirenka išleidžiamą produktą. Kai parametras **Produkto priėmimas** yra nustatytas į *Rankinis*, vartotojas inžinerijos bendrovėje nusprendžia, kurie produkto duomenys turi būti automatiškai paleidžiami į veikiančias bendroves. Vartotojas iš visų veikiančių bendrovių gauna produkto duomenis ir nusprendžia, ar priimti išleidimą. Vartotojas veikiančioje įmonėje gali nustatyti tolesnes parinktis gavęs duomenis:

- Jei gaminiai (naujiniai) nėra svarbūs veikiančiai įmonei, vartotojas gali rinktis nepriimti leidimo.
- Vartotojas gali keisti prekės šabloną naujiems produktams.
- Vartotojas gali rinktis, ar produktas turi būti išleistas kartu su KS ir (arba) maršrutais ir ar jie turi būti išleisti kaip patvirtinti ir įjungti.
- Vartotojas gali keisti produkto įsigalioja nuo datas.

Dėl pavyzdžio, kaip priima produktą, žr. [Peržiūrėti ir priimti produktą prieš jo išleidimą į vietinę bendrovę](engineering-scenarios.md#accept).

> [!NOTE]
> Standartiniams produktams, juos galite išleisti iš bet kurio juridinio asmens į kitą juridinį asmenį. Inžinerinius produktus vienas juridinis asmuo gali išleisti iš inžinerinės bendrovės.

## <a name="release-policies"></a>Išleidimo politika

Ne visos veikiančios bendrovės reikalauja tų pačių produkto duomenų. Bendrai, veikiančios bendrovės gaminančios inžinerinius produktus reikalauja KS, o veikiančios bendrovės, kurios tik parduoda inžinerijos produktus, nereikalauja KS. Galite naudoti išleidimo politikas, kad nustatytumėte parametrus naudojamus produktų išleidimui/

Dėl daugiau informacijos apie inžinerijos produktų kategorijas, žr. [Inžinerijos versijos ir inžinerijos produkto kategorijos](engineering-versions-product-category.md).

Išleidimo proceso metu, galite keisti nustatymus.

## <a name="create-and-manage-product-release-policies"></a>Sukurkite ir valdykite produkto išleidimo politikas

Tam, kad dirbtumėte su produkto išleidimo politikomis, eikite į **Inžinerijos keitimo valdymą \> Nustatymus \> Produkto išleidimo politikos**. Tuomet atlikite vieną iš šių žingsnių.

- Norėdami sukurti naują politiką, rinkitės **Naujas** veiksmų juostoje ir tada nustatykite laukelius kaip aprašyta tolesniuose papildomuose skyriuose.
- Norėdami redaguoti esančią politiką, sąrašo juostoje ją pasirinkite ir rinkitės **Redaguoti** veiksmų juostoje ir tada nustatykite laukelius kaip aprašyta tolesniuose papildomuose skyriuose.
- Norėdami panaikinti politiką, sąrašo juostoje ją pasirinkite ir rinkitės  **Redaguoti** veiksmų juostoje ir tada **Bendri** „FastTab“, įsitikinkite, kad **Įjungta** parinktis nustatyta į *Ne*. Tada rinkitės **Naikinti** veiksmų juostoje.

### <a name="header"></a>Antraštė

Nustatykite tolesnius laukelius produkto išleidimo politikos antraštėje.

| Laukas | aprašymas |
|---|---|
| Pavadinimas / vardas ir (arba) pavardė | Įveskite politikos pavadinimą. |
| aprašymas | Įveskite politikos aprašą. |

### <a name="general-fasttab"></a>Bendras „FastTab“ skirtukas

Nustatykite tolesnius laukelius **Bendri** produkto išleidimo politikos „FastTab“.

| Laukas | aprašymas |
|---|---|
| Produkto tipas | Pasirinkite, ar strategija taikoma produktams *Prekės* ar *Paslaugų* tipo. Negalite keisti šio nustatymo po to, kai įrašote įrašą. |
| Gamybos tipas | Šis laukas pasirodys tik tada, kai įgalinsite [formulių keitimo valdymą](manage-formula-changes.md) savo sistemoje. Pasirinkite gamybos, kuriai taikoma ši išleidimo strategija, tipą:<ul><li>**Sudėtinis produktas** – Naudokite šią išleidimo strategiją sudėtiniams produktams valdyti. Sudėtiniai produktai yra gaminami gamybos proceso metu ir jie nėra versijos ar inžineriniai produktai. Sudėtinių produktų išleidimo strategijos gali padėti užtikrinti, kad svarbūs parametrai, pavyzdžiui, **Saugojimo dimensijų grupė** ir **Sekimo dimensijų grupė**, būtų nustatomi naudojant Išleisto produkto šabloną prieš jų išleidimą į įmonę.</li><li>**Šalutinis produktas** – Naudokite šią išleidimo strategiją šalutiniams produktams valdyti. Šalutiniai produktai yra gaminami gamybos proceso metu ir jie nėra versijos ar inžineriniai produktai. Šalutinių produktų išleidimo strategijos gali padėti užtikrinti, kad svarbūs parametrai, pavyzdžiui, **Saugojimo dimensijų grupė** ir **Sekimo dimensijų grupė**, būtų nustatomi naudojant Išleisto produkto šabloną prieš jų išleidimą į įmonę.</li><li>**Nėra** – Naudokite šią strategiją, norėdami valdyti standartinius produktus, kurie nėra versijos ar inžineriniai produktai, kitaip tariant, sudėtinius arba šalutinius produktus.</li><li>**Planuojama prekė** – Naudokite šią išleidimo strategiją planuojamoms prekėms, kurios gaminamos naudojant gamybos procesą, valdyti. Prekių planavimui naudojamos formulės. Jos yra panašios į sudėtines prekes, tačiau jos naudojamos tik sudėtiniams ir šalutiniams, bet ne baigtiems produktams gaminti.</li><li>**KS** – Naudokite šią išleidimo strategiją inžinerijos produktų, nenaudojančių formulių ir įprastai (tačiau nebūtinai) turinčių KS, valdymui.</li><li>**Formulė** – Naudokite šią išleidimo strategiją užbaigtoms prekėms, kurios gaminamos naudojant gamybos procesą, valdyti. Šios prekės turės formulę, bet ne KS.</li></ul> |
| Taikyti šablonus | Pasirinkite vieną iš tolesnių parinkčių norėdami nurodyti, ar ir kaip produkto išleidimo šablonai turi būti taikomi naudojant politiką:<ul><li>**Visada** – Šabloninis išleistas produktas visada turi būt naudojamas leidimams. Jei pasirenkate šią parinktį, naudokite **Visi produktai** „FastTab“ norėdami nurodyti šabloną naudojamą visoms bendrovėms, į kurias išleidžiate. Jei nenurodote šablono kiekvienai bendrovei esančiai sąraše **Visi produktai** „FastTab“, gausite klaidą bandydami įrašyti politiką.</li><li>**Pasirenkama** – Jei šablonas išleistam produktui nurodomas bendrovei esančiai sąraše **Visi produktai** „FastTab“, kuriam bus naudojamas šablonas išleidžiant tai bendrovei. Kitu atveju, joks šablonas nebus naudojamas. Jei pasirinksite šią parinktį, galite įrašyti politiką nepriskirdami visoms bendrovėms šablonų. (Nebus rodoma jokių įspėjimų.)</li><li>**Niekada** – Joks šablonas išleistam produktui nebus naudojamas jokioms bendrovėms, į kurias išleidžiate, net jei šablonas yra nurodytas bendrovėms esančioms sąraše **Visi produktai** „FastTab“. Šablono stulpeliai bus neprieinami.</li></ul> |
| Aktyvios | Naudokite šią parinktį, kad padėtumėte išlaikyti savo išleidimo politikas. Nustatykite į *Taip* visom jūsų naudojamoms išleidimo politikoms. Nustatykite į *Ne* tam, kad pažymėtumėte išleidimo politiką kaip neaktyvią jos nenaudodami. Įsidėmėkite, kad negali išjungti išleidimo politikos, kuri yra priskirta inžinerijos produkto kategorijai ir galite panaikinti tik neaktyvias leidimo politikas. |

### <a name="all-products-fasttab"></a>Visų produktų „FastTab“

„FastTab“ **Visi produktai** įtraukite eilutę kiekvienai veikiančiai bendrovei, kuriai norite naudoti šią leidimo politiką. Naudokite mygtukus **Visi produktai** „FastTab“ norėdami įtraukti ir pašalinti eilutes, kurių jums reikia. Kiekvienai įtrauktai eilutei, nustatykite tolesnius laukelius.

> [!NOTE]
> Nustatymai **Visi produktai** „FastTab“ taikomi tiek inžinerijos produktams, tiek standartiniams.

| Laukas | aprašymas |
|---|---|
| Įmonės registracijos numeris | Pasirinkite įmonę, kuria eilutė taikoma. Parametrai šioje eilutėje bus taikomi, kai produktai išleisti šiai bendrovei. |
| Išleisto produkto šablonas | Įtraukite produkto šabloną. |
| Kopijuoti KS patvirtinimą | Pasirinkite šį žymimą laukelį, kad nukopijuotumėte KS patvirtinimo būseną į gaunančią bendrovę. |
| Kopijuoti KS aktyvinimą | Pasirinkite šį žymimą laukelį, kad nukopijuotumėte KS įjungimo būseną į gaunančią bendrovę. |
| Kopijuoti maršruto patvirtinimą | Pasirinkite šį žymimą laukelį, kad nukopijuotumėte maršruto patvirtinimo būseną į gaunančią bendrovę.|
| Kopijuoti maršruto aktyvinimą | Pasirinkite šį žymimą laukelį, kad nukopijuotumėte įjungimo patvirtinimo būseną į gaunančią bendrovę. |

### <a name="option-parameters-for-engineering-products-fasttab"></a>Parinkties parametrai inžinerijos produktams „FastTab“

Kas kartą kai įtraukiate eilutę **Visi produktai** „FastTab“, eilutė, kurios atitikmuo buvo **Bendrovės sąskaitų ID** vertė taip pat sukuriama **Parinkties parametrai inžinerijos produktams** „FastTab“. Tuomet, jei pašalinate eilutę iš **Visi produktai** „FastTab“, eilutė, kurios atitikmuo buvo **Bendrovės sąskaitų ID** vertė taip pat pašalinama iš **Parinkties parametrai inžinerijos produktams** „FastTab“.

Kiekvienai eilutei rodomai **Parinkties parametrai inžinerijos produktams** „FastTab“, nustatykite tolesnius laukelius.

> [!NOTE]
> Nustatymai **Parinkties parametrai inžinerijos produktams** „FastTab“ taikomi tik inžinerijos produktams.

| Laukas | aprašymas |
|---|---|
| Šabloninė KS | Kai produktas turintis KS yra išleistas, konkretaus šablono KS eilutės bus įtrauktos. Šis laukelis naudingas įtraukiant vietinius komponentus, tokius kaip pakavimas ar instrukcijos vietine kalba. |
| Maršruto šablonas | Kai produktas turintis maršrutas yra išleistas, konkretaus šablono KS eilutės bus įtrauktos. |
| Kopijuokite efektyvumą | Pasirinkite, ar efektyvumo datos turi būti nukopijuotos iš inžinerijos bendrovės į veikiančią bendrovę išleidžiant produktus. |
| Automatiškai įtraukti į išleidimo pasiūlymą | Pasirinkite šį žymimą laukelį gaminiams, kurie turėtų būti automatiškai išleidžiami inžinerijos keitimo užsakyme. Tokiu būdų, produktai priklausantys inžinerijos produktų kategorijoms, naudojančioms šią leidimo politiką gali būti automatiškai išleidžiami veikiančioms bendrovėms, kai ši parinktis nustatyta. (Dėl daugiau informacijos, žr. [Valdyti keitimus inžinerijos produktams](engineering-change-management.md).)

### <a name="review-each-product-when-you-release-it"></a>Peržiūrėkite visus produktus išleidimo metu

Kuriant produktų inžineriją su KS ar leidžiant maršrutus, parametrai bus nustatyti į numatytąsias vertes, kaip nurodyta leidimo politikoje. Būdamas vartotoju galite veikti tokį elgesį išleidimo vietoje, kai naudojate leidimo produkto struktūrą.

Norėdami išleisti produktus, **Išleisti produktai** puslapyje, pasirinkite išleidimo produktus ir tuomet rinkitės **Išleisti produkto struktūrą**, jei norite atverti išleidimo vedlį. Puslapyje **Pasirinkite inžinerijos produktus išleidimui** rodomi produktai. Pasirinkite vieną produktą ir tada rinktinės **Išleidimo išsami informacija** tam, kad peržiūrėtumėte produkto išsamią išleidimo informaciją.

Puslapyje **Išleidimo išsami informacija** galite keisti **Gauti KS** vertė, **Kopijuoti KS patvirtinimą**, **Kopijuoti KS įjungimo**, **Gauti KS**, **Kopijuoti maršruto patvirtinimo** ir **Kopijuoti maršruto įjungimo** laukelius. Stūmimo ir traukimo scenarijaus metu, galite keisti tų pačių laukelių vertę gavimo pusėje su sąlyga, kad KS ir maršrutai yra išleisti.

## <a name="product-owners-and-product-releases"></a>Produkto savininkai ir produkto leidimai

Kadangi produkto savininkai žino, kuriems juridiniams asmenims reikia jų produktų, produktas gali būti išleidžiamas tik to produkto savininkų grupės narių. Kiti vartotojai negali leisit neturimų produktų.

Toks elgesys taikomas tik, kai produktas yra tiesiogiai pasirinktas leidimui. Produktai esantys kito produkto struktūros dalimis per KS *gali* būti išleisti ne juos turinčių vartotojų, kai jie išleidžia valdančius produktus su sąlyga, kad turi valdantį produktą.

Pavyzdžiui, produktas X yra priskirtas *Kūrimo biurų* produkto savininko grupei. Produktas X taip pat yra KS Y produkto dalis, kuris yra priskirtas *Projektavimo garsiakalbių* produkto savininko grupei. Jei naudotojas iš *Projektavimo garsiakalbių* produkto savininko grupės išleidžia Y produktą ir jo KS, produktas X bus išleistas kartu su produktu Y.

Dėl daugiau informacijos, žr. [Produkto savininkai](product-owner.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
