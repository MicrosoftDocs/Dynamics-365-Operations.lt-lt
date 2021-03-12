---
title: Bendrieji integruoto kliento duomenys
description: Šioje temoje aprašomas klientų duomenų integravimas tarp „Finance and Operations“ ir „Dataverse“.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: b7e9cd27bb918dc3a6088b45803329deb01a864e
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744406"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="daf81-103">Bendrieji integruoto kliento duomenys</span><span class="sxs-lookup"><span data-stu-id="daf81-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="daf81-104">Kliento duomenys gali būti tvarkomi daugiau nei vienoje „Dynamics 365” programoje.</span><span class="sxs-lookup"><span data-stu-id="daf81-104">Customer data can be mastered in more than one Dynamics 365 application.</span></span> <span data-ttu-id="daf81-105">Pavyzdžiui, kliento eilutė gali būti sukurta naudojant pardavimo veiklą programoje „Dynamics 365 Sales“ (modeliu pagrįstoje „Dynamics 365“ programoje) arba eilutė gali būti sukurta naudojant mažmeninės prekybos veiklą programoje „Dynamics 365 Commerce” („Finance and Operations” programoje).</span><span class="sxs-lookup"><span data-stu-id="daf81-105">For example, a customer row can originate though sales activity in Dynamics 365 Sales (a model-driven app in Dynamics 365), or a row can originate through retail activity in Dynamics 365 Commerce (a Finance and Operations app).</span></span> <span data-ttu-id="daf81-106">Neatsižvelgiant į tai, kur paimti kliento duomenys, jie integruojami fone.</span><span class="sxs-lookup"><span data-stu-id="daf81-106">No matter where where the customer data originates, it is integrated behind the scenes.</span></span> <span data-ttu-id="daf81-107">Integruotas kliento šablonas suteikia lankstumo tvarkant kliento duomenis programoje „Dynamics 365“ ir teikia išsamų kliento vaizdą „Dynamics 365“ programų pakete.</span><span class="sxs-lookup"><span data-stu-id="daf81-107">Integrated customer master gives you the flexibility to master customer data in any Dynamics 365 application and provides a comprehensive view of the customer across the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="daf81-108">Kliento duomenų srautas</span><span class="sxs-lookup"><span data-stu-id="daf81-108">Customer data flow</span></span>

<span data-ttu-id="daf81-109">*Klientas* yra aiškiai apibrėžta koncepcija programose.</span><span class="sxs-lookup"><span data-stu-id="daf81-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="daf81-110">Todėl kliento duomenų integravimas yra susijęs su klientų koncepcijos harmonizavimu tarp dviejų programų.</span><span class="sxs-lookup"><span data-stu-id="daf81-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="daf81-111">Tolesnėje iliustracijoje pateiktas kliento duomenų srautas.</span><span class="sxs-lookup"><span data-stu-id="daf81-111">The following illustration shows the customer data flow.</span></span>

![Kliento duomenų srautas](media/dual-write-customer-data-flow.png)

<span data-ttu-id="daf81-113">Klientai gali būti suskirstyti į du tipus: komerciniai/organizaciniai klientai ir vartotojai/galutiniai vartotojai.</span><span class="sxs-lookup"><span data-stu-id="daf81-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="daf81-114">Šie du klientų tipai „Finance and Operations“ ir „Dataverse“ yra saugomi ir tvarkomi skirtingai.</span><span class="sxs-lookup"><span data-stu-id="daf81-114">These two types of customers are stored and handled differently in Finance and Operations and Dataverse.</span></span>

<span data-ttu-id="daf81-115">„Finance and Operations“ tiek komercinių / organizacinių klientų, tiek vartotojų / galutinių vartotojų duomenys naudojami vienoje lentelėje, pavadintoje **CustTable** (CustCustomerV3Entity), ir jie klasifikuojami pagal atributą **Tipas**.</span><span class="sxs-lookup"><span data-stu-id="daf81-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="daf81-116">(Jei **Tipas** nustatytas kaip **Organizacija**, klientas yra komercinis/organizacinis klientas, o jei **Tipas** nustatytas kaip **Asmuo**, klientas yra vartotojas/galutinis vartotojas.) Pagrindinio kontaktinio asmens informacija tvarkoma naudojant lentelę „SMMContactPersonEntity”.</span><span class="sxs-lookup"><span data-stu-id="daf81-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity table.</span></span>

