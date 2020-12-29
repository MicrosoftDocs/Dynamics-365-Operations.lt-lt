---
title: Darbo krūvio pajėgumo planavimas
description: Šioje temoje paaiškinama, kaip nustatyti ir planuoti sandėlio darbuotojų arba visą sandėlio darbo krūvio pajėgumą.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd4225d9e7ad65939c57cb770ba521377c87dea3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433383"
---
# <a name="schedule-workload-capacity"></a>Darbo krūvio pajėgumo planavimas

[!include[banner](../includes/banner.md)]

Galite planuoti darbo krūvio pajėgumus sandėliuose, taip pat prognozuoti dabartinius ir būsimus darbuotojų darbo krūvius atskiruose sandėliuose. Galite prognozuoti viso sandėlio darbo krūvį arba galite prognozuoti darbo krūvį atskirai pagal įeinančio ir išeinančio darbo krūvius.

Norint prognozuoti darbo krūvį pasirinktuose sandėliuose, turi būti prieinami tų sandėlių bendrojo planavimo duomenys. Daugiau informacijos žr. [Bendrųjų planų apžvalga](../master-planning/master-plans.md).

## <a name="schedule-and-view-workloads-for-a-warehouse"></a>Planuoti ir peržiūrėti darbo krūvius sandėlyje

Norėdami suplanuoti darbo krūvį sandėliui, galite sukurti darbo krūvio nustatymą vienam ar keliems sandėliams, ir tada susieti darbo krūvio nustatymą su pagrindiniu planu. Atlikdami darbo krūvio pajėgumo sąranką galite nustatyti įeinančių ir išeinančių operacijų ribas svoriui arba tūriui. Taip pat galite sukurti daugiau nei vieną kiekvieno sandėlio nustatymą, o po to susieti tą nustatymą su atskirais bendraisiais planais. Pavyzdžiui, naudodamiesi šiuo metodu galite prisitaikyti prie sezoninių darbo jėgos pokyčių.

Jei sandėlio darbininkai dirba ir su įeinančio, ir su išeinančio darbo krūvio operacijomis, sandėlio pajėgumų nustatymą galite sukonfigūruoti taip, kad galėtumėte prognozuoti bendrą darbo krūvį.

Norėdami planuoti ir peržiūrėti sandėlių darbo krūvius, turite atlikti toliau nurodytas užduotis.

1. Sukurti darbo krūvio pajėgumų nustatymą ir apibrėžti darbo krūvio pajėgumų ribas viename ar keliuose sandėliuose.
2. Susieti darbo krūvio pajėgumų nustatymą su pagrindinį planu, kad sukurtumėte darbo krūvio prognozes ir nurodytumėte, kiek laiko tos prognozės bus taikomos.

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a>Sukurti darbo krūvio pajėgumų nustatymą sandėliui

1. Pasirinkite **Atsargų valdymas** \> **Sąranka** \> **Sandėlio stebėjimas** \> **Darbo krūvio pajėgumas**.
2. Veiksmų srityje pasirinkę **Nauja** sukurkite darbo krūvio pajėgumų nustatymą.
3. „FastTab“ skirtuke **Sandėliai** pasirinkite **Naujas**, po to eilutėje įveskite reikšmes, kad susietumėte sandėlį su darbo krūvio pajėgumų nustatymu.
4. Jei ataskaitoje **Darbo krūvio pajėgumas** viename rodinyje turėtų būti rodomos įeinančios ir išeinančios operacijos, pažymėkite žymės langelį **Bendras gaunamas ir siunčiamas darbo krūvis**.
5. „FastTab“ skirtuke **Operacijų tipai** pasirinkite įeinančių ir išeinančių operacijų tipus, kuriems bus taikomos darbo krūvio ribos.

    > [!NOTE]
    > Turite pasirinkti bent vieną įeinančio ir išeinančio darbo krūvio operacijos tipą.

#### <a name="define-limits-for-volume-or-weight"></a>Nustatykite tūrio ir svorio ribas

Galite nustatyti tūrio ar svorio ribas, priklausomai nuo to, koks apribojimas taikomas sandėlio darbo jėgai. Apribojimai, kuriuos nurodote, yra įtraukti į darbo krūvio pajėgumų prognozę, kurią galite peržiūrėti ataskaitoje **Darbo krūvio pajėgumas**.

Norint prognozuoti informaciją apie prekių tūrį ir svorį, visiems produktams turi būti nurodytas standartinis atsargų prekės tūris ir vienos atsargų prekės svoris. Reikiamus laukus galima rasti toliau nurodytose puslapio **Patvirtinto produkto informacija** „FastTab“ skirtuko **Atsargų tvarkymas** laukų grupėse.

- Tvarkymas
- Faktinės dimensijos
- Svorio matavimai

Jei nurodyta klaidinga informacija, kurdami ataskaitą **Darbo krūvio pajėgumas** gausite pranešimą. Tada ataskaitoje galėsite įsigilinti į informaciją ir nustatyti, kokios informacijos trūksta norint prognozuoti būsimą darbo krūvį.

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a>Susieti darbo krūvio pajėgumų nustatymą su bendruoju planu

1. Pasirinkite **Atsargų valdymas** \> **Periodinis** \> **Darbo krūvio planavimas**.
2. Lauke **Bendrasis planas** pasirinkite bendrąjį planą, kurį norite naudoti prognozuodami darbo krūvį.
3. Lauke **Dienų skaičius** nurodykite dienų, kurioms parengta darbo krūvio prognozė, skaičių.
4. Lauke **Darbo krūvis** pasirinkite darbo krūvio nustatymą, kurį norite susieti su bendruoju planu.

### <a name="view-workload-capacity"></a>Peržiūrėti darbo krūvio pajėgumus

1. Pasirinkite **Atsargų valdymas** \> **Užklausos ir ataskaitos** \> **Fizinės atsargų ataskaitos** \> **Darbo krūvio pajėgumas**.
2. Lauke **Stulpelių skaičius** nurodykite ataskaitoje rodomų stulpelių skaičių.
3. Lauke **Užsakymo tipas** pasirinkę **Suplanuotas ir patvirtintas**, **Suplanuotas** arba **Patvirtintas** nurodykite užsakymų tipą, kurio prognozės pateikiamos ataskaitoje.
4. Lauke **Load type** pasirinkę apkrovos tipą nurodykite, ar turėtų būti prognozuojami tūrio ar svorio darbo krūvio pajėgumai.
5. Lauke **Darbo krūvio pajėgumas** pasirinkite darbo krūvio pajėgumų nustatymą.
