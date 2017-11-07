---
title: "Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis neprivalomas"
description: "Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorijos dimensija nustatyta padengimui."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 79582e92daeaf0afb032448d36be12edd0926089
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis neprivalomas

[!include[banner](../includes/banner.md)]


Šioje temoje aprašyta, kaip planuojama prekė, kurios teritorijos dimensija nustatyta padengimui.

Į šį bendrojo planavimo scenarijų įeina toliau nurodytos sąlygos.

-   Vietos dimensija yra nustatoma kaip privaloma ir turi būti įvesta vykdant poreikio operaciją.
-   Sandėlio dimensija nėra nustatyta kaip privaloma. Sandėlis gali būti žinomas, bet nenaudojamas bendrojo planavimo skaičiavimo metu.
-   Teritorijos dimensija yra nustatyta padengimo planavimui.
-   Sandėlio dimensija nėra nustatyta padengimo planavimui. Todėl tiekimas ir poreikis sujungiami pagal teritoriją ir galbūt kitas suplanuotas padengimo dimensijas.

Toliau pateiktame grafikos objekte iliustruojama, kaip vyksta bendrasis planavimas. Parametrai, rodomi grafikos duomenyse, ir jų vietos yra tokios:
-   Prekės padengimas yra apibrėžiamas prekei. Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**. Pasirinkite prekę ir tada spustelėkite **Planuoti &gt; Prekių padengimas**.
-   Papildymo ryšiai apibrėžiami sandėliui. Spustelėkite **Atsargų valdymas &gt; Sąranka &gt; Atsargų paskirstymas &gt; Sandėliai**. **Bendrojo planavimo** skirtuke žr. laukų grupę **Pagrindinis sandėlis**.
-   Nustatytas numatytasis užsakymo tipas yra Gamybos, Pirkimo užsakymas arba „kanban“. Spustelėkite **Produkto informacijos valdymas &gt; Produktai &gt; Išleisti produktai**. Pasirinkite prekę ir tada spustelėkite **Planuoti &gt; Numatytosios užsakymo nuostatos**. Formoje **Numatytieji užsakymo parametrai** rasite lauką **Numatytasis užsakymo tipas**.

![Teritorijos padengimo poreikis, sandėlis neprivalomas](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="see-also"></a>Taip pat žiūrėkite
--------

[Bendrasis planavimas ir kelių teritorijų funkcija](master-plan-multisite-functionality.md)

[Bendrasis planavimas – teritorijos padengimo poreikis, sandėlis privalomas](master-plan-site-coverage-warehouse-mandatory.md)

[Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis neprivalomas](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Bendrasis planavimas – teritorijos ir sandėlio padengimas, sandėlis privalomas](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Bendrasis planavimas – kaip nustatoma KS versija](master-plan-bom-version-determined.md)




