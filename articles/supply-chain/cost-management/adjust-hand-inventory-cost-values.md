---
title: Turimų atsargų išlaidų verčių koregavimas
description: Naudokite puslapį „Turimų atsargų koregavimas“, kad koreguotumėte turimų atsargų kiekių savikainos vertę po atsargų uždarymo proceso.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62122454b2fe0f6a9f04f073057156603e66bb22
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673304"
---
# <a name="adjust-on-hand-inventory-cost-values"></a>Turimų atsargų išlaidų verčių koregavimas

[!include [banner](../includes/banner.md)]

Naudokite puslapį „Turimų atsargų koregavimas“, kad koreguotumėte turimų atsargų kiekių savikainos vertę po atsargų uždarymo proceso.

Galite naudoti puslapį **Turimų atsargų koregavimas**, kad koreguotumėte turimų atsargų kiekių savikainos vertę po atsargų uždarymo proceso. **Pastaba:** norėdami atidaryti puslapį **Turimų atsargų koregavimas** puslapyje **Uždarymas ir koregavimas** pasirinkite užbaigto atsargų uždarymo proceso įrašą ir spustelėkite **Koregavimas** &gt; **Turimos atsargos**. **Pavyzdys:** vasario mėnesį atliktos tokios operacijos:

-   Vasario 1 d.: 2 vienetų, kurių savikaina 10,00 USD, finansinis gavimas į atsargas
-   Vasario 5 d.: 1 vieneto, kurio kaina 13,00 USD, finansinis gavimas į atsargas
-   Vasario 19 d.: 1 vieneto, kurio einamoji vidurkio savikaina 11 USD, finansinis išdavimas iš atsargų

Ši prekė buvo nustatyta su „pirmasis į, pirmasis iš“ (FIFO) atsargų modeliu, o atsargų uždarymas buvo atliktas vasario 28 d. 11,00 USD vertės finansinio išdavimo operacija bus sudengta su finansiniu vasario mėn. 1 d. gavimu ir bus atliktas 1,00 USD vertės koregavimas. Tada toliau pateikiamuose atsargų gavimuose bus atvirų atsargų kiekių:

-   Vasario 1 d.: 1 vienetas, kurio kaina 10,00 USD
-   Vasario 5 d.: 1 vienetas, kurio kaina 13,00 USD

Norėdami nustatyti šių dviejų prekių kainą į 15,00 USD, naudokite turimą koregavimo pasirinktį, kad pakoreguotumėte po paskutinio atsargų uždarymo laikotarpio turimus atvirus kiekius. **Pastaba:** turimo kiekio koregavimo operacijos registravimo data bus paskutinio atsargų uždarymo data. Šios datos modifikuoti negalima.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]