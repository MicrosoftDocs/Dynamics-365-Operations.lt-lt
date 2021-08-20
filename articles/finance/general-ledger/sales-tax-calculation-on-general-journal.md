---
title: Bendrojo žurnalo eilučių PVM apskaičiavimas
description: Šioje temoje paaiškinama, kaip bendrojo žurnalo eilutėse apskaičiuojami įvairių tipų sąskaitų (tiekėjo, kliento, DK ir projekto) PVM.
author: EricWang
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: EricWang
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 96a87e5de3fb247e4554a64ecff3a4c63477b6a70f7a969b80f538601cda08bb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746373"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a>Bendrojo žurnalo eilučių PVM apskaičiavimas
[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip bendrojo žurnalo eilutėse apskaičiuojami įvairių tipų sąskaitų (tiekėjo, kliento, DK ir projekto) PVM.

Procesą galima suskirstyti į tris etapus.

- PVM krypties nustatymas.

- PVM sumos, kuri bus fiksuojama laikinoje PVM lentelėje, nustatymas.

- PVM sumos ir kvito sąskaitos nustatymas.

## <a name="determine-the-sales-tax-direction"></a>PVM krypties nustatymas

PVM krypties nustatymo būdas priklauso nuo kvito sąskaitos tipo. PVM kryptis priklauso nuo sąskaitos tipo ir PVM kodo derinio. Toliau esančiuose skyriuose galimybės aprašomos išsamiau. 

### <a name="account-type-is-project"></a>Sąskaitos tipas yra Projektas

Jei kvite yra žurnalo eilutė, kurios sąskaitos tipas yra **Projektas**, visoms kvito žurnalo eilutėms taikoma ta pati mokesčių kryptis. Toliau esančiame paveikslėlyje parodyta taisyklė. Toliau pateikiamuose punktuose rodomos galimos projekto sąskaitų mokesčių kryptys.

• Jei PVM kodas yra naudojimo mokestis, PVM kryptis yra Naudojimo mokestis.

• Jei PVM kodas yra neapmokestinamas, PVM kryptis yra Neapmokestinamas pirkimas.

• Jei PVM kodas yra intracom PVM, PVM kryptis yra Mokėtinas PVM.

• Jei PVM kodas yra atvirkštinis mokestis, PVM kryptis yra Mokėtinas PVM.

Kitu atveju PVM kryptis yra Gautinas PVM.

Toliau pateikiamoje diagramoje taisyklė pavaizduota grafiškai.

![Projekto sąskaitų mokesčių krypties galimybės.](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a>Sąskaitos tipas yra Tiekėjas

Jei kvite yra žurnalo eilutė, kurios sąskaitos tipas yra **Tiekėjas**, visoms kvito žurnalo eilutėms taikoma ta pati mokesčių kryptis. Toliau pateikiamuose punktuose rodomos galimos tiekėjų sąskaitų mokesčių kryptys. 

• Jei PVM kodas yra naudojimo mokestis, PVM kryptis yra Naudojimo mokestis.

• Jei PVM kodas yra neapmokestinamas, PVM kryptis yra Neapmokestinamas pirkimas.

• Jei PVM kodas yra intracom PVM, PVM kryptis yra Mokėtinas PVM.

• Jei PVM kodas yra atvirkštinis mokestis, PVM kryptis yra Mokėtinas PVM.

Kitu atveju PVM kryptis yra Gautinas PVM.

Toliau pateikiamoje diagramoje taisyklė pavaizduota grafiškai.

![Tiekėjų sąskaitų mokesčių krypties galimybės.](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a>Sąskaitos tipas yra Klientas

Jei kvite yra žurnalo eilutė, kurios sąskaitos tipas yra **Klientas**, visoms kvito žurnalo eilutėms taikoma ta pati mokesčių kryptis. Toliau pateikiamuose punktuose rodomos galimos klientų sąskaitų mokesčių kryptys.

• Jei PVM kodas yra neapmokestinamas, PVM kryptis yra Neapmokestinamas pirkimas.

• Jei PVM kodas yra intracom PVM, PVM kryptis yra Gautinas PVM.

• Jei PVM kodas yra atvirkštinis mokestis, PVM kryptis yra Gautinas PVM.

Kitu atveju PVM kryptis yra Mokėtinas PVM.

Toliau pateikiamoje diagramoje taisyklė pavaizduota grafiškai.

![Klientų sąskaitų mokesčių krypties galimybės.](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a>Sąskaitos tipas yra DK

Toliau pateikiamame paveikslėlyje pavaizduota taisyklė, galiojanti, jei kvite yra tik žurnalo eilutės, kurių sąskaitos tipas yra **DK**. Toliau pateikiamuose punktuose rodomos galimos DK sąskaitų mokesčių kryptys.

• Jei PVM kodas yra naudojimo mokestis, PVM kryptis yra Naudojimo mokestis.

• Jei PVM kodas yra neapmokestinamas, PVM kryptis yra Neapmokestinamas pirkimas.

Kitu atveju, jei žurnalo suma yra debetas (teigiama), PVM kryptis yra Gautinas PVM; jei žurnalo suma yra kreditas (neigiama), PVM kryptis yra Mokėtinas PVM.

Toliau pateikiamoje diagramoje taisyklė pavaizduota grafiškai.

![DK sąskaitų mokesčių krypties galimybės.](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a>PVM krypties keitimas

Galite pakeisti PVM kryptį, kai kvite yra tik eilutės, kurių sąskaitų tipas yra **DK**.

Eikite į **DK \> Sąskaitų planas \> Sąskaitos \> Pagrindinės sąskaitos** ir pasirinkite FastTab **Juridinio subjekto nepaisymai**.

## <a name="determine-the-sales-tax-amount"></a>PVM sumos nustatymas

Šiame skyriuje aprašoma, kaip apskaičiuojamas PVM sumos ženklas.

![PVM operacijų puslapis.](media/sales-tax-amount-sign.jpg)

Šioje lentelėje pateikiama bendroji taisyklė, taikoma nustatant mokesčių valdybą ir sumų ženklą laikinoje PVM lentelėje.

| Žurnalo eilutės suma | PVM kryptis  | PVM sumos ženklas |
|---------------------|----------------------|-----------------------|
| Teigiama            | Gautinas PVM | Teigiama              |
| Teigiama            | Mokėtinas PVM    | Neigiamas              |
| Neigiamas            | Gautinas PVM | Neigiamas              |
| Neigiamas            | Mokėtinas PVM    | Teigiama              |

Yra speciali taisyklė, taikoma kvitams, kuriuose yra tik **Projekto** arba **DK** eilučių, kai PVM grupė arba prekės PVM grupė pasirenkama **DK** eilutėje. Šią taisyklę valdo funkcija Įgalinti **nepriklausomą pardavimų mokesčio skaičiavimo funkciją bendriesiems žurnalams**. Kai ši funkcija išjungta, **DK** eilutės mokesčio sumai apskaičiuoti naudojama **Projekto** eilutės debeto / kredito kryptis. Kai ši funkcija įjungta, **DK** eilutės mokesčio sumai apskaičiuoti naudojama jos pačios debeto / kredito kryptis. Toliau esančiose lentelėse pateikiama kiekvieno scenarijaus taisyklė. 

**Taisyklė, kai funkcija įjungta**

| Projekto žurnalo eilutės suma | PVM kryptis  | PVM sumos ženklas |
|--------------------------------|----------------------|-----------------------|
| Teigiama                       | Gautinas PVM | Teigiama              |
| Neigiamas                       | Gautinas PVM | Neigiamas              |

**Taisyklė, kai funkcija išjungta**

| DK žurnalo eilutės suma  | PVM kryptis  | PVM sumos ženklas |
|--------------------------------|----------------------|-----------------------|
| Teigiama                       | Gautinas PVM | Teigiama              |
| Neigiamas                       | Gautinas PVM | Neigiamas              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a>PVM sumos ir kvito sąskaitos nustatymas

Kai registruojate PVM, pagrindinė sąskaita gaunama iš DK registravimo grupės profilio. Kai PVM yra gautinas, sistema naudoja sąskaitą Gautinas PVM, kuris nurodytas profilyje. Kai PVM yra mokėtinas, sistema naudoja sąskaitą Mokėtinas PVM, kuris nurodytas profilyje.

Šioje lentelėje pateikiama bendroji taisyklė.

| PVM kryptis  | PVM sumos ženklas | PVM sąskaita      | Kvito suma |
|----------------------|-----------------------|------------------------|-------------------|
| Gautinas PVM | Teigiama              | Gautino mokesčio sąskaita | Teigiama (debetas)  |
| Gautinas PVM | Neigiamas              | Gautino mokesčio sąskaita | Neigiamas (kreditas)  |
| Mokėtinas PVM    | Teigiama              | Mokėtino mokesčio sąskaita    | Neigiamas (kreditas)  |
| Mokėtinas PVM    | Neigiamas              | Mokėtino mokesčio sąskaita    | Teigiama (debetas)  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
