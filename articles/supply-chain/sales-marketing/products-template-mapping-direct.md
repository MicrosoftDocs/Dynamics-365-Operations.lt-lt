---
title: "Tiesioginis „Finance and Operations“ produktų sinchronizavimas su „Sales“ produktais"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ produktus sinchronizuojant su Microsoft Dynamics 365 for Sales“."
author: ChristianRytt
manager: AnnBe
ms.date: 06/25/2018
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
ms.sourcegitcommit: 03bab1d03be71c0e23a6ea93f542d6a52a212a1f
ms.openlocfilehash: 66506953790fd77c2105591d3211c76991eced08
ms.contentlocale: lt-lt
ms.lasthandoff: 06/25/2018

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="d91dd-103">Tiesioginis „Finance and Operations“ produktų sinchronizavimas su „Sales“ produktais</span><span class="sxs-lookup"><span data-stu-id="d91dd-103">Synchronize products directly from Finance and Operations to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="d91dd-104">Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [„Dynamics 365“ duomenų integravimo funkcija](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="d91dd-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="d91dd-105">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ produktus sinchronizuojant tiesiogiai su „Microsoft Dynamics 365 for Sales“.</span><span class="sxs-lookup"><span data-stu-id="d91dd-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="d91dd-106">Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="d91dd-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="d91dd-107">Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Finance and Operations“ ir „Sales“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="d91dd-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="d91dd-108">Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus.</span><span class="sxs-lookup"><span data-stu-id="d91dd-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="d91dd-109">Toliau pateiktoje iliustracijoje rodoma, kaip duomenys sinchronizuojami tarp „Finance and Operations“ ir „Sales“.</span><span class="sxs-lookup"><span data-stu-id="d91dd-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="d91dd-110">[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="d91dd-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d91dd-111">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="d91dd-111">Templates and tasks</span></span>

<span data-ttu-id="d91dd-112">Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„PowerApps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="d91dd-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="d91dd-113">Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="d91dd-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="d91dd-114">Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami sinchronizuojant „Finance and Operations“ produktus su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="d91dd-114">The following template and underlying tasks are used to synchronize products from Finance and Operations to Sales.</span></span>

- <span data-ttu-id="d91dd-115">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="d91dd-115">**Name of the template in Data integration:** Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="d91dd-116">**Užduoties pavadinimas projekte Duomenų integravimas:** Produktai</span><span class="sxs-lookup"><span data-stu-id="d91dd-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="d91dd-117">Prieš sinchronizuojant produktą, nereikia atlikti jokių sinchronizavimo užduočių.</span><span class="sxs-lookup"><span data-stu-id="d91dd-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="d91dd-118">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="d91dd-118">Entity set</span></span>

| <span data-ttu-id="d91dd-119">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="d91dd-119">Finance and Operations</span></span>     | <span data-ttu-id="d91dd-120">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="d91dd-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="d91dd-121">Parduodami išleisti produktai</span><span class="sxs-lookup"><span data-stu-id="d91dd-121">Sellable released products</span></span> | <span data-ttu-id="d91dd-122">Produktai</span><span class="sxs-lookup"><span data-stu-id="d91dd-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="d91dd-123">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="d91dd-123">Entity flow</span></span>

<span data-ttu-id="d91dd-124">Produktai tvarkomi „Finance and Operations“ ir sinchronizuojami su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="d91dd-124">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="d91dd-125">„Finance and Operations“ duomenų objektas **Parduodami patvirtinti produktai** eksportuoja tik *parduodamus* produktus.</span><span class="sxs-lookup"><span data-stu-id="d91dd-125">The **Sellable released products** data entity in Finance and Operations exports only products that are *sellable*.</span></span> <span data-ttu-id="d91dd-126">Parduodami produktai – tai produktai, apie kuriuos pateikta informacija, reikalinga norint produktus naudoti pardavimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="d91dd-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="d91dd-127">Tos pačios taisyklės taikomos, kai produktas patvirtinamas naudojant puslapio **Patvirtintas produktas** funkciją **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="d91dd-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="d91dd-128">Produkto numeris naudojamas kaip raktas.</span><span class="sxs-lookup"><span data-stu-id="d91dd-128">The product number is used as a key.</span></span> <span data-ttu-id="d91dd-129">Todėl produkto variantus susinchronizavus su „Sales“, kiekvienam produkto variantui priskiriamas atskiras produkto ID.</span><span class="sxs-lookup"><span data-stu-id="d91dd-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="d91dd-130">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="d91dd-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="d91dd-131">Į „Sales“ įtrauktas naujas produktų laukas **Tvarkomas išoriškai**, kad būtų galima nurodyti, jog tam tikras produktas yra tvarkomas išoriškai.</span><span class="sxs-lookup"><span data-stu-id="d91dd-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="d91dd-132">Pagal numatytuosius nustatymus, importuojant į „Sales“ reikšmė nustatoma į parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="d91dd-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="d91dd-133">Galimos šios vertės:</span><span class="sxs-lookup"><span data-stu-id="d91dd-133">The following values are available:</span></span>

- <span data-ttu-id="d91dd-134">**Taip** – produktas paimtas iš „Finance and Operations“ ir jo nebus galima redaguoti sprendime „Sales“.</span><span class="sxs-lookup"><span data-stu-id="d91dd-134">**Yes** – The product originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="d91dd-135">**Ne** – produktas į „Sales“ buvo įtrauktas tiesiogiai.</span><span class="sxs-lookup"><span data-stu-id="d91dd-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="d91dd-136">**(Tuščia)** – prieš įgalinant sprendimą Potencialūs klientai ir grynieji pinigai, produktas teikiamas sprendime „Sales“.</span><span class="sxs-lookup"><span data-stu-id="d91dd-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="d91dd-137">Laukas **Tvarkomas išoriškai** padeda užtikrinti, kad su „Finance and Operations“ bus sinchronizuojami tik pasiūlymai ir pardavimo užsakymai, kuriuose yra išoriškai tvarkomų produktų.</span><span class="sxs-lookup"><span data-stu-id="d91dd-137">The **Is Externally Maintained** field helps guarantee that only quotations and sales orders that have externally maintained products will be synchronized to Finance and Operations.</span></span>

<span data-ttu-id="d91dd-138">Išoriškai tvarkomi produktai automatiškai įtraukiami į pirmąjį tinkamą kainoraštį ta pačia valiuta.</span><span class="sxs-lookup"><span data-stu-id="d91dd-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="d91dd-139">Kainoraščiai išrikiuojami abėcėlės tvarka pagal pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="d91dd-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="d91dd-140">„Finance and Operations“ produkto pardavimo kaina naudojama kaip kainoraščio kaina.</span><span class="sxs-lookup"><span data-stu-id="d91dd-140">The product sales price from Finance and Operations is used as the price on the price list.</span></span> <span data-ttu-id="d91dd-141">Todėl „Sales“ turi būti pateiktas kainoraštis, atitinkantis kiekvieno produkto pardavimo valiutą „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="d91dd-141">Therefore, there must be a price list in Sales for every product sales currency in Finance and Operations.</span></span> <span data-ttu-id="d91dd-142">Patvirtintų parduodamų produktų valiuta nustatyta į juridinio subjekto, iš kurio produktas eksportuojamas, apskaitos valiutą.</span><span class="sxs-lookup"><span data-stu-id="d91dd-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="d91dd-143">Jei nebus valiutą atitinkančio kainoraščio, produktų sinchronizuoti nepavyks.</span><span class="sxs-lookup"><span data-stu-id="d91dd-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="d91dd-144">Naudojamą kainoraštį su integracija galite valdyti projekte Duomenų integravimas susieję pricelevelid.name [Numatytasis kainoraštis (pavadinimas)].</span><span class="sxs-lookup"><span data-stu-id="d91dd-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="d91dd-145">Visą įvestį turi sudaryti mažosios raidės.</span><span class="sxs-lookup"><span data-stu-id="d91dd-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="d91dd-146">Pavyzdžiui, numatytoji „Sales“ kainoraščio pavadinimu „Standartinis“ reikšmė būtų: Paskirties laukas: pricelevelid.name [Numatytasis kainoraštis (pavadinimas)], o Susiejimo tipas: [ { "transformType": "Default", "defaultValue": "standard" } ].</span><span class="sxs-lookup"><span data-stu-id="d91dd-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="d91dd-147">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="d91dd-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="d91dd-148">Prieš sinchronizuojant pirmą kartą, Išskirtųjų produktų lentelė turi būti užpildyta naudojant „Finance and Operations“ esamus produktus.</span><span class="sxs-lookup"><span data-stu-id="d91dd-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Finance and Operations.</span></span> <span data-ttu-id="d91dd-149">Esami produktai nebus sinchronizuojami, kol ši užduotis nebus baigta.</span><span class="sxs-lookup"><span data-stu-id="d91dd-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="d91dd-150">„Finance and Operations“ naudokite parinktį Ieška, norėdami rasti parinktį **Automatiškai įvesti išskirtųjų produktų lentelę**.</span><span class="sxs-lookup"><span data-stu-id="d91dd-150">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="d91dd-151">Norėdami vykdyti užduotį pasirinkite **Automatiškai įvesti išskirtųjų produktų lentelę**.</span><span class="sxs-lookup"><span data-stu-id="d91dd-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="d91dd-152">Šią užduotį reikia vykdyti tik vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="d91dd-152">This job must be run only one time.</span></span>

- <span data-ttu-id="d91dd-153">Įsitikinkite, kad susiejime **SalesUnitSymbol** į **DefaultUnit (pavadinimas)** tarp „Finance and Operations“ ir „Sales“ yra būtina pardavimo matavimo vieneto (MV) reikšmių schema.</span><span class="sxs-lookup"><span data-stu-id="d91dd-153">Make sure that the required value map for the selling unit of measure (UOM) between Finance and Operations and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="d91dd-154">Atnaujinkite **vienetų grupės** (**defaultuomscheduleid.name**) reikšmių schemą, kad ji atitiktų „Sales“ **vienetų grupes**.</span><span class="sxs-lookup"><span data-stu-id="d91dd-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="d91dd-155">Numatytoji šablono reikšmė yra **Numatytasis vienetas**.</span><span class="sxs-lookup"><span data-stu-id="d91dd-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="d91dd-156">Įsitikinkite, kad visų „Finance and Operations“ produktų pardavimo MV pateikiami „Sales“.</span><span class="sxs-lookup"><span data-stu-id="d91dd-156">Make sure that the selling UOMs for all products from Finance and Operations exist in Sales.</span></span>
- <span data-ttu-id="d91dd-157">Įsitikinkite, kad „Sales“ nustatyti kainoraščiai, atitinkantys kiekvieno produkto pardavimo valiutą „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="d91dd-157">Make sure that price lists exist in Sales for every product sales currency in Finance and Operations.</span></span>
- <span data-ttu-id="d91dd-158">„Sales“ sukūrus produktų, jiems gali būti suteikta būsena **Juodraštis** arba **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="d91dd-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="d91dd-159">Veikimas valdomas „Sales“ parinktyje **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimas**.</span><span class="sxs-lookup"><span data-stu-id="d91dd-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="d91dd-160">Sukūrus būsenos **Juodraštis** produktų, šie turi būti suaktyvinti prieš tai, kai juos galima įtraukti į pasiūlymus arba pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="d91dd-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d91dd-161">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="d91dd-161">Template mapping in Data integration</span></span>

<span data-ttu-id="d91dd-162">Toliau pateiktoje iliustracijoje vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="d91dd-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="d91dd-163">Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="d91dd-163">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="d91dd-165">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="d91dd-165">Related topics</span></span>

[<span data-ttu-id="d91dd-166">Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="d91dd-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="d91dd-167">Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Finance and Operations“ klientais</span><span class="sxs-lookup"><span data-stu-id="d91dd-167">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="d91dd-168">Tiesioginis „Sales“ kontaktų sinchronizavimas su „Finance and Operations“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="d91dd-168">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="d91dd-169">Tiesioginis „Finance and Operations“ pardavimo užsakymų antraščių ir eilučių sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="d91dd-169">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="d91dd-170">Tiesioginis „Finance and Operations“ pardavimo sąskaitų faktūrų antraščių ir eilučių sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="d91dd-170">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




