---
title: Nuomos nutraukimo pasiūlymas
description: Šioje temoje paaiškinama, kaip siūlyti nuomos nutraukimą.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseTerminateLeaseListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 6b32f9e8f80827e04269ac8cb6a4fbb5a13af8bc
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881113"
---
# <a name="propose-a-lease-for-termination"></a>Siūlyti nuomos nutraukimą

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Jei nuoma baigiasi anksti, turto nuoma gal įrašyti pabaigos žurnalo įrašą siekiant nurašyti nuomos įsipareigojimus, teisę naudoti (ROU) turtą ir sukauptą nusidėvėjimą bei registruoti pajamas ar nuostolius. Ankstyvas nutraukimo procesas užbaigia nuomą ir su ja susietus žurnalus. Jis neužbaigia atskirų nuomos žurnalų. Ši tema aprašo funkcijas, kurios leidžia jums siūlyti nuomos nutraukimą ir apdoroti nuomos pabaigimo žurnalo objektą.

Jei nuoma nėra klasifikuojama kaip atidėtos nuomos derybos ir nėra susietos su ilgalaikiu turtu, turto nuoma sukuria tolesnį nutraukimo žurnalo įrašą.

| Operacija                           | Debetas (Dr.) | Kreditas (Kr.) |
|---------------------------------------|-------------|--------------|
| Dr. nuomos įsipareigojimai                   | X           |              |
| Dr. sukauptas nusidėvėjimas          | X           |              |
| Dr. pelnas (nuostoliai) iš nuomos keitimo | X           |              |
| Cr. nuomojamas turtas                       |             | X            |
| Cr. pelnas (nuostoliai) iš nuomos keitimo |             | X            |

Jei nuomos registras yra klasifikuojamas kaip atidėtas nuomos žurnalas, įrašas nurašo atidėtos nuomos balansą prieš nuomos pabaigą į pelno ar nuostolių sąskaitą, kaip parodyta čia.

| Operacija                           | Debetas (Dr.) | Kreditas (Kr.) | 
|---------------------------------------|-------------|--------------|
| Dr. Atidėta nuoma                     | X           |              |
| Cr. pelnas (nuostoliai) iš nuomos keitimo |             | X            |
| Cr. Atidėta nuoma                     |             | X            |
| Dr. pelnas (nuostoliai) iš nuomos keitimo | X           |              |

Jei nuomos žurnalas yra susietas su ilgalaikiu turtu, ROU turtas yra apskaičiuojamas ilgalaikiam turtui. Tokia apskaita apima apskaitą dėl ankstyvų nutraukimų. Turto nuoma sukuria tolesnį žurnalo įrašą siekiant nurašyti nuomos teises.

| Operacija                           | Debetas (Dr.) | Kreditas (Kr.) |
|---------------------------------------|-------------|--------------|
| Dr. nuomos įsipareigojimai                   | X           |              |
| Cr. pelnas (nuostoliai) iš nuomos keitimo |             | X            |

Dėl informacijos apie tinkamą būdą talpinti ROU turtą, žr. [Talpinti ilgalaikį turtą kaip nusidėvėjusį](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).

## <a name="propose-a-lease-for-termination"></a>Siūlyti nuomos nutraukimą

1. Eikite į nuomą, kuri turi pasibaigti ir tuomet veiksmų juostoje rinkitės **Siūlymas nutraukti**.

    > [!NOTE]
    > Mygtukas **Nutraukimo siūlymas** yra neprieinamas, jei esama kokių nors nepublikuotų žurnalo įrašų pagal bet kokį žurnalą. Prieš tai, kai galite baigti nuomą, turite publikuoti ir panaikinti visus žurnalo įrašus, kurie buvo sukurti pagal nuomą.

