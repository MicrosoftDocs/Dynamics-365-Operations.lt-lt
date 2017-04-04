---
title: "Turimų atsargų išlaidų verčių koregavimas"
description: "Naudokite puslapį „Turimų atsargų koregavimas“, kad koreguotumėte turimų atsargų kiekių savikainos vertę po atsargų uždarymo proceso."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d1ef775c9783b975fd0f852dc7112506d3897605
ms.lasthandoff: 03/31/2017


---

# <a name="adjust-on-hand-inventory-cost-values"></a>Turimų atsargų išlaidų verčių koregavimas

Naudokite puslapį „Turimų atsargų koregavimas“, kad koreguotumėte turimų atsargų kiekių savikainos vertę po atsargų uždarymo proceso.

Galite naudoti puslapį **Turimų atsargų koregavimas**, kad koreguotumėte turimų atsargų kiekių savikainos vertę po atsargų uždarymo proceso. **Pastaba:** atidaryti, **turimų atsargų koregavimas** p., toliau į **uždarymo ir reguliavimo** puslapį, pažymėkite įrašą, užpildytas aprašo glaudžiai proceso ir spustelėkite **koregavimo**&gt;**turimų**. **Pavyzdys:** vasario mėnesį atliktos tokios operacijos:

-   Vasario 1 d.: 2 vienetų, kurių savaikaina 10,00 USD, finansinis gavimas į atsargas
-   Vasario 5 d.: 1 vieneto, kurio kaina 13,00 USD, finansinis gavimas į atsargas
-   Vasario 19 d.: 1 vieneto, kurio einamoji vidurkio savikaina 11 USD, finansinis išdavimas iš atsargų

Šis punktas buvo įkurta su pirmuoju, pirmas iš (FIFO) atsargų modelį, ir atsargos buvo atliekama nuo vasario 28. USD 11.00 finansų išdavimo operacija bus sudengta finansų gavimas, išleistą vasario 1 d., ir, USD 1.00 koregavimas bus atliktas. Tada toliau pateikiamuose atsargų gavimuose bus atvirų atsargų kiekių:

-   Vasario 1 d.: 1 vienetas, kurio kaina 10,00 USD
-   Vasario 5 d.: 1 vienetas, kurio kaina 13,00 USD

Norėdami nustatyti šių dviejų prekių kainą į 15,00 USD, naudokite turimą koregavimo pasirinktį, kad pakoreguotumėte po paskutinio atsargų uždarymo laikotarpio turimus atvirus kiekius. **Pastaba:** turimo kiekio koregavimo operacijos registravimo data bus paskutinio atsargų uždarymo data. Šios datos modifikuoti negalima.


