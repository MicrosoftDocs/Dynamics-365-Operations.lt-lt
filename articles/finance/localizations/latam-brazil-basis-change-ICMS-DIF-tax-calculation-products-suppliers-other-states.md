---
title: Pagrindo keitimas ICMS-DIF mokesčių skaičiavimuose produktams iš tiekėjų kitose šalyse
description: Šioje temoje aprašoma ICMS-DIF mokesčių tipo skaičiavimų konfigūracija, kai finansinis dokumentas gaunamas Brazilijos būsenos Siera do Vista (RS) arba São Šiuo metu (SP).
author: Kai-Cloud
ms.date: 1/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 16f78b85567e6d08c588e621119513ff070bf618
ms.sourcegitcommit: 68655c5673aef9892063e5913ffee6bfc3817387
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/21/2022
ms.locfileid: "8016148"
---
# <a name="basis-change-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Pagrindo keitimas ICMS-DIF mokesčių skaičiavimuose produktams iš tiekėjų kitose šalyse

Šioje temoje aprašoma ICMS-DIF mokesčių tipo skaičiavimų konfigūracija, kai finansinis dokumentas gaunamas Brazilijos būsenos **Siera do Vista** (RS) arba São Šiuo metu (SP).

Pagal valstybės įstatymų apibrėžimą, surenkama Imposto sobreCulação de Mercculaias e Bajaços (ICMS) turi būti tokia taisyklė:

*ICMS, kurią reikia surinkti = ([( Operacijos suma* *– ICMS iš* *šaltinio*) ÷ *(1 – ICMS % vidinis*)] × *ICMS %* vidinė) – *ICMS suma iš šaltinio*

## <a name="example"></a>Pavyzdys

Brazilijos įmonė RS valstėje gauna fiskalinį dokumentą pirkimui iš tiekėjo, kuris yra SP būsenos. Įmonė turi surinkti ICMS procentinį skirtumą tarp RS būsenos (18 procentų) ir SP būsenos (12 procentų). Tačiau pagrindas turi būti apskaičiuojamas pagal prieš tai buvusią taisyklę.

- **Operacijos suma:** 1000,00 Brazilijos realai (R$ 1000,00)
- **ICMS tarpusavio priklausomybė:** R$ 120,00
- **ICMS procentas RS būsenoje:** 18 procentų
- **ICMS, kuri bus surenkama RS būsenos:**\[ ( (1000 – 120) ÷ (1 – 0,18) \] × 0,18) – 120 = R$ 73,17 

## <a name="resolution"></a>Paaiškinimas

Norėdami apskaičiuoti diferencinę ICMS (ICMS-DIF) pagal RS būsenos taisykles, turite nustatyti PVM kodus ir PVM grupę tokiu būdu:

1. Norėdami gauti 12 procentų ICMS (kitai būsenai), sukurkite PVM kodą. Šis kodas naudojamas tiekėjo gautinų mokesčių sumai registruoti.
2. Norėdami surinkti ICMS-DIF, sukurkite PVM kodą. Šio PVM kodo 18 procentų (jūsų valstijai) procentinė suma turi būti apibrėžta tarp 18 procentų ir 12 procentų. Nustatykite mokesčio tipą **ICMS-DIF.** Šis PVM kodas turi būti nurodytas skaičiavimo parametruose tokiu būdu:

    - Lauke **Šaltinis** pasirinkite Bendros sumos **procentas**.
    - Lauke **Bazinės** bazinės ribos pasirinkite **Grynoji suma pagal** eilutę arba **Grynoji SF balanso** suma.
    - Nustatykite apmokestinimo kodą, kad jo ataskaitinė vertė būtų **3**. Tokiu būdu, įgalinus finansinių knygų modulį, automatiškai **bus sukurta koregavimo** operacija.
    - Konfigūracijoje PVM grupės pasirinkite parinktį **Naudoti** mokestį **ICMS-DIF** PVM kodui.