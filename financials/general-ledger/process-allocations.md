---
title: Apdoroti paskirstymus
description: "Šiame straipsnyje pateikiama informacija apie asignavimus, perdirbti juos Microsoft Dynamics 365 operacijoms, ir kaip jie gali būti naudojami biudžeto planavimo funkcijos. Paskirstymai naudojami sumoms paskirstyti tarp kelių DK sąskaitų derinių. Jie padeda užtikrinti, kad išlaidos ar įplaukos paskiriamos tinkamą apskaitos objektui."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 37f4df5d0b79208a8c565bc9101ddde193a6ef5b
ms.lasthandoff: 03/31/2017


---

# <a name="process-allocations"></a>Apdoroti paskirstymus

Šiame straipsnyje pateikiama informacija apie asignavimus, perdirbti juos Microsoft Dynamics 365 operacijoms, ir kaip jie gali būti naudojami biudžeto planavimo funkcijos. Paskirstymai naudojami sumoms paskirstyti tarp kelių DK sąskaitų derinių. Jie padeda užtikrinti, kad išlaidos ar įplaukos paskiriamos tinkamą apskaitos objektui.

Microsoft Dynamics 365 operacijoms suteikia šias galimybes remti šį procesą:

-   Rankiniu būdu paskirstyti balansų perskyrimo veiksmas naudojant apskaitos paskirstymo arba taikant finansinės dimensijos numatytųjų šablonų į dokumentą. Daugiau informacijos rasite [apskaitos paskirstymo.](\accounts-payable\accounting-distributions.md)
-   Automatiškai paskirstykite operacijų sumas pagal paskirstymo sąlygas, nurodytas atskiroje pagrindinėje sąskaitoje. Paskirstymo sąskaitos įrašai kiekvienam žurnalui bus generuojami pagal procentinę dalį ir paskirties DK sąskaitą, kai apskaitos įrašas atitiks kriterijus, apibrėžtus kaip pirminė DK sąskaita.
-   Automatiškai paskirstykite DK balansus arba fiksuotas sumas pagal DK paskirstymo taisykles. DK paskirstymo taisyklės apdorojamos periodiškai, naudojant paskirstymo žurnalus. 

###  <a name="allocations-in-budget-planning"></a>Biudžeto planavimo paskirstymai

DK paskirstymo taisykles galima naudoti biudžeto planams. Kai DK paskirstymo taisykles naudojate planuodami biudžetą, paskirstymo taisyklės veikia taip pat kaip veiktų DK, bet šaltinio duomenys ir paskirties duomenys gaunami iš biudžeto plano. Galite neautomatiškai pasirinkti DK paskirstymo taisykles, naudotinas biudžeto planams. Be to, galite naudoti paskirstymo grafiką, kuris veikia kaip darbo eigos proceso dalis.

> [!NOTE]
> Biudžetui planuoti negalima naudoti vidinės įmonės DK paskirstymo taisyklių.




