---
title: "Bendrasis planavimas – teritorijos padengimo poreikis, privalomas sandėlis"
description: "Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija yra padengimo dimensija. Sandėlis yra privaloma dimensija."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 39f105bd1c6a6da4b73ae2a9c5657b15c6794ec0
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>Bendrasis planavimas – teritorijos padengimo poreikis, privalomas sandėlis

[!include [banner](../includes/banner.md)]

Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorija yra padengimo dimensija. Sandėlis yra privaloma dimensija.

Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.

-   Vietos dimensija yra nustatoma kaip privaloma ir turi būti įvesta vykdant poreikio operaciją. Šios nuostatos modifikuoti negalima.
-   Sandėlio dimensija yra nustatoma kaip privaloma ir turi būti įvesta poreikio operacijos metu.
-   Teritorijos dimensija yra nustatyta padengimo planavimui. Kitos dimensijos taip pat gali būti nustatytos padengimo planavimui. Tačiau jų neveikia kelių teritorijų funkcionalumas.
-   Sandėlio dimensija nėra nustatyta padengimo planavimui. Todėl tiekimas ir poreikis sujungiami pagal teritoriją ir galbūt kitas suplanuotas padengimo dimensijas.

Toliau pateiktame grafikos objekte iliustruojama, kaip vyksta bendrasis planavimas. Parametrai, rodomi grafikos duomenyse, ir jų vietos yra tokios:
-   Prekės padengimas yra apibrėžiamas prekei. Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**. Pasirinkite prekę ir tada spustelėkite **Planuoti &gt; Prekių padengimas**.
-   Papildymo ryšiai apibrėžiami sandėliui. Spustelėkite **Atsargų valdymas &gt; Sąranka &gt; Atsargų paskirstymas &gt; Sandėliai**. **Bendrojo planavimo** skirtuke žr. laukų grupę **Pagrindinis sandėlis**.
-   Nustatytas numatytasis užsakymo tipas yra Gamybos, Pirkimo užsakymas arba „kanban“. Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**. Pasirinkite prekę ir tada spustelėkite **Planuoti &gt; Numatytosios užsakymo nuostatos**. Formoje **Numatytosios užsakymo nuostatos** žr. **Numatytasis užsakymo tipas**.

![Teritorijos padengimo poreikis, sandėlis privalomas](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a>Papildomi ištekliai
--------

[Bendrasis planavimas ir kelių teritorijų funkcija](master-plan-multisite-functionality.md)

[Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis privalomas](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis privalomas](master-plan-site-coverage-warehouse-mandatory.md)

[Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis neprivalomas](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Bendrasis planavimas – kaip nustatoma KS versija](master-plan-bom-version-determined.md)




