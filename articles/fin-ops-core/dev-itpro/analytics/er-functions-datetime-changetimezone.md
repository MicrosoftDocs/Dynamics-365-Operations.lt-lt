---
title: CHANGETIMEZONE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) CHANGETIMEZONE funkcija.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 48e96cfbc19503daf6a20363c4520c765f11a249
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647947"
---
# <a name="changetimezone-er-function"></a>CHANGETIMEZONE ER funkcija

[!include [banner](../includes/banner.md)]

`CHANGETIMEZONE` funkcija grąžina *[DateTime](er-formula-supported-data-types-primitive.md#datetime)* vertę koordinuotame visuotiniame laike (Pagal Grinvičo vidurdienį \[GMT\]), kuris yra pakeistas iš duotos datos ar laiko vertės vienoje laiko juostoje į kitos laiko juostos datą ir laiką. 

## <a name="syntax"></a>Sintaksė

```vb
CHANGETIMEZONE (datetime, base time zone, target time zone)
```

## <a name="arguments"></a>Argumentai

`datetime`: *DateTime*

Data / laiko vertė Universaliojo laiko laiko zonoje, nurodanti konvertuotiinę datos / laiko vertę.

`base time zone`: *[Eilutė](er-formula-supported-data-types-primitive.md#string)*

Laiko juostos pavadinimas, į kurį prieš konvertavimą perkeliama duota datos/laiko vertė.

`target time zone`: *Eilutė*

Laiko juostos pavadinimas, į kurį prieš konvertavimą perkeliama duota datos/laiko vertė.

## <a name="return-values"></a>Grįžimo vertės

*DateTime*

Gauta datos/laiko vertė universaliojo laiko zonoje.

## <a name="usage-notes"></a>Naudojimo pastabos

Norėdami nurodyti šaltinio ir paskirties laiko juostas, galite naudoti laiko zonų pavadinimus, kuriuos pateikia interneto [priskirtų](https://data.iana.org/time-zones/releases/) pagal [ interneto priskirtų numerių institucija (DNS)](https://www.iana.org/) arba [palaiko](/windows-hardware/manufacture/desktop/default-time-zones) pagal „Microsoft Windows“.

Apdorojimo metu išimtis „Laiko juostos '\<time zone name\>' nėra" pateikiama, jei pateiktas pavadinimas nerastas VZ., sąraše arba „Windows“ registre.

Laiko juostoms, kuriose laikomasi vasaros laiko, konvertavimas atsižvelgia į Universaliojo laiko vasaros laiko korespondentinę sąskaitą. Naujausia turima informacija apie šį korespondentinę sąskaitą naudojama konvertavimo metu.

## <a name="example-1"></a>1 pavyzdys

Šiame pavyzdyje naudojami „Windows" laiko juostų pavadinimai.

Konfigūruojate **Apskaičiuotojo lauko** tipo duomenų šaltinį **DSX**. Jame yra toliau nurodyta sąvoka.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "E. Europe Standard Time", "Hawaiian Standard Time"), "O")
)
```

Jei konfigūruojate apskaičiuoto lauko tipo **DSY** duomenų šaltinį **Apskaičiuotas laukas** tipas `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, **DSX** duomenų šaltinis grąžina tekstą **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Šis tekstas rodo, kad laiko skirtumas tarp dviejų birželio 1 d. pateiktos laiko juostų yra didesnis nei 24 valandos. Todėl konvertuota data / laikas yra viena diena ankstesnė už nurodytą datos / laiko vertę, nes pagrindinė laiko juosta yra už tikslinės laiko zonos ribų.

Jei konfigūruojate apskaičiuoto lauko tipo **DSY** duomenų šaltinį **Apskaičiuotas laukas** tipas `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, **DSX** duomenų šaltinis grąžina tekstą **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Šis tekstas rodo, kad laiko skirtumas tarp dviejų gruodžio 1 d. pateiktos laiko juostų yra mažesnis nei 24 valandos. Todėl konvertuota data / laikas lygus pateiktai datos / laiko vertei.

> [!NOTE]
> Ta pati išraiška pateikia skirtingus nukrypimus tarp pateiktos ir konvertuotos datos / laiko verčių tai pačiai laiko juostų porai, nes nurodytą datą / laiką laikomasi skirtingos Universaliojo laiko vasaros laiko poslinkio vertės.

## <a name="example-2"></a>2 pavyzdys

Šiame pavyzdyje naudojami „IANA" laiko juostų pavadinimai.

Konfigūruojate **Apskaičiuotojo lauko** tipo duomenų šaltinį **DSX**. Jame yra toliau nurodyta sąvoka.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "Europe/Athens", "US/Hawaii"), "O")
)
```

