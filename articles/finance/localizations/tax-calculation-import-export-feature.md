---
title: Mokesčių skaičiavimo importavimas ir eksportavimas
description: Šiame straipsnyje pateikiama informacija apie mokesčių skaičiavimo tarnybos importavimo ir eksportavimo funkciją.
author: Kai-Cloud
ms.date: 11/22/2021
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
ms.openlocfilehash: 9daee683763d7cb0eb9573497eb4e20cba9b1863
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855179"
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
