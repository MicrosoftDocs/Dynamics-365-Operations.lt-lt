---
title: Skaičiuoti ir koreguoti PVM tiekėjo SF
description: Jei pradiniame šaltinio dokumente rodomos mokesčių sumos skiriasi nuo apskaičiuotų, šias sumas prieš registruodami galite koreguoti.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 803c038d907b68a3c72a83a3e035c4e08b8a8661
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545176"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="ccbf3-103">Skaičiuoti ir koreguoti PVM tiekėjo SF</span><span class="sxs-lookup"><span data-stu-id="ccbf3-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ccbf3-104">Jei pradiniame šaltinio dokumente rodomos mokesčių sumos skiriasi nuo apskaičiuotų, šias sumas prieš registruodami galite koreguoti.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-104">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="ccbf3-105">Šioje užduotyje naudojama demonstracinė įmonė DEMF.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-105">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="ccbf3-106">Eikite į Mokėtinos sumos > Sąskaitos faktūros > SF žurnalas.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-106">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="ccbf3-107">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-107">Click New.</span></span>
3. <span data-ttu-id="ccbf3-108">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ccbf3-109">Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-109">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ccbf3-110">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-110">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ccbf3-111">Spustelėkite Eilutės.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-111">Click Lines.</span></span>
7. <span data-ttu-id="ccbf3-112">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="ccbf3-113">Lauke Sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-113">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="ccbf3-114">Lauke Sąskaita faktūra surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-114">In the Invoice field, type a value.</span></span>
10. <span data-ttu-id="ccbf3-115">Lauke Kreditas įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-115">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="ccbf3-116">Lauke Korespondentinė sąskaita nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-116">In the Offset account field, specify the desired values.</span></span>
12. <span data-ttu-id="ccbf3-117">Spustelėkite PVM.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-117">Click Sales tax.</span></span>
13. <span data-ttu-id="ccbf3-118">Lauke Visa faktinė PVM suma įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-118">In the Total actual sales tax amount field, enter a number.</span></span>
14. <span data-ttu-id="ccbf3-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-119">Click OK.</span></span>
15. <span data-ttu-id="ccbf3-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-120">Click Save.</span></span>
16. <span data-ttu-id="ccbf3-121">Spustelėkite PVM.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-121">Click Sales tax.</span></span>
17. <span data-ttu-id="ccbf3-122">Skirtuke Koregavimas PVM sumas galima koreguoti pagal PVM kodą.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-122">On the Adjustment tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
18. <span data-ttu-id="ccbf3-123">Spustelėkite Iš naujo nustatyti faktinius dydžius pagal apskaičiuotas sumas.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-123">Click Reset actual from calculated amounts.</span></span>
19. <span data-ttu-id="ccbf3-124">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-124">Click OK.</span></span>
20. <span data-ttu-id="ccbf3-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ccbf3-125">Click Save.</span></span>

