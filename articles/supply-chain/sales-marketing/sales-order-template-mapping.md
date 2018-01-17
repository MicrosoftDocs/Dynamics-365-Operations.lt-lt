---
title: "Sinchronizuoti „Finance and Operations“ pardavimo užsakymo antraštes ir eilutes su „Sales“"
description: "Temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ pardavimo užsakymų antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Sales“."
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: d7e4c435a3344f6a5d66e1889b633d80cda085eb
ms.contentlocale: lt-lt
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="681e2-103">Sinchronizuoti „Finance and Operations“ pardavimo užsakymo antraštes ir eilutes su „Sales“</span><span class="sxs-lookup"><span data-stu-id="681e2-103">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="681e2-104">Temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ pardavimo užsakymų antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Sales“.</span><span class="sxs-lookup"><span data-stu-id="681e2-104">The topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="681e2-105">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="681e2-105">Template and tasks</span></span>

<span data-ttu-id="681e2-106">Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami sinchronizuojant „Finance and Operations“ pardavimo užsakymų antraštes ir eilutes su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="681e2-106">The following templates and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="681e2-107">**Šablono pavadinimas naudojant funkciją Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="681e2-107">**Name of template in Data integration**</span></span> 

    - <span data-ttu-id="681e2-108">Pardavimo užsakymai (iš „Finance and Operations“ į „Sales“)</span><span class="sxs-lookup"><span data-stu-id="681e2-108">Sales Orders (Fin and Ops to Sales)</span></span>
    
- <span data-ttu-id="681e2-109">**Užduočių pavadinimai projekte Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="681e2-109">**Names of tasks in Data integration project**</span></span>

    - <span data-ttu-id="681e2-110">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="681e2-110">OrderHeader</span></span>
    - <span data-ttu-id="681e2-111">OrderLine</span><span class="sxs-lookup"><span data-stu-id="681e2-111">OrderLine</span></span>

<span data-ttu-id="681e2-112">Reikiamos sinchronizavimo užduotys prieš sinchronizuojant „Sales“ sąskaitų faktūrų antraštes ir eilutes:</span><span class="sxs-lookup"><span data-stu-id="681e2-112">Sync tasks required prior to Sales invoice header and lines sync:</span></span>

- <span data-ttu-id="681e2-113">Produktai (iš „Finance and Operations“ į „Sales“)</span><span class="sxs-lookup"><span data-stu-id="681e2-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="681e2-114">Sąskaitos (iš „Sales“ į „Finance and Operations“) (jei naudojama)</span><span class="sxs-lookup"><span data-stu-id="681e2-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="681e2-115">Iš kontaktų į klientus (iš „Sales“ į „Finance and Operations“) (jei naudojama)</span><span class="sxs-lookup"><span data-stu-id="681e2-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="681e2-116">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="681e2-116">Entity set</span></span>

| <span data-ttu-id="681e2-117">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="681e2-117">Finance and Operations</span></span> |    <span data-ttu-id="681e2-118">„Common Data Service“ (CDS)</span><span class="sxs-lookup"><span data-stu-id="681e2-118">Common Data Service (CDS)</span></span>         |     <span data-ttu-id="681e2-119">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="681e2-119">Sales</span></span>      |
|------------------------|----------------|----------------|
| <span data-ttu-id="681e2-120">CDS pardavimo užsakymų antraštės</span><span class="sxs-lookup"><span data-stu-id="681e2-120">CDS sales order headers</span></span>| <span data-ttu-id="681e2-121">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="681e2-121">SalesOrder</span></span>     | <span data-ttu-id="681e2-122">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="681e2-122">SalesOrders</span></span> |
| <span data-ttu-id="681e2-123">CDS pardavimo užsakymo eilutės</span><span class="sxs-lookup"><span data-stu-id="681e2-123">CDS sales order lines</span></span>  | <span data-ttu-id="681e2-124">SalesOrderLine</span><span class="sxs-lookup"><span data-stu-id="681e2-124">SalesOrderLine</span></span> | <span data-ttu-id="681e2-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="681e2-125">SalesOrderDetails</span></span>|

## <a name="entity-flow"></a><span data-ttu-id="681e2-126">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="681e2-126">Entity flow</span></span>

