---
title: "Potencialūs klientai ir grynieji pinigai"
description: "Temoje apžvelgiamas „Dynamics 365 for Finance and Operations, Enterprise edition“ ir „Dynamics 365 for Sales“ sprendimas Potencialūs klientai ir grynieji pinigai."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 2accf77c5241adff7ad1648737dde451153fde46
ms.contentlocale: lt-lt
ms.lasthandoff: 11/14/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="73e0d-103">Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="73e0d-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="73e0d-104">Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją [Duomenų integravimas](/common-data-service/entity-reference/dynamics-365-integration) ir „Common Data Service“ (CDS) sinchronizuojami duomenys „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ ir „Dynamics 365 for Sales“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="73e0d-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="73e0d-105">Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus ir funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ sąskaitų, kontaktų, produktų, pardavimo pasiūlymų, pardavimo užsakymų ir pardavimo sąskaitų faktūrų duomenų srautus.</span><span class="sxs-lookup"><span data-stu-id="73e0d-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="73e0d-106">Sukūrus duomenų srautą tarp „Finance and Operations“ ir „Sales“ galima vykdyti pardavimo ir rinkodaros veiklas sprendime „Sales“ bei tvarkyti užsakymų įvykdymą naudojant atsargų valdymo funkciją sprendime „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="73e0d-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="73e0d-107">Šiuo sprendimu integruojamos toliau nurodytos sritys.</span><span class="sxs-lookup"><span data-stu-id="73e0d-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="73e0d-108">„Sales“ sąskaitų tvarkymas ir sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="73e0d-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="73e0d-109">„Sales“ kontaktų tvarkymas ir sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="73e0d-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="73e0d-110">„Finance and Operations“ produktų tvarkymas ir sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="73e0d-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="73e0d-111">Pardavimo pasiūlymų kūrimas sprendime „Sales“ ir jų sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="73e0d-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="73e0d-112">Pardavimo užsakymų kūrimas sprendime „Finance and Operations“ ir jų sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="73e0d-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="73e0d-113">Pardavimo sąskaitų faktūrų kūrimas sprendime „Finance and Operations“ ir jų sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="73e0d-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

<span data-ttu-id="73e0d-114">Šiuo sprendimu tiesiogiai sinchronizuojamos toliau nurodytos sritys.</span><span class="sxs-lookup"><span data-stu-id="73e0d-114">This solution provides direct synchronization in the following areas:</span></span>

