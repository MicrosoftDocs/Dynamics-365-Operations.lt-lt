---
title: "„Field Service“ sutarčių SF sinchronizavimas su „Finance and Operations“ laisvos formos SF"
description: "Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Field Service“ sutarčių SF su „Microsoft Dynamics 365 for Finance and Operations“ laisvos formos SF."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 1863814d6dd645da8602495858d024fbad2e7149
ms.contentlocale: lt-lt
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a><span data-ttu-id="12fe8-103">„Field Service“ sutarčių SF sinchronizavimas su „Finance and Operations“ laisvos formos SF</span><span class="sxs-lookup"><span data-stu-id="12fe8-103">Synchronize agreement invoices in Field Service to free text invoices in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="12fe8-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Microsoft Dynamics 365 for Field Service“ sutarčių SF su „Microsoft Dynamics 365 for Finance and Operations“ laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="12fe8-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Microsoft Dynamics 365 for Field Service to free text invoices in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="12fe8-105">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="12fe8-105">Templates and tasks</span></span>

<span data-ttu-id="12fe8-106">Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Field Service“ sutarčių SF su „Finance and Operations“ laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="12fe8-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Finance and Operations.</span></span>

<span data-ttu-id="12fe8-107">**Šablono pavadinimas naudojant funkciją Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="12fe8-107">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="12fe8-108">Sutarčių SF (iš „Field Service“ į „Finance and Operations“)</span><span class="sxs-lookup"><span data-stu-id="12fe8-108">Agreement invoices (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="12fe8-109">**Užduočių pavadinimai projekte Duomenų integravimas:**</span><span class="sxs-lookup"><span data-stu-id="12fe8-109">**Names of the tasks in the Data integration project:**</span></span>

- <span data-ttu-id="12fe8-110">SF antraštės</span><span class="sxs-lookup"><span data-stu-id="12fe8-110">Invoice headers</span></span>
- <span data-ttu-id="12fe8-111">SF eilutės</span><span class="sxs-lookup"><span data-stu-id="12fe8-111">Invoice lines</span></span>

<span data-ttu-id="12fe8-112">Prieš sinchronizuojant sutarčių SF, būtina atlikti toliau nurodytą sinchronizavimo užduotį.</span><span class="sxs-lookup"><span data-stu-id="12fe8-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="12fe8-113">Sąskaitos (iš „Sales“ į „Finance and Operations“) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="12fe8-113">Accounts (Sales to Fin and Ops) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="12fe8-114">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="12fe8-114">Entity set</span></span>

| <span data-ttu-id="12fe8-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="12fe8-115">Field Service</span></span>  | <span data-ttu-id="12fe8-116">„Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="12fe8-116">Finance and Operations</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="12fe8-117">SF</span><span class="sxs-lookup"><span data-stu-id="12fe8-117">invoices</span></span>       | <span data-ttu-id="12fe8-118">CDS kliento laisvos formos sąskaitų faktūrų antraštės</span><span class="sxs-lookup"><span data-stu-id="12fe8-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="12fe8-119">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="12fe8-119">invoicedetails</span></span> | <span data-ttu-id="12fe8-120">CDS kliento laisvos formos sąskaitų faktūrų eilutės</span><span class="sxs-lookup"><span data-stu-id="12fe8-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="12fe8-121">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="12fe8-121">Entity flow</span></span>

<span data-ttu-id="12fe8-122">SF, kurios buvo sukurtos iš „Field Service“ sutarties, su „Finance and Operations“ galima sinchronizuoti per „Common Data Service“ (CDS) duomenų integravimo projektą.</span><span class="sxs-lookup"><span data-stu-id="12fe8-122">Invoices that are created from an agreement in Field Service can be synchronized to Finance and Operations via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="12fe8-123">Jei laisvos formos SF apskaitos būsena yra **Vykdoma**, šių SF naujinimai bus sinchronizuojami su „Finance and Operations“ laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="12fe8-123">Updates to these invoices will be synchronized to the free text invoices in Finance and Operations if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="12fe8-124">„Finance and Operations“ paskelbus laisvos formos SF ir apskaitos būseną atnaujinus į **Baigta**, daugiau nebegalėsite sinchronizuoti „Field Service“ naujinimų.</span><span class="sxs-lookup"><span data-stu-id="12fe8-124">After the free text invoices are posted in Finance and Operations, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="12fe8-125">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="12fe8-125">Field Service CRM solution</span></span>

<span data-ttu-id="12fe8-126">Laukas **Yra eilučių su sutarties kilme** įtrauktas į objektą **SF**.</span><span class="sxs-lookup"><span data-stu-id="12fe8-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="12fe8-127">Šis laukas padeda užtikrinti, kad bus sinchronizuojamos tik tos SF, kurios buvo sukurtos iš sutarties.</span><span class="sxs-lookup"><span data-stu-id="12fe8-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="12fe8-128">Jei SF yra bent viena SF eilutė, kuri buvo perkelta iš sutarties, vertė yra **teisinga**.</span><span class="sxs-lookup"><span data-stu-id="12fe8-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="12fe8-129">Laukas **Nurodyta sutarties kilmė** įtrauktas į objektą **SF eilutė**.</span><span class="sxs-lookup"><span data-stu-id="12fe8-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="12fe8-130">Šis laukas padeda užtikrinti, kad bus sinchronizuojamos tik tos SF eilutės, kurios buvo sukurtos iš sutarties.</span><span class="sxs-lookup"><span data-stu-id="12fe8-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="12fe8-131">Jei SF eilutė perkeliama iš sutarties, vertė yra **teisinga**.</span><span class="sxs-lookup"><span data-stu-id="12fe8-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="12fe8-132">Laukas **SF data** programoje „Finance and Operations“ yra privalomas.</span><span class="sxs-lookup"><span data-stu-id="12fe8-132">**Invoice date** is a mandatory field in Finance and Operations.</span></span> <span data-ttu-id="12fe8-133">Todėl, prieš pradedant sinchronizavimą „Field Service“ lauke turi būti nurodyta reikšmė.</span><span class="sxs-lookup"><span data-stu-id="12fe8-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="12fe8-134">Kad būtų atitiktas šis reikalavimas, įtraukiama toliau nurodyta logika.</span><span class="sxs-lookup"><span data-stu-id="12fe8-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="12fe8-135">Jei laukas **SF data** objekte **Sąskaita faktūra** yra tuščias (t. y., jame neįvesta jokia reikšmė), įtraukus SF eilutę, perkeltą iš sutarties, lauke bus įvesta dabartinė data.</span><span class="sxs-lookup"><span data-stu-id="12fe8-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="12fe8-136">Vartotojas gali pakeisti lauko **SF data** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="12fe8-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="12fe8-137">Tačiau, jei laukas **SF data** sąskaitoje faktūroje bus tuščias, vartotojui bandant įrašyti SF, perkeltą iš sutarties, bus pateikta verslo proceso klaida.</span><span class="sxs-lookup"><span data-stu-id="12fe8-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="12fe8-138">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="12fe8-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="12fe8-139">Programoje „Finance and Operations”</span><span class="sxs-lookup"><span data-stu-id="12fe8-139">In Finance and Operations</span></span>

<span data-ttu-id="12fe8-140">Kad būtų galima atskirti „Finance and Operations“ laisvos formos SF, kurios buvo sukurtos remiantis „Field Service“ sutarties SF, integravime turi būti nustatyta SF kilmė.</span><span class="sxs-lookup"><span data-stu-id="12fe8-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Finance and Operations that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="12fe8-141">Kai sąskaitos faktūros kilmė yra **Sutarties SF integravimas** tipo, laukas **Išorinis sąskaitos faktūros numeris** rodomas lauko **Pardavimo SF** antraštėje.</span><span class="sxs-lookup"><span data-stu-id="12fe8-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="12fe8-142">Lauko **Išorinis sąskaitos faktūros numeris** informacija, rodoma sąskaitos faktūros antraštėje, taip pat galima pasinaudoti, siekiant padėti užtikrinti, kad sąskaitos faktūros, kurios sukurtos remiantis „Field Service“ sutarčių SF, bus filtruojamos „Finance and Operations“ sinchronizavimo su „Field Service“ metu.</span><span class="sxs-lookup"><span data-stu-id="12fe8-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Finance and Operations to Field Service.</span></span>

1. <span data-ttu-id="12fe8-143">Eikite į **Gautinos sumos** \> **Sąranka** \> **Sąskaitų faktūrų kilmės kodai**.</span><span class="sxs-lookup"><span data-stu-id="12fe8-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="12fe8-144">Norėdami sukurti naują sąskaitos faktūros kilmę, pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="12fe8-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="12fe8-145">Lauke **Sąskaitos faktūros kilmė** įveskite sąskaitos faktūros kilmės pavadinimą, pavyzdžiui, **FS**.</span><span class="sxs-lookup"><span data-stu-id="12fe8-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="12fe8-146">Lauke **Aprašas** įveskite aprašą, pvz., **„Field Service“ sutarties sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="12fe8-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="12fe8-147">Pasirinkite žymės langelį **Kilmės tipo priskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="12fe8-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="12fe8-148">Nustatykite lauko **Sąskaitos faktūros kilmės tipas** reikšmę į **Sutarties sąskaitos faktūros integravimas**.</span><span class="sxs-lookup"><span data-stu-id="12fe8-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="12fe8-149">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="12fe8-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="12fe8-150">Duomenų integravimo projekte</span><span class="sxs-lookup"><span data-stu-id="12fe8-150">In the Data Integration project</span></span>

<span data-ttu-id="12fe8-151">Užduotis: **SF eilutės**</span><span class="sxs-lookup"><span data-stu-id="12fe8-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="12fe8-152">Įsitikinkite, kad numatytoji reikšmė „Finance and Operations“ lauke **Pagrindinės sąskaitos rodoma reikšmė** yra atnaujinama, jog atitiktų norimą vertę.</span><span class="sxs-lookup"><span data-stu-id="12fe8-152">Make sure that the default value for the Finance and Operations field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="12fe8-153">Numatytoji šablono vertė yra **401100**.</span><span class="sxs-lookup"><span data-stu-id="12fe8-153">The default template value is **401100**.</span></span>

