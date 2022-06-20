---
title: DUOMENŲ RINKIMO duomenų šaltinių naudojimas elektroninių ataskaitų formatuose
description: Šiame straipsnyje paaiškinama, kaip naudoti DUOMENŲ RINKIMO duomenų šaltinius elektroninių ataskaitų (ER) formatuose.
author: NickSelin
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 7591bed5d01ce2c2f434f0e7c81e441eda98483e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883852"
---
# <a name="use-data-collection-data-sources-in-electronic-reporting-formats"></a>DUOMENŲ RINKIMO duomenų šaltinių naudojimas elektroninių ataskaitų formatuose

[!include [banner](../includes/banner.md)]

Elektroninių ataskaitų [(ER)](general-electronic-reporting.md) sistemos operacijų konstruktorių galite naudoti norėdami konfigūruoti ER sprendimo, kuris naudojamas siunčiamų dokumentų skirtingo formato dokumentams generuoti, formato komponentą. Sukonfigūruoto formato komponento hierarchinė struktūra susideda iš įvairių tipų formato elementų. Šie formato elementai naudojami sugeneruotiems dokumentams užpildyti reikiama informacija vykdymo metu. Numatyta, kad kai vykdote ER formatą, formato elementai vykdomi tokia pačia tvarka, kokia jie pateikiami formato hierarchijoje: po vieną, iš viršaus į apačią.

Kai ER vykdo formato elementą, kuriame yra susiejimas, vykdoma to susiejimo formulė, o formato elementas šią vertę įtraukia į sugeneruotą dokumentą. Pavyzdžiui, susiejimas į formato elementą gali perduoti duomenų modelio lauko vertę. Galite sukonfigūruoti DUOMENŲ RINKIMO duomenų šaltinį duomenų modelio laukų vertėms rinkti vykdymo metu, vertėms sumuoti ir dokumentui sugeneruoti naudojant surinktas vertes. Jei norite naudoti šį metodą, pakeiskite pradinį susiejimą taip, kad sukonfigūruotas DUOMENŲ RINKIMO duomenų šaltinis būtų naudojamas duomenų modelio lauko vertei į formato elementą perduoti. Perduodami vertes į DUOMENŲ RINKIMO duomenų šaltinį, galite surinkti reikiamą informaciją, kurią galėsite naudoti ateityje.

Konfigūruodami DUOMENŲ RINKIMO duomenų šaltinį, nurodykite vertės tipą, kuris bus tvarkomas duomenų šaltinyje. Renkant vertes šiuo metu palaikomi tolesni [duomenų tipai](er-formula-supported-data-types-primitive.md).

- Bulio logika
- Data
- DateTime
- Guid
- Int64
- Sveikasis skaičius
- Tikrasis
- Eilutė
- Laikas

Norėdami perduoti vertę į duomenų šaltinį, kad ji būtų surinkta, galite naudoti DUOMENŲ RINKIMO duomenų šaltinio metodą `Collect(Value)`. Taikant šį metodą, argumentas `Value` yra konstanta arba tinkamas atitinkamo duomenų tipo duomenų šaltinio lauko kelias.

