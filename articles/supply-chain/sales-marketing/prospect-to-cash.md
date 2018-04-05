---
title: "Potencialūs klientai ir grynieji pinigai"
description: "Šioje temoje apžvelgiamas „Microsoft Dynamics 365 for Finance and Operations“ ir „Microsoft Dynamics 365 for Sales“ sprendimas Potencialūs klientai ir grynieji pinigai."
author: ChristianRytt
manager: AnnBe
ms.date: 02/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 025be8b44726194e6fc219816c40d2a15a7349df
ms.contentlocale: lt-lt
ms.lasthandoff: 03/26/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="adda0-103">Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="adda0-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="adda0-104">Sprendimas Potencialūs klientai ir grynieji pinigai leidžia tiesiogiai sinchronizuoti „Dynamics 365 for Finance and Operations“ su „Dynamics 365 for Sales“.</span><span class="sxs-lookup"><span data-stu-id="adda0-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="adda0-105">Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ sąskaitų, kontaktų, produktų, pardavimo pasiūlymų, pardavimo užsakymų ir pardavimo sąskaitų faktūrų duomenų srautus.</span><span class="sxs-lookup"><span data-stu-id="adda0-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="adda0-106">Sukūrus duomenų srautą tarp „Finance and Operations“ ir „Sales“ galima vykdyti pardavimo ir rinkodaros veiklas sprendime „Sales“ bei tvarkyti užsakymų įvykdymą naudojant atsargų valdymo funkciją sprendime „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="adda0-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="adda0-107">Norėdami apie sprendimo Potencialūs klientai ir grynieji pinigai integravimą gauti daugiau informacijos, peržiūrėkite trumpą „YouTube“ vaizdo įrašą:</span><span class="sxs-lookup"><span data-stu-id="adda0-107">For more information about the Prospect to cash integration, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

<span data-ttu-id="adda0-108">Dabartinėje versijoje sprendimas Potencialūs klientai ir grynieji pinigai leidžia šių tipų tiesioginį sinchronizavimą:</span><span class="sxs-lookup"><span data-stu-id="adda0-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="adda0-109">„Sales“ sąskaitų tvarkymas ir tiesioginis „Sales“ sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="adda0-109">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="adda0-110">„Finance and Operations“ produktų tvarkymas ir tiesioginis sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="adda0-110">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="adda0-111">„Sales“ kontaktų tvarkymas ir tiesioginis sinchronizavimas su „Finance and Operations“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="adda0-111">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="adda0-112">Tiesioginis „Sales“ pardavimo pasiūlymų sinchronizavimas iš „Sales“ į „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="adda0-112">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="adda0-113">Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="adda0-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="adda0-114">Tiesioginis pardavimo sąskaitos faktūros sinchronizavimas iš „Finance and Operations“ į „Sales“</span><span class="sxs-lookup"><span data-stu-id="adda0-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="adda0-115">„Finance and Operations“ sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="adda0-115">System requirements for Finance and Operations</span></span>

