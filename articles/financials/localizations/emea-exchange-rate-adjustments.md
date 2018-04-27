---
title: Valiutos kurso koregavimai
description: "Šioje temoje pateikiama informacija apie valiutos kurso koregavimo funkciją, skirtą vartotojams, kurių juridiniai subjektai yra Estijoje, Čekijos Respublikoje, Latvijoje, Lietuvoje, Lenkijoje ir Rusijoje."
author: ShylaThompson
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 272683
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: dbc715a23e14d96e0ac93e47ff793e49fad24b93
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="exchange-rate-adjustments"></a>Valiutos kurso koregavimai

[!INCLUDE [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie valiutos kurso koregavimo funkciją, skirtą vartotojams, kurių juridiniai subjektai yra Estijoje, Čekijos Respublikoje, Latvijoje, Lietuvoje, Lenkijoje ir Rusijoje.

Valiutos kurso koregavimo funkcija, skirta Estijai, Vengrijai, Čekijos Respublikai, Latvijai, Lietuvai, Lenkijai ir Rusijai, apima tolesnius plėtinius, kurie susiję su gautinomis ir mokėtinomis sumomis.

-   Valiutos kurso koregavimų registravimus galima atšaukti kaip pradinių koregavimų taisymus (neigiamas sumas).
-   Kai iš eilės registruojami nerealizuoti koregavimai, naudojami tie patys DK registravimo sąskaita ir operacijos tipas, nepriklausomai nuo to, ar koregavimai nurodo pelną, ar nuostolį.
-   Apskaičiuotas valiutos kurso pelnas visada registruojamas pelno sąskaitose, o apskaičiuoti valiutos kurso nuostoliai visada registruojami nuostolių sąskaitose.

Juridiniai subjektai, kurių pagrindinis adresas yra Čekijos Respublikoje, gali naudoti specialų valiutos kurso koregavimo būdą. Šis būdas vadinamas didėjančios tvarkos metodu. Įjungus šį metodą, dabartinės funkcijos teikiami keitimai netaikomi. Negautas ir gautas pelnas arba nuostoliai apskaičiuojami pagal paskutinį naudotą valiutos kursą. Kaip skaičiavimo pagrindas vietoj pradinės sumos naudojama koreguota suma. Norėdami įjungti valiutos kurso koregavimo didėjančia tvarka metodą, puslapio **DK parametrai** dalies **Užsienio valiutos kurso pasikeitimas** lauke **Skaičiavimo būdas** pasirinkite **Didėjančia tvarka**. Tolesniame pavyzdyje parodyta, kaip valiutos kurso koregavimo funkcija veikia Estijoje, Vengrijoje, Čekijos Respublikoje, Latvijoje, Lietuvoje, Lenkijoje ir Rusijoje. Toliau pateikiamas šio pavyzdžio verslo scenarijus.

-   2012 m. gruodžio 1 d. užregistruojama SF užsienio valiuta.
-   2013 m. sausio 3 d. užregistruojamas mokėjimas užsienio valiuta.
-   Įvykdomas sudengimas, kad mokėjimas būtų priskirtas SF.
-   2012 m. gruodžio 31 d. atliekamas valiutos kurso koregavimas (metodas = standartinis).
-   2013 m. sausio 1 d. atliekamas valiutos kurso koregavimas (metodas = SF data).

Toliau pateikiamas šiame pavyzdyje naudojamas Kanados dolerių (CAD) keitimo į JAV dolerius (USD) kursas.

-   2012 m. gruodžio 1 d.: 400,0000
-   2012 m. gruodžio 31 d.: 450,0000
-   2013 m. sausio 1 3.: 420,0000

### <a name="invoice"></a>PVM sąskaita faktūra

| Data                             | Debetas / kreditas | Sumos               | DK sąskaita    | Operacijos tipas             | Registravimo tipas       | Kreditas | Koregavimas |
|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
| 12-12-01                         | Debetas        | 10 000 CAD / 40 000 USD | GS                             | PVM sąskaita faktūra                      | Kliento balansas   |        |            |
| 12-12-01                         | Kreditas       | 10 000 CAD / 40 000 USD | Korespondavimas                         | PVM sąskaita faktūra                      | DK žurnalas     | X      |

### <a name="payment"></a>Mokėjimas

| Data                             | Debetas / kreditas | Sumos               | DK sąskaita    | Operacijos tipas             | Registravimo tipas       | Kreditas | Koregavimas |
|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
| 13-01-03                         | Debetas        | 10 000 CAD / 42 000 USD | Korespondavimas                         | Mokėjimas                      | DK žurnalas     |        |            |
| 13-01-03                         | Kreditas       | 10 000 CAD / 42 000 USD | GS                             | Mokėjimas                      | Kliento balansas   | X      |            |

### <a name="settlement"></a>Atsiskaitymas

| Data                             | Debetas / kreditas | Sumos               | DK sąskaita    | Operacijos tipas             | Registravimo tipas       | Kreditas | Koregavimas |
|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
|2013 m. sausio 3 d. (= mokėjimo data) | Debetas        | 0 CAD / 2 000 USD       | GS                             | Klientas                     | Valiutos kurso pelnas |        |            |
2013 m. sausio 3 d. (= mokėjimo data) | Kreditas       | 0 CAD / 2 000 USD       | Gautas valiutos koregavimo pelnas   | Klientas                     | Valiutos kurso pelnas | X      |            |


### <a name="revaluation--standard-method-date--december-31-2012"></a>Perkainojimas (standartinis metodas; data = 2012 m. gruodžio 31 d.)
Atkreipkite dėmesį, kad šiame perkainojimo pavyzdyje 2013 m. sausio 3 d. įrašas yra tiesioginis 2012 m. gruodžio 31 d. įrašo atšaukimas. Net DK sąskaitos ir registravimo tipai yra tokie patys. Be to, atkreipkite dėmesį, kad nustatyta parinkties **koregavimas** vėliavėlė.

| Data                             | Debetas / kreditas | Sumos               | DK sąskaita    | Operacijos tipas             | Registravimo tipas       | Kreditas | Koregavimas |
|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
| 12-12-31           | Debetas        | 0 CAD / 5 000 USD       | GS                             | Užsienio valiutos kurso pasikeitimas | Valiutos kurso pelnas |        |            |
| 12-12-31           | Kreditas       | 0 CAD / 5 000 USD       | Negautas valiutos koregavimo pelnas | Užsienio valiutos kurso pasikeitimas | Valiutos kurso pelnas | X      |            |
| 13-01-03            | Debetas        | 0 CAD / 5 000 USD       | GS                             | Užsienio valiutos kurso pasikeitimas | Valiutos kurso pelnas |        | X          |
 13-01-03            | Kreditas       | 0 CAD / 5 000 USD       | Negautas valiutos koregavimo pelnas | Užsienio valiutos kurso pasikeitimas | Valiutos kurso pelnas | X      | X          |


### <a name="revaluation-invoice-date-method-date--january-1-2013"></a>Perkainojimas (SF datos metodas; data = 2013 m. sausio 1 d.)
Atkreipkite dėmesį, kad šiame perkainojimo pavyzdyje 2013 m. sausio 1 d. įrašas yra tiesioginis 2013 m. sausio 3 d. įrašo atšaukimas. Net DK sąskaitos ir registravimo tipai yra tokie patys. Be to, atkreipkite dėmesį, kad nustatyta parinkties **koregavimas** vėliavėlė.

| Data   | Debetas / kreditas | Sumos | DK sąskaita| Operacijos tipas| Registravimo tipas| Kreditas | Koregavimas |
|--------|--------------|---------|----------------------------|----------------|--------|------------|--------------|
|13-01-01 | Debetas  | 0 CAD / 5 000 USD | GS                             | Užsienio valiutos kurso pasikeitimas | Valiutos kurso pelnas |   | X |
|13-01-01 | Kreditas | 0 CAD / 5 000 USD | Negautas valiutos koregavimo pelnas | Užsienio valiutos kurso pasikeitimas | Valiutos kurso pelnas | X | X |
|13-01-03 | Debetas  | 0 CAD / 5 000 USD | GS                             | Užsienio valiutos kurso pasikeitimas | Valiutos kurso pelnas |   |   |
|13-01-03 | Kreditas | 0 CAD / 5 000 USD | Negautas valiutos koregavimo pelnas | Užsienio valiutos kurso pasikeitimas | Valiutos kurso pelnas | X |   |

Sistema veikia taip pat, nepaisant to, ar puslapio **DK parametrai** dalies **Operacijos atšaukimas** parinktis **Koregavimas** nustatyta į **Taip**, ar **Ne**.




