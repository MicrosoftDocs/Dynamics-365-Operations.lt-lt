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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be24e18da63d1a613c3c6e72f7c767c7af9b6656
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222148"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="29ec6-103">Nustatyti PVM ataskaitų kodus</span><span class="sxs-lookup"><span data-stu-id="29ec6-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="29ec6-104">PVM ataskaitų kodai – tai lauko numeris PVM ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="29ec6-104">The Sales tax reporting codes refer to a field number that's listed on a sales tax report.</span></span> <span data-ttu-id="29ec6-105">Jie naudojami konkrečių šalių ataskaitų maketuose.</span><span class="sxs-lookup"><span data-stu-id="29ec6-105">They are used on country-specific report layouts.</span></span> <span data-ttu-id="29ec6-106">Taip pat jie naudojami mokant PVM pagal kodo ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="29ec6-106">They're also used on the Sales tax payment by code report.</span></span> <span data-ttu-id="29ec6-107">Ataskaitoje rodomos kiekvieno ataskaitos kodo sudengimo laikotarpio PVM sumos.</span><span class="sxs-lookup"><span data-stu-id="29ec6-107">That report shows sales tax amounts for a settlement period summarized for each reporting code.</span></span> <span data-ttu-id="29ec6-108">Sukūrus PVM ataskaitų kodus, galima į juos nurodyti „FastTab‟ Ataskaitų sąranka, esančiuose puslapyje **PVM kodas**.</span><span class="sxs-lookup"><span data-stu-id="29ec6-108">After you create Sales tax reporting codes, you can refer to those codes on the Report setup FastTabs, which you can access from the **Sales tax code** page.</span></span> 

<span data-ttu-id="29ec6-109">Šiame įraše naudojama demonstracinė įmonė DEMF.</span><span class="sxs-lookup"><span data-stu-id="29ec6-109">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="29ec6-110">**Naršymo srityje** eikite į **Mokestis > Sąranka > PVM > PVM ataskaitų kodai**.</span><span class="sxs-lookup"><span data-stu-id="29ec6-110">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="29ec6-111">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="29ec6-111">Click **New**.</span></span>
3. <span data-ttu-id="29ec6-112">Pasirinkite ataskaitos maketą, kuriam priklauso ataskaitos kodas.</span><span class="sxs-lookup"><span data-stu-id="29ec6-112">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="29ec6-113">Šis maketas naudojamas filtruoti galimiems ataskaitų PVM kodams.</span><span class="sxs-lookup"><span data-stu-id="29ec6-113">This layout is used to filter the available reporting codes for a sales tax code.</span></span> <span data-ttu-id="29ec6-114">Kiekvienas PVM kodas priklauso sudengimo laikotarpiui, kuris priklauso PVM institucijai, kuri naudoja ataskaitos maketą.</span><span class="sxs-lookup"><span data-stu-id="29ec6-114">Each sales tax code belongs to a settlement period, which belongs to a Sales tax authority, which uses a report layout.</span></span>  
4. <span data-ttu-id="29ec6-115">Lauke **Ataskaitos kodas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="29ec6-115">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="29ec6-116">Lauke **Ataskaitos tekstas** įveskite aprašą, kuris bus rodomas ataskaitose.</span><span class="sxs-lookup"><span data-stu-id="29ec6-116">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="29ec6-117">Lauke **Trumpas aprašas**: įveskite aprašą vidiniam naudojimui.</span><span class="sxs-lookup"><span data-stu-id="29ec6-117">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="29ec6-118">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="29ec6-118">Click **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]