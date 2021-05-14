---
title: Darbuotojai, atsakingi už neatitikties tvirtinimą
description: Šioje temoje aprašoma, kaip konfigūruoti darbuotojus, atsakingus už neatitikimų tvirtinimą.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5979cb33146a00c3ea49ada9577140b24c07928f
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956762"
---
# <a name="workers-responsible-for-approving-nonconformances"></a>Darbuotojai, atsakingi už neatitikties tvirtinimą

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip konfigūruoti darbuotojus, atsakingus už neatitikimų tvirtinimą.

Neatitiktis turi būti patvirtintos prieš tai, kai vartotojai gali pradėti įvesti informaciją, pvz., taisymus ar operacijas. Kad vartotojai galėtų patvirtinti arba atmesti neatitiktis, jų vartotojo ID (vartotojo įrašas) turi būti susietas su darbuotojo įrašu. Galite pasirinktinai konfigūruoti už kokybę atsakingus darbuotojus ir leisti vienam darbuotojui patvirtinti darbą kito darbuotojo vardu.

## <a name="enable-a-user-for-nonconformance-processing"></a>Leidimas vartotojui apdoroti neatitiktis

Kad vartotojas galėtų patvirtinti arba atmesti neatitiktis, susiekite jų vartotojo ID (vartotojo įrašas) su darbuotojo įrašu. Tada patvirtinimo laukus galima nustatyti automatiškai, o dabartiniam vartotojui galima automatiškai įvesti tabelį. Prieš vartotojui naudojant dokumento įrašus, turite taip pat suaktyvinti dokumento tvarkymą jų vartotojų parinktyse.

1. Eikite į **Sistemos administravimas \> Vartotojai \> Vartotojai**.
1. Raskite ir atidarykite vartotoją, kuris turėtų patvirtinti arba atmesti neatitiktis.
1. Lauke **Asmuo** nustatykite darbuotojo, susijusio su dabartiniu vartotojo įrašu, vardą.
1. Veiksmų srityje pasirinkite **Vartotojo parinktys**.
1. Dabartinio **vartotojo** įrašo pasirinkčių puslapyje skirtuke **Nuostatos** nustatykite **pasirinktį Įgalinti dokumentų tvarkymą** kaip *Taip*.
1. Uždarykite puslapius.

## <a name="define-workers-that-are-responsible-for-quality"></a>Nustatyti už kokybę atsakingus darbuotojus

1. Eikite į **Atsargų valdymas \> Nustatymas \> Kokybės kontrolė \> Darbuotojo atsakomybė už kokybę**.
2. Veiksmų srityje pasirinkite **Naujas**.
3. Lauke **Darbuotojas** pasirinkite darbuotoją, kuris įveda kokybės duomenis.
4. Lauke **Atsakingas darbuotojas** pasirinkite darbuotoją, kurio vardu įveda darbą pasirinktas darbuotojas. Kai neatitiktis sukuriamos ir atnaujinamos, šis darbuotojas bus įvestas pagal numatytuosius parametrus **darbuotojo** laukuose.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Kokybės valdymo apžvalga](quality-management-processes.md)
- [Įjungti kiekio ir neatitikties valdymą](enable-quality-management.md)
- [Kokybės išlaidos](quality-charges.md)
- [Neatitikimų sulaikymo zonos](quality-quarantine-zones.md)
- [Neatitikimų diagnostikos tipai](quality-diagnostic-types.md)
- [Neatitikimų kokybės mokesčiai](quality-charges.md)
- [Neatitikties operacijos](quality-operations.md)
- [Sandėlio procesų kokybės valdymas](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
