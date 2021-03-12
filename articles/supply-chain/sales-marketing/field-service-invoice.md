---
title: Sinchronizuokite „Field Service“ sutarčių SF su „Supply Chain Management“ laisvos formos SF
description: Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojamos sinchronizuojant „Dynamics 365 Field Service“ sutarčių SF su „Dynamics 365 Supply Chain Management“ laisvos formos SF.
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: f1790366cebf317472bc1ef9a5ecd2a19fe755d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980836"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="c305e-103">Sinchronizuokite „Field Service“ sutarčių SF su „Supply Chain Management“ laisvos formos SF</span><span class="sxs-lookup"><span data-stu-id="c305e-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c305e-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Dynamics 365 Field Service“ sutarčių SF su „Dynamics 365 Supply Chain Management“ laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="c305e-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c305e-105">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="c305e-105">Templates and tasks</span></span>

<span data-ttu-id="c305e-106">Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Field Service“ sutarčių SF su „Supply Chain Management“ laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="c305e-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="c305e-107">**Šablono pavadinimas naudojant funkciją Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="c305e-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="c305e-108">Sutarties SF („Field Service“ su „Supply Chain Management“)</span><span class="sxs-lookup"><span data-stu-id="c305e-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="c305e-109">**Užduočių pavadinimai projekte Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="c305e-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="c305e-110">SF antraštės</span><span class="sxs-lookup"><span data-stu-id="c305e-110">Invoice headers</span></span>
- <span data-ttu-id="c305e-111">SF eilutės</span><span class="sxs-lookup"><span data-stu-id="c305e-111">Invoice lines</span></span>

<span data-ttu-id="c305e-112">Prieš sinchronizuojant sutarčių SF, būtina atlikti toliau nurodytą sinchronizavimo užduotį.</span><span class="sxs-lookup"><span data-stu-id="c305e-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="c305e-113">Sąskaitos (iš „Sales” į „Supply Chain Management”) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="c305e-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="c305e-114">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="c305e-114">Entity set</span></span>

| <span data-ttu-id="c305e-115">„Field service“</span><span class="sxs-lookup"><span data-stu-id="c305e-115">Field Service</span></span>  | <span data-ttu-id="c305e-116">Tiekimo grandinės valdymas</span><span class="sxs-lookup"><span data-stu-id="c305e-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="c305e-117">SF</span><span class="sxs-lookup"><span data-stu-id="c305e-117">invoices</span></span>       | <span data-ttu-id="c305e-118">Dataverse kliento laisvos formos sąskaitų faktūrų antraštės</span><span class="sxs-lookup"><span data-stu-id="c305e-118">Dataverse customer free text invoice headers</span></span> |
| <span data-ttu-id="c305e-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="c305e-119">invoicedetails</span></span> | <span data-ttu-id="c305e-120">Dataverse kliento laisvos formos sąskaitų faktūrų eilutės</span><span class="sxs-lookup"><span data-stu-id="c305e-120">Dataverse customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="c305e-121">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="c305e-121">Entity flow</span></span>

<span data-ttu-id="c305e-122">SF, kurios buvo sukurtos iš „Field Service“ sutarties, su „Supply Chain Management“ galima sinchronizuoti per „Microsoft Dataverse“ duomenų integravimo projektą.</span><span class="sxs-lookup"><span data-stu-id="c305e-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="c305e-123">Jei laisvos formos SF apskaitos būsena yra **Vykdoma**, šių SF naujinimai bus sinchronizuojami su „Supply Chain Management“ laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="c305e-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="c305e-124">„Supply Chain Management“ paskelbus laisvos formos SF ir apskaitos būseną atnaujinus į **Baigta**, daugiau nebegalėsite sinchronizuoti „Field Service“ naujinimų.</span><span class="sxs-lookup"><span data-stu-id="c305e-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="c305e-125">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="c305e-125">Field Service CRM solution</span></span>

