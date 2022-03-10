---
title: Darbo užsakymų ciklo būsenos
description: Šioje temoje paaiškinamos darbo užsakymų ciklo būsenos modulyje Turto valdymas.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderLifecycleState, EntAssetWorkOrderLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fa0980438ec629ef7ae6bf711d5ae87efca131e6ab86dfcaa1f17d953725147a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768671"
---
# <a name="work-order-lifecycle-states"></a>Darbo užsakymų ciklo būsenos


[!include [banner](../../includes/banner.md)]

 

Darbo užsakymų ciklo būsenos yra būsenos, kurias gali pereiti darbo užsakymas. Pavyzdžiui, **Sukurtas**, **Suplanuotas**, **Vykdomas** ir **Baigtas**. Darbo užsakymų ciklo būsenas galima atnaujinti patiems arba jos gali būti naujinamos automatiškai (pavyzdžiui, planuojant darbo užsakymus).

Reikiamas darbo užsakymų ciklo būsenas būtina pridėti prie atitinkamų projekto etapų puslapyje **Projektų valdymo ir apskaitos parametrai** (**Projektų valdymas ir apskaita** \> **Projektų valdymo ir apskaitos parametrai**). Pirmiausia reikia nustatyti projekto etapus modulyje Projektų valdymas ir apskaita. Tada modulyje Turto valdymas nustatomos darbo užsakymų ciklo būsenos ir darbo užsakymų ciklo modeliai.

Toliau pateiktoje lentelėje aprašomos puslapio **Darbo užsakymo ciklo būsena** (**Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Ciklų būsenos**) „FastTab“ konteinerio **Bendra** skyrių **Darbo užsakymas** ir **Grafikas** parinktys.

![Darbo užsakymo ciklo būsenos puslapis.](media/09-setup-for-work-orders.png)

| Parinkties pavadinimas                   | Aprašas |
|-------------------------------|-------------|
| Aktyvi                        | Šią parinktį nustatykite kaip **Taip**, jei, būdamas šios ciklo būsenos, darbo užsakymas turi būti aktyvus. |
| Įtraukti eilutę                      | Šią parinktį nustatykite kaip **Taip**, jei į šios ciklo būsenos darbo užsakymą galima įtraukti darbo užsakymo užduočių. |
| Naikinti                        | Šią parinktį nustatykite kaip **Taip**, jei šios ciklo būsenos darbo užsakymą galima panaikinti. |
| Naikinti eilutę                   | Šią parinktį nustatykite kaip **Taip**, jei šios ciklo būsenos darbo užsakyme galima panaikinti darbo užsakymo užduotis. |
| Leisti planuoti              | Šią parinktį nustatykite kaip **Taip**, jei šios ciklo būsenos darbo užsakymą galima suplanuoti. |
| Nustatyti faktinį pradžios laiką              | Šią parinktį nustatykite kaip **Taip**, jei, darbo užsakymo ciklo būseną atnaujinus į šią, vartotojas turi būti paragintas pasirinkti faktinę darbo užsakymo pradžios datą. |
| Nustatyti faktinį pabaigos laiką                | Šią parinktį nustatykite kaip **Taip**, jei, darbo užsakymo ciklo būseną atnaujinus į šią, vartotojas turi būti paragintas pasirinkti faktinę darbo užsakymo pabaigos datą. |
| Registruoti žurnalus                 | Šią parinktį nustatykite kaip **Taip**, jei, darbo užsakymo ciklo būseną atnaujinus į šią, turi būti automatiškai registruojami darbo užsakymo žurnalai. Jei registruojant žurnalus įvyksta klaida, parodomas pranešimas ir darbo užsakymo ciklo būsenos naujinimas atšaukiamas. Norėdami peržiūrėti darbo užsakymo žurnalų eilutes, pasirinkite **Turto valdymas** \> **Įprasta** \> **Darbo užsakymai** \> **Visi darbo užsakymai**, **Aktyvūs darbo užsakymai** arba **Mano aktyvūs darbo užsakymai**, sąraše pasirinkite darbo užsakymą, tada – **Žurnalai**. Ši automatinio darbo užsakymų žurnalų registravimo esant konkrečiai ciklo būsenai sąranka yra tokia pati, kaip puslapyje **Darbo užsakymų žurnalai** pasirinkus **Registruoti žurnalus**.<p>**Pastaba.** Jei šią parinktį nustatote kaip **Taip**, žurnalai automatiškai registruojami, jei nenustatyta jokia patvirtinimo darbo eiga. Jei jūsų įmonė naudoją žurnalų tvirtinimo sąranką, sukonfigūruotą puslapyje **Žurnalų tvirtinimas** (**Projektų valdymas ir apskaita** \> **Sąranka** \> **Žurnalai** \> **Žurnalų tvirtinimas**), vadovas ar klerkas turi patikrinti ir registruoti sunaudojimo registracijas.</p> |
| Tvarkyti prižiūrimo turto kontrolinį sąrašą | Šią parinktį nustatykite kaip **Taip**, jei, darbo užsakymo ciklo būseną atnaujinus į šią, turi būti apdoroti visi pridėti prižiūrimo turto kontroliniai sąrašai. Juos apdorojant, registruojamos visos prižiūrimo turto kontroliniame sąraše atliktos skaitiklių registracijos ir įvertinamas viso prižiūrimo turto kontrolinio sąrašo rezultatas. Įvertinamos prižiūrimo turto kontrolinio sąrašo eilutės, kuriose yra rezultatų **Pavyko** ir **Nepavyko** – jei nepavyksta sėkmingai įvertinti bent vienos eilutės, visas prižiūrimo turto kontrolinis sąrašas modulyje Turto valdymas pažymimas kaip **Nepavyko**. |
| Parengta                         | Šią parinktį nustatykite kaip **Taip**, jei, darbo užsakymo ciklo būseną atnaujinus į šią, visų darbo užsakyme sukurtų užduočių grafiko būsena turi būti automatiškai atnaujinama į **Paruošta**. |
| Pradžios                         | Šią parinktį nustatykite kaip **Taip**, jei, darbo užsakymo ciklo būseną atnaujinus į šią, visų darbo užsakyme sukurtų užduočių grafiko būsena turi būti automatiškai atnaujinama į **Pradėta**. |
| Pabaigoje                           | Šią parinktį nustatykite kaip **Taip**, jei, darbo užsakymo ciklo būseną atnaujinus į šią, visų darbo užsakyme sukurtų užduočių grafiko būsena turi būti automatiškai atnaujinama į **Baigta**. |
| Naikinti grafiko eilutes         | Šią parinktį nustatykite kaip **Taip**, jei, darbo užsakymo ciklo būseną atnaujinus į šią, visų jau suplanuotame darbo užsakyme sukurtų užduočių planavimas turi būti panaikintas. Kitaip tariant, bus panaikintos turto, susijusio priežiūros darbuotojo ir susijusių įrankių pajėgumo registracijos. Pavyzdžiui, ši parinktis kaip **Taip** nustatoma prie darbo užsakymo ciklo būsenos pavadinimu **Numatoma**. Tada, grąžinus šią darbo užsakymo ciklo būseną (nes užsakymą reikia perplanuoti), planavimą jame galima panaikinti. |

