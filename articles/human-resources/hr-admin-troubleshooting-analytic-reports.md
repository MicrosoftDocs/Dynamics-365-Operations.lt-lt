---
title: Analizės ataskaitų trikčių diagnostika
description: Šiame straipsnyje paaiškinama, ką daryti, jei kliento duomenų keitimai nerodomi jokioje darbo srityje.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 99d9eb3a16e6470820a2eb0a19c1d50e89bd3d36
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009887"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="6ee74-103">Analizės ataskaitų trikčių diagnostika</span><span class="sxs-lookup"><span data-stu-id="6ee74-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="6ee74-104">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="6ee74-104">**Issue**</span></span>

<span data-ttu-id="6ee74-105">Kliento duomenų keitimai nerodomi jokios kliento darbo srities skirtuke **Analizė**.</span><span class="sxs-lookup"><span data-stu-id="6ee74-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="6ee74-106">**Priežastis**</span><span class="sxs-lookup"><span data-stu-id="6ee74-106">**Cause**</span></span>

<span data-ttu-id="6ee74-107">Pagal numatytuosius nustatymus „Microsoft Power BI“ ataskaitos atnaujinamos kas keturias valandas pagal matavimo vieneto paketinės užduoties visuotinio diegimo grafiką.</span><span class="sxs-lookup"><span data-stu-id="6ee74-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="6ee74-108">**Skiriamoji geba**</span><span class="sxs-lookup"><span data-stu-id="6ee74-108">**Resolution**</span></span>

<span data-ttu-id="6ee74-109">Ši problema gali būti tik laikina.</span><span class="sxs-lookup"><span data-stu-id="6ee74-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="6ee74-110">Norėdami paleisti paketinę užduotį ir atnaujinti analizės darbo sritis, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6ee74-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="6ee74-111">Atidarykite puslapį **Paketinės užduotys**, esantį **Sistemos administravimas \> Saitai \> Paketinės užduotys \> Paketinės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="6ee74-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="6ee74-112">Arba naudokite iešką ir įveskite **Paketinės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="6ee74-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="6ee74-113">Sąraše raskite užduotį **Matavimo vieneto visuotinis diegimas**.</span><span class="sxs-lookup"><span data-stu-id="6ee74-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="6ee74-114">Puslapio viršuje pasirinkite **Redaguoti** ir nustatykite suplanuotos paleidimo datos arba laiko vertę, pagal kurią analizė bus atnaujinta arčiau dabartinio laiko.</span><span class="sxs-lookup"><span data-stu-id="6ee74-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Paketinės užduotys](media/batch-jobs.png)
