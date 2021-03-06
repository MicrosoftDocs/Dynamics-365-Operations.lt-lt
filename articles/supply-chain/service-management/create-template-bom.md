---
title: Šabloninės KS kūrimas
description: Galite sukurti šabloninę KS naudodamiesi įvairiais būdais.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 781df7611ec1e3ee9d3013f971232700df38ada0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836307"
---
# <a name="create-a-template-bom"></a>Šabloninės KS kūrimas   

[!include [banner](../includes/banner.md)]


Galite sukurti šabloninę KS naudodamiesi bet kuriuo iš toliau pateiktų būdų. Visiems būdams laukai **Pradžios data** ir **Pabaigos data** yra pasirenkamieji ir skirti tik informacijai.

## <a name="create-a-template-bom-manually"></a>KS ruošinio kūrimas rankiniu būdu

1.  Eikite į **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.

2.  Pasirinkę **Naujas** atidarykite formą **Kurti šabloninę KS**.

3.  Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite parinktį **Rankiniu būdu**.

4.  Lauke **Prekės numeris** įveskite **KS** tipo prekę.

5.  Lauke **Pavadinimas** įveskite šablono pavadinimą.

6.  Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.

7.  Pasirinkite **Gerai**.

Sukuriama nauja tuščia šabloninė KS.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>KS ruošinio, paremto kitu KS ruošiniu, kūrimas

1.  Pasirinkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.

2.  Pasirinkę **Naujas** atidarykite formą **Kurti šabloninę KS**.

3.  Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite parinktį **Šabloninė KS**.

4.  Lauke **Nuorodos numeris** pasirinkite esamą KS ruošinį, kurį norite kopijuoti į savo naują KS ruošinį.

5.  Lauke **Pavadinimas** įveskite šablono pavadinimą.

6.  Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.

7.  Pasirinkite **Gerai**.

Sukuriama nauja šabloninė KS su eilutėmis, atitinkančiomis eilutes originalioje šabloninėje KS.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>KS ruošinio, paremto prekės KS kūrimas

1.  Pasirinkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.

2.  Pasirinkę **Naujas** atidarykite formą **Kurti šabloninę KS**.

3.  Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite **KS**.

4.  Lauke **Nuorodos numeris** pasirinkite KS versiją. KS tipo prekė nukopijuojama į **Prekės numeris**.

5.  Lauke **Pavadinimas** įveskite šablono pavadinimą.

6.  Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.

7.  Pasirinkite **Gerai**.

Naujas KS ruošinys sukurtas, naudojant eilutes, atitinkančias KS eilutes, išvardytas **Komplektavimo specifikacijos**.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>KS ruošinio, paremto gamybos KS, kūrimas

1.  Pasirinkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo objektai** \> **Šabloninės KS**.

2.  Pasirinkę **Naujas** atidarykite formą **Kurti šabloninę KS**.

3.  Dalyje **Kopijuoti KS eilutes iš nuorodos** pasirinkite **Gamyba**.

4.  Lauke **Nuorodos numeris** pasirinkite gamybos KS.

5.  Lauke **Pavadinimas** įveskite šablono pavadinimą.

6.  Laukuose **Pradžios data** ir **Pabaigos data** įveskite laiko intervalą, kuriuo bus aktyvi šabloninė KS.

7.  Pasirinkite **Gerai**.

Naujas KS ruošinys sukurtas, naudojant eilutes, atitinkančias KS eilutes, išvardytas **KS**.

## <a name="see-also"></a>Taip pat žiūrėkite

[Šabloninės KS](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]