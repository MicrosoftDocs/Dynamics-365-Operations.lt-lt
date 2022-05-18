---
title: Paskirstymų apdorojimas
description: Šioje temoje pateikiama informacija apie paskirstymus, Microsoft Dynamics jų apdorojimo 365 finansuose pasirinktis ir apie tai, kaip juos galima naudoti planuojant biudžetą. Paskirstymai naudojami sumoms paskirstyti tarp kelių DK sąskaitų derinių. Jie padeda užtikrinti, kad išlaidos ar įplaukos paskiriamos tinkamam apskaitos objektui.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: kfend
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d300654269ef0ad52140f160f918707397c843ad
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/06/2022
ms.locfileid: "8721960"
---
# <a name="process-allocations"></a>Paskirstymų apdorojimas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie paskirstymus, jų apdorojimo parinktis ir kaip jie gali būti naudojami planuojant biudžetą. Paskirstymai naudojami sumoms paskirstyti tarp kelių DK sąskaitų derinių. Jie padeda užtikrinti, kad išlaidos ar įplaukos paskiriamos tinkamam apskaitos objektui.

Šis procesas palaiko toliau pateikiamas galimybes.

-   Rankiniu būdu paskirstykite operacijų sumas apskaitos paskirstymuose naudodami skaidymo veiksmą arba dokumentui pritaikydami finansinės dimensijos numatytuosius šablonus. Daugiau informacijos žr. [Apskaitos paskirstymai](../accounts-payable/accounting-distributions.md).
-   Automatiškai paskirstykite operacijų sumas pagal paskirstymo sąlygas, nurodytas atskiroje pagrindinėje sąskaitoje. Paskirstymo sąskaitos įrašai kiekvienam žurnalui bus generuojami pagal procentinę dalį ir paskirties DK sąskaitą, kai apskaitos įrašas atitiks kriterijus, apibrėžtus kaip pirminė DK sąskaita. Dėl platesnės informacijos, žr. [Pagrindinės paskyros paskirstymo sąlygas](../general-ledger/main-account-allocation-terms.md)
-   Automatiškai paskirstykite DK balansus arba fiksuotas sumas pagal DK paskirstymo taisykles. DK paskirstymo taisyklės apdorojamos periodiškai, naudojant paskirstymo žurnalus. Norėdami gauti daugiau informacijos, žr. [Paskirstymo taisykles](../general-ledger/ledger-allocation-rules.md).

###  <a name="allocations-in-budget-planning"></a>Biudžeto planavimo paskirstymai

DK paskirstymo taisykles galima naudoti biudžeto planams. Kai DK paskirstymo taisykles naudojate planuodami biudžetą, paskirstymo taisyklės veikia taip pat kaip veiktų DK, bet šaltinio duomenys ir paskirties duomenys gaunami iš biudžeto plano. Galite neautomatiškai pasirinkti DK paskirstymo taisykles, naudotinas biudžeto planams. Be to, galite naudoti paskirstymo grafiką, kuris veikia kaip darbo eigos proceso dalis.

> [!NOTE]
> Biudžetui planuoti negalima naudoti vidinės įmonės DK paskirstymo taisyklių.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