## <a name="set-up-project-stages-and-work-order-lifecycle-states"></a>Projektų etapų ir darbo užsakymų ciklo būsenų nustatymas

1. Pasirinkite **Projektų valdymas ir apskaita** \> **Sąranka** \> **Projektų valdymo ir apskaitos parametrai**.
2. Skirtuke **Projekto etapas** prie kiekvieno norimo naudoti etapo pažymėkite kiekvieno projekto tipo, reikalingo darbo užsakymuose, žymės langelį. Projektų tipais nustatomos taisyklės apie leidžiamas finansines užduotis. Finansinių užduočių pavyzdžiai: prognozės kūrimas, įvertinimų kūrimas ir pradinių likučių kūrimas.

    > [!IMPORTANT]
    > Jei nepasirenkamas projektų tipo projekto etapas, tačiau jis naudojamas su darbo užsakymo ciklo būsena, darbo užsakymų projektai nebus tinkamai atnaujinti.

3. Puslapį **Projektų valdymo ir apskaitos parametrai** uždarykite.
4. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Ciklo būsenos**.
5. Norėdami sukurti darbo užsakymo ciklo būseną, pasirinkite **Nauja**.
6. Lauke **Ciklo būsena** įveskite ciklo būsenos ID.
7. Tada lauke **Pavadinimas** įveskite pavadinimą.

    „FastTab“ konteinerio **Išsami informacija** lauke **Ciklo modeliai** rodomas darbo užsakymų ciklo modelių, kuriuose naudojama ši ciklo būsena, skaičius.

