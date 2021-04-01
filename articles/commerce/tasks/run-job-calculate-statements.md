---
title: Konfigūruoti ir vykdyti išrašų skaičiavimo užduotį
description: Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančias paketines užduotis, norint kurti ir apskaičiuoti pasirinktos parduotuvės arba parduotuvių grupės išrašus.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8366bfff16bac8ef8f7b15cb97417d474b52f59c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232766"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="c3aa3-103">Konfigūruoti ir vykdyti išrašų skaičiavimo užduotį</span><span class="sxs-lookup"><span data-stu-id="c3aa3-103">Configure and run job to calculate statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3aa3-104">Ši procedūra padeda konfigūruoti ir vykdyti pasikartojančias paketines užduotis, norint kurti ir apskaičiuoti pasirinktos parduotuvės arba parduotuvių grupės išrašus.</span><span class="sxs-lookup"><span data-stu-id="c3aa3-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="c3aa3-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="c3aa3-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="c3aa3-106">Eikite į Visos darbo sritys > Parduotuvės finansai.</span><span class="sxs-lookup"><span data-stu-id="c3aa3-106">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="c3aa3-107">Spustelėkite Skaičiuoti išrašus.</span><span class="sxs-lookup"><span data-stu-id="c3aa3-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="c3aa3-108">Pasirinkite konkrečią parduotuvę arba mazgą, jei norite kurti parduotuvių grupės paketinę užduotį.</span><span class="sxs-lookup"><span data-stu-id="c3aa3-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="c3aa3-109">Spustelėkite rodyklę ir įtraukite savo pasirinkimą.</span><span class="sxs-lookup"><span data-stu-id="c3aa3-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="c3aa3-110">Spustelėkite skirtuką Vykdyti fone.</span><span class="sxs-lookup"><span data-stu-id="c3aa3-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="c3aa3-111">Šalia dalis Paketinis vykdymas pasirinkite „Taip“.</span><span class="sxs-lookup"><span data-stu-id="c3aa3-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="c3aa3-112">Spustelėkite Pasikartojimas.</span><span class="sxs-lookup"><span data-stu-id="c3aa3-112">Click Recurrence.</span></span>
6. <span data-ttu-id="c3aa3-113">Lauke Pradžios data įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="c3aa3-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="c3aa3-114">Lauke Pradžios laikas įveskite laiką.</span><span class="sxs-lookup"><span data-stu-id="c3aa3-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="c3aa3-115">Pasirinkite parinktį Nėra pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="c3aa3-115">Select the No end date option.</span></span>
9. <span data-ttu-id="c3aa3-116">Lauke „PatternUnit“ įveskite „Dienos“.</span><span class="sxs-lookup"><span data-stu-id="c3aa3-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="c3aa3-117">Lauke Per įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="c3aa3-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="c3aa3-118">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c3aa3-118">Click OK.</span></span>
12. <span data-ttu-id="c3aa3-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="c3aa3-119">Click OK.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]