-   [<span data-ttu-id="73e0d-115">„Sales“ sąskaitų tvarkymas ir tiesioginis „Sales“ sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="73e0d-115">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
-   [<span data-ttu-id="73e0d-116">„Finance and Operations“ produktų tvarkymas ir tiesioginis sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="73e0d-116">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
-   [<span data-ttu-id="73e0d-117">„Sales“ kontaktų tvarkymas ir tiesioginis sinchronizavimas su „Finance and Operations“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="73e0d-117">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
-   [<span data-ttu-id="73e0d-118">„Sales“ pardavimo pasiūlymų antraščių ir eilučių tiesioginis sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="73e0d-118">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
-   [<span data-ttu-id="73e0d-119">Pardavimo užsakymų kūrimas sprendime „Finance and Operations“ ir jų tiesioginis sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="73e0d-119">Create sales orders in Finance and Operations and sync them directly to Sales</span></span>](sales-order-template-mapping-direct.md)
-  [<span data-ttu-id="73e0d-120">„Finance and Operations“ pardavimo užsakymo antraščių ir eilučių tiesioginis sinchronizavimas tarp „Sales“ ir „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="73e0d-120">Synchronize sales order headers and lines directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-between-sales-fin.md)
-   [<span data-ttu-id="73e0d-121">Pardavimo užsakymų tiesioginis sinchronizavimas tarp „Sales“ ir „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="73e0d-121">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
-   [<span data-ttu-id="73e0d-122">Pardavimo sąskaitų faktūrų kūrimas sprendime „Finance and Operations“ ir jų tiesioginis sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="73e0d-122">Create sales invoices in Finance and Operations and sync them directly to Sales</span></span>](sales-invoice-template-mapping-direct.md)


## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="73e0d-123">Sprendimui „Dynamics 365 for Finance and Operations, Enterprise edition“ taikomi sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="73e0d-123">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="73e0d-124">Norėdami naudoti sprendimą Potencialūs klientai ir grynieji pinigai, turite įdiegti tolesnius elementus.</span><span class="sxs-lookup"><span data-stu-id="73e0d-124">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="73e0d-125">„Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.) su 8 platformos naujinimu (programa 7.2.11792.56024 su platforma 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="73e0d-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="73e0d-126">„Dynamics 365 for Finance and Operations“ „Enterprise“ leidimo (2017 m. liepos mėn.) karštąsias pataisas.</span><span class="sxs-lookup"><span data-stu-id="73e0d-126">Hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>
        
    -  <span data-ttu-id="73e0d-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) – įdiegus šią karštąją pataisą ir naudojant funkciją Duomenų integravimas „Sales“ ir pardavimo užsakymų sinchronizavimas su „Finance and Operations“, teikiamas šios funkcijos palaikymas, taip pat įgalinama daugelis kitų patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="73e0d-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) - This hotfix enabels support for sales order synchronization with the Data Integration feature from Sales to Finance and Operations, along with a number of other enhancements.</span></span>

    -  <span data-ttu-id="73e0d-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – įdiegus šią karštąją pataisą, galima naudojant funkciją Duomenų integravimas „Finance and Operations“ pardavimo užsakymų eilutes sinchronizuoti su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="73e0d-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="73e0d-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – įdiegus šią karštąją pataisą, galima naudojant funkciją Duomenų integravimas „Finance and Operations“ pardavimo užsakymus sinchronizuoti su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="73e0d-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>

<span data-ttu-id="73e0d-130">**Pastaba**. Turite įdiegti tik KB4045570, nes į įdiegtį įtraukti kitų KB pakeitimai.</span><span class="sxs-lookup"><span data-stu-id="73e0d-130">**Note**: You only need to install KB4045570 because the installation includes the changes from the other KB's.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="73e0d-131">Sprendimui „Dynamics 365 for Sales“ taikomi sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="73e0d-131">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="73e0d-132">Norėdami naudoti sprendimą Potencialūs klientai ir grynieji pinigai, turite įdiegti tolesnius elementus.</span><span class="sxs-lookup"><span data-stu-id="73e0d-132">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="73e0d-133">„Dynamics 365 for Sales“ versija 1612 (8.2.1.207) (DB 8.2.1.207) (internetinė versija).</span><span class="sxs-lookup"><span data-stu-id="73e0d-133">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online.</span></span>
- <span data-ttu-id="73e0d-134">Sprendimui „Dynamics 365 for Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai versija 1.14.0.0 (v14) arba naujesnė.</span><span class="sxs-lookup"><span data-stu-id="73e0d-134">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="73e0d-135">Sprendimui „Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai diegimas</span><span class="sxs-lookup"><span data-stu-id="73e0d-135">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="73e0d-136">Iš „CustomerSource“ atsisiųskite [Sprendimui „Dynamics 365 for Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai paketo ZIP failą](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash).</span><span class="sxs-lookup"><span data-stu-id="73e0d-136">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="73e0d-137">Įsitikinkite, kad ZIP failas yra atblokuotas, kad, diegdami sprendimo paketą, negautumėte klaidos pranešimo „Importavimo paketų nerasta“.</span><span class="sxs-lookup"><span data-stu-id="73e0d-137">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="73e0d-138">Norėdami atblokuoti failą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="73e0d-138">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="73e0d-139">ZIP failą spustelėkite dešiniuoju pelės mygtuku.</span><span class="sxs-lookup"><span data-stu-id="73e0d-139">Right-click the zip file.</span></span>
    -  <span data-ttu-id="73e0d-140">Pasirinkite **Ypatybės**, tada – **Atblokuoti**.</span><span class="sxs-lookup"><span data-stu-id="73e0d-140">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="73e0d-141">Išskleiskite ir paleiskite PackageDeployer.exe.</span><span class="sxs-lookup"><span data-stu-id="73e0d-141">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="73e0d-142">Savo „Sales“ egzemplioriuje įdiekite sprendimą Potencialūs klientai ir grynieji pinigai.</span><span class="sxs-lookup"><span data-stu-id="73e0d-142">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="73e0d-143">Pasirinkite visuotinio diegimo tipą **„Office 365“**.</span><span class="sxs-lookup"><span data-stu-id="73e0d-143">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="73e0d-144">Pasirinkite **Rodyti išplėstines parinktis**.</span><span class="sxs-lookup"><span data-stu-id="73e0d-144">Select **Show advanced**.</span></span>
    - <span data-ttu-id="73e0d-145">Norėdami greitai įdiegti, pasirinkite **regioną**.</span><span class="sxs-lookup"><span data-stu-id="73e0d-145">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="73e0d-146">Jei pasirenkate **Nežinau**, sistema ieško visų regionų ir įdiegti truks ilgiau.</span><span class="sxs-lookup"><span data-stu-id="73e0d-146">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="73e0d-147">Įveskite administratoriaus vartotojo, turinčio diegimo teises, **vartotojo vardą** ir **slaptažodį**.</span><span class="sxs-lookup"><span data-stu-id="73e0d-147">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

