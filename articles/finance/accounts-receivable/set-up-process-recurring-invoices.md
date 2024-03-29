---
title: Pasikartojančių SF nustatymas ir apdorojimas
description: Šiame straipsnyje paaiškinta, kaip nustatyti ir apdoroti pasikartojančias SF. Pasikartojančias SF galite naudoti, jei klientams reguliariai turite išrašyti SF už tą pačią sumą.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: kfend
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce734567f0c5bf02e30c36484449c3869b82dc84
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724761"
---
# <a name="set-up-and-process-recurring-invoices"></a>Pasikartojančių SF nustatymas ir apdorojimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinta, kaip nustatyti ir apdoroti pasikartojančias SF. Pasikartojančias SF galite naudoti, jei klientams reguliariai turite išrašyti SF už tą pačią sumą.

## <a name="create-a-recurring-free-text-invoice-template"></a>Periodinio laisvos formos SF šablono sukūrimas

Norėdami reguliariai siųsti klientams SF už tas pačias paslaugas, turite nustatyti laisvos formos SF šabloną, kurį būtų galima pakartotinai naudoti SF kurti. Šiame šablone pateikiama ši informacija:

-   Antraštės informacija, pvz., mokesčių grupės, mokėjimo sąlygos ir mokėjimo būdas
-   Eilutės informacija, pvz., aptarnavimo aprašymas, įplaukų sąskaitos, vieneto kaina ir SF suma
-   Siuntimo ar tvarkymo išlaidos
-   Apskaitos paskirstymai kartu su finansinės dimensijos informaciją, pvz., išlaidų centrai ir verslo vienetai

Iš esmės jūs sukuriate visą SF ir išsaugote ją kaip šabloną. Galite nustatyti šablonus naudodami puslapį **Pasikartojančios SF**.

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a>Pasikartojančio laisvos formos SF šablono priskyrimas klientui ir pasikartojančios informacijos įvedimas
Sukūrę šabloną, turite jį priskirti klientams, kuriems norite išrašyti SF. Be to, turite nurodyti, kada ir kaip dažnai ši SF bus naudojama. Galite priskirti šablonus puslapio **Klientai** skirtuke **SF**. Įtraukite šabloną į sąrašą ir atnaujinkite šią informaciją:

-   Pasikartojančių sąskaitų teikimo pradžios data ir, pasirinktinai, pabaigos data
-   Kaip dažnai siunčiamos pasikartojančios sąskaitos (pvz., kiekvieną dieną arba vieną kartą per mėnesį)
-   Didžiausia sąskaitos suma (jei ši informacija yra būtina)

Klientas gali turėti kelis skirtingo dažnumo šablonus.

## <a name="generate-the-recurring-invoices"></a>Pasikartojančių SF generavimas
Puslapyje **Pasikartojančios SF** yra užduotis, kuri apdoroja pasikartojančių SF šablonus. Galite nurodyti SF datą ir šabloną, pagal kurį generuosite SF. Bus sugeneruotos SF ir kiekvienai apdorotai SF grupei priskirtas atskiras pasikartojimo ID numeris.

## <a name="post-recurring-free-text-invoices"></a>Pasikartojančių laisvos formos SF registravimas

Sugeneravus pasikartojančias SF, SF pasikartojimo ID rodomas registravimo užduotyje puslapyje **Pasikartojančios SF**. Galite peržiūrėti visas pasikartojimo ID SF spustelėdami saitą. Peržiūrėdami pasikartojimo ID SF galite panaikinti atskiras SF. Kliento pasikartojimo parametrai tame šablone bus nustatyti iš naujo, kad vėliau jį būtų galima vėl sugeneruoti. Galite registruoti vieną, kelias arba visas pasikartojimo ID SF. Jei įgalintos darbo eigos, turite spustelėti **Pateikti**, tada galėsite registruoti SF.

## <a name="print-recurring-free-text-invoices"></a>Pasikartojančių laisvos formos SF spausdinimas

Užregistravę pasikartojančias SF, galite spausdinti SF laisvos formos SF sąrašo puslapyje. Galite spausdinti SF, kurios yra pasirinktos, arba galite pasirinkti spausdinti SF diapazoną.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
