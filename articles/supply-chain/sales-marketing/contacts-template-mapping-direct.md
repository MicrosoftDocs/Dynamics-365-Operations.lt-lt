---
title: Tiesioginis „Sales“ kontaktų sinchronizavimas su „Supply Chain Management“ kontaktais arba klientais
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Sales“ objektus Kontaktas (Kontaktai) ir Kontaktas (Klientai) sinchronizuojant su „Dynamics 365 Supply Chain Management“.
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
ms.openlocfilehash: 81cf79c866ad70bf5bf2a9475a235bf3135d6e50
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840802"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a><span data-ttu-id="b262d-103">Tiesioginis „Sales“ kontaktų sinchronizavimas su „Supply Chain Management“ kontaktais arba klientais</span><span class="sxs-lookup"><span data-stu-id="b262d-103">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="b262d-104">Prieš naudodami sprendimą Potencialūs klientai ir grynieji pinigai, turėtumėte būti susipažinę su [Duomenų integravimas į „Microsoft Dataverse“, skirtą programoms](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="b262d-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="b262d-105">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami „Dynamics 365 Sales“ lenteles Kontaktas (Kontaktai) ir Kontaktas (Klientai) tiesiogiai sinchronizuojant su „Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="b262d-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) tables directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="b262d-106">Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai</span><span class="sxs-lookup"><span data-stu-id="b262d-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="b262d-107">Sprendime Potencialūs klientai ir grynieji pinigai naudojant funkciją Duomenų integravimas sinchronizuojami duomenys „Supply Chain Management“ ir „Sales“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="b262d-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="b262d-108">Naudojant sprendimo Potencialūs klientai ir grynieji pinigai šablonus, kuriuose galima taikyti funkciją Duomenų integravimas, galima kurti „Supply Chain Management“ ir „Sales“ duomenų apie sąskaitas, kontaktus, produktus, pardavimo pasiūlymus, pardavimo užsakymus ir pardavimo sąskaitas faktūras srautus.</span><span class="sxs-lookup"><span data-stu-id="b262d-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="b262d-109">Toliau pateiktoje iliustracijoje rodoma, kaip sinchronizuojami „Supply Chain Management “ ir „Sales“ duomenys.</span><span class="sxs-lookup"><span data-stu-id="b262d-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="b262d-110">[![Duomenų srautas sprendime Potencialūs klientai ir grynieji pinigai](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="b262d-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b262d-111">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="b262d-111">Templates and tasks</span></span>

<span data-ttu-id="b262d-112">Norėdami gauti prieigą prie pasiekiamų šablonų, atidarykite [„PowerApps“ administravimo centrą](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="b262d-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="b262d-113">Pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe – **Naujas projektas** ir pasirinkite viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="b262d-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b262d-114">Toliau pateikti šablonai ir pagrindinės užduotys yra naudojami sinchronizuojant „Sales“ kontakto (kontaktai) lenteles su „Supply Chain Management“ kontakto (klientai) lentele.</span><span class="sxs-lookup"><span data-stu-id="b262d-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) tables in Sales to Contact (Customers) tables in Supply Chain Management.</span></span>

- <span data-ttu-id="b262d-115">**Šablonų pavadinimai naudojant funkciją Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="b262d-115">**Names of the templates in Data integration**</span></span>

    - <span data-ttu-id="b262d-116">Kontaktai (iš „Sales” į „Supply Chain Management”) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="b262d-116">Contacts (Sales to Supply Chain Management) - Direct</span></span>
    - <span data-ttu-id="b262d-117">Iš kontaktų į klientą (iš „Sales” į „Supply Chain Management”) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="b262d-117">Contacts to Customer (Sales to Supply Chain Management) - Direct</span></span>

- <span data-ttu-id="b262d-118">**Užduočių pavadinimai projekte Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="b262d-118">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="b262d-119">Kontaktai</span><span class="sxs-lookup"><span data-stu-id="b262d-119">Contacts</span></span>
    - <span data-ttu-id="b262d-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="b262d-120">ContactToCustomer</span></span>

