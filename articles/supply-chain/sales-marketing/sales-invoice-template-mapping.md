---
title: "Sinchronizuoti „Finance and Operations“ pardavimo SF antraštes ir eilutes su „Sales“"
description: "Temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ pardavimo sąskaitų faktūrų antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Sales“."
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
ms.openlocfilehash: 6db68236f512cc720e75c0d576ce4c49d6c87882
ms.contentlocale: lt-lt
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="85ef9-103">Sinchronizuoti „Finance and Operations“ pardavimo SF antraštes ir eilutes su „Sales“</span><span class="sxs-lookup"><span data-stu-id="85ef9-103">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="85ef9-104">Temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ pardavimo sąskaitų faktūrų antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Sales“.</span><span class="sxs-lookup"><span data-stu-id="85ef9-104">The topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="85ef9-105">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="85ef9-105">Templates and tasks</span></span>

<span data-ttu-id="85ef9-106">Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami sinchronizuojant „Finance and Operations“ pardavimo sąskaitų faktūrų antraštes ir eilutes su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="85ef9-106">The following templates and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="85ef9-107">**Šablono pavadinimas naudojant funkciją Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="85ef9-107">**Name of the template in Data integration**</span></span> 

     - <span data-ttu-id="85ef9-108">Pardavimo sąskaitos faktūros (iš „Finance and Operations“ į „Sales“)</span><span class="sxs-lookup"><span data-stu-id="85ef9-108">Sales Invoices (Fin and Ops to Sales)</span></span>

- <span data-ttu-id="85ef9-109">**Užduočių pavadinimai projekte Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="85ef9-109">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="85ef9-110">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="85ef9-110">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="85ef9-111">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="85ef9-111">SalesInvoiceLine</span></span>

<span data-ttu-id="85ef9-112">Reikiamos sinchronizavimo užduotys prieš sinchronizuojant „Sales“ sąskaitų faktūrų antraštes ir eilutes:</span><span class="sxs-lookup"><span data-stu-id="85ef9-112">Sync tasks required prior to Sales invoice header and lines synchronization:</span></span>
-   <span data-ttu-id="85ef9-113">Produktai (iš „Finance and Operations“ į „Sales“)</span><span class="sxs-lookup"><span data-stu-id="85ef9-113">Products (Fin and Ops to Sales)</span></span>
-   <span data-ttu-id="85ef9-114">Sąskaitos (iš „Sales“ į „Finance and Operations“) (jei naudojama)</span><span class="sxs-lookup"><span data-stu-id="85ef9-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="85ef9-115">Kontaktai (iš „Sales“ į „Finance and Operations“) (jei naudojama)</span><span class="sxs-lookup"><span data-stu-id="85ef9-115">Contacts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="85ef9-116">Pardavimo užsakymo antraštė ir eilutės (iš „Finance and Operations“ į „Sales“)</span><span class="sxs-lookup"><span data-stu-id="85ef9-116">Sales order header and lines (Fin and Ops to Sales)</span></span>

## <a name="entity-set"></a><span data-ttu-id="85ef9-117">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="85ef9-117">Entity set</span></span>

| <span data-ttu-id="85ef9-118">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="85ef9-118">Finance and Operations</span></span>                               | <span data-ttu-id="85ef9-119">„Common Data Service“ (CDS)</span><span class="sxs-lookup"><span data-stu-id="85ef9-119">Common Data Service (CDS)</span></span>              | <span data-ttu-id="85ef9-120">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="85ef9-120">Sales</span></span>          |
|------------------------------------------------------|------------------|----------------|
| <span data-ttu-id="85ef9-121">Išorėje tvarkomų klientų pardavimo SF antraštės</span><span class="sxs-lookup"><span data-stu-id="85ef9-121">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="85ef9-122">SalesInvoice</span><span class="sxs-lookup"><span data-stu-id="85ef9-122">SalesInvoice</span></span>     | <span data-ttu-id="85ef9-123">Sąskaitos faktūros</span><span class="sxs-lookup"><span data-stu-id="85ef9-123">Invoices</span></span>       |
| <span data-ttu-id="85ef9-124">Išorėje tvarkomų klientų pardavimo SF eilutės</span><span class="sxs-lookup"><span data-stu-id="85ef9-124">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="85ef9-125">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="85ef9-125">SalesInvoiceLine</span></span> | <span data-ttu-id="85ef9-126">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="85ef9-126">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="85ef9-127">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="85ef9-127">Entity flow</span></span>

