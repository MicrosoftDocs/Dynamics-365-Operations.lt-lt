---
title: Grąžinimų valdymo sandoriai
description: Šiame skyriuje paaiškinta, kaip kurti grąžinimų valdymų sandorius. Sandoriai naudojami skirtingiems grąžinimų ir autorinių honorarų skaičiavimo metodams ir pagrindams kontroliuoti. Jie apima įtraukimo ir išimčių taisykles.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 76cdbf21cfbc0db7b363d0fbf60a1ecd0046efc1
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689697"
---
# <a name="rebate-management-deals"></a>Grąžinimų valdymo sandoriai

[!include [banner](../includes/banner.md)]

Grąžinimų valdymo sandoriai naudojami skirtingiems grąžinimų ir autorinių honorarų skaičiavimo metodams ir pagrindams kontroliuoti. Jie apima įtraukimo ir išimčių taisykles. Yra trys grąžinimų valdymo sandorių tipai: klientų grąžinimai, kliento autoriniai honorarai ir tiekėjo grąžinimai. Visi trys tipai naudoja panašius parametrus. Šioje temoje nurodomi egzistuojantys skirtumai tarp jų.

## <a name="create-a-deal"></a>Sandorio kūrimas

1. Eikite į **Grąžinimų valdymas \> Grąžinimų valdymo sandoriai \> Visi grąžinimų valdymo sandoriai**. **Visų grąžinimų valdymo sandorių** sąrašo puslapyje galite kurti ir dirbti su visų trijų tipų sandoriais.

    Kitu atveju atlikite vieną iš šių veiksmų. Kiekvienu atveju atsirandantis sąrašo puslapis pateikia visus tuos pačius parametrus kaip ir **Visų grąžinimų valdymo sandorių** sąrašo puslapis, tačiau jis yra filtruotas rodyti tik vieno tipo sandorius.

    - Eikite į **Grąžinimų valdymas \> Grąžinimų valdymo sandoriai \> Klientų grąžinimų sandoriai**, jei norite kurti tik klientų grąžinimų sandorius.
    - Eikite į **Grąžinimų valdymas \> Grąžinimų valdymo sandoriai \> Klientų autorinių honorarų sandoriai**, jei norite kurti tik klientų autorinių honorarų sandorius.
    - Eikite į **Grąžinimų valdymas \> Grąžinimų valdymo sandoriai \> Tiekėjų grąžinimų sandoriai**, jei norite kurti tik tiekėjų grąžinimų sandorius.

1. Veiksmų srityje pasirinkite **Naujas**.
1. Dialogo lange **Naujo sandorio kūrimas** nustatykite tolesnius laukus:

    - **Grąžinimų valdymo sandoris** – jei grąžinimų sandoriams [nustatėte numeraciją](rebate-management-parameters.md), šis laukas yra automatiškai nustatytas į sistemos sugeneruotą unikalųjį ID. Kitu atveju įveskite unikalųjį ID.
    - **Aprašas** – įveskite sandorio aprašą.
    - **Modulis** – pasirinkite partnerio, kuriam taikomas sandoris, tipą (*Klientas* arba *Tiekėjas*). Atsižvelgiant į puslapį, nuo kurio pradėjote, šis laukas gali būti automatiškai nustatytas pagal pasirinktą sandorio tipą. Šiuo atveju lauko režimas yra tik skaityti.
    - **Tipas** – pasirinkite sandorio tipą (*Grąžinimas* arba *Autorinis honoraras*). Atsižvelgiant į puslapį, nuo kurio pradėjote, šis laukas gali būti automatiškai nustatytas pagal pasirinktą sandorio tipą. Šiuo atveju lauko režimas yra tik skaityti.
    - **Derinti pagal** – pasirinkite, kaip sandoris turėtų būti skaičiuojamas ir derinamas:

        - *Sandoris* – vienas grąžinimas turi būti apdorotas visiems sandorio grąžinimams ir atskaitymams.
        - *Eilutė* – grąžinimai turi būti apdorojami kiekvienai sandorio eilutei.

    - **Registravimo šablonas** – pasirinkite [registravimo šabloną](rebate-management-posting.md), skirtą naudoti operacijoms, kurioms taikomas sandoris. Šį lauką galima naudoti nustačius lauką **Derinti pagal** į *Sandoris*. Jeigu jis nustatytas į *Eilutė*, šabloną priskirsite vėliau kiekvienai eilutei, kurią įtraukiate į sandorį.
    - **Registravimo šablonas, skirtas garantijoms** – pasirinkite [registravimo šabloną](rebate-management-posting.md), skirtą naudoti garantijos operacijoms. Garantijos operacijoms reikalingi registravimo šablonai tik tuo atveju, jei autoriniam honorarui taikoma garantija. Priešingu atveju, nors registravimo šablonas neprivalomas, jei nenurodytas joks registravimo šablonas, registruojant garantijas bus rodoma klaida. Šį lauką galima naudoti tik nustačius lauką **Tipas** į *Autorinis honoraras*. 
    - **Grąžinimo išvestis** – pasirinkite, kaip turi būti apmokamas grąžinimas arba autorinis honoraras:

        - *Finansinė* – generuokite laisvos formos kredito pažymą arba mokėtinų sumų debeto pažymą tam, kad sumos būtų apmokėtos arba gautos vėliau. Atkreipkite dėmesį, kad nuostatos **gali** būti naudojamos su grąžinimais, kai pasirinkta ši parinktis. Ši parinktis yra vienintelė galima parinktis, kai laukas **Tipas** nustatytas į *Autorinis honoraras*.
        - *Prekė* – generuokite prekių pardavimo užsakymą pagal sandorio nustatymą. Šiame pardavimo užsakyme kiekvienai prekei priskiriama 0 (nulinė) kaina. Atkreipkite dėmesį, kad nuostatos **negali** būti naudojamos su grąžinimais, kai pasirinkta ši parinktis.

    - **Grąžinimo valiuta** – pasirinkite valiutą, kuri bus naudojama sumokant grąžinimą, atskaitymą arba autorinį honorarą.
    - **Dokumento pastabos** – įveskite pastabas apie sandorį, kaip reikalinga.
    - **Kaupiamoji garantija** – šią parinktį galite nustatyti į *Taip*, tik jei laukas **Tipas** nustatytas į *Autorinis honoraras*. Ši parinktis turi įtakos garantinių atskaitymų mokėjimų skaičiavimui. Toliau pateikiamas pavyzdys.

        - Sandorio garantija yra parduoti vertę, sąlygojančią $10 000 mokėjimą kas ketvirtį.
        - Prekes parduodanti organizacija, parduoda vertę, sąlygojančią $12 000 vertės atskaitymo mokėjimą 1 ketvirtyje. Rezultatas yra sumokėtas $12 000 vertės autorinis atlyginimus, atėmus $10 000 garantiją.
        - Jei parinktis **Kaupiamoji garantija** nustatyta į *Taip*, papildomas $2000 autorinis honoraras, sumokėtas 1 ketvirtyje, bus taikomas 2 ketvirčiui. Todėl klientui garantuojama $8000 suma ($10 000 atėmus papildomą $2000 sumą).
        - 2 ketvirtyje registruojate pardavimus, sąlygojančius $5000 vertės autorinius honorarus.
        - Sistema nustato $3000 mokėjimą (garantiniai $8000 atėmus $5000 sumokėtus autorinius mokesčius).
        - Jei parinktis **Kaupiamoji garantija** nustatyta į *Ne*, visa $10 000 suma bus garantuota kiekvieną ketvirtį. Ši garantija atitinka siūlomą $5000 mokėjimą 2 ketvirtyje (garantiniai $10 000 atėmus $5000 apmokėtus autorinius honorarus).

