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
ms.openlocfilehash: 0d32a5f7859f0200da823a73d94b9a6b2a9c8e7d
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019916"
---
# <a name="integrated-tax"></a><span data-ttu-id="e72b3-103">Integruoti mokesčiai</span><span class="sxs-lookup"><span data-stu-id="e72b3-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="e72b3-104">Mokesčių sąrankos duomenimis apibrėžiama tiek netiesioginių mokesčių (PVM, GST), tiek išskaitomo mokesčio sąranka.</span><span class="sxs-lookup"><span data-stu-id="e72b3-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="e72b3-105">Jais apibūdinama mokesčių skaičiavimo taisyklė, mokesčio tarifas, sudengimas ir kitos sąvokos.</span><span class="sxs-lookup"><span data-stu-id="e72b3-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="e72b3-106">Šablonai</span><span class="sxs-lookup"><span data-stu-id="e72b3-106">Templates</span></span>

<span data-ttu-id="e72b3-107">Mokesčių duomenis sudaro objektų schemų, veikiančių kartu interaktyviai naudojant duomenis (kaip parodyta tolesnėje lentelėje) rinkinys.</span><span class="sxs-lookup"><span data-stu-id="e72b3-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="e72b3-108">„Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="e72b3-108">Finance and Operations</span></span>   | <span data-ttu-id="e72b3-109">Kitos „Dynamics 365” programos</span><span class="sxs-lookup"><span data-stu-id="e72b3-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="e72b3-110">Mokesčių kodai</span><span class="sxs-lookup"><span data-stu-id="e72b3-110">Tax codes</span></span>                  | <span data-ttu-id="e72b3-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="e72b3-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="e72b3-112">Mokesčių grupės</span><span class="sxs-lookup"><span data-stu-id="e72b3-112">Tax groups</span></span>               | <span data-ttu-id="e72b3-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="e72b3-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="e72b3-114">Mokesčių prekių grupės</span><span class="sxs-lookup"><span data-stu-id="e72b3-114">Tax item groups</span></span>          | <span data-ttu-id="e72b3-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="e72b3-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="e72b3-116">Mokesčių lengvatos</span><span class="sxs-lookup"><span data-stu-id="e72b3-116">Tax Exemptions</span></span>           | <span data-ttu-id="e72b3-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="e72b3-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="e72b3-118">Mokesčių institucijos</span><span class="sxs-lookup"><span data-stu-id="e72b3-118">Tax Authorities</span></span>          | <span data-ttu-id="e72b3-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="e72b3-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="e72b3-120">Išskaitomų mokesčių kodai</span><span class="sxs-lookup"><span data-stu-id="e72b3-120">Withholding tax codes</span></span>      | <span data-ttu-id="e72b3-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="e72b3-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="e72b3-122">Išskaitomo mokesčio grupės</span><span class="sxs-lookup"><span data-stu-id="e72b3-122">Withholding tax groups</span></span>   | <span data-ttu-id="e72b3-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="e72b3-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="e72b3-124">Mokesčių DK sąskaitų grupė</span><span class="sxs-lookup"><span data-stu-id="e72b3-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="e72b3-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="e72b3-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

