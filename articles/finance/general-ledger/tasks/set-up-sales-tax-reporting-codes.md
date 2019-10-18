---
title: Nustatyti PVM ataskaitų kodus
description: PVM ataskaitų kodai – tai lauko numeris PVM ataskaitoje.
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4751256858da417ec9bb1b7d9ccd16fb6bef1cac
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185939"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="71881-103">Nustatyti PVM ataskaitų kodus</span><span class="sxs-lookup"><span data-stu-id="71881-103">Set up sales tax reporting codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71881-104">PVM ataskaitų kodai – tai lauko numeris PVM ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="71881-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="71881-105">Jie naudojami konkrečios šalies ataskaitų maketuose ir PVM mokėjimo pagal kodą ataskaitoje spausdinti PVM sumoms už sudengimo laikotarpį, susumuotą pagal ataskaitos kodą.</span><span class="sxs-lookup"><span data-stu-id="71881-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="71881-106">Sukūrus PVM ataskaitų kodus, galima į juos nurodyti „FastTab‟ Ataskaitų sąranka, esančiuose puslapyje PVM kodas.</span><span class="sxs-lookup"><span data-stu-id="71881-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="71881-107">Šiame įraše naudojama demonstracinė įmonė DEMF.</span><span class="sxs-lookup"><span data-stu-id="71881-107">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="71881-108">**Naršymo srityje** eikite į **Mokestis > Sąranka > PVM > PVM ataskaitų kodai**.</span><span class="sxs-lookup"><span data-stu-id="71881-108">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="71881-109">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="71881-109">Click **New**.</span></span>
3. <span data-ttu-id="71881-110">Pasirinkite ataskaitos maketą, kuriam priklauso ataskaitos kodas.</span><span class="sxs-lookup"><span data-stu-id="71881-110">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="71881-111">Šis maketas naudojamas filtruoti galimiems ataskaitų PVM kodams.</span><span class="sxs-lookup"><span data-stu-id="71881-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="71881-112">Kiekvienas PVM kodas priklauso sudengimo laikotarpiui, kuris priklauso PVM institucijai, kuri naudoja ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="71881-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="71881-113">Lauke **Ataskaitos kodas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="71881-113">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="71881-114">Lauke **Ataskaitos tekstas** įveskite aprašą, kuris bus rodomas ataskaitose.</span><span class="sxs-lookup"><span data-stu-id="71881-114">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="71881-115">Lauke **Trumpas aprašas**: įveskite aprašą vidiniam naudojimui.</span><span class="sxs-lookup"><span data-stu-id="71881-115">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="71881-116">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="71881-116">Click **Save**.</span></span>