<span data-ttu-id="c305e-126">Stulpelis **Yra eilučių su sutarties kilme** įtrauktas į **Sąskaita faktūra** lentelę.</span><span class="sxs-lookup"><span data-stu-id="c305e-126">The **Has Lines With Agreement Origin** column has been added to the **Invoice** table.</span></span> <span data-ttu-id="c305e-127">Šis stulpelis padeda užtikrinti, kad bus sinchronizuojamos tik tos SF, kurios buvo sukurtos iš sutarties.</span><span class="sxs-lookup"><span data-stu-id="c305e-127">This column helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="c305e-128">Jei SF yra bent viena SF eilutė, kuri buvo perkelta iš sutarties, vertė yra **teisinga**.</span><span class="sxs-lookup"><span data-stu-id="c305e-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="c305e-129">Stulpelis **Turi sutarties kilmę** įtrauktas į **Sąskaitos faktūros eilutė** lentelę.</span><span class="sxs-lookup"><span data-stu-id="c305e-129">The **Has Agreement Origin** column has been added to the **Invoice Line** table.</span></span> <span data-ttu-id="c305e-130">Šis stulpelis padeda užtikrinti, kad bus sinchronizuojamos tik tos sąskaitos faktūros eilutės, kurios buvo sukurtos iš sutarties.</span><span class="sxs-lookup"><span data-stu-id="c305e-130">This column helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="c305e-131">Jei SF eilutė perkeliama iš sutarties, vertė yra **teisinga**.</span><span class="sxs-lookup"><span data-stu-id="c305e-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="c305e-132">Laukas **SF data** programoje „Supply Chain Management“ yra privalomas.</span><span class="sxs-lookup"><span data-stu-id="c305e-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="c305e-133">Todėl, prieš pradedant sinchronizavimą „Field Service“ stulpelyje turi būti nurodyta reikšmė.</span><span class="sxs-lookup"><span data-stu-id="c305e-133">Therefore, the column must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="c305e-134">Kad būtų atitiktas šis reikalavimas, įtraukiama toliau nurodyta logika.</span><span class="sxs-lookup"><span data-stu-id="c305e-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="c305e-135">Jei stulpelis **Sąskaitos faktūros data** lentelėje **Sąskaita faktūra** yra tuščias (tai yra, jame neįvesta jokia reikšmė), įtraukus sąskaitos faktūros eilutę, perkeltą iš sutarties, lauke bus įvesta dabartinė data.</span><span class="sxs-lookup"><span data-stu-id="c305e-135">If the **Invoice Date** column is blank on the **Invoice** table (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="c305e-136">Vartotojas gali pakeisti stulpelio **Sąskaitos faktūros data** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c305e-136">The user can change the **Invoice Date** column.</span></span> <span data-ttu-id="c305e-137">Tačiau, jei stulpelis **Sąskaitos faktūros data** SF bus tuščias, vartotojui bandant įrašyti sąskaitą faktūrą, perkeltą iš sutarties, bus pateikta verslo proceso klaida.</span><span class="sxs-lookup"><span data-stu-id="c305e-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** column is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c305e-138">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="c305e-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="c305e-139">„Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="c305e-139">In Supply Chain Management</span></span>

<span data-ttu-id="c305e-140">Kad būtų galima atskirti „Supply Chain Management“ laisvos formos SF, kurios buvo sukurtos remiantis „Field Service“ sutarties SF, integravime turi būti nustatyta SF kilmė.</span><span class="sxs-lookup"><span data-stu-id="c305e-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="c305e-141">Kai sąskaitos faktūros kilmė yra **Sutarties SF integravimas** tipo, laukas **Išorinis sąskaitos faktūros numeris** rodomas lauko **Pardavimo SF** antraštėje.</span><span class="sxs-lookup"><span data-stu-id="c305e-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="c305e-142">Lauko **Išorinis sąskaitos faktūros numeris** informacija, rodoma sąskaitos faktūros antraštėje, taip pat galima pasinaudoti, siekiant padėti užtikrinti, kad sąskaitos faktūros, kurios sukurtos remiantis „Field Service“ sutarčių SF, bus filtruojamos „Supply Chain Management“ sinchronizavimo su „Field Service“ metu.</span><span class="sxs-lookup"><span data-stu-id="c305e-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="c305e-143">Eikite į **Gautinos sumos** \> **Sąranka** \> **Sąskaitų faktūrų kilmės kodai**.</span><span class="sxs-lookup"><span data-stu-id="c305e-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="c305e-144">Norėdami sukurti naują sąskaitos faktūros kilmę, pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="c305e-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="c305e-145">Lauke **Sąskaitos faktūros kilmė** įveskite sąskaitos faktūros kilmės pavadinimą, pavyzdžiui, **FS**.</span><span class="sxs-lookup"><span data-stu-id="c305e-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="c305e-146">Lauke **Aprašas** įveskite aprašą, pvz., **„Field Service“ sutarties sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="c305e-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="c305e-147">Pasirinkite žymės langelį **Kilmės tipo priskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="c305e-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="c305e-148">Nustatykite lauko **Sąskaitos faktūros kilmės tipas** reikšmę į **Sutarties sąskaitos faktūros integravimas**.</span><span class="sxs-lookup"><span data-stu-id="c305e-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="c305e-149">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c305e-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="c305e-150">Duomenų integravimo projekte</span><span class="sxs-lookup"><span data-stu-id="c305e-150">In the Data Integration project</span></span>

<span data-ttu-id="c305e-151">Užduotis: **SF eilutės**</span><span class="sxs-lookup"><span data-stu-id="c305e-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="c305e-152">Įsitikinkite, kad numatytoji reikšmė „Supply Chain Management“ lauke **Pagrindinės sąskaitos rodoma reikšmė** yra atnaujinama, jog atitiktų norimą vertę.</span><span class="sxs-lookup"><span data-stu-id="c305e-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="c305e-153">Numatytoji šablono vertė yra **401100**.</span><span class="sxs-lookup"><span data-stu-id="c305e-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c305e-154">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="c305e-154">Template mapping in Data integration</span></span>

<span data-ttu-id="c305e-155">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="c305e-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="c305e-156">Sutarties SF („Field Service“ su „Supply Chain Management“): SF antraštės</span><span class="sxs-lookup"><span data-stu-id="c305e-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="c305e-157">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="c305e-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="c305e-158">Sutarties SF („Field Service“ su „Supply Chain Management“): SF eilutės</span><span class="sxs-lookup"><span data-stu-id="c305e-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="c305e-159">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="c305e-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>
