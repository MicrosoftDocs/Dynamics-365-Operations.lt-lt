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
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026751"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a>Suplanuotas pirkimo užsakymas sukuriamas, kai pirkimas yra per neigiamas dienas

KB numeris: 4614298

## <a name="symptoms"></a>Požymiai

Jei padengimo kodas yra *Min./maks.*, „Planning Optimization“ sukuria suplanuotą pirkimo užsakymą, kai pirkimas yra per neigiamas dienas.

## <a name="resolution"></a>Skiriamoji geba

„Planning Optimization“ nepalaiko neigiamų dienų. Tačiau, jis visada užtikrina, kad gamybos laiko, susijusios su dabartine data, suplanuoti užsakymai nebus planuojami. Pavyzdžiui, pirkimo vykdymo laikas yra 10 dienų, o pirkimo užsakymas turėtų gauti aštuonias dienas nuo šiandien. Šiuo atveju pirkimo užsakymas bus naudojamas kaip tiekimas pagal poreikį, kuris yra penkios dienos nuo šiandienos.

Dėl to rekomenduojame koreguoti gamybos laiką, kad jis apimtų visus (arba beveik visus) jūsų scenarijus.
