---
title: "Išlaidų valdymo pagrindinis puslapis"
description: "Išlaidų valdymas leidžia atlikti žaliavų, pusgaminių, pagamintų prekių ir nebaigtos gamybos turto vertinimą ir apskaitą."
author: AndersGirke
manager: AnnBe
ms.date: 02/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cab2f165a70e5ce8f09f0391282e055e51afb225
ms.openlocfilehash: b1513e5a7cb3a19fd3743a5aac8efd211aa02ce8
ms.contentlocale: lt-lt
ms.lasthandoff: 02/21/2018

---

# <a name="cost-management-home-page"></a>Išlaidų valdymo pagrindinis puslapis

[!INCLUDE [banner](../includes/banner.md)]

[Išlaidų valdymas (vaizdo įrašas)](https://www.youtube.com/watch?v=vXzlC-mOBcg&feature=youtu.be) leidžia atlikti žaliavų, pusgaminių, pagamintų prekių ir nebaigtos gamybos turto vertinimą ir apskaitą. Šio proceso metu apibrėžiama, valdoma ir teikiamos ataskaitos apie [Atsargų apskaitą](cost-object.md) ir [Gamybos apskaitą](bom-calculations.md).

Išlaidų strategijas galite nustatyti šiose srityse: 
-  [Iš anksto nustatyta savikaina](costing-versions.md)
-  [Atsargų apskaita](cost-object.md)
-  [Gamybos apskaita](bom-calculations.md)
-  [Netiesioginių išlaidų apskaita](costing-sheets.md)
-  [DK integracija](production-order-cost-analysis.md)

Pavyzdžiui, galite nurodyti, kuriuos atsargų vertinimo metodus (pvz., [FIFO](fifo-physical-value-marking.md), [Svertinio vidurkio](weighted-average-physical-value-marking.md), [Standartinių išlaidų](prerequisites-standard-costs.md) ar [Slenkančio vidurkio](moving-average.md)) norite taikyti produktams [Prekių modelių grupėje](../inventory/reserve-inventory-quantities.md) atlikdami atsargų apskaitą.

Atsargų apskaitą ir gamybos apskaitą galite atverti iš darbo sričių **Išlaidų administravimas** ir **Išlaidų analizė**. Šiose darbo srityse pateikta išsami dabartinės būsenos, pagrindinių efektyvumo indikatorių (KPI) ir nuokrypių nustatymo apžvalga. 

Gamybos apskaita leidžia atlikti [Užduoties užsakymo įkainojimą](production-order-cost-analysis.md) gamybos užsakymuose ir paketiniuose užsakymuose, o taip pat ir „lean manufacturing“ [Įkainojimą atvirkštine tvarka](backflush-costing.md).

[Išlaidų valdymo „Power BI“ turinys](../../dev-itpro/analytics/cost-management-content-pack.md) suteikia vadovams įžvalgų apie atsargas ir nebaigtos gamybos (NG) atsargas bei tai, kaip jose veikia išlaidų srautas. Informaciją taip pat galima naudoti kaip išsamų finansinės ataskaitos papildinį.

### <a name="additional-resources"></a>Papildomi ištekliai

#### <a name="whats-new-and-in-development"></a>Kas nauja ir kuriama

Norėdami pamatyti naujas išleistas funkcijas ir kuriamas naujas funkcijas, eikite į [„Microsoft Dynamics 365“ plano](https://roadmap.dynamics.com/) svetainę. 

#### <a name="white-paper"></a>Techninė dokumentacija
[KS skaičiavime naudojant įkainojimo lapą](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/white-papers/365operationsbomcalsheet) aprašoma, kaip nustatyti įkainojimo lapą su medžiagomis ir gamyba, ir kaip ši sąranka veikia KS skaičiavimo rezultatus. Siekiant geriau paaiškinti šias temas, ten pateikiami konkretūs scenarijai ir duomenys, kurie rodo įvairių parametrų ir konfigūracijų poveikį. Nesitikime, kad atliksite visus šiuos scenarijus, nes šis dokumentas nesuteikia pakankamai informacijos jiems sukonfigūruoti. Nepaisant to, jei turite bazinių žinių, galite pabandyti atlikti žemiau nurodytas užduotis tokia seka, kokia jos pateikiamos. Panaudokite žinias, kurias įgijote skaitydami šį dokumentą, KS skaičiavimo analizei atlikti. 

-  [Kurti galutinį produktą](tasks/create-finished-product-2016-02.md)
-  [Kurti pusiau baigtą produktą](tasks/create-semi-finished-product-2016-02.md)
-  [Kurti žaliavas](tasks/create-raw-materials-2016-02.md)
-  [Kurti KS](tasks/create-boms-2016-02.md)
-  [Kurti maršrutus](tasks/create-routes-2016-02.md)
-  [KS skaičiavimas naudojant vieno lygio struktūrą](tasks/calculate-bom-single-level-structure-2016-02.md)
-  [KS skaičiavimas naudojant kelių lygių struktūrą](tasks/calculate-bom-multilevel-structure-2016-02.md)


#### <a name="blogs"></a>Tinklaraščiai
Nuomonių, naujienų ir kitos informacijos apie išlaidų valdymą galima rasti [„Dynamics AX‟ gamybos tyrimų ir plėtros komandos tinklaraštyje](https://blogs.msdn.microsoft.com/axmfg) ir [Tiekimo grandinės valdymo sprendime „Dynamics AX‟ pagrindinės tyrimų ir plėtros tinklaraštyje](https://blogs.msdn.microsoft.com/dynamicsaxscm). Kai kurie iš šių įrašų parašyti ankstesnei išlaidų valdymo versijai, tačiau dabartinėje versijoje galioja tie patys principai, o procedūros taip pat yra panašios.

#### <a name="task-guides"></a>Užduočių vedliai
Papildoma pagalba prieinama kaip užduočių vedliai programoje „Finance and Operations‟. Norėdami pasiekti užduočių vedlius, bet kuriame puslapyje spustelėkite mygtuką Žinynas.


