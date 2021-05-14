---
title: Banga negali būti išvalyta
description: Banga negali būti išvalyta
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924332"
---
# <a name="wave-isnt-eligible-for-cleanup"></a><span data-ttu-id="52c6c-103">Banga negali būti išvalyta</span><span class="sxs-lookup"><span data-stu-id="52c6c-103">Wave isn't eligible for cleanup</span></span>

<span data-ttu-id="52c6c-104">Klaidos kodas: WaveNotEligibleForCleanup</span><span class="sxs-lookup"><span data-stu-id="52c6c-104">Error code: WaveNotEligibleForCleanup</span></span>

## <a name="symptoms"></a><span data-ttu-id="52c6c-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="52c6c-105">Symptoms</span></span>

<span data-ttu-id="52c6c-106">Sistema rodo tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="52c6c-106">The system shows the following error message:</span></span>

> <span data-ttu-id="52c6c-107">Bangos %1 valyti negalima.</span><span class="sxs-lookup"><span data-stu-id="52c6c-107">Wave %1 is not eligible for cleanup.</span></span>

<span data-ttu-id="52c6c-108">Bangos duomenų išvalyti negalima.</span><span class="sxs-lookup"><span data-stu-id="52c6c-108">The wave data can't be cleaned up.</span></span>  

## <a name="cause"></a><span data-ttu-id="52c6c-109">Priežastis</span><span class="sxs-lookup"><span data-stu-id="52c6c-109">Cause</span></span>

<span data-ttu-id="52c6c-110">Banga šiuo metu apdorojama, kaip nurodyta vienoje iš šių sąlygų:</span><span class="sxs-lookup"><span data-stu-id="52c6c-110">The wave is currently being processed, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="52c6c-111">**Bangos būsenos** laukelis nustatytas į *Vykdomas*.</span><span class="sxs-lookup"><span data-stu-id="52c6c-111">The **Wave status** field is set to *Executing*.</span></span>
- <span data-ttu-id="52c6c-112">Jums pasirenkant **Paketo darbą** Bangos **grupėje** Bangos **skirtuke** veiksmų juostoje, **Statuso** laukelis nėra nustatytas į *Užbaigtas*, *Klaida* ar *Atšaukta*.</span><span class="sxs-lookup"><span data-stu-id="52c6c-112">When you select **Batch job** in the **Wave** group on the **Wave** tab of the Action Pane, the **Status** field isn't set to *Ended*, *Error*, or *Canceled*.</span></span> <span data-ttu-id="52c6c-113">Todėl paketinė užduotis šiuo metu vykdoma.</span><span class="sxs-lookup"><span data-stu-id="52c6c-113">Therefore, a batch job is currently running.</span></span>

## <a name="resolution"></a><span data-ttu-id="52c6c-114">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="52c6c-114">Resolution</span></span>

<span data-ttu-id="52c6c-115">Veiksmų srities skirtuko Banga grupėje **Bangos** pasirinkite **Paketinė** užduotis ir **atlikite** vieną iš šių veiksmų:</span><span class="sxs-lookup"><span data-stu-id="52c6c-115">On the Action Pane, on the **Wave** tab, in the **Wave** group, select **Batch job**, and then follow one of these steps:</span></span>

- <span data-ttu-id="52c6c-116">Jei **Būsenos** laukelis yra nustatytas į *Vykdomas*: veiksmų juostoje,**Paketo darbe** skirtuke rinkitės **Paketo darbo** grupę ir rinkitės **Peržiūrėti užduotis**.</span><span class="sxs-lookup"><span data-stu-id="52c6c-116">If the **Status** field is set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Batch job** group, select **View tasks**.</span></span> <span data-ttu-id="52c6c-117">Galite stebėti eigą naujindami **Paketų užduotys** puslapį.</span><span class="sxs-lookup"><span data-stu-id="52c6c-117">You can follow the progress by refreshing the **Batch tasks** page.</span></span>
- <span data-ttu-id="52c6c-118">Jei **Būsenos** laukelis nėra nustatytas į *Vykdomas*: veiksmų juostoje,**Paketo darbe** skirtuke rinkitės **Funkcijų darbo** grupę ir rinkitės **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="52c6c-118">If the **Status** field isn't set to *Executing*: On the Action Pane, on the **Batch job** tab, in the **Functions** group, select **Change status**.</span></span> <span data-ttu-id="52c6c-119">Laukelyje **Rinktis naują būseną** rinkitės *Laukiama*.</span><span class="sxs-lookup"><span data-stu-id="52c6c-119">In the **Select new status** field, select *Waiting*.</span></span> <span data-ttu-id="52c6c-120">Tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="52c6c-120">Then select **OK**.</span></span>
