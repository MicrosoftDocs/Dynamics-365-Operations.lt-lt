---
title: Naudojant prekių grąžinimo grupes, klientų grąžinimų kaupti nepavyko
description: Kai kliento grąžinimo sutartis naudojate kartu su prekių grąžinimo grupėmis, grąžinimai apskaičiuojami, bet kaupimo nepavyksta.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026735"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Naudojant prekių grąžinimo grupes, klientų grąžinimų kaupti nepavyko

KB numeris: 4611372

## <a name="symptoms"></a>Požymiai

Kai kliento grąžinimo sutartis naudojate kartu su ( *kiekio* tipu) ir prekių grąžinimo grupėmis, grąžinimai apskaičiuojami, bet kaupimo nepavyksta.

## <a name="resolution"></a>Skiriamoji geba

Sistema veikia kaip sukurta. Prekių grupių grupė tik tos prekės, kurių ribinės vertės sąlyga tokia pati. Grąžinimo sąlyga (ribinė vertė) nustatoma pagal kiekvienos prekės sumą, o ne pagal kiekvienos prekių grupės prekės kaupimo sumą.
