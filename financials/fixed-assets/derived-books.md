---
title: "Išvestinės knygos"
description: "Šiame straipsnyje apžvelgiamos išvestinių knygų funkcijos."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 39035fe2e22987305b2ec6731e5c3b3390043a2a
ms.contentlocale: lt-lt
ms.lasthandoff: 04/25/2017


---

# <a name="derived-books"></a>Išvestinės knygos

[!include[banner](../includes/banner.md)]


Šiame straipsnyje apžvelgiamos išvestinių knygų funkcijos.

Išvestinės knygos suteikia galimybę paprasčiau registruoti reguliariais intervalais planuojamas ilgalaikio turto knygų operacijas.  Knygą reikia pasirinkti kaip pagrindinę knygą. Paprastai tai yra knyga, naudojama apskaitos nusidėvėjimui. Tada prie jos pridedamos kitos knygos, kurios nustatytos operacijas registruoti tokiais pačiais intervalais kaip ir pagrindinė knyga. Mokestinio nusidėvėjimo knygos dažnai nustatomos kaip išvestinės knygos. 

Dažniausios operacijos, kurios nustatomos registruoti išvestinėse knygose, yra įsigijimai, įsigijimo koregavimai ir likvidavimai. 

## <a name="example"></a>Pavyzdys

Knygos B ir C nustatomos kaip išvestinės tipo Įsigijimo operacija knygos A knygos. Knygoje A įveskite turto 123, kurio vertė 1 500,00, įsigijimo operaciją. 

Užregistravus operaciją, generuojama ir registruojama knygos B turto 123 ir knygos C turto 123 įsigijimo operacija, kurios 1 500,00. Kai ruošiate pagrindinės knygos operacijas registruoti ilgalaikio turto žurnale, taip pat galite peržiūrėti ir modifikuoti išvestinių knygų operacijas. Jei pagrindinės knygos operacijas ruošiate kitame žurnale, išvestinių nusidėvėjimo knygų operacijos nerodomos. Tačiau, kai registruojate pagrindinės knygos operacijas, jos registruojamos atitinkamose sąskaitose ir registravimo sluoksniuose.

> [!NOTE]                                                                                                                               
> Knygos, nustatytos registruoti operacijas kitokiais intervalais negu pagrindinė knyga, turi būti susietos su ilgalaikiu turtu kaip atskiros knygos, o ne kaip išvestinės knygos.  

Daugiau informacijos žr. [Registravimas naudojant išvestines knygas](post-derived-value-models.md).