<span data-ttu-id="681e2-127">Pardavimo užsakymai kuriami sprendime „Finance and Operations“ ir sinchronizuojami su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="681e2-127">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="681e2-128">Šablono filtrais užtikrinama, kad sinchronizuojant būtų įtraukiami tik aktualūs pardavimo užsakymai:</span><span class="sxs-lookup"><span data-stu-id="681e2-128">Filters in the template ensure that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="681e2-129">Sinchronizuojant bus įtraukiami tiek užsakantis klientas, tiek sąskaitą faktūrą išrašantis klientas, nurodyti pardavimo užsakyme, gautame iš „Sales“.</span><span class="sxs-lookup"><span data-stu-id="681e2-129">Both ordering and invoicing customer on the sales order that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="681e2-130">Sprendime „Finance and Operations“ laukai **OrderingCustomerIsExternallyMaintained** ir **InvoiceCustomerIsExternallyMaintained** naudojami sinchronizavimui duomenų objektuose sekti.</span><span class="sxs-lookup"><span data-stu-id="681e2-130">In Finance and Operations, the fields **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** are used to track the synchronization in the data entities.</span></span>

- <span data-ttu-id="681e2-131">Sprendime „Finance and Operations“ **pardavimo užsakymą** reikia patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="681e2-131">The **Sales order** in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="681e2-132">Su „Sales“ sinchronizuojami tik patvirtinti pardavimo užsakymai arba pardavimo užsakymai su aukštesne apdorojimo būsena, pavyzdžiui, būsena Išsiųstas arba Išrašyta SF.</span><span class="sxs-lookup"><span data-stu-id="681e2-132">Only the confirmed sales orders or sales orders with higher processing status, for example, Shipped or Invoiced status, are synchronized to Sales.</span></span>

- <span data-ttu-id="681e2-133">Sukūrus arba modifikavus pardavimo užsakymą, reikia vykdyti „Finance and Operations“ paketinę užduotį **Skaičiuoti bendrąsias pardavimo sumas**.</span><span class="sxs-lookup"><span data-stu-id="681e2-133">After creating or modifying a sales order, the batch job **Calculate sales totals** in Finance and Operations must be executed.</span></span> <span data-ttu-id="681e2-134">Su CDS ir „Sales“ bus sinchronizuojami tik tie pardavimo užsakymai, kurių bendrosios pardavimo sumos apskaičiuotos.</span><span class="sxs-lookup"><span data-stu-id="681e2-134">Only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="681e2-135">Su **pardavimo užsakymo antraštės** išlaidomis susijęs mokestis į sinchronizavimo iš „Finance and Operations“ į „Sales“ procesą šiuo metu nėra įtrauktas.</span><span class="sxs-lookup"><span data-stu-id="681e2-135">Tax related to charges on the **Sales order header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="681e2-136">Taip yra todėl, kad „Sales“ nepalaiko mokesčių informacijos antraštės lygyje.</span><span class="sxs-lookup"><span data-stu-id="681e2-136">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="681e2-137">Įtrauktas mokestis, susijęs su išlaidomis eilutės lygyje.</span><span class="sxs-lookup"><span data-stu-id="681e2-137">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="681e2-138">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="681e2-138">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="681e2-139">Į objektą **Užsakymas** įtraukiami nauji toliau nurodyti laukai, kurie rodomi puslapyje.</span><span class="sxs-lookup"><span data-stu-id="681e2-139">New fields are added to the **Order** entity and displayed on the page:</span></span>

- <span data-ttu-id="681e2-140">**Tvarkomas išoriškai** – nustatykite kaip **Taip**, kai užsakymas yra iš „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="681e2-140">**Is Maintained Externally** - Set to **Yes** when the order is coming from Finance and Operations.</span></span>

