---
title: Efektyvumo optimizavimas naudojant automatinio valymo užduotis
description: Šiame straipsnyje paaiškinama, kaip išspręsti tam tikras našumo problemas naudojant „Microsoft Dynamics 365 Human Resources“, valant paketinių užduočių retrospektyvą.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 6a9e94e282aa8f101b42c1378ef21c6c1fe0477e
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053496"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="f4a10-103">Našumo optimizavimas naudojant automatinio valymo užduotis</span><span class="sxs-lookup"><span data-stu-id="f4a10-103">Optimize performance with auto cleanup tasks</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f4a10-104">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="f4a10-104">**Issue**</span></span>

<span data-ttu-id="f4a10-105">Naudojant „Microsoft“ „Dynamics 365 Human Resources“, gali kilti našumo problemų, jei paketinių užduočių retrospektyva tampa per ilga.</span><span class="sxs-lookup"><span data-stu-id="f4a10-105">Microsoft Dynamics 365 Human Resources can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="f4a10-106">**Priežastis**</span><span class="sxs-lookup"><span data-stu-id="f4a10-106">**Cause**</span></span>

<span data-ttu-id="f4a10-107">Jei paketinės užduotys vykdomos dažnai, paketinių užduočių retrospektyva gali pernelyg pailgėti.</span><span class="sxs-lookup"><span data-stu-id="f4a10-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="f4a10-108">Tai gali sukelti našumo problemų.</span><span class="sxs-lookup"><span data-stu-id="f4a10-108">This can cause performance issues.</span></span> 

<span data-ttu-id="f4a10-109">**Nutarimas**</span><span class="sxs-lookup"><span data-stu-id="f4a10-109">**Resolution**</span></span>

<span data-ttu-id="f4a10-110">Suplanuokite automatinę užduotį, kad išvalytumėte paketinių užduočių retrospektyvą.</span><span class="sxs-lookup"><span data-stu-id="f4a10-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="f4a10-111">Rekomenduojame nustatyti, kad užduotis būtų vykdoma kas savaitę, tačiau, atsižvelgiant į jūsų aplinką, gali reikėti valyti dažniau ar rečiau.</span><span class="sxs-lookup"><span data-stu-id="f4a10-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="f4a10-112">Šioje procedūroje pateikiami rekomenduojami parametrai, tačiau juos galite keisti pagal poreikius.</span><span class="sxs-lookup"><span data-stu-id="f4a10-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="f4a10-113">Programoje „Human Resources“ pasirinkite **Sistemos administravimas**.</span><span class="sxs-lookup"><span data-stu-id="f4a10-113">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="f4a10-114">Juostoje **Ieška** įveskite **Paketinių užduočių retrospektyvos valymas**.</span><span class="sxs-lookup"><span data-stu-id="f4a10-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![Paketinių užduočių retrospektyvos valymo ieška](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="f4a10-116">Lauke **Retrospektyvos riba (dienos)** įveskite **30**.</span><span class="sxs-lookup"><span data-stu-id="f4a10-116">In **History limit (days)**, enter **30**.</span></span>

   ![30 dienų retrospektyvos ribos nustatymas](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="f4a10-118">Pasirinkite **Vykdyti fone**, tada pasirinkite **Pasikartojimas**.</span><span class="sxs-lookup"><span data-stu-id="f4a10-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![Pasikartojimo nustatymas](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="f4a10-120">Dalyje **Nurodyti pasikartojimą** nustatykite parinktis **Pradžios data** ir **Pradžios laikas**, kad valymas būtų vykdomas po darbo arba savaitgalį, paskui pasirinkite **NĖRA PABAIGOS DATOS**.</span><span class="sxs-lookup"><span data-stu-id="f4a10-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![Pasikartojimo pradžios datos ir laiko nurodymas](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="f4a10-122">Dalyje **KARTOJIMAS** pasirinkite **Dienos** ir nustatykite parinkties **PAKARTOTI PO NURODYTO INTERVALO** reikšmę **7**.</span><span class="sxs-lookup"><span data-stu-id="f4a10-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![Nustatymas, kad valymas būtų kartojamas kas savaitę](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="f4a10-124">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f4a10-124">Select **OK**.</span></span>

8. <span data-ttu-id="f4a10-125">Jei reikia, dalyje **Vykdyti fone** pakeiskite kitus parametrus, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="f4a10-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]