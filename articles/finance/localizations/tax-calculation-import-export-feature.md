---
title: Mokesčių skaičiavimo importavimas ir eksportavimas
description: Šiame straipsnyje pateikiama informacija apie mokesčių skaičiavimo tarnybos importavimo ir eksportavimo funkciją.
author: Kai-Cloud
ms.date: 10/17/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8666d4971e36279ebd2b1396de7cab37680980e6
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690239"
---
# <a name="import-and-export-tax-calculations"></a>Mokesčių skaičiavimo importavimas ir eksportavimas

Šiame straipsnyje pateikiama informacija apie mokesčių skaičiavimo tarnybos importavimo ir eksportavimo funkciją. Ši funkcija padeda užtikrinti kintamą ir efektyvią konfigūravimo patirtį.

## <a name="import-and-export-tax-codes"></a>Mokesčių kodų importavimas ir eksportavimas

### <a name="export-templates"></a>Šablonų eksportavimas

1. Prisiregistruoti [prie reguliavimo konfigūracijos tarnybos (RCS)](https://marketing.configure.global.dynamics.com/).
2. Globalizavimo **priemonių darbo srityje** pasirinkite **Funkcijos**, tada pasirinkite mokesčių skaičiavimo **išklotinę** sritį.
3. Pasirinkite esamą funkciją arba sukurkite [naują.](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs)
4. Versijų **tinklelyje** pasirinkite **Redaguoti**.
5. **Mokesčių skaičiavimo priemonės** puslapyje nustatykite [konfigūracijos versiją](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Skirtuke **Mokesčių kodai** pasirinkite **Importuoti**.
7. Pasirinkite **Eksportuoti mokesčio kodo šabloną, kad** būtų galima atsisiųsti **failą TaxCodesTemplate.zip**.
8. Išskęskite **TaxCodesTemplate.zip**. Mokesčių kodų šablonai glaudinti atskirai pagal skaičiavimo **kilmės** vertę.
9. Išskdinti **pagal Grynąją sumą.zip**, kad būtų gauti šie kableliais atskirtų verčių (CSV) failai:

    - **TaxCode.csv** – įveskite mokesčių kodus.
    - **TaxLimit.csv** – įveskite kiekvieno mokesčio kodo mokesčių limitus.
    - **TaxRate.csv** – įveskite kiekvieno mokesčio kodo mokesčių tarifus.

> [!NOTE]
> Pagal numatytuosius nustatymus mokesčių **kodo** įrašus galima rasti šablonuose. **Jei pavyzdžio** mokesčio kodas nepašalintas iš CSV failų, jis bus importuotas į funkciją.

### <a name="import-tax-codes"></a>Importuoti mokesčių kodus

Norėdami importuoti pavyzdinį mokesčio kodą **šablone** į savo mokesčių skaičiavimo priemonę, atlikite šiuos veiksmus.

1. RCS mokesčių skaičiavimo **priemonės puslapio mokesčių kodų skirtuke** **pasirinkite Importuoti** **.**
2. Pasirinkite **Naršyti**, rasti ir pasirinkti **TaxCode.csv failą**, tada tikslinių **lentelių** lauke pasirinkite **Mokesčio kodą**.
3. Pasirinkite **Gerai**, norėdami importuoti mokesčio kodą.
4. Raskite ir pasirinkite **TaxRate.csv** failą, tada tikslinių lentelių **lauke** pasirinkite Mokesčių **tarifas**.
5. Pasirinkite **Gerai,** norėdami importuoti mokesčio tarifą.
6. Raskite ir pasirinkite **TaxLimit.csv** failą, tada paskirties lentelės **lauke** pasirinkite Mokesčių **limitas**.
7. Pasirinkite **Gerai,** norėdami importuoti mokesčio limitą.

Taip pat galite tiesiogiai importuoti pašto failą, kuriame yra visi trys CSV failai. Tokiu būdu galite greitai ir lengvai baigti importavimą.

1. RCS mokesčių skaičiavimo **priemonės puslapio mokesčių kodų skirtuke** **pasirinkite Importuoti** **.**
2. Pasirinkite **Naršyti**, rasti ir pasirinkti failą **Pagal grynąją sumą.pašto**, tada pasirinkite **Gerai**.

### <a name="export-tax-codes"></a>Eksporto mokesčių kodai

1. RCS mokesčių skaičiavimo **priemonės puslapio mokesčių kodų skirtuke** **pasirinkite Eksportuoti** **.**

    Mygtukas **Eksportuoti** galimas, kai mokesčių kodų tinklelyje yra bent **vienas mokesčio** kodas.

2. Pasirinkite **Gerai**, jei norite eksportuoti visus pašto failo priemonės mokesčių kodus.

> [!NOTE]
> Norėdami importuoti mokesčių kodus į atitinkamą priemonę, naudokite eksportuotą rinkmeną kaip šabloną.

## <a name="import-and-export-applicability-rules"></a>Importo ir eksportavimo taikymo taisyklės

### <a name="export-applicability-rules"></a>Eksportavimo taikymo taisyklės

1. Prisijunkite prie [RCS](https://marketing.configure.global.dynamics.com/).
2. Globalizavimo **priemonių darbo srityje** pasirinkite **Funkcijos**, tada pasirinkite mokesčių skaičiavimo **išklotinę** sritį.
3. Pasirinkite esamą funkciją arba sukurkite [naują.](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs)
4. Versijų **tinklelyje** pasirinkite **Redaguoti**.
5. **Mokesčių skaičiavimo priemonės** puslapyje nustatykite [konfigūracijos versiją](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Skirtuke **Mokesčių grupės taikomumas** pasirinkite eilutes nustatyti **mokesčių grupės taikomumo tinklelį**.
7. Pasirinkite mygtuką **Atidaryti Microsoft Office**, tada pasirinkite mokesčių tarnybos dinaminės **taikomumo matricos**.

    [![Eksportavimo tinkamumo taisyklės Microsoft Excel mokesčių skaičiavimo priemonės puslapyje.](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. Pasirinkite **Atsisiųsti,** kad eksportuotumėte pasirinktas eilutes į darbalapį Microsoft Excel.

### <a name="import-applicability-rules"></a>Importo taikomumo taisyklės

Jūsų atsisiųstoje "Excel" darbalapyje yra **mokesčių grupės taikomumo tinklelio rinkinio** struktūra. Naujas taisykles galima tiesiogiai įtraukti į darbalapį. Kai baigiate, norėdami importuoti naujas taisykles **atgal į mokesčių grupės taikomumo tinklelį, atlikite šiuos** veiksmus.

1. Excel darbalapyje pasirinkite ir kopijuokite importuoti eilutes.
2. RCS mokesčių **skaičiavimo funkcijos puslapio mokesčių grupės taikomumas skirtuke pasirinkite Įtraukti,** **·** **kad** įterptumėte tuščią įrašą, esantį skirtuko Nustatyti mokesčių grupės taikomumą apačioje.**·**
3. Pasirinkite **Ctrl+V,** norėdami įklijuoti nukopijuotas eilutes į tinklelį.
4. Pasirinkite **Įrašyti**.

## <a name="import-feature-demo-data"></a>Importuoti funkcijos demonstracinius duomenis

Norėdami importuoti demonstracinius priemonės duomenis, atlikite šiuos veiksmus.

1. Prisijunkite prie [RCS](https://marketing.configure.global.dynamics.com/).
2. Globalizavimo **priemonių darbo srityje** pasirinkite **Funkcijos**, tada pasirinkite mokesčių skaičiavimo **išklotinę** sritį.
3. Pasirinkite **Importuoti**, tada puslapyje Importuoti **funkciją iš visuotinės saugyklos pasirinkite** Sinchronizuoti **·**. 
4. Lentelėje pasirinkite mokesčių skaičiavimo-priemonės-demonstracinių **duomenų** funkciją, tada pasirinkite **Importuoti**.
5. Pasirinkite **Rodinį**, norėdami peržiūrėti mokesčių kodus, grupes ir taikomumo taisykles, nustatytas importuotoje priemonėje.
6. Finansų įmonėje pereikite į **DEMF juridinį** subjektą, tada eikite į **Mokesčių nustatymo** \> **mokesčio** \> **konfigūracijos** \> **mokesčių skaičiavimo parametrus.**
7. Skirtuke **Bendra** pasirinkite Įgalinti **mokesčių skaičiavimo tarnybą**.
8. Priemonės nustatymo **pavadinimo lauke** pasirinkite mokesčių **skaičiavimo- priemonės - demonstracinius duomenis**.
9. Pasirinkite naujų **demonstracinių** **mokesčių kodų sudengimo** laikotarpį ir DK registravimo grupę, tada pasirinkite **Patvirtinti**.
10. Pasirinkite **Įrašyti**.

> [!NOTE]
> Mokesčių **skaičiavimo-funkcijos-demonstracinės duomenų** demonstracinės **funkcijos paremtos 40.54.234** versija, skirta **DEMF demonstraciniu** juridiniu subjektui. Įsitikinkite, kad finansų ir RCS atnaujinti į 10.0.26 arba vėlesnę versiją.
