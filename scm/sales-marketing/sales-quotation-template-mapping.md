---
title: "Sinchronizuoti „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“"
description: "Temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ pardavimo pasiūlymų antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimu."
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
ms.openlocfilehash: 172a3da1b6d90a25ea9ebd14265e70e4a6f9bd70
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="9cfff-103">Sinchronizuoti „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="9cfff-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="9cfff-104">Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai susipažinkite su [„Dynamics 365“ duomenų integravimo funkcija](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="9cfff-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="9cfff-105">Temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ („Sales“) pardavimo pasiūlymų antraštes ir eilutes sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimu („Finance and Operations“).</span><span class="sxs-lookup"><span data-stu-id="9cfff-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="9cfff-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="9cfff-106">Template and tasks</span></span>

<span data-ttu-id="9cfff-107">Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami sinchronizuojant „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="9cfff-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="9cfff-108">**Šablono pavadinimas:** pardavimo pasiūlymai (iš „Sales“ į „Finance and Operations“)</span><span class="sxs-lookup"><span data-stu-id="9cfff-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="9cfff-109">**Užduočių pavadinimai projekte**</span><span class="sxs-lookup"><span data-stu-id="9cfff-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="9cfff-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="9cfff-110">QuoteHeader</span></span>
    - <span data-ttu-id="9cfff-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="9cfff-111">QuoteLine</span></span>

