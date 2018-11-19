---
title: "Tiesioginis „Sales“ kontaktų sinchronizavimas su „Finance and Operations“ kontaktais arba klientais"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ Objektus Kontaktas (Kontaktai) ir Kontaktas (Klientai) sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“."
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
ms.openlocfilehash: 5363c64cd1a475f0047c079d9166718ddc765f02
ms.contentlocale: lt-lt
ms.lasthandoff: 11/01/2018

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="30440-103">Tiesioginis „Sales“ kontaktų sinchronizavimas su „Finance and Operations“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="30440-103">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="30440-104">Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [Duomenų integravimas į „Common Data Service“, skirtą programoms](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="30440-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="30440-105">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ Objektus Kontaktas (Kontaktai) ir Kontaktas (Klientai) sinchronizuojant tiesiogiai su „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="30440-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) entities directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="30440-106">Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="30440-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="30440-107">Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Finance and Operations“ ir „Sales“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="30440-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="30440-108">Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Finance and Operations“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus.</span><span class="sxs-lookup"><span data-stu-id="30440-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="30440-109">Toliau pateiktoje iliustracijoje rodoma, kaip duomenys sinchronizuojami tarp „Finance and Operations“ ir „Sales“.</span><span class="sxs-lookup"><span data-stu-id="30440-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="30440-110">[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="30440-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="30440-111">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="30440-111">Templates and tasks</span></span>

<span data-ttu-id="30440-112">Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„PowerApps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="30440-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="30440-113">Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="30440-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="30440-114">Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami sinchronizuojant „Sales“ kontakto (kontaktai) objektą su „Finance and Operations“ kontakto (klientai) objektu.</span><span class="sxs-lookup"><span data-stu-id="30440-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) entities in Sales to Contact (Customers) entities in Finance and Operations:</span></span>

- <span data-ttu-id="30440-115">**Šablonų pavadinimai naudojant funkciją Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="30440-115">**Names of the templates in Data integration:**</span></span>

    - <span data-ttu-id="30440-116">Kontaktai (iš „Sales“ į „Finance and Operations“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="30440-116">Contacts (Sales to Fin and Ops) - Direct</span></span>
    - <span data-ttu-id="30440-117">Iš kontaktų į klientą (iš „Sales“ į „Finance and Operations“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="30440-117">Contacts to Customer (Sales to Fin and Ops) - Direct</span></span>

- <span data-ttu-id="30440-118">**Užduočių pavadinimai projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="30440-118">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="30440-119">Kontaktai</span><span class="sxs-lookup"><span data-stu-id="30440-119">Contacts</span></span>
    - <span data-ttu-id="30440-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="30440-120">ContactToCustomer</span></span>

<span data-ttu-id="30440-121">Toliau nurodytą sinchronizavimo užduotį būtina atlikti prieš įvykstant kontakto sinchronizavimui: Sąskaitos (iš „Sales“ į „Finance and Operations“)</span><span class="sxs-lookup"><span data-stu-id="30440-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="30440-122">Objektų rinkiniai</span><span class="sxs-lookup"><span data-stu-id="30440-122">Entity sets</span></span>

| <span data-ttu-id="30440-123">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="30440-123">Sales</span></span>    | <span data-ttu-id="30440-124">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="30440-124">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="30440-125">Kontaktai</span><span class="sxs-lookup"><span data-stu-id="30440-125">Contacts</span></span> | <span data-ttu-id="30440-126">CDS kontaktai</span><span class="sxs-lookup"><span data-stu-id="30440-126">CDS Contacts</span></span>           |
| <span data-ttu-id="30440-127">Kontaktai</span><span class="sxs-lookup"><span data-stu-id="30440-127">Contacts</span></span> | <span data-ttu-id="30440-128">Klientai V2</span><span class="sxs-lookup"><span data-stu-id="30440-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="30440-129">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="30440-129">Entity flow</span></span>

<span data-ttu-id="30440-130">Kontaktai tvarkomi „Sales“ ir sinchronizuojami su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="30440-130">Contacts are managed in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="30440-131">„Sales“ kontaktas gali tapti „Finance and Operations“ kontaktu arba klientu.</span><span class="sxs-lookup"><span data-stu-id="30440-131">A contact in Sales can become either a contact or a customer in Finance and Operations.</span></span> <span data-ttu-id="30440-132">Norėdama nustatyti, ar „Sales“ kontaktas su „Finance and Operations“ turi būti sinchronizuojamas kaip kontaktas ar klientas, sistema ieško toliau nurodytų „Sales“ kontakto ypatybių.</span><span class="sxs-lookup"><span data-stu-id="30440-132">To determine whether a contact in Sales should be synchronized to Finance and Operations as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="30440-133">**Sinchronizuojant su „Finance and Operations“ klientu:** kontaktų, kur lauko **Yra aktyvus klientas** reikšmė nustatyta į **Taip**</span><span class="sxs-lookup"><span data-stu-id="30440-133">**Synchronization to a customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="30440-134">**Sinchronizuojant su „Finance and Operations“ kontaktu:** kontaktų, kur lauko **Yra aktyvus klientas** reikšmė nustatyta į **Ne**, o **įmonės** (pirminė sąskaita / kontaktas) taškai – į sąskaitą (ne kontaktą).</span><span class="sxs-lookup"><span data-stu-id="30440-134">**Synchronization to a contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="30440-135">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="30440-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="30440-136">Kontaktui įtrauktas naujas **Yra aktyvus klientas** laukas.</span><span class="sxs-lookup"><span data-stu-id="30440-136">A new **Is Active Customer** field has been added to the contact.</span></span> <span data-ttu-id="30440-137">Šis laukas naudojamas kontaktams, pasižymintiems pardavimo veikla, ir kontaktams, nepasižymintiems pardavimo veikla, atskirti.</span><span class="sxs-lookup"><span data-stu-id="30440-137">This field is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="30440-138">Lauko **Yra aktyvus klientas** reikšmė nustatyta į **Taip** tik kontaktams, turintiems susijusių pasiūlymų, užsakymų ar sąskaitų faktūrų.</span><span class="sxs-lookup"><span data-stu-id="30440-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="30440-139">Su „Finance and Operations“ sinchronizuojami tik kaip klientai pažymėti „Sales“ kontaktai.</span><span class="sxs-lookup"><span data-stu-id="30440-139">Only those contacts are synchronized to Finance and Operations as customers.</span></span>

<span data-ttu-id="30440-140">Kontaktui įtrauktas naujas **IsCompanyAnAccount** laukas.</span><span class="sxs-lookup"><span data-stu-id="30440-140">A new **IsCompanyAnAccount** field has been added to the contact.</span></span> <span data-ttu-id="30440-141">Šis laukas nurodo, ar kontaktas susietas su **sąskaitos** tipo įmone (pirmine sąskaita / kontaktu).</span><span class="sxs-lookup"><span data-stu-id="30440-141">This field indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="30440-142">Ši informacija naudojama nustatant kontaktus, kuriuos su „Finance and Operations“ reikia sinchronizuoti kaip kontaktus.</span><span class="sxs-lookup"><span data-stu-id="30440-142">This information is used to identify contacts that should be synchronized to Finance and Operations as contacts.</span></span>

<span data-ttu-id="30440-143">Kontaktui įtrauktas naujas **Kontakto numeris**, kad būtų užtikrintas srities ir unikalus integravimo raktas.</span><span class="sxs-lookup"><span data-stu-id="30440-143">A new **Contact Number** field has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="30440-144">Sukūrus naują kontaktą, lauko **Kontakto numeris** vertė sugeneruojama automatiškai, naudojant numeraciją.</span><span class="sxs-lookup"><span data-stu-id="30440-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="30440-145">Vertę sudaro raidės **CON**, tada didėjanti numeracija ir iš šešių simbolių sudarytas priedėlis.</span><span class="sxs-lookup"><span data-stu-id="30440-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="30440-146">Pavyzdys: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="30440-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="30440-147">Pritaikius „Sales“ skirtą integravimo sprendimą, atnaujinimo scenarijus, naudodamas pirmiau minėtą numeraciją, nustato esamų kontaktų lauką **Kontakto numeris**.</span><span class="sxs-lookup"><span data-stu-id="30440-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** field for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="30440-148">Taip pat atnaujinimo scenarijus visiems pardavimo veikla pasižymintiems klientams nustato lauko **Yra aktyvus klientas** reikšmę į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="30440-148">The upgrade script also sets the **Is Active Customer** field to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="30440-149">Programoje „Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="30440-149">In Finance and Operations</span></span>

<span data-ttu-id="30440-150">Kontaktai žymimi naudojant ypatybę **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="30440-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="30440-151">Ši ypatybė nurodo, kad nurodytas kontaktas tvarkomas išoriškai.</span><span class="sxs-lookup"><span data-stu-id="30440-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="30440-152">Tokiu atveju išoriškai tvarkomus kontaktus tvarko „Sales“.</span><span class="sxs-lookup"><span data-stu-id="30440-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="30440-153">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="30440-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="30440-154">Iš kontakto į klientą</span><span class="sxs-lookup"><span data-stu-id="30440-154">Contact to customer</span></span>

- <span data-ttu-id="30440-155">Laukas **CustomerGroup** būtinas „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="30440-155">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="30440-156">Siekdami padėti išvengti sinchronizavimo klaidų, susiejime galite nurodyti numatytąją vertę.</span><span class="sxs-lookup"><span data-stu-id="30440-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="30440-157">Tokiu atveju, jei „Sales“ laukas paliekamas tuščias, bus naudojama numatytoji reikšmė.</span><span class="sxs-lookup"><span data-stu-id="30440-157">That default value is then used if the field is left blank in Sales.</span></span>

    <span data-ttu-id="30440-158">Numatytoji šablono vertė yra **10**.</span><span class="sxs-lookup"><span data-stu-id="30440-158">The default template value is **10**.</span></span>

- <span data-ttu-id="30440-159">Pridėdami toliau nurodytus susiejimus, galite padėti sumažinti neautomatinių atnaujinimų, kurie būtini „Finance and Operations“, skaičių.</span><span class="sxs-lookup"><span data-stu-id="30440-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="30440-160">Galite naudoti numatytąją vertę arba verčių schemos vertę, pvz., **Šalis / regionas** arba **miestas**.</span><span class="sxs-lookup"><span data-stu-id="30440-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="30440-161">**SiteId** – numatytąją vietą taip pat galima nurodyti ant produktų programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="30440-161">**SiteId** – A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="30440-162">SiteId – vieta būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="30440-162">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="30440-163">Nenurodyta **SiteId** šablono vertė.</span><span class="sxs-lookup"><span data-stu-id="30440-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="30440-164">**WarehouseId** – numatytąjį sandėlį taip pat galima nurodyti ant produktų programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="30440-164">**WarehouseId** – A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="30440-165">Sandėlis būtinas norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="30440-165">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="30440-166">Nenurodyta **WarehouseId** šablono vertė.</span><span class="sxs-lookup"><span data-stu-id="30440-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="30440-167">**LanguageId** – kalba yra būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="30440-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span>
    
        <span data-ttu-id="30440-168">Numatytoji paskirtoji šablono vertė yra **en-us**.</span><span class="sxs-lookup"><span data-stu-id="30440-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="30440-169">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="30440-169">Template mapping in Data integration</span></span>

<span data-ttu-id="30440-170">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="30440-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="30440-171">Susiejime rodoma, kuri lauko informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="30440-171">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="30440-172">Iš kontakto į kontaktą</span><span class="sxs-lookup"><span data-stu-id="30440-172">Contact to contact</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="30440-174">Iš kontakto į klientą</span><span class="sxs-lookup"><span data-stu-id="30440-174">Contact to customer</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="30440-176">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="30440-176">Related topics</span></span>

[<span data-ttu-id="30440-177">Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="30440-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="30440-178">Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Finance and Operations“ klientais</span><span class="sxs-lookup"><span data-stu-id="30440-178">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="30440-179">Tiesioginis „Finance and Operations“ produktų sinchronizavimas su „Sales“ produktais</span><span class="sxs-lookup"><span data-stu-id="30440-179">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="30440-180">Tiesioginis „Finance and Operations“ pardavimo užsakymų antraščių ir eilučių sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="30440-180">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="30440-181">Tiesioginis „Finance and Operations“ pardavimo sąskaitų faktūrų antraščių ir eilučių sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="30440-181">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)



