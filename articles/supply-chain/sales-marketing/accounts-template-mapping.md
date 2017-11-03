---
title: "Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ sąskaitas sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimo)."
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1fdbeaaba53cd439d9872be78b1cf67cbc5a57b9
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="f5f54-103">Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais</span><span class="sxs-lookup"><span data-stu-id="f5f54-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="f5f54-104">Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai susipažinkite su [„Dynamics 365“ duomenų integravimo funkcija](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="f5f54-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="f5f54-105">Temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales (Sales)“ sąskaitas sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimu, „Finance and Operations“).</span><span class="sxs-lookup"><span data-stu-id="f5f54-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="f5f54-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="f5f54-106">Template and task</span></span>

<span data-ttu-id="f5f54-107">Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami sinchronizuojant „Sales“ sąskaitas su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="f5f54-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="f5f54-108">**Šablono pavadinimas:** sąskaitos (iš „Sales“ į „Finance and Operations“)</span><span class="sxs-lookup"><span data-stu-id="f5f54-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="f5f54-109">**Užduoties pavadinimas projekte:** sąskaitos – sąskaita – klientai</span><span class="sxs-lookup"><span data-stu-id="f5f54-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="f5f54-110">Prieš sukuriant sąskaitą būtina sinchronizuoti užduotis / atlikti kliento sinchronizavimą: nėra</span><span class="sxs-lookup"><span data-stu-id="f5f54-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="f5f54-111">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="f5f54-111">Entity set</span></span>

| <span data-ttu-id="f5f54-112">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="f5f54-112">Sales</span></span>    | <span data-ttu-id="f5f54-113">CDS</span><span class="sxs-lookup"><span data-stu-id="f5f54-113">CDS</span></span>     | <span data-ttu-id="f5f54-114">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="f5f54-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="f5f54-115">Sąskaitos</span><span class="sxs-lookup"><span data-stu-id="f5f54-115">Accounts</span></span> | <span data-ttu-id="f5f54-116">Paskyra</span><span class="sxs-lookup"><span data-stu-id="f5f54-116">Account</span></span> | <span data-ttu-id="f5f54-117">Klientai</span><span class="sxs-lookup"><span data-stu-id="f5f54-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="f5f54-118">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="f5f54-118">Entity flow</span></span>

