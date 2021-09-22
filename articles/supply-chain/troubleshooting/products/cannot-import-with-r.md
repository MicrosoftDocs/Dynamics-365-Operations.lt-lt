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
ms.openlocfilehash: bf6eb0eb755de3f2842c235946bfd7ccad04ccf7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474729"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>Negalite importuoti prekės naudodami objektą Išleisti produktai V2

KB numeris: 4611825

## <a name="symptoms"></a>Požymiai

Kai bandote importuoti prekę naudodami objektą *Išleistų produktų V2* ojekte, gaunate klaidos pranešimą, kuris yra panašus į tokį pavyzdį:

> Negalima sukurti įrašo prekėse – sekimo dimensijų grupėse (EcoResTrackingDimensionGroupItem). Prekės numeris: 2040663, Paketas. Toks įrašas jau yra.

## <a name="resolution"></a>Skiriamoji geba

Norėdami importuoti naujus išleistus produktus, naudokite objektą *Išleisto produkto kūrimo V2* o ne *išleistų produktų V2* objektą.