- <span data-ttu-id="681e2-141">**Apdorojimo būsena** – naudojamas „Finance and Operations“ užsakymo apdorojimo būsenai rodyti.</span><span class="sxs-lookup"><span data-stu-id="681e2-141">**Processing status** - Used to show the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="681e2-142">Reikšmės nurodytos toliau.</span><span class="sxs-lookup"><span data-stu-id="681e2-142">Values are:</span></span>

    - <span data-ttu-id="681e2-143">Aktyvu</span><span class="sxs-lookup"><span data-stu-id="681e2-143">Active</span></span>
    - <span data-ttu-id="681e2-144">Pritarta</span><span class="sxs-lookup"><span data-stu-id="681e2-144">Confirmed</span></span>
    - <span data-ttu-id="681e2-145">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="681e2-145">Packing Slip</span></span>
    - <span data-ttu-id="681e2-146">SF išrašyta</span><span class="sxs-lookup"><span data-stu-id="681e2-146">Invoiced</span></span>
    - <span data-ttu-id="681e2-147">Paimta</span><span class="sxs-lookup"><span data-stu-id="681e2-147">Picked</span></span>
    - <span data-ttu-id="681e2-148">Iš dalies paimtas</span><span class="sxs-lookup"><span data-stu-id="681e2-148">Partially Picked</span></span>
    - <span data-ttu-id="681e2-149">Iš dalies supakuotas</span><span class="sxs-lookup"><span data-stu-id="681e2-149">Partially Packed</span></span>
    - <span data-ttu-id="681e2-150">Išsiųsta</span><span class="sxs-lookup"><span data-stu-id="681e2-150">Shipped</span></span>
    - <span data-ttu-id="681e2-151">Iš dalies išsiųstas</span><span class="sxs-lookup"><span data-stu-id="681e2-151">Partially Shipped</span></span>
    - <span data-ttu-id="681e2-152">Iš dalies išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="681e2-152">Partially Invoiced</span></span>
    - <span data-ttu-id="681e2-153">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="681e2-153">Cancelled</span></span>

<span data-ttu-id="681e2-154">Kitose su pardavimo užsakymais susijusiose situacijose (sinchronizuojant iš „Sales“ į „Finance and Operations“) naudojamas parametras **Sudaro tik išoriškai tvarkomi produktai**, kuriuo nuosekliai sekama, ar visą pardavimo užsakymą sudaro tik **Išoriškai tvarkomi produktai**, o tokiu atveju produktai tvarkomi sprendime „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="681e2-154">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (from Sales to Finance and Operation sync) to consistently keep track of whether the sales order is made up entirely of **Externally Maintained Products**, in which case products are maintained in Finance and Operations.</span></span> <span data-ttu-id="681e2-155">Taip užtikrinama, kad nebandysite pardavimo užsakymo eilučių sinchronizuoti su produktais, kurių „Finance and Operations“ neatpažįsta.</span><span class="sxs-lookup"><span data-stu-id="681e2-155">This ensures that you don't try to sync sales order lines with products that are unknown to Finance and Operations.</span></span>
 
<span data-ttu-id="681e2-156">Išoriškai tvarkomuose užsakymuose puslapio **Pardavimo užsakymas** mygtukai **Kurti sąskaitą faktūrą**, **Atšaukti užsakymą**, **Perskaičiuoti**, **Gauti produktų** ir **Peržvelgti adresą** yra paslėpti, nes sąskaitos faktūros bus kuriamos sprendime „Finance and Operations“ ir sinchronizuojamos su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="681e2-156">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products** and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="681e2-157">Užsakymo puslapio redaguoti negalima, nes pardavimo užsakymo informacija bus sinchronizuojama iš „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="681e2-157">The order page is non-editable because sales order information will be synced from Finance and Operations.</span></span>
 
<span data-ttu-id="681e2-158">Sritis **Pardavimo užsakymo būsena** liks aktyvi, siekiant užtikrinti, kad keitimai iš „Finance and Operations“ galėtų būti perkelti į „Sales“ sritį **Pardavimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="681e2-158">The **Sales order status** will remain active to ensure that changes from Finance and Operations can flow to the **Sales order** in Sales.</span></span> <span data-ttu-id="681e2-159">Tai valdoma projekte Duomenų integravimas numatytąją srities **Būsenos kodas [būsena]** reikšmę nustačius kaip **Aktyvu**.</span><span class="sxs-lookup"><span data-stu-id="681e2-159">This is controlled by setting the default **Statecode [Status]** to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="681e2-160">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="681e2-160">Preconditions and mapping setup</span></span> 

<span data-ttu-id="681e2-161">Prieš sinchronizuojant pardavimo užsakymus, svarbu sistemas atnaujinti tolesniu parametru.</span><span class="sxs-lookup"><span data-stu-id="681e2-161">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="681e2-162">Sąranka sprendime „Sales“</span><span class="sxs-lookup"><span data-stu-id="681e2-162">Setup in Sales</span></span>

