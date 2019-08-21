---
title: Nustatyti PVM grupes ir prekių PVM grupes
description: Šis užduoties įrašas apžvelgia grupių PVM ir Prekės PVM sąranką.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxGroup,  TaxItemGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c58755be2c927de1d308576a2bff2ed3340db34
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846276"
---
# <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><span data-ttu-id="4d5f2-103">Nustatyti PVM grupes ir prekių PVM grupes</span><span class="sxs-lookup"><span data-stu-id="4d5f2-103">Set up sales tax groups and item sales tax groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4d5f2-104">Šis užduoties įrašas apžvelgia grupių PVM ir Prekės PVM sąranką.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-104">This task recording walks you through the setup of Sales tax and Item sales tax groups.</span></span> <span data-ttu-id="4d5f2-105">PVM grupės yra PVM kodų, kurie pridėti prie klientų ir tiekėjų, grupės.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-105">Sales tax groups are groups of sales tax codes that are attached to customers and vendors.</span></span> <span data-ttu-id="4d5f2-106">Operacijose, kurios neregistruojamos konkrečiam tiekėjui ar klientui, PVM grupės taip pat pridedamos prie DK sąskaitų.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-106">They are also attached to ledger accounts for transactions that are not posted to a particular vendor or customer.</span></span>  <span data-ttu-id="4d5f2-107">Prekių PVM grupės yra PVM kodų, kurie pridėti prie išteklių, pvz., produktų, grupės.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-107">Item sales tax groups are groups of sales tax codes that are attached to resources like products.</span></span>  <span data-ttu-id="4d5f2-108">Konkrečiai operacijai taikomi PVM nustatomi pagal PVM kodus, kurie įtraukiami ir į operacijos PVM grupę, ir į prekės PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-108">The sales taxes that apply to a particular transaction are determined by the sales tax codes that are included both in the sales tax group and in the item sales tax group of the transaction.</span></span>  <span data-ttu-id="4d5f2-109">Apskaičiuoti PVM galima tik jei pasirinkta kiekvienos operacijos, kurios PVM reikia apskaičiuoti arba įrašyti, PVM grupė ir prekės PVM grupė.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-109">Sales tax can be calculated only if a sales tax group and an item sales tax group are selected for each transaction for which sales tax must be calculated or recorded.</span></span>  

1. <span data-ttu-id="4d5f2-110">Eikite į Mokestis > Netiesioginiai mokesčiai > PVM > PVM grupės.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-110">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="4d5f2-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-111">Click New.</span></span>
3. <span data-ttu-id="4d5f2-112">Lauke PVM grupė surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-112">In the Sales tax group field, type a value.</span></span>
4. <span data-ttu-id="4d5f2-113">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4d5f2-114">Perjunkite dalies Sąranka išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-114">Toggle the expansion of the Setup section.</span></span>
6. <span data-ttu-id="4d5f2-115">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-115">Click Add.</span></span>
7. <span data-ttu-id="4d5f2-116">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-116">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="4d5f2-117">Lauke PVM kodas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-117">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="4d5f2-118">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-118">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="4d5f2-119">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-119">Click Save.</span></span>
11. <span data-ttu-id="4d5f2-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-120">Close the page.</span></span>
12. <span data-ttu-id="4d5f2-121">Eikite į Mokestis > Netiesioginiai mokesčiai > PVM > Prekės PVM grupės.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-121">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
13. <span data-ttu-id="4d5f2-122">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-122">Click New.</span></span>
14. <span data-ttu-id="4d5f2-123">Lauke Prekių PVM grupė surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-123">In the Item sales tax group field, type a value.</span></span>
15. <span data-ttu-id="4d5f2-124">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-124">In the Description field, type a value.</span></span>
16. <span data-ttu-id="4d5f2-125">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-125">Click Add.</span></span>
17. <span data-ttu-id="4d5f2-126">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-126">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="4d5f2-127">Lauke PVM kodas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-127">In the Sales tax code field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="4d5f2-128">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-128">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="4d5f2-129">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="4d5f2-129">Click Save.</span></span>