2. Pasirodžiusiame teksto laukelyje nustatykite **Įsigaliojimo datą** ir **Publikavimo datos** laukelius nutraukimo žurnalo įrašui.
3. Rinkitės **Nutraukimo pasiūlymas** siekiant pasiūlyti nuomą nutraukti.
4. Rinkitės **Publikuoti nuomos nutraukimą** siekiant automatiškai publikuoti nutrauktos nuomos žurnalo įrašą.
5. Puslapyje **Nuomos nutraukimas**, rinkitės nuomos ID, kurią siūlote nutraukti, kad peržiūrėtumėte nutraukimo eilutes. Nutraukimo eilutės rodomos nešamose ROU turto vertėse, nuomos teisėse, sukauptame nusidėvėjime, atidėtoje nuomoje (jei taikoma) ir pelno bei nuostolių eilutėje, kurie turi būti patvirtinti nutraukiant nuomą.

Nuoma dabar parengta nutraukti. Vertė **Nutraukimo būsenos** laukelyje nuomos žurnale yra pakeičiama į **Parengta nutraukit**. Dabar nebegalite daugiau publikuoti žurnalo įrašų pagal nuomą ar keisti arba redaguoti jos. 

## <a name="process-leases-that-are-ready-for-termination"></a>Tvarkykite nuomą, kuri parengta nutraukti

Norėdami tvarkyti nuomas parengtas nutraukti ir publikuoti nutraukimo žurnalo įrašą, atlikite šiuos žingsnius.

1. Puslapyje **Nuomos nutraukimai** rinkitės tvarkomą nuomą ir tada **Nutraukti**.
2. Pasirodžiusiame dialogo lange pasirinkite **Gerai**.

Sistema publikuoja nutraukimo žurnalo įrašą. Laukelis **Nuomos būsena** nuomos žurnalui yra nustatyta į **Nutraukta**, o **Nutraukimo siūlymo būsenos** laukelis yra nustatytas **Užbaigtas**.

## <a name="reverse-a-lease-termination"></a>Nuomos nutraukimo grąžinimas

Norėdami grąžinti nuomos nutraukimo žurnalo įrašą ir atverti užbaigtą nuomą, atlikite šį žingsnį.

- Puslapyje **Nuomos nutraukimai** rinkitės nutraukta nuoma grąžinimui ir tada **nutraukimo grąžinimas**.

Sistema grąžina nutraukimo žurnalo įrašą. Laukelis **Nuomos būsena** nuomos žurnale yra nustatytas į **Atviras**. Nuoma neberodoma **Nuomos nutraukimų** puslapyje ir gali būti siūloma dar kartą nutraukimui.

## <a name="example-of-a-lease-termination"></a>Nuomos nutraukimo pavyzdys

Pavyzdžiui, nuoma yra susiejama su nespecializuotu turtu ir neperduoda nuosavybės teisių į turtą ir nesuteikia nuomininkui parinkties įsigyti turtą.

### <a name="setup"></a>Sąranka

Toliau esančiose lentelėse rodomos reikšmės, kurios yra nustatytos šio pavyzdžio nuomos skirtukuose **Bendra** ir **Mokėjimo grafiko eilutės**.

**Skirtukas Bendra**

| Laukas                      | Reikšmė            |
|----------------------------|------------------|
| Turto tikroji vertė    | 600,000          |
| Valiuta                   | USD              |
| Pradinės tiesioginės išlaidos       | 1000            |
| Apskaičiuota skolinimosi palūkanų norma | 7 %               |
| Sujungimo intervalas       | Kasmet         |
| Turto naudingo naudojimo laikas (mėnesiais) | 600              |
| Anuiteto tipas               | Įprastas anuitetas |
| Pradžios data          | 2019-01-01         |

**Skirtukas Mokėjimo grafiko eilutės**

| Laukas             | Reikšmė      |
|-------------------|------------|
| Pradžios data        | 2019-01-01   |
| Laikotarpio intervalas   | Mėnesinis    |
| Laikotarpiai           | 120        |
| Pabaigos data          | 2028-12-31 |
| Mokėjimo dažnumas | Kasmet   |
| Mokėjimo suma    | 10,000     |

### <a name="steps-for-terminating-the-lease"></a>Nuomos nutraukimo žingsniai

