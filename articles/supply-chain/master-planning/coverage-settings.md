---
title: Padengimo parametrai
description: Šioje temoje pateikiama informacija apie padengimo parametrus, kurie bendrojo planavimo metu naudojami prekių poreikiui skaičiuoti.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538899"
---
# <a name="coverage-settings"></a>Padengimo parametrai

[!include [banner](../includes/banner.md)]

Bendrasis planavimas naudoja padengimo parametrus prekės poreikiui apskaičiuoti.

Galite nurodyti padengimo parametrus keliais būdais:

- Nurodykite padengimo grupės padengimo parametrus.

    Galite sukurti padengimo grupę, kurioje būtų visų su padengimo grupe susijusių produktų parametrai. Norėdami sukurti padengimo grupę, eikite į **Bendrasis planavimas &gt; Sąranka &gt; Padengimas &gt; Padengimo grupės**. Padengimo grupę galite susieti su produktu. Jei saitas yra konkrečios teritorijos, sandėlio ar produkto dimensijos, naudokite puslapio **Prekės padengimas** lauką **Padengimo grupė**. Jei saitas yra bendrasis, neatsižvelgdami į produkto dimensijas, naudokite puslapio **Produkto informacija** sparčiajame skirtuke **Planas** esantį lauką **Padengimo grupė**. Pagal numatytuosius parametrus, jei padengimo grupės nesusiejate su produktu, bendrojo planavimo funkcija kaip numatytąją naudoja puslapyje **Bendrojo planavimo parametrai** nurodytą parinktį Bendroji padengimo grupė.

- Nurodykite produkto padengimo parametrus.

    Galite sukurti konkretaus produkto padengimo parametrus. Eikite į **Produkto informacijos valdymas &gt; Produktai &gt; Patvirtinti produktai**. Pasirinkite produktą ir Veiksmų srities skirtuko **Planas** lauke **Padengimo** grupėje pasirinkite **Prekės padengimas**, kad būtų atidarytas puslapis **Prekės padengimas**. Jei produktas jau susietas su padengimo grupe, galite nepaisyti padengimo grupės parametrų, naudodami lauką **Nepaisyti**. Padengimo parametrams puslapyje**Prekės padengimas** teikiama pirmenybė prieš parametrus puslapyje **Padengimo grupė**.

- Nurodykite produkto padengimo parametrus naudodami vedlį.

    Vediklis nuosekliai pademonstruos pagrindinių prekės padengimo parametrų sąrankos procesą. Veiksmų srities puslapyje **Prekės padengimas** pasirinkite **Vedlys**, kad būtų atidarytas **Prekės padengimo vedlys**.

- Nurodykite dimensijos grupės padengimo parametrus.

    Eikite į **Produkto informacijos valdymas &gt; Produktai &gt; Patvirtinti produktai**. Puslapio **Patvirtinto produkto informacija** sparčiajame skirtuke **Bendra** esančioje sekcijoje **Administravimas** pasirinkite saitą lauke **Saugojimo dimensijų grupė**. Puslapyje **Saugojimo dimensijų grupės** pasirinkite žymės laukelį **Padengimo planas dimensijomis**, kad sukurtumėte saugojimo dimensijų grupės dimensijos padengimo nustatymus. Visose produkto dimensijose, pvz., konfigūracijos, spalvos, dydžio, stiliaus, turi būti pasirinktas laukas **Padengimo planas pagal dimensiją**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Bendrieji planai](master-plans.md)
