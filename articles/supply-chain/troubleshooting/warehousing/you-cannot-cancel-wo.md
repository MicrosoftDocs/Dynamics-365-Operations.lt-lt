---
title: Negalima atšaukti vartotojui būsiančių darbų
description: Negalima atšaukti vartotojui būsiančių darbų
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924406"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a><span data-ttu-id="ad77e-103">Negalima atšaukti vartotojui būsiančių darbų</span><span class="sxs-lookup"><span data-stu-id="ad77e-103">You can't cancel work that is on a user</span></span>

<span data-ttu-id="ad77e-104">Klaidos kodas: WAX708</span><span class="sxs-lookup"><span data-stu-id="ad77e-104">Error code: WAX708</span></span>

## <a name="symptoms"></a><span data-ttu-id="ad77e-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="ad77e-105">Symptoms</span></span>

<span data-ttu-id="ad77e-106">Sistema rodo tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="ad77e-106">The system shows the following error message:</span></span>

> <span data-ttu-id="ad77e-107">Negalima atšaukti vartotojui priskirto darbo.</span><span class="sxs-lookup"><span data-stu-id="ad77e-107">You cannot cancel work that is on a user.</span></span>

## <a name="cause"></a><span data-ttu-id="ad77e-108">Priežastis</span><span class="sxs-lookup"><span data-stu-id="ad77e-108">Cause</span></span>

<span data-ttu-id="ad77e-109">Darbą užrakina vartotojas ir jo atšaukti negalima.</span><span class="sxs-lookup"><span data-stu-id="ad77e-109">The work is locked by a user and can't be canceled.</span></span> <span data-ttu-id="ad77e-110">Norėdami tai patvirtinti, atidarykite darbo ID ir atidarykite **skirtuką** Bendra. Jei darbas užrakintas, darbo būsenos laukas bus nustatytas į Vykdoma, o laukas Užrakinta pagal **bus nustatytas** *kaip* **vartotojo** ID.</span><span class="sxs-lookup"><span data-stu-id="ad77e-110">To confirm this, open the work ID and then open the **General** tab. If the work is locked, the **Work status** field will be set to *In progress*, and the **Locked by** field will be set to a user ID.</span></span>

## <a name="resolution"></a><span data-ttu-id="ad77e-111">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="ad77e-111">Resolution</span></span>

<span data-ttu-id="ad77e-112">Norėdami atšaukti darbą atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="ad77e-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="ad77e-113">Eiti į **Sandėlio valdymo \> periodines užduotis \> Valyti darbą \> Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="ad77e-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="ad77e-114">Lauke **Darbo ID** nurodykite darbo, kurį norite atšaukti, ID.</span><span class="sxs-lookup"><span data-stu-id="ad77e-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="ad77e-115">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ad77e-115">Select **OK**.</span></span>
1. <span data-ttu-id="ad77e-116">Pasirinkite **Taip**, kad patvirtintumėte, kad norite atšaukti darbą.</span><span class="sxs-lookup"><span data-stu-id="ad77e-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="ad77e-117">Dėl platesnės informacijos, žr. [Darbo sandėlyje atšaukimas dėl išimčių tvarkymo](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="ad77e-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
