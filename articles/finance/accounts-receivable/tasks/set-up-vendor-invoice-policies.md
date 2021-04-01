---
title: Tiekėjų sąskaitų faktūrų strategijų nustatymas
description: Šioje temoje paaiškinama, kaip nustatyti tiekėjų SF strategijas.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 678ef8f0b7df00aec615af26cbcadec984331060
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220064"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="2b991-103">Tiekėjų sąskaitų faktūrų strategijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="2b991-103">Set up vendor invoice policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b991-104">Šioje temoje paaiškinama, kaip nustatyti tiekėjų SF strategijas.</span><span class="sxs-lookup"><span data-stu-id="2b991-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="2b991-105">Tiekėjo SF strategijos vykdomos, kai registruojate tiekėjo SF naudodami puslapį Tiekėjo SF ir kai atidarote tiekėjo SF puslapį Strategijos pažeidimai.</span><span class="sxs-lookup"><span data-stu-id="2b991-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="2b991-106">Taip pat galite sukonfigūruoti, kad tiekėjo SF darbo eiga vykdytų tiekėjo SF strategijas kiekvieną kartą, kai į darbo eigą pateikiate SF.</span><span class="sxs-lookup"><span data-stu-id="2b991-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="2b991-107">Tiekėjo SF strategijos netaikomos SF, kurios sukurtos SF registre ar SF žurnale.</span><span class="sxs-lookup"><span data-stu-id="2b991-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="2b991-108">SF gretinimo tikrinimo metu tiekėjo SF strategijos nenaudojamos – jis nustatomas puslapyje Mokėtinų sumų parametrai.</span><span class="sxs-lookup"><span data-stu-id="2b991-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="2b991-109">Šiame įraše naudojama demonstracinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="2b991-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="2b991-110">Šiuos veiksmus paprastai atlieka mokėtinų sumų vadovo arba apskaitos vadovo vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="2b991-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="2b991-111">Prieš pradėdami įsitikinkite, kad pasirinktas SF gretinimo konfigūracijos raktas.</span><span class="sxs-lookup"><span data-stu-id="2b991-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="2b991-112">Pasiruošti kurti tiekėjo SF strategijas</span><span class="sxs-lookup"><span data-stu-id="2b991-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="2b991-113">Pasirinkite **Naršymo sritis > Moduliai > Mokėtinos sumos > Sąranka > Mokėtinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="2b991-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="2b991-114">Pasirinkite skirtuką **SF tikrinimas.**.</span><span class="sxs-lookup"><span data-stu-id="2b991-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="2b991-115">Pažymėkite arba atžymėkite žymės langelio būseną **Automatiškai atnaujinti sąskaitos faktūros antraštę**.</span><span class="sxs-lookup"><span data-stu-id="2b991-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="2b991-116">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2b991-116">Select **OK**.</span></span>
5. <span data-ttu-id="2b991-117">Lauke **Registruoti SF su nesutapimais** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="2b991-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="2b991-118">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2b991-118">Close the page.</span></span>
7. <span data-ttu-id="2b991-119">Eikite į **Naršymo sritis > Moduliai > Mokėtinos sumos > Strategijos nustatymas > Tiekėjo SF strategijos**.</span><span class="sxs-lookup"><span data-stu-id="2b991-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="2b991-120">Pasirinkite **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="2b991-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="2b991-121">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="2b991-121">Select **Add**.</span></span>
10. <span data-ttu-id="2b991-122">Norėdami grįžti į neregistruotų tabelių puslapį, uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2b991-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="2b991-123">Kurti tiekėjo SF strategijos taisyklių tipus</span><span class="sxs-lookup"><span data-stu-id="2b991-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="2b991-124">Eikite į **Naršymo sritis > Moduliai > Mokėtinos sumos > Strategijos nustatymas > Tiekėjo SF strategijos**.</span><span class="sxs-lookup"><span data-stu-id="2b991-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="2b991-125">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="2b991-125">Select **New**.</span></span>
3. <span data-ttu-id="2b991-126">Įveskite reikšmes laukuose **Taisyklės vardas** ir **Aprašas**.</span><span class="sxs-lookup"><span data-stu-id="2b991-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="2b991-127">Laukelyje **Užklausos pavadinimas** pasirinkite išskleidžiamąjį mygtuką, kad atidarytumėte peržvalgą. Tada pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="2b991-127">In the **Query name** field, select the drop-down button to open the lookup, then select the desired record.</span></span>
5. <span data-ttu-id="2b991-128">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2b991-128">Select **Save**.</span></span>
6. <span data-ttu-id="2b991-129">Norėdami grįžti į neregistruotų tabelių puslapį, uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2b991-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="2b991-130">Apibrėžti tiekėjo SF strategiją</span><span class="sxs-lookup"><span data-stu-id="2b991-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="2b991-131">Eikite į **Valdymo skiltis > Moduliai > Mokėtinos sumos > Strategijos nustatymas > Tiekėjo SF strategijos**.</span><span class="sxs-lookup"><span data-stu-id="2b991-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="2b991-132">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="2b991-132">Select **New**.</span></span>
3. <span data-ttu-id="2b991-133">Įveskite reikšmes laukuose **Profilis** ir **Aprašas**.</span><span class="sxs-lookup"><span data-stu-id="2b991-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="2b991-134">Išplėskite arba sutraukite sekciją **Strategijos organizacijos**.</span><span class="sxs-lookup"><span data-stu-id="2b991-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="2b991-135">Medyje pasirinkite **„Contoso“ pramogų sistema (JAV)**.</span><span class="sxs-lookup"><span data-stu-id="2b991-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="2b991-136">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="2b991-136">Select **Add**.</span></span>
7. <span data-ttu-id="2b991-137">Išplėskite arba sutraukite sekciją **Strategijos taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="2b991-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="2b991-138">Pasirinkite **Kurti strategijos taisyklę**.</span><span class="sxs-lookup"><span data-stu-id="2b991-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="2b991-139">Lauke **Strategijos taisyklės aprašas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2b991-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="2b991-140">Pasirinkite **Filtras**.</span><span class="sxs-lookup"><span data-stu-id="2b991-140">Select **Filter**.</span></span>
11. <span data-ttu-id="2b991-141">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="2b991-141">Select **Add**.</span></span> <span data-ttu-id="2b991-142">Pasirinkti aktyvų įrašą</span><span class="sxs-lookup"><span data-stu-id="2b991-142">Select the desired record.</span></span>
12. <span data-ttu-id="2b991-143">Laukuose **Lentelė**,**Išvestinė lentelė** ir **Laukas** pasirinkite arba įveskite parinktis iš išplečiamojo meniu.</span><span class="sxs-lookup"><span data-stu-id="2b991-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="2b991-144">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2b991-144">Close the page.</span></span>
14. <span data-ttu-id="2b991-145">Lauke **Kriterijai** surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2b991-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="2b991-146">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2b991-146">Select **OK**.</span></span>
16. <span data-ttu-id="2b991-147">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2b991-147">Select **OK**.</span></span>
17. <span data-ttu-id="2b991-148">Norėdami grįžti į neregistruotų tabelių puslapį, uždarykite puslapius.</span><span class="sxs-lookup"><span data-stu-id="2b991-148">Close the pages to return to the home page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]