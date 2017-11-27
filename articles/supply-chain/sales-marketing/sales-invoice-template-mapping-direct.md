---
title: "Tiesioginis „Finance and Operations“ pardavimo sąskaitų faktūrų antraščių ir eilučių sinchronizavimas su „Sales“"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ „Enterprise“ leidimo pardavimo sąskaitos faktūros antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Sales“."
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e9d7e756c56932372ed931620016973c794fb3fc
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="b85a0-103">Tiesioginis „Finance and Operations“ pardavimo sąskaitų faktūrų antraščių ir eilučių sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="b85a0-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b85a0-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ „Enterprise“ leidimo pardavimo sąskaitos faktūros antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Sales“.</span><span class="sxs-lookup"><span data-stu-id="b85a0-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="b85a0-105">Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="b85a0-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="b85a0-106">Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Finance and Operations“ ir „Sales“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="b85a0-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="b85a0-107">Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus.</span><span class="sxs-lookup"><span data-stu-id="b85a0-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="b85a0-108">Toliau pateiktoje iliustracijoje rodoma, kaip duomenys sinchronizuojami tarp „Finance and Operations“ ir „Sales“.</span><span class="sxs-lookup"><span data-stu-id="b85a0-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="b85a0-109">[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="b85a0-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b85a0-110">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="b85a0-110">Templates and tasks</span></span>

<span data-ttu-id="b85a0-111">Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„PowerApps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="b85a0-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="b85a0-112">Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="b85a0-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b85a0-113">Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami sinchronizuojant „Finance and Operations“ pardavimo sąskaitų faktūrų antraštes ir eilutes su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="b85a0-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="b85a0-114">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** pardavimo sąskaitų faktūrų (iš „Finance and Operations“ į „Sales“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="b85a0-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="b85a0-115">**Užduočių pavadinimai projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="b85a0-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="b85a0-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="b85a0-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="b85a0-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="b85a0-117">SalesInvoiceLine</span></span>

<span data-ttu-id="b85a0-118">Prieš sinchronizuojant pardavimo sąskaitų faktūrų antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="b85a0-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="b85a0-119">Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="b85a0-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="b85a0-120">Sąskaitos (iš „Sales“ į „Finance and Operations“) – tiesioginis (jei naudojama)</span><span class="sxs-lookup"><span data-stu-id="b85a0-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="b85a0-121">Kontaktai (iš „Sales“ į „Finance and Operations“) – tiesioginis (jei naudojama)</span><span class="sxs-lookup"><span data-stu-id="b85a0-121">Contacts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="b85a0-122">Pardavimo užsakymo antraštė ir eilutės (iš „Finance and Operations“ į „Sales“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="b85a0-122">Sales order header and lines (Fin and Ops to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="b85a0-123">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="b85a0-123">Entity set</span></span>

| <span data-ttu-id="b85a0-124">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="b85a0-124">Finance and Operations</span></span>                               | <span data-ttu-id="b85a0-125">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="b85a0-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="b85a0-126">Išorėje tvarkomų klientų pardavimo SF antraštės</span><span class="sxs-lookup"><span data-stu-id="b85a0-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="b85a0-127">Sąskaitos faktūros</span><span class="sxs-lookup"><span data-stu-id="b85a0-127">Invoices</span></span>       |
| <span data-ttu-id="b85a0-128">Išorėje tvarkomų klientų pardavimo SF eilutės</span><span class="sxs-lookup"><span data-stu-id="b85a0-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="b85a0-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="b85a0-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="b85a0-130">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="b85a0-130">Entity flow</span></span>

<span data-ttu-id="b85a0-131">Pardavimo sąskaitos faktūros kuriamos sprendime „Finance and Operations“ ir sinchronizuojamos su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="b85a0-131">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="b85a0-132">Šiuo metu su pardavimo sąskaitų faktūrų antraštės išlaidomis susijęs mokestis į sinchronizavimo iš „Finance and Operations“ į „Sales“ procesą nėra įtraukiamas.</span><span class="sxs-lookup"><span data-stu-id="b85a0-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="b85a0-133">„Sales“ nepalaikoma mokesčių informacija antraštės lygyje.</span><span class="sxs-lookup"><span data-stu-id="b85a0-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="b85a0-134">Tačiau su išlaidomis eilutės lygyje susijęs mokestis yra įtraukiamas į sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="b85a0-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b85a0-135">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="b85a0-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="b85a0-136">Į objektą **Sąskaita faktūra** įtrauktas ir puslapyje rodomas laukas **Sąskaitos faktūros numeris**.</span><span class="sxs-lookup"><span data-stu-id="b85a0-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="b85a0-137">Puslapyje **Pardavimo užsakymas** esantis mygtukas **Kurti sąskaitą faktūrą** yra paslėptas, nes sąskaitos faktūros bus kuriamos sprendime „Finance and Operations“ ir sinchronizuojamos su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="b85a0-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="b85a0-138">Puslapio **Sąskaita faktūra** redaguoti negalima, nes sąskaitos faktūros bus sinchronizuojamos iš „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="b85a0-138">The **Invoice** page can't be edited, because invoices will be synchronized from Finance and Operations.</span></span>
- <span data-ttu-id="b85a0-139">Kai susijusi „Finance and Operations“ sąskaita faktūra baigiama sinchronizuoti su „Sales“, srities **Pardavimo užsakymo būsena** vertė automatiškai pakeičiama į **Išrašyta sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="b85a0-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Finance and Operations has been synchronized to Sales.</span></span> <span data-ttu-id="b85a0-140">Be to, pardavimo užsakymo, iš kurio buvo sukurta sąskaita faktūra, savininkas priskiriamas sąskaitos faktūros savininku.</span><span class="sxs-lookup"><span data-stu-id="b85a0-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="b85a0-141">Todėl pardavimo užsakymo savininkas gali peržiūrėti sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="b85a0-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="b85a0-142">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="b85a0-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="b85a0-143">Prieš sinchronizuojant pardavimo sąskaitas faktūras, svarbu atnaujinti toliau nurodytus sistemų parametrus.</span><span class="sxs-lookup"><span data-stu-id="b85a0-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="b85a0-144">Sąranka sprendime „Sales“</span><span class="sxs-lookup"><span data-stu-id="b85a0-144">Setup in Sales</span></span>

<span data-ttu-id="b85a0-145">Eikite į **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimai** ir įsitikinkite, kad naudojami toliau nurodyti parametrai.</span><span class="sxs-lookup"><span data-stu-id="b85a0-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="b85a0-146">Parinktis **Naudoti sistemos prizų skaičiavimo sistemą** nustatyta į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="b85a0-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="b85a0-147">Laukas **Nuolaidos skaičiavimo būdas** nustatytas į **Eilutės elementas**.</span><span class="sxs-lookup"><span data-stu-id="b85a0-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="b85a0-148">Sąranka projekte Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="b85a0-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="b85a0-149">SalesInvoiceHeader užduotis</span><span class="sxs-lookup"><span data-stu-id="b85a0-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="b85a0-150">Įsitikinkite, kad yra reikiamas **InvoiceCountryRegionId** susiejimas su **BillingAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="b85a0-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="b85a0-151">Šablono vertė yra vertės schema, kurioje susieta keletas šalių ar regionų.</span><span class="sxs-lookup"><span data-stu-id="b85a0-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="b85a0-152">Norint Sprendime „Sales“ kurti sąskaitas faktūras, reikalingas Kainoraštis.</span><span class="sxs-lookup"><span data-stu-id="b85a0-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="b85a0-153">Dalyje **pricelevelid.name \[Kainoraščio pavadinimas\]** kiekvienos valiutos vertės schemą atnaujinkite į sprendime „Sales“ naudojamą kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="b85a0-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="b85a0-154">Kiekvienai valiutai galite naudoti numatytąjį kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="b85a0-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="b85a0-155">Taip pat, jei turite kainoraščių keliomis valiutomis, galite naudoti vertės schemą.</span><span class="sxs-lookup"><span data-stu-id="b85a0-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="b85a0-156">Dalies **pricelevelid.name \[kainų sąrašo pavadinimas\]** šablono vertė yra vertės schema, pagrįsta USD valiuta = „CRM Service USA“ (pavyzdys).</span><span class="sxs-lookup"><span data-stu-id="b85a0-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="b85a0-157">SalesInvoiceLine užduotis</span><span class="sxs-lookup"><span data-stu-id="b85a0-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="b85a0-158">Įsitikinkite, kad yra reikiamas **Matavimo vieneto** siejimas.</span><span class="sxs-lookup"><span data-stu-id="b85a0-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="b85a0-159">Įsitikinkite, kad „Finance and Operations“ yra **SalesUnitSymbol** būtina verčių schema.</span><span class="sxs-lookup"><span data-stu-id="b85a0-159">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="b85a0-160">Šablono vertė, kurioje yra vertės schema, apibrėžta **SalesUnitSymbol** su **Quantity\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="b85a0-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b85a0-161">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="b85a0-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="b85a0-162">Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti.</span><span class="sxs-lookup"><span data-stu-id="b85a0-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="b85a0-163">Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.</span><span class="sxs-lookup"><span data-stu-id="b85a0-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="b85a0-164">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="b85a0-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="b85a0-165">Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="b85a0-165">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="b85a0-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="b85a0-166">SalesInvoiceHeader</span></span>

![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="b85a0-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="b85a0-168">SalesInvoiceLine</span></span>

![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="b85a0-170">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="b85a0-170">Related topics</span></span>

[<span data-ttu-id="b85a0-171">Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="b85a0-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="b85a0-172">Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Finance and Operations“ klientais</span><span class="sxs-lookup"><span data-stu-id="b85a0-172">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="b85a0-173">Tiesioginis „Finance and Operations“ produktų sinchronizavimas su „Sales“ produktais</span><span class="sxs-lookup"><span data-stu-id="b85a0-173">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="b85a0-174">Tiesioginis „Sales“ kontaktų sinchronizavimas su „Finance and Operations“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="b85a0-174">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="b85a0-175">Tiesioginis „Finance and Operations“ pardavimo užsakymų antraščių ir eilučių sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="b85a0-175">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)