<span data-ttu-id="daf81-117">„Dataverse” komercinių/organizacinių klientų duomenys tvarkomi lentelėje Sąskaita ir jie yra identifikuojami kaip klientai, kai atributas **„RelationshipType”** yra nustatytas į **Klientas**.</span><span class="sxs-lookup"><span data-stu-id="daf81-117">In Dataverse, commercial/organizational customers are mastered in the Account table and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="daf81-118">Tiek vartotojus/galutinius vartotojus, tiek kontaktinius asmenis atstovauja lentelė Kontaktas.</span><span class="sxs-lookup"><span data-stu-id="daf81-118">Both consumers/end users and the contact person are represented by the Contact table.</span></span> <span data-ttu-id="daf81-119">Siekiant aiškiai atskirti vartotoją/galutinį vartotoją ir kontaktinį asmenį, lentelėje **Kontaktas** yra Bulio logikos žymė, pavadinta **Pardavimas**.</span><span class="sxs-lookup"><span data-stu-id="daf81-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** table has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="daf81-120">Jeigu **Pardavimas** yra **Teisinga**, kontaktas yra vartotojas/galutinis vartotojas, ir tam užsakymui gali būti kuriami pasiūlymai ir užsakymai.</span><span class="sxs-lookup"><span data-stu-id="daf81-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="daf81-121">Kai **Pardavimas** yra **Klaidinga**, kontaktas yra tik pirminis kliento kontaktinis asmuo.</span><span class="sxs-lookup"><span data-stu-id="daf81-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="daf81-122">Jeigu pasiūlyme ar užsakymo procese dalyvauja ne pardavimo kontaktas, **Pardavimas** nustatomas į **Teisinga**, kad kontaktas būtų pažymėtas kaip pardavimo kontaktas.</span><span class="sxs-lookup"><span data-stu-id="daf81-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="daf81-123">Kontaktas, kuris tapo pardavimo kontaktu, lieka pardavimo kontaktu.</span><span class="sxs-lookup"><span data-stu-id="daf81-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="daf81-124">Šablonai</span><span class="sxs-lookup"><span data-stu-id="daf81-124">Templates</span></span>

