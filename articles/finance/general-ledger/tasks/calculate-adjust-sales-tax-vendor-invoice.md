---
title: PVM tiekėjo sąskaitoje faktūroje skaičiavimas ir koregavimas
description: Šioje temoje aiškinama, kaip koreguoti PVM tiekėjo SF, esančioje Dynamics 365 Finance.
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
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 03313d875d23489b3293376dd94f808c73a4bd15
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983554"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="249d4-103">PVM tiekėjo sąskaitoje faktūroje skaičiavimas ir koregavimas</span><span class="sxs-lookup"><span data-stu-id="249d4-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="249d4-104">Šioje temoje aiškinama, kaip koreguoti PVM tiekėjo SF.</span><span class="sxs-lookup"><span data-stu-id="249d4-104">This topic explains how to adjust sales tax on a vendor invoice.</span></span> <span data-ttu-id="249d4-105">Jei pradiniame šaltinio dokumente rodomos mokesčių sumos skiriasi nuo apskaičiuotų, šias sumas prieš registruodami galite koreguoti.</span><span class="sxs-lookup"><span data-stu-id="249d4-105">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="249d4-106">Šioje užduotyje naudojama demonstracinė įmonė DEMF.</span><span class="sxs-lookup"><span data-stu-id="249d4-106">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="249d4-107">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > SF > SF žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="249d4-107">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice journal**.</span></span>
2. <span data-ttu-id="249d4-108">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="249d4-108">Select **New**.</span></span>
3. <span data-ttu-id="249d4-109">Naujos eilutės lauke **Pavadinimas** pasirinkite išplečiamajame meniu esančią parinktį.</span><span class="sxs-lookup"><span data-stu-id="249d4-109">In the **Name** field of the new row, select an option in the drop-down menu.</span></span>
4. <span data-ttu-id="249d4-110">Veiksmų srityje pasirinkite **Eilutės**.</span><span class="sxs-lookup"><span data-stu-id="249d4-110">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="249d4-111">Lauke **Sąskaita**nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="249d4-111">In the **Account** field, specify the desired values.</span></span>
6. <span data-ttu-id="249d4-112">Lauke **Sąskaita faktūra** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="249d4-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="249d4-113">Lauke **Kreditas** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="249d4-113">In the **Credit** field, enter a number.</span></span>
8. <span data-ttu-id="249d4-114">Lauke **Korespondentinė sąskaita** nustatykite norimas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="249d4-114">In the **Offset account** field, specify the desired values.</span></span>
9. <span data-ttu-id="249d4-115">Pasirinkite **PVM**.</span><span class="sxs-lookup"><span data-stu-id="249d4-115">Select **Sales tax**.</span></span>
10. <span data-ttu-id="249d4-116">Lauke **Visa faktinė PVM suma** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="249d4-116">In the **Total actual sales tax amount** field, enter a number.</span></span>
11. <span data-ttu-id="249d4-117">Skirtuke **Koregavimas** PVM sumas galima koreguoti pagal PVM kodą.</span><span class="sxs-lookup"><span data-stu-id="249d4-117">On the **Adjustment** tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
12. <span data-ttu-id="249d4-118">Pasirinkite **Iš naujo nustatyti faktinius dydžius pagal apskaičiuotas sumas**.</span><span class="sxs-lookup"><span data-stu-id="249d4-118">Select **Reset actual from calculated amounts**.</span></span>
13. <span data-ttu-id="249d4-119">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="249d4-119">Select **OK**.</span></span>
14. <span data-ttu-id="249d4-120">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="249d4-120">Select **Save**.</span></span>

