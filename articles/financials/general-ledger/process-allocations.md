---
title: Apdoroti paskirstymus
description: "Šiame straipsnyje pateikiama informacija apie paskirstymus, jų apdorojimo parinktis „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ ir kaip jie gali būti naudojami planuojant biudžetą. Paskirstymai naudojami sumoms paskirstyti tarp kelių DK sąskaitų derinių. Jie padeda užtikrinti, kad išlaidos ar įplaukos paskiriamos tinkamą apskaitos objektui."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8859359f70132e9116e6a2d534a0f5f1d0bfeb80
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="process-allocations"></a>Apdoroti paskirstymus

[!include[banner](../includes/banner.md)]


Šiame straipsnyje pateikiama informacija apie paskirstymus, jų apdorojimo parinktis „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ ir kaip jie gali būti naudojami planuojant biudžetą. Paskirstymai naudojami sumoms paskirstyti tarp kelių DK sąskaitų derinių. Jie padeda užtikrinti, kad išlaidos ar įplaukos paskiriamos tinkamą apskaitos objektui.

„Microsoft Dynamics 365 for Finance and Operations“ pateikiamos tokios galimybės palaikyti šį procesą:

-   Rankiniu būdu paskirstykite operacijų sumas apskaitos paskirstymuose naudodami skaidymo veiksmą arba dokumentui pritaikydami finansinės dimensijos numatytuosius šablonus. Daugiau informacijos rasite [Apskaitos paskirstymai.](../accounts-payable/accounting-distributions.md)
-   Automatiškai paskirstykite operacijų sumas pagal paskirstymo sąlygas, nurodytas atskiroje pagrindinėje sąskaitoje. Paskirstymo sąskaitos įrašai kiekvienam žurnalui bus generuojami pagal procentinę dalį ir paskirties DK sąskaitą, kai apskaitos įrašas atitiks kriterijus, apibrėžtus kaip pirminė DK sąskaita.
-   Automatiškai paskirstykite DK balansus arba fiksuotas sumas pagal DK paskirstymo taisykles. DK paskirstymo taisyklės apdorojamos periodiškai, naudojant paskirstymo žurnalus. 

###  <a name="allocations-in-budget-planning"></a>Biudžeto planavimo paskirstymai

DK paskirstymo taisykles galima naudoti biudžeto planams. Kai DK paskirstymo taisykles naudojate planuodami biudžetą, paskirstymo taisyklės veikia taip pat kaip veiktų DK, bet šaltinio duomenys ir paskirties duomenys gaunami iš biudžeto plano. Galite neautomatiškai pasirinkti DK paskirstymo taisykles, naudotinas biudžeto planams. Be to, galite naudoti paskirstymo grafiką, kuris veikia kaip darbo eigos proceso dalis.

> [!NOTE]
> Biudžetui planuoti negalima naudoti vidinės įmonės DK paskirstymo taisyklių.