8. „FastTab“ konteinerio **Bendra** skyriuje **Darbo užsakymas** kaip **Taip** nustatydami atitinkamas parinktis, pasirinkite funkcijas, kurios turi būti pasiekiamos su šia ciklo būsena. Norėdami peržiūrėti parinkčių aprašus, žr. pirmiau šioje temoje pateiktą lentelę.
9. Skyriaus **Projektas** lauke **Etapas** pasirinkite projekto etapą, kuris turi būti susijęs su šia ciklo būsena.
10. Skyriaus **Projektas** parinktį **Uždaryti veiklas** nustatykite kaip **Taip**, jei, darbo užsakymui esant šios ciklo būsenos, turi būti automatiškai uždaromos projekto veiklos, susijusios su kiekviena darbo užsakymo užduotimi.

    > [!NOTE]
    > Norėdami rasti su darbo užsakymo užduotimi susijusios projekto veiklos numerį, pasirinkite **Turto valdymas** \> **Įprasta** \> **Darbo užsakymai** \> **Visi darbo užsakymai**, **Aktyvūs darbo užsakymai** arba **Mano aktyvūs darbo užsakymai**. Atidarykite darbo užsakymą ir pasirinkite darbo užsakymo užduotį. Veiklos numeris rodomas „FastTab“ konteinerio **Eilutės informacija** skirtuko **Bendra** skyriaus **Projektas** lauke **Veiklos numeris**.

11. Skyriaus **Prognozė** parinktį **Kopijuoti valandų prognozę**, **Kopijuoti prekių prognozę** ir (arba) **Kopijuoti išlaidų prognozę** nustatykite kaip **Taip**, jei, darbo užsakymui esant šios ciklo būsenos, darbo užsakymo projektų prognozės turi būti automatiškai nukopijuotos į darbo užsakymo žurnalus.
12. Vieną iš skyriaus **Grafikas** parinkčių nustatykite kaip **Taip**, jei, darbo užsakymui esant šios ciklo būsenos, turi būti atnaujinama darbo užsakymo užduočių grafiko būsena. Norėdami peržiūrėti parinkčių **Parengta**, **Pradžia**, **Pabaiga** ir **Naikinti grafiko eilutes** aprašus, žr. pirmiau šioje temoje pateiktą lentelę.

    > [!NOTE]
    > Norėdami peržiūrėti grafiko eilutes, susijusias su darbo užsakymo užduotimis, pasirinkite **Turto valdymas** \> **Įprasta** \> **Darbo užsakymai** \> **Visi darbo užsakymai**, **Aktyvūs darbo užsakymai** arba **Mano aktyvūs darbo užsakymai**. Atidarykite darbo užsakymą, „FastTab“ konteineryje **Darbo užsakymo užduotys** pasirinkite darbo užsakymo užduotį – „FastTab“ konteineryje **Eilutės informacija** galite peržiūrėti susijusią informaciją. Skirtuko **Grafikas** lauke **Būsena** rodoma darbo užsakymo užduoties būsena. Lauką **Būsena** galima nustatyti kaip šias reikšmes: **Suplanuota**, **Parengta**, **Pradėta**, **Sustabdyta** ir **Baigta**.

