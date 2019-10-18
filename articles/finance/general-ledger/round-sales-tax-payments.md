---
title: PVM mokėjimo ir apvalinimo taisyklės
description: Šiame straipsnyje paaiškinama, kaip srityje PVM rinkėjai veikia apvalinimo taisyklės nustatymas ir paaiškinamas PVM balansas vykdant užduotį Sudengti ir užregistruoti PVM.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 168c2fb9edfc994617ef6764a5b9f5949d599882
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186330"
---
# <a name="sales-tax-payments-and-rounding-rules"></a>PVM mokėjimo ir apvalinimo taisyklės

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip srityje PVM rinkėjai veikia apvalinimo taisyklės nustatymas ir paaiškinamas PVM balansas vykdant užduotį Sudengti ir užregistruoti PVM.

Periodiškai reikia pranešti apie PVM ir sumokėti jį mokesčių institucijoms. Tai galite padaryti atlikdami sudengimą ir registruodami PVM procesą puslapyje PVM. Laikotarpio PVM bus sudengtas pagal PVM sąskaitas ir PVM balansas bus registruojamas PVM sudengimo sąskaitoje. PVM balansą, registruojamą PVM sudengimo sąskaitoje, galima apvalinti pagal mokesčių institucijos reikalavimus, nustačius apvalinimo taisyklę puslapyje PVM. 

Apvalinimo skirtumas užregistruojamas PVM apvalinimo sąskaitoje, pasirinktoje dalies Didžioji knyga lauke Automatinių operacijų sąskaitos.

Tolesniame pavyzdyje pavaizduota, kaip veikia apvalinimo taisyklė PVM institucijai.

## <a name="examples"></a>Pavyzdžiai

Rodoma, kad bendrojo laikotarpio PVM kredito balansas yra –98 765,43. Juridinis subjektas surinko daugiau PVM, nei sumokėjo. Taigi juridinis subjektas skolingas mokesčių institucijai. 

Juridinis subjektas nori naudoti apvalinimo metodą, kuris apvalina likutį iki artimiausio 1,00. Naudotojas, atsakingas už PVM apskaitą, atlieka toliau nurodytus veiksmus.

1.  Spustelėkite Mokestis &gt; Netiesioginiai mokesčiai &gt; PVM &gt; PVM rinkėjai
2.  „FastTab“ skirtuke Bendra esančiame lauke Apvalinimo forma pasirinkite parinktį Įprastas.
3.  Lauke Apvalinimas įveskite 1,00.
4.  Kai ateina laikas mokėti PVM mokesčių inspekcijai, atidarykite puslapį Sudengti ir užregistruoti PVM. (Spustelėkite Mokestis &gt; Deklaracijos &gt; PVM &gt; Sudengti ir užregistruoti PVM.)
5.  PVM sudengimo sąskaitoje mokesčių skolos suma 98 765,43 suapvalinama iki 98 765.

Toliau pateikiamoje lentelėje parodoma, kaip 98 765,43 suma suapvalinama taikant kiekvieną apvalinimo metodą, galimą puslapio PVM rinkėjai lauke Apvalinimo forma.

| Apvalinimo formos parinktis                | Apvalinimo vertė = 0,01 | Apvalinimo vertė = 0,10 | Apvalinimo vertė = 1,00 | Apvalinimo vertė = 100,00 |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| Įprastas                              | 98 765,43              | 98 765,40              | 98 765,00              | 98 800,00                |
| Žemyn                            | 98 765,43              | 98 765,40              | 98 765,00              | 98 700,00                |
| Į didesnę pusę                         | 98 765,43              | 98 765,50              | 98 766,00              | 98 800,00                |
| Pranašumas, kredito balansas | 98 765,43              | 98 765,40              | 98 765,00              | 98 700,00                |
| Pranašumas, debeto balansas  | 98,765.43              | 98,765.50              | 98,766.00              | 98,800.00                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a>Apvalinimo nėra, nes apvalinimas yra 0,00

apvalinimas (1,0151; 0,00) = 1,0151 apvalinimas (1,0149; 0,00) = 1.0149

### <a name="normal-round-and-round-precision-is-001"></a>Įprastas apvalinimas, o apvalinimo tikslumas yra 0,01

<table>
  <tr>
    <td>Apvalinimas
    </td>
    <td>Skaičiavimo procesas
    </td>
  </tr>
    <tr>
    <td>apvalinimas (1,015; 0,01) = 1,02
    </td>
    <td>
      <ol>
        <li>apvalinimas (1,015 / 0,01; 0) = apvalinimas (101,5; 0) = 102
        </li>
        <li>102 * 0,01 = 1,02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>apvalinimas (1,014; 0,01) = 1,01
    </td>
    <td> <ol>
        <li>apvalinimas (1,014 / 0,01; 0) = apvalinimas (101,4; 0) = 101
        </li>
        <li>101 * 0,01 = 1,01
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>apvalinimas (1,011; 0,02) = 1,02
    </td>
    <td> <ol>
        <li>apvalinimas (1,011 / 0,02; 0) = apvalinimas (50,55; 0) = 51
        </li>
        <li>51 * 0,02 = 1,02
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td>apvalinimas (1,009; 0,02) = 1,00
    </td>
    <td> <ol>
        <li>apvalinimas (1,009 / 0,02; 0) = apvalinimas (50,45; 0) = 50
        </li>
        <li>50 * 0,02 = 1,00
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> Jei pasirinksite Pranašumas, visada bus apvalinama juridinio subjekto naudai. 

Daugiau informacijos ieškokite šiose temose:
- [PVM apžvalga](indirect-taxes-overview.md)
- [Kurti PVM mokėjimą](tasks/create-sales-tax-payment.md)
- [Kurti pardavimo operacijas dokumentuose](tasks/create-sales-tax-transactions-documents.md)
- [Registruotų PVM operacijų peržiūra](tasks/view-posted-sales-tax-transactions.md)
- [apvalinimo funkcija](https://msdn.microsoft.com/library/aa850656.aspx)


