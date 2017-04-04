---
title: "Palūkanų tarifų nustatymas palūkanų kodui"
description: "Delspinigių koduose yra parametrų, kurie nustato, kokie delspinigiai taikomi laiku neapmokėtoms sąskaitoms ir kaip jie apskaičiuojami."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 9656718d7afbcc6d89e650ab9379900c083507fe
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-interest-rates-for-an-interest-code"></a>Palūkanų tarifų nustatymas palūkanų kodui

Delspinigių koduose yra parametrų, kurie nustato, kokie delspinigiai taikomi laiku neapmokėtoms sąskaitoms ir kaip jie apskaičiuojami.

Galite nustatyti vieną delspinigių kodą ir jį taikyti keliems klientų registravimo šablonams, atsiskaitymo kodams arba konkrečioms SF eilutėms. Pakeitus delspinigių kodo informaciją, visos kodą naudojančios funkcijos automatiškai pritaikys pakeitimus atliekant naujas operacijas. Galite nustatyti dviejų rūšių delspinigių kodo tarifus:
-   Pajamų iš delspinigių tarifai − tai įplaukos, gaunamos taikant delspinigius SF arba delspinigių pažymoms.
-   Delspinigių mokėjimo tarifai − tai yra mokestis, mokamas už kredito pažymos delspinigius.

Abu šie tarifai gali būti vienu metu naudojami tame pačiame delspinigių kode. Delspinigių tarifai gali būti grindžiami trimis skaičiavimo tipais:
-   Delspinigiai pagal procentus.
-   Delspinigiai pagal sumą.
-   Delspinigiai pagal diapazoną, tada pateikiamas procentas arba suma.

Jei delspinigiams apskaičiuoti naudojamas delspinigių kodas, kiekvienam delspinigių tarifui, galiojančiam tuo metu, kai mokėjimas viršija operacijos atlikimo terminą, sukuriama atskira delspinigių pažyma. **Pajamų** skirtukas, esantis **Delspinigių kodo** puslapyje, naudojamas nustatyti delspinigių, kuriuos gaunate juos nustatę, tarifams. Naudokite **Mokėjimų** skirtuką, kad nustatytumėte mokamų delspinigių tarifus.

## <a name="interest-rates-based-on-a-percentage"></a>Delspinigių tarifai pagal procentą
Galite nustatyti delspinigių tarifus, kurie apskaičiuoja nurodytą procentą.

-   Delspinigių suma taikoma visoms valiutoms.
-   Galima įvesti pasirinktinius delspinigių sumos limitus.
-   **Procentas** pažymėtas ** **, kad **apskaičiuoti palūkanas pagal** lauko į **nustatyti palūkanų kodus** puslapis.

Pvz., Norėdami nustatyti palūkanų kodą, kuris vertina 5 procentų palūkanų per du mėnesius, kad sąskaitos faktūros mokėjimo viršijančią bendrąją operacijos terminas, tai įveskite 2, **apskaičiuoti palūkanas kas** lauko ir pažymėti **mėnesį**.

## <a name="interest-rates-based-on-amounts"></a>Delspinigių tarifai pagal sumas
Galite nustatyti delspinigių tarifus, kurie apskaičiuoja nurodytą sumą pagal valiutą.
-   Delspinigių kode nurodoma kiekvienos valiutos delspinigių suma.
-   Galima įvesti pasirinktinius delspinigių sumos limitus.
-   ** Suma ** pasirenkamas pagal **apskaičiuoti palūkanas pagal** lauko į **nustatyti palūkanų kodus** puslapis.

Pvz., Norėdami nustatyti palūkanų kodą, kuris vertina palūkanos 25.00 kas 20 dienų, kad sąskaitos faktūros mokėjimo viršijančią bendrąją operacijos terminas, turėtumėte įvesti 20 su **apskaičiuoti palūkanas kas** lauko ir pažymėti **diena**.

## <a name="interest-rates-based-on-ranges"></a>Delspinigių tarifai pagal diapazonus
Galite nustatyti delspinigių tarifus, kurie skiriasi atsižvelgiant į pradelstą sumą, pradelstų dienų skaičių arba mėnesių skaičių.
-   Norėdami apibrėžti konkrečias kiekvienos valiutos delspinigių nuostatas, galite naudoti skirtuką **Pajamos pagal valiutą**. Čia taip pat apibrėšite diapazoną.
-   Naudokite **Diapazonų** mygtuką, kad pridėtumėte eilutes, atstojančias norimus nustatyti diapazonus. Reikšmė **Nuo** nurodo diapazono pradžią, o **Delspinigių vertės** skaičius nurodo arba procentą, arba sumą – tai priklauso nuo pasirinkties lauke **Skaičiuoti delspinigius pagal**, esančiame puslapyje **Nustatyti delspinigių kodus**.

