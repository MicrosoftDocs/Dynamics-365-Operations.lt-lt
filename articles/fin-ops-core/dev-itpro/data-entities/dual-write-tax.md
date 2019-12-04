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
ms.openlocfilehash: b6be53e9a2065373ca37c2791568a8161823803f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772415"
---
## <a name="integrated-tax"></a><span data-ttu-id="c7ae7-103">Integruoti mokesčiai</span><span class="sxs-lookup"><span data-stu-id="c7ae7-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7ae7-104">Mokesčių sąrankos duomenimis apibrėžiama tiek netiesioginių mokesčių (PVM, GST), tiek išskaitomo mokesčio sąranka.</span><span class="sxs-lookup"><span data-stu-id="c7ae7-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="c7ae7-105">Jais apibūdinama mokesčių skaičiavimo taisyklė, mokesčio tarifas, sudengimas ir kitos sąvokos.</span><span class="sxs-lookup"><span data-stu-id="c7ae7-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="c7ae7-106">Šablonai</span><span class="sxs-lookup"><span data-stu-id="c7ae7-106">Templates</span></span>

<span data-ttu-id="c7ae7-107">Mokesčių duomenis sudaro objektų schemų, veikiančių kartu interaktyviai naudojant duomenis (kaip parodyta tolesnėje lentelėje) rinkinys.</span><span class="sxs-lookup"><span data-stu-id="c7ae7-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="c7ae7-108">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="c7ae7-108">Finance and Operations</span></span>   | <span data-ttu-id="c7ae7-109">„Customer Engagement“ programa</span><span class="sxs-lookup"><span data-stu-id="c7ae7-109">Customer Engagement application</span></span>
-------------------------|---------------------------------
<span data-ttu-id="c7ae7-110">Mokesčių kodai</span><span class="sxs-lookup"><span data-stu-id="c7ae7-110">Tax codes</span></span>                  | <span data-ttu-id="c7ae7-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="c7ae7-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="c7ae7-112">Mokesčių grupės</span><span class="sxs-lookup"><span data-stu-id="c7ae7-112">Tax groups</span></span>               | <span data-ttu-id="c7ae7-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="c7ae7-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="c7ae7-114">Mokesčių prekių grupės</span><span class="sxs-lookup"><span data-stu-id="c7ae7-114">Tax item groups</span></span>          | <span data-ttu-id="c7ae7-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="c7ae7-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="c7ae7-116">Mokesčių lengvatos</span><span class="sxs-lookup"><span data-stu-id="c7ae7-116">Tax Exemptions</span></span>           | <span data-ttu-id="c7ae7-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="c7ae7-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="c7ae7-118">Mokesčių institucijos</span><span class="sxs-lookup"><span data-stu-id="c7ae7-118">Tax Authorities</span></span>          | <span data-ttu-id="c7ae7-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="c7ae7-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="c7ae7-120">Išskaitomų mokesčių kodai</span><span class="sxs-lookup"><span data-stu-id="c7ae7-120">Withholding tax codes</span></span>      | <span data-ttu-id="c7ae7-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="c7ae7-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="c7ae7-122">Išskaitomo mokesčio grupės</span><span class="sxs-lookup"><span data-stu-id="c7ae7-122">Withholding tax groups</span></span>   | <span data-ttu-id="c7ae7-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="c7ae7-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="c7ae7-124">Mokesčių DK sąskaitų grupė</span><span class="sxs-lookup"><span data-stu-id="c7ae7-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="c7ae7-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="c7ae7-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

