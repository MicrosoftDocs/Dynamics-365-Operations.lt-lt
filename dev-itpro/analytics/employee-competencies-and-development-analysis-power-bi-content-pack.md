---
title: "Darbuotojo kompetencijų ir tobulėjimo „Power BI“ turinys"
description: "Šioje temoje aprašytas „Dynamics 365 for Operations“ darbuotojo kompetencijų ir tobulėjimo „Power BI“ turinys. Paaiškinama, kaip pasiekti į turinio paketą įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 770a832efe8ee2da44d65670b1818be4fcf4bcc0
ms.contentlocale: lt-lt
ms.lasthandoff: 05/25/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>Darbuotojo kompetencijų ir tobulėjimo „Power BI“ turinys

[!include[banner](../includes/banner.md)]


Šioje temoje aprašytas „Dynamics 365 for Operations“ darbuotojo kompetencijų ir tobulėjimo „Power BI“ turinys. Paaiškinama, kaip pasiekti į turinio paketą įtrauktas ataskaitas, ir pateikiama informacija apie duomenų modelį ir objektus, naudojamus turinio paketui kurti.

<a name="accessing-the-content-pack"></a>Prieiga prie turinio paketo
--------------------------

Darbuotojo kompetencijų ir tobulėjimo turinio paketą galite rasti bendrai naudojamo turto bibliotekoje „Microsoft Dynamics Lifecycle Services“ (LCS). Daugiau informacijos apie tai, kaip atsisiųsti turinio paketą ir prijungti jį prie „Microsoft Dynamics 365 for Operations“ duomenų, žr. [„Power BI“ turinys LCS iš „Microsoft“ ir jūsų partnerių](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Į turinio paketą įtrauktos ataskaitos
Prijungus turinio paketą prie „Dynamics 365 for Operations“ duomenų, ataskaitose rodomi jūsų organizacijos duomenys. Jei niekada nenaudojote „Microsoft Power BI“, daugiau apie tai galite sužinoti temoje [„Power BI“ mokymosi vedlio puslapis](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Į turinio paketą įtrauktose ataskaitose yra diagramos ir lentelės, kuriose pateikiama papildoma informacija. Tolesnėje lentelėje aprašomos ataskaitos.

| Ataskaita                            | Turinys                                               |
|-----------------------------------|--------------------------------------------------------|
| Kompetencijų ir tobulėjimo analizė | Komandos nario įgūdžių tipai ir komandos nario įgūdžiai pagal tipą |
| Įgūdžių šablonas                     | Pasirinkto darbuotojo įgūdžių šablonas                |
| Įgūdžių analizė                    | Įgūdžiai pagal tipą ir įvertinimą                              |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
„Dynamics 365 for Operations“ duomenys naudojami ataskaitoms darbuotojo kompetencijų ir tobulėjimo turinio pakete užpildyti. Toliau pateiktoje lentelėje nurodomi objektai, kuriais turinio paketas pagrįstas.

| Objektas                            | Turinys                                                                                                   | Ryšiai su kitais objektais                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Workforce\_CalendarOffset         | Kalendoriaus poslinkiai ataskaitoms skaidyti                                                                          |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Company                | Įmonės, pagal kurias filtruojamos ataskaitos                                                                             |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Compensation           | Užmokesčio tarifas ir dažnis per tam tikrą laikotarpį                                                                           |                                                                                                                                                                                                                                                                                                         |
| Workforce\_CurrentCompensation    | Užmokesčio tarifas ir dažnis dabartinę dieną                                                              | Workforce\_Company Workforce\_CurrentCompensation Workforce\_Demographics Workforce\_Job Workforce\_Position                                                                                                                                                                                            |
| Workforce\_CurrentPosition        | Pareigos dabartinę datą, viso etato ekvivalentas (FTE), laisvos darbo vietos ir laisvos / užimtos darbo vietos | Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                                      |
| Workforce\_CurrentWorker          | Darbuotojai dabartinę dieną, amžius ir darbuotojų skaičius                                                         | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_PersonSkill Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Job Workforce\_Employment Workforce\_Position                     |
| Workforce\_Date                   | Dienos, savaitės, mėnesiai ir metai                                                                             |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Demographics           | Gimimo data, lytis etninė kilmė ir šeimyninė padėtis                                                   |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Employment             | Pradžios data, pabaigos data ir perėjimo data                                                                  |                                                                                                                                                                                                                                                                                                         |
| Workforce\_GeographicLocation     | Miestas, seniūnija, pašto kodas ir šalis arba regionas                                                           |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Job                    | Funkcija, tipas ir pareigos                                                                                  |                                                                                                                                                                                                                                                                                                         |
| Workforce\_JobPreferredSkill      | Svarba, įvertinimas, įgūdis ir įgūdžio lygis                                                                 | Workforce\_Skill Workforce\_Job                                                                                                                                                                                                                                                                         |
| Workforce\_PastPositionAssignment | Priskyrimo priežastis, pradžios data, pabaigos data ir užduotis                                                           | Workforce\_ClaendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_Performance            | Įvertinimas, aprašas ir įvertinimo modelis                                                                      |                                                                                                                                                                                                                                                                                                         |
| Workforce\_PersonSkill            | Lygis, lygio data ir įgūdis                                                                               | Workforce\_Skill                                                                                                                                                                                                                                                                                        |
| Workforce\_PersonSkillAnalysis    | Patvirtintas, lygis, lygio data ir įgūdis                                                                    | Workforce\_WorkerName Workforce\_Skill                                                                                                                                                                                                                                                                  |
| Workforce\_Position               | Padalinys, FTE, pareigos, pareigų tipas ir pareigos                                                        |                                                                                                                                                                                                                                                                                                         |
| Workforce\_PositionTrend          | Pareigos per tam tikrą laikotarpį, FTE ir užduotis                                                                          | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_ReportsToWorkerName    | Vardas, pavardė ir vardas bei pavardė                                                                       |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Skill                  | Įgūdis, įgūdžio tipas ir įvertinimas                                                                              |                                                                                                                                                                                                                                                                                                         |
| Workforce\_TerminatedWorker       | Atleisti darbuotojai, atleidimo data, pareigos ir užduotis                                             | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position |
| Workforce\_WorkerName             | Vardas, pavardė ir vardas bei pavardė                                                                       |                                                                                                                                                                                                                                                                                                         |
| Workforce\_WorkerTitle            | Pareigos ir paaukštinimo data                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce\_WorkerTrend             | Darbuotojai per tam tikrą laiką, darbuotojų skaičius, įmonė ir pareigos                                                        | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job                     |

Šie objektai buvo naudojami skaičiuojamiems matams duomenų modelyje sukurti. Tada šie skaičiuojami matai naudojami skaičiuojant pagrindinius efektyvumo indikatorius (KPI) ir ataskaitas, naudojamas turinio pakete. Jei norite į ataskaitas ir ataskaitų sritį įtraukti papildomų skaičiavimų, galite iš LCS atsisiųsti ir modifikuoti failą CompetenciesandDevelopment.pbix. Šis failas yra numatytasis duomenų modelis, kuris buvo naudojamas turinio paketui kurti. Atlikę keitimus, galite kurti organizacinį turinio paketą ir ataskaitų sritį, kuriuose yra jūsų įtraukta informacija.

## <a name="additional-resources"></a>Papildomi ištekliai
Toliau pateikti keli naudingi saitai, susiję su objektais ir „Power BI“ turinio kūrimu.

-   [Duomenų objektai](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organizacinių turinio paketų kūrimas](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Duomenų modeliavimas naudojant „Power BI“](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [„Power BI“ plytelių įtraukimas į darbo sritis](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





