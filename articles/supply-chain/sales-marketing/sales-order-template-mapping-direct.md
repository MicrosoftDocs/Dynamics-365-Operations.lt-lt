---
title: "„Finance and Operations“ pardavimo užsakymo antraščių ir eilučių tiesioginis sinchronizavimas su „Sales“"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ „Enterprise“ leidimo pardavimo užsakymų antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Sales“."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="ade30-103">„Finance and Operations“ pardavimo užsakymo antraščių ir eilučių tiesioginis sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="ade30-103">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ade30-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ „Enterprise“ leidimo pardavimo užsakymų antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Sales“.</span><span class="sxs-lookup"><span data-stu-id="ade30-104">This topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="ade30-105">Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="ade30-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="ade30-106">Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Finance and Operations“ ir „Sales“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="ade30-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="ade30-107">Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus.</span><span class="sxs-lookup"><span data-stu-id="ade30-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="ade30-108">Toliau pateiktoje iliustracijoje rodoma, kaip duomenys sinchronizuojami tarp „Finance and Operations“ ir „Sales“.</span><span class="sxs-lookup"><span data-stu-id="ade30-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="ade30-109">[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="ade30-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ade30-110">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="ade30-110">Templates and tasks</span></span>

<span data-ttu-id="ade30-111">Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„PowerApps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="ade30-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="ade30-112">Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="ade30-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="ade30-113">Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami sinchronizuojant „Finance and Operations“ pardavimo užsakymų antraštes ir eilutes su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="ade30-113">The following template and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="ade30-114">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** pardavimo užsakymai (iš „Finance and Operations“ į „Sales“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="ade30-114">**Name of the template in Data integration:** Sales Orders (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="ade30-115">**Užduočių pavadinimai projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="ade30-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="ade30-116">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="ade30-116">OrderHeader</span></span>
    - <span data-ttu-id="ade30-117">OrderLine</span><span class="sxs-lookup"><span data-stu-id="ade30-117">OrderLine</span></span>

<span data-ttu-id="ade30-118">Prieš sinchronizuojant pardavimo sąskaitų faktūrų antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="ade30-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="ade30-119">Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="ade30-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="ade30-120">Sąskaitos (iš „Sales“ į „Finance and Operations“) – tiesioginis (jei naudojama)</span><span class="sxs-lookup"><span data-stu-id="ade30-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="ade30-121">Iš kontaktų į klientus (iš „Sales“ į „Finance and Operations“) – tiesioginis (jei naudojama)</span><span class="sxs-lookup"><span data-stu-id="ade30-121">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="ade30-122">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="ade30-122">Entity set</span></span>

| <span data-ttu-id="ade30-123">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="ade30-123">Finance and Operations</span></span>  | <span data-ttu-id="ade30-124">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="ade30-124">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="ade30-125">CDS pardavimo užsakymų antraštės</span><span class="sxs-lookup"><span data-stu-id="ade30-125">CDS sales order headers</span></span> | <span data-ttu-id="ade30-126">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="ade30-126">SalesOrders</span></span>       |
| <span data-ttu-id="ade30-127">CDS pardavimo užsakymo eilutės</span><span class="sxs-lookup"><span data-stu-id="ade30-127">CDS sales order lines</span></span>   | <span data-ttu-id="ade30-128">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="ade30-128">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="ade30-129">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="ade30-129">Entity flow</span></span>

<span data-ttu-id="ade30-130">Pardavimo užsakymai kuriami sprendime „Finance and Operations“ ir sinchronizuojami su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="ade30-130">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="ade30-131">Naudojant šablono filtrus padedama užtikrinti, kad sinchronizuojant būtų įtraukiami tik aktualūs pardavimo užsakymai:</span><span class="sxs-lookup"><span data-stu-id="ade30-131">Filters in the template help guarantee that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="ade30-132">Sinchronizuojant bus įtraukiami „Sales“ pardavimo užsakyme nurodyti užsakantis klientas ir sąskaitą faktūrą išrašantis klientas.</span><span class="sxs-lookup"><span data-stu-id="ade30-132">On the sales order, both the ordering customer and the invoicing customer that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="ade30-133">Sprendime „Finance and Operations“ laukai **OrderingCustomerIsExternallyMaintained** ir **InvoiceCustomerIsExternallyMaintained** naudojami sinchronizavimui duomenų objektuose sekti.</span><span class="sxs-lookup"><span data-stu-id="ade30-133">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to track the synchronization in the data entities.</span></span>
- <span data-ttu-id="ade30-134">Sprendime „Finance and Operations“ pardavimo užsakymą reikia patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="ade30-134">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="ade30-135">Su „Sales“ sinchronizuojami tik patvirtinti pardavimo užsakymai arba pardavimo užsakymai, kurių apdorojimo būsena aukštesnė, pavyzdžiui, **Išsiųsta** arba **Išrašyta SF**.</span><span class="sxs-lookup"><span data-stu-id="ade30-135">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="ade30-136">Sukūrus arba modifikavus pardavimo užsakymą, „Finance and Operations“ reikia vykdyti paketinę užduotį **Skaičiuoti bendrąsias pardavimo sumas**.</span><span class="sxs-lookup"><span data-stu-id="ade30-136">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="ade30-137">Su „Sales“ bus sinchronizuojami tik tie pardavimo užsakymai, kuriuose apskaičiuotos bendrosios pardavimo sumos.</span><span class="sxs-lookup"><span data-stu-id="ade30-137">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="ade30-138">Šiuo metu su pardavimo užsakymo antraštės išlaidomis susijęs mokestis į sinchronizavimo iš „Finance and Operations“ į „Sales“ procesą nėra įtraukiamas.</span><span class="sxs-lookup"><span data-stu-id="ade30-138">Currently, tax that is related to charges on the sales order header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="ade30-139">„Sales“ nepalaikoma mokesčių informacija antraštės lygyje.</span><span class="sxs-lookup"><span data-stu-id="ade30-139">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="ade30-140">Tačiau su išlaidomis eilutės lygyje susijęs mokestis yra įtraukiamas į sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="ade30-140">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="ade30-141">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="ade30-141">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="ade30-142">Į objektą **Užsakymas** įtraukiami nauji toliau nurodyti laukai, rodomi puslapyje.</span><span class="sxs-lookup"><span data-stu-id="ade30-142">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="ade30-143">**Tvarkomas išoriškai** – šią parinktį nustatykite į **Taip**, kai užsakymas yra iš „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="ade30-143">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="ade30-144">**Apdorojimo būsena** – šiame lauke rodoma „Finance and Operations“ užsakymo apdorojimo būsena.</span><span class="sxs-lookup"><span data-stu-id="ade30-144">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="ade30-145">Galimos šios vertės:</span><span class="sxs-lookup"><span data-stu-id="ade30-145">The following values are available:</span></span>

    - <span data-ttu-id="ade30-146">Aktyvu</span><span class="sxs-lookup"><span data-stu-id="ade30-146">Active</span></span>
    - <span data-ttu-id="ade30-147">Pritarta</span><span class="sxs-lookup"><span data-stu-id="ade30-147">Confirmed</span></span>
    - <span data-ttu-id="ade30-148">Važtaraštis</span><span class="sxs-lookup"><span data-stu-id="ade30-148">Packing Slip</span></span>
    - <span data-ttu-id="ade30-149">SF išrašyta</span><span class="sxs-lookup"><span data-stu-id="ade30-149">Invoiced</span></span>
    - <span data-ttu-id="ade30-150">Paimta</span><span class="sxs-lookup"><span data-stu-id="ade30-150">Picked</span></span>
    - <span data-ttu-id="ade30-151">Iš dalies paimtas</span><span class="sxs-lookup"><span data-stu-id="ade30-151">Partially Picked</span></span>
    - <span data-ttu-id="ade30-152">Iš dalies supakuotas</span><span class="sxs-lookup"><span data-stu-id="ade30-152">Partially Packed</span></span>
    - <span data-ttu-id="ade30-153">Išsiųsta</span><span class="sxs-lookup"><span data-stu-id="ade30-153">Shipped</span></span>
    - <span data-ttu-id="ade30-154">Iš dalies išsiųstas</span><span class="sxs-lookup"><span data-stu-id="ade30-154">Partially Shipped</span></span>
    - <span data-ttu-id="ade30-155">Iš dalies išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="ade30-155">Partially Invoiced</span></span>
    - <span data-ttu-id="ade30-156">Atšaukta</span><span class="sxs-lookup"><span data-stu-id="ade30-156">Cancelled</span></span>

<span data-ttu-id="ade30-157">Parametras **Sudaro tik išoriškai tvarkomi produktai** naudojamas kitose su pardavimo užsakymu susijusiose situacijose (pavyzdžiui, sinchronizuojant iš „Sales“ į „Finance and Operations“), kad būtų nuosekliai sekama, ar pardavimo užsakymą sudaro vien tik Išoriškai tvarkomi produktai.</span><span class="sxs-lookup"><span data-stu-id="ade30-157">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (for example, synchronization from Sales to Finance and Operation) to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="ade30-158">Jei pardavimo užsakymą sudaro tik išoriškai tvarkomi produktai, produktai tvarkomi „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="ade30-158">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="ade30-159">Šis parametras padeda užtikrinti, kad nebandysite sinchronizuoti pardavimo užsakymo eilučių, kuriose pateikti „Finance and Operations“ neatpažįstami produktai.</span><span class="sxs-lookup"><span data-stu-id="ade30-159">This setting helps guarantee that you don't try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="ade30-160">Išoriškai tvarkomuose užsakymuose puslapio **Pardavimo užsakymas** mygtukai **Kurti sąskaitą faktūrą**, **Atšaukti užsakymą**, **Perskaičiuoti**, **Gauti produktų** ir **Peržvelgti adresą** yra paslėpti, nes sąskaitos faktūros bus kuriamos sprendime „Finance and Operations“ ir sinchronizuojamos su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="ade30-160">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="ade30-161">Užsakymo puslapio numerio redaguoti negalima, nes pardavimo užsakymo informacija bus sinchronizuojama su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="ade30-161">The order page can't be edited, because sales order information will be synchronized from Finance and Operations.</span></span>

<span data-ttu-id="ade30-162">Pardavimo užsakymo būsena liks **aktyvi**, kad padėtų užtikrinti, jog keitimai iš „Finance and Operations“ galėtų būti perkelti į „Sales“ pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="ade30-162">The status of a sales order will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="ade30-163">Norėdami valdyti šią veikseną, numatytąją **Būsenos kodas \[Būsena\]** reikšmę projekte Duomenų integravimas nustatykite į **Aktyvu**.</span><span class="sxs-lookup"><span data-stu-id="ade30-163">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="ade30-164">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="ade30-164">Preconditions and mapping setup</span></span>

<span data-ttu-id="ade30-165">Prieš sinchronizuojant pardavimo užsakymus, svarbu atnaujinti toliau nurodytus sistemų parametrus.</span><span class="sxs-lookup"><span data-stu-id="ade30-165">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="ade30-166">Sąranka sprendime „Sales“</span><span class="sxs-lookup"><span data-stu-id="ade30-166">Setup in Sales</span></span>

- <span data-ttu-id="ade30-167">Įsitikinkite, kad komandai, kuriai priskirtas vartotojas iš „Sales“ ryšio rinkinio, nustatytos teisės.</span><span class="sxs-lookup"><span data-stu-id="ade30-167">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="ade30-168">Jei naudojate demonstracinius duomenis, prieiga paprastai suteikiama vartotojui, bet ne komandai.</span><span class="sxs-lookup"><span data-stu-id="ade30-168">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="ade30-169">Jei komanda taip pat neturės administratoriaus prieigos, vykdydami Duomenų integravimo projektą gausite klaidos pranešimą, kad trūksta pagrindinės komandos.</span><span class="sxs-lookup"><span data-stu-id="ade30-169">If the team doesn't also have admin access, when you run the project from Data integration, you will receive an error message that states that Principal team is missing.</span></span>

    <span data-ttu-id="ade30-170">Eikite į **Parametrai** > **Sauga** > **Komandos**, pasirinkite reikiamą komandą, pasirinkite **Valdyti vaidmenis** ir pasirinkite vaidmenį, kuriam suteiktos norimos teisės, pvz., **Sistemos administratorius**.</span><span class="sxs-lookup"><span data-stu-id="ade30-170">Go to **Settings** > **Security** > **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="ade30-171">Eikite į **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimai** ir įsitikinkite, kad naudojami toliau nurodyti parametrai.</span><span class="sxs-lookup"><span data-stu-id="ade30-171">Go to **Settings** > **Administration** > **System settings** > **Sales**, and makes sure that the following settings are used:</span></span>

    - <span data-ttu-id="ade30-172">Parinktis **Naudoti sistemos prizų skaičiavimo sistemą** nustatyta į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ade30-172">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="ade30-173">Laukas **Nuolaidos skaičiavimo būdas** nustatytas į **Eilutės elementas**.</span><span class="sxs-lookup"><span data-stu-id="ade30-173">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="ade30-174">Sąranka sprendime „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="ade30-174">Setup in Finance and Operations</span></span>

<span data-ttu-id="ade30-175">Eikite į **Pardavimas ir rinkodara** > **Periodinės užduotys** > **Skaičiuoti bendrąsias pardavimo sumas** ir nustatykite, kad užduotis būtų vykdoma kaip paketinė užduotis.</span><span class="sxs-lookup"><span data-stu-id="ade30-175">Go to **Sales and marketing** > **Periodic tasks** > **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="ade30-176">Parinktį **Skaičiuoti bendrąsias pardavimo užsakymų sumas** nustatykite į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ade30-176">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="ade30-177">Šis veiksmas svarbus, nes su „Sales“ bus sinchronizuojami tik tie pardavimo užsakymai, kuriuose bus apskaičiuotos bendrosios pardavimo sumos.</span><span class="sxs-lookup"><span data-stu-id="ade30-177">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="ade30-178">Paketinės užduoties dažnumas turi būti lygus pardavimo užsakymų sinchronizavimo dažnumui.</span><span class="sxs-lookup"><span data-stu-id="ade30-178">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="ade30-179">Sąranka projekte Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="ade30-179">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="ade30-180">SalesHeader užduotis</span><span class="sxs-lookup"><span data-stu-id="ade30-180">SalesHeader task</span></span>

- <span data-ttu-id="ade30-181">Įsitikinkite, kad yra reikiamas **InvoiceCountryRegionId** susiejimas su **BillingAddress\_Country** ir **DeliveryCountryRegionId** susiejimas su **DeliveryAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="ade30-181">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country** and for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="ade30-182">Šablono vertė yra vertės schema, kurioje susieta keletas šalių ar regionų.</span><span class="sxs-lookup"><span data-stu-id="ade30-182">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="ade30-183">Norint sprendime „Sales“ kurti užsakymus, reikalingas Kainoraštis.</span><span class="sxs-lookup"><span data-stu-id="ade30-183">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="ade30-184">Dalyje **pricelevelid.name \[Kainoraščio pavadinimas\]** kiekvienos valiutos vertės schemą atnaujinkite į sprendime „Sales“ naudojamą kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="ade30-184">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="ade30-185">Kiekvienai valiutai galite naudoti numatytąjį kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="ade30-185">You can use the default price list for a single currency.</span></span> <span data-ttu-id="ade30-186">Taip pat, jei turite kainoraščių keliomis valiutomis, galite naudoti vertės schemą.</span><span class="sxs-lookup"><span data-stu-id="ade30-186">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="ade30-187">Numatytoji **pricelevelid.name \[Kainoraščio pavadinimas\]** šablono reikšmė yra **„CRM Service USA“ (pavyzdys)**.</span><span class="sxs-lookup"><span data-stu-id="ade30-187">The default template value for **pricelevelid.name \[Price list name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="ade30-188">SalesLine užduotis</span><span class="sxs-lookup"><span data-stu-id="ade30-188">SalesLine task</span></span>

- <span data-ttu-id="ade30-189">Įsitikinkite, kad yra reikiamas **DeliveryCountryRegionId** susiejimas su **DeliveryAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="ade30-189">Make sure that the required mapping exists for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="ade30-190">Šablono vertė yra vertės schema, kurioje susieta keletas šalių ar regionų.</span><span class="sxs-lookup"><span data-stu-id="ade30-190">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="ade30-191">Įsitikinkite, kad „Finance and Operations“ yra **SalesUnitSymbol** būtina verčių schema.</span><span class="sxs-lookup"><span data-stu-id="ade30-191">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="ade30-192">Šablono vertė, kurioje yra vertės schema, apibrėžta **SalesUnitSymbol** su **Quantity\_UOM**.</span><span class="sxs-lookup"><span data-stu-id="ade30-192">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ade30-193">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="ade30-193">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="ade30-194">Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti.</span><span class="sxs-lookup"><span data-stu-id="ade30-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="ade30-195">Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.</span><span class="sxs-lookup"><span data-stu-id="ade30-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="ade30-196">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="ade30-196">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="ade30-197">Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="ade30-197">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="orderheader"></a><span data-ttu-id="ade30-198">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="ade30-198">OrderHeader</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a><span data-ttu-id="ade30-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="ade30-200">OrderLine</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="ade30-202">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="ade30-202">Related topics</span></span>

[<span data-ttu-id="ade30-203">Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="ade30-203">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="ade30-204">Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Finance and Operations“ klientais</span><span class="sxs-lookup"><span data-stu-id="ade30-204">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="ade30-205">Tiesioginis „Finance and Operations“ produktų sinchronizavimas su „Sales“ produktais</span><span class="sxs-lookup"><span data-stu-id="ade30-205">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="ade30-206">Tiesioginis „Sales“ kontaktų sinchronizavimas su „Finance and Operations“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="ade30-206">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="ade30-207">Tiesioginis „Finance and Operations“ pardavimo sąskaitų faktūrų antraščių ir eilučių sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="ade30-207">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




