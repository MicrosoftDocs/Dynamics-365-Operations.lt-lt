---
title: PVM mokėjimo ir apvalinimo taisyklės
description: Šiame straipsnyje paaiškinama, kaip srityje PVM rinkėjai veikia apvalinimo taisyklės nustatymas ir paaiškinamas PVM balansas vykdant užduotį Sudengti ir užregistruoti PVM.
author: kailiang
ms.date: 10/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: kfend
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ff69afae675b9f8824ac0b29b5611420136b6a57
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726556"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>PVM mokėjimo ir apvalinimo taisyklės

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip srityje PVM rinkėjai veikia apvalinimo taisyklės nustatymas ir paaiškinamas PVM balansas vykdant užduotį Sudengti ir užregistruoti PVM.

Periodiškai reikia pranešti apie PVM ir sumokėti jį mokesčių institucijoms. Šis veiksmas gali būti užbaigtas atliekant Sudengimą ir registruoj pardavimų mokesčio procesą **Pardavimų mokesčių** puslapyje. Laikotarpio PVM bus sudengtas pagal PVM sąskaitas, ir PVM balansas bus registruojamas PVM sudengimo sąskaitoje. PVM balansą, registruojamą PVM sudengimo sąskaitoje, galima apvalinti pagal mokesčių institucijos reikalavimus, nustačius apvalinimo taisyklę **PVM** puslapyje. 

Apvalinimo skirtumas užregistruojamas PVM apvalinimo sąskaitoje, pasirinktoje dalies Didžioji knyga lauke Automatinių operacijų sąskaitos.

Tolesniame pavyzdyje pavaizduota, kaip veikia apvalinimo taisyklė PVM institucijai.

## <a name="examples"></a>Pavyzdžiai

Rodoma, kad bendrojo laikotarpio PVM kredito balansas yra –98 765,43. Juridinis subjektas surinko daugiau PVM, nei sumokėjo. Taigi juridinis subjektas skolingas mokesčių institucijai. 

Juridinis subjektas nori naudoti apvalinimo metodą, kuris apvalina likutį iki artimiausio 1,00. Naudotojas, atsakingas už PVM apskaitą, atlieka toliau nurodytus veiksmus.

1. Spustelėkite **Mokestis** > **Netiesioginiai mokesčiai** > **PVM** > **PVM institucijos**.
2. „FastTab“ konteineryje **Bendra** esančiame lauke **Apvalinimo forma** pasirinkite **Įprasta**.
3. Lauke **Apvalinimas** įveskite 1,00.
4. Kai ateina laikas mokėti PVM mokesčių inspekcijai, eikite į **Mokestis** > **Deklaracijos** > **PVM** > **Sudengti ir užregistruoti PVM**. PVM sudengimo sąskaitoje galite matyti, kad mokesčių skolos suma **98 765,43** suapvalinama iki **98 765**.

Toliau pateikiamoje lentelėje parodoma, kaip 98 765,43 suma suapvalinama taikant kiekvieną apvalinimo metodą, galimą puslapio **PVM rinkėjai** lauke **Apvalinimo forma**.

> [!NOTE]                                                                                  
> Jei apvalinimo reikšmė nustatyta kaip 0,00, tada:
>
> - Apvalinant įprastai, apvalinimo veiksmas yra toks pats, kaip **Apvalinimas = 0,01**.
> - Naudojant **Apvalinimo formos parinktys**, **Mažinant**, **Apvalinimas** ir **Pranašumas**, veiksmas yra toks pats kaip **Apvalinimas = 1,00**.

| Apvalinimo formos parinktis                | Apvalinimo vertė = 0,01 | Apvalinimo vertė = 0,10 | Apvalinimo vertė = 1,00 | Apvalinimo vertė = 100,00 | Apvalinimo vertė = 0,00   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| Įprasta                              | 98,765.43              | 98,765.40              | 98,765.00              | 98,800.00                | 98,765.43                |
| Žemyn                            | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Apvalinimas į didesnę pusę                         | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |
| Pranašumas, kredito balansas | 98,765.43              | 98,765.40              | 98,765.00              | 98,700.00                | 98,765.00                |
| Pranašumas, debeto balansas  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                | 98,766.00                |

### <a name="normal-round-and-round-precision-is-001"></a>Įprastas apvalinimas, o apvalinimo tikslumas yra 0,01

```<table>
  <tr>
    <td>Rounding
    </td>
    <td>Calculation process
    </td>
  </tr>
    <tr>
    <td>round(1.015, 0.01) = 1.02
    </td>
    <td>
      <ol>
        <li>round(1.015 / 0.01, 0) = round(101.5, 0) = 102
        </li>
        <li>102 * 0.01 = 1.02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.014, 0.01) = 1.01
    </td>
    <td> <ol>
        <li>round(1.014 / 0.01, 0) = round(101.4, 0) = 101
        </li>
        <li>101 * 0.01 = 1.01
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.011, 0.02) = 1.02
    </td>
    <td> <ol>
        <li>round(1.011 / 0.02, 0) = round(50.55, 0) = 51
        </li>
        <li>51 * 0.02 = 1.02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>round(1.009, 0.02) = 1.00
    </td>
    <td> <ol>
        <li>round(1.009 / 0.02, 0) = round(50.45, 0) = 50
        </li>
        <li>50 * 0.02 = 1.00
        </li>
      </ol>
    </td>
  </tr>
</table>
```

> [!NOTE]                                                                                  
> Jei pasirinksite Pranašumas, visada bus apvalinama juridinio subjekto naudai. 

Daugiau informacijos ieškokite šiose temose:
- [PVM apžvalga](indirect-taxes-overview.md)
- [PVM mokėjimo kūrimas](tasks/create-sales-tax-payment.md)
- [PVM operacijų kūrimas dokumentuose](tasks/create-sales-tax-transactions-documents.md)
- [Registruotų PVM operacijų peržiūra](tasks/view-posted-sales-tax-transactions.md)
- [apvalinimo funkcija](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
