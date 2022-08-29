---
title: Pagrindo keitimas ICMS-DIF mokesčių skaičiavimuose produktams iš tiekėjų kitose šalyse
description: Šiame straipsnyje aprašoma ICMS-DIF mokesčių tipo skaičiavimų konfigūracija, kai finansinis dokumentas gaunamas Brazilijos valskaitėjeVza do Vista (RS) arba São Šiuo metu (SP).
author: Kai-Cloud
ms.date: 06/21/2022
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
ms.openlocfilehash: 1bd9982a3804778a27203b4311682ee8bc3c4841
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218657"
---
# <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>Pagrindo keitimas (dvigubas pagrindas) ICMS-DIF mokesčių skaičiavimuose produktams iš tiekėjų kitose valstijose

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
    - Lauke Bazinės **bazinės** ribos pasirinkite **Grynoji suma pagal eilutę**.
    - Nustatykite apmokestinimo kodą, kad jo finansinis dydis būtų **3**. Tokiu būdu, įgalinus finansinių knygų modulį, automatiškai **bus sukurta koregavimo** operacija.
    - Konfigūracijoje PVM grupės pasirinkite parinktį **Naudoti mokestį** **ICMS-DIF PVM** kodui.

### <a name="use-the-delta-tax-rate-in-the-configuration-of-dual-base-icms-dif-sales-tax-codes"></a>Naudoti pokyčių mokesčio tarifą konfigūracijoje dvigubos bazės ICMS-DIF PVM kodų

Kai naudojami anksčiau aprašyti parametrai, **ICMS-DIF** PVM kodas bus skaičiuojamas dviguboje bazinėje taisyklėje. Tačiau nominalusis mokesčio tarifas tampa 18 procentų, o tai skiriasi nuo 6 procentų tarifo paprastoje bazinėje taisyklėje. Dėl šio skirtumo finansinio dokumento ir mokesčių ataskaitose kyla nenuoseklumo problemų. Microsoft Dynamics Nuo 365 finansų versijos 10.0.29 galite įgalinti (Brazilija) Konfigūruokite pokyčių mokesčio tarifą ICMS-DIF **mokesčio** **kode, kuris taikomas dvigubo pagrindinio atvejo funkcijai funkcijų valdymo srityje,** kad būtų pašalinti nenuoseklumas.

- Be ankstesnio skyriaus veiksmų užbaigimo, **lauke PVM taikomas PVM pasirinkite ICMS 12** **PVM** kodą.
- **ICMS-DIF PVM kodo mokesčio tarifą** nustatykite kaip 18 procentų. Nominalaus **mokesčio tarifo** vertė bus 6 procentai.

> [!NOTE]
> **ICMS-DIF** ir **ICMS 12** PVM kodai turi būti priskirti tai pačiai PVM grupei.

## <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-to-non-taxpayer-consumers-difal-in-other-states"></a>Pagrindo keitimas (dvigubas pagrindas) ICMS-DIF mokesčių skaičiavimuose produktams ne mokesčių mokėtojams (DIFAL) kitose šalyse

**Įgalinti (Brazilija) Dvigubo bazės skaičiavimo ICMS-DIFAL** **pardavimo** operacijų funkcijai funkcijų valdymas, kad būtų galima pakeisti pagrindą prekybos ICMS-DIF į mokesčių mokėtojais ne mokesčių mokėtojų vartotojus iš kitos šalies. ICMS-DIF PVM kodo pavyzdys įsigalioja pardavimo užsakymo ir laisvos formos SF operacijose.

**Įgalinti (Brazilija) IpI** **atvejų** funkcijų ICMS-DIFAL dvigubo pagrindo skaičiavimą, kad būtų palaikomi scenarijai, kai prekyba ne mokesčių mokėtojams iš kitos šalies taip pat apmokestinama už Imposto sobre Produtos Industrializados (IPI). IPI PVM kodo mokesčių suma bus atpažinta ir taikoma ICMS-DIFAL mokesčių bazėje.

- Pardavimo užsakymo arba laisvos formos SF antraštėje, **skirtuke** Fiskalinė informacija "FastTab", galutinio **vartotojo** parinktis turi būti nustatyta kaip **Taip**.
- Pirkimo užsakymo arba tiekėjo SF antraštėje, **skirtuke Fiskalinė informacija "FastTab", parinktis** **Naudojimas ir suvartojimas turi būti nustatyta kaip** Taip **.**
