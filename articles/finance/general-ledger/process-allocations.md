---
title: Paskirstymų apdorojimas
description: Šioje temoje pateikiama informacija apie paskirstymus, jų apdorojimo parinktis „Microsoft Dynamics 365 Finance“ ir kaip jie gali būti naudojami planuojant biudžetą. Paskirstymai naudojami sumoms paskirstyti tarp kelių DK sąskaitų derinių. Jie padeda užtikrinti, kad išlaidos ar įplaukos paskiriamos tinkamam apskaitos objektui.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b79282abd0edf86f1a9f39fd869cf1fab28b9a4
ms.sourcegitcommit: 4f8465729d7ae0bf5150a2785a6140c984c7030e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/31/2021
ms.locfileid: "7726997"
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
