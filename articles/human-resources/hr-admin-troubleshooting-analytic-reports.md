---
title: Analizės ataskaitų trikčių diagnostika
description: Šiame straipsnyje paaiškinama, ką daryti, jei kliento duomenų keitimai nerodomi jokioje darbo srityje.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: c5e1a1d7044567a07acedf71e65ed244275acfd9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113560"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="c58ef-103">Analizės ataskaitų trikčių diagnostika</span><span class="sxs-lookup"><span data-stu-id="c58ef-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="c58ef-104">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="c58ef-104">**Issue**</span></span>

<span data-ttu-id="c58ef-105">Kliento duomenų keitimai nerodomi jokios kliento darbo srities skirtuke **Analizė**.</span><span class="sxs-lookup"><span data-stu-id="c58ef-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="c58ef-106">**Priežastis**</span><span class="sxs-lookup"><span data-stu-id="c58ef-106">**Cause**</span></span>

<span data-ttu-id="c58ef-107">Pagal numatytuosius nustatymus „Microsoft Power BI“ ataskaitos atnaujinamos kas keturias valandas pagal matavimo vieneto paketinės užduoties visuotinio diegimo grafiką.</span><span class="sxs-lookup"><span data-stu-id="c58ef-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="c58ef-108">**Skiriamoji geba**</span><span class="sxs-lookup"><span data-stu-id="c58ef-108">**Resolution**</span></span>

<span data-ttu-id="c58ef-109">Ši problema gali būti tik laikina.</span><span class="sxs-lookup"><span data-stu-id="c58ef-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="c58ef-110">Norėdami paleisti paketinę užduotį ir atnaujinti analizės darbo sritis, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="c58ef-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="c58ef-111">Atidarykite puslapį **Paketinės užduotys**, esantį **Sistemos administravimas \> Saitai \> Paketinės užduotys \> Paketinės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="c58ef-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="c58ef-112">Arba naudokite iešką ir įveskite **Paketinės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="c58ef-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="c58ef-113">Sąraše raskite užduotį **Matavimo vieneto visuotinis diegimas**.</span><span class="sxs-lookup"><span data-stu-id="c58ef-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="c58ef-114">Puslapio viršuje pasirinkite **Redaguoti** ir nustatykite suplanuotos paleidimo datos arba laiko vertę, pagal kurią analizė bus atnaujinta arčiau dabartinio laiko.</span><span class="sxs-lookup"><span data-stu-id="c58ef-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Paketinės užduotys](media/batch-jobs.png)
