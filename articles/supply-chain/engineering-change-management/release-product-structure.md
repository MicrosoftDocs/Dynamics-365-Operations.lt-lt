---
title: Išleidžiamo produkto struktūros
description: Šioje temoje paaiškinta, kaip galite išleisti užbaigtas produkto struktūras kartu su išleidžiamais produktais kartu su jų inžinerijos versijomis. Tokiu būdu, galite užtikrinti, kad inžinerijos produkto duomenys gali būti nesunkiai panaudojami kituose juridiniuose asmenyse.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductReleaseSiteBulkEdit, EngChgProductReleaseSendListPage, EngChgProductReleaseSendDetails,EngChgProductReleaseSelection,EngChgProductReleaseReceiveListPage, EngChgProductReleaseReceiveDetails, EngChgProductReleasePreviewPane, EngChgProductReleasePolicy, EngChgProductReleasePart, EngChgProductReleaseNote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 971ff16b862a48581365523edc6b64052b29c380
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967237"
---
# <a name="release-product-structures"></a>Išleidžiamo produkto struktūros

[!include [banner](../includes/banner.md)]

Siekiant užtikrinti, kad su inžinerija susiję produkto duomenys galėtų būti nesunkiai panaudoti kituose juridiniuose asmenyse, galite išleisti užbaigtas produkto struktūras kartu su išleidžiamais produktais ir jų inžinerinėmis versijomis. Dėl to, galite išleisti keletą medžiagų aprašų (BOM) struktūrų kartu su valdančiu vieno išleidimo veiksmu. Tokiu atveju, BOM ir žemesnio lygio produktai taip pat išleidžiami.

Inžinerijos produktai sukuriami ir prižiūrimi jų inžinerijos bendrovės taip, kad jie atitiktų kokybės reikalavimus jų sukūrimo metu. Kiekviena veikianti bendrovė ir gaminanti produktą turi turėti tą produktą ir jį paremiantį BOM. Priklausomai nuo gamybos patalpų, maršrutą galima sukurti lokaliai. Tokiu atveju, jūs neišleisite maršruto kartu su produktu. Juridiniams asmenims, kurie parduos produktus, bet jų negamins, BOM gali nereikėti.

Noredami padaryti procesą efektyvesnį, visi su inžinerija susiję duomenys gali būti išleisti į kitas veikiančias įmones tuo pat metu. Šie duomenys apima produkto struktūrą. Išleidimo proceso metu galite pasirinkti, kuri produkto duomenų dalis turi būti išleista.

Dėl išsamesnės informacijos apie inžinerijos įmones ir veikiančias įmones, žr. [Inžinerijos įmonės ir duomenų turėjimo taisyklės](engineering-org-data-ownership-rules.md).

Atkreipkite dėmesį, kad galite išleisti tiek standartinius produktus, tiek inžinerinius kartu su išleidžiamo produkto struktūra. Šio proceso metu visa produkto struktūrą bus išleista net jei BOM ir maršrutas bendrovei, kuros produktai yra išleidžiami.

