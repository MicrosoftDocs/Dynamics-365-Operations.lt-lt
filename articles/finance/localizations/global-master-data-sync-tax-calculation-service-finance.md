---
title: Sinchronizuoti mokesčių nustatymą iš mokesčių skaičiavimo tarnybos į "Dynamics 365 Finance"
description: Šiame straipsnyje paaiškinama, kaip sinchronizuoti mokesčių skaičiavimo tarnybos ir Microsoft Dynamics 365 finansų mokesčių nustatymo pagrindinius duomenis.
author: EricWangChen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.custom: intro-internal
ms.search.form: TaxIntegration, TaxServiceParameters
ms.openlocfilehash: 315f2b27a64906ca0fc404d704d0b170dbfa48c5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283860"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>Sinchronizuoti mokesčių nustatymą iš mokesčių skaičiavimo tarnybos į "Dynamics 365 Finance"

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip sinchronizuoti mokesčių skaičiavimo tarnybos ir Microsoft Dynamics 365 finansų mokesčių nustatymo pagrindinius duomenis.

Atlikę reikiamus nustatymo veiksmus skyriuje [Pradėti nuo mokesčių skaičiavimo](global-get-started-with-tax-calculation-service.md), šie mokesčių nustatymo duomenys automatiškai sinchronizuojami iš mokesčių skaičiavimo tarnybos į finansus.

## <a name="sales-tax-code"></a>PVM kodas

| Mokesčių skaičiavimo paslauga           | „Finance“                             |
| --------------------------------- | ----------------------------------- |
| Mokesčio kodas                          | PVM kodas                      |
| Aprašymas                       | Vardas                                |
| Vartotojo įvestis                        | Sudengimo laikotarpis                   |
| Vartotojo įvestis                        | DK registravimo grupė                |
| Vartotojo įvestis                        | PVM valiuta                  |
| Sukonfigūruotas neigiamas mokesčio tarifas | Leisti neigiamą PVM procentą |

## <a name="tax-value"></a>Mokesčių vertė

| Mokesčių skaičiavimo paslauga | „Finance“                   |
| ----------------------- | ------------------------- |
| Nuo operacijos datos   | Nuo datos                 |
| Iki operacijos datos     | Iki datos                   |
| Minimali suma          | Minimali riba             |
| Didžiausia suma          | Aukščiausia riba             |
| Mokesčio tarifas                | Reikšmė                     |
| Neatskaitomas tarifas     | Neišskaičiuojamas procentas |

## <a name="tax-limits"></a>Mokesčių ribos

| Mokesčių skaičiavimo paslauga | „Finance“           |
| ----------------------- | ----------------- |
| Nuo operacijos datos   | Nuo datos         |
| Iki operacijos datos     | Iki datos           |
| Minimali mokesčio suma      | Min. PVM |
| Maksimali mokesčio suma      | Maks. PVM |

## <a name="sales-tax-group"></a>PVM grupė

| Mokesčių skaičiavimo paslauga                         | „Finance“                                    |
| ----------------------------------------------- | ------------------------------------------ |
| Mokesčių grupė                                       | PVM grupė                            |
| Šios mokesčių grupės mokesčių kodai                  | PVM kodai šioje PVM grupėje |
| Mokesčio kodas pažymėtas kaip **Neapmokestinamas**         | Neapmokestinama                                     |
| Mokesčio kodas pažymėtas kaip **Neapmokestinamas**         | Neapmokestinimo kodas                                |
| Mokesčio kodas pažymėtas kaip Atvirkštinis **mokestis** | Atvirkštinis apmokestinimas                             |
| Mokesčio kodas pažymėtas kaip **Naudojimo mokestis**        | Naudojimo mokestis                                    |

## <a name="item-sales-tax-group"></a>Prekės PVM grupė

| Mokesčių skaičiavimo paslauga             | „Finance“                                         |
| ----------------------------------- | ----------------------------------------------- |
| Prekės mokesčių grupė                      | Prekės PVM grupė                            |
| Mokesčių kodai šioje prekės mokesčių grupėje | PVM kodai šioje prekės PVM grupėje |

Baigę sinchronizuoti tęskite ir toliau prižiūrėkite likusius finansų parametrus, kad būtų galima registruoti ir skelbti.

> [!NOTE]
> Mokesčių nustatymo iš Finansų į mokesčių skaičiavimo tarnybą sinchronizavimas nepalaikomas. Pirmiausia esamoje finansų aplinkoje sukurkite mokesčių nustatymą Mokesčių skaičiavimo paslaugoje. Tada sinchronizuokite nustatymo duomenis atgal į finansų aplinką.
