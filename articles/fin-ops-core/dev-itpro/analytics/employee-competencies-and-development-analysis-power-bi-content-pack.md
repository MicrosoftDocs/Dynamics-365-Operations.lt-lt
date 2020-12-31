---
title: Darbuotojų kompetencijų ir tobulinimo „Power BI“ turinys
description: Šioje temoje aprašomas „Power BI“ turinys Darbuotojo kompetencijos ir tobulėjimas.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bed461677cbdfa57b0a198b7179eccb9828dc944
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687131"
---
# <a name="employee-competencies-and-development-power-bi-content"></a>Darbuotojų kompetencijų ir tobulinimo „Power BI“ turinys

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomas „Power BI“ turinys Darbuotojo kompetencijos ir tobulėjimas. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Į turinio paketą įtrauktos ataskaitos
Prijungus turinio paketą prie duomenų, ataskaitose rodomi jūsų organizacijos duomenys. Jei niekada nenaudojote „Microsoft Power BI“, daugiau apie tai galite sužinoti temoje [„Power BI“ mokymosi vedlio puslapis](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Į turinio paketą įtrauktose ataskaitose yra diagramos ir lentelės, kuriose pateikiama papildoma informacija. Tolesnėje lentelėje aprašomos ataskaitos.

| Ataskaita                            | Turinys                                               |
|-----------------------------------|--------------------------------------------------------|
| Kompetencijų ir tobulėjimo analizė | Komandos nario įgūdžių tipai ir komandos nario įgūdžiai pagal tipą |
| Įgūdžių šablonas                     | Pasirinkto darbuotojo įgūdžių šablonas                |
| Įgūdžių analizė                    | Įgūdžiai pagal tipą ir įvertinimą                              |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
Programos duomenys naudojami ataskaitoms darbuotojo kompetencijų ir tobulėjimo turinio pakete užpildyti. Toliau pateiktoje lentelėje nurodomi objektai, kuriais turinio paketas pagrįstas.

| Objektas                            | Turinys                                                                                                   | Ryšiai su kitais objektais |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | Kalendoriaus poslinkiai ataskaitoms skaidyti                                                                          | |
| Workforce\_Company                | Įmonės, pagal kurias filtruojamos ataskaitos                                                                             | |
| Workforce\_Compensation           | Užmokesčio tarifas ir dažnis per tam tikrą laikotarpį                                                                           | |
| Workforce\_CurrentCompensation    | Užmokesčio tarifas ir dažnis dabartinę dieną                                                              | Workforce\_Company, Workforce\_CurrentCompensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentPosition        | Pareigos dabartinę datą, viso etato ekvivalentas (FTE), laisvos darbo vietos ir laisvos / užimtos darbo vietos | Workforce\_Job Workforce\_Position |
| Workforce\_CurrentWorker          | Darbuotojai dabartinę dieną, amžius ir darbuotojų skaičius                                                         | Workforce\_Company Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_PersonSkill, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position |
| Workforce\_Date                   | Dienos, savaitės, mėnesiai ir metai                                                                             | |
| Workforce\_Demographics           | Gimimo data, lytis etninė kilmė ir šeimyninė padėtis                                                   | |
| Workforce\_Employment             | Pradžios data, pabaigos data ir perėjimo data                                                                  | |
| Workforce\_GeographicLocation     | Miestas, seniūnija, pašto kodas ir šalis arba regionas                                                           | |
| Workforce\_Job                    | Funkcija, tipas ir pareigos                                                                                  | |
| Workforce\_JobPreferredSkill      | Svarba, įvertinimas, įgūdis ir įgūdžio lygis                                                                 | Workforce\_Skill, Workforce\_Job |
| Workforce\_PastPositionAssignment | Priskyrimo priežastis, pradžios data, pabaigos data ir užduotis                                                           | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_Performance            | Įvertinimas, aprašas ir įvertinimo modelis                                                                      | |
| Workforce\_PersonSkill            | Lygis, lygio data ir įgūdis                                                                               | Workforce\_Skill |
| Workforce\_PersonSkillAnalysis    | Patvirtintas, lygis, lygio data ir įgūdis                                                                    | Workforce\_WorkerName, Workforce\_Skill |
| Workforce\_Position               | Padalinys, FTE, pareigos, pareigų tipas ir pareigos                                                        | |
| Workforce\_PositionTrend          | Pareigos per tam tikrą laikotarpį, FTE ir užduotis                                                                          | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_ReportsToWorkerName    | Vardas, pavardė ir vardas bei pavardė                                                                       | |
| Workforce\_Skill                  | Įgūdis, įgūdžio tipas ir įvertinimas                                                                              | |
| Workforce\_TerminatedWorker       | Atleisti darbuotojai, atleidimo data, pareigos ir užduotis                                             | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position |
| Workforce\_WorkerName             | Vardas, pavardė ir vardas bei pavardė                                                                       | |
| Workforce\_WorkerTitle            | Pareigos ir paaukštinimo data                                                                                   | |
| Workorce\_WorkerTrend             | Darbuotojai per tam tikrą laiką, darbuotojų skaičius, įmonė ir pareigos                                                        | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job |