13. Skyriaus **Priežiūros užklausos** lauke **Ciklo būsena** pasirinkite priežiūros užklausos ciklo būseną, į kurią turi būti atnaujintos susijusios priežiūros užklausos. Atnaujinama automatiškai. Tai galima atlikti, tik jei naudojamame priežiūros užklausos ciklo modelyje pasirinkta priežiūros užklausos ciklo būsena.
14. Skyriaus **Turtas** parinktį **Atnaujinti turto KS** nustatykite kaip **Taip**, jei, darbo užsakymo ciklo būseną atnaujinus į šią, visos darbo užsakyme naudojamos prekės turi būti automatiškai atnaujinamos puslapyje **Turto KS**. Šis parametras gali būti aktualus, jei, pavyzdžiui, darbo užsakymo ciklo būsena darbo užsakymą nustato kaip įvykdytą arba baigtą.
15. Skyriaus **Darbo užsakymų telkinys** parinktį **Naikinti telkinio nuorodą** nustatykite kaip **Taip**, jei šios ciklo būsenos darbo užsakymai turi būti automatiškai panaikinami darbo užsakymų telkiniuose.
16. „FastTab“ konteineryje **Tikrinti** kaip **Taip** nustatydami atitinkamas parinktis, pasirinkite tikrinimo tipus, kurie turi būti suaktyvinti su šia ciklo būsena. Tada kiekvieno pasirinkto tikrinimo tipo lauke **Tipas** pasirinkite pranešimo tipą, kuris turi būti rodomas, jei nepatikrinti privalomi laukai, susiję su tikrinimo tipu. Jei pasirenkate **Klaida**, darbo užsakymo ciklo būsenos naujinimas atšaukiamas iki tol, kol atnaujinami susiję privalomi darbo užsakymo laukai.

    - Parinktys **Prižiūrimo turto prastova**, **Prižiūrimo turto kontrolinis sąrašas**, **Gedimo požymis**, **Gedimo priežastis** ir **Gedimo šalinimo priemonė** yra susijusios su puslapio **Darbo užsakymų tipai** (**Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Darbo užsakymų tipai**) skyriaus **Privalomi** parinktimis. Norint suaktyvinti šias patikras, prie naudojamo darbo užsakymo tipo susijusias parinktis taip pat reikia nustatyti kaip **Taip**.
    - Jei ciklo būsenos, į kurią atnaujinamas darbo užsakymas, parinktis **Prižiūrimo turto kontrolinis sąrašas** yra nustatoma kaip **Taip**, patikrinama, ar kaip **Privaloma** pažymėtos prižiūrimo turto kontrolinis sąrašo eilutės užregistruotos kaip **Patikrinta** arba **Netaikoma**. Jei privalomos eilutės neužregistruotos nė vienu iš šių būdų, darbo užsakymo ciklo būseną atnaujinus į šią, rodomas informacinis, klaidos arba įspėjamasis pranešimas.
    - Jei ciklo būsenos, į kurią atnaujinamas darbo užsakymas, parinktis **Skirti kaštai** yra nustatoma kaip **Taip**, apskaičiuojama visa kiekvienos darbo užsakymo užduoties patvirtintų kaštų (tai yra, visos išlaidų, kurias juridinis subjektas įsipareigojo sumokėti, sumos), suma. Jei skirtų kaštų suma yra didesnė už 0 (nulį), rodomas pranešimas. Įtraukti kaštų skyrimo tipai pasirenkami puslapio **Projektų valdymo ir apskaitos parametrai** (**Projektų valdymas ir apskaita** \> **Sąranka** \> **Projektų valdymo ir apskaitos parametrai**) skirtuko **Kaštų valdymas** „FastTab“ konteineryje **Kaštų skyrimas**.
    - Jei ciklo būsenos, į kurią atnaujinamas darbo užsakymas, parinktis **Prižiūrimo turto prastova** yra nustatoma kaip **Taip**, patikrinama su darbo užsakymu susijusio prižiūrimo turto prastova. Jei prižiūrimo turto prastovos registracija atlikta, tačiau registracijos **Baigta** nėra, darbo užsakymo ciklo būseną atnaujinus į šią, rodomas pranešimas.
    - Jei standartinė projekto sąranka neapima visų etapų, kurių reikia nustatant modulį Turto valdymas, puslapio **Projektų valdymo ir apskaitos parametrai** skirtuke **Projekto etapas** galite sukonfigūruoti vartotojų nustatytus projekto etapus. Tolesnėje iliustracijoje rodomas puslapio **Projektų valdymo ir apskaitos parametrai** skirtukas **Projekto etapas**.

    ![Įvairių projekto tipų projekto etapų nustatymo puslapis.](media/10-setup-for-work-orders.png)

> [!NOTE]
> Jei ciklo būsena, į kurią atnaujinate darbo užsakymą, yra neaktyvi, su darbo užsakymu susiję, tačiau dar neužregistruoti žurnalai automatiškai panaikinami. Taip lengviau užtikrinti automatinį nenaudojamų duomenų išvalymą. (Ciklo būsena yra neaktyvi, jei puslapio **Darbo užsakymo ciklo būsena** „FastTab“ konteineryje **Bendra** būsenos parinktis **Aktyvi** yra nustatyta kaip **Ne**.)
>
> Tačiau, jei patys nustatote, kad darbo užsakymas būtų neaktyvus, su darbo užsakymu susiję, tačiau dar neužregistruoti žurnalai **nėra** automatiškai panaikinami. (Norėdami patys supasyvinti darbo užsakymą, pasirinkite **Turto valdymas** \> **Įprasta** \> **Darbo užsakymai** \> **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**. Atidarykite darbo užsakymą ir rodinį perjunkite į **Antraštė**. „FastTab“ konteineryje **Bendra** pasirinkite **Redaguoti**, tada parinktį **Aktyvus** nustatykite kaip **Ne**.)

## <a name="relations-among-work-order-lifecycle-models-work-order-types-and-work-order-lifecycle-states"></a>Darbo užsakymų ciklo modelių, darbo užsakymų tipų ir darbo užsakymų ciklo būsenų ryšiai

