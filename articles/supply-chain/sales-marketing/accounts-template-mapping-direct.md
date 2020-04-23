---
title: Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Supply Chain Management“ klientais
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Sales“ sąskaitas sinchronizuojant su „Supply Chain Management“.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
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
ms.openlocfilehash: 1146fce7cf620a002231a5bc9246c706b97d478d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210139"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="37f1e-103">Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Supply Chain Management“ klientais</span><span class="sxs-lookup"><span data-stu-id="37f1e-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="37f1e-104">Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [Duomenų integravimas į „Common Data Service“, skirtą programoms](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="37f1e-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="37f1e-105">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Sales“ sąskaitas tiesiogiai sinchronizuojant su „Dynamics 365 Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="37f1e-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="37f1e-106">Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="37f1e-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="37f1e-107">Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Supply Chain Management“ ir „Sales“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="37f1e-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="37f1e-108">Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Supply Chain Management“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus.</span><span class="sxs-lookup"><span data-stu-id="37f1e-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="37f1e-109">Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami „Supply Chain Management “ ir „Sales“ duomenys.</span><span class="sxs-lookup"><span data-stu-id="37f1e-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="37f1e-110">[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="37f1e-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="37f1e-111">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="37f1e-111">Templates and tasks</span></span>

<span data-ttu-id="37f1e-112">Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„Power Apps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="37f1e-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="37f1e-113">Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="37f1e-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="37f1e-114">Toliau pateiktas šablonas ir pagrindinė užduotis yra naudojami sinchronizuojant „Sales“ sąskaitas su „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="37f1e-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="37f1e-115">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** Sąskaitos (iš „Sales“ į „Finance and Operations“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="37f1e-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="37f1e-116">**Užduoties pavadinimas projekte:** Sąskaitos – Klientai</span><span class="sxs-lookup"><span data-stu-id="37f1e-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="37f1e-117">Prieš sinchronizuojant sąskaitą / klientą, nereikia atlikti jokių sinchronizavimo užduočių.</span><span class="sxs-lookup"><span data-stu-id="37f1e-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="37f1e-118">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="37f1e-118">Entity set</span></span>

| <span data-ttu-id="37f1e-119">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="37f1e-119">Sales</span></span>    | <span data-ttu-id="37f1e-120">„Supply Chain Management”</span><span class="sxs-lookup"><span data-stu-id="37f1e-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="37f1e-121">Sąskaitos</span><span class="sxs-lookup"><span data-stu-id="37f1e-121">Accounts</span></span> | <span data-ttu-id="37f1e-122">Klientai V2</span><span class="sxs-lookup"><span data-stu-id="37f1e-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="37f1e-123">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="37f1e-123">Entity flow</span></span>

<span data-ttu-id="37f1e-124">Sąskaitos valdomos programoje „Sales“ ir su „Supply Chain Management“ sinchronizuojamos kaip klientai.</span><span class="sxs-lookup"><span data-stu-id="37f1e-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="37f1e-125">Ypatybė **Tvarkoma išoriškai** šiems klientams nustatyta į **Taip**, kad būtų galima sekti „Sales“ klientus.</span><span class="sxs-lookup"><span data-stu-id="37f1e-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="37f1e-126">Išrašant sąskaitą faktūrą ši informacija naudojama sąskaitoms faktūros, sinchronizuojamoms su „Sales“, filtruoti.</span><span class="sxs-lookup"><span data-stu-id="37f1e-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="37f1e-127">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="37f1e-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="37f1e-128">Laukas **Sąskaitos numeris** galimas puslapyje **Sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="37f1e-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="37f1e-129">Integracijai palaikyti buvo sukurtas srities ir unikalus raktas.</span><span class="sxs-lookup"><span data-stu-id="37f1e-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="37f1e-130">Ryšių su klientais valdymo (CRM) sprendimo srities rakto funkcija gali turėti įtakos klientams, jau naudojantiems lauką **Sąskaitos numeris**, bet nenaudojantiems unikalių **Sąskaitos numerio** verčių kiekvienoje sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="37f1e-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="37f1e-131">Šiuo metu integravimo sprendimas nepalaiko šio atvejo.</span><span class="sxs-lookup"><span data-stu-id="37f1e-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="37f1e-132">Sukūrus naują sąskaitą, bet nesant vertei **Sąskaitos numeris**, ji automatiškai sugeneruojama naudojant numeraciją.</span><span class="sxs-lookup"><span data-stu-id="37f1e-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="37f1e-133">Vertę sudaro raidės **ACC**, tada didėjanti numeracija ir iš šešių simbolių sudarytas priedėlis.</span><span class="sxs-lookup"><span data-stu-id="37f1e-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="37f1e-134">Pavyzdys: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="37f1e-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="37f1e-135">Pritaikius integravimo sprendimą „Sales“ naujinimo scenarijus nustato lauką **Sąskaitos numeris** „Sales“ esamoms sąskaitoms.</span><span class="sxs-lookup"><span data-stu-id="37f1e-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="37f1e-136">Jei lauko **Sąskaitos numeris** verčių nėra, naudojama anksčiau minėta numeracija.</span><span class="sxs-lookup"><span data-stu-id="37f1e-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="37f1e-137">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="37f1e-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="37f1e-138">**CustomerGroupId** susiejimą reikia atnaujinti į tinkamą „Supply Chain Management“ vertę.</span><span class="sxs-lookup"><span data-stu-id="37f1e-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="37f1e-139">Galite nurodyti numatytąją vertę arba ją nustatyti naudodami verčių schemą.</span><span class="sxs-lookup"><span data-stu-id="37f1e-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="37f1e-140">Numatytoji šablono vertė yra **10**.</span><span class="sxs-lookup"><span data-stu-id="37f1e-140">The default template value is **10**.</span></span>

- <span data-ttu-id="37f1e-141">Pridėdami toliau nurodytus susiejimus, galite padėti sumažinti neautomatinių atnaujinimų, kurie būtini „Supply Chain Management“, skaičių.</span><span class="sxs-lookup"><span data-stu-id="37f1e-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="37f1e-142">Galite naudoti numatytąją vertę arba verčių schemos vertę, pvz., **Šalis / regionas** arba **miestas**.</span><span class="sxs-lookup"><span data-stu-id="37f1e-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="37f1e-143">**SiteId** – vieta būtina norint generuoti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="37f1e-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="37f1e-144">Numatytąją vietą galima paimti iš produkto arba iš kliento užsakymo antraštės.</span><span class="sxs-lookup"><span data-stu-id="37f1e-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="37f1e-145">Numatytoji šablono vertė yra **1**.</span><span class="sxs-lookup"><span data-stu-id="37f1e-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="37f1e-146">**WarehouseId** – sandėlis yra būtinas norint apdoroti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="37f1e-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="37f1e-147">Numatytąjį sandėlį galima paimti iš produkto arba iš „Supply Chain Management“ kliento užsakymo antraštės.</span><span class="sxs-lookup"><span data-stu-id="37f1e-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="37f1e-148">Numatytoji šablono vertė yra **13**.</span><span class="sxs-lookup"><span data-stu-id="37f1e-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="37f1e-149">**LanguageId** – kalba būtina norint generuoti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="37f1e-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="37f1e-150">Pagal numatytuosius nustatymus naudojama kalba iš kliento užsakymo antraštės.</span><span class="sxs-lookup"><span data-stu-id="37f1e-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="37f1e-151">Numatytoji šablono vertė yra **en-us**.</span><span class="sxs-lookup"><span data-stu-id="37f1e-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="37f1e-152">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="37f1e-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="37f1e-153">Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti.</span><span class="sxs-lookup"><span data-stu-id="37f1e-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="37f1e-154">Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.</span><span class="sxs-lookup"><span data-stu-id="37f1e-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="37f1e-155">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="37f1e-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="37f1e-156">Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="37f1e-156">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="37f1e-158">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="37f1e-158">Related topics</span></span>


[<span data-ttu-id="37f1e-159">Potencialaus kliento pavertimas pinigais</span><span class="sxs-lookup"><span data-stu-id="37f1e-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="37f1e-160">Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Supply Chain Management“ klientais</span><span class="sxs-lookup"><span data-stu-id="37f1e-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="37f1e-161">Tiesioginis „Sales“ kontaktų sinchronizavimas su „Supply Chain Management“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="37f1e-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="37f1e-162">Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir Tiekimo grandinės valdymo</span><span class="sxs-lookup"><span data-stu-id="37f1e-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="37f1e-163">Tiesioginis „Supply Chain Management“ pardavimo SF antraščių ir eilučių sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="37f1e-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

