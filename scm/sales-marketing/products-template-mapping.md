---
title: "Sinchronizuoti „Finance and Operations“ produktus su „Sales“ produktais"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimo) produktus sinchronizuojant su „Microsoft Dynamics 365 for Sales“."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
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
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2f14b06b57930256f9211f2085512aa589df083e
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="4a512-103">Sinchronizuoti „Finance and Operations“ produktus su „Sales“ produktais</span><span class="sxs-lookup"><span data-stu-id="4a512-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="4a512-104">Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai susipažinkite su [„Dynamics 365“ duomenų integravimo funkcija](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="4a512-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="4a512-105">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimo) produktus sinchronizuojant su „Microsoft Dynamics 365 for Sales“.</span><span class="sxs-lookup"><span data-stu-id="4a512-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="4a512-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="4a512-106">Template and task</span></span>

<span data-ttu-id="4a512-107">Toliau nurodyti šablonai ir pagrindinės užduotys naudojami „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimo („Finance and Operations“) produktus sinchronizuojant su „Microsoft Dynamics 365 for Sales“.</span><span class="sxs-lookup"><span data-stu-id="4a512-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="4a512-108">Šablono pavadinimas: Produktai (iš „Finance and Operations“ į „Sales“)</span><span class="sxs-lookup"><span data-stu-id="4a512-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="4a512-109">Projekto užduoties pavadinimas: Produktai</span><span class="sxs-lookup"><span data-stu-id="4a512-109">Name of task in project: Products</span></span>

<span data-ttu-id="4a512-110">Prieš sinchronizuojant produktus būtina sinchronizuoti užduotis: Nėra</span><span class="sxs-lookup"><span data-stu-id="4a512-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="4a512-111">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="4a512-111">Entity set</span></span>

| <span data-ttu-id="4a512-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="4a512-112">**Finance and Operations**</span></span> | <span data-ttu-id="4a512-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="4a512-113">**CDS**</span></span> | <span data-ttu-id="4a512-114">**Pardavimas**</span><span class="sxs-lookup"><span data-stu-id="4a512-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="4a512-115">Parduodami išleisti produktai</span><span class="sxs-lookup"><span data-stu-id="4a512-115">Sellable released products</span></span> | <span data-ttu-id="4a512-116">Produktas</span><span class="sxs-lookup"><span data-stu-id="4a512-116">Product</span></span> | <span data-ttu-id="4a512-117">Produktai</span><span class="sxs-lookup"><span data-stu-id="4a512-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="4a512-118">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="4a512-118">Entity flow</span></span>

<span data-ttu-id="4a512-119">Produktai tvarkomi „Finance and Operations“ ir sinchronizuojami su „Sales“.</span><span class="sxs-lookup"><span data-stu-id="4a512-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="4a512-120">„Finance and Operations“ duomenų objektas **Parduodami patvirtinti produktai** eksportuoja tik parduodamus produktus, tai reiškia, kad nurodyta produktų informacija, reikalinga juos norint naudoti pardavimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="4a512-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="4a512-121">Tos pačios taisyklės taikomos, kai produktas patvirtinamas naudojant puslapio **Patvirtintas produktas** funkciją **Tikrinti**.</span><span class="sxs-lookup"><span data-stu-id="4a512-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="4a512-122">**Produkto numeris** naudojamas kaip raktas, t. y. produkto variantai sinchronizuojami su CDS ir „Sales“ naudojant atskirus **produkto varianto** **produkto ID**.</span><span class="sxs-lookup"><span data-stu-id="4a512-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="4a512-123">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="4a512-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="4a512-124">Į „Sales“ įtrauktas naujas produktų laukas **Tvarkomas išoriškai**, kad būtų galima nurodyti, jog tam tikras produktas yra tvarkomas išoriškai.</span><span class="sxs-lookup"><span data-stu-id="4a512-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="4a512-125">Pagal numatytuosius parametrus importuojant į „Sales“ reikšmė nustatyta į parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="4a512-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="4a512-126">**Tvarkomas išoriškai = Taip**: produktas paimtas iš „Finance and Operations“ ir jo nebus galima redaguoti „Sales“.</span><span class="sxs-lookup"><span data-stu-id="4a512-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="4a512-127">**Tvarkomas išoriškai = Ne**: produktas įvestas tiesiogiai į „Sales“.</span><span class="sxs-lookup"><span data-stu-id="4a512-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="4a512-128">**Tvarkomas išoriškai = Tuščia**: produktas įtrauktas į „Sales“ prieš įjungiant sprendimą Potencialūs klientai ir grynieji pinigai.</span><span class="sxs-lookup"><span data-stu-id="4a512-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="4a512-129">Parinkties **Tvarkomas išoriškai** informacija naudojama norint užtikrinti, kad su „Finance and Operations“ bus sinchronizuojami tik **Pasiūlymai** ir **Pardavimo užsakymai** su **išoriškai tvarkomais produktais**.</span><span class="sxs-lookup"><span data-stu-id="4a512-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="4a512-130">**Išoriškai tvarkomi produktai** automatiškai įtraukiami į pirmąjį tinkamą **kainoraštį** ta pačia valiuta.</span><span class="sxs-lookup"><span data-stu-id="4a512-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="4a512-131">Atkreipkite dėmesį, kad sąrašas rikiuojamas abėcėlės tvarka pagal **pavadinimą**.</span><span class="sxs-lookup"><span data-stu-id="4a512-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="4a512-132">„Finance and Operations“ produkto pardavimo kaina naudojama kaip **kainoraščio** kaina.</span><span class="sxs-lookup"><span data-stu-id="4a512-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="4a512-133">Tai reiškia, kad „Sales“ turi būti sukurtas **Kainoraštis**, skirtas kiekvienai atskirai „Finance and Operations“ **produkto pardavimo valiutai**.</span><span class="sxs-lookup"><span data-stu-id="4a512-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="4a512-134">Patvirtintų parduodamų produktų valiuta nustatyta į juridinio subjekto, iš kurio produktas eksportuojamas, apskaitos valiutą.</span><span class="sxs-lookup"><span data-stu-id="4a512-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="4a512-135">Produkto sinchronizavimo nepavyks atlikti, jei nebus valiutą atitinkančio **kainoraščio**.</span><span class="sxs-lookup"><span data-stu-id="4a512-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="4a512-136">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="4a512-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="4a512-137">Prieš sinchronizuojant pirmą kartą, **Išskirtųjų produktų lentelė** turi būti užpildyta naudojant „Finance and Operations“ esamus produktus.</span><span class="sxs-lookup"><span data-stu-id="4a512-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="4a512-138">Esami produktai nebus sinchronizuojami, kol ši užduotis nebus baigta.</span><span class="sxs-lookup"><span data-stu-id="4a512-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="4a512-139">„Finance and Operations“ naudokite parinktį Ieška, norėdami rasti parinktį **Automatiškai įvesti išskirtųjų produktų lentelę**.</span><span class="sxs-lookup"><span data-stu-id="4a512-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="4a512-140">Norėdami vykdyti užduotį spustelėkite parinktį **Automatiškai įvesti išskirtųjų produktų lentelę**.</span><span class="sxs-lookup"><span data-stu-id="4a512-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="4a512-141">Šią užduotį reikia vykdyti tik vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="4a512-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="4a512-142">Įsitikinkite, kad **Source -\> CDS susiejime (SalesUnitSymbol / DefaultSellingUnitOfMeasure**) yra būtina „Finance and Operations“ pardavimo **matavimo vieneto** (MV) **Reikšmių schema**.</span><span class="sxs-lookup"><span data-stu-id="4a512-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="4a512-143">Įsitikinkite, MV **Palaikomos dešimtainės dalys** atitinka **CD -\> Paskirties vieta** reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="4a512-143">Ensure that **Decimals supported** for UOM match your requirements in **CDS -\> Destination**.</span></span> <span data-ttu-id="4a512-144">Jei vienam MV reikia priskirti skirtingas reikšmes., tai galima atlikti naudojant vieneto **reikšmių schemą**, pvz., [kiekvienam: 0] ir [svarai: 2].</span><span class="sxs-lookup"><span data-stu-id="4a512-144">If you require different values per UOM, this can be done with **ValueMap** from Unit, for example, [Each : 0] & [Pound : 2].</span></span>

    -   <span data-ttu-id="4a512-145">Numatytoji šablono reikšmė yra 0.</span><span class="sxs-lookup"><span data-stu-id="4a512-145">Template value is defaulted to 0.</span></span>