1. Sukūrę nuomą, kaip anksčiau aprašyta šioje temoje, eikite į nuomos knygą ir patvirtinkite mokėjimo grafiką. Tada registruokite pradinį pripažinimo žurnalo įrašą. Pradinis ROU turtas yra $71,235.81, o nuomos teisės turi būti $70,235.81. Šiuo atveju, nuoma buvo klasifikuojama kaip operavimo nuoma pagal Apskaitos standartų kodifikavimo temą 842 (ASC 842).
2. Vykdyti paketinio žurnalo procesą tris kartus, kad būtų imituotas trejų metų laikotarpis, skirtas nuomos mokėjimams, palūkanų išlaidoms ir nusidėvėjimo išlaidoms.
3. Kai baigsite vykdyti tris paketų darbus, eikite atgal į nuomos žurnalą ir atverkite teisių ir turto transakcijų lenteles, kad peržiūrėtumėte esamą nešančią ROU vertę turtui ir nuomos teises. Po trijų metų, teisių vertė turi būti apie $-53,893.00, o turto vertė maždaug $54,593.00.

    Praėjus trims metams, verslas ir nuomotojas kartu sutinka nutraukti nuomą. Dėl to, turite dabar nutraukti nuomą.

4. Eikite į nuomą, kuri turi pasibaigti ir tuomet veiksmų juostoje rinkitės **Siūlymas nutraukti**. 
5. Pasirodžiusiame teksto laukelyje nustatykite **Įsigaliojimo datą** ir **Publikavimo datos** laukelį, įveskite **1/1/2021**.
6. Rinkitės **Nutraukimo pasiūlymas** siekiant pasiūlyti nuomą nutraukti.

    **Nuomos nutraukimų** puslapis pasirodo ir rodo nutraukiamą nuomą.

7. Norėdami peržiūrėti nutraukimo eilutes, rinkitės nuomos ID, kurią siūlote nutraukti, kad peržiūrėtumėte nutraukimo eilutes. Nutraukimo eilutės rodo esančias nuomos vertes. Tolesnė lentelė rodo, kokios šios vertės turi būti šiuo atveju. 

    | Laukas                                                 | Reikšmė      |
    |-------------------------------------------------------|------------|
    | Esamos teisių transakcijos valiutoje vertės | $53,892.89 |
    | Teisė naudoti turtą transakcijos valiutoje            | $71,235.81 |
    | Sukauptas nusidėvėjimas transakcijos valiutoje      | $16,642.92 |
    | Pelnas (nuostoliai) transakcijos valiutoje                   | $-700.00   |

8. Norėdami publikuoti žurnalo įrašo nutraukimą, pasirinkite nuomą **Nuomos nutraukimai** rinkitės nutraukta nuoma grąžinimui ir tada **Nutraukti**.
9. Pasirodžiusiame dialogo lange pasirinkite **Gerai**.
10. Norėdami peržiūrėti nutraukimo žurnalo įrašą, kuris buvo sukurtas ir publikuotas, eikite į turto nuomos žurnalą nuomos registre. Tolesnė lentelė rodo, kaip turi atrodyti šis įrašas šiuo atveju.

    | Operacija                           | Debetas (Dr.) | Kreditas (Kr.) |
    |---------------------------------------|-------------|--------------|
    | Dr. nuomos įsipareigojimai                   | 53,892.89   |              |
    | Dr. sukauptas nusidėvėjimas          | 16,642.92   |              |
    | Dr. pelnas (nuostoliai) iš nuomos keitimo | 700.00      |              |
    | Cr. nuomojamas turtas                       |             | 71,235.81    |

11. Norėdami peržiūrėti grynąjį nutraukimo poveikį, kai ROU turtas ir nuomos teisės bus 0 (nulis), atverkite teisių ir turto operacijų lenteles.

Nuomos būsena dabar turi būti **Nutraukta**. Jokių papildomų žurnalų įrašų nebus publikuojama pagal nuomą, nebent nutraukimas bus grąžinamas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
