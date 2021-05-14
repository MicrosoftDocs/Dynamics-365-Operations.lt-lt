---
title: Darbas neužblokuotas
description: Darbas neužblokuotas
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d64ab282972e46e8857581b59e5705dd15667328
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924209"
---
# <a name="work-isnt-blocked"></a><span data-ttu-id="82991-103">Darbas neužblokuotas</span><span class="sxs-lookup"><span data-stu-id="82991-103">Work isn't blocked</span></span>

<span data-ttu-id="82991-104">Klaidos kodas: WHSUnblockNotBlockedWorkErrorMessage</span><span class="sxs-lookup"><span data-stu-id="82991-104">Error code: WHSUnblockNotBlockedWorkErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="82991-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="82991-105">Symptoms</span></span>

<span data-ttu-id="82991-106">Sistema rodo tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="82991-106">The system shows the following error message:</span></span>

> <span data-ttu-id="82991-107">Dirbas su ID %1 nėra užblokuotas.</span><span class="sxs-lookup"><span data-stu-id="82991-107">Work with Id %1 is not blocked.</span></span>

## <a name="cause"></a><span data-ttu-id="82991-108">Priežastis</span><span class="sxs-lookup"><span data-stu-id="82991-108">Cause</span></span>

<span data-ttu-id="82991-109">Bangos **parinktis** Užblokuota banga nustatyta kaip *Ne*.</span><span class="sxs-lookup"><span data-stu-id="82991-109">The **Blocked wave** option on the wave is set to *No*.</span></span> <span data-ttu-id="82991-110">Darbo atblokuoti negalima, nes jis šiuo metu nėra užblokuotas.</span><span class="sxs-lookup"><span data-stu-id="82991-110">The work can't be unblocked because it isn't currently blocked.</span></span>

## <a name="resolution"></a><span data-ttu-id="82991-111">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="82991-111">Resolution</span></span>

 <span data-ttu-id="82991-112">Galima **atblokuoti tik** darbą, kai nustatyta *parinktis* Užblokuota banga kaip Taip.</span><span class="sxs-lookup"><span data-stu-id="82991-112">Only work where the **Blocked wave** option is set to *Yes* can be unblocked.</span></span>
