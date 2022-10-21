---
title: SF fiksavimo sprendimo skelbimų sritis
description: Šiame straipsnyje aprašoma SF fiksavimo sprendimų skelbimų sritis.
author: sunfzam
ms.date: 10/15/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4c9000039488c1290f4ab992d7fe79b8ccac7b19
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690152"
---
# <a name="invoice-capture-solution-dashboard"></a>SF fiksavimo sprendimo skelbimų sritis

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Sf fiksavime skelbimų srityje yra diagramos, kurios pateikia importuotų SF peržiūrą. Šios diagramos gali padėti mokėtinų sumų (AP) vadybininkui analizuoti SF generavimo proceso efektyvumą. AP vadovas gali peržiūrėti SF generavimo proceso būseną, o pritaikęs skirtingus filtrus taip pat gali peržiūrėti informaciją.

## <a name="available-charts"></a>Galimos diagramos

Šios diagramos yra skelbimų skelbimų srityje:

- **Visa užfiksuota SF pagal būseną** – šioje diagramoje rodomos šios užfiksuotos SF būsenos. Pasirinkdami būseną vartotojai gali filtruoti užfiksuotas SF išsamiuose sąraše.

    - Užfiksuoti
    - Baigta
    - Peržiūrima
    - Nebenaudojama

- **Bendroji užfiksuotos SF apimtis** – šioje diagramoje rodomas užfiksuotas SF skaičius pagal laikotarpį. Laikotarpį vartotojai gali keisti naudodami išplečiamąjį sąrašą.
- **Užfiksuota SF iš geriausių tiekėjų** – šioje diagramoje rodomas bendras tiekėjo SF skaičius. Viršuje rodomi tiekėjai, kurių SF yra daugiausia.
- **DIENOS, kurios turi būti užbaigtos vienai SF su** išimtimis – šioje diagramoje rodomas vidutinis dienų, kurių reikia vienai SF užfiksuoti, skaičius. Ši informacija gali padėti AP vadybininkui analizuoti SF vykdymo laiką, kai reikalingas neautomatinis veiksmai. Jei yra aukštyn esanti tendencija, vartotojai gali peržiūrėti proceso informaciją ir koreguoti parametrus, kad padėtų sumažinti reikalaujamą dienų skaičių.
- **Nebaigtos** SF pagal laukiantį laiką – šioje diagramoje rodomas dienų, kurias užfiksuota SF nebuvo sugeneruota įmonės išteklių planavimo (ERP) sistemoje, skaičius. Kuo didesnis laukiančių dienų skaičius, tuo ilgesnis SF generavimo procesas. AP vadovas gali detalizuoti detaliai užfiksuotas SF ir generuoti SF ERP sistemoje.
