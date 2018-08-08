---
title: "Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Finance and Operations“ klientais"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ sąskaitas sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 0e917634572efcb7fcfa277d5b3fb479bffd1366
ms.contentlocale: lt-lt
ms.lasthandoff: 08/07/2018

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="2eb83-103">Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Finance and Operations“ klientais</span><span class="sxs-lookup"><span data-stu-id="2eb83-103">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="2eb83-104">Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [„Dynamics 365“ duomenų integravimo funkcija](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="2eb83-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="2eb83-105">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ sąskaitas sinchronizuojant tiesiogiai su „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="2eb83-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="2eb83-106">Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="2eb83-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="2eb83-107">Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Finance and Operations“ ir „Sales“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="2eb83-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span>  <span data-ttu-id="2eb83-108">Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus.</span><span class="sxs-lookup"><span data-stu-id="2eb83-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="2eb83-109">Toliau pateiktoje iliustracijoje rodoma, kaip duomenys sinchronizuojami tarp „Finance and Operations“ ir „Sales“.</span><span class="sxs-lookup"><span data-stu-id="2eb83-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="2eb83-110">[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="2eb83-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="2eb83-111">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="2eb83-111">Templates and tasks</span></span>

<span data-ttu-id="2eb83-112">Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„PowerApps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="2eb83-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="2eb83-113">Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="2eb83-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="2eb83-114">Toliau pateiktas šablonas ir pagrindinė užduotis yra naudojami sinchronizuojant „Sales“ sąskaitas su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="2eb83-114">The following template and underlying task are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="2eb83-115">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** Sąskaitos (iš „Sales“ į „Finance and Operations“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="2eb83-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="2eb83-116">**Užduoties pavadinimas projekte:** Sąskaitos – Klientai</span><span class="sxs-lookup"><span data-stu-id="2eb83-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="2eb83-117">Prieš sinchronizuojant sąskaitą / klientą, nereikia atlikti jokių sinchronizavimo užduočių.</span><span class="sxs-lookup"><span data-stu-id="2eb83-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="2eb83-118">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="2eb83-118">Entity set</span></span>

| <span data-ttu-id="2eb83-119">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="2eb83-119">Sales</span></span>    | <span data-ttu-id="2eb83-120">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="2eb83-120">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="2eb83-121">Sąskaitos</span><span class="sxs-lookup"><span data-stu-id="2eb83-121">Accounts</span></span> | <span data-ttu-id="2eb83-122">Klientai V2</span><span class="sxs-lookup"><span data-stu-id="2eb83-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="2eb83-123">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="2eb83-123">Entity flow</span></span>

<span data-ttu-id="2eb83-124">Sąskaitos valdomos programoje „Sales“ ir su „Finance and Operations“ sinchronizuojamos kaip klientai.</span><span class="sxs-lookup"><span data-stu-id="2eb83-124">Accounts are managed in Sales and synchronized to Finance and Operations as customers.</span></span> <span data-ttu-id="2eb83-125">Ypatybė **Tvarkoma išoriškai** šiems klientams nustatyta į **Taip**, kad būtų galima sekti „Sales“ klientus.</span><span class="sxs-lookup"><span data-stu-id="2eb83-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="2eb83-126">Išrašant sąskaitą faktūrą ši informacija naudojama sąskaitoms faktūros, sinchronizuojamoms su „Sales“, filtruoti.</span><span class="sxs-lookup"><span data-stu-id="2eb83-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="2eb83-127">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="2eb83-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="2eb83-128">Laukas **Sąskaitos numeris** galimas puslapyje **Sąskaita**.</span><span class="sxs-lookup"><span data-stu-id="2eb83-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="2eb83-129">Integracijai palaikyti buvo sukurtas srities ir unikalus raktas.</span><span class="sxs-lookup"><span data-stu-id="2eb83-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="2eb83-130">Ryšių su klientais valdymo (CRM) sprendimo srities rakto funkcija gali turėti įtakos klientams, jau naudojantiems lauką **Sąskaitos numeris**, bet nenaudojantiems unikalių **Sąskaitos numerio** verčių kiekvienoje sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="2eb83-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="2eb83-131">Šiuo metu integravimo sprendimas nepalaiko šio atvejo.</span><span class="sxs-lookup"><span data-stu-id="2eb83-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="2eb83-132">Sukūrus naują sąskaitą, bet nesant vertei **Sąskaitos numeris**, ji automatiškai sugeneruojama naudojant numeraciją.</span><span class="sxs-lookup"><span data-stu-id="2eb83-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="2eb83-133">Vertę sudaro raidės **ACC**, tada didėjanti numeracija ir iš šešių simbolių sudarytas priedėlis.</span><span class="sxs-lookup"><span data-stu-id="2eb83-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="2eb83-134">Pavyzdys: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="2eb83-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="2eb83-135">Pritaikius integravimo sprendimą „Sales“ naujinimo scenarijus nustato lauką **Sąskaitos numeris** „Sales“ esamoms sąskaitoms.</span><span class="sxs-lookup"><span data-stu-id="2eb83-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="2eb83-136">Jei lauko **Sąskaitos numeris** verčių nėra, naudojama anksčiau minėta numeracija.</span><span class="sxs-lookup"><span data-stu-id="2eb83-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="2eb83-137">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="2eb83-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="2eb83-138">**CustomerGroupId** susiejimą reikia atnaujinti į tinkamą „Finance and Operations“ vertę.</span><span class="sxs-lookup"><span data-stu-id="2eb83-138">The **CustomerGroupId** mapping must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="2eb83-139">Galite nurodyti numatytąją vertę arba ją nustatyti naudodami verčių schemą.</span><span class="sxs-lookup"><span data-stu-id="2eb83-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="2eb83-140">Numatytoji šablono vertė yra **10**.</span><span class="sxs-lookup"><span data-stu-id="2eb83-140">The default template value is **10**.</span></span>

- <span data-ttu-id="2eb83-141">Pridėdami toliau nurodytus susiejimus, galite padėti sumažinti neautomatinių atnaujinimų, kurie būtini „Finance and Operations“, skaičių.</span><span class="sxs-lookup"><span data-stu-id="2eb83-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="2eb83-142">Galite naudoti numatytąją vertę arba verčių schemos vertę, pvz., **Šalis / regionas** arba **miestas**.</span><span class="sxs-lookup"><span data-stu-id="2eb83-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="2eb83-143">**SiteId** – vieta būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="2eb83-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="2eb83-144">Numatytąją vietą galima paimti iš produkto arba iš kliento užsakymo antraštės.</span><span class="sxs-lookup"><span data-stu-id="2eb83-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="2eb83-145">Numatytoji šablono vertė yra **1**.</span><span class="sxs-lookup"><span data-stu-id="2eb83-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="2eb83-146">**WarehouseId** – sandėlis yra būtinas norint apdoroti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="2eb83-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="2eb83-147">Numatytąjį sandėlį galima paimti iš produkto arba iš „Finance and Operations“ kliento užsakymo antraštės.</span><span class="sxs-lookup"><span data-stu-id="2eb83-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span>

        <span data-ttu-id="2eb83-148">Numatytoji šablono vertė yra **13**.</span><span class="sxs-lookup"><span data-stu-id="2eb83-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="2eb83-149">**LanguageId** – kalba yra būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="2eb83-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="2eb83-150">Pagal numatytuosius nustatymus naudojama kalba iš kliento užsakymo antraštės.</span><span class="sxs-lookup"><span data-stu-id="2eb83-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="2eb83-151">Numatytoji šablono vertė yra **en-us**.</span><span class="sxs-lookup"><span data-stu-id="2eb83-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="2eb83-152">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="2eb83-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="2eb83-153">Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti.</span><span class="sxs-lookup"><span data-stu-id="2eb83-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="2eb83-154">Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.</span><span class="sxs-lookup"><span data-stu-id="2eb83-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="2eb83-155">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="2eb83-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="2eb83-156">Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="2eb83-156">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="2eb83-158">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="2eb83-158">Related topics</span></span>


[<span data-ttu-id="2eb83-159">Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="2eb83-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="2eb83-160">Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Finance and Operations“ klientais</span><span class="sxs-lookup"><span data-stu-id="2eb83-160">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="2eb83-161">Tiesioginis „Sales“ kontaktų sinchronizavimas su „Finance and Operations“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="2eb83-161">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="2eb83-162">Tiesioginis „Finance and Operations“ pardavimo užsakymų antraščių ir eilučių sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="2eb83-162">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="2eb83-163">Tiesioginis „Finance and Operations“ pardavimo sąskaitų faktūrų antraščių ir eilučių sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="2eb83-163">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)


