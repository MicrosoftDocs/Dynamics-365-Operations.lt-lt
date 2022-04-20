---
title: Nustatyti PVM kodus
description: Šioje temoje paaiškinama, kaip nustatyti PVM kodus "Dynamics 365 Finance".
author: twheeloc
ms.date: 09/27/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69e2cf9a16fe0e694154cccf9b49944b49c79b90
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2022
ms.locfileid: "8565859"
---
# <a name="set-up-sales-tax-codes"></a>Nustatyti PVM kodus

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

    Jei „FastTab“ skirtuke **Skaičiavimas** lauke **Kilmė** pasirinkta, **Suma pagal vienetą** kad būtų apskaičiuota PVM suma, reikšmė bus padauginta iš operacijos kiekio.  Jei mokesčio kodas yra ne vienetinis mokestis, reikšmė yra procentinė dalis, taikoma šio mokesčio kodo kilmei, kad būtų apskaičiuota PVM suma.     

11. Pasirinkite **Įrašyti**.
12. Uždarykite puslapį.
13. Pasirinkite **Įrašyti**.

Microsoft Dynamics Nuo 365 finansų versijos 10.0.22, [jei](../../localizations/global-tax-calcuation-service-overview.md) naudojate mokesčių tarnybą, [**·**](../../localizations/emea-multiple-vat-registration-numbers.md)**o** funkcijų valdymo darbo srityje įjungta kelių PVM registracijos numerių palaikymo funkcija, **galite** naudoti mokesčio lauko tipą mokesčio tipui nurodyti. Galimos šios vertės:

- Standartinis PVM
- Sumažintas PVM
- 0% PVM
- Akcizas
- Kita

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
