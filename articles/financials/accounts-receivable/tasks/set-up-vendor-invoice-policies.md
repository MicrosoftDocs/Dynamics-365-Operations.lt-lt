---
title: Nustatyti tiekėjų SF strategijas
description: Tiekėjo SF strategijos vykdomos, kai registruojate tiekėjo SF naudodami puslapį Tiekėjo SF ir kai atidarote tiekėjo SF puslapį Strategijos pažeidimai.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b424eee7c91ef1085c98828c0d5e5cf674717a81
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "323185"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="bc7e3-103">Nustatyti tiekėjų SF strategijas</span><span class="sxs-lookup"><span data-stu-id="bc7e3-103">Set up vendor invoice policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bc7e3-104">Tiekėjo SF strategijos vykdomos, kai registruojate tiekėjo SF naudodami puslapį Tiekėjo SF ir kai atidarote tiekėjo SF puslapį Strategijos pažeidimai.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="bc7e3-105">Taip pat galite sukonfigūruoti, kad tiekėjo SF darbo eiga vykdytų tiekėjo SF strategijas kiekvieną kartą, kai į darbo eigą pateikiate SF.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="bc7e3-106">Tiekėjo SF strategijos netaikomos SF, kurios sukurtos SF registre ar SF žurnale.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="bc7e3-107">SF gretinimo tikrinimo metu tiekėjo SF strategijos nenaudojamos – jis nustatomas puslapyje Mokėtinų sumų parametrai.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="bc7e3-108">Šiame įraše naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="bc7e3-109">Šiuos veiksmus paprastai atlieka mokėtinų sumų vadovo arba apskaitos vadovo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="bc7e3-110">Prieš pradėdami įsitikinkite, kad pasirinktas SF gretinimo konfigūracijos raktas.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="bc7e3-111">Pasiruošti kurti tiekėjo SF strategijas</span><span class="sxs-lookup"><span data-stu-id="bc7e3-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="bc7e3-112">Pasirinkite Mokėtinos sumos > Sąranka > Mokėtinų sumų parametrai.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="bc7e3-113">Spustelėkite skirtuką SF tikrinimas.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="bc7e3-114">Pažymėkite arba atžymėkite žymės langelį Automatiškai atnaujinti sąskaitos faktūros antraštės būseną.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="bc7e3-115">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-115">Click OK.</span></span>
5. <span data-ttu-id="bc7e3-116">Lauke Registruoti SF su nesutapimais pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="bc7e3-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-117">Close the page.</span></span>
7. <span data-ttu-id="bc7e3-118">Pasirinkite Mokėtinos sumos > Strategijos nustatymas > Tiekėjo SF strategijos.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="bc7e3-119">Spustelėkite Parametrai.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-119">Click Parameters.</span></span>
9. <span data-ttu-id="bc7e3-120">Spustelėkite btnAdd.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-120">Click btnAdd.</span></span>
10. <span data-ttu-id="bc7e3-121">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="bc7e3-122">Kurti tiekėjo SF strategijos taisyklių tipus</span><span class="sxs-lookup"><span data-stu-id="bc7e3-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="bc7e3-123">Pasirinkite Mokėtinos sumos > Strategijos nustatymas > Tiekėjo SF strategijos taisyklių tipai.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="bc7e3-124">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-124">Click New.</span></span>
3. <span data-ttu-id="bc7e3-125">Lauke Taisyklės pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="bc7e3-126">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bc7e3-127">Lauke Užklausos pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="bc7e3-128">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="bc7e3-129">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="bc7e3-130">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-130">Click Save.</span></span>
9. <span data-ttu-id="bc7e3-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="bc7e3-132">Apibrėžti tiekėjo SF strategiją</span><span class="sxs-lookup"><span data-stu-id="bc7e3-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="bc7e3-133">Pasirinkite Mokėtinos sumos > Strategijos nustatymas > Tiekėjo SF strategijos.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="bc7e3-134">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-134">Click New.</span></span>
3. <span data-ttu-id="bc7e3-135">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="bc7e3-136">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bc7e3-137">Išplėskite arba sutraukite dalį Strategijos organizacijos.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="bc7e3-138">Medyje pasirinkite „Contoso Entertainment System USA‟.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="bc7e3-139">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-139">Click Add.</span></span>
8. <span data-ttu-id="bc7e3-140">Išplėskite arba sutraukite dalį Strategijos taisyklės.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="bc7e3-141">Spustelėkite Kurti strategijos taisyklę.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="bc7e3-142">Lauke Strategijos taisyklės aprašas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="bc7e3-143">Spustelėkite Filtras.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-143">Click Filter.</span></span>
12. <span data-ttu-id="bc7e3-144">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-144">Click Add.</span></span>
13. <span data-ttu-id="bc7e3-145">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="bc7e3-146">Lauke Lentelė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="bc7e3-147">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="bc7e3-148">Lauke Išvestinė lentelė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="bc7e3-149">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="bc7e3-150">Lauke Laukas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="bc7e3-151">Lauke Laukas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="bc7e3-152">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-152">Close the page.</span></span>
21. <span data-ttu-id="bc7e3-153">Lauke Kriterijai surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="bc7e3-154">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-154">Click OK.</span></span>
23. <span data-ttu-id="bc7e3-155">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-155">Click OK.</span></span>
24. <span data-ttu-id="bc7e3-156">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-156">Close the page.</span></span>
25. <span data-ttu-id="bc7e3-157">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bc7e3-157">Close the page.</span></span>

