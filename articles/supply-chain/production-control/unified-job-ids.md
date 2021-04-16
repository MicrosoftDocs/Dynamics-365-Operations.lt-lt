---
title: Bendra užduočių ID numerių seka
description: Ši funkcija suteikia bendrą, suvienodintą numeraciją, kuri sugeneruoja užduočių ID gamybos kontrolės, gamybos vykdymo ir laiko bei dalyvavo moduliams.
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824947"
---
# <a name="unified-number-sequence-for-job-ids"></a><span data-ttu-id="34006-103">Bendra užduočių ID numerių seka</span><span class="sxs-lookup"><span data-stu-id="34006-103">Unified number sequence for job IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34006-104">Ši funkcija suteikia bendrą, suvienodintą numeraciją, kuri sugeneruoja užduočių ID gamybos kontrolės, gamybos vykdymo ir laiko bei dalyvavo moduliams.</span><span class="sxs-lookup"><span data-stu-id="34006-104">This feature provides a single, unified number sequence that generates job IDs for the Production control, Manufacturing execution, and Time and attendance modules.</span></span> <span data-ttu-id="34006-105">Anksčiau galėjote pasirinkti skirtingą numeraciją kiekvienam šių modulių, tad galėdavo būti nesuderinamų užduočių ID, jei dvi ar daugiau numeracijų naudojo tą patį formatą.</span><span class="sxs-lookup"><span data-stu-id="34006-105">Previously, you were able to choose a different number sequence for each of these modules, which could result in conflicting job IDs if two or more of these sequences used an identical format.</span></span> <span data-ttu-id="34006-106">Toks nesuderinamumas gali sugadinti duomenis.</span><span class="sxs-lookup"><span data-stu-id="34006-106">Such a conflict can cause data corruption.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="34006-107">Šios funkcijos įjungimas sistemoje</span><span class="sxs-lookup"><span data-stu-id="34006-107">Turn on this feature for your system</span></span>

<span data-ttu-id="34006-108">Jei jūsų sistemoje dar nėra šioje temoje aprašytos funkcijos, eikite į [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ir įjunkite funkciją *Suvienodinta užduočių ID numeracija*.</span><span class="sxs-lookup"><span data-stu-id="34006-108">If your system doesn't already include the feature described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Unified number sequence for job IDs* feature.</span></span>

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a><span data-ttu-id="34006-109">Suvienodintos užduočių ID numeracijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="34006-109">Set up the unified number sequence for job IDs</span></span>

<span data-ttu-id="34006-110">Įgalinus šią funkciją, esami **Užduoties identifikacijos** numeracijos parametrai, esantys gamybos kontrolės, gamybos vykdymo ir laiko bei dalyvavimo modulių parametrų puslapiuose, bus nerekomenduojami ir bus įtrauktas naujas laukas **Suvienodinti užduočių ID**.</span><span class="sxs-lookup"><span data-stu-id="34006-110">After enabling this feature, the existing **Job identification** number-sequence settings located on the parameters pages for the Production control, Manufacturing execution, and Time and attendance modules will be deprecated and a new **Unified job ID** field will be added.</span></span> <span data-ttu-id="34006-111">Reikšmę **Suvienodinti užduočių ID** bendrai naudoja visi trys moduliai ir taip užtikrinama, kad visi moduliai nurodo tą pačią numeraciją.</span><span class="sxs-lookup"><span data-stu-id="34006-111">The **Unified job ID** value is shared by all three modules, thus ensuring that all modules reference the same number sequence.</span></span> <span data-ttu-id="34006-112">Todėl užduočių ID bus unikalūs visuose trijuose moduliuose, tad niekada neatsiras nesuderinamumas.</span><span class="sxs-lookup"><span data-stu-id="34006-112">Job IDs will therefore be unique across all three modules and a conflict will never occur.</span></span>

<span data-ttu-id="34006-113">Norėdami nustatyti suvienodintą užduočių ID numeraciją:</span><span class="sxs-lookup"><span data-stu-id="34006-113">To set up the unified number sequence for job IDs:</span></span>

1. <span data-ttu-id="34006-114">Įjunkite funkciją, kaip aprašyta ankstesniame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="34006-114">Turn on the feature as described in the previous section.</span></span>
1. <span data-ttu-id="34006-115">Nustatykite numeraciją, kurią norite naudoti savo vieningiems užduočių ID, arba sukurkite naują.</span><span class="sxs-lookup"><span data-stu-id="34006-115">Either identify the number sequence you want to use for your unified job IDs, or create a new one.</span></span> <span data-ttu-id="34006-116">Daugiau informacijos žr. skyriuje [Numeracijos apžvalga](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="34006-116">For more information, see [Number sequences overview](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).</span></span>
1. <span data-ttu-id="34006-117">Eikite į **Gamybos kontrolės parametrai**, **Gamybos vykdymo parametrai** arba **Laiko bei dalyvavimo parametrai** puslapį.</span><span class="sxs-lookup"><span data-stu-id="34006-117">Go to the **Production control parameters**, **Manufacturing execution parameters**, or **Time and attendance parameters** page.</span></span> <span data-ttu-id="34006-118">Nesvarbu, kurį puslapį pasirinksite, nes kai nustatote parametrą bet kuriame šių puslapių, visi kiti puslapiai atsinaujina automatiškai.</span><span class="sxs-lookup"><span data-stu-id="34006-118">It doesn't matter which one you choose because when you make this setting on any of those pages, all of the other pages will update automatically.</span></span>
1. <span data-ttu-id="34006-119">Atidarykite skirtuką **Numeracijos** pasirinktame parametrų puslapyje.</span><span class="sxs-lookup"><span data-stu-id="34006-119">Open the **Number sequences** tab on your selected parameters page.</span></span>
1. <span data-ttu-id="34006-120">Priskirkite **Numeracijos kodą**, kurį anksčiau nustatėte tinklelio eilutėje **Suvienodinti užduočių ID**.</span><span class="sxs-lookup"><span data-stu-id="34006-120">Assign the **Number sequence code** that you identified previously to the **Unified job IDs** row of the grid.</span></span>