Ciklo modeliai yra susiję su darbo eigomis, o ciklo būsenos ciklo modelyje pasirenkamos eilės tvarka. Ciklo modeliai nustatomi su darbo užsakymų tipais. Darbo užsakymų tipai nustato darbo eigų ir darbo procesų dydį arba mastą. Pavyzdžiui, **Priežiūra** – standartinis darbo užsakymų tipas – gali būti susijęs su darbo užsakymo ciklo modeliu, turinčiu daug ciklo būsenų. Priešingai, gali būti naudojamas darbo užsakymų tipas **Taisomasis**, kai darbo užsakymai nesuplanuoti arba kai dėl skubios situacijos darbo užsakymo užduotis įvykdoma prieš sukuriant darbo užsakymą. Šis darbo užsakymų tipas gali būti susijęs su darbo užsakymo ciklo modeliu, turinčiu tik keletą ciklo būsenų.

Tipai naudojami todėl, nes, kai nustatomas, pavyzdžiui, darbo užsakymo ar turto tipas, automatiškai nustatomi susiję darbo procesai (ciklo būsenos). Norėdami apie tai, kaip nustatyti darbo užsakymų tipus, gauti daugiau informacijos, žr. [Darbo užsakymų tipai](../setup-for-work-orders/work-order-types.md).

> [!NOTE]
> Ciklo būsenos, ciklo modeliai ir tipai be darbo užsakymų taikomi funkcinėms vietoms, turtui bei priežiūros užklausoms.

Tolesnėje iliustracijoje parodyti darbo užsakymų tipų, ciklo modelių ir ciklo būsenų ryšiai.

![Darbo užsakymo tipo puslapio palyginimas su darbo užsakymo ciklo modelių puslapiu.](media/11-setup-for-work-orders.png)

## <a name="work-order-lifecycle-models"></a>Darbo užsakymo ciklo modeliai

Sukūrus reikiamas darbo užsakymų ciklo būsenas, jas galima suskirstyti į darbo užsakymų ciklo modelius. Turite sukurti mažiausiai vieną standartinį ciklo modelį.

1. Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Ciklo modeliai**.
2. Norėdami sukurti darbo užsakymo ciklo modelį, pasirinkite **Naujas**.
3. Lauke **Ciklo modelis** įveskite ciklo modelio ID.
4. Tada lauke **Pavadinimas** įveskite pavadinimą.

    „FastTab“ konteinerio **Išsami informacija** lauke **Ciklo būsenos** rodomas šiame ciklo modelyje pasirinktų ciklo būsenų skaičius. Lauke **Darbo užsakymų tipai** rodomas darbo užsakymų tipų, su kuriais naudojamas šis ciklo modelis, skaičius.

5. „FastTab“ skirtuke **Ciklo būsenos** pasirinkite ciklo būsenas, kurios turėtų būti įtrauktos į šį ciklo modelį:

    - Norėdami įtraukti ciklo būseną į ciklo modelį, pasirinkite ją **Likusios ciklo būsenos** skyriuje, o tada pasirinkite dešinės rodyklės mygtuką ![Rodyklė dešinėn.](media/12-setup-for-work-orders.png) jos perkėlimui į **Pasirinktos ciklo būsenos** skyrių.
    - Norėdami į ciklo modelį įtraukti visas galimas ciklo būsenas, pasirinkite mygtuką **Pasirinkti visus galimus etapus** ![Pasirinkti visus galimus etapus.](media/13-setup-for-work-orders.png). Visos ciklo būsenos bus perkeltos į skyrių **Pasirinktos ciklo būsenos**.
    - Norėdami pašalinti ciklo būseną iš ciklo modelio, pasirinkite ją **Pasirinktos ciklo būsenos** skyriuje, o tada pasirinkite kairės rodyklės mygtuką ![Rodyklė kairėn.](media/14-setup-for-work-orders.png) jos perkėlimui į **Likusios ciklo būsenos** skyrių.

6. Pasirinkę **Ciklo būsenų naujinimai** nustatykite ciklo būsenas, kurios gali sekti pasirinktą ciklo būseną.
7. „FastTab“ **Naujinimai** lauke **Suplanuota būsena** pasirinkite ciklo būseną, kuri visada turi būti parenkama suplanuotam darbo užsakymui, neatsižvelgiant į ankstesnę jo ciklo būseną.
8. Lauke **Nesuplanuota ciklo būsena** pasirinkite ciklo būseną, kuri visada turi būti parenkama darbo užsakymui, jei jo planavimas yra panaikinamas.
9. Darbo užsakymo ciklo modelį įrašykite.

![Darbo užsakymo ciklo modelių puslapis.](media/15-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]