---
title: "KS versiją sprogimas"
description: "Šiame straipsnyje paaiškinama, bendrojo planavimo scenarijų, kuris apima sprogimo komplektavimo specifikacijos (KS) versija."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 6461a07f8c8f02f584e5ef70b21ebaf04f29b57b
ms.lasthandoff: 03/31/2017


---

# <a name="explosion-of-a-bom-version"></a>KS versiją sprogimas

Šiame straipsnyje paaiškinama, bendrojo planavimo scenarijų, kuris apima sprogimo komplektavimo specifikacijos (KS) versija.

Komplektavimo specifikacijos (KS) versijos poreikio išskleidimas sukuria kiekvienos KS eilutės poreikį tam tikroje teritorijoje ir, galbūt, tam tikrame sandėlyje. Teritorijai būdingoje KS galima nustatyti konkretų kiekvienos KS eilutės sandėlį. Taip pat kiekvienos KS eilutės prekės dimensijos parametrai nurodo, ar sandėlis būtinas. Gautas kiekvienos KS eilutės prekės poreikis savo ruožtu tampa papildomo poreikio išskleidimo pradžios tašku. Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.

-   Teritorijos dimensija yra privaloma ir turi būti įvesta poreikio operacijoje.
-   Teritorijos dimensija yra nuosekli. Todėl teritorija žemesnio lygio poreikiui yra ta pati, kaip pradinio poreikio operacijos teritorija.

Tolesniame paveikslėlyje parodyta, kaip vyksta bendrojo planavimo poreikio išskleidimas. ![Poreikio išplėtimas naudojantis KS versija](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Bendrojo planavimo - kaip nustatoma KS versijos](master-plan-bom-version-determined.md)

[Master planning and multisite functionality](master-plan-multisite-functionality.md)