<span data-ttu-id="b262d-121">Toliau nurodytą sinchronizavimo užduotį būtina atlikti prieš įvykstant kontakto sinchronizavimui: Sąskaitos (iš „Sales“ į „Supply Chain Management“)</span><span class="sxs-lookup"><span data-stu-id="b262d-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Supply Chain Management)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="b262d-122">Objektų rinkiniai</span><span class="sxs-lookup"><span data-stu-id="b262d-122">Entity sets</span></span>

| <span data-ttu-id="b262d-123">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="b262d-123">Sales</span></span>    | <span data-ttu-id="b262d-124">„Supply Chain Management”</span><span class="sxs-lookup"><span data-stu-id="b262d-124">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="b262d-125">Kontaktai</span><span class="sxs-lookup"><span data-stu-id="b262d-125">Contacts</span></span> | <span data-ttu-id="b262d-126">„Dataverse” kontaktai</span><span class="sxs-lookup"><span data-stu-id="b262d-126">Dataverse Contacts</span></span>           |
| <span data-ttu-id="b262d-127">Kontaktai</span><span class="sxs-lookup"><span data-stu-id="b262d-127">Contacts</span></span> | <span data-ttu-id="b262d-128">Klientai V2</span><span class="sxs-lookup"><span data-stu-id="b262d-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="b262d-129">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="b262d-129">Entity flow</span></span>

<span data-ttu-id="b262d-130">Kontaktai valdomi programoje „Sales“ ir sinchronizuojami su „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="b262d-130">Contacts are managed in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="b262d-131">„Sales“ kontaktas gali tapti „Supply Chain Management“ kontaktu arba klientu.</span><span class="sxs-lookup"><span data-stu-id="b262d-131">A contact in Sales can become either a contact or a customer in Supply Chain Management.</span></span> <span data-ttu-id="b262d-132">Norėdama nustatyti, ar „Sales“ kontaktas su „Supply Chain Management“ turi būti sinchronizuojamas kaip kontaktas ar klientas, sistema ieško toliau nurodytų „Sales“ kontakto ypatybių.</span><span class="sxs-lookup"><span data-stu-id="b262d-132">To determine whether a contact in Sales should be synchronized to Supply Chain Management as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="b262d-133">**Sinchronizuojant su „Supply Chain Management“ klientu:** kontaktų, kur lauko **Yra aktyvus klientas** reikšmė nustatyta į **Taip**</span><span class="sxs-lookup"><span data-stu-id="b262d-133">**Synchronization to a customer in Supply Chain Management:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="b262d-134">**Sinchronizuojant su „Supply Chain Management“ kontaktu:** kontaktų, kur lauko **Yra aktyvus klientas** reikšmė nustatyta į **Ne**, o **įmonės** (pirminė sąskaita / kontaktas) taškai – į sąskaitą (ne kontaktą)</span><span class="sxs-lookup"><span data-stu-id="b262d-134">**Synchronization to a contact in Supply Chain Management:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b262d-135">„Sales“ skirtas potencialių klientų ir grynųjų pinigų sprendimas</span><span class="sxs-lookup"><span data-stu-id="b262d-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="b262d-136">Kontaktui įtrauktas naujas **Yra aktyvus klientas** stulpelis.</span><span class="sxs-lookup"><span data-stu-id="b262d-136">A new **Is Active Customer** column has been added to the contact.</span></span> <span data-ttu-id="b262d-137">Šis stulpelis naudojamas kontaktams, pasižymintiems pardavimo veikla, ir kontaktams, nepasižymintiems pardavimo veikla, atskirti.</span><span class="sxs-lookup"><span data-stu-id="b262d-137">This column is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="b262d-138">Lauko **Yra aktyvus klientas** reikšmė nustatyta į **Taip** tik kontaktams, turintiems susijusių pasiūlymų, užsakymų ar sąskaitų faktūrų.</span><span class="sxs-lookup"><span data-stu-id="b262d-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="b262d-139">Su „Supply Chain Management“ sinchronizuojami tik kaip klientai pažymėti „Sales“ kontaktai.</span><span class="sxs-lookup"><span data-stu-id="b262d-139">Only those contacts are synchronized to Supply Chain Management as customers.</span></span>