- <span data-ttu-id="681e2-163">Suteikite teises komandai, kuriai priskirtas vartotojas (iš „Sales“ **ryšio rinkinio**).</span><span class="sxs-lookup"><span data-stu-id="681e2-163">Ensure permissions for the team that the user (from your Sales **Connection set**) is assigned to.</span></span> <span data-ttu-id="681e2-164">Jei naudojate demonstracinius duomenis, paprastai administravimo prieigą turi vartotojas, bet ne komanda.</span><span class="sxs-lookup"><span data-stu-id="681e2-164">If you are using demo data, usually the user has admin access, but not the team.</span></span> <span data-ttu-id="681e2-165">To nenustatę, vykdydami projektą duomenų integratoriuje, gausite klaidą, kad trūksta pagrindinės komandos.</span><span class="sxs-lookup"><span data-stu-id="681e2-165">Without this you will get an error that Principal team is missing when running the project from Data integrator.</span></span> 

    - <span data-ttu-id="681e2-166">Srityje **Parametrai** > **Sauga** > **Komandos** pasirinkite reikiamą komandą, spustelėkite **Valdyti vaidmenis** ir pasirinkite vaidmenį su norimomis teisėmis, pvz., Sistemos administratorius.</span><span class="sxs-lookup"><span data-stu-id="681e2-166">Under **Settings** > **Security** > **Teams**, select the relevant team, click **Manage Roles** and select a role with the desired permissions e.g. System Administrator.</span></span>

- <span data-ttu-id="681e2-167">Įsitikinkite, kad dalyje **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimas** parinktis **Naudoti sistemos prizų skaičiavimo sistemą** nustatyta kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="681e2-167">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="681e2-168">Įsitikinkite, kad dalyje **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimas** parinktis **Nuolaidos skaičiavimo būdas** nustatyta kaip **Eilutės prekė**.</span><span class="sxs-lookup"><span data-stu-id="681e2-168">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="681e2-169">Sąranka sprendime „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="681e2-169">Setup in Finance and Operations</span></span>

<span data-ttu-id="681e2-170">Nustatykite, kad užduotis **Pardavimas ir rinkodara** > **Periodinės užduotys** > **Skaičiuoti bendrąsias pardavimo sumas** būtų vykdoma kaip paketinė užduotis, o parinktį **Skaičiuoti bendrąsias pardavimo užsakymų sumas** nustatykite kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="681e2-170">Set **Sales and marketing** > **Periodic tasks** > **Calculate sales totals** to run as a batch job, with **Calculate totals for sales orders** set to **Yes**.</span></span> <span data-ttu-id="681e2-171">Tai – svarbu, nes su CDS ir „Sales“ bus sinchronizuojami tik tie pardavimo užsakymai, kurių bendrosios pardavimo sumos apskaičiuotos.</span><span class="sxs-lookup"><span data-stu-id="681e2-171">This is important because only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span> <span data-ttu-id="681e2-172">Paketinės užduoties dažnumas turi būti lygus pardavimo užsakymų sinchronizavimo dažnumui.</span><span class="sxs-lookup"><span data-stu-id="681e2-172">The frequency of the batch job should be alligned with the frequency of the sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="681e2-173">Sąranka projekte Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="681e2-173">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="681e2-174">SalesHeader užduotis</span><span class="sxs-lookup"><span data-stu-id="681e2-174">SalesHeader task</span></span>

- <span data-ttu-id="681e2-175">Dalyje **Šaltinis** > **CDS** atnaujinkite CDS organizacijos ID susiejimą.</span><span class="sxs-lookup"><span data-stu-id="681e2-175">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span>

    - <span data-ttu-id="681e2-176">Numatytoji **Account_Organization_OrganizationId** šablono reikšmė yra ORG001.</span><span class="sxs-lookup"><span data-stu-id="681e2-176">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="681e2-177">Numatytoji **InvoiceAccount_Organization_OrganizationId** šablono reikšmė yra ORG001.</span><span class="sxs-lookup"><span data-stu-id="681e2-177">Default template value for **InvoiceAccount_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="681e2-178">Numatytoji **Organization_OrganizationId** šablono reikšmė yra ORG001.</span><span class="sxs-lookup"><span data-stu-id="681e2-178">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="681e2-179">Įsitikinkite, kad dalyje **Šaltinis** > **InvoiceCountryRegionId su BillingAddress_Country CDS** ir **DeliveryCountryRegionId su DeliveryAddress_Country** yra reikiamas susiejimas.</span><span class="sxs-lookup"><span data-stu-id="681e2-179">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** and for **DeliveryCountryRegionId to DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="681e2-180">Šablono reikšmė yra **ValueMap** su susietų šalių skaičiumi.</span><span class="sxs-lookup"><span data-stu-id="681e2-180">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="681e2-181">Sprendime „Sales“ norint kurti užsakymus, reikalingas **Kainoraštis**.</span><span class="sxs-lookup"><span data-stu-id="681e2-181">**Price list** is required to create orders in Sales.</span></span> <span data-ttu-id="681e2-182">**Dalyje** **CDS** > **pricelevelid.name paskirtis [kainoraščio pavadinimas]** kiekvienos valiutos reikšmę **ValueMap** atnaujinkite į sprendime „Sales“ naudojamą **kainoraštį**.</span><span class="sxs-lookup"><span data-stu-id="681e2-182">Update the **ValueMap** in **CDS** > **Destination** for **pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="681e2-183">Galite naudoti numatytąjį vienos valiutos **kainoraštį** arba **ValueMap**, jei turite **kainoraščių** keliomis valiutomis.</span><span class="sxs-lookup"><span data-stu-id="681e2-183">You can either used the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>
    
    - <span data-ttu-id="681e2-184">Numatytoji **pricelevelid.name [kainoraščio pavadinimas]** šablono reikšmė yra „CRM Service USA“ (pavyzdys).</span><span class="sxs-lookup"><span data-stu-id="681e2-184">Default template value for **pricelevelid.name [Price List Name]** is CRM Service USA (sample).</span></span> 

