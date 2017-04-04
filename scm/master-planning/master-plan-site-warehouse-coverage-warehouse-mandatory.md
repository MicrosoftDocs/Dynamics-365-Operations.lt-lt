---
title: "Bendrojo planavimo vietai ir sandėliui aprėptį, sandėlio privalomas"
description: "Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija ir sandėlis yra padengimo dimensijos. Sandėlio dimensija privaloma."
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
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: a0931d88f84544160803e42466575c02f47588a4
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>Bendrojo planavimo vietai ir sandėliui aprėptį, sandėlio privalomas

Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija ir sandėlis yra padengimo dimensijos. Sandėlio dimensija privaloma.

Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.

-   Vietos dimensija yra nustatoma kaip privaloma ir turi būti įvesta vykdant poreikio operaciją.
-   Sandėlio dimensija yra nustatoma kaip privaloma ir turi būti įvesta poreikio operacijos metu.
-   Teritorijos ir sandėlio dimensijos nustatytos padengimui planuoti. Kitos dimensijos taip pat gali būti nustatytos padengimui planuoti. Tačiau jų neveikia kelių teritorijų funkcionalumas.

Toliau pateiktame grafikos objekte iliustruojama, kaip vyksta bendrasis planavimas. Parametrai, rodomi grafikos duomenyse, ir jų vietos yra tokios:
-   Sandėlis nustatytas į **Rankinis**. Spustelėkite **atsargų valdymo &gt;nustatymo &gt;atsargų paskirstymas &gt;sandėlių**. **Bendrojo planavimo** „FastTab‟ žr. lauką **Rankinis**.
-   Prekės padengimas yra apibrėžiamas prekei. Spustelėkite **produkto informacijos valdymo &gt;gaminiai&gt; išleisti produktai**. Pasirinkite elementą, ir tada, ir veiksmų srityje, apie į **planas** skirtuką, spustelėkite **prekės padengimas**.
-   Papildymo ryšiai apibrėžiami sandėliui. Spustelėkite **atsargų valdymo &gt;nustatymo &gt;atsargų paskirstymas &gt;sandėlių**. **Bendrojo planavimo** „FastTab‟ žr. laukų grupę **Pagrindinis sandėlis**.
-   Nustatytas numatytasis užsakymo tipas yra Gamybos, Pirkimo užsakymas arba „kanban“. Spustelėkite **produkto informacijos valdymo &gt;gaminiai&gt; išleisti produktai**. Pasirinkite elementą, ir tada, ir veiksmų srityje, apie į **planas** skirtuką, spustelėkite **numatytieji parametrai tvarka**. Formoje **Numatytosios užsakymo nuostatos** žr. **Numatytasis užsakymo tipas**.

![Poreikio teritorija ir sandėlio padengimas, sandėlis privalomas](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="see-also"></a>Taip pat žiūrėkite
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis privalomas](master-plan-site-coverage-warehouse-mandatory.md)

[Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis neprivalomas](master-plan-site-coverage-warehouse-not-mandatory.md)

[Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis neprivalomas](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Bendrasis planavimas – kaip nustatoma KS versija](master-plan-bom-version-determined.md)


