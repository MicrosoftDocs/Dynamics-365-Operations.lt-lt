---
title: Tiesioginis Tiekimo grandinės valdymo pardavimo sąskaitų faktūrų antraščių ir eilučių sinchronizavimas su „Sales“
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Supply Chain Management“ leidimo pardavimo sąskaitų faktūrų antraštes ir eilutes tiesiogiai sinchronizuojant su „Dynamics 365 Sales“.
author: ChristianRytt
manager: tfehr
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 6cbc4d86ac41d90480428ec5439d1360c4d67137
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433468"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="d520d-103">Tiesioginis „Finance and Operations“ pardavimo sąskaitų faktūrų antraščių ir eilučių sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="d520d-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d520d-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Supply Chain Management“ leidimo pardavimo sąskaitų faktūrų antraštes ir eilutes tiesiogiai sinchronizuojant su „Dynamics 365 Sales“.</span><span class="sxs-lookup"><span data-stu-id="d520d-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="d520d-105">Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="d520d-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="d520d-106">Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Supply Chain Management“ ir „Sales“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="d520d-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="d520d-107">Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Supply Chain Management“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus.</span><span class="sxs-lookup"><span data-stu-id="d520d-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="d520d-108">Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami „Supply Chain Management “ ir „Sales“ duomenys.</span><span class="sxs-lookup"><span data-stu-id="d520d-108">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="d520d-109">[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="d520d-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d520d-110">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="d520d-110">Templates and tasks</span></span>

<span data-ttu-id="d520d-111">Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„Power Apps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="d520d-111">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="d520d-112">Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="d520d-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="d520d-113">Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami tiesiogiai sinchronizuojant „Supply Chain Management“ SF antraštes ir eilutes su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="d520d-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Supply Chain Management to Sales:</span></span>

- <span data-ttu-id="d520d-114">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** pardavimo sąskaitų faktūrų (iš „Finance and Operations“ į „Sales“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="d520d-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="d520d-115">**Užduočių pavadinimai projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="d520d-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="d520d-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="d520d-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="d520d-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="d520d-117">SalesInvoiceLine</span></span>

<span data-ttu-id="d520d-118">Prieš sinchronizuojant pardavimo sąskaitų faktūrų antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="d520d-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="d520d-119">Produktai (iš Tiekimo grandinės valdymo į „Sales“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="d520d-119">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="d520d-120">Sąskaitos (iš „Sales“ į Tiekimo grandinės valdymą) – tiesioginis (jei naudojamas)</span><span class="sxs-lookup"><span data-stu-id="d520d-120">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="d520d-121">Kontaktai (iš „Sales“ į Tiekimo grandinės valdymą) – tiesioginis (jei naudojamas)</span><span class="sxs-lookup"><span data-stu-id="d520d-121">Contacts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="d520d-122">Pardavimo užsakymų antraštės ir eilutės (iš Tiekimo grandinės valdymo į „Sales“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="d520d-122">Sales order header and lines (Supply Chain Management to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="d520d-123">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="d520d-123">Entity set</span></span>

| <span data-ttu-id="d520d-124">Tiekimo grandinės valdymas</span><span class="sxs-lookup"><span data-stu-id="d520d-124">Supply Chain Management</span></span>                              | <span data-ttu-id="d520d-125">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="d520d-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="d520d-126">Išorėje tvarkomų klientų pardavimo SF antraštės</span><span class="sxs-lookup"><span data-stu-id="d520d-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="d520d-127">Sąskaitos faktūros</span><span class="sxs-lookup"><span data-stu-id="d520d-127">Invoices</span></span>       |
| <span data-ttu-id="d520d-128">Išorėje tvarkomų klientų pardavimo SF eilutės</span><span class="sxs-lookup"><span data-stu-id="d520d-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="d520d-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="d520d-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="d520d-130">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="d520d-130">Entity flow</span></span>

<span data-ttu-id="d520d-131">Pardavimo sąskaitos faktūros kuriamos Tiekimo grandinės valdyme ir sinchronizuojamos su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="d520d-131">Sales invoices are created in Supply Chain Management and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="d520d-132">Šiuo metu su pardavimo sąskaitų faktūrų antraštės išlaidomis susijęs mokestis į sinchronizavimo iš Tiekimo grandinės valdymo į „Sales“ procesą nėra įtraukiamas.</span><span class="sxs-lookup"><span data-stu-id="d520d-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Supply Chain Managements to Sales.</span></span> <span data-ttu-id="d520d-133">„Sales“ nepalaikoma mokesčių informacija antraštės lygyje.</span><span class="sxs-lookup"><span data-stu-id="d520d-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="d520d-134">Tačiau su išlaidomis eilutės lygyje susijęs mokestis yra įtraukiamas į sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="d520d-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="d520d-135">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="d520d-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="d520d-136">Į objektą **Sąskaita faktūra** įtrauktas ir puslapyje rodomas laukas **Sąskaitos faktūros numeris**.</span><span class="sxs-lookup"><span data-stu-id="d520d-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="d520d-137">Puslapyje **Pardavimo užsakymas** esantis mygtukas **Kurti sąskaitą faktūrą** yra paslėptas, nes sąskaitos faktūros bus kuriamos Tiekimo grandinės valdyme ir sinchronizuojamos su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="d520d-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="d520d-138">Puslapio **Sąskaita faktūra** redaguoti negalima, nes sąskaitos faktūros bus sinchronizuojamos iš Tiekimo grandinės valdymo.</span><span class="sxs-lookup"><span data-stu-id="d520d-138">The **Invoice** page can't be edited, because invoices will be synchronized from Supply Chain Management.</span></span>
- <span data-ttu-id="d520d-139">Kai susijusi Tiekimo grandinės valdymo sąskaita faktūra baigiama sinchronizuoti su „Sales“, srities **Pardavimo užsakymo būsena** reikšmė automatiškai pakeičiama į **Išrašyta sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="d520d-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Supply Chain Management has been synchronized to Sales.</span></span> <span data-ttu-id="d520d-140">Be to, pardavimo užsakymo, iš kurio buvo sukurta sąskaita faktūra, savininkas priskiriamas sąskaitos faktūros savininku.</span><span class="sxs-lookup"><span data-stu-id="d520d-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="d520d-141">Todėl pardavimo užsakymo savininkas gali peržiūrėti sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="d520d-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="d520d-142">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d520d-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="d520d-143">Prieš sinchronizuojant pardavimo sąskaitas faktūras, svarbu atnaujinti toliau nurodytus sistemų parametrus.</span><span class="sxs-lookup"><span data-stu-id="d520d-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="d520d-144">Sąranka sprendime „Sales“</span><span class="sxs-lookup"><span data-stu-id="d520d-144">Setup in Sales</span></span>

<span data-ttu-id="d520d-145">Eikite į **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimai** ir įsitikinkite, kad naudojami toliau nurodyti parametrai.</span><span class="sxs-lookup"><span data-stu-id="d520d-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="d520d-146">Parinktis **Naudoti sistemos prizų skaičiavimo sistemą** nustatyta į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="d520d-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="d520d-147">Laukas **Nuolaidos skaičiavimo būdas** nustatytas į **Eilutės elementas**.</span><span class="sxs-lookup"><span data-stu-id="d520d-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="d520d-148">Sąranka projekte Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="d520d-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="d520d-149">SalesInvoiceHeader užduotis</span><span class="sxs-lookup"><span data-stu-id="d520d-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="d520d-150">Įsitikinkite, kad yra reikiamas **InvoiceCountryRegionId** susiejimas su **BillingAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="d520d-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="d520d-151">Šablono vertė yra vertės schema, kurioje susieta keletas šalių ar regionų.</span><span class="sxs-lookup"><span data-stu-id="d520d-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="d520d-152">Norint Sprendime „Sales“ kurti sąskaitas faktūras, reikalingas Kainoraštis.</span><span class="sxs-lookup"><span data-stu-id="d520d-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="d520d-153">Dalyje **pricelevelid.name \[Kainoraščio pavadinimas\]** kiekvienos valiutos vertės schemą atnaujinkite į sprendime „Sales“ naudojamą kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="d520d-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="d520d-154">Kiekvienai valiutai galite naudoti numatytąjį kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="d520d-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="d520d-155">Taip pat, jei turite kainoraščių keliomis valiutomis, galite naudoti vertės schemą.</span><span class="sxs-lookup"><span data-stu-id="d520d-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="d520d-156">Dalies **pricelevelid.name \[kainų sąrašo pavadinimas\]** šablono vertė yra vertės schema, pagrįsta USD valiuta = „CRM Service USA“ (pavyzdys).</span><span class="sxs-lookup"><span data-stu-id="d520d-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="d520d-157">SalesInvoiceLine užduotis</span><span class="sxs-lookup"><span data-stu-id="d520d-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="d520d-158">Įsitikinkite, kad yra reikiamas **Matavimo vieneto** siejimas.</span><span class="sxs-lookup"><span data-stu-id="d520d-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="d520d-159">Įsitikinkite, kad reikiamas **SalesUnitSymbol** skirtas susiejimas yra Tiekimo grandinės valdyme.</span><span class="sxs-lookup"><span data-stu-id="d520d-159">Make sure that the required value map for **SalesUnitSymbol** in Supply Chain Management exists.</span></span>

    <span data-ttu-id="d520d-160">Šablono vertė, kurioje yra vertės schema, apibrėžta **SalesUnitSymbol** su **Quantity\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="d520d-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d520d-161">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="d520d-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="d520d-162">Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti.</span><span class="sxs-lookup"><span data-stu-id="d520d-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="d520d-163">Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.</span><span class="sxs-lookup"><span data-stu-id="d520d-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="d520d-164">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="d520d-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="d520d-165">Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="d520d-165">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="d520d-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="d520d-166">SalesInvoiceHeader</span></span>

![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="d520d-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="d520d-168">SalesInvoiceLine</span></span>

![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="d520d-170">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="d520d-170">Related topics</span></span>

[<span data-ttu-id="d520d-171">Potencialaus kliento pavertimas pinigais</span><span class="sxs-lookup"><span data-stu-id="d520d-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="d520d-172">Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Supply Chain Management“ klientais</span><span class="sxs-lookup"><span data-stu-id="d520d-172">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="d520d-173">Tiesioginis „Supply Chain Management“ produktų sinchronizavimas su „Sales“ produktais</span><span class="sxs-lookup"><span data-stu-id="d520d-173">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="d520d-174">Tiesioginis „Sales“ kontaktų sinchronizavimas su „Supply Chain Management“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="d520d-174">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="d520d-175">Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir Tiekimo grandinės valdymo</span><span class="sxs-lookup"><span data-stu-id="d520d-175">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)
