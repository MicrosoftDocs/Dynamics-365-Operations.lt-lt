---
title: Savikainos apskaitos analizės „Power BI“ turinys
description: Šiame straipsnyje aprašoma, kas įtraukta į kaštų apskaitos analizės Power BI turinį.
author: AndersGirke
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.openlocfilehash: 7339d0abf8d087ca8fcc8f46dc91a5e78ec0f325
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269732"
---
# <a name="cost-accounting-analysis-power-bi-content"></a>Savikainos apskaitos analizės „Power BI“ turinys

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kas įtraukta į kaštų **apskaitos analizės** Microsoft Power BI turinį. Jame paaiškinta, kaip pasiekti „Power BI“ ataskaitas, ir pateikta informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

## <a name="overview"></a>Peržiūrėti

„Power BI“ turinys **Kaštų apskaitos analizė** skirtas išlaidų kontrolieriams arba bet kam, kas yra atsakingas už organizacijos išlaidų valdymą. Jis apima pagrindinius duomenis, pvz., išlaidas, reikšmę ir išlaidų koeficientą pagal faktines išlaidas, biudžeto išlaidas ir kintamas biudžeto išlaidas. Jame naudojami operacijų duomenys iš modulio **Išlaidų apskaita** ir pateikiamas sujungtas visos įmonės išlaidų rodinys viena ataskaitų valiuta. Vadovai gali filtruoti duomenis pagal išlaidų objektus, kad atliktų savo organizacijos vienetų išlaidų kontrolę, net jei organizacija turėtų kelis juridinius subjektus.

Kadangi turinys **išlaidų apskaitos analizės** išskiria nuokrypius tarp faktinių išlaidų ir biudžeto išlaidų, vadovus galima įspėti apie teigiamas ir neigiamas jų valdomų vienetų tendencijas. Vadybininkai gali detalizuoti iki išlaidų elementų hierarchijų arba atskirų išlaidų elementų. Tokiu būdu vadybininkai gali įgyti išsamų supratimą apie tai, kaip atsirado išlaidų nuokrypiai, o po to imtis veiksmų.

Turinys **Kaštų apskaitos analizė** išlaidų buhalteriams suteikia galimybę analizuoti visos organizacijos išlaidų objektų srautus.

Norėdami daugiau sužinoti apie išlaidų apskaitą, žr. [Išlaidų apskaitos pagrindinis puslapis](../../../finance/cost-accounting/cost-accounting-home-page.md).