1. Pasirinkite **Gerai** tam, kad sukurtumėte sandorį ir uždarytumėte dialogo langą.

Ši procedūra sukuria naujo sandorio antraštės lygį. Toliau į sandorį įtrauksite eilutes.

## <a name="add-lines-to-a-deal"></a>Eilučių įtraukimas į sandorį

Sukūrę sandorį, kaip aprašyta ankstesniame skyriuje, galite jį atidaryti iš sąrašo puslapio. Tada galite pridėti eilutes, skirtas identifikuoti klientams arba tiekėjams, prekėms, skirtiesiems laikams, pagrindui ir skaičiavimo metodams. Sandoris gali turėti vieną arba kelias eilutes. Jei sandoris turi kelias eilutes, jos paprastai yra to paties tipo arba su jomis yra susieti tie patys parametrai. Kol į sandorį neįtrauksite eilučių, sandoris nieko nedarys.

1. Atidarykite atitinkamą grąžinimų sandorių sąrašo puslapį, kaip aprašyta ankstesniame skyriuje.
1. Suraskite ir atidarykite sandorį, su kuriuo norite dirbti.
1. „FastTab” **Grąžinimų valdymas** pasirinkite vieną iš toliau nurodytų mygtukų, jei norite įtraukti sandorio eilutę į tinklelį:

    - **Įtraukti eilutę** – įtraukite naują, tuščią sandorio eilutę.
    - **Kopijuoti eilutę** – jei esama sandorio eilutė yra panaši į įtraukti norimą sandorio eilutę, galite pasirinkti šį mygtuką jai kopijuoti. Naujoje sandorio eilutėje bus įtraukti visi parametrai iš susijusios grąžinimo valdymo išsamios informacijos. Tada galite redaguoti parametrus. Pavyzdžiui, įprastai atnaujinsite prekės ryšį ir grąžinimo procentą.

1. Naujo sandorio eilutėje nustatykite šiuos laukus:

    - **Grąžinimų valdymo numeris** – jei [nustatėte numeraciją](rebate-management-parameters.md) grąžinimų valdymo numeriams, šis laukas yra automatiškai nustatytas į sistemos sugeneruotą unikalųjį ID. Kitu atveju įveskite unikalųjį ID.
    - **Tipas** – eilutei taikomo sandorio tipas (*Grąžinimas* arba *Autorinis honoraras*). Reikšmė yra nukopijuojama iš antraštės ir negali būti keičiama.
    - **Aprašas** – įveskite sandorio eilutės aprašą.
    - **Įmonė** – pasirinkite įmonę (juridinį subjektą), kuriai taikoma sandorio eilutė. Apdorojimo metu vartotojai gali apdoroti tik tas sandorio eilutes, kurios priskirtos jų šiuo metu naudojamai įmonei. **Kliento grąžinimų sandorių** sąrašo puslapis pateikia kelių įmonių rodinį, pagrįstą vartotojo saugos prieiga. Tačiau jūs galite redaguoti ir apdoroti grąžinimus tik tai įmonei, kurią naudojate šiuo metu.
    - **Paskyros kodas** – pasirinkite klientų arba tiekėjų, kuriems taikoma sandorio eilutė, aprėptį:

        - *Lentelė* – sandorio eilutė taikoma konkrečiam klientui arba tiekėjui.
        - *Grupė* – sandorio eilutė taikoma klientų arba tiekėjų grupei. Daugiau informacijos, apie tai, kaip nustatyti grupes, rasite [Grąžinimų valdymo grupės](rebate-management-groups.md).
        - *Visi* – sandorio eilutė taikoma visiems klientams arba tiekėjams.

    - **Paskyros ryšys** – jei lauke **Paskyros kodas** pasirinkote *Lentelė*, pasirinktie klientą arba tiekėją, kuriam taikomas sandoris. Jei pasirinkote *Grupė*, pasirinkite klientų arba tiekėjų grupę. Jei pasirinkote *Visi*, šis laukas negalimas.
    - **Prekės kodas** – pasirinkite prekių, kurioms taikoma sandorio eilutė, aprėptį:

        - *Lentelė* – sandorio eilutė taikoma konkrečiai prekei.
        - *Grupė* – sandorio eilutė taikoma prekių grupei. Daugiau informacijos, apie tai, kaip nustatyti grupes, rasite [Grąžinimų valdymo grupės](rebate-management-groups.md).
        - *Visi* – sandorio eilutė taikoma visoms prekėms.

    - **Prekės ryšys** – jei lauke **Prekės kodas** pasirinkote *Lentelė*, pasirinktie prekę, kuriai taikoma sandorio eilutė. Jei pasirinkote *Grupė*, pasirinkite prekių grupę. Jei pasirinkote *Visi*, šis laukas negalimas.
    - **Vieneto tipas** – pasirinkite vieneto tipą, kuris taikomas sandorio eilutei (*Atsargų vienetas* arba esamo *Svorio vienetas*). Atkreipkite dėmesį, kad šis laukas senesniems įrašams gali būti tuščias. Tokiu atveju *Atsargų vieneto* vertė yra numatoma.
    - **(Atsargų valdymo parametrai)** – likusiuose sandorio eilutės laukuose nurodykite atsargų valdymo parametrų, kurie bus naudojami į sandorį įtrauktoms prekėms apibūdinti, reikšmes (pavyzdžiui, prekės dydis, spalva, stilius, vieta ir sandėlis). Norėdami įtraukti arba pašalinti dimensijas, veiksmų srityje pasirinkite **Rodyti dimensijas**.