<span data-ttu-id="85ef9-128">Pardavimo sąskaitos faktūros kuriamos sprendime „Finance and Operations“ ir sinchronizuojamos su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="85ef9-128">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="85ef9-129">Su **pardavimo sąskaitos faktūros antraštės** išlaidomis susijęs mokestis į sinchronizavimo iš „Finance and Operations“ į „Sales“ procesą šiuo metu nėra įtrauktas.</span><span class="sxs-lookup"><span data-stu-id="85ef9-129">Tax related to charges on the **Sales invoice header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="85ef9-130">Taip yra todėl, kad „Sales“ nepalaiko mokesčių informacijos antraštės lygyje.</span><span class="sxs-lookup"><span data-stu-id="85ef9-130">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="85ef9-131">Įtrauktas mokestis, susijęs su išlaidomis eilutės lygyje.</span><span class="sxs-lookup"><span data-stu-id="85ef9-131">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="85ef9-132">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="85ef9-132">Prospect to cash solution for Sales</span></span>

-  <span data-ttu-id="85ef9-133">Į objektą **Sąskaita faktūra** įtraukiamas ir puslapyje rodomas laukas **Sąskaitos faktūros numeris**.</span><span class="sxs-lookup"><span data-stu-id="85ef9-133">An **Invoice number field** is added to the **Invoice** entity and displayed on the page.</span></span>
 
-  <span data-ttu-id="85ef9-134">Puslapyje **Pardavimo užsakymas** esantis mygtukas **Kurti sąskaitą faktūrą** yra paslėptas, nes sąskaitos faktūros bus kuriamos sprendime „Finance and Operations“ ir sinchronizuojamos su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="85ef9-134">The **Create invoice** button on the **Sales order** page is hidden because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="85ef9-135">Puslapio **Sąskaita faktūra** redaguoti negalima, nes sąskaitos faktūros bus sinchronizuojamos iš „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="85ef9-135">The **Invoice** page is non-editable because invoices will be synced from Finance and Operations.</span></span>
 
-  <span data-ttu-id="85ef9-136">Kai susijusi „Finance and Operations“ sąskaita faktūra baigiama sinchronizuoti su „Sales“, **pardavimo užsakymo būsena** automatiškai pasikeičia į **Išrašyta sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="85ef9-136">The **Sales order status** changes automatically to **Invoiced** when the related invoice from Finance and Operations has been  synchronized to Sales.</span></span> <span data-ttu-id="85ef9-137">Be to, pardavimo užsakymo, iš kurio buvo sukurta sąskaita faktūra, savininkas priskiriamas sąskaitos faktūros savininku.</span><span class="sxs-lookup"><span data-stu-id="85ef9-137">Also, the owner of the sales order from which the invoice was created is assigned as the owner of the invoice.</span></span> <span data-ttu-id="85ef9-138">Taip pardavimo užsakymo savininkui suteikiama galimybė peržiūrėti sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="85ef9-138">This gives the owner of the sales order the ability to view the invoice.</span></span>
 
## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="85ef9-139">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="85ef9-139">Preconditions and mapping setup</span></span>

<span data-ttu-id="85ef9-140">Prieš sinchronizuojant pardavimo sąskaitas faktūras, svarbu sistemas atnaujinti tolesniu parametru.</span><span class="sxs-lookup"><span data-stu-id="85ef9-140">Before synchronizing sales invoices, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="85ef9-141">Sąranka sprendime „Sales“</span><span class="sxs-lookup"><span data-stu-id="85ef9-141">Setup in Sales</span></span>

- <span data-ttu-id="85ef9-142">Įsitikinkite, kad dalyje **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimas** parinktis **Naudoti sistemos prizų skaičiavimo sistemą** nustatyta kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="85ef9-142">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="85ef9-143">Įsitikinkite, kad dalyje **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimas** parinktis **Nuolaidos skaičiavimo būdas** nustatyta kaip **Eilutės prekė**.</span><span class="sxs-lookup"><span data-stu-id="85ef9-143">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="85ef9-144">Sąranka projekte Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="85ef9-144">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="85ef9-145">SalesInvoiceHeader užduotis</span><span class="sxs-lookup"><span data-stu-id="85ef9-145">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="85ef9-146">Dalyje **Šaltinis** > **CDS** atnaujinkite **CDS organizacijos ID** susiejimą.</span><span class="sxs-lookup"><span data-stu-id="85ef9-146">Update the mapping for **CDS Organization ID** in **Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="85ef9-147">Numatytoji **SalesOrder_Organization_OrganizationId** šablono reikšmė yra ORG001.</span><span class="sxs-lookup"><span data-stu-id="85ef9-147">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="85ef9-148">Numatytoji **Account_Organization_OrganizationId** šablono reikšmė yra ORG001.</span><span class="sxs-lookup"><span data-stu-id="85ef9-148">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="85ef9-149">Numatytoji **Organization_OrganizationId** šablono reikšmė yra ORG001.</span><span class="sxs-lookup"><span data-stu-id="85ef9-149">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="85ef9-150">Įsitikinkite, kad dalyje **Šaltinis** > **InvoiceCountryRegionId CDS** yra reikiamas susiejimas su **BillingAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="85ef9-150">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span></span>

    -  <span data-ttu-id="85ef9-151">Šablono reikšmė yra **ValueMap** su susietų šalių skaičiumi.</span><span class="sxs-lookup"><span data-stu-id="85ef9-151">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="85ef9-152">Sprendime „Sales“ norint kurti sąskaitas faktūras, reikalingas **Kainoraštis**.</span><span class="sxs-lookup"><span data-stu-id="85ef9-152">**Price list** is required to create invoices in Sales.</span></span> <span data-ttu-id="85ef9-153">Dalyje **CDS** > **pricelevelid.name paskirtis [kainoraščio pavadinimas]** kiekvienos valiutos reikšmę **ValueMap** atnaujinkite į sprendime „Sales“ naudojamą **kainoraštį**.</span><span class="sxs-lookup"><span data-stu-id="85ef9-153">Update the **ValueMap** in **CDS** > **Destination for pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="85ef9-154">Galite naudoti numatytąjį vienos valiutos **kainoraštį** arba **ValueMap**, jei turite **kainoraščių** keliomis valiutomis.</span><span class="sxs-lookup"><span data-stu-id="85ef9-154">You can either use the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>

    -  <span data-ttu-id="85ef9-155">**pricelevelid.name [kainoraščio pavadinimas]** šablono reikšmė yra **ValueMap** pagal **valiutą**.</span><span class="sxs-lookup"><span data-stu-id="85ef9-155">Template value for **pricelevelid.name [Price List Name]** is **ValueMap** based on **Currency**.</span></span>
    -  <span data-ttu-id="85ef9-156">usd: CRM Service USA (pavyzdys).</span><span class="sxs-lookup"><span data-stu-id="85ef9-156">usd: CRM Service USA (sample).</span></span> 

