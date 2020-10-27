---
title: Eksperimentavimas „Dynamics 365 Commerce”
description: Eksperimentavimas leidžia kurti, redaguoti ir valdyti puslapio maketų bei turinio apdorojimo būdus svetainių daryklėje. Palaikomas visapusis eksperimentavimas el. prekybos puslapiuose ir puslapyje esančiuose objektuose.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 8b2e97167d12b8ceecf72af075ee0362101c4fa0
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930255"
---
# <a name="experimentation-in-dynamics-365-commerce"></a>Eksperimentavimas „Dynamics 365 Commerce”
Naudokite „Dynamics 365 Commerce” eksperimentavimą, norėdami patvirtinti jūsų „e-Commerce” puslapių efektyvumo hipotezes ir priimti patikimus, duomenimis pagrįstus sprendimus. „Commerce” palaiko A / B tikrinimą puslapiuose, moduliuose ir fragmentuose bei leidžia įvertinti siūlomų svetainės pakeitimų poveikį.

Svetainių daryklėje galite kurti, redaguoti ir valdyti puslapių bei turinio apdorojimo būdus, vadinamus **variacijomis**. „Commerce” integruojama su trečiųjų šalių paslaugomis, kurias galite naudoti eksperimentams ir apdorojimo užduotims kurti. „Commerce” užfiksuoti realiojo laiko įvykių srautai leidžia atlikti analizę, nurodančią eksperimento rezultatus trečiosios šalies paslaugoje. Tada galite panaudoti šią analizę, norėdami patvirtinti arba paneigti jūsų hipotezę.

## <a name="set-up-prerequisites"></a>Būtinųjų sąlygų nustatymas
1. **Gaukite tinkamą „Commerce” versiją** – atnaujinkite jūsų modulių biblioteką, interneto kanalo SDK išplečiamumą ir „Commerce Scale Unit” į „Commerce” 10.0.13 arba naujesnę versiją.
1. **Nustatykite eksperimento jungtį** – eksperimento jungtis leidžia „Commerce” prisijungti prie trečiųjų šalių paslaugų ir gauti eksperimentų sąrašą siekiant nustatyti, kada vartotojui parodyti eksperimentą. Galite įsigyti trečiosios šalies jungtį iš [„AppSource”](https://appsource.microsoft.com). Sekite leidėjo pateiktas nustatymo instrukcijas. Taip pat galite naudoti „Commerce” bandymo jungtį, norėdami patikrinti eksperimento darbo eigą, nekonfigūruodami išorinės paslaugos. Daugiau informacijos žr. [Jungčių konfigūravimas ir įjungimas](e-commerce-extensibility/connectors.md). 
1. **Įjunkite eksperimentavimo funkcijų vėliavėles „Commerce”** – galite įjungti eksperimentavimą nuomotojo lygiu, nuėję į **Nuomotojo parametrai > Funkcijos**, arba svetainės lygiu, nuėję į **Svetainės parametrai > Funkcijos**.
    - Įjunkite vėliavėlę **Eksperimentavimas**, norėdami sukurti puslapyje esančių modulių eksperimento variacijas, nepaveikdami ar nekopijuodami kito turinio, kuris nėra eksperimento dalis. Tai užtikrina, kad vykdomi turinio naujinimai ne eksperimente liks sinchronizuoti eksperimento ciklo metu. Išjungus šią vėliavėlę, sustabdomas visų eksperimentų rodymas vartotojams ir pašalinamos visos svetainių daryklės redagavimo funkcijos.
    - Įjunkite vėliavėlę **Puslapių ar fragmentų eksperimentų vykdymas**, norėdami vykdyti puslapio ar fragmento eksperimentus. Tai sukuria visą visų modulių, esančių puslapyje arba fragmente, puslapio arba fragmento egzemplioriaus kopiją. Naudokite šį režimą, kai norite tikrinti išsamius turinio keitimus arba kai vykdomų turinio pakeitimų sinchronizavimas egzemplioriuose nėra problema. Išjungus šią vėliavėlę, neleidžiama kurti ir redaguoti naujų puslapių ir fragmentų eksperimentų.
    > [!NOTE]
    > Vėliavėlė **Eksperimentavimas** turi būti įjungta, kad veiktų funkcija **Puslapių ar fragmentų eksperimentų vykdymas**.
    
## <a name="experimentation-lifecycle"></a>Eksperimento ciklas
Eksperimento nustatymas, variacijų kūrimas ir eksperimento vykdymas yra kartotinis procesas. Toliau pateiktoje diagramoje rodomas eksperimento ciklas „Commerce” ir trečiosios šalies paslaugoje. 

[ ![Eksperimento ciklas](./media/experimentation_lifecycle.svg) ](./media/experimentation_lifecycle.svg#lightbox)

Norėdami sužinoti daugiau apie kiekvieną eksperimentavimo proceso veiksmą, žr. toliau pateiktas temas.
- [Eksperimento hipotezės ir metrikos nustatymas](experimentation-identify.md)
- [Eksperimento nustatymas](experimentation-setup.md)
- [Eksperimento prijungimas ir redagavimas](experimentation-connect-edit.md)
- [Eksperimento peržiūra ir publikavimas](experimentation-preview-publish.md)
- [Eksperimento vykdymas ir stebėjimas](experimentation-run-monitor.md)
- [Variacijos skatinimas ir eksperimento užbaigimas](experimentation-review-complete.md)

> [!NOTE]
> Norėdami sužinoti, kurioje ciklo vietoje yra eksperimentas, eikite į skirtuką **Eksperimentai** svetainių daryklėje. Rodomas eksperimentų sąrašas su kiekvieno eksperimento būsena „Commerce” ir trečiosios šalies paslaugoje. Daugiau informacijos žr. [Eksperimento būsenos peržiūra](experimentation-status.md).

## <a name="next-step"></a>Kitas veiksmas
[Eksperimento hipotezės ir sėkmės metrikos nustatymas](experimentation-identify.md) 
