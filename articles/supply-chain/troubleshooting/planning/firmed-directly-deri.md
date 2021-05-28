---
title: Tiesiogiai išvesti patvirtinti užsakymai yra apdorojami peržiūros darbo eigos
description: Tiesiogiai išvesti patvirtinti užsakymai yra apdorojami peržiūros darbo eigos, kurios būsena yra peržiūrima.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026753"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Tiesiogiai išvesti patvirtinti užsakymai yra apdorojami peržiūros darbo eigos

KB numeris: 4612450

## <a name="symptoms"></a>Požymiai

Tiesiogiai išvesti patvirtinti užsakymai yra apdorojami peržiūros darbo eigos, kurios būsena yra *peržiūrima*.

## <a name="resolution"></a>Skiriamoji geba

Kai keitimo sekimas yra įjungtas, *Peržiūrima* būsena yra priskirta pasirašytiems išvestiniams užsakymams (papildomos sutarties pirkimo užsakymams). Todėl, jei pirkimo užsakymas išvestas (subrangos pirkimo užsakymas), jis pateikiamas tik darbo eigai. Jei pirkimo užsakymas yra patvirtintas suplanuotas pirkimo užsakymas, jis automatiškai patvirtintas siekiant užtikrinti, kad planavimo variklis nekuria naujų suplanuotų užsakymų, kol pirkimo užsakymo būsena dar yra *Juodraštis*.
