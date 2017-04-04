---
title: "Bendrojo planavimo vietai ir sandėliui aprėptį, sandėlio neprivalomi."
description: "Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija ir sandėlis yra padengimo dimensijos. Sandėlio dimensija nėra privaloma."
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
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 3671024dc097c94638b1579d7cacc8447c49e97b
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>Bendrojo planavimo vietai ir sandėliui aprėptį, sandėlio neprivalomi.

Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija ir sandėlis yra padengimo dimensijos. Sandėlio dimensija nėra privaloma.

Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.

-   Vietos dimensija yra nustatoma kaip privaloma ir turi būti įvesta vykdant poreikio operaciją. Šios nuostatos modifikuoti negalima.
-   Sandėlio dimensija nėra nustatyta kaip privaloma. Sandėlis gali būti žinomas, bet nenaudojamas bendrojo planavimo skaičiavimo metu.
-   Teritorijos ir sandėlio dimensijos nustatytos padengimui planuoti. Kitos dimensijos taip pat gali būti nustatytos padengimui planuoti. Tačiau jų neveikia kelių teritorijų funkcionalumas.

Toliau pateiktame grafikos objekte iliustruojama, kaip vyksta bendrasis planavimas. Parametrai, rodomi grafikos duomenyse, ir jų vietos yra tokios:
-   Sandėlis nustatytas į Rankinis. Spustelėkite **atsargų valdymo &gt;nustatymo &gt;atsargų paskirstymas &gt;sandėlių**. **Bendrojo planavimo** „FastTab‟ žr. lauką **Rankinis**.
-   Prekės padengimas yra apibrėžiamas prekei. Spustelėkite **produkto informacijos valdymo &gt;gaminiai&gt; išleisti produktai**. Pasirinkite elementą, ir tada, ir veiksmų srityje, apie į **planas** skirtuką, spustelėkite **prekės padengimas**.
-   Papildymo ryšiai apibrėžiami sandėliui. Spustelėkite **atsargų valdymo &gt;nustatymo &gt;atsargų paskirstymas &gt;sandėlių**. **Bendrojo planavimo** „FastTab‟ žr. laukų grupę **Pagrindinis sandėlis**.
-   Nustatytas numatytasis užsakymo tipas yra Gamybos, Pirkimo užsakymas arba „kanban“. Spustelėkite **produkto informacijos valdymo &gt;gaminiai&gt; išleisti produktai**. Pasirinkite elementą, ir tada, ir veiksmų srityje, apie į **planas** skirtuką, spustelėkite **numatytieji parametrai tvarka**. Formoje **Numatytosios užsakymo nuostatos** žr. **Numatytasis užsakymo tipas**.

![Teritorijos ir sandėlio poreikis, sandėlis neprivalomas](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)

 
-



<a name="see-also"></a>Taip pat žiūrėkite
--------

[Master planning and multisite functionality](master-plan-multisite-functionality.md)

[Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis privalomas](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis privalomas](master-plan-site-coverage-warehouse-mandatory.md)

[Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis neprivalomas](master-plan-site-coverage-warehouse-not-mandatory.md)

[Bendrasis planavimas – kaip nustatoma KS versija](master-plan-bom-version-determined.md)


