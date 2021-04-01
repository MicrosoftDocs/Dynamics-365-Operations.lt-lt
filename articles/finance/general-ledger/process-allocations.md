---
title: Apdoroti paskirstymus
description: Šiame straipsnyje pateikiama informacija apie paskirstymus, jų apdorojimo parinktis „Microsoft“ „Dynamics 365 Finance“ ir kaip jie gali būti naudojami planuojant biudžetą. Paskirstymai naudojami sumoms paskirstyti tarp kelių DK sąskaitų derinių. Jie padeda užtikrinti, kad išlaidos ar įplaukos paskiriamos tinkamam apskaitos objektui.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b13496e764f907201a23f0dd6772ee22efffb250
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204983"
---
# <a name="process-allocations"></a>Paskirstymų apdorojimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie paskirstymus, jų apdorojimo parinktis ir kaip jie gali būti naudojami planuojant biudžetą. Paskirstymai naudojami sumoms paskirstyti tarp kelių DK sąskaitų derinių. Jie padeda užtikrinti, kad išlaidos ar įplaukos paskiriamos tinkamam apskaitos objektui.

Šis procesas palaiko toliau pateikiamas galimybes.

-   Rankiniu būdu paskirstykite operacijų sumas apskaitos paskirstymuose naudodami skaidymo veiksmą arba dokumentui pritaikydami finansinės dimensijos numatytuosius šablonus. Daugiau informacijos žr. [Apskaitos paskirstymai](../accounts-payable/accounting-distributions.md).
-   Automatiškai paskirstykite operacijų sumas pagal paskirstymo sąlygas, nurodytas atskiroje pagrindinėje sąskaitoje. Paskirstymo sąskaitos įrašai kiekvienam žurnalui bus generuojami pagal procentinę dalį ir paskirties DK sąskaitą, kai apskaitos įrašas atitiks kriterijus, apibrėžtus kaip pirminė DK sąskaita. Dėl platesnės informacijos, žr. [Pagrindinės paskyros paskirstymo sąlygas](../general-ledger/main-account-allocation-terms.md)
-   Automatiškai paskirstykite DK balansus arba fiksuotas sumas pagal DK paskirstymo taisykles. DK paskirstymo taisyklės apdorojamos periodiškai, naudojant paskirstymo žurnalus. Norėdami gauti daugiau informacijos, žr. [Paskirstymo taisykles](../general-ledger/ledger-allocation-rules.md).

###  <a name="allocations-in-budget-planning"></a>Biudžeto planavimo paskirstymai

DK paskirstymo taisykles galima naudoti biudžeto planams. Kai DK paskirstymo taisykles naudojate planuodami biudžetą, paskirstymo taisyklės veikia taip pat kaip veiktų DK, bet šaltinio duomenys ir paskirties duomenys gaunami iš biudžeto plano. Galite neautomatiškai pasirinkti DK paskirstymo taisykles, naudotinas biudžeto planams. Be to, galite naudoti paskirstymo grafiką, kuris veikia kaip darbo eigos proceso dalis.

> [!NOTE]
> Biudžetui planuoti negalima naudoti vidinės įmonės DK paskirstymo taisyklių.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]