<span data-ttu-id="9cfff-112">Prieš sinchronizuojant pardavimo pasiūlymų antraštes ir eilutes, būtina atlikti toliau pateiktas sinchronizavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="9cfff-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="9cfff-113">Produktai</span><span class="sxs-lookup"><span data-stu-id="9cfff-113">Products</span></span>
- <span data-ttu-id="9cfff-114">Sąskaitos (jei naudojamos)</span><span class="sxs-lookup"><span data-stu-id="9cfff-114">Accounts (if used)</span></span>
- <span data-ttu-id="9cfff-115">Kontaktai (jei naudojami)</span><span class="sxs-lookup"><span data-stu-id="9cfff-115">Contacts (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="9cfff-116">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="9cfff-116">Entity set</span></span>

| <span data-ttu-id="9cfff-117">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="9cfff-117">Sales</span></span>        | <span data-ttu-id="9cfff-118">CDS</span><span class="sxs-lookup"><span data-stu-id="9cfff-118">CDS</span></span>           | <span data-ttu-id="9cfff-119">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="9cfff-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="9cfff-120">Pasiūlymai</span><span class="sxs-lookup"><span data-stu-id="9cfff-120">Quotes</span></span>       | <span data-ttu-id="9cfff-121">Pasiūlymas</span><span class="sxs-lookup"><span data-stu-id="9cfff-121">Quotation</span></span>     | <span data-ttu-id="9cfff-122">Pardavimo pasiūlymo antraštės</span><span class="sxs-lookup"><span data-stu-id="9cfff-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="9cfff-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="9cfff-123">QuoteDetails</span></span> | <span data-ttu-id="9cfff-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="9cfff-124">QuotationLine</span></span> | <span data-ttu-id="9cfff-125">CDS pardavimo pasiūlymo eilutės</span><span class="sxs-lookup"><span data-stu-id="9cfff-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="9cfff-126">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="9cfff-126">Entity flow</span></span>

<span data-ttu-id="9cfff-127">Pardavimo pasiūlymai kuriami „Sales“ ir sinchronizuojami su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="9cfff-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="9cfff-128">„Sales“ pardavimo pasiūlymai sinchronizuojami tik jei tenkinamos tolesnės sąlygos.</span><span class="sxs-lookup"><span data-stu-id="9cfff-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="9cfff-129">Visi produktai pardavimo pasiūlymo eilutėse yra tvarkomi išoriškai.</span><span class="sxs-lookup"><span data-stu-id="9cfff-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="9cfff-130">Pardavimo pasiūlymas yra aktyvus arba suaktyvintas.</span><span class="sxs-lookup"><span data-stu-id="9cfff-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="9cfff-131">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="9cfff-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="9cfff-132">Laukas **Sudaro tik išoriškai tvarkomi produktai** įtrauktas į objektą Pasiūlymas, kad būtų galima nuosekliai sekti, ar pardavimo pasiūlymą sudaro tik išoriškai tvarkomi produktai.</span><span class="sxs-lookup"><span data-stu-id="9cfff-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="9cfff-133">Jei pardavimo pasiūlymui priskirti tik išoriškai tvarkomi produktai, produktai tvarkomi „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="9cfff-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="9cfff-134">Tai padeda užtikrinti, kad nebandysite pardavimo pasiūlymo eilučių sinchronizuoti su produktais, kurių „Finance and Operations“ neatpažįsta.</span><span class="sxs-lookup"><span data-stu-id="9cfff-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="9cfff-135">Visi pasiūlymo produktai ir eilutės atnaujinami, įtraukiant pasiūlymo antraštės informaciją **Sudaro tik išoriškai tvarkomi produktai**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="9cfff-136">Šią informaciją galima rasti pasiūlymo eilutės objekto lauke **Pasiūlymą sudaro tik išoriškai tvarkomi produktai**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="9cfff-137">Sudėtinga „Finance and Operations“ sąranka valdo laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="9cfff-138">Ši sąranka šiuo metu nepalaiko integravimo susiejimo.</span><span class="sxs-lookup"><span data-stu-id="9cfff-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="9cfff-139">Dabartinėje versijoje laukus **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** valdo bei tvarko „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="9cfff-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="9cfff-140">„Sales“ versijoje šis sprendimas toliau nurodytus laukus nustato kaip tik skaitomus, nes reikšmės nėra sinchronizuojamos su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="9cfff-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="9cfff-141">**Tik skaitomi pardavimo pasiūlymo antraštės laukai:** Nuolaida %, Nuolaida, Transportavimo suma</span><span class="sxs-lookup"><span data-stu-id="9cfff-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="9cfff-142">**Tik skaitomi pardavimo pasiūlymo eilučių laukai:** Mokesčiai</span><span class="sxs-lookup"><span data-stu-id="9cfff-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="9cfff-143">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="9cfff-143">Preconditions and mapping setup</span></span>

- <span data-ttu-id="9cfff-144">Prieš sinchronizuodami pardavimo pasiūlymus, „Sales“ pasirinkite **Parametrai** &gt; **Administravimas** &gt; **Sistemos parametrai** &gt; **Pardavimas** ir įsitikinkite, kad laukas **Nuolaidos skaičiavimo būdas** nustatytas į parinktį **Taikoma vienetui**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-144">Before you synchronize sales quotations, in Sales, go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="9cfff-145">Šis parametras padeda užtikrinti, kad „Sales“ eilutės prekės nuolaida atitinka „Finance and Operations“ parametrą.</span><span class="sxs-lookup"><span data-stu-id="9cfff-145">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="9cfff-146">Priešingu atveju „Finance and Operations“ nuolaida bus neteisinga, nes „Finance and Operations“ nuolaidą skaičiuos kaip vienetui taikomą nuolaidą, net jei „Sales“ nustatyta eilutei taikoma nuolaida.</span><span class="sxs-lookup"><span data-stu-id="9cfff-146">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>
- <span data-ttu-id="9cfff-147">„Finance and Operations“ pasirinkite **Gautinos sumos** &gt; **Sąranka** &gt; **Gautinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-147">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="9cfff-148">Skirtuke **Numeracija** pasirinkite pardavimo pasiūlymų numeraciją ir tada spustelėkite **Peržiūrėti informaciją**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-148">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="9cfff-149">Tada dalyje **Bendroji Sąranka** nustatykite lauką **Neautomatinis** į parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-149">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="9cfff-150">„Finance and Operations“ pasirinkite **Gautinos sumos** &gt; **Sąranka** &gt; **Gautinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-150">In Finance and Operations, go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="9cfff-151">Tada skirtuke **Siuntos** nustatykite lauką **Pristatymo datos valdymas** į parinktį **Nėra**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-151">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="9cfff-152">Šis parametras padeda užtikrinti sėkmingą pardavimo pasiūlymų sinchronizavimą.</span><span class="sxs-lookup"><span data-stu-id="9cfff-152">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="9cfff-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="9cfff-153">QuoteHeader</span></span>

- <span data-ttu-id="9cfff-154">„Finance and Operations“ laukas **Pageidaujama pristatymo data** yra būtinas, ir sinchronizavimas nepavyksta, jei šis laukas bus tuščias.</span><span class="sxs-lookup"><span data-stu-id="9cfff-154">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="9cfff-155">Siekiant išvengti tokios problemos, jei laukas paliekamas tuščias, numatytoji data paimama iš čia: **Šaltinis &gt;CD**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-155">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="9cfff-156">Data turėtų būti atnaujinta į pageidaujamą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9cfff-156">The date should be updated to a preferred value.</span></span> <span data-ttu-id="9cfff-157">Šiuo metu negalima įvesti tokios reikšmės kaip **Šiandien**, kad ji nurodytų šios dienos datą.</span><span class="sxs-lookup"><span data-stu-id="9cfff-157">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="9cfff-158">Turite įvesti konkrečią datą.</span><span class="sxs-lookup"><span data-stu-id="9cfff-158">You must enter a specific date.</span></span> <span data-ttu-id="9cfff-159">Numatytoji šablono lauko **Pageidaujama pristatymo data** reikšmė yra **2020-01-01**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-159">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="9cfff-160">„Finance and Operations“ laukas **Adreso šalies regiono kodas** yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="9cfff-160">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="9cfff-161">Norėdami išvengti sinchronizavimo klaidų, galite nurodyti numatytąją reikšmę, kuri bus naudojama, jei „Sales“ laukas paliekamas tuščias.</span><span class="sxs-lookup"><span data-stu-id="9cfff-161">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="9cfff-162">Be to, ši numatytoji reikšmė yra naudinga, nes jums nereikia patiems įvesti reikšmės vietinio adreso lauke **Šalies regionas**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-162">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="9cfff-163">Numatytosios **DeliveryAddressCountryRegionISOCode** šablono reikšmės nėra.</span><span class="sxs-lookup"><span data-stu-id="9cfff-163">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="9cfff-164">Atnaujinkite **CDS organizacijos ID** susiejimą dalyje **Šaltinis &gt; CDS**, kad jis atitiktų **CDS organizaciją** objekte Organizacija.</span><span class="sxs-lookup"><span data-stu-id="9cfff-164">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="9cfff-165">Numatytoji **Organization_OrganizationId** šablono reikšmė yra **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-165">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="9cfff-166">Numatytoji **Account_Organization_OrganizationId** šablono reikšmė yra **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-166">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="9cfff-167">Numatytoji **InvoiceAccount_OrganizationId** šablono reikšmė yra **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-167">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

### <a name="quoteline"></a><span data-ttu-id="9cfff-168">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="9cfff-168">QuoteLine</span></span>

- <span data-ttu-id="9cfff-169">Atnaujinkite **CDS organizacijos ID** susiejimą dalyje **Šaltinis &gt; CDS**, kad jis atitiktų **CDS organizaciją** objekte Organizacija.</span><span class="sxs-lookup"><span data-stu-id="9cfff-169">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="9cfff-170">Numatytoji **Organization_OrganizationId** šablono reikšmė yra **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-170">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="9cfff-171">Numatytoji **Product_Organization_Organization_OrganizationId** šablono reikšmė yra **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-171">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="9cfff-172">Numatytoji **Quotation_Organization_Organization_OrganizationId** šablono reikšmė yra **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-172">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="9cfff-173">„Finance and Operations“ laukas **Pageidaujama pristatymo data** yra būtinas, ir sinchronizavimas nepavyksta, jei šis laukas bus tuščias.</span><span class="sxs-lookup"><span data-stu-id="9cfff-173">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="9cfff-174">Siekiant išvengti tokios problemos, jei laukas paliekamas tuščias, numatytoji data paimama iš čia: **Šaltinis &gt;CD**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-174">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="9cfff-175">Data turėtų būti atnaujinta į pageidaujamą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="9cfff-175">The date should be updated to a preferred value.</span></span> <span data-ttu-id="9cfff-176">Šiuo metu negalima įvesti tokios reikšmės kaip **Šiandien**, kad ji nurodytų šios dienos datą.</span><span class="sxs-lookup"><span data-stu-id="9cfff-176">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="9cfff-177">Turite įvesti konkrečią datą.</span><span class="sxs-lookup"><span data-stu-id="9cfff-177">You must enter a specific date.</span></span> <span data-ttu-id="9cfff-178">Numatytoji šablono lauko **Pageidaujama pristatymo data** reikšmė yra **2020-01-01**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-178">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="9cfff-179">Iš dalies **CDS &gt; Paskirties vieta** galite įtraukti toliau nurodytus susiejimus, norėdami užtikrinti, kad pasiūlymo eilutės importuojamos „Finance and Operations“, jei nenurodyta kliento arba produkto numatytoji informacija.</span><span class="sxs-lookup"><span data-stu-id="9cfff-179">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="9cfff-180">**SiteId** – vieta būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="9cfff-180">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="9cfff-181">Numatytosios **SiteId** šablono reikšmės nėra.</span><span class="sxs-lookup"><span data-stu-id="9cfff-181">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="9cfff-182">**WarehouseId** – sandėlis yra būtinas norint apdoroti pasiūlymus ir „Finance and Operations“ pardavimo užsakymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="9cfff-182">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="9cfff-183">Numatytosios **WarehouseId** šablono reikšmės nėra.</span><span class="sxs-lookup"><span data-stu-id="9cfff-183">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="9cfff-184">Įsitikinkite, kad **CDS &gt; Paskirties vieta** susiejime (**Quantity_UOM** į **SALESUNITSYMBOL**) yra būtina „Finance and Operations“ pardavimo matavimo vieneto (MV) reikšmių schema.</span><span class="sxs-lookup"><span data-stu-id="9cfff-184">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="9cfff-185">Šablono susiejimas duomenų integratoriuje</span><span class="sxs-lookup"><span data-stu-id="9cfff-185">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="9cfff-186">Sudėtinga „Finance and Operations“ sąranka valdo laukus **Nuolaida**, **Išlaidos** ir **Mokesčiai**.</span><span class="sxs-lookup"><span data-stu-id="9cfff-186">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="9cfff-187">Ši sąranka šiuo metu nepalaiko integravimo susiejimo.</span><span class="sxs-lookup"><span data-stu-id="9cfff-187">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="9cfff-188">Dabartinėje versijoje laukus **Kaina**, **Nuolaida**, **Išlaidos** ir **Mokesčiai** tvarko „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="9cfff-188">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="9cfff-189">Laukai **Mokėjimo sąlygos**, **Transportavimo sąlygos**, **Pristatymo sąlygos**, **Siuntimo būdas** ir **Pristatymo būdas** į numatytuosius susiejimus neįtraukti.</span><span class="sxs-lookup"><span data-stu-id="9cfff-189">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="9cfff-190">Norėdami susieti šiuos laukus, turite nustatyti reikšmių schemą, kuri atitinka organizacijų, tarp kurių objektas sinchronizuojamas, duomenis.</span><span class="sxs-lookup"><span data-stu-id="9cfff-190">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="9cfff-191">Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.</span><span class="sxs-lookup"><span data-stu-id="9cfff-191">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="9cfff-192">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="9cfff-192">QuoteHeader</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="9cfff-195">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="9cfff-195">QuoteLine</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Šablono susiejimas duomenų integratoriuje](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="9cfff-198">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="9cfff-198">Related topics</span></span>

[<span data-ttu-id="9cfff-199">Sinchronizuoti „Finance and Operations“ produktus su „Sales“ produktais</span><span class="sxs-lookup"><span data-stu-id="9cfff-199">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="9cfff-200">Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais</span><span class="sxs-lookup"><span data-stu-id="9cfff-200">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="9cfff-201">Sinchronizuoti Pardavimo kontaktus su „Finance and Operations“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="9cfff-201">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



