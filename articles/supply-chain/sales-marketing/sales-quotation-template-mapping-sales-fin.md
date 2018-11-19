---
title: "„Sales“ pardavimo pasiūlymų antraščių ir eilučių tiesioginis sinchronizavimas su „Finance and Operations“"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ pardavimo pasiūlymo antraštes ir eilutes tiesiogiai sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
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
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: efe943f5c874ed041ce7984272ebc19f57cca6ef
ms.contentlocale: lt-lt
ms.lasthandoff: 11/01/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="56335-103">„Sales“ pardavimo pasiūlymų antraščių ir eilučių tiesioginis sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="56335-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56335-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ pardavimo pasiūlymo antraštes ir eilutes tiesiogiai sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="56335-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="56335-105">Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [Duomenų integravimas į „Common Data Service“, skirtą programoms](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="56335-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="56335-106">Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="56335-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="56335-107">Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Finance and Operations“ ir „Sales“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="56335-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="56335-108">Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ sąskaitų, kontaktų, produktų, pardavimo pasiūlymų, pardavimo užsakymų ir pardavimo sąskaitų faktūrų duomenų srautus.</span><span class="sxs-lookup"><span data-stu-id="56335-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="56335-109">Toliau pateiktoje iliustracijoje rodoma, kaip duomenys sinchronizuojami tarp „Finance and Operations“ ir „Sales“.</span><span class="sxs-lookup"><span data-stu-id="56335-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="56335-110">[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="56335-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="56335-111">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="56335-111">Template and tasks</span></span>

<span data-ttu-id="56335-112">Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami tiesiogiai sinchronizuojant „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="56335-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="56335-113">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** pardavimo pasiūlymai (iš „Sales“ į „Finance and Operations“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="56335-113">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="56335-114">**Užduočių pavadinimai projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="56335-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="56335-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="56335-115">QuoteHeader</span></span>
    - <span data-ttu-id="56335-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="56335-116">QuoteLine</span></span>

<span data-ttu-id="56335-117">Prieš sinchronizuojant pardavimo pasiūlymų antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="56335-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="56335-118">Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="56335-118">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="56335-119">Sąskaitos (iš „Sales“ į „Finance and Operations“) – tiesioginis (jei naudojama)</span><span class="sxs-lookup"><span data-stu-id="56335-119">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="56335-120">Iš kontaktų į klientus (iš „Sales“ į „Finance and Operations“) – tiesioginis (jei naudojama)</span><span class="sxs-lookup"><span data-stu-id="56335-120">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="56335-121">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="56335-121">Entity set</span></span>

| <span data-ttu-id="56335-122">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="56335-122">Sales</span></span>        | <span data-ttu-id="56335-123">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="56335-123">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="56335-124">Pasiūlymai</span><span class="sxs-lookup"><span data-stu-id="56335-124">Quotes</span></span>       | <span data-ttu-id="56335-125">CDS pardavimo pasiūlymo antraštė</span><span class="sxs-lookup"><span data-stu-id="56335-125">CDS sales quotation header</span></span> |
| <span data-ttu-id="56335-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="56335-126">QuoteDetails</span></span> | <span data-ttu-id="56335-127">CDS pardavimo pasiūlymo eilutės</span><span class="sxs-lookup"><span data-stu-id="56335-127">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="56335-128">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="56335-128">Entity flow</span></span>

<span data-ttu-id="56335-129">Pardavimo pasiūlymai kuriami „Sales“ ir sinchronizuojami su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="56335-129">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="56335-130">„Sales“ pardavimo pasiūlymai sinchronizuojami tik jei tenkinamos tolesnės sąlygos.</span><span class="sxs-lookup"><span data-stu-id="56335-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="56335-131">Visi produktų pasiūlymai pardavimo pasiūlyme yra tvarkomi išoriškai.</span><span class="sxs-lookup"><span data-stu-id="56335-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="56335-132">Spustelėjus **Aktyvinti pasiūlymą**, pardavimo pasiūlymas tampa aktyvus.</span><span class="sxs-lookup"><span data-stu-id="56335-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="56335-133">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="56335-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="56335-134">Laukas **Sudaro tik išoriškai tvarkomi produktai** įtrauktas į objektą **Pasiūlymas** , kad būtų galima nuosekliai sekti, ar pardavimo pasiūlymą sudaro tik išoriškai tvarkomi produktai.</span><span class="sxs-lookup"><span data-stu-id="56335-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="56335-135">Jei pardavimo pasiūlymui priskirti tik išoriškai tvarkomi produktai, produktai tvarkomi „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="56335-135">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="56335-136">Tai padeda užtikrinti, kad nebandysite sinchronizuoti pardavimo pasiūlymo eilučių, kuriose nurodyti „Finance and Operations“ neatpažįstami produktai.</span><span class="sxs-lookup"><span data-stu-id="56335-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="56335-137">Visi produktų pasiūlymai pardavimo pasiūlyme atnaujinami, įtraukiant pardavimo pasiūlymo antraštės informaciją **Sudaro tik išoriškai tvarkomi produktai**.</span><span class="sxs-lookup"><span data-stu-id="56335-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="56335-138">Šią informacija pateikiama **QuoteDetails** objekto lauke **Pasiūlymą sudaro tik išoriškai tvarkomi produktai**.</span><span class="sxs-lookup"><span data-stu-id="56335-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="56335-139">Į produkto pasiūlymą gali būti įtraukta nuolaida ir visa tai bus sinchronizuojama su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="56335-139">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="56335-140">Antraštės laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai** valdo „Finance and Operations“ sąranka.</span><span class="sxs-lookup"><span data-stu-id="56335-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="56335-141">Šiuo metu šioje sąrankoje nepalaikomas integravimo susiejimas.</span><span class="sxs-lookup"><span data-stu-id="56335-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="56335-142">Dabartinėje versijoje laukai **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** prižiūrimi bei tvarkomi programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="56335-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="56335-143">„Sales“ versijoje šis sprendimas toliau nurodytus laukus nustato kaip tik skaitomus, nes reikšmės nėra sinchronizuojamos su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="56335-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="56335-144">Tik skaitomi pardavimo pasiūlymo antraštės laukai: **Nuolaida %**, **Nuolaida** ir **Transportavimo suma**</span><span class="sxs-lookup"><span data-stu-id="56335-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="56335-145">Tik skaitomi produktų pasiūlymo laukai: **Mokestis**</span><span class="sxs-lookup"><span data-stu-id="56335-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="56335-146">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="56335-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="56335-147">Prieš sinchronizuojant pardavimo pasiūlymus, svarbu atnaujinti toliau nurodytus parametrus.</span><span class="sxs-lookup"><span data-stu-id="56335-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="56335-148">Sąranka sprendime „Sales“</span><span class="sxs-lookup"><span data-stu-id="56335-148">Setup in Sales</span></span>

- <span data-ttu-id="56335-149">Įsitikinkite, kad komandai, kuriai nustatytas vartotojas iš „Sales“ ryšio rinkinio, nustatytos teisės.</span><span class="sxs-lookup"><span data-stu-id="56335-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="56335-150">Jei naudojate demonstracinius duomenis, prieiga paprastai suteikiama vartotojui, bet ne komandai.</span><span class="sxs-lookup"><span data-stu-id="56335-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="56335-151">Jei komanda neturės administratoriaus prieigos, vykdydami Duomenų integravimo projektą gausite klaidos pranešimą, kad trūksta pagrindinės komandos.</span><span class="sxs-lookup"><span data-stu-id="56335-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="56335-152">Norėdami nustatyti komandos teises, eikite į **Parametrai** &gt; **Sauga** &gt; **Komandas** ir pasirinkite reikiamą komandą.</span><span class="sxs-lookup"><span data-stu-id="56335-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="56335-153">Pasirinkite **Valdyti vaidmenis**, tada pasirinkite vaidmenį, kuriam suteiktos pageidaujamos teisės, pavyzdžiui, **Sistemos administratorius**.</span><span class="sxs-lookup"><span data-stu-id="56335-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="56335-154">Eikite į **Parametrai** &gt; **Administravimas** &gt; **Sistemos parametrai** &gt; **Pardavimai** ir įsitikinkite, kad naudojami toliau nurodyti parametrai.</span><span class="sxs-lookup"><span data-stu-id="56335-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="56335-155">Parinktis **Naudoti sistemos prizų skaičiavimo sistemą** nustatyta į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="56335-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="56335-156">Laukas **Nuolaidos skaičiavimo būdas** nustatytas į **Eilutės elementas**.</span><span class="sxs-lookup"><span data-stu-id="56335-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="56335-157">Sąranka projekte Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="56335-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="56335-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="56335-158">QuoteHeader</span></span>

- <span data-ttu-id="56335-159">Įsitikinkite, kad yra reikiamas **Shipto\_country** susiejimas su **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="56335-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="56335-160">Vertės schemoje galite nurodyti numatytąją reikšmę, naudojamą tada, jei reikšmės laukas yra tuščias.</span><span class="sxs-lookup"><span data-stu-id="56335-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="56335-161">Tiesiog kairiąją pusę palikite tuščią, o dešiniąją nustatykite į pageidaujamą šalį arba regioną.</span><span class="sxs-lookup"><span data-stu-id="56335-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="56335-162">Tokiu būdu, atliekant užsakymus šalies viduje jums nereikės įvesti šalies arba regiono.</span><span class="sxs-lookup"><span data-stu-id="56335-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="56335-163">Šablono vertė yra vertės schema, kurioje susieta keletas šalių ar regionų ir kurioje tuščios vertės laukas lygus vertei **JAV**.</span><span class="sxs-lookup"><span data-stu-id="56335-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="56335-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="56335-164">QuoteLine</span></span>

- <span data-ttu-id="56335-165">Įsitikinkite, kad „Finance and Operations“ yra **SalesUnitSymbol** būtina verčių schema.</span><span class="sxs-lookup"><span data-stu-id="56335-165">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="56335-166">Įsitikinkite, kad „Sales“ apibrėžti reikiami vienetai.</span><span class="sxs-lookup"><span data-stu-id="56335-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="56335-167">Šablono vertė, kurioje yra vertės schema, apibrėžta **oumid.name** į **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="56335-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="56335-168">Pasirinktina: galite įtraukti toliau nurodytus susiejimus, norėdami užtikrinti, kad pardavimo pasiūlymo eilutės importuojamos „Finance and Operations“, jei nenurodyta kliento arba produkto numatytoji informacija.</span><span class="sxs-lookup"><span data-stu-id="56335-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="56335-169">**SiteId** – vieta būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="56335-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="56335-170">Numatytosios **SiteId** šablono reikšmės nėra.</span><span class="sxs-lookup"><span data-stu-id="56335-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="56335-171">**WarehouseId** – sandėlis yra būtinas norint apdoroti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="56335-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="56335-172">Numatytosios **WarehouseId** šablono reikšmės nėra.</span><span class="sxs-lookup"><span data-stu-id="56335-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="56335-173">Šablono susiejimas duomenų integratoriuje</span><span class="sxs-lookup"><span data-stu-id="56335-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="56335-174">Sudėtinga „Finance and Operations“ sąranka valdo laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai**.</span><span class="sxs-lookup"><span data-stu-id="56335-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="56335-175">Šiuo metu šioje sąrankoje nepalaikomas integravimo susiejimas.</span><span class="sxs-lookup"><span data-stu-id="56335-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="56335-176">Dabartinėje versijoje laukus **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** tvarko „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="56335-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="56335-177">Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti.</span><span class="sxs-lookup"><span data-stu-id="56335-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="56335-178">Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.</span><span class="sxs-lookup"><span data-stu-id="56335-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="56335-179">Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.</span><span class="sxs-lookup"><span data-stu-id="56335-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="56335-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="56335-180">QuoteHeader</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="56335-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="56335-182">QuoteLine</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="56335-184">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="56335-184">Related topics</span></span>

[<span data-ttu-id="56335-185">Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="56335-185">Prospect to cash</span></span>](prospect-to-cash.md)