-   <span data-ttu-id="4a512-146">Atnaujinkite **CDS organizacijos ID (Organization_OrganizationId)** dalyje **Šaltinis \> CDS**.</span><span class="sxs-lookup"><span data-stu-id="4a512-146">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="4a512-147">Numatytoji šablono reikšmė yra ORG001.</span><span class="sxs-lookup"><span data-stu-id="4a512-147">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="4a512-148">Atnaujinkite **vienetų grupės** (**defaultuomscheduleid.name**) **reikšmių schemą** dalyje **CDS -\> Paskirties vieta**, kad ji atitiktų „Sales“ **vienetų grupes**.</span><span class="sxs-lookup"><span data-stu-id="4a512-148">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="4a512-149">Numatytoji šablono reikšmė **Numatytasis vienetas**.</span><span class="sxs-lookup"><span data-stu-id="4a512-149">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="4a512-150">Naudodami **Išrinkimo dokumentai** reikšmę įsitikinkite, kad visų „Finance and Operations“ produktų pardavimo MV pateikiami „Sales“.</span><span class="sxs-lookup"><span data-stu-id="4a512-150">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="4a512-151">Įsitikinkite, „Sales“ nustatyti **Kainoraščiai**, atitinkantys kiekvieno produkto pardavimo valiutą „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="4a512-151">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="4a512-152">„Sales“ produktus galima kurti nustatant būseną **Juodraštis** arba **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="4a512-152">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="4a512-153">Tai valdoma naudojant „Sales“ **sistemos parametrus**, pateikiamus dalyje **Pardavimas**.</span><span class="sxs-lookup"><span data-stu-id="4a512-153">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="4a512-154">Produktus, sukurtus naudojant juodraščio būseną, reikia suaktyvinti, kad juos būtų galima įtraukti į **pasiūlymą** arba **pardavimo užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="4a512-154">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="4a512-155">Šablono susiejimas duomenų integratoriuje</span><span class="sxs-lookup"><span data-stu-id="4a512-155">Template mapping in data integrator</span></span>

<span data-ttu-id="4a512-156">Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.</span><span class="sxs-lookup"><span data-stu-id="4a512-156">The following illustrations show an example of a template mapping in data integrator.</span></span>

![šablono susiejimas duomenų integratoriuje](./media/products-template-mapping-data-integrator-1.png)

![produktų šablono susiejimas duomenų integratoriuje](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="4a512-159">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="4a512-159">Related topics</span></span>

[<span data-ttu-id="4a512-160">Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais</span><span class="sxs-lookup"><span data-stu-id="4a512-160">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="4a512-161">Sinchronizuoti Pardavimo kontaktus su „Finance and Operations“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="4a512-161">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="4a512-162">Sinchronizuoti pardavimo pasiūlymų antraštes ir eilutes „Sales“ su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="4a512-162">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)


