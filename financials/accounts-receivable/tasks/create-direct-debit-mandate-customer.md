--- 
title: "Kurti kliento tiesioginio debeto įgaliojimą"
description: "Šis užduočių vadovas parodo, kaip sukurti tiesioginio debeto įgaliojimą ir jį naudoti SF."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e1ac289c261922f013b679eecfb054390b8aef73
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a>Kurti kliento tiesioginio debeto įgaliojimą

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šis užduočių vadovas parodo, kaip sukurti tiesioginio debeto įgaliojimą ir jį naudoti SF.


## <a name="create-a-bank-account"></a>Kurti banko sąskaitą
1. Pasirinkite Gautinos sumos > Klientai > Visi klientai.
2. Pavyzdžiui, pasirinkite US-001
3. Veiksmų srityje spustelėkite Klientas.
4. Spustelėkite Banko sąskaitos.
5. Spustelėkite Naujas.
6. Lauke Banko sąskaita surinkite reikšmę.
7. Lauke Pavadinimas surinkite reikšmę.
8. Lauke IBAN surinkite reikšmę.
9. Lauke Valiuta surinkite reikšmę.
10. Spustelėkite Įrašyti.
11. Uždarykite puslapį.
12. Pasirinkite Grynųjų pinigų ir banko valdymas > Banko kodai > Banko kodai.
13. Sąraše raskite ir pasirinkite norimą įrašą.
14. Sąraše spustelėkite saitą pasirinktoje eilutėje.
15. Spustelėkite Redaguoti.
16. Išplėskite skyrių Papildoma identifikacija.
17. Lauke Tiesioginio debeto ID įveskite reikšmę.
18. Lauke IBAN surinkite reikšmę.
19. Uždarykite puslapį.
20. Uždarykite puslapį.

## <a name="define-the-electronic-payment-method"></a>Apibrėžti elektroninio mokėjimo būdą
1. Pasirinkite Gautinos sumos > Mokėjimų sąranka > Mokėjimo būdai.
2. Spustelėkite Naujas.
3. Lauke Mokėjimo būdas surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Tiesioginio debeto įgaliojimo mokėjimo tipas turi būti Elektroninis mokėjimas.
6. Lauke Reikalauti įgaliojimo pasirinkite Taip.
7. Uždarykite puslapį.

## <a name="add-a-direct-debit-mandate-to-a-customer"></a>Prie kliento pridėkite tiesioginio debeto įgaliojimą.
1. Pasirinkite Gautinos sumos > Klientai > Visi klientai.
2. Pavyzdžiui, pasirinkite US-001
3. Spustelėkite Redaguoti.
4. Išplėskite dalį Numatytosios mokėjimo nuostatos.
5. Lauke Mokėjimo metodas įveskite arba pasirinkite vertę.
6. Išplėskite dalį Numatytosios mokėjimo nuostatos.
7. Išplėskite dalį Tiesioginio debeto įgaliojimai.
8. Spustelėkite Pridėti.
9. Lauke Banko sąskaita įveskite arba pasirinkite reikšmę.
10. Lauke Kreditoriaus banko sąskaita įveskite arba pasirinkite reikšmę.
11. Įveskite šio įgaliojimo mokėjimų, kuriuos numatote apdoroti, skaičių.
12. Spustelėkite GERAI.
13. Spustelėkite Spausdinti.
14. Spustelėkite Įgaliojimo ataskaita.
15. Uždarykite puslapį.
16. Spustelėkite Redaguoti.
17. Lauke Pasirašymo data įveskite datą.
18. Spustelėkite Taip.
19. Įveskite vietą, kurioje buvo pasirašytas įgaliojimas.
20. Spustelėkite GERAI.
21. Uždarykite puslapį.

## <a name="create-a-free-text-invoice-with-mandate"></a>Kurti laisvos formos SF su įgaliojimu
1. Pasirinkite Gautinos sumos > Sąskaitos faktūros > Visos laisvos formos SF.
2. Spustelėkite Naujas.
3. Pasirinkite klientą, prie kurio pridėjote įgaliojimą.
4. Lauke Tiesioginio debeto įgaliojimo ID įveskite arba pasirinkite vertę.


