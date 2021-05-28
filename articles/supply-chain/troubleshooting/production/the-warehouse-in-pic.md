---
title: Sandėlis išrinkimo dokumento žurnale nėra atnaujintas KS eilutėje.
description: Sandėlis išrinkimo dokumento žurnale nėra atnaujintas medžiagos važtaraštyje KS eilutėje.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdJournalTransBOM
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 5d24c0b8538f3894fd1d2a3edb3a6ed8633c9609
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026736"
---
# <a name="the-warehouse-in-the-picking-list-journal-isnt-updated-on-a-bom-line"></a><span data-ttu-id="2383c-103">Sandėlis išrinkimo dokumento žurnale nėra atnaujintas KS eilutėje</span><span class="sxs-lookup"><span data-stu-id="2383c-103">The warehouse in the picking list journal isn't updated on a BOM line</span></span>

<span data-ttu-id="2383c-104">KB numeris: 4614848</span><span class="sxs-lookup"><span data-stu-id="2383c-104">KB number: 4614848</span></span>

## <a name="symptoms"></a><span data-ttu-id="2383c-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="2383c-105">Symptoms</span></span>

<span data-ttu-id="2383c-106">Sandėlis išrinkimo dokumento žurnale nėra atnaujintas medžiagos važtaraštyje KS eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2383c-106">The warehouse in the picking list journal isn't updated on a bill of materials (BOM) line.</span></span>

## <a name="resolution"></a><span data-ttu-id="2383c-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="2383c-107">Resolution</span></span>

<span data-ttu-id="2383c-108">Sistema veikia kaip sukurta.</span><span class="sxs-lookup"><span data-stu-id="2383c-108">The system is behaving as designed.</span></span> <span data-ttu-id="2383c-109">Jei sukuriama išrinkimo dokumento žurnalo eilutė su nuoroda (per partijos ID) į gamybos KS eilutę, gamybos KS eilutėje nurodytas sandėlis nebus atnaujinamas, jei sandėlio dimensija gamybos išrinkimo dokumento žurnalo eilutėje bus pakeista vėliau.</span><span class="sxs-lookup"><span data-stu-id="2383c-109">If a picking list journal line is created that has a reference (via the lot ID) to a production BOM line, the warehouse on the production BOM line won't be updated if the warehouse dimension on the production picking list journal line is changed later.</span></span>
