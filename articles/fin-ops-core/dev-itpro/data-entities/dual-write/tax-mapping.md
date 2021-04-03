---
title: Integruoti mokesčiai
description: Šioje temoje aprašomas mokesčių duomenų integravimas tarp „Finance and Operations“ ir „Dataverse“.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 7501ef21492a96c81b971e1d9077beaba9be897b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560342"
---
# <a name="integrated-tax"></a><span data-ttu-id="29d86-103">Integruoti mokesčiai</span><span class="sxs-lookup"><span data-stu-id="29d86-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="29d86-104">Mokesčių sąrankos duomenimis apibrėžiama tiek netiesioginių mokesčių (PVM, GST), tiek išskaitomo mokesčio sąranka.</span><span class="sxs-lookup"><span data-stu-id="29d86-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="29d86-105">Jais apibūdinama mokesčių skaičiavimo taisyklė, mokesčio tarifas, sudengimas ir kitos sąvokos.</span><span class="sxs-lookup"><span data-stu-id="29d86-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="29d86-106">Šablonai</span><span class="sxs-lookup"><span data-stu-id="29d86-106">Templates</span></span>

<span data-ttu-id="29d86-107">Mokesčių duomenis sudaro lentelių schemų, veikiančių kartu interaktyviai naudojant duomenis (kaip parodyta tolesnėje lentelėje) rinkinys.</span><span class="sxs-lookup"><span data-stu-id="29d86-107">Tax data includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="29d86-108">„Finance and Operations” programėlės</span><span class="sxs-lookup"><span data-stu-id="29d86-108">Finance and Operations apps</span></span> | <span data-ttu-id="29d86-109">Modeliu grįstos programos „Dynamics 365“</span><span class="sxs-lookup"><span data-stu-id="29d86-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="29d86-110">aprašymas</span><span class="sxs-lookup"><span data-stu-id="29d86-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="29d86-111">Prekės PVM grupė</span><span class="sxs-lookup"><span data-stu-id="29d86-111">Item sales tax group</span></span> | <span data-ttu-id="29d86-112">msdyn_mokesčiųprekiųgrupės</span><span class="sxs-lookup"><span data-stu-id="29d86-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="29d86-113">PVM rinkėjai</span><span class="sxs-lookup"><span data-stu-id="29d86-113">Sales tax authorities</span></span> | <span data-ttu-id="29d86-114">msdyn_mokesčiųinspekcijos</span><span class="sxs-lookup"><span data-stu-id="29d86-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="29d86-115">Atleidimo nuo PVM kodo objekto CDS</span><span class="sxs-lookup"><span data-stu-id="29d86-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="29d86-116">msdyn_mokesčiųlengvatųkodai</span><span class="sxs-lookup"><span data-stu-id="29d86-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="29d86-117">PVM grupės</span><span class="sxs-lookup"><span data-stu-id="29d86-117">Sales tax groups</span></span> | <span data-ttu-id="29d86-118">msdyn_mokesčiųgrupės</span><span class="sxs-lookup"><span data-stu-id="29d86-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="29d86-119">Didžiosios knygos PVM registravimo grupės V2</span><span class="sxs-lookup"><span data-stu-id="29d86-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="29d86-120">msdyn_mokesčiųregistravimogrupės</span><span class="sxs-lookup"><span data-stu-id="29d86-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="29d86-121">Išskaitomų mokesčių kodai</span><span class="sxs-lookup"><span data-stu-id="29d86-121">Withholding tax codes</span></span> | <span data-ttu-id="29d86-122">msdyn_atidedamųmokesčiųkodai</span><span class="sxs-lookup"><span data-stu-id="29d86-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="29d86-123">Išskaitomo mokesčio grupės</span><span class="sxs-lookup"><span data-stu-id="29d86-123">Withholding tax groups</span></span> | <span data-ttu-id="29d86-124">msdyn_atidedamųmokesčiųgrupės</span><span class="sxs-lookup"><span data-stu-id="29d86-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]