<span data-ttu-id="f5f54-119">Sąskaitos valdomos programoje „Sales“ ir su „Finance and Operations“ sinchronizuojamos kaip klientai.</span><span class="sxs-lookup"><span data-stu-id="f5f54-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="f5f54-120">Ypatybė **Tvarkoma išoriškai** šiems klientams nustatyta į **Taip**, kad būtų galima sekti klientus, atsirandančius iš „Sales“.</span><span class="sxs-lookup"><span data-stu-id="f5f54-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="f5f54-121">Išrašant sąskaitą faktūrą ši informacija naudojama sąskaitoms faktūros, sinchronizuojamoms su „Sales“, filtruoti.</span><span class="sxs-lookup"><span data-stu-id="f5f54-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="f5f54-122">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="f5f54-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="f5f54-123">Laukas **Sąskaitos numeris** galimas puslapyje **Sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="f5f54-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="f5f54-124">Integracijai palaikyti buvo sukurtas srities ir unikalus raktas.</span><span class="sxs-lookup"><span data-stu-id="f5f54-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="f5f54-125">Ryšių su klientais valdymo (CRM) sprendimo srities rakto funkcija gali turėti įtakos klientams, jau naudojantiems lauką **Sąskaitos numeris**, bet nenaudojantiems unikalių **Sąskaitos numerio** verčių kiekvienoje sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="f5f54-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="f5f54-126">Šiuo metu integravimo sprendimas nepalaiko šio atvejo.</span><span class="sxs-lookup"><span data-stu-id="f5f54-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="f5f54-127">Sukūrus naują sąskaitą, bet nesant vertei **Sąskaitos numeris**, ji automatiškai sugeneruojama naudojant numeraciją.</span><span class="sxs-lookup"><span data-stu-id="f5f54-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="f5f54-128">Vertę sudaro raidės **ACC**, tada didėjanti numeracija ir iš šešių simbolių sudarytas priedėlis.</span><span class="sxs-lookup"><span data-stu-id="f5f54-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="f5f54-129">Pavyzdys: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="f5f54-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="f5f54-130">Pritaikius integravimo sprendimą „Sales“ naujinimo scenarijus nustato lauką **Sąskaitos numeris** „Sales“ esamoms sąskaitoms.</span><span class="sxs-lookup"><span data-stu-id="f5f54-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="f5f54-131">Jei lauko **Sąskaitos numeris** verčių nėra, naudojama anksčiau aprašyta numeracija.</span><span class="sxs-lookup"><span data-stu-id="f5f54-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="f5f54-132">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="f5f54-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="f5f54-133">**CustomerGroupId** susiejimą iš **CDS &gt; Paskirties vieta** reikia atnaujinti į tinkamą „Finance and Operations“ reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5f54-133">**CustomerGroupId** mapping from **CDS &gt; Destination** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="f5f54-134">Galite nurodyti numatytąją vertę arba ją nustatyti naudodami verčių schemą.</span><span class="sxs-lookup"><span data-stu-id="f5f54-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="f5f54-135">Numatytoji šablono vertė yra **10**.</span><span class="sxs-lookup"><span data-stu-id="f5f54-135">The default template value is **10**.</span></span>
- <span data-ttu-id="f5f54-136">„Finance and Operations“ laukas **Adreso šalies regiono kodas** yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="f5f54-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="f5f54-137">Norėdami išvengti sinchronizavimo klaidų, susiejime iš **CDS &gt; Paskirties vieta** galite nurodyti numatytąją reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f5f54-137">To avoid synchronization errors, you can specify a default value in the mapping from **CDS &gt; Destination**.</span></span> <span data-ttu-id="f5f54-138">Tokiu atveju, jei „Sales“ laukas paliekamas tuščias, bus naudojama numatytoji reikšmė.</span><span class="sxs-lookup"><span data-stu-id="f5f54-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="f5f54-139">Numatytoji **AddressCountryRegionISOCode** šablono vertė yra **USA**.</span><span class="sxs-lookup"><span data-stu-id="f5f54-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="f5f54-140">Numatytoji **DeliveryAddressCountryRegionISOCode** šablono reikšmė vertė **USA**.</span><span class="sxs-lookup"><span data-stu-id="f5f54-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="f5f54-141">Pridėdami toliau nurodytus susiejimus iš **CDS &gt; Paskirties vietos** galite padėti sumažinti neautomatinių atnaujinimų, kurie būtini „Finance and Operations“, skaičių.</span><span class="sxs-lookup"><span data-stu-id="f5f54-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="f5f54-142">Galite naudoti numatytąją vertę arba verčių schemos vertę, pvz., **Šalis / regionas** arba **miestas**.</span><span class="sxs-lookup"><span data-stu-id="f5f54-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="f5f54-143">**SiteId** – vieta būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="f5f54-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="f5f54-144">Numatytąją vietą galima paimti iš produkto arba iš kliento užsakymo antraštės.</span><span class="sxs-lookup"><span data-stu-id="f5f54-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="f5f54-145">Numatytoji **SiteId** šablono vertė yra **1**.</span><span class="sxs-lookup"><span data-stu-id="f5f54-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="f5f54-146">**WarehouseId** – sandėlis yra būtinas norint apdoroti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="f5f54-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="f5f54-147">Numatytąjį sandėlį galima paimti iš produkto arba iš „Finance and Operations“ kliento užsakymo antraštės.</span><span class="sxs-lookup"><span data-stu-id="f5f54-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="f5f54-148">Numatytoji **WarehouseId** šablono vertė yra **13**.</span><span class="sxs-lookup"><span data-stu-id="f5f54-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="f5f54-149">**LanguageId** – kalba yra būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="f5f54-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="f5f54-150">Pagal numatytuosius nustatymus naudojama kalba iš kliento užsakymo antraštės.</span><span class="sxs-lookup"><span data-stu-id="f5f54-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="f5f54-151">Numatytoji **LanguageId** šablono vertė yra **en-us**.</span><span class="sxs-lookup"><span data-stu-id="f5f54-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="f5f54-152">Atnaujinkite CDS organizacijos ID (**Organization_OrganizationId**) dalies **Šaltinis &gt; CDS** susiejime.</span><span class="sxs-lookup"><span data-stu-id="f5f54-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="f5f54-153">Numatytoji šablono vertė yra **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f5f54-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="f5f54-154">Šablono susiejimas duomenų integratoriuje</span><span class="sxs-lookup"><span data-stu-id="f5f54-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="f5f54-155">Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti.</span><span class="sxs-lookup"><span data-stu-id="f5f54-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="f5f54-156">Norėdami susieti šiuos laukus, turite nustatyti verčių schemą.</span><span class="sxs-lookup"><span data-stu-id="f5f54-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="f5f54-157">Verčių susiejimams būdingi duomenys organizacijų, tarp kurių objektas yra sinchronizuojamas.</span><span class="sxs-lookup"><span data-stu-id="f5f54-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="f5f54-158">Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.</span><span class="sxs-lookup"><span data-stu-id="f5f54-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/accounts-template-mapping-data-integrator-1.png)

![Sąskaitų šablono susiejimas duomenų integratoriuje](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="f5f54-161">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="f5f54-161">Related topics</span></span>

[<span data-ttu-id="f5f54-162">Sinchronizuoti „Finance and Operations“ produktus su „Sales“ produktais</span><span class="sxs-lookup"><span data-stu-id="f5f54-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="f5f54-163">Sinchronizuoti Pardavimo kontaktus su „Finance and Operations“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="f5f54-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="f5f54-164">Sinchronizuoti „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="f5f54-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="f5f54-165">Sinchronizuoti „Finance and Operations“ pardavimo užsakymo antraštes ir eilutes su „Sales“</span><span class="sxs-lookup"><span data-stu-id="f5f54-165">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="f5f54-166">Sinchronizuoti „Finance and Operations“ pardavimo SF antraštes ir eilutes su „Sales“</span><span class="sxs-lookup"><span data-stu-id="f5f54-166">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)




