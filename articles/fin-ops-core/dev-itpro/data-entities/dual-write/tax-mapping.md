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
ms.openlocfilehash: 69521ec8c664a7025050c94105eca58f7f2c5c00
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435565"
---
# <a name="integrated-tax"></a><span data-ttu-id="0b755-103">Integruoti mokesčiai</span><span class="sxs-lookup"><span data-stu-id="0b755-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="0b755-104">Mokesčių sąrankos duomenimis apibrėžiama tiek netiesioginių mokesčių (PVM, GST), tiek išskaitomo mokesčio sąranka.</span><span class="sxs-lookup"><span data-stu-id="0b755-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="0b755-105">Jais apibūdinama mokesčių skaičiavimo taisyklė, mokesčio tarifas, sudengimas ir kitos sąvokos.</span><span class="sxs-lookup"><span data-stu-id="0b755-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="0b755-106">Šablonai</span><span class="sxs-lookup"><span data-stu-id="0b755-106">Templates</span></span>

<span data-ttu-id="0b755-107">Mokesčių duomenis sudaro objektų schemų, veikiančių kartu interaktyviai naudojant duomenis (kaip parodyta tolesnėje lentelėje) rinkinys.</span><span class="sxs-lookup"><span data-stu-id="0b755-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="0b755-108">„Finance and Operations” programėlės</span><span class="sxs-lookup"><span data-stu-id="0b755-108">Finance and Operations apps</span></span> | <span data-ttu-id="0b755-109">Modeliu grįstos programos „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="0b755-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="0b755-110">aprašymas</span><span class="sxs-lookup"><span data-stu-id="0b755-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="0b755-111">Prekės PVM grupė</span><span class="sxs-lookup"><span data-stu-id="0b755-111">Item sales tax group</span></span> | <span data-ttu-id="0b755-112">msdyn_mokesčiųprekiųgrupės</span><span class="sxs-lookup"><span data-stu-id="0b755-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="0b755-113">PVM rinkėjai</span><span class="sxs-lookup"><span data-stu-id="0b755-113">Sales tax authorities</span></span> | <span data-ttu-id="0b755-114">msdyn_mokesčiųinspekcijos</span><span class="sxs-lookup"><span data-stu-id="0b755-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="0b755-115">Atleidimo nuo PVM kodo objekto CDS</span><span class="sxs-lookup"><span data-stu-id="0b755-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="0b755-116">msdyn_mokesčiųlengvatųkodai</span><span class="sxs-lookup"><span data-stu-id="0b755-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="0b755-117">PVM grupės</span><span class="sxs-lookup"><span data-stu-id="0b755-117">Sales tax groups</span></span> | <span data-ttu-id="0b755-118">msdyn_mokesčiųgrupės</span><span class="sxs-lookup"><span data-stu-id="0b755-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="0b755-119">Didžiosios knygos PVM registravimo grupės V2</span><span class="sxs-lookup"><span data-stu-id="0b755-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="0b755-120">msdyn_mokesčiųregistravimogrupės</span><span class="sxs-lookup"><span data-stu-id="0b755-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="0b755-121">Išskaitomų mokesčių kodai</span><span class="sxs-lookup"><span data-stu-id="0b755-121">Withholding tax codes</span></span> | <span data-ttu-id="0b755-122">msdyn_atidedamųmokesčiųkodai</span><span class="sxs-lookup"><span data-stu-id="0b755-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="0b755-123">Išskaitomo mokesčio grupės</span><span class="sxs-lookup"><span data-stu-id="0b755-123">Withholding tax groups</span></span> | <span data-ttu-id="0b755-124">msdyn_atidedamųmokesčiųgrupės</span><span class="sxs-lookup"><span data-stu-id="0b755-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

