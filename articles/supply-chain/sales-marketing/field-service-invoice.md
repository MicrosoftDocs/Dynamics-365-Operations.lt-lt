---
title: „Field Service“ sutarčių SF sinchronizavimas su „Finance and Operations“ laisvos formos SF
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Field Service“ sutarčių SF su „Microsoft Dynamics 365 for Finance and Operations“ laisvos formos SF.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 55301ba39dd28fbae5b6c21b1da3c3d9cf6afd8a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "333259"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a><span data-ttu-id="decf8-103">„Field Service“ sutarčių sąskaitų faktūrų sinchronizavimas su „Finance and Operations“ laisvos formos sąskaitomis faktūromis</span><span class="sxs-lookup"><span data-stu-id="decf8-103">Synchronize agreement invoices in Field Service to free text invoices in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="decf8-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Field Service“ sutarčių SF su „Microsoft Dynamics 365 for Finance and Operations“ laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="decf8-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Microsoft Dynamics 365 for Field Service to free text invoices in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="decf8-105">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="decf8-105">Templates and tasks</span></span>

<span data-ttu-id="decf8-106">Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Field Service“ sutarčių SF su „Finance and Operations“ laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="decf8-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Finance and Operations.</span></span>

<span data-ttu-id="decf8-107">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="decf8-107">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="decf8-108">Sutarčių SF (iš „Field Service“ į „Finance and Operations“)</span><span class="sxs-lookup"><span data-stu-id="decf8-108">Agreement invoices (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="decf8-109">**Užduočių pavadinimai projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="decf8-109">**Names of the tasks in the Data integration project:**</span></span>

- <span data-ttu-id="decf8-110">SF antraštės</span><span class="sxs-lookup"><span data-stu-id="decf8-110">Invoice headers</span></span>
- <span data-ttu-id="decf8-111">SF eilutės</span><span class="sxs-lookup"><span data-stu-id="decf8-111">Invoice lines</span></span>

<span data-ttu-id="decf8-112">Prieš sinchronizuojant sutarčių SF, būtina atlikti toliau nurodytą sinchronizavimo užduotį.</span><span class="sxs-lookup"><span data-stu-id="decf8-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="decf8-113">Sąskaitos (iš „Sales“ į „Finance and Operations“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="decf8-113">Accounts (Sales to Fin and Ops) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="decf8-114">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="decf8-114">Entity set</span></span>

| <span data-ttu-id="decf8-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="decf8-115">Field Service</span></span>  | <span data-ttu-id="decf8-116">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="decf8-116">Finance and Operations</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="decf8-117">SF</span><span class="sxs-lookup"><span data-stu-id="decf8-117">invoices</span></span>       | <span data-ttu-id="decf8-118">CDS kliento laisvos formos sąskaitų faktūrų antraštės</span><span class="sxs-lookup"><span data-stu-id="decf8-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="decf8-119">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="decf8-119">invoicedetails</span></span> | <span data-ttu-id="decf8-120">CDS kliento laisvos formos sąskaitų faktūrų eilutės</span><span class="sxs-lookup"><span data-stu-id="decf8-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="decf8-121">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="decf8-121">Entity flow</span></span>

<span data-ttu-id="decf8-122">SF, kurios buvo sukurtos iš „Field Service“ sutarties, su „Finance and Operations“ galima sinchronizuoti per „Common Data Service“ (CDS) duomenų integravimo projektą.</span><span class="sxs-lookup"><span data-stu-id="decf8-122">Invoices that are created from an agreement in Field Service can be synchronized to Finance and Operations via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="decf8-123">Jei laisvos formos SF apskaitos būsena yra **Vykdoma**, šių SF naujinimai bus sinchronizuojami su „Finance and Operations“ laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="decf8-123">Updates to these invoices will be synchronized to the free text invoices in Finance and Operations if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="decf8-124">„Finance and Operations“ paskelbus laisvos formos SF ir apskaitos būseną atnaujinus į **Baigta**, daugiau nebegalėsite sinchronizuoti „Field Service“ naujinimų.</span><span class="sxs-lookup"><span data-stu-id="decf8-124">After the free text invoices are posted in Finance and Operations, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="decf8-125">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="decf8-125">Field Service CRM solution</span></span>

<span data-ttu-id="decf8-126">Laukas **Yra eilučių su sutarties kilme** įtrauktas į objektą **SF**.</span><span class="sxs-lookup"><span data-stu-id="decf8-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="decf8-127">Šis laukas padeda užtikrinti, kad bus sinchronizuojamos tik tos SF, kurios buvo sukurtos iš sutarties.</span><span class="sxs-lookup"><span data-stu-id="decf8-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="decf8-128">Jei SF yra bent viena SF eilutė, kuri buvo perkelta iš sutarties, vertė yra **teisinga**.</span><span class="sxs-lookup"><span data-stu-id="decf8-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="decf8-129">Laukas **Nurodyta sutarties kilmė** įtrauktas į objektą **SF eilutė**.</span><span class="sxs-lookup"><span data-stu-id="decf8-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="decf8-130">Šis laukas padeda užtikrinti, kad bus sinchronizuojamos tik tos SF eilutės, kurios buvo sukurtos iš sutarties.</span><span class="sxs-lookup"><span data-stu-id="decf8-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="decf8-131">Jei SF eilutė perkeliama iš sutarties, vertė yra **teisinga**.</span><span class="sxs-lookup"><span data-stu-id="decf8-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="decf8-132">Laukas **SF data** programoje „Finance and Operations“ yra privalomas.</span><span class="sxs-lookup"><span data-stu-id="decf8-132">**Invoice date** is a mandatory field in Finance and Operations.</span></span> <span data-ttu-id="decf8-133">Todėl, prieš pradedant sinchronizavimą „Field Service“ lauke turi būti nurodyta reikšmė.</span><span class="sxs-lookup"><span data-stu-id="decf8-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="decf8-134">Kad būtų atitiktas šis reikalavimas, įtraukiama toliau nurodyta logika.</span><span class="sxs-lookup"><span data-stu-id="decf8-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="decf8-135">Jei laukas **SF data** objekte **Sąskaita faktūra** yra tuščias (t. y., jame neįvesta jokia reikšmė), įtraukus SF eilutę, perkeltą iš sutarties, lauke bus įvesta dabartinė data.</span><span class="sxs-lookup"><span data-stu-id="decf8-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="decf8-136">Vartotojas gali pakeisti lauko **SF data** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="decf8-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="decf8-137">Tačiau, jei laukas **SF data** sąskaitoje faktūroje bus tuščias, vartotojui bandant įrašyti SF, perkeltą iš sutarties, bus pateikta verslo proceso klaida.</span><span class="sxs-lookup"><span data-stu-id="decf8-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="decf8-138">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="decf8-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="decf8-139">Programoje „Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="decf8-139">In Finance and Operations</span></span>

<span data-ttu-id="decf8-140">Kad būtų galima atskirti „Finance and Operations“ laisvos formos SF, kurios buvo sukurtos remiantis „Field Service“ sutarties SF, integravime turi būti nustatyta SF kilmė.</span><span class="sxs-lookup"><span data-stu-id="decf8-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Finance and Operations that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="decf8-141">Kai sąskaitos faktūros kilmė yra **Sutarties SF integravimas** tipo, laukas **Išorinis sąskaitos faktūros numeris** rodomas lauko **Pardavimo SF** antraštėje.</span><span class="sxs-lookup"><span data-stu-id="decf8-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="decf8-142">Lauko **Išorinis sąskaitos faktūros numeris** informacija, rodoma sąskaitos faktūros antraštėje, taip pat galima pasinaudoti, siekiant padėti užtikrinti, kad sąskaitos faktūros, kurios sukurtos remiantis „Field Service“ sutarčių SF, bus filtruojamos „Finance and Operations“ sinchronizavimo su „Field Service“ metu.</span><span class="sxs-lookup"><span data-stu-id="decf8-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Finance and Operations to Field Service.</span></span>

1. <span data-ttu-id="decf8-143">Eikite į **Gautinos sumos** \> **Sąranka** \> **Sąskaitų faktūrų kilmės kodai**.</span><span class="sxs-lookup"><span data-stu-id="decf8-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="decf8-144">Norėdami sukurti naują sąskaitos faktūros kilmę, pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="decf8-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="decf8-145">Lauke **Sąskaitos faktūros kilmė** įveskite sąskaitos faktūros kilmės pavadinimą, pavyzdžiui, **FS**.</span><span class="sxs-lookup"><span data-stu-id="decf8-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="decf8-146">Lauke **Aprašas** įveskite aprašą, pvz., **„Field Service“ sutarties sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="decf8-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="decf8-147">Pasirinkite žymės langelį **Kilmės tipo priskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="decf8-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="decf8-148">Nustatykite lauko **Sąskaitos faktūros kilmės tipas** reikšmę į **Sutarties sąskaitos faktūros integravimas**.</span><span class="sxs-lookup"><span data-stu-id="decf8-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="decf8-149">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="decf8-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="decf8-150">Duomenų integravimo projekte</span><span class="sxs-lookup"><span data-stu-id="decf8-150">In the Data Integration project</span></span>

<span data-ttu-id="decf8-151">Užduotis: **SF eilutės**</span><span class="sxs-lookup"><span data-stu-id="decf8-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="decf8-152">Įsitikinkite, kad numatytoji reikšmė „Finance and Operations“ lauke **Pagrindinės sąskaitos rodoma reikšmė** yra atnaujinama, jog atitiktų norimą vertę.</span><span class="sxs-lookup"><span data-stu-id="decf8-152">Make sure that the default value for the Finance and Operations field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="decf8-153">Numatytoji šablono vertė yra **401100**.</span><span class="sxs-lookup"><span data-stu-id="decf8-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="decf8-154">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="decf8-154">Template mapping in Data integration</span></span>

<span data-ttu-id="decf8-155">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="decf8-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a><span data-ttu-id="decf8-156">Sutarčių SF (iš „Field Service“ į „Finance and Operations“): SF antraštės</span><span class="sxs-lookup"><span data-stu-id="decf8-156">Agreement invoices (Field Service to Fin and Ops): Invoice headers</span></span>

<span data-ttu-id="decf8-157">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="decf8-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a><span data-ttu-id="decf8-158">Sutarčių SF (iš „Field Service“ į „Finance and Operations“): SF eilutės</span><span class="sxs-lookup"><span data-stu-id="decf8-158">Agreement invoices (Field Service to Fin and Ops): Invoice lines</span></span>

<span data-ttu-id="decf8-159">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="decf8-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>
