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
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a><span data-ttu-id="28a1d-103">Negalite importuoti prekės naudodami objektą Išleisti produktai V2</span><span class="sxs-lookup"><span data-stu-id="28a1d-103">You can't import an item by using the Released products V2 entity</span></span>

<span data-ttu-id="28a1d-104">KB numeris: 4611825</span><span class="sxs-lookup"><span data-stu-id="28a1d-104">KB number: 4611825</span></span>

## <a name="symptoms"></a><span data-ttu-id="28a1d-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="28a1d-105">Symptoms</span></span>

<span data-ttu-id="28a1d-106">Kai bandote importuoti prekę naudodami objektą *Išleistų produktų V2* ojekte, gaunate klaidos pranešimą, kuris yra panašus į tokį pavyzdį:</span><span class="sxs-lookup"><span data-stu-id="28a1d-106">When you try to import an item by using the *Released products V2* entity, you receive an error message that resembles the following example:</span></span>

> <span data-ttu-id="28a1d-107">Negalima sukurti įrašo prekėse – sekimo dimensijų grupėse (EcoResTrackingDimensionGroupItem).</span><span class="sxs-lookup"><span data-stu-id="28a1d-107">Cannot create a record in Items - tracking dimension groups (EcoResTrackingDimensionGroupItem).</span></span> <span data-ttu-id="28a1d-108">Prekės numeris: 2040663, Paketas.</span><span class="sxs-lookup"><span data-stu-id="28a1d-108">Item number: 2040663, Batch.</span></span> <span data-ttu-id="28a1d-109">Toks įrašas jau yra.</span><span class="sxs-lookup"><span data-stu-id="28a1d-109">The record already exists.</span></span>

## <a name="resolution"></a><span data-ttu-id="28a1d-110">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="28a1d-110">Resolution</span></span>

<span data-ttu-id="28a1d-111">Norėdami importuoti naujus išleistus produktus, naudokite objektą *Išleisto produkto kūrimo V2* o ne *išleistų produktų V2* objektą.</span><span class="sxs-lookup"><span data-stu-id="28a1d-111">To import new released products, you must use the *Released product creation V2* entity instead of the *Released products V2* entity.</span></span>
