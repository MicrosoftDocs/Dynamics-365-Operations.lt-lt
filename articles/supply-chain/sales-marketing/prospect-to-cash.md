---
title: "Potencialūs klientai ir grynieji pinigai"
description: "Temoje apžvelgiamas „Dynamics 365 for Finance and Operations, Enterprise edition“ ir „Dynamics 365 for Sales“ sprendimas Potencialūs klientai ir grynieji pinigai."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="e0f61-103">Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="e0f61-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e0f61-104">Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją [Duomenų integravimas](/common-data-service/entity-reference/dynamics-365-integration) ir „Common Data Service“ (CDS) sinchronizuojami duomenys „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ ir „Dynamics 365 for Sales“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="e0f61-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="e0f61-105">Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus ir funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ sąskaitų, kontaktų, produktų, pardavimo pasiūlymų, pardavimo užsakymų ir pardavimo sąskaitų faktūrų duomenų srautus.</span><span class="sxs-lookup"><span data-stu-id="e0f61-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="e0f61-106">Sukūrus duomenų srautą tarp „Finance and Operations“ ir „Sales“ galima vykdyti pardavimo ir rinkodaros veiklas sprendime „Sales“ bei tvarkyti užsakymų įvykdymą naudojant atsargų valdymo funkciją sprendime „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="e0f61-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="e0f61-107">Šiuo sprendimu integruojamos toliau nurodytos sritys.</span><span class="sxs-lookup"><span data-stu-id="e0f61-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="e0f61-108">„Sales“ sąskaitų tvarkymas ir sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="e0f61-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="e0f61-109">„Sales“ kontaktų tvarkymas ir sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="e0f61-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="e0f61-110">„Finance and Operations“ produktų tvarkymas ir sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="e0f61-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="e0f61-111">Pardavimo pasiūlymų kūrimas sprendime „Sales“ ir jų sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="e0f61-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="e0f61-112">Pardavimo užsakymų kūrimas sprendime „Finance and Operations“ ir jų sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="e0f61-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="e0f61-113">Pardavimo sąskaitų faktūrų kūrimas sprendime „Finance and Operations“ ir jų sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="e0f61-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="e0f61-114">Sprendimui „Dynamics 365 for Finance and Operations, Enterprise edition“ taikomi sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="e0f61-114">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="e0f61-115">Norėdami naudoti sprendimą Potencialūs klientai ir grynieji pinigai, turite įdiegti tolesnius elementus.</span><span class="sxs-lookup"><span data-stu-id="e0f61-115">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="e0f61-116">„Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.) su 8 platformos naujinimu (programa 7.2.11792.56024 su platforma 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="e0f61-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="e0f61-117">Dvi „Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. liepos mėn.) karštąsias pataisas.</span><span class="sxs-lookup"><span data-stu-id="e0f61-117">Two hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>

    -  <span data-ttu-id="e0f61-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – įdiegus šią karštąją pataisą, galima naudojant funkciją Duomenų integravimas „Finance and Operations“ pardavimo užsakymų eilutes sinchronizuoti su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="e0f61-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="e0f61-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – įdiegus šią karštąją pataisą, galima naudojant funkciją Duomenų integravimas „Finance and Operations“ pardavimo užsakymus sinchronizuoti su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="e0f61-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
    
<span data-ttu-id="e0f61-120">**Pastaba**. Turite įdiegti tik KB4036524, nes į įdiegtį įtraukti pakeitimai iš KB4036461.</span><span class="sxs-lookup"><span data-stu-id="e0f61-120">**Note**: You only need to install KB4036524 because the installation includes the changes from KB4036461.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="e0f61-121">Sprendimui „Dynamics 365 for Sales“ taikomi sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="e0f61-121">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="e0f61-122">Norėdami naudoti sprendimą Potencialūs klientai ir grynieji pinigai, turite įdiegti tolesnius elementus.</span><span class="sxs-lookup"><span data-stu-id="e0f61-122">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="e0f61-123">„Dynamics 365 for Sales“ versija 1612 (8.2.1.207) (DB 8.2.1.207) (internetinė versija) arba naujesnė versija.</span><span class="sxs-lookup"><span data-stu-id="e0f61-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or later.</span></span>
- <span data-ttu-id="e0f61-124">Sprendimui „Dynamics 365 for Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai versija 1.14.0.0 (v14) arba naujesnė.</span><span class="sxs-lookup"><span data-stu-id="e0f61-124">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e0f61-125">Sprendimui „Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai diegimas</span><span class="sxs-lookup"><span data-stu-id="e0f61-125">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="e0f61-126">Iš „CustomerSource“ atsisiųskite [Sprendimui „Dynamics 365 for Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai paketo ZIP failą](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash).</span><span class="sxs-lookup"><span data-stu-id="e0f61-126">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="e0f61-127">Įsitikinkite, kad ZIP failas yra atblokuotas, kad, diegdami sprendimo paketą, negautumėte klaidos pranešimo „Importavimo paketų nerasta“.</span><span class="sxs-lookup"><span data-stu-id="e0f61-127">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="e0f61-128">Norėdami atblokuoti failą, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e0f61-128">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="e0f61-129">ZIP failą spustelėkite dešiniuoju pelės mygtuku.</span><span class="sxs-lookup"><span data-stu-id="e0f61-129">Right-click the zip file.</span></span>
    -  <span data-ttu-id="e0f61-130">Pasirinkite **Ypatybės**, tada – **Atblokuoti**.</span><span class="sxs-lookup"><span data-stu-id="e0f61-130">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="e0f61-131">Išskleiskite ir paleiskite PackageDeployer.exe.</span><span class="sxs-lookup"><span data-stu-id="e0f61-131">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="e0f61-132">Savo „Sales“ egzemplioriuje įdiekite sprendimą Potencialūs klientai ir grynieji pinigai.</span><span class="sxs-lookup"><span data-stu-id="e0f61-132">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="e0f61-133">Pasirinkite visuotinio diegimo tipą **„Office 365“**.</span><span class="sxs-lookup"><span data-stu-id="e0f61-133">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="e0f61-134">Pasirinkite **Rodyti išplėstines parinktis**.</span><span class="sxs-lookup"><span data-stu-id="e0f61-134">Select **Show advanced**.</span></span>
    - <span data-ttu-id="e0f61-135">Norėdami greitai įdiegti, pasirinkite **regioną**.</span><span class="sxs-lookup"><span data-stu-id="e0f61-135">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="e0f61-136">Jei pasirenkate **Nežinau**, sistema ieško visų regionų ir įdiegti truks ilgiau.</span><span class="sxs-lookup"><span data-stu-id="e0f61-136">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="e0f61-137">Įveskite administratoriaus vartotojo, turinčio diegimo teises, **vartotojo vardą** ir **slaptažodį**.</span><span class="sxs-lookup"><span data-stu-id="e0f61-137">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

