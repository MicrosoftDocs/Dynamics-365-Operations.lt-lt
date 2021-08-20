---
title: Vartotojų importavimas iš „Azure Active Directory“
description: Šią procedūrą gali naudoti sistemos administratoriai, norėdami neautomatiškai importuoti pasirinktus vartotojus arba importuoti didelį skaičių vartotojų iš „Azure Active Directory“.
author: peakerbl
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce8c98add0c6d5fb07b3ba5338037d9a12b1d8e50a2d2039b0231d3d305c9ebe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748293"
---
# <a name="import-users-from-azure-active-directory"></a>Vartotojų importavimas iš „Azure Active Directory“

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a>Pasirinktų vartotojų importavimas

Šią procedūrą gali naudoti sistemos administratoriai, norėdami importuoti pasirinktus vartotojus iš „Azure Active Directory“ („Azure AD“).

1. Vartotojas bus importuotas su dabartine seanso įmone kaip numatytoji įmonė. Jei reikia, prieš importuodami vartotojus, keiskite šią įmonę.
2. Pasirinkite **Sistemos administravimas > Vartotojai > Vartotojai**.
3. Spustelėkite **Importuoti vartotojus**.
4. Pasirinkite vartotojus, kuriuos reikia importuoti ir pasirinkite **Importuoti vartotojus**.

Baigus importavimą bus reikalaujama, kad vartotojai priskirtų vaidmenis.

## <a name="import-users-in-bulk"></a>Masinis vartotojų importavimas

Šią procedūrą gali naudoti sistemos administratoriai, norėdami importuoti didelį skaičių vartotojų iš „Azure Active Directory“.
Atkreipkite dėmesį, kad naudojant paketinio importavimo pasirinktį vartotojo pasirinkti negalima.

## <a name="run-the-import-as-a-batch-job"></a>Importavimo kaip paketinės užduoties vykdymas
1. Vartotojas bus importuotas su dabartine seanso įmone kaip numatytoji įmonė. Jei reikia, prieš importuodami vartotojus, keiskite šią įmonę.
2. Pasirinkite **Sistemos administravimas > Vartotojai > Vartotojai**.
3. Spustelėkite **Paketinis importavimas**.
4. Išplėskite skyrių **Vykdyti fone**.
4. Pasirinkite **Taip** lauke **Paketinis vykdymas**.
6. Lauke **Paketinė grupė** įveskite arba pasirinkite vertę. Tai pasirinktinis veiksmas.  
7. Lauke **Privatus** pasirinkite **Taip**. Tai pasirinktinis veiksmas.  
8. Lauke **Kritinė užduotis** pasirinkite **Taip**. Tai pasirinktinis veiksmas.  
9. Lauke **Stebėjimo kategorija** pasirinkite parinktį.
10. Spustelėkite **Gerai**.

Baigus importavimą bus reikalaujama, kad vartotojai priskirtų vaidmenis.

## <a name="run-in-a-sandbox-environment"></a>Paleiskite smėlio dėžės aplinkoje
1. Pasirinkite **Paketinis importavimas**.
2. Pasirinkite **Gerai**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]