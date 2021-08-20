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
ms.openlocfilehash: fc3381dab77cf80c0fd65f3bc27c11b814e72368631bd0e2145aac0be4f4fba4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760375"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>Naudojant prekių grąžinimo grupes, klientų grąžinimų kaupti nepavyko

KB numeris: 4611372

## <a name="symptoms"></a>Požymiai

Kai kliento grąžinimo sutartis naudojate kartu su ( *kiekio* tipu) ir prekių grąžinimo grupėmis, grąžinimai apskaičiuojami, bet kaupimo nepavyksta.

## <a name="resolution"></a>Skiriamoji geba

Sistema veikia kaip sukurta. Prekių grupių grupė tik tos prekės, kurių ribinės vertės sąlyga tokia pati. Grąžinimo sąlyga (ribinė vertė) nustatoma pagal kiekvienos prekės sumą, o ne pagal kiekvienos prekių grupės prekės kaupimo sumą.
