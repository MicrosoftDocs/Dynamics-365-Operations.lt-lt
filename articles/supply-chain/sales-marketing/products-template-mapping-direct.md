---
title: Tiesioginis produktų sinchronizavimas naudojant „Supply Chain Management” su „Sales“ produktais
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojamos „Dynamics 365 Supply Chain Management“ produktus sinchronizuojant su „Dynamics 365 Sales“.
author: ChristianRytt
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 29bb9d05aa939ec82595e153faf03f290e219589
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817826"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a><span data-ttu-id="f49f3-103">Tiesioginis produktų sinchronizavimas naudojant „Supply Chain Management” su „Sales“ produktais</span><span class="sxs-lookup"><span data-stu-id="f49f3-103">Synchronize products directly from Supply Chain Management to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="f49f3-104">Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [Duomenų integravimas į „Microsoft Dataverse“, skirtą programoms](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="f49f3-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="f49f3-105">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojamos „Dynamics 365 Supply Chain Management“ produktus tiesiogiai sinchronizuojant su „Dynamics 365 Sales“.</span><span class="sxs-lookup"><span data-stu-id="f49f3-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="f49f3-106">Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="f49f3-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="f49f3-107">Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Supply Chain Management“ ir „Sales“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="f49f3-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="f49f3-108">Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Supply Chain Management“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus.</span><span class="sxs-lookup"><span data-stu-id="f49f3-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="f49f3-109">Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami „Supply Chain Management “ ir „Sales“ duomenys.</span><span class="sxs-lookup"><span data-stu-id="f49f3-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="f49f3-110">[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="f49f3-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="f49f3-111">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="f49f3-111">Templates and tasks</span></span>

