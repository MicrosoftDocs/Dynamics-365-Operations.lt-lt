---
title: Kurti ir tvarkyti atsargų blokavimą
description: Šiame straipsnyje aprašoma, kaip naudoti atsargų blokavimą norint neleisti, kad faktinės turimos atsargos nebūtų rezervuojamos kituose siuntimo šaltinio dokumentuose.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba95b689bedfc76598dfa81548a074f4fb7c833a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859349"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Kurti ir tvarkyti atsargų blokavimą

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip naudoti atsargų blokavimą norint neleisti, kad faktinės turimos atsargos nebūtų rezervuojamos kituose siuntimo šaltinio dokumentuose. Prieš pradėdami šiame straipsnyje aprašomas procedūras, turite turėti prekę, kurios faktinės turimos atsargos yra.

## <a name="block-inventory"></a>Blokuoti atsargas

Norėdami sukurti atsargų blokavimo įrašą, kad atsargos būtų užblokuotos, atlikite šiuos veiksmus.

1. Pasirinkite **Atsargų valdymas \> Periodinės užduotys \> Atsargų blokavimas**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Naujo blokavimo įrašo antraštėje nustatykite prekės, kurią norite blokuoti, lauką Prekės numeris **įveskite** aprašymą.
1. **Bendra** „FastTab” skirtuke, **Kiekis** lauke, įveskite blokuojamų elementų skaičių.
1. Atsargų **dimensijų** „FastTab“ nurodykite vieta ir sandėlį, kuriame šiuo metu yra prekės, kurias norite užblokuoti.
1. Veiksmų srityje pasirinkite **Įrašyti**.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Atnaujinti atsargų blokavimo sąlygas

Norėdami atnaujinti atsargų blokavimo įrašą, atlikite šiuos veiksmus.

1. Pasirinkite **Atsargų valdymas \> Periodinės užduotys \> Atsargų blokavimas**.
1. Sąrašo srityje pažymėkite atitinkamą blokavimo įrašą.
1. Redaguokite įrašą pagal reikalą. Pavyzdžiui, galite keisti tikėtinos datos **Laukelio** vertę, tam, kad galėtumėte nurodyti, kada galima rezervuoti užblokuotas atsargas, priskirdami numatomą datą. Jei **pasirinkta pasirinktis** Numatomi gaviniai, data bus rodoma tikėtinoje operacijoje. (Toliau **Numatyta, kad** numatyta gavimo pasirinktis pasirenkama rankiniu būdu kuriant blokavimo įrašą.)
1. Veiksmų srityje pasirinkite **Įrašyti**.

## <a name="unblock-inventory"></a>Atsargų atblokavimas

Norėdami panaikinti atsargų blokavimo įrašą, kad atsargos būtų atblokuotos, atlikite šiuos veiksmus.

1. Pasirinkite **Atsargų valdymas \> Periodinės užduotys \> Atsargų blokavimas**.
1. Sąrašo srityje pažymėkite atitinkamą blokavimo įrašą.
1. Rinkitės **Naikinti** veiksmų juostoje.
1. Jus paragins patvirtinti operaciją. Pasirinkite **Taip** tam, kad tęstumėte.
1. Uždarykite puslapį.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