#### <a name="salesline-task"></a><span data-ttu-id="681e2-185">SalesLine užduotis</span><span class="sxs-lookup"><span data-stu-id="681e2-185">SalesLine task</span></span>

- <span data-ttu-id="681e2-186">Dalyje **Šaltinis** > **CDS** atnaujinkite CDS organizacijos ID susiejimą.</span><span class="sxs-lookup"><span data-stu-id="681e2-186">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 
    
    - <span data-ttu-id="681e2-187">Numatytoji **SalesOrder_Organization_OrganizationId** šablono reikšmė yra ORG001.</span><span class="sxs-lookup"><span data-stu-id="681e2-187">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="681e2-188">Numatytoji **Product_Organization_OrganizationId** šablono reikšmė yra ORG001.</span><span class="sxs-lookup"><span data-stu-id="681e2-188">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="681e2-189">Įsitikinkite, kad dalyje **Šaltinis** > **CDS** yra reikiamas **DeliveryCountryRegionId** susiejimas su **DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="681e2-189">Ensure that the needed mapping exists in **Source** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="681e2-190">Šablono reikšmė yra **ValueMap** su susietų šalių skaičiumi.</span><span class="sxs-lookup"><span data-stu-id="681e2-190">Template value is **ValueMap** with a number of countries mapped.</span></span>
    
- <span data-ttu-id="681e2-191">Įsitikinkite, kad „Finance and Operations“ dalyje **Šaltinis** > **CDS susiejimas** yra reikiama **SalesUnitSymbol** **ValueMap** reikšmė.</span><span class="sxs-lookup"><span data-stu-id="681e2-191">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span>

    - <span data-ttu-id="681e2-192">Apibrėžta **SalesUnitSymbol su Quantity_UOM** šablono reikšmė su **ValueMap**.</span><span class="sxs-lookup"><span data-stu-id="681e2-192">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="681e2-193">Šablono susiejimas duomenų integratoriuje</span><span class="sxs-lookup"><span data-stu-id="681e2-193">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="681e2-194">Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti.</span><span class="sxs-lookup"><span data-stu-id="681e2-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="681e2-195">Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.</span><span class="sxs-lookup"><span data-stu-id="681e2-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="681e2-196">Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.</span><span class="sxs-lookup"><span data-stu-id="681e2-196">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="orderheader"></a><span data-ttu-id="681e2-197">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="681e2-197">OrderHeader</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/sales-order-template-mapping-data-integrator-1.png)

![Šablono susiejimas duomenų integratoriuje](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a><span data-ttu-id="681e2-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="681e2-200">OrderLine</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/sales-order-template-mapping-data-integrator-3.png)

![Šablono susiejimas duomenų integratoriuje](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="681e2-203">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="681e2-203">Related topics</span></span>

[<span data-ttu-id="681e2-204">Sinchronizuoti „Finance and Operations“ produktus su „Sales“ produktais</span><span class="sxs-lookup"><span data-stu-id="681e2-204">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="681e2-205">Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais</span><span class="sxs-lookup"><span data-stu-id="681e2-205">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="681e2-206">Sinchronizuoti Pardavimo kontaktus su „Finance and Operations“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="681e2-206">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="681e2-207">Sinchronizuoti „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="681e2-207">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="681e2-208">Sinchronizuoti „Finance and Operations“ pardavimo SF antraštes ir eilutes su „Sales“</span><span class="sxs-lookup"><span data-stu-id="681e2-208">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