Jei konfigūruojate apskaičiuoto lauko tipo **DSY** duomenų šaltinį **Apskaičiuotas laukas** tipas `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, **DSX** duomenų šaltinis grąžina tekstą **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Šis tekstas rodo, kad laiko skirtumas tarp dviejų birželio 1 d. pateiktos laiko juostų yra didesnis nei 24 valandos. Todėl konvertuota data / laikas yra viena diena ankstesnė už nurodytą datos / laiko vertę, nes pagrindinė laiko juosta yra už tikslinės laiko zonos ribų.

Jei konfigūruojate apskaičiuoto lauko tipo **DSY** duomenų šaltinį **Apskaičiuotas laukas** tipas `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, **DSX** duomenų šaltinis grąžina tekstą **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Šis tekstas rodo, kad laiko skirtumas tarp dviejų gruodžio 1 d. pateiktos laiko juostų yra mažesnis nei 24 valandos. Todėl konvertuota data / laikas lygus pateiktai datos / laiko vertei.

## <a name="example-3"></a>3 pavyzdys

Konfigūruojate **Apskaičiuotojo lauko** tipo duomenų šaltinį **DSX**. Jame yra toliau nurodyta sąvoka.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "US/Hawaii", "Europe/Athens"), "O")
)
```

Jei konfigūruojate apskaičiuoto lauko tipo **DSY** duomenų šaltinį **Apskaičiuotas laukas** tipas `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, **DSX** duomenų šaltinis grąžina tekstą **2021-06-01T12:55:00.0000000+00:00 -> 2021-06-02T01:55:00.0000000+00:00**. Šis tekstas rodo, kad laiko skirtumas tarp dviejų birželio 1 d. pateiktos laiko juostų yra didesnis nei 24 valandos. Todėl konvertuota data / laikas yra viena diena vėlesnė už nurodytą datos / laiko vertę, nes pagrindinė laiko juosta yra už tikslinės pagrindinio zonos ribų.

## <a name="example-4"></a>4 pavyzdys

Galite gauti datos / laiko antspaudą iš išorinio šaltinio kaip tekstą, kuriame nėra laiko juostos informacijos. Tačiau galite žinoti laiko juostą, kuriuo operuoja šaltinis. Pavyzdžiui, gaunate datos/laiko antspaudą **01/12/2021 12:55:00** iš aptarnavimo, kuris operuoja Ispanijoje. Norėdami tinkamai įrašyti šią datos /laiko vertę į duomenų bazę, atlikite šį konvertavimą:

- Sukonfigūruokite **DSY** duomenų šaltinio **Apskaičiuoto lauko** tipo konvertavimas datos ar laiko juostos iš teksto į Koordinuoto universalaus laiko datos ar laiko vertę.

    `DATETIMEVALUE ("01/12/2021 12:55:00", "dd/MM/yyyy HH:mm:ss", "ES")`

- Sukonfigūruokite **DSX** duomenų šaltinį **Apskaičiuota laiko** tipo keitimą į konvertuotą datą ar laiko vertę į Koordinuotą universalų laiką kaip datos ar laiko vertės laiko išorinio šaltinio juostą.

    `CHANGETIMEZONE(DSY, "Romance Standard Time", "GMT Standard Time")`

> [!NOTE]
> Kai naudojate datos/laiko konvertavimo funkciją, žinokite, kad bet kokia datos / laiko vertė duomenų bazėje saugoma kaip vertė universaliojo `CHANGETIMEZONE` laiko zonoje. Prieš tai, kai šią vertę bus galima pateikti programos puslapiuose, ji transformuojama. Pakeitimas taikomas laiko juostai, kuri nustatoma kaip pageidaujama šiuo metu [prisijungusio](../../fin-ops/organization-administration/tasks/set-users-preferred-time-zone.md) programos vartotojo zona.

## <a name="additional-resources"></a>Papildomi ištekliai

[Datos ir laiko funkcijos](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
