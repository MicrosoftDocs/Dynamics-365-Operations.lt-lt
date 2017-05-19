---
title: Valiutos kurso koregavimai
description: "Šioje temoje pateikiama informacija apie valiutos kurso koregavimo funkciją, skirtą vartotojams, kurių juridiniai subjektai yra Estijoje, Čekijos Respublikoje, Latvijoje, Lietuvoje, Lenkijoje ir Rusijoje."
author: ShylaThompson
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Operations, Core
ms.custom: 272683
ms.assetid: cd1b9f11-4640-41a1-a114-222483333972
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 5becb8bcc5aa619edfc0ad2fdcd31a483d003f0a
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="exchange-rate-adjustments"></a>Valiutos kurso koregavimai

[!include[banner](../includes/banner.md)]


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

| Įvykis                                       | Data                             | Debetas / kreditas | Sumos               | DK sąskaita    | Operacijos tipas             | Registravimo tipas       | Kreditas | Koregavimas |
|---------------------------------------------|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
| PVM sąskaita faktūra                                     | 12-12-01                         | Debetas        | 10 000 CAD / 40 000 USD | GS                             | PVM sąskaita faktūra                      | Kliento balansas   |        |            |
| PVM sąskaita faktūra                                     | 12-12-01                         | Kreditas       | 10 000 CAD / 40 000 USD | Korespondavimas                         | PVM sąskaita faktūra                      | DK žurnalas     | X      |            |
| Mokėjimas                                     | 13-01-03                         | Debetas        | 10 000 CAD / 42 000 USD | Korespondavimas                         | Mokėjimas                      | DK žurnalas     |        |            |
| Mokėjimas                                     | 13-01-03                         | Kreditas       | 10 000 CAD / 42 000 USD | GS                             | Mokėjimas                      | Kliento balansas   | X      |            |
| Atsiskaitymas                                  | 2013 m. sausio 3 d. (= mokėjimo data) | Debetas        | 0 CAD / 2 000 USD       | GS                             | Klientas                     | Valiutos kurso pelnas |        |            |
| Atsiskaitymas                                  | 2013 m. sausio 3 d. (= mokėjimo data) | Kreditas       | 0 CAD / 2 000 USD       | Gautas valiutos koregavimo pelnas   | Klientas                     | Valiutos kurso pelnas | X      |            |
| Perkainojimas (standartinis metodas; data = 2012 m. gruodžio 31 d.) | 12-12-31           | Debetas        | 0 CAD / 5 000 USD       | GS                             | Užsienio valiutos kurso pasikeitimas | Valiutos kurso pelnas |        |            |
| Perkainojimas (standartinis metodas; data = 2012 m. gruodžio 31 d.) | 12-12-31           | Kreditas       | 0 CAD / 5 000 USD       | Negautas valiutos koregavimo pelnas | Užsienio valiutos kurso pasikeitimas | Valiutos kurso pelnas | X      |            |
| Perkainojimas (standartinis metodas; data = 2012 m. gruodžio 31 d.) | 13-01-03            | Debetas        | 0 CAD / 5 000 USD       | GS                             | Užsienio valiutos kurso pasikeitimas | Valiutos kurso pelnas |        | X          |
| Perkainojimas (standartinis metodas; data = 2012 m. gruodžio 31 d.) | 13-01-03            | Kreditas       | 0 CAD / 5 000 USD       | Negautas valiutos koregavimo pelnas | Užsienio valiutos kurso pasikeitimas | Valiutos kurso pelnas | X      | X          |



Atkreipkite dėmesį, kad ankstesnio perkainojimo įrašas nuo 2013 m. sausio 3 d. yra tiesioginis virš jo esančio įrašo (nuo 2012 m. gruodžio 31 d.) atšaukimas. Net DK sąskaitos ir registravimo tipai yra tokie patys. Be to, atkreipkite dėmesį, kad nustatyta parinkties **koregavimas** vėliavėlė.
||||||||||
|-----------------------------------------------------------|----------|--------|-----------------|--------------------------------|------------------------------|--------------------|---|---|
|Perkainojimas (SF datos metodas; data = 2013 m. sausio 1 d.)  | 13-01-01 | Debetas  | 0 CAD / 5 000 USD | GS                             | Užsienio valiutos kurso pasikeitimas | Valiutos kurso pelnas |   | X |
| Perkainojimas (SF datos metodas; data = 2013 m. sausio 1 d.) | 13-01-01 | Kreditas | 0 CAD / 5 000 USD | Negautas valiutos koregavimo pelnas | Užsienio valiutos kurso pasikeitimas | Valiutos kurso pelnas | X | X |
| Perkainojimas (SF datos metodas; data = 2013 m. sausio 1 d.) | 13-01-03 | Debetas  | 0 CAD / 5 000 USD | GS                             | Užsienio valiutos kurso pasikeitimas | Valiutos kurso pelnas |   |   |
| Perkainojimas (SF datos metodas; data = 2013 m. sausio 1 d.) | 13-01-03 | Kreditas | 0 CAD / 5 000 USD | Negautas valiutos koregavimo pelnas | Užsienio valiutos kurso pasikeitimas | Valiutos kurso pelnas | X |   |

Atkreipkite dėmesį, kad ankstesnio perkainojimo įrašas nuo 2013 m. sausio 1 d. yra tiesioginis po juo esančio įrašo (nuo 2013 m. sausio 3 d.) atšaukimas. Net DK sąskaitos ir registravimo tipai yra tokie patys. Be to, atkreipkite dėmesį, kad nustatyta parinkties **koregavimas** vėliavėlė.

Sistema veikia taip pat, nepaisant to, ar puslapio **DK parametrai** dalies **Operacijos atšaukimas** parinktis **Koregavimas** nustatyta į **Taip**, ar **Ne**.





