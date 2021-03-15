---
title: Išvestinės knygos
description: Šiame straipsnyje apžvelgiamos išvestinių knygų funkcijos.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 911bb476a696facfad9dec177261821724d2bfe0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994920"
---
# <a name="derived-books"></a>Išvestinės knygos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje apžvelgiamos išvestinių knygų funkcijos.

Išvestinės knygos suteikia galimybę paprasčiau registruoti reguliariais intervalais planuojamas ilgalaikio turto knygų operacijas.  Knygą reikia pasirinkti kaip pagrindinę knygą. Paprastai tai yra knyga, naudojama apskaitos nusidėvėjimui. Tada prie jos pridedamos kitos knygos, kurios nustatytos operacijas registruoti tokiais pačiais intervalais kaip ir pagrindinė knyga. Mokestinio nusidėvėjimo knygos dažnai nustatomos kaip išvestinės knygos. 

Dažniausios operacijos, kurios nustatomos registruoti išvestinėse knygose, yra įsigijimai, įsigijimo koregavimai ir likvidavimai. 

## <a name="example"></a>Pavyzdys

Knygos B ir C nustatomos kaip išvestinės tipo Įsigijimo operacija knygos A knygos. Knygoje A įveskite turto 123, kurio vertė 1 500,00, įsigijimo operaciją. 

Užregistravus operaciją, generuojama ir registruojama knygos B turto 123 ir knygos C turto 123 įsigijimo operacija, kurios 1 500,00. Kai ruošiate pagrindinės knygos operacijas registruoti ilgalaikio turto žurnale, taip pat galite peržiūrėti ir modifikuoti išvestinių knygų operacijas. Jei pagrindinės knygos operacijas ruošiate kitame žurnale, išvestinių nusidėvėjimo knygų operacijos nerodomos. Tačiau, kai registruojate pagrindinės knygos operacijas, jos registruojamos atitinkamose sąskaitose ir registravimo sluoksniuose.

> [!NOTE]                                                                                                                               
> Knygos, nustatytos registruoti operacijas kitokiais intervalais negu pagrindinė knyga, turi būti susietos su ilgalaikiu turtu kaip atskiros knygos, o ne kaip išvestinės knygos.  

Daugiau informacijos rasite [Registravimas naudojant išvestines knygas](post-derived-value-models.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]