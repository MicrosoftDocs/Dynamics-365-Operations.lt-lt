---
title: "Darbuotojų kompetencijos ir plėtros Power BI turinio"
description: "Šioje temoje aprašoma Dynamics 365 operacijų - darbuotojų kompetencijas ir plėtros Power BI turinį. Jis paaiškina, kaip pasiekti ataskaitas, kurios įtraukiamos į turinio paketą, ir pateikia informaciją apie duomenų modelio ir subjektai, kurie buvo naudojami sukurti turinio paketas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1fd6f978b6a871f9f7d3d5e91ab3e0aac789ae88
ms.lasthandoff: 03/31/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>Darbuotojų kompetencijos ir plėtros Power BI turinio

Šioje temoje aprašoma Dynamics 365 operacijų - darbuotojų kompetencijas ir plėtros Power BI turinį. Jis paaiškina, kaip pasiekti ataskaitas, kurios įtraukiamos į turinio paketą, ir pateikia informaciją apie duomenų modelio ir subjektai, kurie buvo naudojami sukurti turinio paketas.

<a name="accessing-the-content-pack"></a>Prieiga prie turinio paketas
--------------------------

Jūs galite rasti darbuotojų kompetencijas ir plėtros turinio pack bendro naudojimo turto bibliotekoje Microsoft Dynamics gyvavimo ciklo paslaugų (LKD). Daugiau informacijos apie tai, kaip atsisiųsti turinio paketą ir prijungti jį prie savo "Microsoft Dynamics 365" operacijų duomenų, rasite [LCS iš "Microsoft" ir savo partnerių kiekis Power BI](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Pranešimų, kurie yra įtraukti į turinio paketas
Prijungę turinio pack Dynamics "365" operacijų duomenų ataskaitose nurodoma organizacijos duomenis. Jei niekada nenaudojote "Microsoft" Power BI prieš, galite sužinoti daugiau apie tai ant to [vadovaujasi mokymosi puslapis, Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Pranešimų, kurie yra įtraukti į turinio paketas yra diagramos ir lentelės, kuriose papildomos informacijos. Tolesnėje lentelėje aprašomos ataskaitos.

| Ataskaita                            | Turinys                                               |
|-----------------------------------|--------------------------------------------------------|
| Kompetencijos ir plėtros analizė | Komandos narė įgūdžių tipus ir komandos narių įgūdžius pagal tipą |
| Įgūdžių šabloną                     | Įgūdžių šabloną pasirinkto darbuotojo                |
| Įgūdžių analizė                    | Įgūdžių tipas ir vardinė galia                              |

Galite filtruoti diagramas bei plyteles ant šios ataskaitos ir grafikai ir plytelės prie prietaisù skydelio. Daugiau informacijos apie filtro ir PIN kodą, Power BI, rasite [kurti ir konfigūruoti ataskaitų srities A](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
Dinamika 365 operacijų duomenys yra naudojamas užpildyti ataskaitos darbuotojų kompetencijas ir plėtros turinio paketas. Šioje lentelėje subjektų buvo pagrįsta turinio paketas.

| Objektas                            | Turinys                                                                                                   | Santykių su kitais subjektais                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Darbo jėgos\_CalendarOffset         | Kalendorinių kompensuoja gabaliuką ataskaitas                                                                          |                                                                                                                                                                                                                                                                                                         |
| Darbo jėgos\_įmonė                | Bendrovės filtruoti ataskaitas                                                                             |                                                                                                                                                                                                                                                                                                         |
| Darbo jėgos\_kompensacijos           | Užmokesčio tarifas ir dažnis bėgant                                                                           |                                                                                                                                                                                                                                                                                                         |
| Darbo jėgos\_CurrentCompensation    | Mokėjimo koeficientą ir dažnių esamą                                                              | Darbo jėgos\_įmonės darbuotojams\_CurrentCompensation darbo jėgos\_darbo jėgos demografija\_darbo jėgos\_pozicija                                                                                                                                                                                            |
| Darbo jėgos\_CurrentPosition        | Pozicijas nuo dabartinės datos, dirbančius (FTE), atvirų pozicijų ir atidaryti užpildyti vietas | Darbo jėgos\_darbo jėgos\_pozicija                                                                                                                                                                                                                                                                      |
| Darbo jėgos\_CurrentWorker          | Darbuotojų dabartinės datos, amžiaus ir skaičiaus apskaičiavimas                                                         | Darbo jėgos\_įmonės darbuotojų\_kompensacijos darbuotojams\_GeographicLocation darbo jėgos\_darbo jėgos našumo\_PersonSkill darbo jėgos\_WorkerName darbo jėgos\_ReportsToWorkerName darbo jėgos\_WorkerTitle darbo jėgos\_darbo jėgos demografija\_darbo jėgos\_darbo jėgos\_pozicija                     |
| Darbo jėgos\_dienos                   | Dienas, savaites, mėnesius ir metus                                                                             |                                                                                                                                                                                                                                                                                                         |
| Darbo jėgos\_demografija           | Data gimimo, lyties, etninės kilmės ir šeimyninė padėtis                                                   |                                                                                                                                                                                                                                                                                                         |
| Darbo jėgos\_darbo             | Pradžios data, pabaigos data ir perėjimo data                                                                  |                                                                                                                                                                                                                                                                                                         |
| Darbo jėgos\_GeographicLocation     | Miesto, apskrities, pašto kodas, ir valstiją arba provinciją                                                           |                                                                                                                                                                                                                                                                                                         |
| Darbo jėgos\_darbo                    | Funkciją, tipas ir pavadinimas                                                                                  |                                                                                                                                                                                                                                                                                                         |
| Darbo jėgos\_JobPreferredSkill      | Svarbą, reitingas, įgūdžių ir įgūdžių lygis                                                                 | Darbo jėgos\_darbo jėgos įgūdžių\_darbo                                                                                                                                                                                                                                                                         |
| Darbo jėgos\_PastPositionAssignment | Priskyrimo priežastis, pradžios datą, pabaigos datą ir darbo                                                           | Darbo jėgos\_ClaendarOffset darbo jėgos\_šiol darbo jėgos\_darbo jėgos\_pozicija                                                                                                                                                                                                                            |
| Darbo jėgos\_veiklos            | Reitingas, apibūdinimo ir vertinimo modelis                                                                      |                                                                                                                                                                                                                                                                                                         |
| Darbo jėgos\_PersonSkill            | Lygio ir lygio datą įgūdžių                                                                               | Darbo jėgos\_įgūdžių                                                                                                                                                                                                                                                                                        |
| Darbo jėgos\_PersonSkillAnalysis    | Sertifikuotos, lygio, lygį datą ir įgūdžių                                                                    | Darbo jėgos\_WorkerName darbo\_įgūdžių                                                                                                                                                                                                                                                                  |
| Darbo jėgos\_pozicija               | Departamentas, visos darbo dienos ekvivalentas, pozicija, pozicijos tipas ir pavadinimas                                                        |                                                                                                                                                                                                                                                                                                         |
| Darbo jėgos\_PositionTrend          | Bėgant laikui, visos darbo dienos ekvivalentas ir darbo vietų                                                                          | Darbo jėgos\_CalendarOffset darbo jėgos\_šiol darbo jėgos\_darbo jėgos\_pozicija                                                                                                                                                                                                                            |
| Darbo jėgos\_ReportsToWorkerName    | Vardas, pavardė ir vardas, pavardė                                                                       |                                                                                                                                                                                                                                                                                                         |
| Darbo jėgos\_įgūdžių                  | Įgūdžių, įgūdžio tipą ir Vertinimas                                                                              |                                                                                                                                                                                                                                                                                                         |
| Darbo jėgos\_TerminatedWorker       | Nutraukta darbuotojų, galiojimo pabaigos data, pavadinimas, pozicijos ir darbo                                             | Darbo jėgos\_įmonės darbuotojų\_kompensacijos darbuotojams\_GeographicLocation darbo jėgos\_darbo jėgos našumo\_WorkerName darbo jėgos\_ReportsToWorkerName darbo jėgos\_CalendarOffset darbo jėgos\_dienos darbo jėgos\_WorkerTitle darbo jėgos\_darbo jėgos demografija\_darbo jėgos\_darbo jėgos\_pozicija |
| Darbo jėgos\_WorkerName             | Vardas, pavardė ir vardas, pavardė                                                                       |                                                                                                                                                                                                                                                                                                         |
| Darbo jėgos\_WorkerTitle            | Pavadinimas ir stažo data                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce\_WorkerTrend             | Darbuotojų laiko, darbuotojų skaičius, įmonės ir pozicijos                                                        | Darbo jėgos\_įmonės darbuotojų\_kompensacijos darbuotojams\_GeographicLocation darbo jėgos\_darbo jėgos našumo\_WorkerName darbo jėgos\_ReportsToWorkerName darbo jėgos\_CalendarOffset darbo jėgos\_dienos darbo jėgos\_WorkerTitle darbo jėgos\_darbo jėgos demografija\_darbo jėgos\_darbo                     |

Šių subjektų buvo naudojama siekiant sukurti apskaičiuojamieji matai duomenų modelio. Tai apskaičiuojama priemonės naudojami apskaičiuoti pagrindinius veiklos rodiklius (KPI) ir ataskaitų, kurias naudoja turinio paketas. Jei norite įtraukti papildomų skaičiavimų ataskaitos ir prietaisų skydelio, galite atsisiųsti ir pakeisti CompetenciesandDevelopment.pbix failą iš LKD. Šis failas yra numatytasis duomenų modelis, kuris buvo naudojamas sukurti turinio paketas. Po to, kai jūs atlikote pakeitimus, galite sukurti organizacijos turinio paketas ir valdymo skydelį, kuriame yra informacija, kurią įtraukėte.

## <a name="additional-resources"></a>Papildomi ištekliai
Toliau pateikti keli naudingi saitai, susiję su objektais ir „Power BI“ turinio kūrimu.

-   [Duomenų objektai](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organizacinių turinio paketų kūrimas](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Duomenų modeliavimas naudojant „Power BI“](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [„Power BI“ plytelių įtraukimas į darbo sritis](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



