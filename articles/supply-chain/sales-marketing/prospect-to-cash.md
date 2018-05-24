---
title: "Potencialūs klientai ir grynieji pinigai"
description: "Šioje temoje apžvelgiamas „Microsoft Dynamics 365 for Finance and Operations“ ir „Microsoft Dynamics 365 for Sales“ sprendimas Potencialūs klientai ir grynieji pinigai."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f43b3943ce27c44cc0b4756d1d5f23e3be093273
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="1c3c2-103">Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="1c3c2-103">Prospect to cash</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c3c2-104">Sprendimas Potencialūs klientai ir grynieji pinigai leidžia tiesiogiai sinchronizuoti „Dynamics 365 for Finance and Operations“ su „Dynamics 365 for Sales“.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="1c3c2-105">Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ sąskaitų, kontaktų, produktų, pardavimo pasiūlymų, pardavimo užsakymų ir pardavimo sąskaitų faktūrų duomenų srautus.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="1c3c2-106">Sukūrus duomenų srautą tarp „Finance and Operations“ ir „Sales“ galima vykdyti pardavimo ir rinkodaros veiklas sprendime „Sales“ bei tvarkyti užsakymų įvykdymą naudojant atsargų valdymo funkciją sprendime „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="1c3c2-107">Norėdami apie sprendimo Potencialūs klientai ir grynieji pinigai integravimą gauti daugiau informacijos, peržiūrėkite trumpą „YouTube“ vaizdo įrašą:</span><span class="sxs-lookup"><span data-stu-id="1c3c2-107">For more information about the Prospect to cash integration, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

