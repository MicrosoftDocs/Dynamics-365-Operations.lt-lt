---
title: "Standartinių savikainų įkainojimo versijų apribojimai"
description: "Šioje temoje aprašomi apribojimai, taikomi standartinių savikainų įkainojimo versijai."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e14d5d11e987d2dbc841f86c39fc7e94864144d3
ms.openlocfilehash: 658575492597eed91509561f4710f07e271c53c8
ms.contentlocale: lt-lt
ms.lasthandoff: 01/17/2018

---


#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="0249f-103">Standartinių savikainų įkainojimo versijų apribojimai</span><span class="sxs-lookup"><span data-stu-id="0249f-103">Restrictions on costing versions for standard costs</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0249f-104">Šioje temoje aprašomi apribojimai, taikomi standartinių savikainų įkainojimo versijai.</span><span class="sxs-lookup"><span data-stu-id="0249f-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="0249f-105">Tolesni apribojimai padeda užtikrinti griežtą standartinių įkainojimo principų laikymąsi.</span><span class="sxs-lookup"><span data-stu-id="0249f-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="0249f-106">Išlaidos turi būti įtrauktos į prekės savikainą.</span><span class="sxs-lookup"><span data-stu-id="0249f-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="0249f-107">Pagamintos prekės išlaidos nurodo komplektavimo specifikacijos (KS) ir maršruto informacijos amortizuotas pastovias išlaidas.</span><span class="sxs-lookup"><span data-stu-id="0249f-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="0249f-108">Todėl išlaidos turi būti įtrauktos į vieneto savikainą.</span><span class="sxs-lookup"><span data-stu-id="0249f-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="0249f-109">Nupirktos prekės išlaidos taip pat įtrauktos į prekės vieneto savikainą.</span><span class="sxs-lookup"><span data-stu-id="0249f-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="0249f-110">Pagamintų prekių standartinių išlaidų skaičiavimas turi būti pagrįstas standartinių išlaidų įkainojimo versijos išlaidų įrašais.</span><span class="sxs-lookup"><span data-stu-id="0249f-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="0249f-111">Alternatyvūs išlaidų duomenų šaltiniai gali būti naudojami tik su planuojamų išlaidų įkainojimo versija, pvz., nupirktų prekių pirkimo kainų prekybos sutartimis.</span><span class="sxs-lookup"><span data-stu-id="0249f-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="0249f-112">Alternatyvius išlaidų duomenų šaltinius nustato KS skaičiavimo grupė.</span><span class="sxs-lookup"><span data-stu-id="0249f-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="0249f-113">KS skaičiavimai turi būti atliekami vieno lygio išskleidimo režimu.</span><span class="sxs-lookup"><span data-stu-id="0249f-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="0249f-114">Prekės standartinių išlaidų duomenys gali būti kopijuojami į kitą įkainojimo versiją, į kurią įtrauktos standartinės išlaidos arba planuojamos išlaidos.</span><span class="sxs-lookup"><span data-stu-id="0249f-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="0249f-115">Tačiau prekės planuojamų išlaidų duomenys negali būti kopijuojami į išlaidų versiją, į kurią įtrauktos standartinės savikainos, nes anksčiau šioje temoje išvardyti apribojimai netaikomi planuojamoms išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="0249f-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="0249f-116">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="0249f-116">Related topics</span></span>
--------

[<span data-ttu-id="0249f-117">Įkainojimo versijos</span><span class="sxs-lookup"><span data-stu-id="0249f-117">Costing versions</span></span>](costing-versions.md)

[<span data-ttu-id="0249f-118">Standartinių išlaidų atnaujinimas ne gamybos aplinkoje</span><span class="sxs-lookup"><span data-stu-id="0249f-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="0249f-119">Pagamintų prekių standartinių savikainų paruošimas priežiūrai</span><span class="sxs-lookup"><span data-stu-id="0249f-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)


