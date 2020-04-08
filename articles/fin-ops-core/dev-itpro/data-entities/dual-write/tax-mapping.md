---
title: Integruoti mokesčiai
description: Šioje temoje aprašomas mokesčių duomenų integravimas tarp „Finance and Operations“ ir „Common Data Service“.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a4da37d45698290b40f6c72148f1500bef72127a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173090"
---
# <a name="integrated-tax"></a><span data-ttu-id="b2af5-103">Integruoti mokesčiai</span><span class="sxs-lookup"><span data-stu-id="b2af5-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="b2af5-104">Mokesčių sąrankos duomenimis apibrėžiama tiek netiesioginių mokesčių (PVM, GST), tiek išskaitomo mokesčio sąranka.</span><span class="sxs-lookup"><span data-stu-id="b2af5-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="b2af5-105">Jais apibūdinama mokesčių skaičiavimo taisyklė, mokesčio tarifas, sudengimas ir kitos sąvokos.</span><span class="sxs-lookup"><span data-stu-id="b2af5-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="b2af5-106">Šablonai</span><span class="sxs-lookup"><span data-stu-id="b2af5-106">Templates</span></span>

<span data-ttu-id="b2af5-107">Mokesčių duomenis sudaro objektų schemų, veikiančių kartu interaktyviai naudojant duomenis (kaip parodyta tolesnėje lentelėje) rinkinys.</span><span class="sxs-lookup"><span data-stu-id="b2af5-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="b2af5-108">„Finance and Operations” programėlės</span><span class="sxs-lookup"><span data-stu-id="b2af5-108">Finance and Operations apps</span></span> | <span data-ttu-id="b2af5-109">Modeliu grįstos programos „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="b2af5-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="b2af5-110">aprašymas</span><span class="sxs-lookup"><span data-stu-id="b2af5-110">Description</span></span> |
-------------------------|---------------------------------
<span data-ttu-id="b2af5-111">Mokesčių kodai</span><span class="sxs-lookup"><span data-stu-id="b2af5-111">Tax codes</span></span>                   | <span data-ttu-id="b2af5-112">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="b2af5-112">msdyn\_taxcodes.md</span></span> | 
<span data-ttu-id="b2af5-113">Mokesčių grupės</span><span class="sxs-lookup"><span data-stu-id="b2af5-113">Tax groups</span></span>                 | <span data-ttu-id="b2af5-114">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="b2af5-114">msdyn\_taxgroups.md</span></span> | 
<span data-ttu-id="b2af5-115">Mokesčių prekių grupės</span><span class="sxs-lookup"><span data-stu-id="b2af5-115">Tax item groups</span></span>             | <span data-ttu-id="b2af5-116">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="b2af5-116">msdyn\_taxitemgroups.md</span></span> | 
<span data-ttu-id="b2af5-117">Mokesčių lengvatos</span><span class="sxs-lookup"><span data-stu-id="b2af5-117">Tax Exemptions</span></span>             | <span data-ttu-id="b2af5-118">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="b2af5-118">msdyn\_taxexemptcodes.md</span></span> | 
<span data-ttu-id="b2af5-119">Mokesčių institucijos</span><span class="sxs-lookup"><span data-stu-id="b2af5-119">Tax Authorities</span></span>             | <span data-ttu-id="b2af5-120">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="b2af5-120">msdyn\_taxauthorities.md</span></span> | 
<span data-ttu-id="b2af5-121">Išskaitomų mokesčių kodai</span><span class="sxs-lookup"><span data-stu-id="b2af5-121">Withholding tax codes</span></span>       | <span data-ttu-id="b2af5-122">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="b2af5-122">msdyn\_withholdingtaxcodes.md</span></span> | 
<span data-ttu-id="b2af5-123">Išskaitomo mokesčio grupės</span><span class="sxs-lookup"><span data-stu-id="b2af5-123">Withholding tax groups</span></span>     | <span data-ttu-id="b2af5-124">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="b2af5-124">msdyn\_withholdingtaxgroups.md</span></span> | 
<span data-ttu-id="b2af5-125">Mokesčių DK sąskaitų grupė</span><span class="sxs-lookup"><span data-stu-id="b2af5-125">Tax Ledger Account Group</span></span> | <span data-ttu-id="b2af5-126">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="b2af5-126">msdyn\_taxpostinggroups</span></span>     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

