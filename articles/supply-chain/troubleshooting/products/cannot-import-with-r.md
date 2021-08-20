---
title: Negalite importuoti prekės naudodami objektą Išleisti produktai V2
description: Negalite importuoti prekės naudodami objektą Išleisti produktai V2.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: efd773313f89784d8fca6b37d867e204cb2d06ab29694a19cbec7eed107a8019
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764697"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Negalite importuoti prekės naudodami objektą Išleisti produktai V2

KB numeris: 4611825

## <a name="symptoms"></a>Požymiai

Kai bandote importuoti prekę naudodami objektą *Išleistų produktų V2* ojekte, gaunate klaidos pranešimą, kuris yra panašus į tokį pavyzdį:

> Negalima sukurti įrašo prekėse – sekimo dimensijų grupėse (EcoResTrackingDimensionGroupItem). Prekės numeris: 2040663, Paketas. Toks įrašas jau yra.

## <a name="resolution"></a>Skiriamoji geba

Norėdami importuoti naujus išleistus produktus, naudokite objektą *Išleisto produkto kūrimo V2* o ne *išleistų produktų V2* objektą.
