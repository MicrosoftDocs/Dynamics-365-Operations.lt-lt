---
title: Bendrasis vietos padengimo, sandėlis privalomas
description: Šiame straipsnyje aprašoma, kaip suplanuota prekė, kurios svetainė yra padengimo dimensija. Sandėlis yra privaloma dimensija.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df58017c25737cc946d09bf86ff7ad8bd33f4176
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741046"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>Bendrasis vietos padengimo, sandėlis privalomas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip suplanuota prekė, kurios svetainė yra padengimo dimensija. Sandėlis yra privaloma dimensija.

Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.

-   Vietos dimensija yra nustatoma kaip privaloma ir turi būti įvesta vykdant poreikio operaciją. Šios nuostatos modifikuoti negalima.
-   Sandėlio dimensija yra nustatoma kaip privaloma ir turi būti įvesta poreikio operacijos metu.
-   Teritorijos dimensija yra nustatyta padengimo planavimui. Kitos dimensijos taip pat gali būti nustatytos padengimo planavimui. Tačiau jų neveikia kelių teritorijų funkcionalumas.
-   Sandėlio dimensija nėra nustatyta padengimo planavimui. Todėl tiekimas ir poreikis sujungiami pagal teritoriją ir galbūt kitas suplanuotas padengimo dimensijas.

Toliau pateiktame grafikos objekte iliustruojama, kaip vyksta bendrasis planavimas. Parametrai, rodomi grafikos duomenyse, ir jų vietos yra tokios:
-   Prekės padengimas yra apibrėžiamas prekei. Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**. Pasirinkite prekę ir tada spustelėkite **Planuoti &gt; Prekių padengimas**.
-   Papildymo ryšiai apibrėžiami sandėliui. Spustelėkite **Atsargų valdymas &gt; Sąranka &gt; Atsargų paskirstymas &gt; Sandėliai**. **Bendrojo planavimo** skirtuke žr. laukų grupę **Pagrindinis sandėlis**.
-   Nustatytas numatytasis užsakymo tipas yra Gamybos, Pirkimo užsakymas arba „kanban“. Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**. Pasirinkite prekę ir tada spustelėkite **Planuoti &gt; Numatytosios užsakymo nuostatos**. Formoje **Numatytosios užsakymo nuostatos** žr. **Numatytasis užsakymo tipas**.

![Teritorijos padengimo poreikis, sandėlis privalomas.](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a>Papildomi ištekliai

- [Bendrojo planavimo ir kelių teritorijų funkcijos apžvalga](master-plan-multisite-functionality.md)
- [Bendrasis vietos ir sandėlio padengimo planas, sandėlis privalomas](master-plan-site-warehouse-coverage-warehouse-mandatory.md)
- [Bendrasis vietos padengimo, sandėlis privalomas](master-plan-site-coverage-warehouse-mandatory.md)
- [Bendrasis vietos ir sandėlio padengimo planas, sandėlis neprivalomas](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [KS versijos nustatymas](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]