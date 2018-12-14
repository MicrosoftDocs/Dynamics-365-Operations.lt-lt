---
title: "„Retail” kliento SF ir grąžinimo pardavimo užsakymai Rytų Europos šalyse"
description: "Šioje temoje aprašoma, kaip nustatyti informaciją apie kliento SF ir grąžinimo pardavimo užsakymus Rytų Europos šalyse."
author: epopov
manager: annbe
ms.date: 10/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 01239f0eff3e59f62188fca64f99e93be843d2e2
ms.openlocfilehash: 20ae19fb03acb075b6553b95808779c905bcd31b
ms.contentlocale: lt-lt
ms.lasthandoff: 10/24/2018

---

# <a name="retail-customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a>„Retail” kliento SF ir grąžinimo pardavimo užsakymai Rytų Europos šalyse


[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip nustatyti informaciją apie kliento SF ir grąžinimo pardavimo užsakymus Rytų Europos šalyse.

Galite nustatyti toliau nurodytą kliento SF ir grąžinimo pardavimo užsakymų, sugeneruotų naudojantis mažmeninės prekybos elektroniniu kasos aparatu (EKA), informaciją.

- Norėdami apdoroti grąžinimus naudodami grąžinimo pardavimo užsakymus, galite naudoti PVM grupes. Eikite į **Mažmeninė prekyba > Būstinės sąranka > Parametrai > Mažmeninės prekybos parametrai**. Atidarykite skirtuką **Registravimas > Sąskaita faktūra**, paskui nustatykite funkcijos **Taikyti PVM grupę grąžinimams** parinktį **Taip**. 

  * Norėdami nurodyti kliento atliktų grąžinimų PVM grupę, puslapyje **Klientai**, „FastTab“ skirtuko **Mažmeninė prekyba** lauke **PVM grupė, taikoma grąžinimams**, pasirinkite PVM grupę. Kai registruojate kliento grąžinimo pardavimo užsakymą, grąžinimo pardavimo užsakymo eilutė atnaujinama įtraukiant formoje **Klientas** nurodytą grąžinimų PVM grupę.
  
  * Norėdami nurodyti „Retail POS“ kliento atliktų grąžinimų PVM grupę, puslapyje **Parduotuvės**, „FastTab“ skirtuko **Bendra** lauke **PVM grupė, taikoma grąžinimams**, pasirinkite PVM grupę. Kai registruojate mažmeninės prekybos parduotuvės kliento grąžinimo pardavimo užsakymą, grąžinimo pardavimo užsakymo eilutė atnaujinama įtraukiant puslapyje **Parduotuvės** nurodytų grąžinimų PVM grupę.

- Jei sąskaita faktūra arba grąžinimas neturi numatytosios pardavimo datos, kaip sąskaitos faktūros arba grąžinimo pardavimo datą galite naudoti mažmeninės prekybos kliento SF arba grąžinimo SF registravimo datą. Eikite į **Mažmeninė prekyba > Būstinės sąranka > Parametrai > Mažmeninės prekybos parametrai**. Atidarykite skirtuką **Registravimas > Sąskaita faktūra**, paskui nustatykite funkcijos **Naudoti registravimo datą kaip pardavimo datą** parinktį **Taip**.

- Numeruodami Latvijos ir Lietuvos klientų SF ir grąžinimo pardavimo užsakymus galite naudoti mokesčių institucijų nurodytą numeraciją. 

  * Eikite į **Organizacijos administravimas > Numeracijos > Skaitiklių valdymas**. Turi būti įrašas, kuriame **Modulis** = **Pardavimas** ir **Tipas** = **Sąskaita faktūra**.

  * Eikite į **Organizacijos administravimas > Numeracijos > SF numeravimo nustatymas**. Pažymėkite numeracijos eilutės, naudojamos kliento SF numeruoti, žymės langelį **Mažmeninė prekyba**.