## <a name="example-1-interest-by-range--amount"></a>1 pavyzdys: delspinigiai pagal diapazoną = suma
Nustatykite delspinigių kodą, kuris paskaičiuoja delspinigius vieną kartą kas tris mėnesius, kiek vėluojama apmokėti SF. Norite skaičiuoti delspinigius pagal procentinę delspinigių vertę, pakopiniais sumos intervalais. Delspinigių vertė bus 1 proc. už SF sumas, neviršijančias 1 000,00, 2 proc. už sumas nuo 1 001,00 iki 5 000,00 ir 3 proc. už sumas, viršijančias 5 000,00 sumas. Nustatykite delspinigių kodo lauko vertes, kaip nurodyta toliau.

| **Lauko pavadinimas**                  | **Lauko vertė** |
|---------------------------------|-----------------|
| **Palūkanų kodas**               | 3M%ByAmt        |
| **Apskaičiuoti palūkanas kas**    | 3/mėn.         |
| **Palūkanos pagal diapazoną**           | Suma          |
| **Skaičiuoti palūkanas pagal** | Procentai      |

Galite nustatyti diapazono informaciją, kaip nurodyta toliau.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 1                  |
| 1,001          | 2                  |
| 5,001          | 3                  |

 
## <a name="example-2-interest-by-range--days"></a>2 pavyzdys: delspinigiai pagal diapazoną = dienos
--------------------------------------------------

Nustatykite delspinigių kodą, kuris paskaičiuoja delspinigius vieną kartą kas 15 dienų, kiek vėluojama apmokėti SF. Norite skaičiuoti delspinigius pagal sumos delspinigių vertę, pakopiniais dienos intervalais. Delspinigių vertė bus 10,00 už 15 dienų pirmąsias 60 dienų, 15,00 už 15 dienų, kai vėluojama 61–90 d., ir 20,00 už 15 dienų, kai vėluojama daugiau nei 91 d. Nustatykite delspinigių kodo lauko vertes, kaip nurodyta toliau.

| **Lauko pavadinimas**                  | **Lauko vertė** |
|---------------------------------|-----------------|
| **Palūkanų kodas**               | 15DAmtXDay      |
| **Apskaičiuoti palūkanas kas**    | 15/dien.          |
| **Palūkanos pagal diapazoną**           | Dienos            |
| **Skaičiuoti palūkanas pagal** | Suma          |

Galite nustatyti diapazono informaciją, kaip nurodyta toliau.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 10                 |
| 61             | 15                 |
| 91             | 20                 |

 
## <a name="example-3-interest-by-range--months"></a>3 pavyzdys: delspinigiai pagal diapazoną = mėnesiai
----------------------------------------------------

Nustatykite delspinigių kodą, kuris paskaičiuoja delspinigius vieną kartą kas mėnesį, kiek vėluojama apmokėti SF. Norite skaičiuoti delspinigius pagal procentinę delspinigių vertę, pakopiniais mėnesio intervalais. Delspinigių vertė bus 1,5 proc. už mėnesį pirmuosius tris mėnesius, kiek vėluojama sumokėti, 2,0 proc. už mėnesį už kitus tris mėnesius, 2,5 proc. už kiekvieną paskesnį mėnesį (kai vėluojama daugiau nei 6 mėnesius). Nustatykite delspinigių kodo lauko vertes, kaip nurodyta toliau.

| **Lauko pavadinimas**                  | **Lauko vertė** |
|---------------------------------|-----------------|
| **Palūkanų kodas**               | 1M%ByMth        |
| **Apskaičiuoti palūkanas kas**    | 1/mėn.         |
| **Palūkanos pagal diapazoną**           | Mėnesiai          |
| **Skaičiuoti palūkanas pagal** | Procentai      |

Galite nustatyti diapazono informaciją, kaip nurodyta toliau.

| **From value** | **Interest value** |
|----------------|--------------------|
| 0              | 1.5                |
| 4              | 2                  |
| 7              | 2,5                |

## <a name="new-versions"></a>Naujos versijos
Delspinigių kodai turi galiojimo datą. Jei norite modifikuoti delspinigių tarifą, galite sukurti **naują versiją**, kuri galiotų nuo būsimos datos.

Norėdami peržiūrėti skirtingas versijas, galite naudoti meniu pasirinktį **Taikymo pradžios data** ir pasirinkti galutinę datą. Taip pat galite pasirinkti **Rodyti visus įrašus**, kad puslapyje matytumėte visus delspinigių kodus.


