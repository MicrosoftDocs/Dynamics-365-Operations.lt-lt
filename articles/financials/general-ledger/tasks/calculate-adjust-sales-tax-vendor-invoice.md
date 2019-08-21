---
title: PVM tiekėjo sąskaitoje faktūroje skaičiavimas ir koregavimas
description: Šioje temoje aiškinama, kaip koreguoti PVM tiekėjo SF, esančioje Dynamics 365 for Finance and Operations.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 684529087d5348c9e02310f812f8aa6f64c6655f
ms.sourcegitcommit: 016832198c306e8329ad21b5254e7d1cdff74c2f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862619"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="06c27-103">PVM tiekėjo sąskaitoje faktūroje skaičiavimas ir koregavimas</span><span class="sxs-lookup"><span data-stu-id="06c27-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="06c27-104">Šioje temoje aiškinama, kaip koreguoti PVM tiekėjo SF, esančioje Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="06c27-104">This topic explains how to adjust sales tax on a vendor invoice in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="06c27-105">Jei pradiniame šaltinio dokumente rodomos mokesčių sumos skiriasi nuo apskaičiuotų, šias sumas prieš registruodami galite koreguoti.</span><span class="sxs-lookup"><span data-stu-id="06c27-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="06c27-106">Šioje užduotyje naudojama demonstracinė įmonė DEMF.</span><span class="sxs-lookup"><span data-stu-id="06c27-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="06c27-107">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > SF > SF žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="06c27-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="06c27-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="06c27-108">Select **New**.</span></span>
3. <span data-ttu-id="06c27-109">Naujos eilutės lauke **Pavadinimas** pasirinkite išplečiamajame meniu esančią parinktį.</span><span class="sxs-lookup"><span data-stu-id="06c27-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="06c27-110">Veiksmų srityje pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="06c27-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="06c27-111">Lauke **Sąskaita**nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="06c27-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="06c27-112">Lauke **Sąskaita faktūra** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="06c27-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="06c27-113">Lauke **Credit** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="06c27-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="06c27-114">Lauke **Offset account** nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="06c27-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="06c27-115">Pasirinkite **PVM**.</span><span class="sxs-lookup"><span data-stu-id="06c27-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="06c27-116">Lauke **Visa faktinė PVM suma** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="06c27-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="06c27-117">Skirtuke **Koregavimas** PVM sumas galima koreguoti pagal PVM kodą.</span><span class="sxs-lookup"><span data-stu-id="06c27-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="06c27-118">Pasirinkite **Iš naujo nustatyti faktinius dydžius pagal apskaičiuotas sumas**.</span><span class="sxs-lookup"><span data-stu-id="06c27-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="06c27-119">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="06c27-119">Select **OK**.</span></span>
14. <span data-ttu-id="06c27-120">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="06c27-120">Select **Save**.</span></span>