1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Jei norite dar labiau apriboti prekių, kurioms taikoma sandorio eilutė, rinkinį, pasirinkite eilutę ir tada „FastTab” **Grąžinimų valdymas** pasirinkite **Filtruoti**, jei norite atidaryti įprastinį **Užklausos** dialogo langą.
1. Kiekvienoje jūsų įtrauktoje sandorio eilutėje nustatykite skaičiavimo ir kitą informaciją „FastTab” **Grąžinimų valdymo informacija**, kaip apibūdinta kitame skyriuje.

## <a name="add-rebate-management-details-to-a-deal-line"></a>Grąžinimų valdymo informacijos įtraukimas į sandorio eilutę

Kiekvienai jūsų sandorio eilutei turite nustatyti išsamią informaciją „FastTab” skirtuke **Grąžinimų valdymo informacija**. Pirma pasirinkite sandorio eilutę iš „FastTab” **Grąžinimų valdymas**. Tada nustatykite tos sandorio eilutės reikšmes naudodami įvairius skirtukus, esančius **Grąžinimų valdymo informacijos** „FastTab”. Toliau pateikti poskyriai aprašo, kaip naudoti kiekvieną skirtuką.

### <a name="settings-on-the-general-tab"></a>Parametrai, esantys Bendra skirtuke

Skirtukas **Bendra**, esantis „FastTab” **Grąžinimų valdymo informacija** leidžia jums nustatyti pasirinktos sandorio eilutės skaičiavimo metodą ir pagrindą. Šis nustatymas kontroliuoja tai, ar reikia minimalaus pirkimo, su sandorio eilute susijusių registravimo šablonus ir skaičiavimo informaciją. Toliau pateikiamoje lentelėje aprašomi laukai, kuriuos galima naudoti.

