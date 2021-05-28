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
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026737"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Negalite importuoti prekės naudodami objektą Išleisti produktai V2

KB numeris: 4611825

## <a name="symptoms"></a>Požymiai

Kai bandote importuoti prekę naudodami objektą *Išleistų produktų V2* ojekte, gaunate klaidos pranešimą, kuris yra panašus į tokį pavyzdį:

> Negalima sukurti įrašo prekėse – sekimo dimensijų grupėse (EcoResTrackingDimensionGroupItem). Prekės numeris: 2040663, Paketas. Toks įrašas jau yra.

## <a name="resolution"></a>Skiriamoji geba

Norėdami importuoti naujus išleistus produktus, naudokite objektą *Išleisto produkto kūrimo V2* o ne *išleistų produktų V2* objektą.