<span data-ttu-id="f49f3-112">Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„Power Apps“ administravimo centrą](https://admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="f49f3-112">To access the available templates, open [Power Apps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="f49f3-113">Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="f49f3-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="f49f3-114">Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami sinchronizuojant „Supply Chain Management” produktus su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="f49f3-114">The following template and underlying tasks are used to synchronize products from Supply Chain Management to Sales.</span></span>

- <span data-ttu-id="f49f3-115">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** Produktai (iš „Supply Chain Management” į „Sales“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="f49f3-115">**Name of the template in Data integration:** Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="f49f3-116">**Užduoties pavadinimas projekte Duomenų integravimas:** Produktai</span><span class="sxs-lookup"><span data-stu-id="f49f3-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="f49f3-117">Prieš sinchronizuojant produktą, nereikia atlikti jokių sinchronizavimo užduočių.</span><span class="sxs-lookup"><span data-stu-id="f49f3-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="f49f3-118">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="f49f3-118">Entity set</span></span>

| <span data-ttu-id="f49f3-119">„Supply Chain Management”</span><span class="sxs-lookup"><span data-stu-id="f49f3-119">Supply Chain Management</span></span>    | <span data-ttu-id="f49f3-120">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="f49f3-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="f49f3-121">Parduodami išleisti produktai</span><span class="sxs-lookup"><span data-stu-id="f49f3-121">Sellable released products</span></span> | <span data-ttu-id="f49f3-122">Produktai</span><span class="sxs-lookup"><span data-stu-id="f49f3-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="f49f3-123">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="f49f3-123">Entity flow</span></span>

<span data-ttu-id="f49f3-124">Produktai tvarkomi „Supply Chain Management” ir sinchronizuojami su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="f49f3-124">Products are managed in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="f49f3-125">„Supply Chain Management” duomenų objektas **Parduodami patvirtinti produktai** eksportuoja tik *parduodamus* produktus.</span><span class="sxs-lookup"><span data-stu-id="f49f3-125">The **Sellable released products** data entity in Supply Chain Management exports only products that are *sellable*.</span></span> <span data-ttu-id="f49f3-126">Parduodami produktai – tai produktai, apie kuriuos pateikta informacija, reikalinga norint produktus naudoti pardavimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="f49f3-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="f49f3-127">Tos pačios taisyklės taikomos, kai produktas patvirtinamas naudojant puslapio **Patvirtintas produktas** funkciją **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="f49f3-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="f49f3-128">Produkto numeris naudojamas kaip raktas.</span><span class="sxs-lookup"><span data-stu-id="f49f3-128">The product number is used as a key.</span></span> <span data-ttu-id="f49f3-129">Todėl produkto variantus susinchronizavus su „Sales“, kiekvienam produkto variantui priskiriamas atskiras produkto ID.</span><span class="sxs-lookup"><span data-stu-id="f49f3-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="f49f3-130">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="f49f3-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="f49f3-131">Į „Sales“ įtrauktas naujas produktų laukas **Tvarkomas išoriškai**, kad būtų galima nurodyti, jog tam tikras produktas yra tvarkomas išoriškai.</span><span class="sxs-lookup"><span data-stu-id="f49f3-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="f49f3-132">Pagal numatytuosius nustatymus, importuojant į „Sales“ reikšmė nustatoma į parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="f49f3-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="f49f3-133">Galimos šios vertės:</span><span class="sxs-lookup"><span data-stu-id="f49f3-133">The following values are available:</span></span>

- <span data-ttu-id="f49f3-134">**Taip** – produktas paimtas iš „Supply Chain Management” ir jo nebus galima redaguoti sprendime „Sales“.</span><span class="sxs-lookup"><span data-stu-id="f49f3-134">**Yes** – The product originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="f49f3-135">**Ne** – produktas į „Sales“ buvo įtrauktas tiesiogiai.</span><span class="sxs-lookup"><span data-stu-id="f49f3-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="f49f3-136">**(Tuščia)** – prieš įgalinant sprendimą Potencialūs klientai ir grynieji pinigai, produktas teikiamas sprendime „Sales“.</span><span class="sxs-lookup"><span data-stu-id="f49f3-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="f49f3-137">Laukas **Tvarkomas išoriškai** padeda užtikrinti, kad su „Supply Chain Management” bus sinchronizuojami tik pasiūlymai ir pardavimo užsakymai, kuriuose yra išoriškai tvarkomų produktų.</span><span class="sxs-lookup"><span data-stu-id="f49f3-137">The **Is Externally Maintained** field helps ensure that only quotations and sales orders that have externally maintained products will be synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="f49f3-138">Išoriškai tvarkomi produktai automatiškai įtraukiami į pirmąjį tinkamą kainoraštį ta pačia valiuta.</span><span class="sxs-lookup"><span data-stu-id="f49f3-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="f49f3-139">Kainoraščiai išrikiuojami abėcėlės tvarka pagal pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="f49f3-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="f49f3-140">„Supply Chain Management” produkto pardavimo kaina naudojama kaip kainoraščio kaina.</span><span class="sxs-lookup"><span data-stu-id="f49f3-140">The product sales price from Supply Chain Management is used as the price on the price list.</span></span> <span data-ttu-id="f49f3-141">Todėl „Sales“ turi būti pateiktas kainoraštis, atitinkantis kiekvieno produkto pardavimo valiutą „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="f49f3-141">Therefore, there must be a price list in Sales for every product sales currency in Supply Chain Management.</span></span> <span data-ttu-id="f49f3-142">Patvirtintų parduodamų produktų valiuta nustatyta į juridinio subjekto, iš kurio produktas eksportuojamas, apskaitos valiutą.</span><span class="sxs-lookup"><span data-stu-id="f49f3-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="f49f3-143">Jei nebus valiutą atitinkančio kainoraščio, produktų sinchronizuoti nepavyks.</span><span class="sxs-lookup"><span data-stu-id="f49f3-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="f49f3-144">Naudojamą kainoraštį su integracija galite valdyti projekte Duomenų integravimas susieję pricelevelid.name [Numatytasis kainoraštis (pavadinimas)].</span><span class="sxs-lookup"><span data-stu-id="f49f3-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="f49f3-145">Visą įvestį turi sudaryti mažosios raidės.</span><span class="sxs-lookup"><span data-stu-id="f49f3-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="f49f3-146">Pavyzdžiui, numatytoji „Sales“ kainoraščio pavadinimu „Standartinis“ reikšmė būtų: Paskirties laukas: pricelevelid.name [Numatytasis kainoraštis (pavadinimas)], o Susiejimo tipas: [ { "transformType": "Default", "defaultValue": "standard" } ].</span><span class="sxs-lookup"><span data-stu-id="f49f3-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="f49f3-147">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="f49f3-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="f49f3-148">Prieš sinchronizuojant pirmą kartą, Išskirtųjų produktų lentelė turi būti užpildyta naudojant esamus produktus „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="f49f3-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Supply Chain Management.</span></span> <span data-ttu-id="f49f3-149">Esami produktai nebus sinchronizuojami, kol ši užduotis nebus baigta.</span><span class="sxs-lookup"><span data-stu-id="f49f3-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="f49f3-150">„Supply Chain Management” naudokite parinktį Ieška, norėdami rasti parinktį **Automatiškai įvesti išskirtųjų produktų lentelę**.</span><span class="sxs-lookup"><span data-stu-id="f49f3-150">In Supply Chain Management, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="f49f3-151">Norėdami vykdyti užduotį pasirinkite **Automatiškai įvesti išskirtųjų produktų lentelę**.</span><span class="sxs-lookup"><span data-stu-id="f49f3-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="f49f3-152">Šią užduotį reikia vykdyti tik vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="f49f3-152">This job must be run only one time.</span></span>

- <span data-ttu-id="f49f3-153">Įsitikinkite, kad susiejime **SalesUnitSymbol** į **DefaultUnit (pavadinimas)** tarp „Supply Chain Management” ir „Sales“ yra būtina pardavimo matavimo vieneto (MV) reikšmių schema.</span><span class="sxs-lookup"><span data-stu-id="f49f3-153">Make sure that the required value map for the selling unit of measure (UOM) between Supply Chain Management and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="f49f3-154">Atnaujinkite **vienetų grupės** (**defaultuomscheduleid.name**) reikšmių schemą, kad ji atitiktų „Sales“ **vienetų grupes**.</span><span class="sxs-lookup"><span data-stu-id="f49f3-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="f49f3-155">Numatytoji šablono reikšmė yra **Numatytasis vienetas**.</span><span class="sxs-lookup"><span data-stu-id="f49f3-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="f49f3-156">Įsitikinkite, kad visų „Supply Chain Management” produktų pardavimo MV pateikiami „Sales“.</span><span class="sxs-lookup"><span data-stu-id="f49f3-156">Make sure that the selling UOMs for all products from Supply Chain Management exist in Sales.</span></span>
- <span data-ttu-id="f49f3-157">Įsitikinkite, kad „Sales“ nustatyti kainoraščiai, atitinkantys kiekvieno produkto pardavimo valiutą „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="f49f3-157">Make sure that price lists exist in Sales for every product sales currency in Supply Chain Management.</span></span>
- <span data-ttu-id="f49f3-158">„Sales“ sukūrus produktų, jiems gali būti suteikta būsena **Juodraštis** arba **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="f49f3-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="f49f3-159">Veikimas valdomas „Sales“ parinktyje **Parametrai** > **Administravimas** > **Sistemos parametrai** > **Pardavimas**.</span><span class="sxs-lookup"><span data-stu-id="f49f3-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="f49f3-160">Sukūrus būsenos **Juodraštis** produktų, šie turi būti suaktyvinti prieš tai, kai juos galima įtraukti į pasiūlymus arba pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="f49f3-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f49f3-161">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="f49f3-161">Template mapping in Data integration</span></span>

<span data-ttu-id="f49f3-162">Toliau pateiktoje iliustracijoje vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="f49f3-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="f49f3-163">Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="f49f3-163">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="f49f3-165">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="f49f3-165">Related topics</span></span>

[<span data-ttu-id="f49f3-166">Potencialaus kliento pavertimas pinigais</span><span class="sxs-lookup"><span data-stu-id="f49f3-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="f49f3-167">Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Supply Chain Management“ klientais</span><span class="sxs-lookup"><span data-stu-id="f49f3-167">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="f49f3-168">Tiesioginis „Sales“ kontaktų sinchronizavimas su „Supply Chain Management“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="f49f3-168">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="f49f3-169">Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir „Supply Chain Management”</span><span class="sxs-lookup"><span data-stu-id="f49f3-169">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="f49f3-170">Tiesioginis „Supply Chain Management“ pardavimo SF antraščių ir eilučių sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="f49f3-170">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]