<span data-ttu-id="b262d-140">Kontaktui įtrauktas naujas **„IsCompanyAnAccount”** stulpelis.</span><span class="sxs-lookup"><span data-stu-id="b262d-140">A new **IsCompanyAnAccount** column has been added to the contact.</span></span> <span data-ttu-id="b262d-141">Šis stulpelis nurodo, ar kontaktas susietas su **sąskaitos** tipo įmone (pirmine sąskaita / kontaktu).</span><span class="sxs-lookup"><span data-stu-id="b262d-141">This column indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="b262d-142">Ši informacija naudojama nustatant kontaktus, kuriuos su „Supply Chain Management“ reikia sinchronizuoti kaip kontaktus.</span><span class="sxs-lookup"><span data-stu-id="b262d-142">This information is used to identify contacts that should be synchronized to Supply Chain Management as contacts.</span></span>

<span data-ttu-id="b262d-143">Kontaktui įtrauktas naujas stulpelis **Kontakto numeris** tam, kad būtų užtikrintas srities ir unikalus integravimo raktas.</span><span class="sxs-lookup"><span data-stu-id="b262d-143">A new **Contact Number** column has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="b262d-144">Sukūrus naują kontaktą, lauko **Kontakto numeris** vertė sugeneruojama automatiškai, naudojant numeraciją.</span><span class="sxs-lookup"><span data-stu-id="b262d-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="b262d-145">Vertę sudaro raidės **CON**, tada didėjanti numeracija ir iš šešių simbolių sudarytas priedėlis.</span><span class="sxs-lookup"><span data-stu-id="b262d-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="b262d-146">Pavyzdys: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="b262d-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="b262d-147">Pritaikius „Sales“ skirtą integravimo sprendimą, atnaujinimo scenarijus nustato esamų kontaktų stulpelį **Kontakto numeris** naudodamas anksčiau minėtą numeraciją.</span><span class="sxs-lookup"><span data-stu-id="b262d-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** column for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="b262d-148">Taip pat atnaujinimo scenarijus nustato lauko **Yra aktyvus klientas** reikšmę į **Taip** visiems pardavimo veikla pasižymintiems klientams.</span><span class="sxs-lookup"><span data-stu-id="b262d-148">The upgrade script also sets the **Is Active Customer** column to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-supply-chain-management"></a><span data-ttu-id="b262d-149">„Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="b262d-149">In Supply Chain Management</span></span>

<span data-ttu-id="b262d-150">Kontaktai žymimi naudojant ypatybę **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="b262d-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="b262d-151">Ši ypatybė nurodo, kad nurodytas kontaktas tvarkomas išoriškai.</span><span class="sxs-lookup"><span data-stu-id="b262d-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="b262d-152">Tokiu atveju išoriškai tvarkomus kontaktus tvarko „Sales“.</span><span class="sxs-lookup"><span data-stu-id="b262d-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="b262d-153">Išankstinės sąlygos ir susiejimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="b262d-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="b262d-154">Iš kontakto į klientą</span><span class="sxs-lookup"><span data-stu-id="b262d-154">Contact to customer</span></span>

