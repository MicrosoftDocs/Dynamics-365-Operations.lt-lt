---
title: "Bendrojo planavimo svetainė aprėptį, sandėlyje nėra privaloma"
description: "Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorijos dimensija nustatyta padengimui."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 28607f0fc8db99c9fc8e96b4514763b8cf589dd8
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Bendrojo planavimo svetainė aprėptį, sandėlyje nėra privaloma

Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorijos dimensija nustatyta padengimui.

Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.

-   Vietos dimensija yra nustatoma kaip privaloma ir turi būti įvesta vykdant poreikio operaciją.
-   Sandėlio dimensija nėra nustatyta kaip privaloma. Sandėlis gali būti žinomas, bet nenaudojamas bendrojo planavimo skaičiavimo metu.
-   Teritorijos dimensija yra nustatyta padengimo planavimui.
-   Sandėlio dimensija nėra nustatyta padengimo planavimui. Todėl tiekimas ir poreikis sujungiami pagal teritoriją ir galbūt kitas suplanuotas padengimo dimensijas.

Toliau pateiktame grafikos objekte iliustruojama, kaip vyksta bendrasis planavimas. Parametrai, rodomi grafikos duomenyse, ir jų vietos yra tokios:
-   Prekės padengimas yra apibrėžiamas prekei. Spustelėkite **produkto informacijos valdymo &gt;gaminiai&gt; išleisti produktai**. Pasirinkite elementą, o tada spustelėkite **planas &gt;prekės padengimas**.
-   Papildymo ryšiai apibrėžiami sandėliui. Spustelėkite **atsargų valdymo &gt;nustatymo &gt;atsargų paskirstymas &gt;sandėlių**. **Bendrojo planavimo** skirtuke žr. laukų grupę **Pagrindinis sandėlis**.
-   Nustatytas numatytasis užsakymo tipas yra Gamybos, Pirkimo užsakymas arba „kanban“. Spustelėkite **produkto informacijos valdymo &gt;gaminiai&gt; išleisti produktai**. Pasirinkite elementą, o tada spustelėkite **planas &gt;numatytieji parametrai tvarka**. Formoje **Numatytieji užsakymo parametrai** rasite lauką **Numatytasis užsakymo tipas**.

![Teritorijos padengimo poreikis, sandėlis neprivalomas](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="see-also"></a>Taip pat žiūrėkite
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis privalomas](master-plan-site-coverage-warehouse-mandatory.md)

[Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis neprivalomas](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis privalomas](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Bendrojo planavimo - kaip nustatoma KS versijos](master-plan-bom-version-determined.md)