<span data-ttu-id="adda0-116">Sprendimo Potencialūs klientai ir grynieji pinigai integravimo funkcija palaikoma tolesnėse versijose.</span><span class="sxs-lookup"><span data-stu-id="adda0-116">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="adda0-117">„Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3“ (2017 m. gruodžio mėn.)</span><span class="sxs-lookup"><span data-stu-id="adda0-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="adda0-118">„Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. gruodžio mėn.) – programos komponavimo versija 7.3.11971.56116 su 12 platformos naujinimu (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="adda0-118">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="adda0-119">„Dynamics 365 for Finance and Operations, Enterprise Edition“ (2017 m. liepos mėn.)</span><span class="sxs-lookup"><span data-stu-id="adda0-119">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="adda0-120">„Dynamics 365 for Finance and Operations Enterprise Edition“ (2017 m. liepos mėn.) – su 8 platformos naujinimu (programos komponavimo versija 7.2.11792.56024, platformos komponavimo versija 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="adda0-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="adda0-121">Būtinos toliau nurodytos karštosios pataisos.</span><span class="sxs-lookup"><span data-stu-id="adda0-121">The following hotfixes are required:</span></span>

    - <span data-ttu-id="adda0-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – įdiegus šias karštąsias pataisas, naudojant funkciją Duomenų integravimas galima „Sales“ pardavimo užsakymus sinchronizuoti su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="adda0-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="adda0-123">Jos taip pat suteikia kelis kitus patobulinimus.</span><span class="sxs-lookup"><span data-stu-id="adda0-123">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="adda0-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – įdiegus šias karštąsias pataisas, naudojant funkciją Duomenų integravimas galima „Finance and Operations“ pardavimo užsakymų eilutes sinchronizuoti su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="adda0-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="adda0-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – įdiegus šias karštąsias pataisas, naudojant funkciją Duomenų integravimas galima „Finance and Operations“ pardavimo užsakymus sinchronizuoti su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="adda0-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="adda0-126">Turite įdiegti tik KB4045570, nes į įdiegtį įtraukti kitų karštųjų pataisų pakeitimai.</span><span class="sxs-lookup"><span data-stu-id="adda0-126">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="adda0-127">„Dynamics 365 for Finance and Operations‟ 1611 versija (2016 m. lapkričio mėn.)</span><span class="sxs-lookup"><span data-stu-id="adda0-127">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="adda0-128">„Dynamics 365 for Finance and Operations“ 1611 versija (2016 m. lapkričio mėn.) su 8 arba naujesniu platformos naujinimu</span><span class="sxs-lookup"><span data-stu-id="adda0-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="adda0-129">Būtinos toliau nurodytos karštosios pataisos.</span><span class="sxs-lookup"><span data-stu-id="adda0-129">The following hotfixes are required:</span></span>

    - <span data-ttu-id="adda0-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** – įgalina naudojant funkciją Duomenų integravimas „Finance and Operations“ pardavimo užsakymų sinchronizavimą su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="adda0-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
    - <span data-ttu-id="adda0-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** – įgalina naudojant funkciją Duomenų integravimas „Finance and Operations“ pardavimo užsakymo antraščių ir eilučių sinchronizavimą su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="adda0-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
    - <span data-ttu-id="adda0-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** – reikalingas potencialių klientų ir grynųjų pinigų integravimo naudojant duomenų objektus palaikymas.</span><span class="sxs-lookup"><span data-stu-id="adda0-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="adda0-133">Įdiegę karštąsias pataisas, turite paleisti paketinę užduotį formoje **SalesPopulateProspectToCash**.</span><span class="sxs-lookup"><span data-stu-id="adda0-133">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="adda0-134">Ši forma paslėpta, nes jos jums reikia tik kartą.</span><span class="sxs-lookup"><span data-stu-id="adda0-134">This form is hidden because you only need it once.</span></span> <span data-ttu-id="adda0-135">Norėdami atidaryti formą, prisijunkite prie aplinkos ir prie naršyklės adreso pridėkite šį URL: &mi=action:SalesPopulateProspectToCash, pvz., `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="adda0-135">To access the form, log in to the environment and add the following to the URL in your browser address: &mi=action:SalesPopulateProspectToCash, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="adda0-136">Atsidarius formai spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="adda0-136">When the form opens, click OK.</span></span> <span data-ttu-id="adda0-137">Į naują lauką **LineCreationSequnceNumber** lentelėse **SalesLine**, **SalesQuotationLine** ir **CustInvoiceTrans** bus automatiškai įvestos unikalios reikšmės ir atnaujintas produktų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="adda0-137">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="adda0-138">Tai yra būtina, veiktų potencialių klientų ir grynųjų pinigų integravimas.</span><span class="sxs-lookup"><span data-stu-id="adda0-138">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="adda0-139">„Sales“ sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="adda0-139">System requirements for Sales</span></span>

<span data-ttu-id="adda0-140">Norėdami naudoti sprendimą Potencialūs klientai ir grynieji pinigai, turite įdiegti šiuos komponentus:</span><span class="sxs-lookup"><span data-stu-id="adda0-140">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="adda0-141">„Dynamics 365 for Sales“ versija 1612 (8.2.1.207) (DB 8.2.1.207) (internetinė versija) arba naujesnė versija</span><span class="sxs-lookup"><span data-stu-id="adda0-141">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="adda0-142">Sprendimui „Dynamics 365 for Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai versija 1.15.0.0 (v15)</span><span class="sxs-lookup"><span data-stu-id="adda0-142">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="adda0-143">Sprendimui „Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai diegimas</span><span class="sxs-lookup"><span data-stu-id="adda0-143">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="adda0-144">Iš „CustomerSource“ atsisiųskite [Sprendimui „Dynamics 365 for Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai paketo ZIP failą](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash).</span><span class="sxs-lookup"><span data-stu-id="adda0-144">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="adda0-145">Užtikrinkite, kad ZIP failas atblokuotas.</span><span class="sxs-lookup"><span data-stu-id="adda0-145">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="adda0-146">Priešingu atveju, kai bandysite įdiegti sprendimo paketą, galite gauti tokį klaidos pranešimą: „Nerasta jokių importavimo paketų“.</span><span class="sxs-lookup"><span data-stu-id="adda0-146">Otherwise, when you try to install the solution package, you may receive the following error message, "No import packages were found."</span></span> <span data-ttu-id="adda0-147">Norėdami atblokuoti ZIP failą, spustelėkite jį dešiniuoju pelės mygtuku ir pasirinkite **Ypatybės**.</span><span class="sxs-lookup"><span data-stu-id="adda0-147">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="adda0-148">Pasirinkite **Atblokuoti**.</span><span class="sxs-lookup"><span data-stu-id="adda0-148">Select **Unblock**.</span></span>
3. <span data-ttu-id="adda0-149">Išskleiskite ir paleiskite **PackageDeployer.exe**.</span><span class="sxs-lookup"><span data-stu-id="adda0-149">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="adda0-150">Savo „Sales“ egzemplioriuje įdiekite sprendimą Potencialūs klientai ir grynieji pinigai:</span><span class="sxs-lookup"><span data-stu-id="adda0-150">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="adda0-151">Pasirinkite **„Office 365“** kaip visuotinio diegimo tipą.</span><span class="sxs-lookup"><span data-stu-id="adda0-151">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="adda0-152">Pasirinkite **Rodyti išplėstines parinktis**.</span><span class="sxs-lookup"><span data-stu-id="adda0-152">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="adda0-153">Norėdami greitai įdiegti, pasirinkite regioną.</span><span class="sxs-lookup"><span data-stu-id="adda0-153">For a quick installation, select a region.</span></span> <span data-ttu-id="adda0-154">Jei pasirenkate **Nežinau**, sistema ieško visų regionų ir diegimas trunka ilgiau.</span><span class="sxs-lookup"><span data-stu-id="adda0-154">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="adda0-155">Įveskite administratoriaus vartotojo, turinčio diegimo teises, vartotojo vardą ir slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="adda0-155">Enter the user name and password of an admin user who has installation rights.</span></span>



