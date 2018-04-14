---
title: "PVM mokėjimo ir apvalinimo taisyklės"
description: "Šiame straipsnyje paaiškinama, kaip srityje PVM rinkėjai veikia apvalinimo taisyklės nustatymas ir paaiškinamas PVM balansas vykdant užduotį Sudengti ir užregistruoti PVM."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 13470282efc6b9135e86355cf8071b841aad3071
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="sales-tax-payments-and-rounding-rules"></a>PVM mokėjimo ir apvalinimo taisyklės

[!INCLUDE [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip srityje PVM rinkėjai veikia apvalinimo taisyklės nustatymas ir paaiškinamas PVM balansas vykdant užduotį Sudengti ir užregistruoti PVM.

Periodiškai reikia pranešti apie PVM ir sumokėti jį mokesčių institucijoms. Tai galite padaryti atlikdami sudengimą ir registruodami PVM procesą puslapyje PVM. Laikotarpio PVM bus sudengtas pagal PVM sąskaitas ir PVM balansas bus registruojamas PVM sudengimo sąskaitoje. PVM balansą, registruojamą PVM sudengimo sąskaitoje, galima apvalinti pagal mokesčių institucijos reikalavimus, nustačius apvalinimo taisyklę puslapyje PVM. 

Apvalinimo skirtumas užregistruojamas PVM apvalinimo sąskaitoje, pasirinktoje dalies Didžioji knyga lauke Automatinių operacijų sąskaitos.

Tolesniame pavyzdyje pavaizduota, kaip veikia apvalinimo taisyklė PVM institucijai.

### <a name="example"></a>Pavyzdys:

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
| Pranašumas, debeto balansas  | 98 765,43              | 98 765,50              | 98 766,00              | 98 800,00                |

> [!NOTE]                                                                                  
> Jei pasirinksite Pranašumas, visada bus apvalinama juridinio subjekto naudai. 

Daugiau informacijos ieškokite šiose temose:
- [PVM apžvalga](indirect-taxes-overview.md)
- [Kurti PVM mokėjimą](tasks/create-sales-tax-payment.md)
- [Kurti pardavimo operacijas dokumentuose](tasks/create-sales-tax-transactions-documents.md)
- [Peržiūrėti užregistruotas PVM operacijas](tasks/view-posted-sales-tax-transactions.md)