#### <a name="salesinvoiceline-task"></a><span data-ttu-id="85ef9-157">SalesInvoiceLine užduotis</span><span class="sxs-lookup"><span data-stu-id="85ef9-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="85ef9-158">Įsitikinkite, kad dalyje **Šaltinis** > **CDS matavimo vienetas** yra reikiamas susiejimas.</span><span class="sxs-lookup"><span data-stu-id="85ef9-158">Ensure that the needed mapping exists in **Source** > **CDS for Unit of measure**.</span></span>

- <span data-ttu-id="85ef9-159">Įsitikinkite, kad „Finance and Operations“ dalyje **Šaltinis** > **CDS susiejimas** yra reikiama **SalesUnitSymbol** **ValueMap** reikšmė.</span><span class="sxs-lookup"><span data-stu-id="85ef9-159">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span> 
    
    - <span data-ttu-id="85ef9-160">Apibrėžta **SalesUnitSymbol su Quantity_UOM** šablono reikšmė su **ValueMap**.</span><span class="sxs-lookup"><span data-stu-id="85ef9-160">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>
    
-  <span data-ttu-id="85ef9-161">Dalyje **Šaltinis** > **CDS** atnaujinkite CDS organizacijos ID susiejimą.</span><span class="sxs-lookup"><span data-stu-id="85ef9-161">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="85ef9-162">Numatytoji **SalesInvoicer_Organization_OrganizationId** šablono reikšmė yra ORG001.</span><span class="sxs-lookup"><span data-stu-id="85ef9-162">Default template value for **SalesInvoicer_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="85ef9-163">Numatytoji **Product_Organization_OrganizationId** šablono reikšmė yra ORG001.</span><span class="sxs-lookup"><span data-stu-id="85ef9-163">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>
 
## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="85ef9-164">Šablono susiejimas duomenų integratoriuje</span><span class="sxs-lookup"><span data-stu-id="85ef9-164">Template mapping in Data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="85ef9-165">**Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti.</span><span class="sxs-lookup"><span data-stu-id="85ef9-165">**Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** are not part of the default mappings.</span></span> <span data-ttu-id="85ef9-166">Norint susieti šiuos laukus, reikia nustatyti reikšmių susiejimą, kuris atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.</span><span class="sxs-lookup"><span data-stu-id="85ef9-166">Mapping of these fields requires value mapping to be set up, which is specific to the data in the organizations between which the entity is synchronized.</span></span>

<span data-ttu-id="85ef9-167">Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.</span><span class="sxs-lookup"><span data-stu-id="85ef9-167">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Šablono susiejimas duomenų integratoriuje](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Šablono susiejimas duomenų integratoriuje](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Šablono susiejimas duomenų integratoriuje](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="85ef9-172">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="85ef9-172">Related topics</span></span>

[<span data-ttu-id="85ef9-173">Sinchronizuoti „Finance and Operations“ produktus su „Sales“ produktais</span><span class="sxs-lookup"><span data-stu-id="85ef9-173">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="85ef9-174">Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais</span><span class="sxs-lookup"><span data-stu-id="85ef9-174">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="85ef9-175">Sinchronizuoti Pardavimo kontaktus su „Finance and Operations“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="85ef9-175">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="85ef9-176">Sinchronizuoti „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="85ef9-176">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="85ef9-177">Sinchronizuoti „Finance and Operations“ pardavimo užsakymo antraštes ir eilutes su „Sales“</span><span class="sxs-lookup"><span data-stu-id="85ef9-177">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)


