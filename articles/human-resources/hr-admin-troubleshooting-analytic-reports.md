---
title: Analizės ataskaitų trikčių diagnostika
description: Šiame straipsnyje paaiškinama, ką daryti, jei kliento duomenų keitimai nerodomi jokioje darbo srityje.
author: andreabichsel
ms.date: 02/03/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b500d519d61edfd20456355376e3fc81f16517a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794978"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="786f2-103">Analizės ataskaitų trikčių diagnostika</span><span class="sxs-lookup"><span data-stu-id="786f2-103">Troubleshoot analytic reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="786f2-104">**Išduoti**</span><span class="sxs-lookup"><span data-stu-id="786f2-104">**Issue**</span></span>

<span data-ttu-id="786f2-105">Kliento duomenų keitimai nerodomi jokios kliento darbo srities skirtuke **Analizė**.</span><span class="sxs-lookup"><span data-stu-id="786f2-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="786f2-106">**Priežastis**</span><span class="sxs-lookup"><span data-stu-id="786f2-106">**Cause**</span></span>

<span data-ttu-id="786f2-107">Pagal numatytuosius nustatymus „Microsoft Power BI“ ataskaitos atnaujinamos kas keturias valandas pagal matavimo vieneto paketinės užduoties visuotinio diegimo grafiką.</span><span class="sxs-lookup"><span data-stu-id="786f2-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="786f2-108">**Skiriamoji geba**</span><span class="sxs-lookup"><span data-stu-id="786f2-108">**Resolution**</span></span>

<span data-ttu-id="786f2-109">Ši problema gali būti tik laikina.</span><span class="sxs-lookup"><span data-stu-id="786f2-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="786f2-110">Norėdami paleisti paketinę užduotį ir atnaujinti analizės darbo sritis, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="786f2-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="786f2-111">Atidarykite puslapį **Paketinės užduotys**, esantį **Sistemos administravimas \> Saitai \> Paketinės užduotys \> Paketinės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="786f2-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="786f2-112">Arba naudokite iešką ir įveskite **Paketinės užduotys**.</span><span class="sxs-lookup"><span data-stu-id="786f2-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="786f2-113">Sąraše raskite užduotį **Matavimo vieneto visuotinis diegimas**.</span><span class="sxs-lookup"><span data-stu-id="786f2-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="786f2-114">Puslapio viršuje pasirinkite **Redaguoti** ir nustatykite suplanuotos paleidimo datos arba laiko vertę, pagal kurią analizė bus atnaujinta arčiau dabartinio laiko.</span><span class="sxs-lookup"><span data-stu-id="786f2-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Paketinės užduotys](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]