Dėl pavyzdžio, kaip išleisti produktą, žr. [Išleisti inžinerijos produktą vietinei bendrovei](engineering-scenarios.md#release)

## <a name="released-data-for-a-product-when-the-release-product-structure-is-used"></a>Išleisti duomenys produktui, kai išleidžiamo produkto struktūra yra naudojama

Tolesni duomenys apima išleidžiamus inžinerinius produktus:

- **Produkto duomenys** – Sukuriamas naujas išleistas produktas.
- **Inžinerijos versijos data** – Inžinerijos versija ir jos duomenys yra sukuriami ir atnaujinami. Atkreipkite dėmesį, kad jei išleidžiate tą pačią inžinerijos versiją dar kartą į veikiančią įmonę, inžinerijos duomenys bus užrašyti.
- **Inžinerijos atributai** – Inžinerijos atributai ir jų versijos yra sukuriami ir atnaujinami.
- **Inžinerijos medžiagų aprašas** – Inžinerijos BOM ir jos eilutės gali būti sukurtos ir atnaujintos. Dėl išsamensės informacijos apie duomenų turėjimą, žr. [Produkto savininkai](product-owner.md).
- **Inžinerijos maršrutai** – Inžinerijos maršrutai ir jų veiksmai gali būti sukurti ir atnaujinti. Dėl išsamensės informacijos apie duomenų turėjimą, žr. [Produkto savininkai](product-owner.md).
- **Inžinerijos dokumentai** – Su inžinerijos versija susieti inžinerijos dokumentai yra sukurti ar atnaujinti.

Jum įjungus inžinerijos keitimo valdymą jūsų sistemoje, išleidžiama produkto struktūra yra prieinama. Taip pat, standartiniai produktai apimantys savo BOMs ir maršrutus jų išleidimo metu.

## <a name="product-acceptance"></a>Produkto priėmimas

**Produkto priėmimas** yra pagrindinis parametras veikiantis išleidimo procesą. Galite nustatyti šį parametrą kiekvienai bendrovei patekę į **Inžinerijos keitimo valdymas \> Nustatymai \> Inžinerijos keitimo valdymo parametrai**. Dėl daugiau informacijos, žr. [Inžinerijos keitimo valdymo parametrai](engineering-parameters.md).

### <a name="automatic-product-acceptance"></a>Automatinis produkto priėmimas

Kiekvienas produktų inžinerijos išleidimas prasideda, kai kas nors iš inžinerijos bendrovės pasirenka išleidžiamą produktą. Kai parametras **Produkto priėmimas** yra nustatytas į *Automatinis*, vartotojas inžinerijos bendrovėje nusprendžia, kurie produkto duomenys turi būti automatiškai paleidžiami į veikiančias bendroves. Produktas tuomet yra automatiškai išleidžiamas į įmones, pasirinktas išleidimo vedlyje.

### <a name="manual-product-acceptance"></a>Rankinis produkto priėmimas

Kiekvienas produktų inžinerijos išleidimas prasideda, kai kas nors iš inžinerijos bendrovės pasirenka išleidžiamą produktą. Kai parametras **Produkto priėmimas** yra nustatytas į *Rankinis*, vartotojas inžinerijos bendrovėje nusprendžia, kurie produkto duomenys turi būti automatiškai paleidžiami į veikiančias bendroves. Vartotojas iš visų veikiančių bendrovių gauna produkto duomenis ir nusprendžia, ar priimti išleidimą. Vartotojas veikiančioje įmonėje gali nustatyti tolesnes parinktis gavęs duomenis:

- Jei gaminiai (naujiniai) nėra svarbūs veikiančiai įmonei, vartotojas gali rinktis nepriimti leidimo.
- Vartotojas gali keisti prekės šabloną naujiems produktams.
- Vartotojas gali rinktis, ar produktas turi būti išleistas kartu su BOM ir (arba) maršrutais ir ar jie turi būti išleisti kaip patvirtinti ir įjungti.
- Vartotojas gali keisti produkto įsigalioja nuo datas.

Dėl pavyzdžio, kaip priima produktą, žr. [Peržiūrėti ir priimti produktą prieš jo išleidimą į vietinę bendrovę](engineering-scenarios.md#accept).

> [!NOTE]
> Standartiniams produktams, juos galite išleisti iš bet kurio juridnio asmens į kitą juridinį asmenį. Inžinerinius produktus vienas juridinis asmuo gali išleisti iš inžinerinės bendrovės.

## <a name="release-policies"></a>Išleidimo politika

Ne visos veikiančios bendrovės reikalauja tų pačių produkto duomenų. Bendrai, veikiančios bendrovės gaminančios inžinerinius produktus reikalauja BOM, o veikiančios bendrovės, kuriso tik parduoda inžinerijos produktus, nereikalauja BOM. Galite naudoti išleidimo politikas, kad nustatytumėte parametrus naudojamus produktų išleidimui/

Inžineriniams produktams išleidimo politika priskiriama prie inžinerijos produkto kategorijos, o laukelis yra privalomas. Standartiniams produktams išleidimo politika priskiriama prie bendrinto produkto kategorijos, o laukelis yra pasirenkamas.

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
| Produkto tipas | Pasirinkite, ar politika taikoma produktams *Prekės* ar *Paslaugų* tipo. Negalite keisti šio nustatymo po to, kai įrašote įrašą. |
| Taikyti šablonus | Pasirinkite vieną iš tolesnių parinkčių norėdami nurodyti, ar ir kaip produkto išleidimo šablonai turi būti taikomi naudojant politiką:<ul><li>**Visada** – Šabloninis išleistas produktas visada turi būt naudojamas leidimams. Jei pasirenkate šią parinktį, naudokite **Visi produktai** „FastTab“ norėdami nurodyti šabloną naudojamą visoms bendrovėms, į kurias išleidžiate. Jei nenurodoto šablono kiekvienai bendrovei esančiai sąraše **Visi produktai** „FastTab“, gausite klaidą bandydami įrašyti politiką.</li><li>**Pasirenkama** – Jei šablonas išleistam produktui nurodomas bendrovei esančiai sąraše **Visi produktai** „FastTab“, kuriam bus naudojamas šablonas išleidžiant tai bendrovei. Kitu atveju, joks šablonas nebus naudojamas. Jei pasirinksite šią parinktį, galite įrašyti politiką nepriskirdami visoms bendrovėms šablonų. (Nebus rodoma jokių įspėjimų.)</li><li>**Niekada** – Joks šablonas išleistam produktui nebus naudojamas jokioms bendrovėms, į kurias išleidžiate, net jei šablonas yra nurodytas bendrovėms esančioms sąraša **Visi produktai** „FastTab“. Šablono stulpeliai bus neprieinami.</li></ul> |
| Aktyvios | Naudokite šią parinktį, kad padėtumėte išlaikyti savo išleidimo politikas. Nustatykite į *Taip* visom jūsų naudojamoms išleidimo politikoms. Nustatykite į *Ne* tam, kad pažymėtumėte išleidimo politiką kaip neaktyvią jos nenaudodami. Įsidėmėkite, kad negali išjungti išleidimo politikos, kuri yra priskirta inžinerijos produkto kategorijai ir galite panaikinti tik neaktyvias leidimo politikas. |

### <a name="all-products-fasttab"></a>Visų produktų „FastTab“

„FastTab“ **Visi produktai** įtraukite eilutę kiekvienai veikiančiai bendrovei, kuriai norite naudoti šią leidimo politiką. Naudokite mygtukus **Visi produktai** „FastTab“ norėdami įtraukti ir pašalinti eilutes, kurių jums reikia. Kiekvienai įtrauktai eilutei, nustatykite tolesnius laukelius.

> [!NOTE]
> Nustatymai **Visi produktai** „FastTab“ taikomi tiek inžinerijos produktams, tiek standartiniams.

| Laukas | aprašymas |
|---|---|
| Įmonės registracijos numeris | Pasirinkite įmonę, kuria eilutė taikoma. Parametrai šioje eilutėje bus taikomi, kai produktai išleisti šiai bendrovei. |
| Išleisto produkto šablonas | Įtraukite produkto šabloną. |
| Kopijuoti KS patvirtinimą | Pasirinkite šį žymimą laukelį, kad nukopijuotumėte BOM patvirtinimo būseną į gaunančią bendrovę. |
| Kopijuoti KS aktyvinimą | Pasirinkite šį žymimą laukelį, kad nukopijuotumėte BOM įjungimo būseną į gaunančią bendrovę. |
| Kopijuoti maršruto patvirtinimą | Pasirinkite šį žymimą laukelį, kad nukopijuotumėte maršruto patvirtinimo būseną į gaunančią bendrovę.|
| Kopijuoti maršruto aktyvinimą | Pasirinkite šį žymimą laukelį, kad nukopijuotumėte įjungimo patvirtinimo būseną į gaunančią bendrovę. |

### <a name="option-parameters-for-engineering-products-fasttab"></a>Parinkties parametrai inžinerijos produktams „FastTab“

Kas kartą kai įtraukiate eilutę **Visi produktai** „FastTab“, eilutė, kurios atitikmuo buvo **Bendrovės sąskaitų ID** vertė taip pat sukuriama **Parinkties parametrai inžinerijos produktams** „FastTab“. Tuomet, jei pašalinate eilutę iš **Visi produktai** „FastTab“, eilutė, kurios atitikmuo buvo **Bendrovės sąskaitų ID** vertė taip pat pašalinama iš **Parinkties parametrai inžinerijos produktams** „FastTab“.

Kiekvienai eilutei rodomai **Parinkties parametrai inžinerijos produktams** „FastTab“, nustatykite tolesnius laukelius.

> [!NOTE]
> Nustatymai **Parinkties parametrai inžinerijos produktams** „FastTab“ taikomi tik inžinerijos produktams.

| Laukas | aprašymas |
|---|---|
| Šabloninė KS | Kai produktas turintis BOM yra išleistas, konkretaus šablono BOM eilutės bus įtrauktos. Šis laukelis naudingas įtraukiant vietinius komponentus, tokius kaip pakavimas ar instrukcijos vietine kalba. |
| Maršruto šablonas | Kai produktas turintis maršrutas yra išleistas, konkretaus šablono BOM eilutės bus įtrauktos. |
| Kopijuokite efektyvumą | Pasirinkite, ar efektyvumo datos turi būti nukopijuotos iš inžinerijos bendrovės į veikiančią bendrovę išleidžiant produktus. |
| Automatiškai įtraukti į išleidimo pasiūlymą | Pasirinkite šį žymimą laukelį gaminiams, kurie turėtų būti automatiškai išleidžiami inžinerijos keitimo užsakyme. Tokiu būdų, produktai priklausantys inžinerijos produktų kategorijoms, naudojančioms šią leidimo politiką gali būti automatiškai išleidžiami veikiančioms bendrovėms, kai ši parinktis nustatyta. (Dėl daugiau informacijos, žr. [Valdyti keitimus inžinerijos produktams](engineering-change-management.md).)

### <a name="review-each-product-when-you-release-it"></a>Peržiūrėkite visus produktus išleidimo metu

Kuriant produktų inžineriją su BOM ar leidžiant maršrutus, parametrai bus nustatyti į numatytąsias vertes, kaip nurodyta leidimo politikoje. Būdamas vartotoju galite veikti tokį elgesį išleidimo vietoje, kai naudojate leidimo produkto struktūrą.

Norėdami išleisti produktus, **Išleisti produktai** puslapyje, pasirinkite išleidimo produktus ir tuomet rinkitės **Išleisti produkto struktūrą**, jei norite atverti išleidimo vedlį. Puslapyje **Pasirinkite inžinerijos produktus išleidimui** rodomi produktai. Pasirinkite vieną produktą ir tada rinktinės **Išleidimo išsami informacija** tam, kad peržiūrėtumėte produkto išsamią išleidimo informaciją.

Puslapyje **Išleidimo išsami informacija** galite keisti **Gauti BOM** vertė, **Kopijuoti BOM patvirtinimą**, **Kopijuoti BOM įjungimo**, **Gauti BOM**, **Kopijuoti maršruto patvirtinimo** ir **Kopijuoti maršruto įjungimo** laukelius. Stūmimo ir traukimo scenarijaus metu, galite keisti tų pačių laukelių vertę gavimo pusėje su sąlyga, kad BOM ir maršrutai yra išleisti.

## <a name="product-owners-and-product-releases"></a>Produkto savininkai ir produkto leidimai

Kadangi produkto savininkai žino, kuriems juridiniams asmenims reikia jų produktų, produktas gali būti išleidžiamas tik to produkto savininkų grupės narių. Kiti vartotojai negali leisit neturimų produktų.

Toks elgesys taikomas tik, kai produktas yra tiesiogiai pasirinktas leidimui. Produktai esantys kito produkto struktūso dalimis per BOM *gali* būti išleisti ne juos turinčių vartotojų, kai jie išleidžia valdančius produktus su sąlyga, kad turi valdantį produktą.

Pavyzdžiui, produktas X yra priskirtas *Kūrimo biurų* produkto savininko grupei. Produktas X taip pat yra BOM Y produkto dalis, kuris yra priskirtas *Projektavimo garsiakalbių* produkto savininko grupei. Jei naudotojas iš *Projektavimo garsiakalbių* produkto savininko grupės išleidžia Y produktą ir jo BOM, produktas X bus išleistas kartu su produktu Y.

Dėl daugiau informacijos, žr. [Produkto savininkai](product-owner.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]