| Laukas | Aprašas |
|---|---|
| Skaičiavimo metodas | Pasirinkite metodą, kurį reikia naudoti, kai pasirinkta sandorio eilutė derinama su kitomis sandorio eilutėmis (*Sustabdyta*, *Kaupiamoji*, *Sumavimas* arba *Iš viso*). Šio lauko reikšmė gali turėti didelės įtakos jūsų grąžinimo skaičiavimų rezultatams. Kiekvieno metodo pilną aprašymą ir pavyzdžius, rodančius, kaip tai veikia grąžinimo skaičiavimą, rasite tolesniame šios temos skyriuje [Sandorio eilučių skaičiavimo metodai](#calc-methods). |
| Pagrindas | Pasirinkite, ar grąžinimas taikomas pagal kiekį (tai yra, bendrą nupirktų arba parduotų vienetų skaičių), ar vertę (tai yra, bendrą nupirktų arba parduotų prekių kainą). |
| Operacijos tipas | <p>Pasirinkti proceso atkarpą, kada turi įvykti skaičiavimas:</p><ul><li>*Užsakyta* – naudokite užsakytą kiekį ar reikšmę kaip skaičiavimo pagrindą.</li><li>*Pristatyta* – naudokite pristatytą kiekį ar reikšmę kaip skaičiavimo pagrindą.</li><li>*Sąskaita faktūra* – naudokite kiekį ar reikšmę, kuriems išrašyta sąskaita faktūra, kaip skaičiavimo pagrindą.</li></ul> |
| Vienetas | Jei lauke *Pagrindas* pasirinkote **Kiekis**, pasirinkite vienetą, kuriam turi būti nurodytas kiekis. |
| Minimali suma | Įveskite minimalią sumą, kuri turi būti sumokėta per tam tikrą laikotarpį. Galite įvesti neigiamą reikšmę, kad leistumėte neigiamas grąžinimo sumas, jeigu kredito pažymų skaičius viršija pardavimo per tam tikrą laikotarpį skaičių. |
| Grąžinimo mažinimo principas | Pasirinkite [grąžinimo mažinimo principą](rebate-reduction-principle.md), taikomą sandorio eilutei. |
| Varianto numeris | Jei sandorio eilutė taikoma variantų turinčiai prekei, pasirinkite variantą, kuriam taikoma sandorio eilutei. |
| Tiekėjo grąžinimų pagrindimai | <p>Šis laukas rodomas tik tiekėjo grąžinimams (tai yra, sandoriams, kurių laukas **Modulis** yra nustatytas kaip *Tiekėjas*). Pasirinkite tiekėjo grąžinimo pagrindą:</p><ul><li>*Pirkimo užsakymas* – tiekėjo gaunamas grąžinimas yra pagrįstas kiekiu arba verte pirkimo užsakyme.</li><li>*Pardavimo užsakymas* – tiekėjas gauna grąžinimą tik pardavus prekes. Grąžinimas yra pagrįstas kiekiu arba verte pardavimo užsakyme.</li></ul> |
| Kainos pagrindas | <p>Šis laukas rodomas tik tiekėjo grąžinimams (sandoriams, kurių laukas **Modulis** yra nustatytas kaip *Tiekėjas*). Jei lauke **Tiekėjo grąžinimo pagrindas** pasirinkote *Pardavimo užsakymas*, pasirinkite taikytiną kainos pagrindą:</p><ul><li><p>*FIFO* – periodinę užduotį **Skaičiuoti FIFO pirkimo kainą** reikia vykdyti, kad būtų galima apskaičiuoti grąžinimą. (Norėdami vykdyti užduotį, eikite į **Grąžinimų valdymas \> Periodinės užduotys \> Skaičiuoti FIFO pirkimo kainą**.) Pirmas ateina, pirmas išeina (FIFO) taisyklė bus naudojama skaičiuojant parduotų atsargų vertę. Tada ši vertė bus naudojama tiekėjo grąžinimams skaičiuoti. Toliau pateikiamas pavyzdys.</p><ul><li>**Parduotos atsargos:** 1000 vienetų po $3,00 už vienetą = $3000</li><li>**Dabartinė pirkimo kaina, pagrįsta FIFO:** $2,00</li><li>**Veikiantis skaičiavimas:** *Parduoti vienetai* × *Dabartinė pirkimo kaina* = 1000 × $2,00 = $2000</li></ul></li><li><p>*Naujausio pirkimo kaina* – paskutinio pirkimo operacijos vertė bus naudojama tiekėjo grąžinimams apskaičiuoti. Toliau pateikiamas pavyzdys.</p><ul><li>**Parduotos atsargos:** 1000 vienetų po $3,00 už vienetą = $3000</li><li>**Paskutinė pirkimo kaina:** $2,00</li><li>**Veikiantis skaičiavimas:** *Parduoti vienetai* × *Naujausio pirkimo kaina* = 1000 × $2,00 = $2000</li></ul></li><li><p>*Vidutinė pirkimo kaina* – svertinė vidutinė paskutinių *X* mėnesių vertė bus naudojama tiekėjo grąžinimams skaičiuoti. Jei pasirenkate šią parinktį, turite įvesti mėnesių skaičių lauke **Mėnesių skaičius** (jis yra galimas tik tada, kai laukas **Kainos pagrindas** nustatytas į *Vidutinė pirkimo kaina*). Toliau pateikiamas pavyzdys.</p><ul><li>**Parduotos atsargos:** 1000 vienetų po $3,00 už vienetą = $3000</li><li>**Vidutinė pirkimo kaina:** $2,00</li><li>**Veikiantis skaičiavimas:** *Parduoti vienetai* × *Vidutinė pirkimo kaina* = 1000 × $2,00 = $2000</li></ul></li><li><p>*Pardavimo kaina* – pardavimo kaina bus naudojama tiekėjo grąžinimams skaičiuoti. Toliau pateikiamas pavyzdys.</p><ul><li>**Parduotos atsargos:** 1000 vienetų po $3,00 už vienetą = $3000</li><li>**Vidutinė pirkimo kaina:** $2,00</li><li>**Veikiantis skaičiavimas:** *Parduoti vienetai* × *Pardavimo kaina* = 1000 × $3,00 = $3000</li></ul></li></ul> |
| Mėnesių skaičius | Šis laukas rodomas tik tiekėjo grąžinimams (sandoriams, kurių laukas **Modulis** yra nustatytas kaip *Tiekėjas*). Jei pasirinkote *Vidutinę pirkimo kainą* lauke **Kainos pagrindas**, įveskite mėnesių skaičių, kurį reikia naudoti. |
| Registravimo profilis | Pasirinkite [redagavimo šabloną](rebate-management-posting.md) taikomą pasirinktai sandorio eilutei. Šis šablonas naudojamas tik tada, kai sandorio antraštėje laukas **Derinti pagal** nustatytas į *Eilutė*. Jei laukas **Derinti pagal** nustatytas kaip *Sandoris*, visada naudojamas registravimo šablonas, nustatytas sandorio antraštėje. Jei sandorio eilutėje nenustatytas joks laukas, naudojamas registravimo šablonas, nustatytas sandorio antraštėje. |
| Registravimo šablonas garantijai | Šis laukas veikia kaip **Registravimo šablono** laukas, tačiau yra taikomas tik autoriniams honorarams. |
| Mokėjimo tipas | Sandoriui pasirinkto registravimo šablono mokėjimo tipas. |
| PVM imtinai | Pasirinkite, ar į operaciją įskaičiuoti mokesčius. Mokesčių įskaičiavimas yra svarbus tik tada, kai laukas **Pagrindas** nustatytas į *Vertė*. Sąskaitos faktūros suma bus naudojama kaip suma su mokesčiais. Jei grąžinimo skaičiavimas pagrįstas procentine dalimi, sistema padaugins grąžinimo procentą iš sumos su mokesčiais. Atkreipkite dėmesį, kad skaičiuojant naudojama pardavimo mokesčio vertė iš sandorio eilutės. |
| Įtraukti kredito pažymas | <p>Nustatykite šią parinktį į *Taip*, jei norite įtraukti kredito pažymas į grąžinimo skaičiavimą.</p><p>Jei nustatote šią parinktį į *Taip*, poveikis skiriasi, priklausomai nuo lauko **Operacijos tipas** reikšmė:</p><ul><li>Jei laukas **Operacijos tipas** nustatytas į *Sąskaita faktūra*, skaičiavimas veiks kredito pažymose. Ši konfigūracija yra įprastinė.</li><li>Jei laukas **Operacijos tipas** nustatytas į *Užsakymas*, skaičiavimas veiks pardavimo užsakymuose, turinčiuose neigiamas vertes, ir atidarytuose grąžintuose užsakymuose.</li></ul> |
| Nuolaidos suma | Nustatykite šią parinktį į *Taip* skaičiavimui pagrįsti prekės ar prekių suma su nuolaida tais atvejais, kai pateikiamos sandorio eilutės nuolaidos. |
| Tik apmokėtos sąskaitos faktūros | Nustatykite šią parinktį į *Taip*, jei norite, kad skaičiuojant būtų atsižvelgta tik į pilnai apmokėtas sąskaitas faktūras. (Kitaip tariant, grąžinimai nebus skaičiuojami iš dalies apmokėtoms sąskaitoms faktūroms.) Ši parinktis galima tik tada, kai laukas **Operacijos tipas** nustatytas į *Sąskaita faktūra*. |
| Įtraukti laisvos formos sąskaitą faktūrą | Nustatykite šią parinktį į *Taip*, jei norite įtraukti laisvos formos sąskaitas faktūras į skaičiavimą. Laisvos formos sąskaitas faktūras galima įtraukti tik toms sandorio eilutėms, kuriose laukas **Prekės kodas** nustatytas į *Visi*. |
| Įtraukti sudengimo nuolaidą | Nustatykite šią parinktį į *Taip*, jei norite sumažinti grąžinimą pagal pirmąją sudengimo nuolaidą. Laikoma, kad organizacija paims pirmąją sudengimo nuolaidą. Nustatykite šią parinktį į *Ne*, jei norite įgalinti sudengimo nuolaidą vėlesniam naudojimui. |
| Dokumento pastabos | Įveskite pastabas, kurios turėtų būti naudojamos kaip operacijos tekstas grąžinimų operacijų žurnalo eilutėse. |

### <a name="settings-on-the-dates-tab"></a>Nustatymai Datų skirtuke

Skirtuko **Datos** parametrai, esantys „FastTab” **Grąžinimų valdymo informacija** apibrėžia skirtuke **Bendra** nurodytų skaičiavimų dažnumą ir laiką Jie nustato, kaip skaičiavimai vyksta apdorojimo metu.

Šis skirtukas leidžia jums nurodyti datų diapazoną, kuriam galioja pasirinkta sandorio eilutė, ir skaičiavimo dažnį. Taip pat galite nurodyti, ar garantija turėtų būti užregistruota ir jei taip, tai kada.

Galite naudoti mygtukus įrankių juostoje, kad įtrauktumėte datos eilutes į tinklelį arba panaikintumėte jas. Jei yra kelios datos eilutės, galiojantys datų diapazonai neturėtų persidengti. Priešingu atveju, gausite klaidos pranešimą bandydami išsaugoti sandorį.

Šioje lentelėje apibūdinami kiekvienai datos eilutei galimi laukai.

| Laukas | Aprašas |
|---|---|
| Data nuo | Įveskite pirmąją datą, taikomą datos eilutei. Jei datos „nuo” ir „iki” datos yra nurodytos sandorio antraštėje, jos naudojamos kaip numatytosios reikšmės kiekvienai naujai datos eilutei. |
| Data iki | Įveskite paskutinę datą, taikomą datos eilutei. Jei datos „nuo” ir „iki” datos yra nurodytos sandorio antraštėje, jos naudojamos kaip numatytosios reikšmės kiekvienai naujai datos eilutei. |
| Per | Nurodykite, kaip dažnai reikėtų apskaičiuoti sandorio eilutę. Čia įveskite sveikąjį skaičių ir lauke **Sumuoti pagal** pasirinkite vienetą. Pavyzdžiui, norėdami atlikti skaičiavimą kas antrą savaitę, nustatykite **lauką Per** į *2*, o lauką **Skaičiuoti pagal** į *Savaitės*. |
| Skaičiuoti pagal | Pasirinkite vienetą, kuriam taikomas **Per parametras**. Pasirinkite *Egzistavimo laikotarpis*, jei norite apskaičiuoti visą sandorio eilutės egzistavimo laikotarpį. Pasirinkite *Pasirinktinį laikotarpį*, jei norite pasirinkti didžiojoje knygoje apibrėžtą laikotarpį. Tokiu atveju taip pat turite nustatyti **Laikotarpio tipo** lauką. |
| Laikotarpio tipas | Šį lauką galima naudoti nustačius lauką **Skaičiuoti pagal** į *Pasirinktinis laikotarpis*. Vertės, kurias galima pasirinkti, yra iš didžiojoje knygoje apibrėžtų laikotarpio tipų. |
| Pirma savaitės diena | Nurodykite, kaip laikotarpio savaitės yra identifikuojamos. Šį lauką galima naudoti nustačius lauką **Skaičiuoti pagal** į *Savaitės*. |
| Pareikalauti per | Nurodykite, kaip dažnai gali būti pareikalauta grąžinimo pinigų sandorio eilutei. Čia įveskite sveikąjį skaičių ir lauke **Pareikalauti pagal** pasirinkite vienetą. |
| Pareikalauti pagal | Pasirinkite vienetą, kuriam taikomas **Pareikalauti pagal** parametras. Pasirinkite *Egzistavimo laikotarpį*, jei norite leisti pareikalavimus tik vieną kartą per visą sandorio eilutės egzistavimo laikotarpį. Pasirinkite *Pasirinktinį laikotarpį*, jei norite pasirinkti didžiojoje knygoje apibrėžtą laikotarpį. Tokiu atveju taip pat turite nustatyti **Pareikalavimo laikotarpio tipo** lauką. |
| Reikalavimo laikotarpio tipas | Šį lauką galima naudoti nustačius lauką **Pareikalauti pagal** į *Pasirinktinis laikotarpis*. Vertės, kurias galima pasirinkti, yra iš didžiojoje knygoje apibrėžtų laikotarpio tipų. |
| Apdorojimas registruojant | Pasirinkite šį žymės langelį, jei registravimo metu reikia apdoroti sandorio eilutę. Ši parinktis galima tik sandorio eilutėms, kurių **Bendra** skirtuko laukas **Operacijos tipas** nustatytas į *Pristatyta* arba *Sąskaita faktūra*. Nuostata bus užregistruota sugeneravus pristatymo pažymą arba sąskaitą faktūrą. |
| Garantija per | Šis laukas taikomas tik autorinių honorarų sandoriams. Nurodykite, kaip dažnai turėtų būti skaičiuojamas autorinis honoraras parametro **Sumuoti pagal** apibrėžtu laikotarpiu. Čia įveskite sveikąjį skaičių ir lauke **Apmokėta garantija** pasirinkite mokėjimo laiką. |
| Apmokėta garantija | <p>Šis laukas taikomas tik autorinių honorarų sandoriams. Jis veikia kartu su lauku **Garantija per** apibrėžiant garantijos skaičiavimo dažnį. Pasirinkite vieną iš šių reikšmių:</p><ul><li><p>*Laikotarpio pradžia* – garantija mokama datos eilutėje apibrėžto sutarties laikotarpio pradžioje. Pirmiausia apdorojama pilna garantija. Tik garantinę sumą viršijanti autorinių honorarų vertė užregistruojama kaip autorinis honoraras. Toliau pateikiamas pavyzdys.</p><ul><li>**Garantijos minimumas:** $10 000 per du mėnesius.</li><li>**1 mėnuo:** $10 000 buvo užregistruota kaip garantija ir $0 – kaip autoriniai honorarai.</li><li>**2 mėnuo:** $2000 buvo užregistruota kaip autoriniai honorarai ir $0 – kaip garantijos.</li><li>**Veikiantis skaičiavimas:** *Likusi garantija* – *Užregistruoti autoriniai honorarai* = $0 – $2000 = -$2,000.</li></ul><p>Kadangi būtina atlikti $2000 mokėjimą, sukuriamas žurnalas, skirtas $2,000 vertei.</p><p>**Pastaba:** garantija turėtų būti apskaičiuota ir užregistruota kartu su pirmojo laikotarpio atskaitymų nuostata.</p></li><li><p>*Laikotarpio pabaiga* – garantija nėra mokama iki atskaitymų sutarties pabaigos, kaip nurodyta datos eilutėje. Toliau pateikiamas pavyzdys.</p><ul><li>**Garantijos minimumas:** $10 000 per du mėnesius.</li><li>**1 mėnuo:** $5000 buvo užregistruota kaip autorinis atlyginimas ir sukurtas žurnalas.</li><li>**2 mėnuo:** $7000 buvo užregistruota kaip autorinis atlyginimas ir sukurtas žurnalas.</li><li>**Veikiantis skaičiavimas:** kadangi autoriniai atlyginimai viršija garantijos sumą, $0 užregistruojama garantijoje.</li></ul><p>**Pastaba:** garantija turėtų būti apskaičiuota ir užregistruota tik kartu su galutinio laikotarpio atskaitymų ir grąžinimų operacijomis.</p></li></ul> |
| Minimali garantija | Šis laukas taikomas tik autorinių honorarų sandoriams. Įvesti minimalią garantinę autorinio honoraro sumą valiuta, nustatyta sandorio antraštėje. |

### <a name="settings-on-the-lines-tab"></a>Nustatymai eilučių skirtuke

Skirtukas **Eilutės**, esantis „FastTab” **Grąžinimų valdymo informacija** leidžia jums apibrėžti pasirinktos sandorio eilutės skaičiavimo eilutes. Kiekviena skaičiavimo eilutė nustato kiekio ar vertės ribinės vertę ir susijusią kompensacijos sumą arba prekes. **Bendra** laukas **Pagrindas** nurodo, kuo pagrįsta kiekviena skaičiavimo eilutė: kiekiu, ar verte.

Galite naudoti mygtukus įrankių juostoje, kad įtrauktumėte skaičiavimo eilutes į tinklelį arba panaikintumėte jas. Galite turėti tiek skaičiavimo eilučių, kiek norite. Tačiau, jei yra kelios skaičiavimo eilutės, „iki” ir „nuo” kiekio ar verčių diapazonai neturėtų persidengti.

Šioje lentelėje apibūdinami kiekvienai skaičiavimo eilutei galimi laukai.

| Laukas | Aprašas |
|---|---|
| Nuo kiekio/vertės | Įveskite minimalų kiekį ar vertę, taikomą skaičiavimo eilutei. |
| Iki kiekio/vertės | Įveskite maksimalų kiekį ar vertę, taikomą skaičiavimo eilutei. |
| Grąžinimų valdymo metodas | <p>Šis laukas galimas tik tiems sandoriams, kurių antraštės laukas **Grąžinimo išvestis** nustatyta į *Finansinė*. Pasirinkti metodą grąžinimui apskaičiuoti:</p><ul><li>*Fiksuotas* – eilutei naudojama fiksuota kainos suma.</li><li>*Procentas* – naudojamas pardavimo sumos procentinė dalis.</li><li>*Tarifas* – naudojama fiksuotos užsakymo kainos suma.</li></ul><p>**Svarbu:** primygtinai rekomenduojame naudoti tą patį metodą kiekvienai skirtuko **Eilutės** skaičiavimo eilutei Jei reikia naujo metodo, sukurkite naują sandorio eilutę. Atminkite, kad galite naudoti „FastTab” **Grąžinimų valdymas** mygtuką **Kopijuoti eilutę**, kad sukurtumėte naują sandorio eilutę iš esamos sandorio eilutės.</p><p>**Pastaba:** jei laukas **Grąžinimo išeiga** nustatytas kaip *Prekė*, šis laukas visada nustatomas į *Fiksuotas*. Daugiau informacijos apie tai, kaip nurodyti prekes, rasite tekste, esančiame po šia lentelėje. |
| Grąžinimų valdymo suma | Šis laukas galimas tik tiems sandoriams, kurių antraštės **Grąžinimo išvestis** nustatyta į *Finansinė*. Įveskite sumą, kuri turėtų būti naudojama grąžinimui apskaičiuoti pagal metodą, kurį pasirinkote **Grąžinimų valdymo metodo** lauke. |

Kaip buvo minėta ankstesnėje lentelėje, sandoriams, kurių laukas **Grąžinimo išeiga** antraštėje buvo nustatytas į *Prekė*, turite nurodyti prekes, kurios bus pateiktos kiekvienai skirtuko **Eilutės** skaičiavimo eilutei Norėdami nurodyti prekes, atlikite šiuos veiksmus.

1. Skirtuke **Eilutės** sukurkite reikiamą skaičiavimo eilutę, jei jos nėra, ir pasirinkite ją.
1. Jei sandoris nebuvo įrašytas nuo tada, kai sukūrėte skaičiavimo eilutę, veiksmų srityje pasirinkite **Įrašyti**.
1. Skirtuke **Eilutės** pasirinkite **Prekės**.
1. Puslapyje **Prekės** naudokite veiksmų srities mygtukus, kad įtrauktumėte prekes į tinklelį arba iš jo pašalintumėte, jeigu reikia. Kiekvienai eilutei nustatykite šiuos laukus:

    - **Prekės numeris** – pasirinkite prekę, kuri bus pateikta.
    - **(Kitos dimensijos)** – jei prekei apibrėžti reikia daugiau dimensijų (pavyzdžiui, prekės konfigūracija, dydis, spalva, stilius, vieta ar sandėlis), nurodykite jas. Norėdami įtraukti arba pašalinti galimas dimensijas, veiksmų srityje pasirinkite **Rodyti dimensijas**.
    - **Kiekis** – įveskite kiekį, kuris bus pateiktas pasiekus pasirinktos skaičiavimo eilutės ribinę vertę.
    - **Vienetas** – pasirinkite vienetą, kuriuo nurodoma **Kiekio** vertė.
    - **Keli** – šis laukas veikia kartu su **Kiekio** lauku. Pavyzdžiui, prekės eilutėje nustatote **Kiekio** lauką į *2*, o lauką **Keli** – į *100*. Jeigu tada turite bendrą pardavimo užsakymo kiekį 150, dvi prekės bus laisvos (100 skirtos dvi).

### <a name="settings-on-the-inventory-dimensions-tab"></a>Atsargų dimensijų skirtuko parametrai

Skirtuke **Atsargų dimensijos**, esančiame „FastTab” **Grąžinimų valdymo informacija** rodomos visos galimos produkto, nurodyto pasirinktai sandorio eilutei, reikšmes. Jis apima dimensijas, kurios nėra rodomos „FastTab” **Grąžinimų valdymas**. Galite redaguoti tik tų dimensijų reikšmes, kurios taikomos pasirinktam produktui.

Galite įtraukti į daugiau dimensijų į tinklelį per **Grąžinimų valdymo** „FastTab” veiksmų srityje pasirinkdami **Rodyti dimensijas**.

## <a name="calculation-methods-for-deal-lines"></a><a name="calc-methods"></a>Sandorio eilučių skaičiavimo metodai

Kiekvieną kartą nustatydami vienos iš savo sandorio eilučių informaciją, kaip aprašyta ankstesniame skyriuje, turite pasirinkti skaičiavimo metodą tai eilutei. Šiame skyriuje paaiškinamas kiekvienas skaičiavimo metodas ir pateikiami pavyzdžiai, kaip kiekvienas metodas apskaičiuoja bendrą užsakymų ir sandorio eilučių grąžinimą. Šiuose pavyzdžiuose užsakymai ir sandorio eilutės yra identiškos. Skiriasi tik skaičiavimo metodai.

### <a name="stepped-calculation-method"></a>Žingsninis skaičiavimo metodas

Žingsniniu skaičiavimo metodu skaičiuojama nuosekliai, žingsnis po žingsnio, kai kiekviena sandorio eilutė vis daugiau prisideda prie grąžinimo, kol pasiekiamas pardavimo kiekis arba vertė. Veiksmai gali būti pagrįsti parduotų prekių kiekiu arba verte, priklausomai nuo skirtuko **Bendra** lauko **Pagrindas** parametro, esančio „FastTab” **Grąžinimų valdymo informacija**.

Pavyzdžiui, sandorio eilutė nustatyta taip, kad laukas **Skaičiavimo metodas** būtų nustatytas į *Žingsninis*, o laukas **Pagrindas** – į *Reikšmė*. Ji apima skaičiavimo eilutes, kuriose pateikiami šie grąžinimai:

- **Eilutė A:** 10 procentų iki $1000
- **Eilutė B:** 25 procentai iki $2500

Jei nupirktų ar parduotų prekių vertė yra $2000, gautas $350 vertės grąžinimas apskaičiuojamas tokiu būdu:

- **Grąžinimas (A):** *Ribinė vertė (A)* × *Procentas (A)* = $1000 × 10 procentų = $100
- **Grąžinimas (B):** (*Parduota vertė* – *Ribinė vertė (A)* ) × *Procentas (B)* = ($2000 – $1000) × 25 procentai = $250
- **Bendras grąžinimas:** *Grąžinimas (A)* + *Grąžinimas (B)* = $100 + $250 = $350

Jei laukas **Pagrindas** nustatytas kaip *Kiekis*, o ne *Vertė*, žingsninis skaičiavimo būdas veikia panašiai. Pirmasis veiksmas naudojamas nustatytam kiekiui, kol prieinama prie antro veiksmo. Tada naudojamas antrasis veiksmas naudojamas visam kiekiui aukščiau pirmojo veiksmo, kol prieinama prie trečiojo veiksmo. Tada šis procesas tęsis per visus tolesnius veiksmus.

### <a name="cumulative-calculation-method"></a>Sukauptas skaičiavimo metodas

Sukauptas skaičiavimo metodas naudoja tik vieną skaičiavimo eilutę grąžinimui apskaičiuoti. Jei sandorio eilutei galimos kelios skaičiavimo eilutės, pasiekta didžiausios vertės arba didžiausio kiekio skaičiavimo eilutė yra naudojama visam kiekiui arba vertei. Kaip ir kiti skaičiavimo metodai, kaupiamasis metodas naudoja skirtuko **Bendra** lauką **Pagrindas**, esantį „FastTab” **Grąžinimų valdymo informacija**, siekiant nustatyti, kas naudojama grąžinimų skaičiavimui – pardavimų kiekis ar vertė.

Pavyzdžiui, sandorio eilutė nustatyta taip, kad laukas **Skaičiavimo metodas** būtų nustatytas į *Sukauptas*, o laukas **Pagrindas** – į *Reikšmė*. Ji apima skaičiavimo eilutes, kuriose pateikiami šie grąžinimai:

- **Eilutė A:** 10 procentų iki $1000
- **Eilutė B:** 25 procentai iki $2500

Jei nupirktų ar parduotų prekių vertė yra $2000, skaičiavimas naudoja tik B eilutę Gautas $500 vertės grąžinimas apskaičiuojamas tokiu būdu:

- **Bendras grąžinimas** *Parduota vertė* × *Grąžinimas (B)* = $2000 × 25 procentai = $500

### <a name="rolling-calculation-method"></a>Suminis skaičiavimo metodas

Suminis skaičiavimo metodas apskaičiuoja visas įmanomas sandorio skaičiavimo eilutes. Jeigu yra kelios skaičiavimo eilutės ir daugiau negu viena jų pasiekiama, bus naudojamos visos pasiektos skaičiavimo eilutės, tačiau kiekvienai procentinei daliai taikomos viršutinės ribinės vertės. Kaip ir kiti skaičiavimo metodai, suminis metodas naudoja skirtuko **Bendra** lauką **Pagrindas**, esantį „FastTab” **Grąžinimų valdymo informacija**, siekiant nustatyti, kas naudojama grąžinimų skaičiavimui – pardavimų kiekis ar vertė.

Pavyzdžiui, sandorio eilutė nustatyta taip, kad laukas **Skaičiavimo metodas** būtų nustatytas į *Suminis*, o laukas **Pagrindas** – į *Reikšmė*. Ji apima skaičiavimo eilutes, kuriose pateikiami šie grąžinimai:

- **Eilutė A:** 10 procentų iki $1000
- **Eilutė B:** 25 procentai iki $2500

Jei nupirktų ar parduotų prekių vertė yra $2000, gautas $600 vertės grąžinimas apskaičiuojamas tokiu būdu:

- **Grąžinimas (A):** *Ribinė vertė (A)* × *Procentas (A)* = $1000 × 10 procentų = $100
- **Grąžinimas (B):** *Parduota vertė* × *Procentas (B)* = $2000 × 25 procentai = $500
- **Bendras grąžinimas:** *Grąžinimas (A)* + *Grąžinimas (B)* = $100 + $500 = $600

### <a name="total-calculation-method"></a>Bendrojo skaičiavimo metodas

Bendrojo skaičiavimo metodas naudoja visas skaičiavimo eilutes grąžinimui apskaičiuoti. Jis taiko bendrą kiekį apskaičiuoti kiekvienos pasiektos grąžinimo eilutės grąžinimą ir kiekviena grąžinimo eilutė taiko jos procentą visai sumai. Kaip ir kiti skaičiavimo metodai, bendrasis metodas naudoja skirtuko **Bendra** lauką **Pagrindas**, esantį „FastTab” **Grąžinimų valdymo informacija**, siekiant nustatyti, kas naudojama grąžinimų skaičiavimui – pardavimų kiekis ar vertė.

Pavyzdžiui, sandorio eilutė nustatyta taip, kad laukas **Skaičiavimo metodas** būtų nustatytas į *Bendrasis*, o laukas **Pagrindas** – į *Reikšmė*. Ji apima skaičiavimo eilutes, kuriose pateikiami šie grąžinimai:

- **Eilutė A:** 10 procentų iki $1000
- **Eilutė B:** 25 procentai iki $2500

Jei nupirktų ar parduotų prekių vertė yra $2000, gautas $700 vertės grąžinimas apskaičiuojamas tokiu būdu:

- **Grąžinimas (A):** *Parduota vertė* × *Procentas (A)* = $2000 × 10 procentai = $200
- **Grąžinimas (B):** *Parduota vertė* × *Procentas (B)* = $2000 × 25 procentai = $500
- **Bendras grąžinimas:** *Grąžinimas (A)* + *Grąžinimas (B)* = $200 + $500 = $700
