---
title: Pagrindo keitimas ICMS-DIF mokesčių skaičiavimuose produktams iš tiekėjų kitose šalyse
description: Šiame straipsnyje aprašoma ICMS-DIF mokesčių tipo skaičiavimų konfigūracija, kai finansinis dokumentas gaunamas Brazilijos valskaitėjeVza do Vista (RS) arba São Šiuo metu (SP).
author: Kai-Cloud
ms.date: 1/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 1fde18c79f375db4db6bc52cdb5c40a61625ae63
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868268"
---
# <a name="basis-change-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Pagrindo keitimas ICMS-DIF mokesčių skaičiavimuose produktams iš tiekėjų kitose šalyse

Šiame straipsnyje aprašoma ICMS-DIF **mokesčių tipo skaičiavimų konfigūracija, kai finansinis dokumentas gaunamas Brazilijos valskaitėjeVza** do Vista (RS) arba São Šiuo metu (SP).

Pagal valstybės įstatymų apibrėžimą, surenkama Imposto sobreCulação de Mercculaias e Bajaços (ICMS) turi būti tokia taisyklė:

*ICMS,* kurią reikia surinkti = ([(*Operacijos* suma – *ICMS* iš šaltinio) ÷ (1 – *ICMS %* vidinis)] × *ICMS %* vidinės) – *ICMS suma iš šaltinio*

## <a name="example"></a>Pavyzdys

Brazilijos įmonė RS valstėje gauna fiskalinį dokumentą pirkimui iš tiekėjo, kuris yra SP būsenos. Įmonė turi surinkti ICMS procentinį skirtumą tarp RS būsenos (18 procentų) ir SP būsenos (12 procentų). Tačiau pagrindas turi būti apskaičiuojamas pagal prieš tai buvusią taisyklę.

- **Operacijos suma:** 1000,00 Brazilijos realai (R$ 1000,00)
- **ICMS tarpusavio priklausomybė:** R$ 120,00
- **ICMS procentas RS būsenoje:** 18 procentų
- **ICMS, kuri bus surenkama RS būsenos:** (\[(1000 – 120) ÷ (1 – 0,18)\] × 0,18) – 120 = R$ 73,17 

## <a name="resolution"></a>Paaiškinimas

Norėdami apskaičiuoti diferencinę ICMS (ICMS-DIF) pagal RS būsenos taisykles, turite nustatyti PVM kodus ir PVM grupę tokiu būdu:

1. Norėdami gauti 12 procentų ICMS (kitai būsenai), sukurkite PVM kodą. Šis kodas naudojamas tiekėjo gautinų mokesčių sumai registruoti.
2. Norėdami surinkti ICMS-DIF, sukurkite PVM kodą. Šio PVM kodo 18 procentų (jūsų valstijai) procentinė suma turi būti apibrėžta tarp 18 procentų ir 12 procentų. Nustatykite mokesčio tipą **ICMS-DIF**. Šis PVM kodas turi būti nurodytas skaičiavimo parametruose tokiu būdu:

    - Lauke Šaltinis **pasirinkite** Bendros **sumos procentas**.
    - Lauke Bazinės **bazinės** ribos pasirinkite **Grynoji suma pagal eilutę** arba **Grynoji SF balanso suma**.
    - Nustatykite apmokestinimo kodą, kad jo finansinis dydis būtų **3**. Tokiu būdu, įgalinus finansinių knygų modulį, automatiškai **bus sukurta koregavimo** operacija.
    - Konfigūracijoje PVM grupės pasirinkite parinktį **Naudoti mokestį** **ICMS-DIF PVM** kodui.