Nustatydami kaštų apskaitos prieigos lygio saugą ir ją suderindami su „Power BI“ eilutės lygio sauga, visiems išlaidų objektų savininkams galite suteikti prieigą prie „Power BI“ turinio **Kaštų apskaitos analizė**. Tada visi vaizdinių priemonių duomenys bus filtruojami pagal išlaidų apskaitos valdomą prieigos lygį. Norėdami daugiau sužinoti apie prieigos lygio saugą ir eilutės lygio saugą, žr. temą [Power BI turinio išlaidų apskaitos analizės saugos nustatymas](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio
„Power BI“turinį **Kaštų apskaitos analizė** galite rasti bendrai naudojamo turto bibliotekoje „Microsoft Dynamics Lifecycle Services“ (LCS). Norėdami gauti daugiau informacijos apie tai, kaip atsisiųsti turinį ir įdiegti jį savo organizacijoje, žr. [„Power BI“ turinys LCS iš „Microsoft“ ir jūsų partnerių](/archive/blogs/dynamicsaxbi/power-bi-content-from-microsoft-and-your-partners).

Įsitikinkite, kad atsisiunčiate tą turinį **Kaštų apskaitos analizė**, kuris taikomas jūsų naudojamai „Microsoft Dynamics 365“ versijai.

> [!NOTE]
> KB 4011327 yra būtinoji šio „Power BI“ turinio sąlyga. Prisijungę prie LCS, KB galite pasiekti adresu <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos metrikos
Į turinį įtrauktas ataskaitų puslapių rinkinys. Kiekvieną puslapį sudaro metrikų, pavaizduotų diagramomis, plytelėmis ir lentelėmis, rinkinys. Toliau pateiktoje lentelėje pateikiama „Power BI“ turinio **Kaštų apskaitos analizė** vizualizacijų apžvalga.

| Ataskaitų puslapis                      | Diagrama                                                                                                                         | Išklotinė                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Išlaidų kontrolė pagal finansinį laikotarpį    | Faktinės išlaidos ir biudžeto išlaidos pagal išlaidų elemento hierarchijos lygį                                                                   | Faktinės išlaidos ir biudžeto išlaidos                    |
|                                  | Biudžeto nuokrypis pagal išlaidų elemento hierarchijos lygį                                                                               | Faktinių išlaidų koeficientas ir biudžeto išlaidų koeficientas          |
|                                  | 10 geriausių biudžeto nuokrypių procentais pagal išlaidų elementą                                                                          | Faktinė reikšmė ir biudžeto reikšmė          |
| Išlaidų kontrolė pagal metus iki šios dienos     | Faktinės išlaidos ir biudžeto išlaidos pagal kalendorinių metų laikotarpį                                                                           | Faktinės išlaidos ir biudžeto išlaidos                    |
|                                  | Biudžeto nuokrypis pagal kalendorinių metų laikotarpį                                                                                       | Faktinių išlaidų koeficientas ir biudžeto išlaidų koeficientas          |
|                                  | 10 geriausių biudžeto nuokrypių procentais pagal išlaidų elementą                                                                          | Faktinė reikšmė ir biudžeto reikšmė          |
| Išlaidų koeficientas pagal finansinius metus         | Faktinių išlaidų koeficientas pagal išlaidų veikimo būdą                                                                                             | Faktinių išlaidų koeficientas ir biudžeto išlaidų koeficientas          |
|                                  | Faktinių išlaidų koeficientas, biudžeto išlaidų koeficiento nuokrypis, biudžeto išlaidų koeficiento procentas ir biudžeto išlaidų koeficientas pagal išlaidų elemento hierarchijos lygį | Faktinė reikšmė ir biudžeto reikšmė          |
|                                  | Biudžeto nuokrypis pagal išlaidų elemento hierarchijos lygį                                                                               |                                               |
|                                  | 10 geriausių biudžeto nuokrypių procentais pagal išlaidų elementą                                                                          |                                               |
| Kintantis biudžetas pagal finansinį laikotarpį | Faktinės išlaidos, biudžeto išlaidos ir kintamo biudžeto išlaidos pagal išlaidų elemento hierarchijos lygį                                             | Faktinė reikšmė ir biudžeto reikšmė          |
|                                  | Biudžeto nuokrypis ir kintamo biudžeto nuokrypis pagal išlaidų elemento hierarchijos lygį                                                  | Faktinės išlaidos ir kintamo biudžeto išlaidos           |
|                                  | Faktinės išlaidos, biudžeto išlaidos ir kintamos išlaidos pagal išlaidų veikimo būdą ir išlaidų elemento hierarchijos lygį                                  | Faktinių išlaidų koeficientas ir kintamo biudžeto išlaidų koeficientas |
| Išlaidų išrašas pagal finansinį laikotarpį  | Faktinės išlaidos pagal išlaidų elemento hierarchijos lygį ir išlaidų objekto dimensijos nario pavadinimą                                             |                                               |
|                                  | Faktinės išlaidos pagal išlaidų objekto dimensijos nario pavadinimą ir išlaidų elemento dimensijos nario pavadinimą                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
Tolesniais duomenimis pildomi „Power BI“ turinio **Kaštų apskaitos analizė** ataskaitų puslapiai. Šie duomenys pateikiami sujungtais matavimo vienetais, paskirstytais objektų saugykloje. Objektų saugykla yra „Microsoft SQL Server“ duomenų bazė, optimizuota analizei atlikti. Daugiau informacijos žr. [„Power BI“ integravimo su objekto parduotuve apžvalga](power-bi-integration-entity-store.md).

Šie pagrindiniai sujungti matavimo vienetai naudojami kaip turinio pagrindas.

| Objektas                  | Pagrindiniai sujungti matavimo vienetai | „Dynamics 365“ duomenų šaltinis      | Laukas     | aprašymas                                        |
|-------------------------|---------------------------|-----------------------------------|-----------|----------------------------------------------------|
| Išlaidų apskaitos įrašai | SUM(Amount)               | CAMDATAAggregatedCostEntry        | Suma    | Suma išlaidų apskaitos DK valiuta. |
| Statistiniai įrašai     | SUM(Magnitude)            | CAMDATAAggregatedStatisctialEntry | Reikšmė |                                                    |

Šioje lentelėje parodyta, kaip pagrindiniai sujungti matavimo vienetai naudojami kuriant kelis skaičiuojamus matus turinio duomenų rinkinyje.

| Mato vnt.                                       | Kaip matas apskaičiuojamas                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Faktinės išlaidos                                   | CALCULATE('Išlaidų apskaitos įrašai'\[Matas\], 'Operacijos versijos'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)            |
| Biudžeto išlaidos                                   | CALCULATE('Išlaidų apskaitos įrašai'\[Matas\], 'Operacijos versijos'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)            |
| Biudžeto išlaidų nuokrypis                          | \[Biudžeto išlaidos\] - \[Faktinės išlaidos\]                                                                                      |
| Biudžeto nuokrypio procentas                    | IF(\[Biudžeto išlaidos\] = 0, tuščia(), \[Biudžeto nuokrypis\] / \[Biudžeto išlaidos\])                                                |
| Faktinė reikšmė                              | CALCULATE('Statistiniai įrašai'\[FullMagnitude\], 'Operacijos versijos'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)          |
| Biudžeto reikšmė                              | CALCULATE(\[FullMagnitude\], 'Operacijos versijos'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)                               |
| Statistinis biudžeto nuokrypis                   | \[Biudžeto reikšmė\] - \[Faktinė reikšmė\]                                                                            |
| Statistinio biudžeto nuokrypio procentas        | IF(\[Biudžeto reikšmė\] = 0, tuščia(), \[Statistinis biudžeto nuokrypis\] / \[Biudžeto reikšmė\])                          |
| Faktinių išlaidų tarifas                              | IF(\[Faktinė reikšmė\] = 0, NENURODYTA(), \[Faktinės išlaidos\] / \[Faktinė reikšmė\])                                          |
| Biudžeto išlaidų tarifas                              | IF(\[Biudžeto reikšmė\] = 0, NENURODYTA(), \[Biudžeto išlaidos\] / \[Biudžeto reikšmė\])                                          |
| Biudžeto išlaidų koeficiento nuokrypis                     | \[Biudžeto išlaidų koeficientas\] - \[Faktinių išlaidų koeficientas\]                                                                            |
| Biudžeto išlaidų koeficiento nuokrypio procentas          | IF(\[Biudžeto išlaidos\] = 0, tuščia(), \[Biudžeto išlaidų koeficiento nuokrypis\] / \[Biudžeto išlaidų koeficientas\])                                 |
| Fiksuotos biudžeto išlaidos                             | CALCULATE(\[Biudžeto išlaidos\], 'Išlaidų apskaitos įrašai'\[COSTBEHAVIOR\] = 1)                                              |
| Nuokrypio biudžeto išlaidos                          | CALCULATE(\[Biudžeto išlaidos\], 'Išlaidų apskaitos įrašai'\[COSTBEHAVIOR\] = 2)                                              |
| Fiksuotos kintamos biudžeto išlaidos                    | \[Fiksuotos biudžeto išlaidos\]                                                                                                  |
| Nuokrypio kintamos biudžeto išlaidos                 | IF\[Biudžeto reikšmė\] = 0, NENURODYTA(), (\[Nuokrypio biudžeto išlaidos\] / \[Biudžeto reikšmė\] \* \[Faktinė reikšmė\])       |
| Kintamos biudžeto išlaidos                          | \[Fiksuotos kintamos biudžeto išlaidos\] + \[Nuokrypio kintamos biudžeto išlaidos\]                                                     |
| Fiksuotas biudžeto nuokrypis                      | \[Faktinės biudžeto išlaidos\] - \[Faktinės išlaidos\]                                                                             |
| Kintamo biudžeto nuokrypio procentas           | IF(\[Kintamos biudžeto išlaidos\] = 0, TUŠČIA(), \[Kintamas biudžeto nuokrypis\] / \[Kintamos biudžeto išlaidos\])                     |
| Kintamų biudžeto išlaidų koeficientas                     | IF(\[Faktinė reikšmė\] = 0, NENURODYTA(), \[Kintamos biudžeto išlaidos\] / \[Faktinė reikšmė\])                                 |
| Kintamų biudžeto išlaidų koeficiento nuokrypis            | \[Kintamų biudžeto išlaidų koeficientas\] - \[Faktinių išlaidų koeficientas\]                                                                   |
| Kintamų biudžeto išlaidų koeficiento nuokrypio procentas | IF(\[Kintamų biudžeto išlaidų koeficientas\] = 0, TUŠČIA(), \[Kintamų biudžeto išlaidų nuokrypis\] / \[Kintamų biudžeto išlaidų koeficientas\]) |

Šios pagrindinės dimensijos naudojamos kaip filtrai sujungtiems matavimo vienetams skaidyti, siekiant didesnio detalumo ir gilesnių analitinių įžvalgų.

| Objektas                             | Atributų pavyzdžiai                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Savikainos apskaitos didžiosios knygos            | Savikainos apskaitos didžioji knyga                                                                                               |
| Savikainos kontrolės įtaisai                 | Savikainos kontrolės įtaiso pavadinimas                                                                                               |
| Savikainos elemento dimensijos            | Išlaidų elementų dimensijos pavadinimas, išlaidų elemento dimensijos nario pavadinimas, išlaidų elemento dimensijos nario aprašas          |
| Savikainos objekto dimensijos             | Išlaidų objekto dimensijos pavadinimas, išlaidų objekto dimensijos nario pavadinimas, išlaidų objekto dimensijos nario aprašas              |
| Statistinės dimensijos             | Statistinis dimensijos pavadinimas, statistinis dimensijos nario pavadinimas, statistinis dimensijos nario aprašas              |
| Išlaidų objekto dimensijų hierarchijos  | Išlaidų objekto dimensijų hierarchijos pavadinimas, išlaidų objekto dimensijų hierarchijos lygis, išlaidų objekto dimensijų hierarchijos medis    |
| Išlaidų elemento dimensijų hierarchijos | Išlaidų elemento dimensijų hierarchijos pavadinimas, išlaidų elemento dimensijų hierarchijos lygis, išlaidų elemento dimensijų hierarchijos medis |
| Statistinių dimensijų hierarchijos  | Statistinių dimensijų hierarchijos pavadinimas, statistinių objekto dimensijų hierarchijos lygis, statistinių dimensijų hierarchijos medis    |
| Operacijų versijos               | Versijos pavadinimas                                                                                                         |
| Finansiniai kalendoriai                   | Kalendorius, kalendoriaus aprašymas                                                                                       |
| Finansiniai metai                       | Kalendoriniai metai                                                                                                        |
| Ataskaitiniai laikotarpiai                     | Kalendorinių metų laikotarpis                                                                                                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
