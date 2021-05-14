---
title: Darbo atšaukti negalima dėl jo būsenos
description: Darbo atšaukti negalima dėl jo būsenos
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
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924260"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a><span data-ttu-id="cf778-103">Darbo atšaukti negalima dėl jo būsenos</span><span class="sxs-lookup"><span data-stu-id="cf778-103">Work can't be canceled because of its status</span></span>

<span data-ttu-id="cf778-104">Klaidos kodas: WAX2190</span><span class="sxs-lookup"><span data-stu-id="cf778-104">Error code: WAX2190</span></span>

## <a name="symptoms"></a><span data-ttu-id="cf778-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="cf778-105">Symptoms</span></span>

<span data-ttu-id="cf778-106">Sistema rodo tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="cf778-106">The system shows the following error message:</span></span>

> <span data-ttu-id="cf778-107">Darbo %1 atšaukti negalite, nes jo būsena %2.</span><span class="sxs-lookup"><span data-stu-id="cf778-107">You cannot cancel work %1 because it has a status of %2.</span></span>

## <a name="cause"></a><span data-ttu-id="cf778-108">Priežastis</span><span class="sxs-lookup"><span data-stu-id="cf778-108">Cause</span></span>

<span data-ttu-id="cf778-109">Dabartinės darbo būsenos atšaukti negalima.</span><span class="sxs-lookup"><span data-stu-id="cf778-109">The work can't be canceled in its current state.</span></span>

<span data-ttu-id="cf778-110">Darbo antraštėje arba darbo eilutėse nėra numatomos **darbo būsenos** vertės.</span><span class="sxs-lookup"><span data-stu-id="cf778-110">The work header or work lines don't have the expected **Work status** value.</span></span> <span data-ttu-id="cf778-111">Darbo **antraštės laukas Darbo būsena nėra nustatytas** *kaip* Atidaryta arba *Vykdoma*.</span><span class="sxs-lookup"><span data-stu-id="cf778-111">The **Work status** field on the work header isn't set to *Open* or *In progress*.</span></span>

## <a name="resolution"></a><span data-ttu-id="cf778-112">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="cf778-112">Resolution</span></span>

<span data-ttu-id="cf778-113">Norėdami atšaukti darbą atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="cf778-113">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="cf778-114">Eiti į **Sandėlio valdymo \> periodines užduotis \> Valyti darbą \> Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="cf778-114">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="cf778-115">Lauke **Darbo ID** nurodykite darbo, kurį norite atšaukti, ID.</span><span class="sxs-lookup"><span data-stu-id="cf778-115">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="cf778-116">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="cf778-116">Select **OK**.</span></span>
1. <span data-ttu-id="cf778-117">Pasirinkite **Taip**, kad patvirtintumėte, kad norite atšaukti darbą.</span><span class="sxs-lookup"><span data-stu-id="cf778-117">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="cf778-118">Dėl platesnės informacijos, žr. [Darbo sandėlyje atšaukimas dėl išimčių tvarkymo](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="cf778-118">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
