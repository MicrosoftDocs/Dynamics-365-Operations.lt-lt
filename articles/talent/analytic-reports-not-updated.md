---
title: "Analitinės ataskaitos neatnaujinamos"
description: "Šioje temoje paaiškinama, ką daryti, jei kliento duomenų keitimai nerodomi jokioje darbo srityje."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.contentlocale: lt-lt
ms.lasthandoff: 12/04/2018

---

# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="27e06-103">Analitinės ataskaitos neatnaujinamos</span><span class="sxs-lookup"><span data-stu-id="27e06-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="27e06-104">**Problema**</span><span class="sxs-lookup"><span data-stu-id="27e06-104">**Issue**</span></span>

<span data-ttu-id="27e06-105">Kliento duomenų keitimai nerodomi jokios kliento darbo srities skirtuke **Analizė**.</span><span class="sxs-lookup"><span data-stu-id="27e06-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="27e06-106">**Priežastis**</span><span class="sxs-lookup"><span data-stu-id="27e06-106">**Cause**</span></span>

<span data-ttu-id="27e06-107">Pagal numatytuosius nustatymus „Microsoft Power BI“ ataskaitos atnaujinamos kas keturias valandas pagal matavimo vieneto paketinės užduoties visuotinio diegimo grafiką.</span><span class="sxs-lookup"><span data-stu-id="27e06-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="27e06-108">**Skiriamoji geba**</span><span class="sxs-lookup"><span data-stu-id="27e06-108">**Resolution**</span></span>

<span data-ttu-id="27e06-109">Ši problema gali būti tik laikina.</span><span class="sxs-lookup"><span data-stu-id="27e06-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="27e06-110">Norėdami paleisti paketinę užduotį ir atnaujinti analizės darbo sritis, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="27e06-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="27e06-111">Atidarykite puslapį **Paketinės užduotys**, esantį **Sistemos administravimas \> Saitai \> Paketinės užduotys \> Paketinės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="27e06-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="27e06-112">Arba naudokite iešką ir įveskite **Paketinės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="27e06-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="27e06-113">Sąraše raskite užduotį **Matavimo vieneto visuotinis diegimas**.</span><span class="sxs-lookup"><span data-stu-id="27e06-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="27e06-114">Puslapio viršuje pasirinkite **Redaguoti** ir nustatykite suplanuotos paleidimo datos arba laiko vertę, pagal kurią analizė bus atnaujinta arčiau dabartinio laiko.</span><span class="sxs-lookup"><span data-stu-id="27e06-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Paketinės užduotys](media/batch-jobs.png)

