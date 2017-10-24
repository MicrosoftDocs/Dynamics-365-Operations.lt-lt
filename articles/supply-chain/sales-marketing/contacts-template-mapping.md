---
title: "Sinchronizuoti Pardavimo kontaktus su „Finance and Operations“ kontaktais arba klientais"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ kontaktą (kontaktai) ir kontaktą (klientai) sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimu)."
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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 41e27776b94df059ada13efb9a3dbf6a29d67f36
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="0bc9b-103">Sinchronizuoti Pardavimo kontaktus su „Finance and Operations“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="0bc9b-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="0bc9b-104">Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai susipažinkite su [„Dynamics 365“ duomenų integravimo funkcija](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="0bc9b-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="0bc9b-105">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Microsoft Dynamics 365 for Sales“ („Sales“) kontakto (kontaktai) objektus ir kontaktą (klientai) sinchronizuojant su „Microsoft Dynamics 365 for Finance and Operations“ („Enterprise“ leidimu, „Finance and Operations“).</span><span class="sxs-lookup"><span data-stu-id="0bc9b-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="0bc9b-106">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="0bc9b-106">Templates and tasks</span></span>

<span data-ttu-id="0bc9b-107">Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami sinchronizuojant „Sales“ kontaktą (kontaktai) su „Finance and Operations“ kontaktu (klientai).</span><span class="sxs-lookup"><span data-stu-id="0bc9b-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="0bc9b-108">**Šablono pavadinimai**</span><span class="sxs-lookup"><span data-stu-id="0bc9b-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="0bc9b-109">Kontaktai (iš „Sales“ į „Finance and Operations“)</span><span class="sxs-lookup"><span data-stu-id="0bc9b-109">Contacts (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="0bc9b-110">Iš kontaktų į klientą (iš „Sales“ į „Finance and Operations“)</span><span class="sxs-lookup"><span data-stu-id="0bc9b-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="0bc9b-111">**Užduočių pavadinimai projekte**</span><span class="sxs-lookup"><span data-stu-id="0bc9b-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="0bc9b-112">Kontaktai</span><span class="sxs-lookup"><span data-stu-id="0bc9b-112">Contacts</span></span>
    - <span data-ttu-id="0bc9b-113">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="0bc9b-113">ContactToCustomer</span></span>

<span data-ttu-id="0bc9b-114">Toliau nurodytą sinchronizavimo užduotį būtina atlikti prieš sinchronizuojant kontaktą: sąskaitos (iš „Sales“ į „Finance and Operations“)</span><span class="sxs-lookup"><span data-stu-id="0bc9b-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="0bc9b-115">Objektų rinkiniai</span><span class="sxs-lookup"><span data-stu-id="0bc9b-115">Entity sets</span></span>

| <span data-ttu-id="0bc9b-116">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="0bc9b-116">Sales</span></span>    | <span data-ttu-id="0bc9b-117">CDS</span><span class="sxs-lookup"><span data-stu-id="0bc9b-117">CDS</span></span>     | <span data-ttu-id="0bc9b-118">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="0bc9b-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="0bc9b-119">Kontaktai</span><span class="sxs-lookup"><span data-stu-id="0bc9b-119">Contacts</span></span> | <span data-ttu-id="0bc9b-120">Kontaktas</span><span class="sxs-lookup"><span data-stu-id="0bc9b-120">Contact</span></span> | <span data-ttu-id="0bc9b-121">CDS kontaktai</span><span class="sxs-lookup"><span data-stu-id="0bc9b-121">CDS Contacts</span></span>           |
| <span data-ttu-id="0bc9b-122">Kontaktai</span><span class="sxs-lookup"><span data-stu-id="0bc9b-122">Contacts</span></span> | <span data-ttu-id="0bc9b-123">Paskyra</span><span class="sxs-lookup"><span data-stu-id="0bc9b-123">Account</span></span> | <span data-ttu-id="0bc9b-124">Klientai V2</span><span class="sxs-lookup"><span data-stu-id="0bc9b-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="0bc9b-125">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="0bc9b-125">Entity flow</span></span>

<span data-ttu-id="0bc9b-126">Kontaktai valdomi programoje „Sales“ ir sinchronizuojami su „Finance and Operations“ programa „Common Data Service“ (CDS).</span><span class="sxs-lookup"><span data-stu-id="0bc9b-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="0bc9b-127">„Sales“ kontaktas gali tapti CDS ir „Finance and Operations“ kontaktu.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="0bc9b-128">Taip pat jis gali atsidaryti sąskaitą CDS ir tapti „Finance and Operations“ klientu.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="0bc9b-129">Norėdama nustatyti, ar kontaktą reikia paimti iš „Sales“ ir sinchronizuoti su CDS ir „Finance and Operations“ (pvz., „Sales“ kontaktus &gt;CDS kontaktą &gt; „Finance and Operations“ kontaktą), sistema ieško toliau nurodytų „Sales“ kontakto ypatybių.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="0bc9b-130">**Sinchronizuojant su CDS sąskaita ir „Finance and Operations“ klientu:** kontaktų, kur lauko **Yra aktyvus klientas** reikšmė nustatyta į **Taip**</span><span class="sxs-lookup"><span data-stu-id="0bc9b-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="0bc9b-131">**Sinchronizuojant su CDS kontaktu ir „Finance and Operations“ kontaktu:** kontaktų, kur lauko **Yra aktyvus klientas** reikšmė nustatyta į **Ne**, o **įmonės** (pirminė sąskaita / kontaktas) taškai į sąskaitą (ne kontaktą).</span><span class="sxs-lookup"><span data-stu-id="0bc9b-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="0bc9b-132">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="0bc9b-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="0bc9b-133">Kontaktui įtrauktas naujas **Yra aktyvus klientas** laukas.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="0bc9b-134">Šis laukas naudojamas kontaktams, pasižymintiems pardavimo veikla, ir kontaktams, nepasižymintiems pardavimo veikla, atskirti.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="0bc9b-135">Lauko **Yra aktyvus klientas** reikšmė nustatyta į **Taip** tik kontaktams, turintiems susijusių pasiūlymų, užsakymų ar sąskaitų faktūrų.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="0bc9b-136">Su „Finance and Operations“ sinchronizuojami tik kaip klientai pažymėti „Sales“ kontaktai.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="0bc9b-137">Kontaktui įtrauktas naujas **IsCompanyAnAccount** laukas.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="0bc9b-138">Šis laukas naudojamas nurodyti, ar kontaktas susietas su **sąskaitos** tipo įmone (pirmine sąskaita / kontaktu).</span><span class="sxs-lookup"><span data-stu-id="0bc9b-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="0bc9b-139">Ši informacija naudojama nustatant kontaktus, kuriuos su „Finance and Operations“ reikia sinchronizuoti kaip kontaktus.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="0bc9b-140">Kontaktui įtrauktas naujas **Kontakto numeris**, kad būtų užtikrintas srities ir unikalus integravimo raktas.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="0bc9b-141">Sukūrus naują kontaktą lauko **Kontakto numeris** vertė sugeneruojama automatiškai, naudojant numeraciją.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="0bc9b-142">Vertę sudaro raidės **CON**, tada didėjanti numeracija ir iš šešių simbolių sudarytas priedėlis.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="0bc9b-143">Pavyzdys: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="0bc9b-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="0bc9b-144">Į „Sales“ įtraukus „Sales“ skirtą integravimo sprendimą, atnaujinimo scenarijus, naudodamas pirmiau minėtą numeraciją, nustato esamų kontaktų lauką **Kontakto numeris**.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="0bc9b-145">Taip pat atnaujinimo scenarijus visiems pardavimo veikla pasižymintiems klientams nustato lauko **Yra aktyvus klientas** reikšmę į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="0bc9b-146">Programoje „Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="0bc9b-146">In Finance and Operations</span></span> 

<span data-ttu-id="0bc9b-147">Kontaktai žymimi naudojant ypatybę **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="0bc9b-148">Ši ypatybė nurodo, kad nurodytas kontaktas tvarkomas išoriškai.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="0bc9b-149">Tokiu atveju išoriškai tvarkomus kontaktus tvarko „Sales“.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="0bc9b-150">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="0bc9b-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="0bc9b-151">Iš kontakto į kontaktą</span><span class="sxs-lookup"><span data-stu-id="0bc9b-151">Contact to Contact</span></span>

- <span data-ttu-id="0bc9b-152">Atnaujinkite **CDS organizacijos ID** susiejime **Šaltinis &gt;CDS**.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="0bc9b-153">Numatytoji **Organization_OrganizationId [organizacijos ID]** šablono reikšmė yra **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="0bc9b-154">Numatytoji **PrimaryAccount_Organization_OrganizationId [organizacijos ID]** šablono reikšmė yra **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="0bc9b-155">„Finance and Operations“ laukas **Adreso šalies regiono kodas** yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="0bc9b-156">Norėdami išvengti sinchronizavimo klaidų, susiejime **CDS &gt; Operacijos** galite nurodyti numatytąją vertę.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="0bc9b-157">Tokiu atveju, jei „Sales“ laukas paliekamas tuščias, bus naudojama numatytoji reikšmė.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="0bc9b-158">Numatytoji **PrimaryAddressCountryRegionISOCode** šablono reikšmė vertė **USA**.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="0bc9b-159">Įsitikinkite, kad „Finance and Operations“ yra toliau nurodyto lauko vertė.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="0bc9b-160">Jei „Finance and Operations“ ši informacija nebūtina, galite pašalinti susiejimą iš susiejimo **CDS &gt; Paskirties vieta**.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="0bc9b-161">**Lauko pavadinimas programoje „Finance and Operations“:** sprendimas</span><span class="sxs-lookup"><span data-stu-id="0bc9b-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="0bc9b-162">**Susiejimas:** PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="0bc9b-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="0bc9b-163">Iš kontakto į klientą</span><span class="sxs-lookup"><span data-stu-id="0bc9b-163">Contact to Customer</span></span>

- <span data-ttu-id="0bc9b-164">Atnaujinkite **CDS organizacijos ID** susiejime **Šaltinis &gt;CDS**.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="0bc9b-165">Numatytoji **Organization_OrganizationId [organizacijos ID]** šablono reikšmė yra **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="0bc9b-166">„Finance and Operations“ laukas **Adreso šalies regiono kodas** yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="0bc9b-167">Norėdami išvengti sinchronizavimo klaidų, susiejime **CDS &gt; Paskirties vieta** galite nurodyti numatytąją vertę.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="0bc9b-168">Tokiu atveju, jei „Sales“ laukas paliekamas tuščias, bus naudojama numatytoji reikšmė.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="0bc9b-169">Numatytoji **PrimaryAddressCountryRegionISOCode** šablono reikšmė vertė **USA**.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="0bc9b-170">Laukas **CustomerGroup** būtinas „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="0bc9b-171">Norėdami išvengti sinchronizavimo klaidų, susiejime **CDS &gt; Paskirties vieta** galite nurodyti numatytąją vertę.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="0bc9b-172">Tokiu atveju, jei „Sales“ laukas paliekamas tuščias, bus naudojama numatytoji reikšmė.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="0bc9b-173">Numatytoji **CustomerGroupId** šablono vertė yra **10**.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="0bc9b-174">Pridėdami toliau nurodytus susiejimus iš **CDS &gt; Paskirties vietos** galite padėti sumažinti neautomatinių atnaujinimų, kurie būtini „Finance and Operations“, skaičių.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="0bc9b-175">Galite naudoti numatytąją vertę arba verčių schemos vertę, pvz., **Šalis / regionas** arba **miestas**.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="0bc9b-176">**SiteId** – numatytąją vietą taip pat galima nurodyti ant produktų programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="0bc9b-177">SiteId – vieta būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="0bc9b-178">Nenurodyta **SiteId** šablono vertė.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="0bc9b-179">**WarehouseId** – numatytąjį sandėlį taip pat galima nurodyti ant produktų programoje „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="0bc9b-180">Sandėlis būtinas norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="0bc9b-181">Nenurodyta **WarehouseId** šablono vertė.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="0bc9b-182">**LanguageId** – kalba yra būtina norint generuoti pasiūlymus ir „Finance and Operations“ pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="0bc9b-183">Numatytoji **LanguageId** šablono vertė yra **en-us**.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="0bc9b-184">Šablono susiejimas duomenų integratoriuje</span><span class="sxs-lookup"><span data-stu-id="0bc9b-184">Template mapping in data integrator</span></span>

<span data-ttu-id="0bc9b-185">Tolesnėse iliustracijose pateikiamas šablono susiejimo pavyzdys duomenų integratoriuje.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="0bc9b-186">Iš kontakto į kontaktą</span><span class="sxs-lookup"><span data-stu-id="0bc9b-186">Contact to Contact</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/contacts-template-mapping-data-integrator-1.png)

