---
title: Klientų SF ir grąžinimo pardavimo užsakymai Rytų Europos šalyse
description: Šioje temoje aprašoma, kaip nustatyti informaciją apie kliento SF ir grąžinimo pardavimo užsakymus Rytų Europos šalyse.
author: epopov
manager: annbe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: f5b46748ad2f780bfd56078631f3ac66814df9cc
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018847"
---
# <a name="customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a>Klientų SF ir grąžinimo pardavimo užsakymai Rytų Europos šalyse


[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip nustatyti informaciją apie kliento SF ir grąžinimo pardavimo užsakymus Rytų Europos šalyse.

Galite nustatyti toliau nurodytą kliento SF ir grąžinimo pardavimo užsakymų, sugeneruotų naudojantis mažmeninės prekybos elektroniniu kasos aparatu (EKA), informaciją.

- Norėdami apdoroti grąžinimus naudodami grąžinimo pardavimo užsakymus, galite naudoti PVM grupes. Eikite į **Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Parametrai \> Prekybos parametrai**. Atidarykite skirtuką **Registravimas \> Sąskaita faktūra**, tada nustatykite funkcijos **Taikyti PVM grupę grąžinimams** parinktį **Taip**.

    * Norėdami nurodyti kliento atliktų grąžinimų PVM grupę, puslapyje **Klientai**, „FastTab“ **Prekyba** lauke **PVM grupė, taikoma grąžinimams**, pasirinkite PVM grupę. Kai registruojate kliento grąžinimo pardavimo užsakymą, grąžinimo pardavimo užsakymo eilutė atnaujinama įtraukiant formoje **Klientas** nurodytą grąžinimų PVM grupę.
    * Norėdami nurodyti „Retail POS“ kliento atliktų grąžinimų PVM grupę, puslapyje **Parduotuvės**, „FastTab“ skirtuko **Bendra** lauke **PVM grupė, taikoma grąžinimams**, pasirinkite PVM grupę. Kai registruojate parduotuvės kliento grąžinimo pardavimo užsakymą, grąžinimo pardavimo užsakymo eilutė atnaujinama įtraukiant puslapyje **Parduotuvės** nurodytų grąžinimų PVM grupę.

- Jei sąskaita faktūra arba grąžinimas neturi numatytosios pardavimo datos, kaip sąskaitos faktūros arba grąžinimo pardavimo datą galite naudoti kliento SF arba grąžinimo SF registravimo datą. Eikite į **Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Parametrai \> Prekybos parametrai**. Atidarykite skirtuką **Registravimas \> Sąskaita faktūra**, paskui nustatykite funkcijos **Naudoti registravimo datą kaip pardavimo datą** parinktį **Taip**.
- Numeruodami Latvijos ir Lietuvos klientų SF ir grąžinimo pardavimo užsakymus galite naudoti mokesčių institucijų nurodytą numeraciją.

    * Pasirinkite **Organizacijos administravimas \> Numeracijos \> Skaitiklių valdymas**. Turi būti įrašas, kuriame **Modulis** = **Pardavimas** ir **Tipas** = **Sąskaita faktūra**.
    * Pasirinkite **Organizacijos administravimas \> Numeracijos \> SF numeravimo nustatymas**. Pažymėkite numeracijos eilutės, naudojamos kliento SF numeruoti, žymės langelį **Prekyba**.
