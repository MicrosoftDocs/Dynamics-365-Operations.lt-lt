---
title: Nustatyti PVM ataskaitų kodus
description: PVM ataskaitų kodai – tai lauko numeris PVM ataskaitoje.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 830a3465944b32cc17feee60e3cbc5ad0a4dc9d7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834780"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="fc686-103">Nustatyti PVM ataskaitų kodus</span><span class="sxs-lookup"><span data-stu-id="fc686-103">Set up sales tax reporting codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc686-104">PVM ataskaitų kodai – tai lauko numeris PVM ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="fc686-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="fc686-105">Jie naudojami konkrečios šalies ataskaitų maketuose ir PVM mokėjimo pagal kodą ataskaitoje spausdinti PVM sumoms už sudengimo laikotarpį, susumuotą pagal ataskaitos kodą.</span><span class="sxs-lookup"><span data-stu-id="fc686-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="fc686-106">Sukūrus PVM ataskaitų kodus, galima į juos nurodyti „FastTab‟ Ataskaitų sąranka, esančiuose puslapyje PVM kodas.</span><span class="sxs-lookup"><span data-stu-id="fc686-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="fc686-107">Šiame įraše naudojama demonstracinė įmonė DEMF.</span><span class="sxs-lookup"><span data-stu-id="fc686-107">This recording uses the DEMF demo company.</span></span>



1. <span data-ttu-id="fc686-108">Eikite į Mokestis > Sąranka > PVM > PVM ataskaitų kodai.</span><span class="sxs-lookup"><span data-stu-id="fc686-108">Go to Tax > Setup > Sales tax > Sales tax reporting codes.</span></span>
2. <span data-ttu-id="fc686-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="fc686-109">Click New.</span></span>
3. <span data-ttu-id="fc686-110">Pasirinkite ataskaitos maketą, kuriam priklauso ataskaitos kodas.</span><span class="sxs-lookup"><span data-stu-id="fc686-110">Select the report layout that the reporting code belongs to.</span></span>
    * <span data-ttu-id="fc686-111">Šis maketas naudojamas filtruoti galimiems ataskaitų PVM kodams.</span><span class="sxs-lookup"><span data-stu-id="fc686-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="fc686-112">Kiekvienas PVM kodas priklauso sudengimo laikotarpiui, kuris priklauso PVM institucijai, kuri naudoja ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="fc686-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="fc686-113">Įveskite numerį, kuris nurodo į lauką, esantį PVM ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="fc686-113">Enter a number that refers to a field on a sales tax report.</span></span>
5. <span data-ttu-id="fc686-114">Lauke Ataskaitos tekstas įveskite aprašą, rodytiną ataskaitose.</span><span class="sxs-lookup"><span data-stu-id="fc686-114">In the Report text field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="fc686-115">Lauke Trumpas aprašas įveskite aprašą, skirtą vidiniams tikslams.</span><span class="sxs-lookup"><span data-stu-id="fc686-115">In the Brief description field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="fc686-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="fc686-116">Click Save.</span></span>