![Kontaktų šablono susiejimas duomenų integratoriuje](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="0bc9b-189">Iš kontakto į klientą</span><span class="sxs-lookup"><span data-stu-id="0bc9b-189">Contact to Customer</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/contacts-template-mapping-data-integrator-3.png)

![Kontaktų šablono susiejimas duomenų integratoriuje](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="0bc9b-192">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="0bc9b-192">Related topics</span></span>

[<span data-ttu-id="0bc9b-193">Sinchronizuoti „Finance and Operations“ produktus su „Sales“ produktais</span><span class="sxs-lookup"><span data-stu-id="0bc9b-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="0bc9b-194">Sinchronizuoti „Sales“ sąskaitas su „Finance and Operations“ klientais</span><span class="sxs-lookup"><span data-stu-id="0bc9b-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="0bc9b-195">Sinchronizuoti „Sales“ pardavimo pasiūlymų antraštes ir eilutes su „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="0bc9b-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="0bc9b-196">Sinchronizuoti „Finance and Operations“ pardavimo užsakymo antraštes ir eilutes su „Sales“</span><span class="sxs-lookup"><span data-stu-id="0bc9b-196">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="0bc9b-197">Sinchronizuoti „Finance and Operations“ pardavimo SF antraštes ir eilutes su „Sales“</span><span class="sxs-lookup"><span data-stu-id="0bc9b-197">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)

