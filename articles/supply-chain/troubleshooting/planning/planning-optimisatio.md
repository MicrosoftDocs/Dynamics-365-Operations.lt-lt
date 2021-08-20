---
title: Suplanuotas pirkimo užsakymas sukuriamas, kai pirkimas yra per neigiamas dienas
description: Jei padengimo kodas yra min. / maks., „Planning Optimization“ sukuria suplanuotą pirkimo užsakymą, kai pirkimas yra per neigiamas dienas.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 94d569684a0bfa2398e98147b9b85531954f8d56748894034a048fa627230ef0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775512"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a>Suplanuotas pirkimo užsakymas sukuriamas, kai pirkimas yra per neigiamas dienas

KB numeris: 4614298

## <a name="symptoms"></a>Požymiai

Jei padengimo kodas yra *Min./maks.*, „Planning Optimization“ sukuria suplanuotą pirkimo užsakymą, kai pirkimas yra per neigiamas dienas.

## <a name="resolution"></a>Skiriamoji geba

„Planning Optimization“ nepalaiko neigiamų dienų. Tačiau, jis visada užtikrina, kad gamybos laiko, susijusios su dabartine data, suplanuoti užsakymai nebus planuojami. Pavyzdžiui, pirkimo vykdymo laikas yra 10 dienų, o pirkimo užsakymas turėtų gauti aštuonias dienas nuo šiandien. Šiuo atveju pirkimo užsakymas bus naudojamas kaip tiekimas pagal poreikį, kuris yra penkios dienos nuo šiandienos.

Dėl to rekomenduojame koreguoti gamybos laiką, kad jis apimtų visus (arba beveik visus) jūsų scenarijus.