[<span data-ttu-id="1c3c2-108">Potencialių klientų ir grynųjų pinigų integravimas („YouTube“ vaizdo įrašas)</span><span class="sxs-lookup"><span data-stu-id="1c3c2-108">Prospect to cash integration (YouTube video)</span></span>](https://youtu.be/AVV9x5x-XCg) 

<span data-ttu-id="1c3c2-109">Dabartinėje versijoje sprendimas Potencialūs klientai ir grynieji pinigai leidžia šių tipų tiesioginį sinchronizavimą:</span><span class="sxs-lookup"><span data-stu-id="1c3c2-109">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="1c3c2-110">„Sales“ sąskaitų tvarkymas ir tiesioginis „Sales“ sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="1c3c2-110">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="1c3c2-111">„Finance and Operations“ produktų tvarkymas ir tiesioginis sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="1c3c2-111">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="1c3c2-112">„Sales“ kontaktų tvarkymas ir tiesioginis sinchronizavimas su „Finance and Operations“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="1c3c2-112">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="1c3c2-113">Tiesioginis „Sales“ pardavimo pasiūlymų sinchronizavimas iš „Sales“ į „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="1c3c2-113">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="1c3c2-114">Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="1c3c2-114">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="1c3c2-115">Tiesioginis pardavimo sąskaitos faktūros sinchronizavimas iš „Finance and Operations“ į „Sales“</span><span class="sxs-lookup"><span data-stu-id="1c3c2-115">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="1c3c2-116">„Finance and Operations“ sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="1c3c2-116">System requirements for Finance and Operations</span></span>
<span data-ttu-id="1c3c2-117">Sprendimo Potencialūs klientai ir grynieji pinigai integravimo funkcija palaikoma tolesnėse versijose.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-117">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="1c3c2-118">„Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3“ (2017 m. gruodžio mėn.)</span><span class="sxs-lookup"><span data-stu-id="1c3c2-118">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="1c3c2-119">„Dynamics 365 for Finance and Operations, Enterprise edition“ (2017 m. gruodžio mėn.) – programos komponavimo versija 7.3.11971.56116 su 12 platformos naujinimu (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="1c3c2-119">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="1c3c2-120">„Dynamics 365 for Finance and Operations, Enterprise Edition“ (2017 m. liepos mėn.)</span><span class="sxs-lookup"><span data-stu-id="1c3c2-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="1c3c2-121">„Dynamics 365 for Finance and Operations Enterprise Edition“ (2017 m. liepos mėn.) – su 8 platformos naujinimu (programos komponavimo versija 7.2.11792.56024, platformos komponavimo versija 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="1c3c2-121">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="1c3c2-122">Būtinos toliau nurodytos karštosios pataisos.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-122">The following hotfixes are required:</span></span>

  - <span data-ttu-id="1c3c2-123">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – įdiegus šias karštąsias pataisas, naudojant funkciją Duomenų integravimas galima „Sales“ pardavimo užsakymus sinchronizuoti su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-123">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="1c3c2-124">Jos taip pat suteikia kelis kitus patobulinimus.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-124">It also provides several other enhancements.</span></span>
  - <span data-ttu-id="1c3c2-125">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – įdiegus šias karštąsias pataisas, naudojant funkciją Duomenų integravimas galima „Finance and Operations“ pardavimo užsakymų eilutes sinchronizuoti su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-125">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
  - <span data-ttu-id="1c3c2-126">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – įdiegus šias karštąsias pataisas, naudojant funkciją Duomenų integravimas galima „Finance and Operations“ pardavimo užsakymus sinchronizuoti su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-126">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1c3c2-127">Turite įdiegti tik KB4045570, nes į įdiegtį įtraukti kitų karštųjų pataisų pakeitimai.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-127">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="1c3c2-128">„Dynamics 365 for Finance and Operations‟ 1611 versija (2016 m. lapkričio mėn.)</span><span class="sxs-lookup"><span data-stu-id="1c3c2-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="1c3c2-129">„Dynamics 365 for Finance and Operations“ 1611 versija (2016 m. lapkričio mėn.) su 8 arba naujesniu platformos naujinimu</span><span class="sxs-lookup"><span data-stu-id="1c3c2-129">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="1c3c2-130">Būtinos toliau nurodytos karštosios pataisos.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-130">The following hotfixes are required:</span></span>

  - <span data-ttu-id="1c3c2-131">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** – įgalina naudojant funkciją Duomenų integravimas „Finance and Operations“ pardavimo užsakymų sinchronizavimą su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-131">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
  - <span data-ttu-id="1c3c2-132">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** – įgalina naudojant funkciją Duomenų integravimas „Finance and Operations“ pardavimo užsakymo antraščių ir eilučių sinchronizavimą su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-132">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
  - <span data-ttu-id="1c3c2-133">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** – reikalingas potencialių klientų ir grynųjų pinigų integravimo naudojant duomenų objektus palaikymas.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-133">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="1c3c2-134">Įdiegę karštąsias pataisas, turite paleisti paketinę užduotį formoje **SalesPopulateProspectToCash**.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-134">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="1c3c2-135">Ši forma paslėpta, nes jos jums reikia tik kartą.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-135">This form is hidden because you only need it once.</span></span> <span data-ttu-id="1c3c2-136">Norėdami atidaryti formą, prisijunkite prie aplinkos ir prie naršyklės adreso pridėkite šį URL: *&mi=action:SalesPopulateProspectToCash*, pvz., `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-136">To access the form, log in to the environment and add the following to the URL in your browser address: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="1c3c2-137">Atsidarius formai spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-137">When the form opens, click OK.</span></span> <span data-ttu-id="1c3c2-138">Į naują lauką **LineCreationSequnceNumber** lentelėse **SalesLine**, **SalesQuotationLine** ir **CustInvoiceTrans** bus automatiškai įvestos unikalios reikšmės ir atnaujintas produktų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-138">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="1c3c2-139">Tai yra būtina, veiktų potencialių klientų ir grynųjų pinigų integravimas.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-139">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="1c3c2-140">„Sales“ sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="1c3c2-140">System requirements for Sales</span></span>

<span data-ttu-id="1c3c2-141">Norėdami naudoti sprendimą Potencialūs klientai ir grynieji pinigai, turite įdiegti šiuos komponentus:</span><span class="sxs-lookup"><span data-stu-id="1c3c2-141">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="1c3c2-142">„Dynamics 365 for Sales“ versija 1612 (8.2.1.207) (DB 8.2.1.207) (internetinė versija) arba naujesnė versija</span><span class="sxs-lookup"><span data-stu-id="1c3c2-142">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="1c3c2-143">Sprendimui „Dynamics 365 for Sales“ skirto sprendimo Potencialūs klientai ir grynieji pinigai 1.15.0.0 arba naujesnė versija.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-143">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 or a later version.</span></span> <span data-ttu-id="1c3c2-144">Sprendimą galima atsisiųsti iš „AppSource“.</span><span class="sxs-lookup"><span data-stu-id="1c3c2-144">The solution is available for download from AppSource.</span></span> <span data-ttu-id="1c3c2-145">[„Dynamics 365“ sprendimo Potencialaus kliento pavertimo pinigais atsisiuntimas](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="1c3c2-145">[Download Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>

