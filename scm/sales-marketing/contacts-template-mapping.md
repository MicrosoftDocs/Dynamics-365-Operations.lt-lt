---
title: "Sinchronizuoti Pardavimo kontaktus su „Finance and Operations“ kontaktais arba klientais"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ kontaktą (kontaktai) ir kontaktą (klientai) sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimu)."
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
ms.openlocfilehash: 7a856a9460d092925a34a0733f37f89354c2ddf1
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="f498a-103">Sinchronizuoti Pardavimo kontaktus su „Finance and Operations“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="f498a-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="f498a-104">Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai susipažinkite su [„Dynamics 365“ duomenų integravimo funkcija](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="f498a-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="f498a-105">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ („Sales“) kontakto (kontaktai) objektus ir kontaktą (klientai) sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimu, „Finance and Operations“).</span><span class="sxs-lookup"><span data-stu-id="f498a-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="f498a-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="f498a-106">Templates and tasks</span></span>

<span data-ttu-id="f498a-107">Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami sinchronizuojant „Sales“ kontaktą (kontaktai) su „Finance and Operations“ kontaktu (klientai).</span><span class="sxs-lookup"><span data-stu-id="f498a-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="f498a-108">**Šablono pavadinimai**</span><span class="sxs-lookup"><span data-stu-id="f498a-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="f498a-109">Iš kontaktų į kontaktą (iš „Sales“ į „Finance and Operations“)</span><span class="sxs-lookup"><span data-stu-id="f498a-109">Contacts to Contact (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="f498a-110">Iš kontaktų į klientą (iš „Sales“ į „Finance and Operations“)</span><span class="sxs-lookup"><span data-stu-id="f498a-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="f498a-111">**Užduočių pavadinimai projekte**</span><span class="sxs-lookup"><span data-stu-id="f498a-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="f498a-112">Kontaktai</span><span class="sxs-lookup"><span data-stu-id="f498a-112">Contacts</span></span>
    - <span data-ttu-id="f498a-113">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="f498a-113">ContactToCustomer</span></span>

<span data-ttu-id="f498a-114">Toliau nurodytą sinchronizavimo užduotį būtina atlikti prieš sinchronizuojant kontaktą: sąskaitos (iš „Sales“ į „Finance and Operations“)</span><span class="sxs-lookup"><span data-stu-id="f498a-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="f498a-115">Objektų rinkiniai</span><span class="sxs-lookup"><span data-stu-id="f498a-115">Entity sets</span></span>

| <span data-ttu-id="f498a-116">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="f498a-116">Sales</span></span>    | <span data-ttu-id="f498a-117">CDS</span><span class="sxs-lookup"><span data-stu-id="f498a-117">CDS</span></span>     | <span data-ttu-id="f498a-118">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="f498a-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="f498a-119">Kontaktai</span><span class="sxs-lookup"><span data-stu-id="f498a-119">Contacts</span></span> | <span data-ttu-id="f498a-120">Kontaktas</span><span class="sxs-lookup"><span data-stu-id="f498a-120">Contact</span></span> | <span data-ttu-id="f498a-121">CDS kontaktai</span><span class="sxs-lookup"><span data-stu-id="f498a-121">CDS Contacts</span></span>           |
| <span data-ttu-id="f498a-122">Kontaktai</span><span class="sxs-lookup"><span data-stu-id="f498a-122">Contacts</span></span> | <span data-ttu-id="f498a-123">Paskyra</span><span class="sxs-lookup"><span data-stu-id="f498a-123">Account</span></span> | <span data-ttu-id="f498a-124">Klientai V2</span><span class="sxs-lookup"><span data-stu-id="f498a-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="f498a-125">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="f498a-125">Entity flow</span></span>

<span data-ttu-id="f498a-126">Kontaktai valdomi programoje „Sales“ ir sinchronizuojami su „Finance and Operations“ programa „Common Data Service“ (CDS).</span><span class="sxs-lookup"><span data-stu-id="f498a-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="f498a-127">„Sales“ kontaktas gali tapti CDS ir „Finance and Operations“ kontaktu.</span><span class="sxs-lookup"><span data-stu-id="f498a-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="f498a-128">Taip pat jis gali atsidaryti sąskaitą CDS ir tapti „Finance and Operations“ klientu.</span><span class="sxs-lookup"><span data-stu-id="f498a-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="f498a-129">Norėdama nustatyti, ar kontaktą reikia paimti iš „Sales“ ir sinchronizuoti su CDS ir „Finance and Operations“ (pvz., „Sales“ kontaktus &gt;CDS kontaktą &gt; „Finance and Operations“ kontaktą), sistema ieško toliau nurodytų „Sales“ kontakto ypatybių.</span><span class="sxs-lookup"><span data-stu-id="f498a-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="f498a-130">**Sinchronizuojant su CDS sąskaita ir „Finance and Operations“ klientu:** kontaktų, kur lauko **Yra aktyvus klientas** reikšmė nustatyta į **Taip**</span><span class="sxs-lookup"><span data-stu-id="f498a-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="f498a-131">**Sinchronizuojant su CDS kontaktu ir „Finance and Operations“ kontaktu:** kontaktų, kur lauko **Yra aktyvus klientas** reikšmė nustatyta į **Ne**, o **įmonės** (pirminė sąskaita / kontaktas) taškai į sąskaitą (ne kontaktą).</span><span class="sxs-lookup"><span data-stu-id="f498a-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="f498a-132">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="f498a-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="f498a-133">Kontaktui įtrauktas naujas **Yra aktyvus klientas** laukas.</span><span class="sxs-lookup"><span data-stu-id="f498a-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="f498a-134">Šis laukas naudojamas kontaktams, pasižymintiems pardavimo veikla, ir kontaktams, nepasižymintiems pardavimo veikla, atskirti.</span><span class="sxs-lookup"><span data-stu-id="f498a-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="f498a-135">Lauko **Yra aktyvus klientas** reikšmė nustatyta į **Taip** tik kontaktams, turintiems susijusių pasiūlymų, užsakymų ar sąskaitų faktūrų.</span><span class="sxs-lookup"><span data-stu-id="f498a-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="f498a-136">Su „Finance and Operations“ sinchronizuojami tik kaip klientai pažymėti „Sales“ kontaktai.</span><span class="sxs-lookup"><span data-stu-id="f498a-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="f498a-137">Kontaktui įtrauktas naujas **IsCompanyAnAccount** laukas.</span><span class="sxs-lookup"><span data-stu-id="f498a-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="f498a-138">Šis laukas naudojamas nurodyti, ar kontaktas susietas su **sąskaitos** tipo įmone (pirmine sąskaita / kontaktu).</span><span class="sxs-lookup"><span data-stu-id="f498a-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="f498a-139">Ši informacija naudojama nustatant kontaktus, kuriuos su „Finance and Operations“ reikia sinchronizuoti kaip kontaktus.</span><span class="sxs-lookup"><span data-stu-id="f498a-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="f498a-140">Kontaktui įtrauktas naujas **Kontakto numeris**, kad būtų užtikrintas srities ir unikalus integravimo raktas.</span><span class="sxs-lookup"><span data-stu-id="f498a-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="f498a-141">Sukūrus naują kontaktą lauko **Kontakto numeris** vertė sugeneruojama automatiškai, naudojant numeraciją.</span><span class="sxs-lookup"><span data-stu-id="f498a-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="f498a-142">Vertę sudaro raidės **CON**, tada didėjanti numeracija ir iš šešių simbolių sudarytas priedėlis.</span><span class="sxs-lookup"><span data-stu-id="f498a-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="f498a-143">Pavyzdys: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="f498a-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="f498a-144">Į „Sales“ įtraukus „Sales“ skirtą integravimo sprendimą, atnaujinimo scenarijus, naudodamas pirmiau minėtą numeraciją, nustato esamų kontaktų lauką **Kontakto numeris**.</span><span class="sxs-lookup"><span data-stu-id="f498a-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="f498a-145">Taip pat atnaujinimo scenarijus visiems pardavimo veikla pasižymintiems klientams nustato lauko **Yra aktyvus klientas** reikšmę į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="f498a-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="f498a-146">Programoje „Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="f498a-146">In Finance and Operations</span></span> 

<span data-ttu-id="f498a-147">Kontaktai žymimi naudojant ypatybę **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="f498a-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="f498a-148">Ši ypatybė nurodo, kad nurodytas kontaktas tvarkomas išoriškai.</span><span class="sxs-lookup"><span data-stu-id="f498a-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="f498a-149">Tokiu atveju išoriškai tvarkomus kontaktus tvarko „Sales“.</span><span class="sxs-lookup"><span data-stu-id="f498a-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="f498a-150">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="f498a-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="f498a-151">Iš kontakto į kontaktą</span><span class="sxs-lookup"><span data-stu-id="f498a-151">Contact to Contact</span></span>

- <span data-ttu-id="f498a-152">Atnaujinkite **CDS organizacijos ID** susiejime **Šaltinis &gt;CDS**.</span><span class="sxs-lookup"><span data-stu-id="f498a-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="f498a-153">Numatytoji **Organization_OrganizationId [organizacijos ID]** šablono reikšmė yra **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f498a-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="f498a-154">Numatytoji **PrimaryAccount_Organization_OrganizationId [organizacijos ID]** šablono reikšmė yra **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f498a-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="f498a-155">„Finance and Operations“ laukas **Adreso šalies regiono kodas** yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="f498a-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="f498a-156">Norėdami išvengti sinchronizavimo klaidų, susiejime **CDS &gt; Operacijos** galite nurodyti numatytąją vertę.</span><span class="sxs-lookup"><span data-stu-id="f498a-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="f498a-157">Tokiu atveju, jei „Sales“ laukas paliekamas tuščias, bus naudojama numatytoji reikšmė.</span><span class="sxs-lookup"><span data-stu-id="f498a-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="f498a-158">Numatytoji **PrimaryAddressCountryRegionISOCode** šablono reikšmė vertė **USA**.</span><span class="sxs-lookup"><span data-stu-id="f498a-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="f498a-159">Įsitikinkite, kad „Finance and Operations“ yra toliau nurodyto lauko vertė.</span><span class="sxs-lookup"><span data-stu-id="f498a-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="f498a-160">Jei „Finance and Operations“ ši informacija nebūtina, galite pašalinti susiejimą iš susiejimo **CDS &gt; Paskirties vieta**.</span><span class="sxs-lookup"><span data-stu-id="f498a-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="f498a-161">**Lauko pavadinimas programoje „Finance and Operations“:** sprendimas</span><span class="sxs-lookup"><span data-stu-id="f498a-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="f498a-162">**Susiejimas:** PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="f498a-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="f498a-163">Iš kontakto į klientą</span><span class="sxs-lookup"><span data-stu-id="f498a-163">Contact to Customer</span></span>

- <span data-ttu-id="f498a-164">Atnaujinkite **CDS organizacijos ID** susiejime **Šaltinis &gt;CDS**.</span><span class="sxs-lookup"><span data-stu-id="f498a-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="f498a-165">Numatytoji **Organization_OrganizationId [organizacijos ID]** šablono reikšmė yra **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="f498a-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="f498a-166">„Finance and Operations“ laukas **Adreso šalies regiono kodas** yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="f498a-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="f498a-167">Norėdami išvengti sinchronizavimo klaidų, susiejime **CDS &gt; Paskirties vieta** galite nurodyti numatytąją vertę.</span><span class="sxs-lookup"><span data-stu-id="f498a-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="f498a-168">Tokiu atveju, jei „Sales“ laukas paliekamas tuščias, bus naudojama numatytoji reikšmė.</span><span class="sxs-lookup"><span data-stu-id="f498a-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="f498a-169">Numatytoji **PrimaryAddressCountryRegionISOCode** šablono reikšmė vertė **USA**.</span><span class="sxs-lookup"><span data-stu-id="f498a-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="f498a-170">Laukas **CustomerGroup** būtinas „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="f498a-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="f498a-171">Norėdami išvengti sinchronizavimo klaidų, susiejime **CDS &gt; Paskirties vieta** galite nurodyti numatytąją vertę.</span><span class="sxs-lookup"><span data-stu-id="f498a-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="f498a-172">Tokiu atveju, jei „Sales“ laukas paliekamas tuščias, bus naudojama numatytoji reikšmė.</span><span class="sxs-lookup"><span data-stu-id="f498a-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="f498a-173">Numatytoji **CustomerGroupId** šablono vertė yra **10**.</span><span class="sxs-lookup"><span data-stu-id="f498a-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="f498a-174">Pridėdami toliau nurodytus susiejimus iš **CDS &gt; Paskirties vietos** galite padėti sumažinti neautomatinių atnaujinimų, kurie būtini „Finance and Operations“, skaičių.</span><span class="sxs-lookup"><span data-stu-id="f498a-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="f498a-175">Galite naudoti numatytąją vertę arba verčių schemos vertę, pvz., **Šalis / regionas** arba **miestas**.</span><span class="sxs-lookup"><span data-stu-id="f498a-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="f498a-176">**SiteId** – numatytąją vietą taip pat galima nurodyti ant produktų programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="f498a-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="f498a-177">SiteId – vieta būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="f498a-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="f498a-178">Nenurodyta **SiteId** šablono vertė.</span><span class="sxs-lookup"><span data-stu-id="f498a-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="f498a-179">**WarehouseId** – numatytąjį sandėlį taip pat galima nurodyti ant produktų programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="f498a-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="f498a-180">Sandėlis būtinas norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="f498a-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="f498a-181">Nenurodyta **WarehouseId** šablono vertė.</span><span class="sxs-lookup"><span data-stu-id="f498a-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="f498a-182">**LanguageId** – kalba yra būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="f498a-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="f498a-183">Numatytoji **LanguageId** šablono vertė yra **en-us**.</span><span class="sxs-lookup"><span data-stu-id="f498a-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="f498a-184">Šablono susiejimas duomenų integratoriuje</span><span class="sxs-lookup"><span data-stu-id="f498a-184">Template mapping in data integrator</span></span>

<span data-ttu-id="f498a-185">Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.</span><span class="sxs-lookup"><span data-stu-id="f498a-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="f498a-186">Iš kontakto į kontaktą</span><span class="sxs-lookup"><span data-stu-id="f498a-186">Contact to Contact</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/contacts-template-mapping-data-integrator-1.png)

![Kontaktų šablono susiejimas duomenų integratoriuje](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="f498a-189">Iš kontakto į klientą</span><span class="sxs-lookup"><span data-stu-id="f498a-189">Contact to Customer</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/contacts-template-mapping-data-integrator-3.png)

![Kontaktų šablono susiejimas duomenų integratoriuje](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="f498a-192">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="f498a-192">Related topics</span></span>

[<span data-ttu-id="f498a-193">Sinchronizuoti „Finance and Operations“ produktus su „Sales“ produktais</span><span class="sxs-lookup"><span data-stu-id="f498a-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="f498a-194">Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais</span><span class="sxs-lookup"><span data-stu-id="f498a-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="f498a-195">Sinchronizuoti pardavimo pasiūlymų antraštes ir eilutes „Sales“ su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="f498a-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

