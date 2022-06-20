---
title: Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis neprivalomas
description: Šiame straipsnyje aprašoma, kaip suplanuota prekė, kurios padengimo vietos dimensijų rinkinys yra nustatytas.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 327bb259cc108f1fad068c847441229dcaee7ff1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859233"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis neprivalomas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip suplanuota prekė, kurios padengimo vietos dimensijų rinkinys yra nustatytas.

Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.

-   Vietos dimensija yra nustatoma kaip privaloma ir turi būti įvesta vykdant poreikio operaciją.
-   Sandėlio dimensija nėra nustatyta kaip privaloma. Sandėlis gali būti žinomas, bet nenaudojamas bendrojo planavimo skaičiavimo metu.
-   Teritorijos dimensija yra nustatyta padengimo planavimui.
-   Sandėlio dimensija nėra nustatyta padengimo planavimui. Todėl tiekimas ir poreikis sujungiami pagal teritoriją ir galbūt kitas suplanuotas padengimo dimensijas.

Toliau pateiktame grafikos objekte iliustruojama, kaip vyksta bendrasis planavimas. Parametrai, rodomi grafikos duomenyse, ir jų vietos yra tokios:
-   Prekės padengimas yra apibrėžiamas prekei. Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**. Pasirinkite prekę ir tada spustelėkite **Planuoti &gt; Prekių padengimas**.
-   Papildymo ryšiai apibrėžiami sandėliui. Spustelėkite **Atsargų valdymas &gt; Sąranka &gt; Atsargų paskirstymas &gt; Sandėliai**. **Bendrojo planavimo** skirtuke žr. laukų grupę **Pagrindinis sandėlis**.
-   Nustatytas numatytasis užsakymo tipas yra Gamybos, Pirkimo užsakymas arba „kanban“. Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**. Pasirinkite prekę ir tada spustelėkite **Planuoti &gt; Numatytosios užsakymo nuostatos**. Formoje **Numatytieji užsakymo parametrai** rasite lauką **Numatytasis užsakymo tipas**.

![Teritorijos padengimo poreikis, sandėlis neprivalomas.](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>Papildomi ištekliai

[Bendrojo planavimo ir kelių teritorijų funkcijos apžvalga](master-plan-multisite-functionality.md)

[Bendrasis vietos ir sandėlio padengimo planas, sandėlis privalomas](master-plan-site-coverage-warehouse-mandatory.md)

[Bendrasis vietos padengimo, sandėlis privalomas](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Bendrasis vietos padengimo planavimas, sandėlis neprivalomas](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[KS versijos nustatymas](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]