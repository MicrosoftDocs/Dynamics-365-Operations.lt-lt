---
title: Klientų SF ir grąžinimo pardavimo užsakymai Rytų Europos šalyse
description: Šiame straipsnyje aprašoma, kaip nustatyti informaciją apie kliento SF ir grąžinamus pardavimo užsakymus Rytų Europos šalyse.
author: EvgenyPopovMBS
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: josaw
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.search.industry: Retail
ms.openlocfilehash: 6ebf3740b9ae93cecd5592a5564574e7f49ab5b4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286549"
---
# <a name="customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a>Klientų SF ir grąžinimo pardavimo užsakymai Rytų Europos šalyse


[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti informaciją apie kliento SF ir grąžinamus pardavimo užsakymus Rytų Europos šalyse.

Galite nustatyti toliau nurodytą kliento SF ir grąžinimo pardavimo užsakymų, sugeneruotų naudojantis mažmeninės prekybos elektroniniu kasos aparatu (EKA), informaciją.

- Norėdami apdoroti grąžinimus naudodami grąžinimo pardavimo užsakymus, galite naudoti PVM grupes. Eikite į **Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Parametrai \> Prekybos parametrai**. Atidarykite skirtuką **Registravimas \> Sąskaita faktūra**, tada nustatykite funkcijos **Taikyti PVM grupę grąžinimams** parinktį **Taip**.

    * Norėdami nurodyti kliento atliktų grąžinimų PVM grupę, puslapyje **Klientai**, „FastTab“ **Prekyba** lauke **PVM grupė, taikoma grąžinimams**, pasirinkite PVM grupę. Kai registruojate kliento grąžinimo pardavimo užsakymą, grąžinimo pardavimo užsakymo eilutė atnaujinama įtraukiant formoje **Klientas** nurodytą grąžinimų PVM grupę.
    * Norėdami nurodyti „Retail POS“ kliento atliktų grąžinimų PVM grupę, puslapyje **Parduotuvės**, „FastTab“ skirtuko **Bendra** lauke **PVM grupė, taikoma grąžinimams**, pasirinkite PVM grupę. Kai registruojate parduotuvės kliento grąžinimo pardavimo užsakymą, grąžinimo pardavimo užsakymo eilutė atnaujinama įtraukiant puslapyje **Parduotuvės** nurodytų grąžinimų PVM grupę.

- Jei sąskaita faktūra arba grąžinimas neturi numatytosios pardavimo datos, kaip sąskaitos faktūros arba grąžinimo pardavimo datą galite naudoti kliento SF arba grąžinimo SF registravimo datą. Eikite į **Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Parametrai \> Prekybos parametrai**. Atidarykite skirtuką **Registravimas \> Sąskaita faktūra**, paskui nustatykite funkcijos **Naudoti registravimo datą kaip pardavimo datą** parinktį **Taip**.
- Numeruodami Latvijos ir Lietuvos klientų SF ir grąžinimo pardavimo užsakymus galite naudoti mokesčių institucijų nurodytą numeraciją.

    * Pasirinkite **Organizacijos administravimas \> Numeracijos \> Skaitiklių valdymas**. Turi būti įrašas, kuriame **Modulis** = **Pardavimas** ir **Tipas** = **Sąskaita faktūra**.
    * Pasirinkite **Organizacijos administravimas \> Numeracijos \> SF numeravimo nustatymas**. Pažymėkite numeracijos eilutės, naudojamos kliento SF numeruoti, žymės langelį **Prekyba**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
