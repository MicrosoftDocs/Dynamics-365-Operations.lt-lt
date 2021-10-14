---
title: Neatitikimų diagnostikos problemos
description: Šioje temoje aprašoma, kaip sukurti ir naudoti problemos tipo neatitiktims.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26705dd12f478f4ca6046c7265d4ae3cb1d08c69
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568812"
---
# <a name="problem-types-for-nonconformances"></a>Neatitikimų diagnostikos problemos

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip sukurti ir naudoti problemos tipo neatitiktims.

Naudodami puslapį **Problemų tipai** apibrėžkite kokybės problemų, su kuriomis galima susidurti įvairiuose neatitikimo tipuose, klasifikaciją. Turite nurodyti kiekvieno sukurto problemos tipo neatitiktys, su kuria gali būti naudojamas problemos tipas, tipus. Galite nustatyti šiuos neatitikimo tipus:

- **Vidinis – šio tipo neatitiktis yra susijusios su turimomis** atsargomis (pvz., kokybės užsakymais arba sulaikymo užsakymais).
- **Klientas** – šio tipo neatitiktis susijusios su pardavimo užsakymais.
- **Tiekėjas** – šio tipo neatitiktis susijusios su pirkimo užsakymais.
- **Paslaugos užklausa** – šio tipo neatitiktis susijusios su paslaugų užsakymais.
- **Gamyba** – Šio tipo neatitiktys yra susijusios su paketo užsakymais ar gamybos užsakymais.
- **Bendro produkto gamyba** – Šio tipo neatitiktys yra susijusios su paketo užsakymais ar bendro produkto užsakymais.

Kai sukuriate naują problemos tipą, veiksmų srityje pasirinkite Neatitikties tipai, kad sukurtumėte vieno ar daugiau neatitikties tipų, kurie leidžiami problemos **tipui**, sąrašą. Pvz., problemos tipas, susijęs su defekto kodu, gali būti pritaikytas visiems neatitikties tipams. Tačiau problemos tipas, susijęs su kliento nusiskundimais, gali būti taikomas tik **kliento** ir **aptarnavimo** užklausos neatitikties tipams.

## <a name="examples-of-problem-types"></a>Problemų tipų pavyzdžiai

Toliau pateikiami keletas scenarijų problemų tipams, kurie gali būti naudojami su skirtingais neatitikties tipais:

- **Klientas:** klientas užpildė pakeitimus, klientas pateikė grąžinimą arba kokybės specifikacijų nebuvo.
- **Tiekėjas: produktas buvo sugadintas, kokybės specifikacijos įvykdytos** arba gautas netinkamas produktas.
- **Aptarnavimo** užklausa: nebuvo įvykdytos kokybės specifikacijos, klientas užpildė priežiūrą arba reikalinga įrenginio priežiūra.
- **Gamyba:** neatitinka kokybės specifikacijų, reikalinga įrenginio priežiūra arba produktas buvo sugadintas.
- **Bendro produkto gamyba:** neatitinka kokybės specifikacijų, reikalinga įrenginio priežiūra arba produktas buvo sugadintas.

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a>Kurti problemos tipą ir priskirti jį neatitikties tipams

1. Pasirinkite **Atsargų valdymas \> Nustatymas \> Kokybės valdymas \> Problemų tipai**.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį. Tada nustatykite šiuos laukus naujai eilutei:

    - **Problemos tipas** – Įveskite unikalų ID ar problemos tipo pavadinimą.
    - **Aprašas** – įveskite išsamų problemos tipo aprašą.

1. Kol nauja eilutė vis dar pasirinkta, **veiksmų srityje pasirinkite** Neatitikties tipai.
1. Veiksmų srityje pasirinkite **Nauja**, kad pridėtumėte eilutę į tinklelį. Tada naujoje eilutėje nustatykite neatitikties tipo lauką kaip neatitikties tipą, **kurį norite leisti naudoti problemos** tipui.
1. Pakartokite ankstesnį veiksmą su kiekvienu papildomu neatitikties tipu, kurį norite autorizuoti problemos tipui.
1. Uždarykite puslapius.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Kokybės valdymo apžvalga](quality-management-processes.md)
- [Įjungti kiekio ir neatitikties valdymą](enable-quality-management.md)
- [Darbuotojai, atsakingi už neatitikties tvirtinimą](quality-responsible-workers.md)
- [Neatitikimų sulaikymo zonos](quality-quarantine-zones.md)
- [Neatitikimų diagnostikos tipai](quality-diagnostic-types.md)
- [Neatitikimų kokybės mokesčiai](quality-charges.md)
- [Neatitikties operacijos](quality-operations.md)
- [Sandėlio procesų kokybės valdymas](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
