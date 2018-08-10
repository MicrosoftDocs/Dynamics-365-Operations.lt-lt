---
title: "Šabloninės KS kūrimas"
description: "Galite sukurti šabloninę KS naudodamiesi įvairiais būdais."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a80cf596a3e7c7f08d493a0fb7350fad62d38c3e
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="create-a-template-bom"></a>Šabloninės KS kūrimas   

[!include [banner](../includes/banner.md)]


Galite sukurti šabloninę KS naudodamiesi bet kuriuo iš toliau pateiktų būdų. Visiems būdams laukai **Pradžios data** ir **Pabaigos data** yra pasirenkamieji ir skirti tik informacijai.

## <a name="create-a-template-bom-manually"></a>KS ruošinio kūrimas rankiniu būdu

1.  Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.

2.  Paspaudę CTRL+N atidarykite formą **Kurti šabloninę KS**.

3.  Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite parinktį **Rankiniu būdu**.

4.  Lauke **Prekės numeris** įveskite **KS** tipo prekę.

5.  Lauke **Pavadinimas** įveskite šablono pavadinimą.

6.  Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.

7.  Spustelėkite **GERAI**.

Sukuriama nauja tuščia šabloninė KS.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>KS ruošinio, paremto kitu KS ruošiniu, kūrimas

1.  Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.

2.  Paspaudę CTRL+N atidarykite formą **Kurti šabloninę KS**.

3.  Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite parinktį **Šabloninė KS**.

4.  Lauke **Nuorodos numeris** pasirinkite esamą KS ruošinį, kurį norite kopijuoti į savo naują KS ruošinį.

5.  Lauke **Pavadinimas** įveskite šablono pavadinimą.

6.  Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.

7.  Spustelėkite **GERAI**.

Sukuriama nauja šabloninė KS su eilutėmis, atitinkančiomis eilutes originalioje šabloninėje KS.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>KS ruošinio, paremto prekės KS kūrimas

1.  Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.

2.  Paspaudę CTRL+N atidarykite formą **Kurti šabloninę KS**.

3.  Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite **KS**.

4.  Lauke **Nuorodos numeris** pasirinkite KS versiją. KS tipo prekė nukopijuojama į **Prekės numeris**.

5.  Lauke **Pavadinimas** įveskite šablono pavadinimą.

6.  Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.

7.  Spustelėkite **GERAI**.

Naujas KS ruošinys sukurtas, naudojant eilutes, atitinkančias KS eilutes, išvardytas **Komplektavimo specifikacijos**.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>KS ruošinio, paremto gamybos KS, kūrimas

1.  Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.

2.  Paspaudę CTRL+N atidarykite formą **Kurti šabloninę KS**.

3.  Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite **Gamyba**.

4.  Lauke **Nuorodos numeris** pasirinkite gamybos KS.

5.  Lauke **Pavadinimas** įveskite šablono pavadinimą.

6.  Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.

7.  Spustelėkite **GERAI**.

Naujas KS ruošinys sukurtas, naudojant eilutes, atitinkančias KS eilutes, išvardytas **KS**.

## <a name="see-also"></a>Taip pat žiūrėkite

[Šabloninės KS](template-boms.md)

  



