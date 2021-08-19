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
ms.openlocfilehash: d20f1c1d6e8fc83dd996b04bf0321a41f7b39290f306d1ac9f4fcd17514832e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721180"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>Tiesiogiai išvesti patvirtinti užsakymai yra apdorojami peržiūros darbo eigos

KB numeris: 4612450

## <a name="symptoms"></a>Požymiai

Tiesiogiai išvesti patvirtinti užsakymai yra apdorojami peržiūros darbo eigos, kurios būsena yra *peržiūrima*.

## <a name="resolution"></a>Skiriamoji geba

Kai keitimo sekimas yra įjungtas, *Peržiūrima* būsena yra priskirta pasirašytiems išvestiniams užsakymams (papildomos sutarties pirkimo užsakymams). Todėl, jei pirkimo užsakymas išvestas (subrangos pirkimo užsakymas), jis pateikiamas tik darbo eigai. Jei pirkimo užsakymas yra patvirtintas suplanuotas pirkimo užsakymas, jis automatiškai patvirtintas siekiant užtikrinti, kad planavimo variklis nekuria naujų suplanuotų užsakymų, kol pirkimo užsakymo būsena dar yra *Juodraštis*.
