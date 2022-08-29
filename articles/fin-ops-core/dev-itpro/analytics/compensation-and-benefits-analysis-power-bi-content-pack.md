---
title: Kompensacijų ir išmokų „Power BI“ turinys
description: Šiame straipsnyje aprašomas kompensacijų ir išmokų Power BI turinys.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.openlocfilehash: 978aa4897c58518c430decd8570fa30c851349aa
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291865"
---
# <a name="compensation-and-benefits-power-bi-content"></a>Kompensacijų ir išmokų „Power BI“ turinys

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomas kompensacijų ir išmokų Power BI turinys. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Į turinio paketą įtrauktos ataskaitos
Prijungus turinio paketą prie duomenų, ataskaitose rodomi jūsų organizacijos duomenys. Jei niekada nenaudojote „Microsoft Power BI“, daugiau apie tai galite sužinoti temoje [„Power BI“ mokymosi vedlio puslapis](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Į turinio paketą įtrauktose ataskaitose yra diagramos ir lentelės, kuriose pateikiama papildoma informacija. Tolesnėje lentelėje aprašomos ataskaitos.

| Ataskaita                     | Turinys                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Kompensacijų ir išmokų analizė | Valandinį ir fiksuotą užmokestį gaunantys darbuotojai pagal įmonę, vidutinis valandinis užmokestis, vidutinis fiksuotas užmokestis, darbuotojai pagal įdarbinimo tipą ir plano registracija |
| Darbuotojų išmokos          | Darbuotojo registravimas pagal pasirinktą išmoką                                                                                               |

Šių ataskaitų diagramas ir plyteles galima filtruoti ir prisegti prie ataskaitų srities. Daugiau informacijos apie tai, kaip „Power BI“ filtruoti ir prisegti, žr. [Ataskaitų srities kūrimas ir konfigūravimas](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Duomenų modelio ir objektų supratimas
Programos duomenys naudojami ataskaitoms kompetencijų ir išmokų turinio pakete užpildyti. Toliau pateiktoje lentelėje nurodomi objektai, kuriais turinio paketas pagrįstas.

| Objektas                            | Turinys                                                                                                   | Ryšiai su kitais objektais |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | Kalendoriaus poslinkiai ataskaitoms skaidyti                                                                          | Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_WorkerTrend, Workforce\_TerminatedWorker |
| Workforce\_Company                | Įmonės, pagal kurias filtruojamos ataskaitos                                                                             | Workforce\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Compensation           | Užmokesčio tarifas ir dažnis per tam tikrą laikotarpį                                                                           | Workforce\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_CurrentCompensation    | Užmokesčio tarifas ir dažnis dabartinę dieną                                                              | Workforce\_Company, Workforce\_Compensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentPosition        | Pareigos dabartinę datą, viso etato ekvivalentas (FTE), laisvos darbo vietos ir laisvos / užimtos darbo vietos | Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentWorker          | Darbuotojai dabartinę dieną, amžius ir darbuotojų skaičius                                                         | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position, Workforce\_WorkerBenefit |
| Workforce\_Date                   | Dienos, savaitės, mėnesiai ir metai                                                                             | Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Demographics           | Gimimo data, lytis etninė kilmė ir šeimyninė padėtis                                                   | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Employment             | Pradžios data, pabaigos data ir perėjimo data                                                                  | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_GeographicLocation     | Miestas, seniūnija, pašto kodas ir šalis arba regionas                                                           | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Job                    | Funkcija, tipas ir pareigos                                                                                  | Workforce\_CurrentPosition, Workforce\_CurrentWorker |
| Workforce\_PastPositionAssignment | Priskyrimo priežastis, pradžios data, pabaigos data ir užduotis                                                           | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_Performance            | Įvertinimas, aprašas ir įvertinimo modelis                                                                      | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Position               | Padalinys, FTE, pareigos, pareigų tipas ir pareigos                                                        | Workforce\_CurrentPosition, Workforce\_CurrentWorker |
| Workforce\_PositionTrend          | Pareigos per tam tikrą laikotarpį, FTE ir užduotis                                                                          | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_ReportsToWorkerName    | Vardas, pavardė ir vardas bei pavardė                                                                       | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Skill                  | Įgūdis, įgūdžio tipas ir įvertinimas                                                                              | |
| Workforce\_TerminatedWorker       | Atleisti darbuotojai, atleidimo data, pareigos ir užduotis                                             | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position, Workforce\_WorkerBenefit |
| Workforce\_WorkerBenefit          | Galiojimo data, išmokos parinktis, išmokos planas ir išmokos tipas                                             | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_WorkerName             | Vardas, pavardė ir vardas bei pavardė                                                                       | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_WorkerTitle            | Pareigos ir paaukštinimo data                                                                                   | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_WorkerTrend            | Darbuotojai per tam tikrą laiką, darbuotojų skaičius, įmonė ir pareigos                                                        | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_WorkerBenefit |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