Norėdami pasiekti surinktų verčių sąrašą, naudokite DUOMENŲ RINKIMO duomenų šaltinio ypatybę `Result`. Ši ypatybė pateikia [įrašų sąrašą](er-formula-supported-data-types-composite.md#record-list). Įrašų sąrašo įrašuose yra laukas `Value`, kurį galite naudoti surinktoms vertėms pasiekti.

Pagal numatytuosius parametrus DUOMENŲ RINKIMO duomenų šaltinis renka tik unikalias vertes.

Norėdami rinkti visas vertes, sukonfigūruoto DUOMENŲ RINKIMO duomenų šaltinio lauką **Rinkti visas vertes** nustatykite kaip **Taip**. Kai laukas **Rinkti visas vertes** nustatytas kaip **Taip**, galima parametrizuota ypatybė `Sum(Flag)`. Šią ypatybę galite naudoti norėdami gauti bendrą visų šiuo metu surinktų verčių sumą. Šioje ypatybėje argumentas `Flag` yra [Bulio logikos](er-formula-supported-data-types-primitive.md#boolean) vertė, naudojama norint nurodyti, ar reikia iš naujo nustatyti bendrąją vertę.

- Kai pateikta vertė **False**, sumavimas tęsiamas nuo anksčiau surinktos sumos.
- Kai pateikta vertė **True**, pradedamas naujas sumavimas.

Sumuojant šiuo metu palaikomi tolesni duomenų tipai.

- Int64
- Sveikasis skaičius
- Tikrasis

Norėdami daugiau sužinoti apie šią funkciją, atlikite toliau pateiktą pavyzdį.

## <a name="example-configure-an-er-format-to-do-counting-and-summing-by-using-a-data-collection-data-source"></a>Pavyzdys: ER formato sukonfigūravimas, kad būtų skaičiuojama ir sumuojama naudojant DUOMENŲ RINKIMO duomenų šaltinį

Šiame pavyzdyje parodoma, kaip sistemos administratoriaus arba elektroninių ataskaitų funkcijų konsultanto vaidmenį turintis vartotojas gali sukonfigūruoti ER formatą, kuriame būtų DUOMENŲ RINKIMO duomenų šaltinis, naudojamas bendrosioms sumoms skaičiuoti ir susumuotoms vertėms surinkti.

Šiame pavyzdyje pateiktas procedūras galima atlikti JAV Microsoft Dynamics 365 finansų įmonėje.

### <a name="upload-and-use-the-provided-er-solution"></a>Pateikto ER sprendimo nusiuntimas ir naudojimas

1. [Importuoti pavyzdines ER konfigūracijas](er-defer-sequence-element.md#import-the-sample-er-configurations).
2. [Aktyvuoti konfigūracijos tiekėją](er-defer-sequence-element.md#activate-a-configurations-provider).
3. [Peržiūrėkite importuotų modelių susiejimą](er-defer-sequence-element.md#review-the-imported-model-mapping).
4. [Peržiūrėti importuotą formatą](er-defer-sequence-element.md#review-the-imported-format).
5. [Vykdykite importuotą formatą](er-defer-sequence-element.md#run-the-imported-format).

### <a name="run-the-format-of-the-provided-er-solution"></a>Pateikto ER sprendimo formato vykdymas

1. Puslapyje **Formato dizaino įrankis** pasirinkite **Vykdyti**.
2. Dialogo lange **Elektroninių ataskaitų parametrai** pasirinkite **Gerai**.
3. Atsisiųskite ir peržiūrėkite failą, kuris siūlomas žiniatinklio naršyklėje.

    ![Atsisiųstas failas, kuriame yra pradinio formato vykdymo rezultatai](./media/er-data-collection-data-sources-01.png)

### <a name="modify-the-format-of-the-er-solution-to-calculate-the-running-tax-total"></a>ER sprendimo formato modifikavimas, kad būtų galima apskaičiuoti bendrąją mokesčių sumą

Jei operacijų kiekis yra daug didesnis, nei kiekis šiame pavyzdyje, susumuoti reikalingas laikas gali padidėti ir gali kilti našumo problemų. Pakeisdami formato parametrus, galite padėti išvengti šių našumo problemų. Kadangi mokesčių vertės įtraukiamos į sugeneruotą ataskaitą, galima pakartotinai panaudoti šią informaciją mokesčių vertėms sumuoti.

1. Puslapio **Formato dizaino įrankis** skirtuke **Susiejimas** pasirinkite **Įtraukti šakninį elementą**.
2. Dialogo lange **Duomenų šaltinio įtraukimas** pasirinkite **Funkcijos** \> **Duomenų rinkimas**.
3. Dialogo lange **Duomenų rinkimo duomenų šaltinio ypatybės** atlikite tolesnius veiksmus.

    1. Lauke **Pavadinimas** įveskite **CollectedTaxValues**.
    2. Lauke **Elemento tipas** pasirinkite **Realusis skaičius**.
    3. Lauke **Rinkti visas vertes** pasirinkite **Taip**.
    4. Pasirinkite **Gerai**.

4. Pasirinkite skaitinį formato elementą **Ataskaitos\\Eilutės\\Įrašas\\TaxAmount**.

    > [!NOTE]
    > Šiuo metu šiam elementui sukonfigūruotas susiejimas `@.Value`. Todėl sugeneruotas dokumentas užpildomas mokesčių vertėmis iš lauko `model.Data.List.Value`.

5. Pasirinkite **Redaguoti formulę**.
6. Puslapyje **Formulės konstruktorius** atlikite tolesnius veiksmus.

    1. Lauke **Formulė** elementą `@.Value` pakeiskite elementu `CollectedTaxValues.Collect(@.Value)`.
    2. Įrašykite keitimus ir uždarykite puslapį.

    > [!NOTE]
    > Naujasis susiejimas tas pačias mokesčių vertes perduos į sugeneruotą dokumentą. Tačiau tos vertės taip pat bus surinktos duomenų šaltinyje **CollectedTaxValues**.

7. Pasirinkite skaitinį formato elementą **Ataskaitos\\Eilutės\\Įrašas\\RunningTotal**.
8. Pasirinkite **Redaguoti formulę**.
9. Puslapyje **Formulės konstruktorius** atlikite tolesnius veiksmus.

    1. Lauke **Formulė** įveskite `CollectedTaxValues.Sum(false)`.
    2. Įrašykite keitimus ir uždarykite puslapį.

    > [!NOTE]
    > Naujasis susiejimas į sugeneruotą dokumentą perduos bendrą jau įvestų mokesčių verčių sumą.

    ![Skaitiniai elementai, kurių susiejimai atnaujinti puslapyje Formato dizaino įrankis](./media/er-data-collection-data-sources-02.png)

10. Pasirinkite **Įrašyti**, tada pasirinkite **Vykdyti**.
11. Dialogo lange **Elektroninių ataskaitų parametrai** pasirinkite **Gerai**.
12. Atsisiųskite ir peržiūrėkite failą, kuris siūlomas žiniatinklio naršyklėje.

    ![Atsisiųstas failas, kuriame yra modifikuoto formato vykdymo rezultatai](./media/er-data-collection-data-sources-03.png)

### <a name="modify-the-format-to-evaluate-the-list-of-collected-tax-values"></a>Formato modifikavimas norint įvertinti surinktų mokesčių verčių sąrašą

1. Puslapio **Formato dizaino įrankis** skirtuke **Formatas** pasirinkite skaitinį formato elementą **Ataskaita\\Eilutės\\Įrašas\\RunningTotal**, tada atlikite tolesnius veiksmus.

    1. Lauke **Skaitinis tipas** vertę iš **Realusis skaičius** pakeiskite į **Sveikasis skaičius**.
    2. Lauke **Skaitinis formatas** vertę **F2** pakeiskite į **F0**.

3. Skirtuke **Susiejimas** pasirinkite **Redaguoti formulę**.
4. Puslapyje **Formulės konstruktorius** atlikite tolesnius veiksmus.

    1. Lauke **Formulė** įveskite `COUNT(CollectedTaxValues.Result)`.
    2. Įrašykite keitimus ir uždarykite puslapį.

    > [!NOTE]
    > Naujasis susiejimas į sugeneruotą dokumentą perduos įrašų skaičių sąraše, kuriame renkamos mokesčių vertės.

5. Pasirinkite **Įrašyti**, tada pasirinkite **Vykdyti**.
6. Dialogo lange **Elektroninių ataskaitų parametrai** pasirinkite **Gerai**.
7. Atsisiųskite ir peržiūrėkite failą, kuris siūlomas žiniatinklio naršyklėje.

    ![Atsisiųstas failas, kuriame yra kito modifikuoto formato vykdymo rezultatai](./media/er-data-collection-data-sources-04.png)

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions"></a>Jei man reikia skaičiuoti bendrąsias sumas ir rinkti duomenis, kuo skiriasi DUOMENŲ RINKIMO duomenų šaltinis ir integruotos DUOMENŲ RINKIMO funkcijos?

Tiek DUOMENŲ RINKIMO duomenų šaltinis, tiek integruotos [DUOMENŲ RINKIMO](er-functions-category-data-collection.md) funkcijos gali būti naudojamos duomenims rinkti, sumuoti ir skaičiuoti, remiantis informacija, kuri perduodama į sugeneruotą siunčiamą dokumentą. Tačiau kai bandote nuspręsti, kokį metodą naudoti, turite atsižvelgti į tolesnius aspektus.

| Duomenų šaltinis | Integruotos funkcijos |
|-------------| ------------------ |
| Renkamos tik vertės. | <p>Renkamos tik įvardytosios vertės. Todėl galima apskaičiuoti atskirų verčių grupių sumas.</p><p>Be to, grupes galima gauti kaip sąrašą.</p><p>Tekstinės vertės taip pat gali būti renkamos.</p> |
| Unikalios vertės yra renkamos automatiškai. | Norint iš surinktų verčių gauti unikalių verčių sąrašą, reikia naudoti papildomus parametrus. |
| Našumas priklauso nuo surinktų verčių kiekio. | Praktikoje našumas nepriklauso nuo surinktų verčių kiekio. |
| Šis metodais veikia su visų tipų siunčiamais dokumentais. | Šis metodas veikia tik su teksto ir XML dokumentais. |

## <a name="additional-resources"></a>Papildomi ištekliai

- [Formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti](./tasks/er-format-counting-summing-1.md)
- [Sekos elementų ER formatais vykdymo atidėjimas](er-defer-sequence-element.md#Example)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