- <span data-ttu-id="b262d-155">Laukas **CustomerGroup** būtinas „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="b262d-155">**CustomerGroup** is required in Supply Chain Management.</span></span> <span data-ttu-id="b262d-156">Siekdami padėti išvengti sinchronizavimo klaidų, susiejime galite nurodyti numatytąją vertę.</span><span class="sxs-lookup"><span data-stu-id="b262d-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="b262d-157">Bus naudojama numatytoji reikšmė, jei „Sales“ stulpelis yra paliktas tuščias.</span><span class="sxs-lookup"><span data-stu-id="b262d-157">That default value is then used if the column is left blank in Sales.</span></span>

    <span data-ttu-id="b262d-158">Numatytoji šablono vertė yra **10**.</span><span class="sxs-lookup"><span data-stu-id="b262d-158">The default template value is **10**.</span></span>

- <span data-ttu-id="b262d-159">Pridėdami toliau nurodytus susiejimus, galite padėti sumažinti neautomatinių atnaujinimų, kurie būtini „Supply Chain Management“, skaičių.</span><span class="sxs-lookup"><span data-stu-id="b262d-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="b262d-160">Galite naudoti numatytąją vertę arba verčių schemos vertę, pvz., **Šalis / regionas** arba **miestas**.</span><span class="sxs-lookup"><span data-stu-id="b262d-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="b262d-161">**SiteId** – numatytąją vietą taip pat galima nurodyti ant produktų programoje „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="b262d-161">**SiteId** – A default site can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="b262d-162">Vieta būtina norint generuoti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="b262d-162">A site is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="b262d-163">Nenurodyta **SiteId** šablono vertė.</span><span class="sxs-lookup"><span data-stu-id="b262d-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="b262d-164">**WarehouseId** – numatytąjį sandėlį taip pat galima nurodyti ant produktų programoje „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="b262d-164">**WarehouseId** – A default warehouse can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="b262d-165">Sandėlis būtinas norint generuoti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="b262d-165">A warehouse is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="b262d-166">Nenurodyta **WarehouseId** šablono vertė.</span><span class="sxs-lookup"><span data-stu-id="b262d-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="b262d-167">**LanguageId** – kalba būtina norint generuoti pasiūlymus ir „Supply Chain Management“ pardavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="b262d-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>
    
        <span data-ttu-id="b262d-168">Numatytoji paskirtoji šablono vertė yra **en-us**.</span><span class="sxs-lookup"><span data-stu-id="b262d-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b262d-169">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="b262d-169">Template mapping in Data integration</span></span>

<span data-ttu-id="b262d-170">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimo pavyzdys naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="b262d-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="b262d-171">Susiejime rodoma, kuri stulpelio informacija bus sinchronizuota atliekant „Sales“ sinchronizavimą su „Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="b262d-171">The mapping shows which column information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="b262d-172">Iš kontakto į kontaktą</span><span class="sxs-lookup"><span data-stu-id="b262d-172">Contact to contact</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="b262d-174">Iš kontakto į klientą</span><span class="sxs-lookup"><span data-stu-id="b262d-174">Contact to customer</span></span>

![Šablono susiejimas duomenų integratoriuje](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="b262d-176">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="b262d-176">Related topics</span></span>

[<span data-ttu-id="b262d-177">Potencialaus kliento pavertimas pinigais</span><span class="sxs-lookup"><span data-stu-id="b262d-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="b262d-178">Tiesioginis „Sales“ sąskaitų sinchronizavimas su „Supply Chain Management“ klientais</span><span class="sxs-lookup"><span data-stu-id="b262d-178">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="b262d-179">Tiesioginis „Supply Chain Management“ produktų sinchronizavimas su „Sales“ produktais</span><span class="sxs-lookup"><span data-stu-id="b262d-179">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="b262d-180">Tiesioginis pardavimo užsakymų sinchronizavimas tarp „Sales“ ir „Supply Chain Management”</span><span class="sxs-lookup"><span data-stu-id="b262d-180">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="b262d-181">Tiesioginis „Supply Chain Management“ pardavimo SF antraščių ir eilučių sinchronizavimas su „Sales“</span><span class="sxs-lookup"><span data-stu-id="b262d-181">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]