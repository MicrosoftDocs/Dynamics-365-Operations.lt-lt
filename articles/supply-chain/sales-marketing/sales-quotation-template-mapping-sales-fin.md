---
title: "„Sales“ pardavimo pasiūlymų antraščių ir eilučių tiesioginis sinchronizavimas su „Finance and Operations“"
description: "Temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ pardavimo pasiūlymų antraštes ir eilutes tiesiogiai sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“ „Enterprise“ leidimu."
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
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
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 8a75c6dd91020ab3e676e2bb40d5c822731e244f
ms.contentlocale: lt-lt
ms.lasthandoff: 11/14/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="69ff5-103">„Sales“ pardavimo pasiūlymų antraščių ir eilučių tiesioginis sinchronizavimas su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="69ff5-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="69ff5-104">Temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ pardavimo pasiūlymų antraštes ir eilutes tiesiogiai sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“ „Enterprise“ leidimu.</span><span class="sxs-lookup"><span data-stu-id="69ff5-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

> [!NOTE]
> <span data-ttu-id="69ff5-105">Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [„Dynamics 365“ duomenų integravimo funkcija](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="69ff5-105">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="69ff5-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="69ff5-106">Template and tasks</span></span>

<span data-ttu-id="69ff5-107">Toliau pateiktas šablonas ir pagrindinės užduotys yra naudojami tiesiogiai sinchronizuojant „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="69ff5-107">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="69ff5-108">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:** pardavimo pasiūlymai (iš „Sales“ į „Finance and Operations“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="69ff5-108">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="69ff5-109">**Užduočių pavadinimai projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="69ff5-109">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="69ff5-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="69ff5-110">QuoteHeader</span></span>
    - <span data-ttu-id="69ff5-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="69ff5-111">QuoteLine</span></span>

<span data-ttu-id="69ff5-112">Prieš sinchronizuojant pardavimo pasiūlymų antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="69ff5-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="69ff5-113">Produktai (iš „Finance and Operations“ į „Sales“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="69ff5-113">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="69ff5-114">Sąskaitos (iš „Sales“ į „Finance and Operations“) – tiesioginis (jei naudojama)</span><span class="sxs-lookup"><span data-stu-id="69ff5-114">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="69ff5-115">Iš kontaktų į klientus (iš „Sales“ į „Finance and Operations“) – tiesioginis (jei naudojama)</span><span class="sxs-lookup"><span data-stu-id="69ff5-115">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="69ff5-116">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="69ff5-116">Entity set</span></span>

| <span data-ttu-id="69ff5-117">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="69ff5-117">Sales</span></span>        | <span data-ttu-id="69ff5-118">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="69ff5-118">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="69ff5-119">Pasiūlymai</span><span class="sxs-lookup"><span data-stu-id="69ff5-119">Quotes</span></span>       | <span data-ttu-id="69ff5-120">CDS pardavimo pasiūlymo antraštė</span><span class="sxs-lookup"><span data-stu-id="69ff5-120">CDS sales quotation header</span></span> |
| <span data-ttu-id="69ff5-121">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="69ff5-121">QuoteDetails</span></span> | <span data-ttu-id="69ff5-122">CDS pardavimo pasiūlymo eilutės</span><span class="sxs-lookup"><span data-stu-id="69ff5-122">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="69ff5-123">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="69ff5-123">Entity flow</span></span>

<span data-ttu-id="69ff5-124">Pardavimo pasiūlymai kuriami „Sales“ ir sinchronizuojami su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="69ff5-124">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="69ff5-125">„Sales“ pardavimo pasiūlymai sinchronizuojami tik jei tenkinamos tolesnės sąlygos.</span><span class="sxs-lookup"><span data-stu-id="69ff5-125">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="69ff5-126">Visi produktų pasiūlymai pardavimo pasiūlyme yra tvarkomi išoriškai.</span><span class="sxs-lookup"><span data-stu-id="69ff5-126">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="69ff5-127">Spustelėjus **Aktyvinti pasiūlymą**, pardavimo pasiūlymas tampa aktyvus.</span><span class="sxs-lookup"><span data-stu-id="69ff5-127">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="69ff5-128">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="69ff5-128">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="69ff5-129">Laukas **Sudaro tik išoriškai tvarkomi produktai** įtrauktas į objektą **Pasiūlymas** , kad būtų galima nuosekliai sekti, ar pardavimo pasiūlymą sudaro tik išoriškai tvarkomi produktai.</span><span class="sxs-lookup"><span data-stu-id="69ff5-129">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="69ff5-130">Jei pardavimo pasiūlymui priskirti tik išoriškai tvarkomi produktai, produktai tvarkomi „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="69ff5-130">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="69ff5-131">Tai padeda užtikrinti, kad nebandysite sinchronizuoti pardavimo pasiūlymo eilučių, kuriose nurodyti „Finance and Operations“ neatpažįstami produktai.</span><span class="sxs-lookup"><span data-stu-id="69ff5-131">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="69ff5-132">Visi produktų pasiūlymai pardavimo pasiūlyme atnaujinami, įtraukiant pardavimo pasiūlymo antraštės informaciją **Sudaro tik išoriškai tvarkomi produktai**.</span><span class="sxs-lookup"><span data-stu-id="69ff5-132">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="69ff5-133">Šią informacija pateikiama **QuoteDetails** objekto lauke **Pasiūlymą sudaro tik išoriškai tvarkomi produktai**.</span><span class="sxs-lookup"><span data-stu-id="69ff5-133">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="69ff5-134">Į produkto pasiūlymą gali būti įtraukta nuolaida ir visa tai bus sinchronizuojama su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="69ff5-134">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="69ff5-135">Antraštės laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai** valdo „Finance and Operations“ sąranka.</span><span class="sxs-lookup"><span data-stu-id="69ff5-135">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="69ff5-136">Šiuo metu šioje sąrankoje nepalaikomas integravimo susiejimas.</span><span class="sxs-lookup"><span data-stu-id="69ff5-136">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="69ff5-137">Dabartinėje versijoje laukai **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** prižiūrimi bei tvarkomi programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="69ff5-137">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="69ff5-138">„Sales“ versijoje šis sprendimas toliau nurodytus laukus nustato kaip tik skaitomus, nes reikšmės nėra sinchronizuojamos su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="69ff5-138">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="69ff5-139">Tik skaitomi pardavimo pasiūlymo antraštės laukai: **Nuolaida %**, **Nuolaida** ir **Transportavimo suma**</span><span class="sxs-lookup"><span data-stu-id="69ff5-139">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="69ff5-140">Tik skaitomi produktų pasiūlymo laukai: **Mokestis**</span><span class="sxs-lookup"><span data-stu-id="69ff5-140">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="69ff5-141">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="69ff5-141">Preconditions and mapping setup</span></span>

<span data-ttu-id="69ff5-142">Prieš sinchronizuojant pardavimo pasiūlymus, svarbu atnaujinti toliau nurodytus parametrus.</span><span class="sxs-lookup"><span data-stu-id="69ff5-142">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="69ff5-143">Sąranka sprendime „Sales“</span><span class="sxs-lookup"><span data-stu-id="69ff5-143">Setup in Sales</span></span>

- <span data-ttu-id="69ff5-144">Įsitikinkite, kad komandai, kuriai nustatytas vartotojas iš „Sales“ ryšio rinkinio, nustatytos teisės.</span><span class="sxs-lookup"><span data-stu-id="69ff5-144">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="69ff5-145">Jei naudojate demonstracinius duomenis, prieiga paprastai suteikiama vartotojui, bet ne komandai.</span><span class="sxs-lookup"><span data-stu-id="69ff5-145">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="69ff5-146">Jei komanda neturės administratoriaus prieigos, vykdydami Duomenų integravimo projektą gausite klaidos pranešimą, kad trūksta pagrindinės komandos.</span><span class="sxs-lookup"><span data-stu-id="69ff5-146">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="69ff5-147">Norėdami nustatyti komandos teises, eikite į **Parametrai** &gt; **Sauga** &gt; **Komandas** ir pasirinkite reikiamą komandą.</span><span class="sxs-lookup"><span data-stu-id="69ff5-147">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="69ff5-148">Pasirinkite **Valdyti vaidmenis**, tada pasirinkite vaidmenį, kuriam suteiktos pageidaujamos teisės, pavyzdžiui, **Sistemos administratorius**.</span><span class="sxs-lookup"><span data-stu-id="69ff5-148">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="69ff5-149">Eikite į **Parametrai** &gt; **Administravimas** &gt; **Sistemos parametrai** &gt; **Pardavimai** ir įsitikinkite, kad naudojami toliau nurodyti parametrai.</span><span class="sxs-lookup"><span data-stu-id="69ff5-149">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="69ff5-150">Parinktis **Naudoti sistemos prizų skaičiavimo sistemą** nustatyta į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="69ff5-150">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="69ff5-151">Laukas **Nuolaidos skaičiavimo būdas** nustatytas į **Eilutės elementas**.</span><span class="sxs-lookup"><span data-stu-id="69ff5-151">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="69ff5-152">Sąranka projekte Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="69ff5-152">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="69ff5-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="69ff5-153">QuoteHeader</span></span>

- <span data-ttu-id="69ff5-154">Įsitikinkite, kad yra reikiamas **Shipto\_country** susiejimas su **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="69ff5-154">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="69ff5-155">Vertės schemoje galite nurodyti numatytąją reikšmę, naudojamą tada, jei reikšmės laukas yra tuščias.</span><span class="sxs-lookup"><span data-stu-id="69ff5-155">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="69ff5-156">Tiesiog kairiąją pusę palikite tuščią, o dešiniąją nustatykite į pageidaujamą šalį arba regioną.</span><span class="sxs-lookup"><span data-stu-id="69ff5-156">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="69ff5-157">Tokiu būdu, atliekant užsakymus šalies viduje jums nereikės įvesti šalies arba regiono.</span><span class="sxs-lookup"><span data-stu-id="69ff5-157">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="69ff5-158">Šablono vertė yra vertės schema, kurioje susieta keletas šalių ar regionų ir kurioje tuščios vertės laukas lygus vertei **JAV**.</span><span class="sxs-lookup"><span data-stu-id="69ff5-158">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="69ff5-159">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="69ff5-159">QuoteLine</span></span>

- <span data-ttu-id="69ff5-160">Įsitikinkite, kad „Finance and Operations“ yra **SalesUnitSymbol** būtina verčių schema.</span><span class="sxs-lookup"><span data-stu-id="69ff5-160">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="69ff5-161">Įsitikinkite, kad „Sales“ apibrėžti reikiami vienetai.</span><span class="sxs-lookup"><span data-stu-id="69ff5-161">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="69ff5-162">Šablono vertė, kurioje yra vertės schema, apibrėžta **oumid.name** į **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="69ff5-162">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="69ff5-163">Pasirinktina: galite įtraukti toliau nurodytus susiejimus, norėdami užtikrinti, kad pardavimo pasiūlymo eilutės importuojamos „Finance and Operations“, jei nenurodyta kliento arba produkto numatytoji informacija.</span><span class="sxs-lookup"><span data-stu-id="69ff5-163">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="69ff5-164">**SiteId** – vieta būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="69ff5-164">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="69ff5-165">Numatytosios **SiteId** šablono reikšmės nėra.</span><span class="sxs-lookup"><span data-stu-id="69ff5-165">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="69ff5-166">**WarehouseId** – sandėlis yra būtinas norint apdoroti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="69ff5-166">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="69ff5-167">Numatytosios **WarehouseId** šablono reikšmės nėra.</span><span class="sxs-lookup"><span data-stu-id="69ff5-167">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="69ff5-168">Šablono susiejimas duomenų integratoriuje</span><span class="sxs-lookup"><span data-stu-id="69ff5-168">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="69ff5-169">Sudėtinga „Finance and Operations“ sąranka valdo laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai**.</span><span class="sxs-lookup"><span data-stu-id="69ff5-169">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="69ff5-170">Šiuo metu šioje sąrankoje nepalaikomas integravimo susiejimas.</span><span class="sxs-lookup"><span data-stu-id="69ff5-170">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="69ff5-171">Dabartinėje versijoje laukus **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** tvarko „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="69ff5-171">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="69ff5-172">Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti.</span><span class="sxs-lookup"><span data-stu-id="69ff5-172">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="69ff5-173">Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.</span><span class="sxs-lookup"><span data-stu-id="69ff5-173">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="69ff5-174">Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.</span><span class="sxs-lookup"><span data-stu-id="69ff5-174">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="69ff5-175">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="69ff5-175">QuoteHeader</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="69ff5-177">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="69ff5-177">QuoteLine</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="69ff5-179">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="69ff5-179">Related topics</span></span>

[<span data-ttu-id="69ff5-180">Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="69ff5-180">Prospect to cash</span></span>](prospect-to-cash.md)


