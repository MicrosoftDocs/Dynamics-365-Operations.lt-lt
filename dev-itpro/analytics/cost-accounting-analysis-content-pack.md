---
title: "Sąnaudų apskaitos analizės Power BI turinys"
description: "Šioje temoje aprašoma, kas įeina į Power BI turinį sąnaudų apskaitos analizės. Jis paaiškina, kaip jas pasiekti Power BI ir pateikia informaciją apie duomenų modelio ir subjektai, kurie buvo naudojami sukurti turinį."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 50e7bd92ee693f59fd013226aee22bd1a54c81e2
ms.lasthandoff: 03/31/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Sąnaudų apskaitos analizės Power BI turinys

Šioje temoje aprašoma, kas įeina į Power BI turinį sąnaudų apskaitos analizės. Jis paaiškina, kaip jas pasiekti Power BI ir pateikia informaciją apie duomenų modelio ir subjektai, kurie buvo naudojami sukurti turinį.

<a name="overview"></a>Apžvalga
--------

Pagal **išlaidų apskaitos analizė** Microsoft Power BI turinys skirtas išlaidas duomenų valdytojas ar bet kam, kas yra atsakingas už išlaidų kontrolės organizacijos. Ji apima pagrindinius rodiklius, pvz., išlaidas, masto ir išlaidų tarifas pagal faktines išlaidas, biudžeto išlaidų ir kintamo biudžeto išlaidų. Jis naudoja sandorio duomenis iš sąnaudų apskaitos Microsoft Dynamics 365 operacijų ir bendras vaizdas į išlaidas numatyta visai organizacijai vieną ataskaitų valiuta. Valdytojai duomenis galite filtruoti pagal išlaidų objektų atlikti išlaidų kontrolę, jų organizacinius vienetus, net jei organizacija gali turėti keletą juridinių asmenų. Nes į **sąnaudų apskaitos analizės** Power BI turinio pabrėžia skirtumus tarp faktinės išlaidos ir biudžete numatytoms išlaidoms, vadovai gali būti pranešta apie teigiamas ir neigiamas tendencijas, jų veiklos vienetų. Vadovai gali naudoti detalizavimą sąnaudų elementų hierarchijos ar atskirų išlaidų elementų išsamios perprasti kaip sąnaudų skirtumus įvyko, o tada imtis efektyvių veiksmų. Pagal **išlaidų apskaitos analizė** Power BI turinio kaina buhalterių Panagrinėkime kaip išlaidų teka visos organizacijos išlaidų objektus. Norėdami sužinoti daugiau apie kaštų apskaitos, pamatyti [sąnaudų apskaitos pagrindiniame puslapyje](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page.md). Prieigos lygį saugumo kaštų apskaitos ir derinant ją su eilutės lygio saugumo, Power BI, galite suteikti visų išlaidų objekto savininkų prieigą prie to **sąnaudų apskaitos analizės** Power BI turinį. Visi duomenys, esantys vizualizacijos bus tada filtruojamas pagal prieigos lygį, kuris valdo kaštų apskaitos. Norėdami sužinoti daugiau apie prieigos lygio sauga ir eilutės lygio saugumo, pamatyti [saugumo kaštų apskaitos kiekio nustatymas Power BI](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Naudotis prieigos prie turinio Power BI
Galite rasti ir **sąnaudų apskaitos analizės** Power BI turinio bendro naudojimo turto bibliotekoje Microsoft Dynamics gyvavimo ciklo paslaugų (LKD). Daugiau informacijos apie tai, kaip atsisiųsti turinį ir prijungti jį prie savo dinamika 365 operacijų duomenis, matyti, [LKD iš "Microsoft" ir savo partnerių kiekis Power BI](power-bi-content-microsoft-partners.md). **Pastaba:** KB4011327 ** ** yra būtina sąlyga tam, kad **sąnaudų apskaitos analizės** Power BI turinį.  Po to, kai prisijungiate prie paslaugų gyvavimo ciklą, galite pasiekti KB čia: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Rodikliai, kurie yra įtraukti į Power BI turinys
Turinys apima ataskaitų puslapių rinkinį. Kiekviename puslapyje sudaro metriką, kuri yra ryškinamos diagramas, plytelės ir lentelių rinkinys. Šioje lentelėje apžvelgiami vizualizacijas, kad **sąnaudų apskaitos analizės** Power BI turinį.

| Ataskaitų puslapio                      | Diagrama                                                                                                                         | Išklotinė                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Ry¹iù kainos tikrinimas pagal ataskaitinio laikotarpio    | Faktinių ir biudžeto išlaidas pagal išlaidų elementų hierarchijos lygį                                                                   | Faktinė kaina vs biudžeto išlaidų                    |
|                                  | Biudžeto dispersija iš sąnaudų elementų hierarchijos lygį                                                                               | Faktinių išlaidų tarifas prieš biudžeto išlaidų normos          |
|                                  | 10 geriausių nebrangių dispersija, procentinė dalis sąnaudų elementas                                                                          | Faktinį dydį prieš biudžeto dydį          |
| Ry¹iù kainos tikrinimas iš metai iki datos     | Faktinių ir biudžeto išlaidų pagal kalendorinių metų laikotarpį                                                                           | Faktinė kaina vs biudžeto išlaidų                    |
|                                  | Biudžeto dispersiją pagal kalendorinių metų laikotarpį                                                                                       | Faktinių išlaidų tarifas prieš biudžeto išlaidų normos          |
|                                  | 10 geriausių nebrangių dispersija, procentinė dalis sąnaudų elementas                                                                          | Faktinį dydį prieš biudžeto dydį          |
| Išlaidų tarifas pagal finansinius metus         | Faktinių išlaidų tarifas iš išlaidų elgesys                                                                                             | Faktinių išlaidų tarifas prieš biudžeto išlaidų normos          |
|                                  | Faktinių išlaidų tarifas, biudžeto išlaidų dydžio dispersija, biudžeto išlaidų procento ir biudžeto išlaidų tarifas iš sąnaudų elementų hierarchijos lygį | Faktinį dydį prieš biudžeto dydį          |
|                                  | Biudžeto dispersija iš sąnaudų elementų hierarchijos lygį                                                                               |                                               |
|                                  | 10 geriausių nebrangių dispersija, procentinė dalis sąnaudų elementas                                                                          |                                               |
| Lankstus biudžetas pagal ataskaitinio laikotarpio | Faktinių išlaidų, biudžeto išlaidų ir kintamo biudžeto išlaidų iš sąnaudų elementų hierarchijos lygį                                             | Faktinį dydį prieš biudžeto dydį          |
|                                  | Biudžeto dispersija ir kintamo biudžeto dispersija iš sąnaudų elementų hierarchijos lygį                                                  | Faktines išlaidas palyginti kintamo biudžeto išlaidų           |
|                                  | Faktinių išlaidų, biudžeto išlaidų ir lankstus išlaidų kainavo elgesį ir sąnaudų elementų hierarchijos lygį                                  | Faktinių išlaidų tarifas palyginti kintamo biudžeto išlaidų tarifas |
| Ataskaitinio laikotarpio sąnaudomis pareiškimas  | Faktinių išlaidų elementų hierarchijos lygį ir išlaidų objekto matmuo nario vardą                                             |                                               |
|                                  | Faktinių išlaidų objekto matmuo nario vardą ir sąnaudų elementas dimensijos valstybės pavadinimas                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
Dinamika 365 operacijų duomenys yra naudojamas užpildyti ataskaitos puslapius ir **sąnaudų apskaitos analizės** Power BI turinį. Šie duomenys yra vaizduojamas kaip bendra matavimų, kurie yra pastatytas įmonės parduotuvėje, kuri yra "Microsoft" SQL duomenų bazę, kuri yra optimizuota Google analytics. Daugiau informacijos rasite [apžvalga, Power BI integracija su įmonės parduotuvė](power-bi-integration-entity-store.md). Šie pagrindiniai bendra matavimai naudojami turinio pagrindu.

| Objektas                  | Pagrindinis bendras matavimo | Duomenų šaltinis Dynamics 365 operacijoms | Laukas     | aprašymas                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Kaštų apskaitos įrašai | SUM(amount)               | CAMDATAAggregatedCostEntry                  | Suma    | Kaštų apskaitos knygos valiutos suma |
| Statistiniai įrašai     | SUM(magnitude)            | CAMDATAAggregatedStatisctialEntry           | Reikšmė |                                               |

Ši lentelė parodo, kaip pagrindinis bendras matavimai naudojami sukurti keletą apskaičiuotus matavimus ir turinio duomenų rinkinyje.

| Mato vnt.                                       | Kaip apskaičiuojamas priemonė                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Faktinės išlaidos                                   | SKAIČIUOTI ("sąnaudų apskaitos įrašai"\[priemonės\], "Operacija versijos"\[ISSOURCEVERSIONBUDGET\_vertė\] = 0)            |
| Biudžeto išlaidos                                   | SKAIČIUOTI ("sąnaudų apskaitos įrašai"\[priemonės\], "Operacija versijos"\[ISSOURCEVERSIONBUDGET\_vertė\] = 1)            |
| Biudžeto išlaidų nukrypimas                          | \[Biudžeto išlaidos\] - \[faktinės išlaidos\]                                                                                      |
| Biudžeto nukrypimo procentas                    | Jei (\[biudžeto išlaidų\] = 0, blank(), \[biudžeto dispersijos\] / \[biudžeto išlaidų\])                                                |
| Tikrasis dydis                              | SKAIČIUOTI ('Statistikos įrašai'\[FullMagnitude\], "Sandorio versijos"\[ISSOURCEVERSIONBUDGET\_vertė\] = 0)          |
| Biudžeto dydį                              | SKAIČIUOTI (\[FullMagnitude\], "Operacija versijos"\[ISSOURCEVERSIONBUDGET\_vertė\] = 1)                               |
| Statistikos biudžeto dispersija                   | \[Biudžeto dydis\] - \[tikrasis dydis\]                                                                            |
| Statistikos biudžeto nukrypimo procentas        | Jei (\[biudžeto dydį\] = 0, blank(), \[statistikos biudžeto dispersijos\] / \[biudžeto dydį\])                          |
| Faktinių išlaidų tarifas                              | Jei (\[tikrasis dydis\] = 0, BLANK(), \[faktinės sąnaudos\] / \[tikrasis dydis\])                                          |
| Biudžeto išlaidų tarifas                              | Jei (\[biudžeto dydį\] = 0, BLANK(), \[biudžeto išlaidos\] / \[biudžeto dydį\])                                          |
| Biudžeto išlaidų normos dispersija                     | \[Biudžeto išlaidų normos\] - \[tikrasis išlaidų tarifas\]                                                                            |
| Biudžeto išlaidų normos nukrypimo procentas          | Jei (\[biudžeto išlaidų\] = 0, blank(), \[biudžeto išlaidų dydžio dispersijos\] / \[biudžeto išlaidų tarifas\])                                 |
| Ilgalaikio biudžeto išlaidų                             | SKAIČIUOTI (\[biudžeto išlaidų\], 'Sąnaudų apskaitos įrašai'\[COSTBEHAVIOR\] = 1)                                              |
| Kintamo biudžeto išlaidų                          | SKAIČIUOTI (\[biudžeto išlaidų\], 'Sąnaudų apskaitos įrašai'\[COSTBEHAVIOR\] = 2)                                              |
| Fiksuotas kintamo biudžeto išlaidų                    | \[Ilgalaikio biudžeto išlaidų\]                                                                                                  |
| Kintamojo kintamo biudžeto išlaidų                 | Jei (\[biudžeto dydį\] = 0, BLANK(), (\[kintamo biudžeto išlaidos\] / \[biudžeto dydį\]) \*\[tikrasis dydis\])       |
| Kintamo biudžeto išlaidų                          | \[Nustatytas kintamo biudžeto išlaidos\] + \[kintamojo kintamo biudžeto išlaidų\]                                                     |
| Lankstus biudžetas dispersija                      | \[Kintamo biudžeto išlaidos\] - \[faktinės išlaidos\]                                                                             |
| Lankstus biudžetas nukrypimo procentas           | Jei (\[kintamo biudžeto išlaidų\] = 0, BLANK(), \[kintamame biudžete dispersijos\] / \[kintamo biudžeto išlaidų\])                     |
| Kintamo biudžeto išlaidų normos                     | Jei (\[tikrasis dydis\] = 0, BLANK(), \[kintamo biudžeto išlaidos\] / \[tikrasis dydis\])                                 |
| Kintamo biudžeto išlaidų dydžio dispersija            | \[Kintamo biudžeto išlaidų tarifas\] - \[tikrasis išlaidų tarifas\]                                                                   |
| Kintamo biudžeto išlaidų norma nukrypimo procentas | Jei (\[kintamo biudžeto išlaidų tarifas\] = 0, BLANK(), \[kintamo biudžeto išlaidų dydžio dispersijos\] / \[kintamo biudžeto išlaidų tarifas\]) |

Pagrindiniai matmenys yra naudojamas kaip filtrų Supjaustykite bendra matavimų pasiekti didesnio detalumo ir suteikia gilesnių analitinių įžvalgų.

| Objektas                             | Atributų pavyzdžiai                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Savikainos apskaitos didžiosios knygos            | Savikainos apskaitos didžioji knyga                                                                                               |
| Savikainos kontrolės įtaisai                 | Savikainos kontrolės įtaiso pavadinimas                                                                                               |
| Savikainos elemento dimensijos            | Išlaidų elementai dimensijos pavadinimas, išlaidų elementas dimensijos valstybės pavadinimas, išlaidų elementas dimensijos valstybės Aprašymas          |
| Savikainos objekto dimensijos             | Išlaidų objektas dimensijos pavadinimas, išlaidų objekto matmuo valstybės pavadinimas, išlaidų objekto dimensijos valstybės Aprašymas              |
| Statistinės dimensijos             | Statistikos dimensijos pavadinimas, statistinis aspektas nario vardą, statistinis aspektas valstybės Aprašymas              |
| Išlaidų objektas dimensijų hierarchijas  | Kaina objekto dimensijų hierarchijos pavadinimas, išlaidų objekto dimensijų hierarchijos lygis, išlaidų objekto dimensijų hierarchijos medis    |
| Sąnaudų elementas dimensijų hierarchijas | Sąnaudų elementas dimensijų hierarchijos pavadinimas, išlaidų elementas dimensijų hierarchijos lygis, sąnaudų elementas dimensijų hierarchijos medis |
| Statistikos dimensijų hierarchijas  | Statistikos dimensijų hierarchijos pavadinimas, statistikos dimensijų hierarchijos lygis, statistikos dimensijų hierarchijos medis    |
| Operacijų versijos               | Versijos pavadinimas                                                                                                         |
| Finansiniai kalendoriai                   | Kalendorius, kalendorius Aprašymas                                                                                       |
| Finansinių metų                       | Kalendoriniai metai                                                                                                        |
| Ataskaitiniai laikotarpiai                     | Kalendorinių metų laikotarpį                                                                                                 |

## <a name="additional-resources"></a>Papildomi ištekliai
Toliau pateikti keli naudingi saitai, susiję su objektais ir „Power BI“ turinio kūrimu.

-   [Duomenų objektai](..\data-entities\data-entities.md)
-   [Organizacinių turinio paketų kūrimas](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Duomenų modeliavimas naudojant „Power BI“](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [„Power BI“ plytelių įtraukimas į darbo sritis](configure-power-bi-integration.md)
-   [Power BI saugumo kaštų apskaitos kiekio nustatymas](setup-security-cost-accounting-content-pack.md)


