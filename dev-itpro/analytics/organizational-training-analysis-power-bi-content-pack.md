---
title: Organizacijos mokymo Power BI turinys
description: "Šioje temoje aprašoma Dynamics 365 operacijų - organizacijos mokymo Power BI turinį. Tai paaiškinama kaip prieiti prie turinio pack, ir aprašomi duomenų modelis ir subjektai, kurie buvo naudojami sukurti turinio paketas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 104164f8ffd0d2bc3a64bf15d2fb5213234046ce
ms.lasthandoff: 03/31/2017


---

# <a name="organizational-training-power-bi-content"></a>Organizacijos mokymo Power BI turinys

Šioje temoje aprašoma Dynamics 365 operacijų - organizacijos mokymo Power BI turinį. Tai paaiškinama kaip prieiti prie turinio pack, ir aprašomi duomenų modelis ir subjektai, kurie buvo naudojami sukurti turinio paketas.

<a name="accessing-the-content-pack"></a>Prieiga prie turinio paketas
--------------------------

Organizacijos mokymo turinio paketą galite rasti bendro naudojimo turto bibliotekoje Microsoft Dynamics gyvavimo ciklo paslaugų (LKD). Daugiau informacijos apie tai, kaip atsisiųsti turinio paketą ir prijungti jį prie savo "Microsoft Dynamics 365" operacijų duomenų, rasite [LCS iš "Microsoft" ir savo partnerių kiekis Power BI](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Pranešimų, kurie yra įtraukti į turinio paketas
Prijungę turinio pack Dynamics "365" operacijų duomenų ataskaitose nurodoma organizacijos duomenis. Jei niekada nenaudojote "Microsoft" Power BI prieš, galite sužinoti daugiau apie tai ant to [vadovaujasi mokymosi puslapis, Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Pranešimų, kurie yra įtraukti į turinio paketas yra diagramos ir lentelės, kuriose papildomos informacijos. Tolesnėje lentelėje aprašomos ataskaitos.

| Ataskaita          | Turinys                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Priežasčių analizę | Registracijos vietovę, kursų dalyvių statusas bei registracijos sąrašas |
| Kursų tipus    | Kursų tipai pagal įgūdžius                                                       |

Galite filtruoti diagramas bei plyteles ant šios ataskaitos ir grafikai ir plytelės prie prietaisù skydelio. Daugiau informacijos apie filtro ir PIN kodą, Power BI, rasite [kurti ir konfigūruoti ataskaitų srities A](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
Dinamika 365 operacijų duomenys yra naudojamas užpildyti ataskaitos organizacijos mokymo turinio paketas. Šioje lentelėje subjektų buvo pagrįsta turinio paketas.

| Objektas                    | Turinys                                                         | Santykių su kitais subjektais                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mokymo\_CalendarOffset  | Kalendorinių kompensuoja gabaliuką ataskaitas                                | Mokymo\_CourseAgenda mokymo\_CourseAttendees                                                                                                                                                   |
| Mokymo\_įmonė         | Bendrovės filtruoti ataskaitas                                   | Mokymo\_CourseAgenda mokymo\_CourseAttendees                                                                                                                                                   |
| Mokymo\_kursai          | Žinoma, aprašymas, instruktoriaus vardas, vietą, numeris ir statusas | Mokymo\_CourseAgenda mokymo\_CourseAttendees mokymo\_CourseSkill                                                                                                                             |
| Mokymo\_CourseAgenda    | Darbotvarkės, žinoma ir pradžios ir pabaigos laiką                          | Mokymo\_apmokymo įmonėje\_CalendarOffset mokymo\_šiol mokymo\_kursai                                                                                                                         |
| Mokymo\_CourseAttendees | Pavadinimas, statusas, darbo ir registracijos data                         | Mokymo\_apmokymo įmonėje\_CalendarOffset mokymo\_šiol mokymo\_gyventojai mokymo\_darbo mokymą\_kursai mokymo\_WorkerName mokymo\_WorkerTitle mokymo\_profesinį mokymą\_pozicija |
| Mokymo\_CourseSkill     | Įgūdžių, įgūdžio tipą ir lygį                                     | Mokymo\_kursai                                                                                                                                                                                   |
| Mokymo\_dienos            | Dienas, savaites, mėnesius ir metus                                   | Mokymo\_CourseAgenda mokymo\_CourseAttendees                                                                                                                                                   |
| Mokymo\_demografija    | Data gimimo, lyties, etninės kilmės ir šeimyninė padėtis         | Mokymo\_CourseAgenda mokymo\_CourseAttendees                                                                                                                                                   |
| Mokymo\_darbo      | Pradžios data, pabaigos data ir perėjimo data                        | Mokymo\_CourseAgenda mokymo\_CourseAttendees                                                                                                                                                   |
| Mokymo\_darbo             | Funkciją, tipas ir pavadinimas                                        | Mokymo\_CourseAgenda mokymo\_CourseAttendees                                                                                                                                                   |
| Mokymo\_pozicija        | Pozicija, pavadinimas ir dirbančius (FTE)                  | Mokymo\_CourseAgenda mokymo\_CourseAttendees                                                                                                                                                   |
| Mokymo\_WorkerName      | Vardas, pavardė ir vardas, pavardė                             | Mokymo\_CourseAttendees                                                                                                                                                                          |
| Mokymo\_WorkerTitle     | Pavadinimas ir stažo data                                         | Mokymo\_CourseAttendees                                                                                                                                                                          |

Šių subjektų buvo naudojama siekiant sukurti apskaičiuojamieji matai duomenų modelio. Tai apskaičiuojama priemonės naudojami apskaičiuoti pagrindinius veiklos rodiklius (KPI) ir ataskaitų, kurias naudoja turinio paketas. Jei norite įtraukti papildomų skaičiavimų ataskaitos ir prietaisų skydelio, galite atsisiųsti ir pakeisti Training.pbix failą iš LKD. Šis failas yra numatytasis duomenų modelis, kuris buvo naudojamas sukurti turinio paketas. Po to, kai jūs atlikote pakeitimus, galite sukurti organizacijos turinio paketas ir valdymo skydelį, kuriame yra informacija, kurią įtraukėte.

## <a name="additional-resources"></a>Papildomi ištekliai
Toliau pateikti keli naudingi saitai, susiję su objektais ir „Power BI“ turinio kūrimu.

-   [Duomenų objektai](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organizacinių turinio paketų kūrimas](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Duomenų modeliavimas naudojant „Power BI“](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [„Power BI“ plytelių įtraukimas į darbo sritis](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



