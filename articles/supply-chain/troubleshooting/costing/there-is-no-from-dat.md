---
title: Prekių kainų puslapio skirtuke Aktyvios kainos nėra vertės Nuo datos
description: Prekių kainų puslapio skirtuke Aktyvios kainos nėra vertės Nuo datos.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026760"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a>Prekių kainų puslapio skirtuke Aktyvios kainos nėra vertės Nuo datos

KB numeris: 4613548

## <a name="symptoms"></a>Požymiai

Nėra jokios **Nuo datos** vertės **Aktyvios kainos** skirtuke **Prekių kaina** puslapyje.

## <a name="resolution"></a>Skiriamoji geba

Datos **Nuo vertės** (galiojimo data), kuri nustatyta laukiančią kainą, nepervesta į aktyvią kainą.

Kai pirmą kartą įvedamas prekės išlaidų įrašas, jo būsena yra *Laukiantis* ir jis turi numatomą įsigaliojimo datą. Kai prekės išlaidų įrašą suaktyvinate, būsena atnaujinama į *Aktyvus*, o įsigaliojimo data atnaujinama į aktyvavimo datą. Todėl aktyvios kainos aktyvinimo data visada yra faktinė aktyvinimo data.

Daugiau informacijos rasite [Kaštų versijos apžvalga](../../cost-management/costing-versions.md).
