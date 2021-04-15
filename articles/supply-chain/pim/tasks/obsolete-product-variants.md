---
title: Nebenaudojamų produktų variantų radimas
description: Šioje procedūroje parodoma, kaip rasti pasenusius išleistus produktus arba produkto variantus ir kaip susieti produkto ciklo būseną su pasenusiais produktais.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 807297a87a7f0e59023d80fbd371bffbf2b086bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807997"
---
# <a name="find-obsolete-product-variants"></a>Nebenaudojamų produktų variantų radimas 

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodoma, kaip rasti pasenusius išleistus produktus arba produkto variantus ir kaip susieti produkto ciklo būseną su pasenusiais produktais. Būtinoji sąlyga: prieš paleisdami šį užduočių vedlį turite nurodyti bent vieną produkto ciklo būseną, kuri yra neaktyvi planuojant.


## <a name="run-a-simulation"></a>Modeliavimo vykdymas
1. Eikite į Produkto informacijos valdymas > Periodinės užduotys > Keisti pasenusių produktų ciklo būseną.
2. Lauke Naujo produkto ciklo būsena įveskite arba pasirinkite reikšmę.
3. Lauke Vykdyti modeliavimą nenaujinant produktų duomenų pažymėkite Taip.
4. Lauke Neįtraukti produktų, sukurtų per ši dienų skaičių įveskite skaičių.
5. Lauke Neįtraukti produktų, naudojamų operacijose (tam tikrą dienų skaičių) įveskite skaičių.
6. Išplėskite dalį Įtrauktini įrašai.
7. Spustelėkite Filtras.
8. Sąraše pažymėkite pasirinktą eilutę.
9. Lauke Kriterijai surinkite reikšmę.
10. Spustelėkite GERAI.
11. Spustelėkite GERAI.

> [!NOTE]
> Jei ketinate ieškoti daug produktų, modeliavimą rekomenduojama atlikti pakete. Taip pat įsitikinkite, kad modeliavimas neatliekamas aktyviausiu įmonės darbo metu.  

## <a name="review-the-simulation-results"></a>Peržiūrėti modeliavimo rezultatus
1. Eikite į Produkto informacijos valdymas > Užklausos ir ataskaitos > Produkto ciklo būsenos priežiūros istorija.
   
> [!NOTE]
> Šia puslapyje galite peržiūrėti modeliavimo rezultatus ir įvertinti, kiek produktų ir produkto variantų bus susieti su nauja produkto ciklo būsena vykdant naujinimą be modeliavimo.  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a>Paleisti pasenusių produktų ciklo būsenos atnaujinimą
1. Uždarykite puslapį.
2. Eikite į Produkto informacijos valdymas > Periodinės užduotys > Keisti pasenusių produktų ciklo būseną.
3. Išplėskite dalį Įtrauktini įrašai.

> [!NOTE]
> Atkreipkite dėmesį į tai, kad paskutinis pasirinkimas išsaugomas.  

4. Lauke Vykdyti modeliavimą nenaujinant produktų duomenų pažymėkite Ne.
5. Išplėskite dalį Vykdyti fone.

> [!NOTE]
> Priklausomai nuo to, kiek esama paveiktų produktų ir produkto variantų, apsvarstykite galimybę paleisti šią užduotį pakete. Įsitikinkite, kad aktyviausiu įmonės darbo metu nevykdomos didelės apimties naujinimo užduotys.  

6. Spustelėkite GERAI.
7. Eikite į Produkto informacijos valdymas > Užklausos ir ataskaitos > Produkto ciklo būsenos priežiūros istorija.

> [!NOTE]
> Peržiūrėkite pakeistus ir išleistus produktus ir produkto variantus.  

8. Sąraše raskite ir pasirinkite norimą įrašą.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]