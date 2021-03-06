---
title: PVM kodų nustatymas
description: Šioje temoje paaiškinama, kaip nustatyti užsakymų sulaikymo kodus Dynamics 365 Finance.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c7208fa65905fcc902d9c08b5b90178745e76d4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815049"
---
# <a name="set-up-sales-tax-codes"></a>PVM kodų nustatymas

[!include [banner](../../includes/banner.md)]

Šioje temoje paaiškinama, kaip nustatyti PVM kodus. PVM kodai sukurti kiekvienam netiesioginiam mokesčiui ar muitui, kuriuos juridinis subjektas yra įsipareigojęs skaičiuoti, rinkti ir mokėti PVM institucijoms.

Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Pasirinkite **Mokestis > Netiesioginiai mokesčiai > PVM > PVM kodai**.
2. Pasirinkite **Naujas**.
3. Lauke **PVM kodas** įveskite reikšmę.
4. Lauke **Pavadinimas** įveskite reikšmę.
5. Pasirinkite **Sudengimo laikotarpis**, kad nurodytumėte, kuriai PVM institucijai ir kuriais intervalais reikia pranešti apie šį PVM ir jį mokėti.
6. Pasirinkite **DK registravimo grupė**, kad nurodytumėte pagrindines sąskaitas, kuriose į DK registruoti PVM.
7. Išplėskite „FastTab“ skirtuką **Skaičiavimas**. Jis apima kelis laukus, kurie kontroliuoja, kaip bus apskaičiuojamos PVM sumos. Tinkamai užpildykite šiuos laukelius.  
8. Sąsajos viršutinėje dalyje **Veiksmų sritis** pasirinkite **PVM kodas**.
9. Pasirinkite **Reikšmės**.
10. Įveskite šio mokesčio kodo reikšmę stulpelyje **Reikšmė**.
    - Jei „FastTab“ skirtuke **Skaičiavimas** lauke Kilmė pasirinkta Suma pagal vienetą, kad būtų apskaičiuota PVM suma, reikšmė bus padauginta iš operacijos kiekio.  Jei mokesčio kodas yra ne vienetinis mokestis, reikšmė yra procentinė dalis, taikoma šio mokesčio kodo kilmei, kad būtų apskaičiuota PVM suma.     
11. Pasirinkite **Įrašyti**.
12. Uždarykite puslapį.
13. Pasirinkite **Įrašyti**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]