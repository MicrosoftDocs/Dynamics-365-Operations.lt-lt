---
title: Tiesioginis „Sales“ pardavimo pasiūlymų antraščių ir eilučių sinchronizavimas su „Supply Chain Management”
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Sales“ pardavimo pasiūlymų antraštes ir eilutes tiesiogiai sinchronizuojant su „Dynamics 365 Supply Chain Management“.
author: ChristianRytt
ms.date: 10/25/2018
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
ms.openlocfilehash: bdca4d63fbe04a01cf1bbf2ccd7b095d4718a115
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/16/2021
ms.locfileid: "5910310"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a><span data-ttu-id="6e555-103">Tiesioginis „Sales“ pardavimo pasiūlymų antraščių ir eilučių sinchronizavimas su „Supply Chain Management”</span><span class="sxs-lookup"><span data-stu-id="6e555-103">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6e555-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Sales“ pardavimo pasiūlymų antraštes ir eilutes tiesiogiai sinchronizuojant su „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="6e555-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="6e555-105">Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [Duomenų integravimas į „Microsoft Dataverse“, skirtą programoms](/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="6e555-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="6e555-106">Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="6e555-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="6e555-107">Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Supply Chain Management“ ir „Sales“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="6e555-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="6e555-108">Sprendimo Potencialūs klientai ir grynieji pinigai šablonai, pasiekiami naudojant duomenų integravimo funkciją, įjungia sąskaitų, kontaktų, produktų, pardavimo pasiūlymų, pardavimo užsakymų ir pardavimo SF duomenų srautą tarp „Supply Chain Management” ir „Sales“.</span><span class="sxs-lookup"><span data-stu-id="6e555-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="6e555-109">Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami „Supply Chain Management “ ir „Sales“ duomenys.</span><span class="sxs-lookup"><span data-stu-id="6e555-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="6e555-110">[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="6e555-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="6e555-111">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="6e555-111">Template and tasks</span></span>

<span data-ttu-id="6e555-112">Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami tiesiogiai sinchronizuojant „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="6e555-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="6e555-113">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** Pardavimo pasiūlymai (iš „Sales“ į „Supply Chain Management”) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="6e555-113">**Name of the template in Data integration:** Sales Quotes (Sales to Supply Chain Management) - Direct</span></span>
- <span data-ttu-id="6e555-114">**Užduočių pavadinimai projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="6e555-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="6e555-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="6e555-115">QuoteHeader</span></span>
    - <span data-ttu-id="6e555-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="6e555-116">QuoteLine</span></span>

<span data-ttu-id="6e555-117">Prieš sinchronizuojant pardavimo pasiūlymų antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="6e555-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="6e555-118">Produktai (iš „Supply Chain Management” į „Sales“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="6e555-118">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="6e555-119">Sąskaitos (iš „Sales“ į „Supply Chain Management”) – tiesioginis (jei naudojamas)</span><span class="sxs-lookup"><span data-stu-id="6e555-119">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="6e555-120">Kontaktai klientams (iš „Sales“ į „Supply Chain Management”) – tiesioginis (jei naudojamas)</span><span class="sxs-lookup"><span data-stu-id="6e555-120">Contacts to Customers (Sales to Supply Chain Management) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="6e555-121">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="6e555-121">Entity set</span></span>

| <span data-ttu-id="6e555-122">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="6e555-122">Sales</span></span>        | <span data-ttu-id="6e555-123">„Supply Chain Management”</span><span class="sxs-lookup"><span data-stu-id="6e555-123">Supply Chain Management</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="6e555-124">Pasiūlymai</span><span class="sxs-lookup"><span data-stu-id="6e555-124">Quotes</span></span>       | <span data-ttu-id="6e555-125">„Dataverse” pardavimo kainos pasiūlymo antraštė</span><span class="sxs-lookup"><span data-stu-id="6e555-125">Dataverse sales quotation header</span></span> |
| <span data-ttu-id="6e555-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="6e555-126">QuoteDetails</span></span> | <span data-ttu-id="6e555-127">„Dataverse” pardavimo kainos pasiūlymų eilutės</span><span class="sxs-lookup"><span data-stu-id="6e555-127">Dataverse sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="6e555-128">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="6e555-128">Entity flow</span></span>

<span data-ttu-id="6e555-129">Pardavimo pasiūlymai kuriami sprendime „Sales“ ir sinchronizuojami su „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="6e555-129">Sales quotations are created in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="6e555-130">„Sales“ pardavimo pasiūlymai sinchronizuojami tik jei tenkinamos tolesnės sąlygos.</span><span class="sxs-lookup"><span data-stu-id="6e555-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="6e555-131">Visi produktų pasiūlymai pardavimo pasiūlyme yra tvarkomi išoriškai.</span><span class="sxs-lookup"><span data-stu-id="6e555-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="6e555-132">Spustelėjus **Aktyvinti pasiūlymą**, pardavimo pasiūlymas tampa aktyvus.</span><span class="sxs-lookup"><span data-stu-id="6e555-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="6e555-133">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="6e555-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="6e555-134">Laukas **Sudaro tik išoriškai tvarkomi produktai** įtrauktas į objektą **Pasiūlymas** , kad būtų galima nuosekliai sekti, ar pardavimo pasiūlymą sudaro tik išoriškai tvarkomi produktai.</span><span class="sxs-lookup"><span data-stu-id="6e555-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="6e555-135">Jei pardavimo pasiūlymui priskirti tik išoriškai tvarkomi produktai, produktai tvarkomi „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="6e555-135">If a sales quotation has only externally maintained products, the products are maintained in Supply Chain Management.</span></span> <span data-ttu-id="6e555-136">Tai padeda užtikrinti, kad nebandysite sinchronizuoti pardavimo pasiūlymų eilučių, kuriose nurodyti „Supply Chain Management” neatpažįstami produktai.</span><span class="sxs-lookup"><span data-stu-id="6e555-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Supply Chain Management.</span></span>

<span data-ttu-id="6e555-137">Visi produktų pasiūlymai pardavimo pasiūlyme atnaujinami, įtraukiant pardavimo pasiūlymo antraštės informaciją **Sudaro tik išoriškai tvarkomi produktai**.</span><span class="sxs-lookup"><span data-stu-id="6e555-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="6e555-138">Šią informacija pateikiama **QuoteDetails** objekto lauke **Pasiūlymą sudaro tik išoriškai tvarkomi produktai**.</span><span class="sxs-lookup"><span data-stu-id="6e555-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="6e555-139">Į produkto pasiūlymą gali būti įtraukta nuolaida ir visa tai bus sinchronizuojama su „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="6e555-139">A discount can be added to the quote product and will be synchronized to Supply Chain Management.</span></span> <span data-ttu-id="6e555-140">Antraštės laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai** valdo „Supply Chain Management” sąranka.</span><span class="sxs-lookup"><span data-stu-id="6e555-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="6e555-141">Šiuo metu šioje sąrankoje nepalaikomas integravimo susiejimas.</span><span class="sxs-lookup"><span data-stu-id="6e555-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="6e555-142">Dabartinėje versijoje laukai **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** prižiūrimi bei tvarkomi naudojant „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="6e555-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in FSupply Chain Management.</span></span>

<span data-ttu-id="6e555-143">Sprendime „Sales“ šis sprendimas toliau nurodytus laukus nustato kaip tik skaitomus, nes reikšmės nėra sinchronizuojamos su „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="6e555-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Supply Chain Management:</span></span>

- <span data-ttu-id="6e555-144">Tik skaitomi pardavimo pasiūlymo antraštės laukai: **Nuolaida %**, **Nuolaida** ir **Transportavimo suma**</span><span class="sxs-lookup"><span data-stu-id="6e555-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="6e555-145">Tik skaitomi produktų pasiūlymo laukai: **Mokestis**</span><span class="sxs-lookup"><span data-stu-id="6e555-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="6e555-146">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="6e555-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="6e555-147">Prieš sinchronizuojant pardavimo pasiūlymus, svarbu atnaujinti toliau nurodytus parametrus.</span><span class="sxs-lookup"><span data-stu-id="6e555-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="6e555-148">Sąranka sprendime „Sales“</span><span class="sxs-lookup"><span data-stu-id="6e555-148">Setup in Sales</span></span>

- <span data-ttu-id="6e555-149">Įsitikinkite, kad komandai, kuriai nustatytas vartotojas iš „Sales“ ryšio rinkinio, nustatytos teisės.</span><span class="sxs-lookup"><span data-stu-id="6e555-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="6e555-150">Jei naudojate demonstracinius duomenis, prieiga paprastai suteikiama vartotojui, bet ne komandai.</span><span class="sxs-lookup"><span data-stu-id="6e555-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="6e555-151">Jei komanda neturės administratoriaus prieigos, vykdydami Duomenų integravimo projektą gausite klaidos pranešimą, kad trūksta pagrindinės komandos.</span><span class="sxs-lookup"><span data-stu-id="6e555-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="6e555-152">Norėdami nustatyti komandos teises, eikite į **Parametrai** &gt; **Sauga** &gt; **Komandas** ir pasirinkite reikiamą komandą.</span><span class="sxs-lookup"><span data-stu-id="6e555-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="6e555-153">Pasirinkite **Valdyti vaidmenis**, tada pasirinkite vaidmenį, kuriam suteiktos pageidaujamos teisės, pavyzdžiui, **Sistemos administratorius**.</span><span class="sxs-lookup"><span data-stu-id="6e555-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="6e555-154">Eikite į **Parametrai** &gt; **Administravimas** &gt; **Sistemos parametrai** &gt; **Pardavimai** ir įsitikinkite, kad naudojami toliau nurodyti parametrai.</span><span class="sxs-lookup"><span data-stu-id="6e555-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="6e555-155">Parinktis **Naudoti sistemos prizų skaičiavimo sistemą** nustatyta į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="6e555-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="6e555-156">Laukas **Nuolaidos skaičiavimo būdas** nustatytas į **Eilutės elementas**.</span><span class="sxs-lookup"><span data-stu-id="6e555-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="6e555-157">Sąranka projekte Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="6e555-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="6e555-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="6e555-158">QuoteHeader</span></span>

- <span data-ttu-id="6e555-159">Įsitikinkite, kad yra reikiamas **Shipto\_country** susiejimas su **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="6e555-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="6e555-160">Vertės schemoje galite nurodyti numatytąją reikšmę, naudojamą tada, jei reikšmės laukas yra tuščias.</span><span class="sxs-lookup"><span data-stu-id="6e555-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="6e555-161">Tiesiog kairiąją pusę palikite tuščią, o dešiniąją nustatykite į pageidaujamą šalį arba regioną.</span><span class="sxs-lookup"><span data-stu-id="6e555-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="6e555-162">Tokiu būdu, atliekant užsakymus šalies viduje jums nereikės įvesti šalies arba regiono.</span><span class="sxs-lookup"><span data-stu-id="6e555-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="6e555-163">Šablono vertė yra vertės schema, kurioje susieta keletas šalių ar regionų ir kurioje tuščios vertės laukas lygus vertei **JAV**.</span><span class="sxs-lookup"><span data-stu-id="6e555-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="6e555-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="6e555-164">QuoteLine</span></span>

- <span data-ttu-id="6e555-165">Įsitikinkite, kad reikiamas **SalesUnitSymbol** skirtas susiejimas yra „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="6e555-165">Make sure that the required value map exists for **SalesUnitSymbol** in Supply Chain Management.</span></span>
- <span data-ttu-id="6e555-166">Įsitikinkite, kad „Sales“ apibrėžti reikiami vienetai.</span><span class="sxs-lookup"><span data-stu-id="6e555-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="6e555-167">Šablono vertė, kurioje yra vertės schema, apibrėžta **oumid.name** į **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="6e555-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="6e555-168">Pasirinktina: galite įtraukti toliau nurodytus susiejimus, norėdami užtikrinti, kad pardavimo pasiūlymo eilutės importuojamos į „Supply Chain Management”, jei nenurodyta kliento arba produkto numatytoji informacija.</span><span class="sxs-lookup"><span data-stu-id="6e555-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Supply Chain Management if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="6e555-169">**SiteId** – vieta būtina norint generuoti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="6e555-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="6e555-170">Numatytosios **SiteId** šablono reikšmės nėra.</span><span class="sxs-lookup"><span data-stu-id="6e555-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="6e555-171">**WarehouseId** – sandėlis yra būtinas norint apdoroti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="6e555-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="6e555-172">Numatytosios **WarehouseId** šablono reikšmės nėra.</span><span class="sxs-lookup"><span data-stu-id="6e555-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="6e555-173">Šablono susiejimas duomenų integratoriuje</span><span class="sxs-lookup"><span data-stu-id="6e555-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="6e555-174">Laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai** valdo sudėtinga „Supply Chain Management” sąranka.</span><span class="sxs-lookup"><span data-stu-id="6e555-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Supply Chain Management.</span></span> <span data-ttu-id="6e555-175">Šiuo metu šioje sąrankoje nepalaikomas integravimo susiejimas.</span><span class="sxs-lookup"><span data-stu-id="6e555-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="6e555-176">Dabartinėje versijoje laukus **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** tvarko „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="6e555-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Supply Chain Management.</span></span>
> - <span data-ttu-id="6e555-177">Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti.</span><span class="sxs-lookup"><span data-stu-id="6e555-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="6e555-178">Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.</span><span class="sxs-lookup"><span data-stu-id="6e555-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="6e555-179">Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.</span><span class="sxs-lookup"><span data-stu-id="6e555-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="6e555-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="6e555-180">QuoteHeader</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="6e555-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="6e555-182">QuoteLine</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="6e555-184">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="6e555-184">Related topics</span></span>

[<span data-ttu-id="6e555-185">Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="6e555-185">Prospect to cash</span></span>](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]