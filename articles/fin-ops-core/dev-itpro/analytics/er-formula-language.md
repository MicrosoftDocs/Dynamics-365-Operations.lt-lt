---
title: Modulio Elektroninės ataskaitos formulių kalba
description: Šioje temoje pateikiama informacijos apie tai, kaip naudoti modulio Elektroninės ataskaitos (ER) formulių kalbą.
author: NickSelin
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 470b4fa1c8b15ae4a9e9ebef81af9e4ca107422d
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/10/2021
ms.locfileid: "6223991"
---
# <a name="electronic-reporting-formula-language"></a>Modulio Elektroninės ataskaitos formulių kalba

[!include [banner](../includes/banner.md)]

Modulyje Elektroninės ataskaitos (ER) suteikiama galingų duomenų transformavimo funkcijų. Kalba, kurią naudojant išreiškiami reikiami duomenų manipuliavimo veiksmai [ER formulių konstruktoriuje](general-electronic-reporting-formula-designer.md), panaši į „Microsoft Excel“ formulių kalbą.

## <a name="basic-syntax"></a>Pagrindinė sintaksė

ER išraiškos gali turėti bet kurį arba visus iš šių elementų:

- [Konstantos](#Constants)
- [Operatoriai](#Operators)
- [Nuorodos](#References)
- [Keliai](#Paths)
- [Funkcijos](#Functions)

## <a name="constants"></a><a name="Constants"></a>Konstantos

Kurdami išraiškas galite naudoti tekstines ir skaitines konstantas (t. y., reikšmes, kurios nėra apskaičiuojamos). Pavyzdžiui, reiškinyje `VALUE ("100") + 20` naudojama skaitinė konstanta **20** ir eilutės konstanta **100** bei pateikiama skaitinė reikšmė **120**.

ER formulių dizaino įrankis palaiko kaitos sekas. Todėl galite nurodyti, kurią išraiškos eilutę reikėtų tvarkyti kitaip. Pavyzdžiui, reiškinys `"Leo Tolstoy ""War and Peace"" Volume 1"` pateikia teksto eilutę **Leo Tolstoy "War and Peace" Volume 1**.

## <a name="operators"></a><a name="Operators"></a>Operatoriai

Toliau pateikiamoje lentelėje parodyti aritmetiniai operatoriai, kuriais galite atlikti pagrindines matematikos operacijas, pvz., sudėtį, atimtį, daugybą ir dalybą.

| Operatorius | Reikšmė               | Pavyzdys     |
|----------|-----------------------|-------------|
| +        | Priedas              | `1+2`       |
| -        | Atimtis, neigimas | `5-2`, `-1` |
| \*       | Daugyba        | `7\*8`      |
| /        | Padalinys              | `9/3`       |

Toliau pateikiamoje lentelėje parodyti palyginimo operatoriai, kurie yra palaikomi. Juos naudodami galite palyginti dvi reikšmes.

| Operatorius | Reikšmė                  | Pavyzdys      |
|----------|--------------------------|--------------|
| =        | Lygu                    | `X=Y`        |
| &gt;     | Didesnis nei             | `X>Y`        |
| &lt;     | Mažiau nei                | `X<Y`        |
| &gt;=    | Didesnis nei arba lygus | `X>=Y`       |
| &lt;=    | Mažiau nei arba lygu    | `X<=Y`       |
| &lt;&gt; | Nelygu             | `X<>Y`       |

Be to, galite naudoti ampersendą (&) kaip teksto sujungimo operatorių. Taip vieną ar kelias teksto eilutes galite sujungti ar susieti į vientisą tekstą.

| Operatorius | Reikšmė     | Pavyzdys                                               |
|----------|-------------|-------------------------------------------------------|
| &        | Sujungti | `"Nothing to print:" & " " & "no records found"`      |

### <a name="operator-precedence"></a>Operatoriaus pirmenybė

Tvarka, kuria vertinamos sudėtinės išraiškos dalys, yra svarbi. Pavyzdžiui, reiškinio `1 + 4 / 2` rezultatas skiriasi, atsižvelgiant į tai, ar pirma atliekama sudėties, ar dalybos operacija. Galite naudoti skliaustus, kad aiškiai apibrėžtumėte, kaip vertinti išraišką. Pavyzdžiui, jei norite nurodyti, kad pirma turėtų būti atliekama sudėties operacija, minėtą reiškinį galite pakeisti į `(1 + 4) / 2`. Jei aiškiai nenurodote išraiškoje atliekamų operacijų tvarkos, ji nustatoma pagal numatytąją pirmenybę, kuri priskiriama palaikomiems operatoriams. Tolesnėje lentelėje parodyta pirmenybė, priskirta kiekvienam operatoriui. Aukštesnę pirmenybę (pvz., 7) turintys operatoriai vertinami prieš žemesnę pirmenybę (pvz., 1) turinčius operatorius.

| Pirmumas | Operatoriai      | Sintaksė                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Grupavimas       | ( … )                                                                   |
| 6          | Nario prieiga  | … . …                                                                   |
| 5          | Funkcijos iškvietimas  | … ( … )                                                                 |
| 4          | Dauginamasis | … \* …<br>… / …                                                         |
| 3          | Priedas       | … + …<br>… - …                                                          |
| 2          | Palyginimas     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Atskyrimas     | … , …                                                                   |

Jei išraiškoje iš eilės yra keli operatoriai, turintys tokią pačią pirmenybę, operacijos vertinamos iš kairės į dešinę. Pavyzdžiui, reiškinys `1 + 6 / 2 \* 3 > 5` pateikia reikšmę **true**. Aiškiai nurodyti norimą išraiškų vertinimo tvarką rekomenduojame naudojant skliaustus, kad išraiškas būtų lengviau skaityti ir tvarkyti.

## <a name="references"></a><a name="References"></a>Nuorodos

Visi dabartinio ER komponento duomenų šaltiniai, kurie yra pasiekiami kuriant išraišką, gali būti naudojami kaip įvardytosios nuorodos. Dabartinis ER komponentas gali būti modelio susiejimas arba formatas. Pavyzdžiui, dabartiniame ER modelio susiejime yra duomenų šaltinis **Ataskaitos data** kuris pateikia duomenų tipo [*DataLaikas*](er-formula-supported-data-types-primitive.md#datetime) reikšmę. Norint, kad reikšmė generuojamame dokumente būtų pateikiama teisingai suformatuota, reiškinyje duomenų šaltinį galima nurodyti tokį: `DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")`.

Prieš visus nuorodos duomenų šaltinio pavadinime esančius simbolius, kurie nėra abėcėlės raidė, turi būti padėtas viengubos kabutės ženklas ('). Jei nuorodos duomenų šaltinio pavadinime yra bent vienas simbolis, kuris nėra abėcėlės raidė, pavadinimas turi būti išskiriamas viengubomis kabutėmis. Pavyzdžiui, šie neabėcėliniai simboliai gali būti skyrybos ženklai arba kiti rašytiniai simboliai. Štai keletas pavyzdžių:

- Duomenų šaltinis **Today's date & time** ER reiškinyje turi būti nurodytas taip: `'Today''s date & time'`.
- Duomenų šaltinio **Klientai** metodas **name()** ER reiškinyje turi būti nurodytas taip: `Customers.'name()'`.

Jei programos duomenų šaltinių metodai turi parametrų, šie metodai iškviečiami naudojant toliau pateiktą sintaksę.

- Jei **isLanguageRTL** metodas pagal **Sistemos** duomenų šaltinį turi **EN-US** parametrą [*Eilutė*](er-formula-supported-data-types-primitive.md#string) duomenų tipą, šis metodas bus nukreipiamas į ER išraišką kaip `System.isLanguageRTL("EN-US")`.
- Kai metodo pavadinimą sudaro tik raidiniai ir skaitiniai simboliai, kabutės neprivalomos. Tačiau jos būtinos lentelės metodo atveju, jei pavadinime yra skliaustai.

Į ER susiejimą, kuris nurodo programos klasę **Visuotinė**, įtraukus duomenų šaltinį **Sistema**, reiškinys `System.isLanguageRTL("EN-US ")` pateikia *Bulio logikos* reikšmę **FALSE**. Modifikuotas reiškinys `System.isLanguageRTL("AR")` pateikia *Bulio logikos* reikšmę **TRUE**.

Galite riboti tai, kaip reikšmės perduodamos šio tipo metodo parametrams.

- Šio tipo metodams galima perduoti tik konstantas. Konstantų reikšmės apibrėžiamos kūrimo metu.
- Tik [primityvūs](er-formula-supported-data-types-primitive.md) parametrai palaiko tik nesudėtingus (pagrindinius) duomenų tipus. Nesudėtingi duomenų tipai yra *Sveikasis skaičius*, *Realusis skaičius*, *Bulio logika* ir *Eilutė*.

## <a name="paths"></a><a name="Paths"></a>Keliai

Kai išraiška nurodo susistemintų duomenų šaltinį, galite naudoti kelio aprašą, kad pasirinktumėte konkretų nesudėtingą duomenų šaltinio elementą. Taško simbolis (.) naudojamas atskiriant atskirus susistemintų duomenų šaltinio elementus. Pavyzdžiui, dabartiniame ER modelio susiejime yra duomenų šaltinis **InvoiceTransactions**, kuris pateikia įrašų sąrašą. **InvoiceTransactions** įrašo struktūroje yra laukai **AmountDebit** ir **AmountCredit**, kurie abu pateikia skaitines reikšmes. Todėl SF sumai skaičiuoti galite sukurti tokį reiškinį: `InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit`. Šio reiškinio konstrukcija `InvoiceTransactions.AmountDebit` yra kelias, kurį naudojant pasiekiamas tipo *Įrašų sąrašas* duomenų šaltinio **InvoiceTransactions** laukas **AmountDebit**.

### <a name="relative-path"></a>Santykinis kelias

Jei susistemintų duomenų šaltinio kelias prasideda ženklu „@“, šis kelias yra santykinis. Ženklas „@“ rodomas vietoj likusios naudojamos hierarchinės medžio struktūros absoliučiojo kelio dalies. Toliau pateikiamoje iliustracijoje vaizduojamas pavyzdys. Čia absoliutusis kelias `Ledger.'accountingCurrency()'` nurodo, kad apskaitos valiutos reikšmė iš duomenų šaltinio **Didžioji knyga** įvedama į duomenų modelio lauką **AccountingCurrency**.

![Absoliučiojo kelio pavyzdys ER modelio susiejimo kūrimo įrankio puslapyje](./media/ER-FormulaLanguage-AbsolutePath.png)

Tolesnėje iliustracijoje pateiktame pavyzdyje parodyta, kaip naudojamas santykinis kelias. Santykinis kelias `@.AccountNum` nurodo, kad, naudojant duomenų šaltinio **„Intrastat“** lauką **AccountNum** (kuris duomenų modelio hierarchiniame medyje rodomas vienu lygiu aukščiau lauko **AccountNum**), duomenų modelio lauke **AccountNum** įvedamas kliento arba tiekėjo sąskaitos numeris.

![Santykinio kelio pavyzdys ER modelio susiejimo kūrimo įrankio puslapyje](./media/ER-FormulaLanguage-RelativePath1.png)

Likusi absoliučiojo kelio dalis taip pat rodoma [ER formulių rengyklėje](general-electronic-reporting-formula-designer.md).

![Likusi absoliučiojo kelio dalis ER formulių kūrimo įrankio puslapyje](./media/ER-FormulaLanguage-RelativePath2.png)

Daugiau informacijos žr. [Santykinio kelio naudojimas ER modelių ir formatų duomenų sąsajose](relative-path-data-bindings-er-models-format.md).

## <a name="functions"></a><a name="Functions"></a>Funkcijos

ER reiškiniuose galima naudoti integruotąsias ER funkcijas. Visi reiškinio konteksto (tai yra, esamo ER modelio susiejimo arba ER formato) duomenų šaltiniai pagal iškvietimo funkcijų argumentų sąrašą gali būti naudojami kaip iškvietimo funkcijų parametrai. Kaip iškvietimo funkcijos parametrus taip pat galima naudoti konstantas. Pavyzdžiui, dabartiniame ER modelio susiejime yra duomenų šaltinis **InvoiceTransactions**, kuris pateikia įrašų sąrašą. **InvoiceTransactions** įrašo struktūroje yra laukai **AmountDebit** ir **AmountCredit**, kurie abu pateikia skaitines reikšmes. Todėl, kad apskaičiuotumėte SF sumą, galite sukurti tokį reiškinį, kuris naudoja integruotąją ER apvalinimo funkciją: `ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)`.

Kurdami ER modelių susiejimus ir ER ataskaitas, galite naudoti tolesnių kategorijų ER funkcijas.

- [Datos ir laiko funkcijos](er-functions-category-datetime.md)
- [Sąrašo funkcijos](er-functions-category-list.md)
- [Loginės funkcijos](er-functions-category-logical.md)
- [Matematinės funkcijos](er-functions-category-mathematical.md)
- [Įrašo funkcijos](er-functions-category-record.md)
- [Tekstinės funkcijos](er-functions-category-text.md)
- [Duomenų rinkinio funkcijos](er-functions-category-data-collection.md)
- [Kitos (konkrečios verslo srities) funkcijos](er-functions-category-other.md)
- [Tipo konvertavimo funkcijos](er-functions-category-type-conversion.md)

## <a name="functions-list-extension"></a>Funkcijų sąrašo papildymas

ER leidžia papildyti ER išraiškose naudojamų funkcijų sąrašą. Tam reikės atitinkamų inžinerinių pastangų. Išsamią informaciją žr. [Elektroninių ataskaitų (ER) funkcijų sąrašo išplėtimas](general-electronic-reporting-formulas-list-extension.md).

## <a name="compound-expressions"></a>Sudėtiniai reiškiniai

Jei sutampa duomenų tipai, galite kurti sudėtinius reiškinius, kuriuose naudojamos skirtingų kategorijų funkcijos. Kai kartu naudojate kelias funkcijas, užtikrinkite, kad vienos funkcijos išvesties duomenų tipas sutaptų su įvesties duomenų tipu, kurio reikia kitai funkcijai. Pavyzdžiui, siekdami išvengti galimos klaidos „sąrašas tuščias“ lauką susiejant su ER formato elementu, kategorijos [Sąrašas](er-functions-category-list.md) funkcijas suderinkite su kategorijos [Loginės](er-functions-category-logical.md) funkcija, kaip parodyta tolesniame pavyzdyje. Šioje formulėje naudojant funkciją [IF](er-functions-logical-if.md) patikrinama, ar sąrašas **IntrastatTotals** yra tuščias, o tada pateikiama reikiamo telkimo reikšmė iš to sąrašo. Jei sąrašas **IntrastatTotals** yra tuščias, formulė pateikia **0** (nulį).

```vb
IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="multiple-solutions"></a>Keli sprendimai

Dažnai tą pačią duomenų transformaciją galite pasiekti keliais būdais, naudodami skirtingų kategorijų funkcijas arba skirtingas tos pačios kategorijos funkcijas. Pavyzdžiui, ankstesnį reiškinį taip pat galima sukonfigūruoti naudojant kategorijos [Sąrašas](er-functions-category-list.md) funkciją [COUNT](er-functions-list-count.md).

```vb
IF(COUNT (IntrastatTotals)=0, 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)

[Elektroninių ataskaitų funkcijų sąrašo išplėtimas](general-electronic-reporting-formulas-list-extension.md)

[Palaikomų primityvių duomenų tipai](er-formula-supported-data-types-primitive.md)

[Palaikomi sudedamųjų duomenų tipai](er-formula-supported-data-types-composite.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