<span data-ttu-id="daf81-125">Kliento duomenys apima visą informaciją apie klientą, pvz., klientų grupę, adresus, kontaktinę informaciją, mokėjimo profilį, sąskaitos faktūros profilį ir lojalumo būseną.</span><span class="sxs-lookup"><span data-stu-id="daf81-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="daf81-126">Lentelių susiejimų rinkinys veikia kartu atliekant kliento duomenų sąveiką, kaip parodyta tolesnėje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="daf81-126">A collection of table maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="daf81-127">„Finance and Operations” programėlės</span><span class="sxs-lookup"><span data-stu-id="daf81-127">Finance and Operations apps</span></span> | <span data-ttu-id="daf81-128">Kitos „Dynamics 365” programos</span><span class="sxs-lookup"><span data-stu-id="daf81-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="daf81-129">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="daf81-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="daf81-130">CDS kontaktai V2</span><span class="sxs-lookup"><span data-stu-id="daf81-130">CDS Contacts V2</span></span>             | <span data-ttu-id="daf81-131">kontaktai</span><span class="sxs-lookup"><span data-stu-id="daf81-131">contacts</span></span>                        | <span data-ttu-id="daf81-132">Naudojant šį šabloną sinchronizuojama visa tiek klientų, tiek tiekėjų pirminė, antrinė ir tretinė kontaktinė informacija.</span><span class="sxs-lookup"><span data-stu-id="daf81-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="daf81-133">Klientų grupės</span><span class="sxs-lookup"><span data-stu-id="daf81-133">Customer groups</span></span>             | <span data-ttu-id="daf81-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="daf81-134">msdyn_customergroups</span></span>            | <span data-ttu-id="daf81-135">Naudojant šį šabloną sinchronizuojama klientų grupių informacija.</span><span class="sxs-lookup"><span data-stu-id="daf81-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="daf81-136">Kliento mokėjimo būdas</span><span class="sxs-lookup"><span data-stu-id="daf81-136">Customer payment method</span></span>     | <span data-ttu-id="daf81-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="daf81-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="daf81-138">Naudojant šį šabloną sinchronizuojama klientų mokėjimo būdų informacija.</span><span class="sxs-lookup"><span data-stu-id="daf81-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="daf81-139">Klientai V3</span><span class="sxs-lookup"><span data-stu-id="daf81-139">Customers V3</span></span>                | <span data-ttu-id="daf81-140">sąskaitos</span><span class="sxs-lookup"><span data-stu-id="daf81-140">accounts</span></span>                        | <span data-ttu-id="daf81-141">Naudojant šį šabloną sinchronizuojama komercinių ir organizacijos klientų bendroji informacija.</span><span class="sxs-lookup"><span data-stu-id="daf81-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="daf81-142">Klientai V3</span><span class="sxs-lookup"><span data-stu-id="daf81-142">Customers V3</span></span>                | <span data-ttu-id="daf81-143">kontaktai</span><span class="sxs-lookup"><span data-stu-id="daf81-143">contacts</span></span>                        | <span data-ttu-id="daf81-144">Naudojant šį šabloną sinchronizuojmi vartotojų ir galutinių vartotojų klientų bendrieji duomenys.</span><span class="sxs-lookup"><span data-stu-id="daf81-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="daf81-145">Pavadinimo afiksai</span><span class="sxs-lookup"><span data-stu-id="daf81-145">Name affixes</span></span>                | <span data-ttu-id="daf81-146">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="daf81-146">msdyn_nameaffixes</span></span>               | <span data-ttu-id="daf81-147">Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų pavadinimų afiksų nuorodos duomenys.</span><span class="sxs-lookup"><span data-stu-id="daf81-147">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="daf81-148">Mokėjimo dienos eilutės CDS V2</span><span class="sxs-lookup"><span data-stu-id="daf81-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="daf81-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="daf81-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="daf81-150">Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo dienų eilučių nuorodos duomenys.</span><span class="sxs-lookup"><span data-stu-id="daf81-150">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="daf81-151">Mokėjimo dienos CDS</span><span class="sxs-lookup"><span data-stu-id="daf81-151">Payment days CDS</span></span>            | <span data-ttu-id="daf81-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="daf81-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="daf81-153">Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo dienų nuorodos duomenys.</span><span class="sxs-lookup"><span data-stu-id="daf81-153">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="daf81-154">Mokėjimo grafiko eilutės</span><span class="sxs-lookup"><span data-stu-id="daf81-154">Payment schedule lines</span></span>      | <span data-ttu-id="daf81-155">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="daf81-155">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="daf81-156">Sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo grafikų eilučių nuorodos duomenys.</span><span class="sxs-lookup"><span data-stu-id="daf81-156">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="daf81-157">Mokėjimo grafikas</span><span class="sxs-lookup"><span data-stu-id="daf81-157">Payment schedule</span></span>            | <span data-ttu-id="daf81-158">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="daf81-158">msdyn_paymentschedules</span></span>          | <span data-ttu-id="daf81-159">Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo grafikų nuorodos duomenys.</span><span class="sxs-lookup"><span data-stu-id="daf81-159">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="daf81-160">Mokėjimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="daf81-160">Terms of payment</span></span>            | <span data-ttu-id="daf81-161">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="daf81-161">msdyn_paymentterms</span></span>              | <span data-ttu-id="daf81-162">Naudojant šį šabloną sinchronizuojami tiek klientų, tiek tiekėjų mokėjimo sąlygų nuorodos duomenys.</span><span class="sxs-lookup"><span data-stu-id="daf81-162">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
