---
title: Iš naujo nustatyti įstrigusias paketines užduotis
description: Šioje temoje paaiškinama, kaip išspręsti problemas, susijusias su paketine užduotimis, kurios yra įstrigusios.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 01ef0bf8ccc486614eec42d3fb6f0b2941fc47c0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794954"
---
# <a name="reset-stuck-batch-jobs"></a><span data-ttu-id="a290a-103">Iš naujo nustatyti įstrigusias paketines užduotis</span><span class="sxs-lookup"><span data-stu-id="a290a-103">Reset stuck batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a><span data-ttu-id="a290a-104">Išdavimas</span><span class="sxs-lookup"><span data-stu-id="a290a-104">Issue</span></span>

<span data-ttu-id="a290a-105">Programoje gali kilti problemų dėl paketinių užduočių, kurios yra vykdymo arba atšaukimo būsenos „Microsoft Dynamics 365 Human Resources“ **ir nėra** **baigtos**.</span><span class="sxs-lookup"><span data-stu-id="a290a-105">Microsoft Dynamics 365 Human Resources can experience issues with batch jobs that are stuck in either an **Executing** or **Canceling** state and don't complete.</span></span>

## <a name="resolution"></a><span data-ttu-id="a290a-106">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="a290a-106">Resolution</span></span>

<span data-ttu-id="a290a-107">Kai paketinės užduoties būsena yra Vykdoma arba Atšaukiama, galite grąžinti būseną **užduočiai** **atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="a290a-107">When a batch job is stuck in an **Executing** or **Canceling** state, you can reset the status by forcing the cancellation of the job.</span></span> <span data-ttu-id="a290a-108">Atšaukę paketinę užduotį galite ją nustatyti iš naujo, nustatydami laukimo **būseną**.</span><span class="sxs-lookup"><span data-stu-id="a290a-108">After you cancel it, you can reset the batch job by setting it to a **Waiting** status.</span></span> <span data-ttu-id="a290a-109">Tada jis bus paimtas dar kartą, kad būtų galima vykdyti kitame suplanuotame pakete.</span><span class="sxs-lookup"><span data-stu-id="a290a-109">It will then be picked up again for execution in the next scheduled batch run.</span></span>

1. <span data-ttu-id="a290a-110">Sistemos administravimo **darbo srityje pasirinkite puslapį** **Saitai ir pasirinkite** **Paketinės** užduotys.</span><span class="sxs-lookup"><span data-stu-id="a290a-110">In the **System administration** workspace, select the **Links** page, and select **Batch jobs**.</span></span>

2. <span data-ttu-id="a290a-111">Paketinių **užduočių sąrašo puslapyje pasirinkite** užduotį, kurią reikia nustatyti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="a290a-111">On the **Batch job** list page, select the job that needs to be reset.</span></span>

3. <span data-ttu-id="a290a-112">Veiksmų juostelėje pasirinkite **Atšaukti ir** patvirtinkite veiksmą.</span><span class="sxs-lookup"><span data-stu-id="a290a-112">On the action ribbon, select **Force cancel**, and confirm the action.</span></span>

   > [!NOTE]
   > <span data-ttu-id="a290a-113">Veiksmas Priversties atšaukimas galimas tik tada, kai pasirinktos paketinės užduoties būsena yra Vykdoma arba Atšaukiama ir užduoties paketinio vykdymo **arba atšaukimo procesai** **nėra** **vykdomos**.</span><span class="sxs-lookup"><span data-stu-id="a290a-113">The **Force cancel** action is only available when the selected batch job has a status of either **Executing** or **Canceling**, and no batch execution or cancellation processes are running for the job.</span></span>

4. <span data-ttu-id="a290a-114">Veiksmų juostoje rinkitės **Keisti būseną**.</span><span class="sxs-lookup"><span data-stu-id="a290a-114">On the action ribbon, select **Change status**.</span></span>

5. <span data-ttu-id="a290a-115">Puslapyje **Pasirinkti naują** būseną pasirinkite **Laukiama**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a290a-115">On the **Select new status** page, select **Waiting**, and then select **OK**.</span></span>

   ![Pasirinkti naują paketinės užduoties būseną](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a><span data-ttu-id="a290a-117">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="a290a-117">See also</span></span>

[<span data-ttu-id="a290a-118">Efektyvumo optimizavimas planuojant paketines užduotis po darbo valandų</span><span class="sxs-lookup"><span data-stu-id="a290a-118">Optimize performance by scheduling batch jobs after hours</span></span>](hr-admin-troubleshooting-batch-jobs.md)<br>
[<span data-ttu-id="a290a-119">Efektyvumo optimizavimas naudojant automatinio valymo užduotis</span><span class="sxs-lookup"><span data-stu-id="a290a-119">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
