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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: c2d0f671d4b824cb5d38a5d11c4b06b2e97bd0c8
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528250"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="c26cc-103">Sinchronizuokite „Field Service“ sutarčių SF su „Supply Chain Management“ laisvos formos SF</span><span class="sxs-lookup"><span data-stu-id="c26cc-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c26cc-104">Šioje temoje aptariami šablonai ir pagrindinės užduotys, naudojami sinchronizuojant „Dynamics 365 Field Service“ sutarčių SF su „Dynamics 365 Supply Chain Management“ laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="c26cc-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c26cc-105">Šablonai ir užduotys</span><span class="sxs-lookup"><span data-stu-id="c26cc-105">Templates and tasks</span></span>

<span data-ttu-id="c26cc-106">Toliau nurodytas šablonas ir pagrindinės užduotys naudojami sinchronizuojant „Field Service“ sutarčių SF su „Supply Chain Management“ laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="c26cc-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="c26cc-107">**Šablono pavadinimas naudojant funkciją Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="c26cc-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="c26cc-108">Sutarties SF („Field Service“ su „Supply Chain Management“)</span><span class="sxs-lookup"><span data-stu-id="c26cc-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="c26cc-109">**Užduočių pavadinimai projekte Duomenų integravimas**</span><span class="sxs-lookup"><span data-stu-id="c26cc-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="c26cc-110">SF antraštės</span><span class="sxs-lookup"><span data-stu-id="c26cc-110">Invoice headers</span></span>
- <span data-ttu-id="c26cc-111">SF eilutės</span><span class="sxs-lookup"><span data-stu-id="c26cc-111">Invoice lines</span></span>

<span data-ttu-id="c26cc-112">Prieš sinchronizuojant sutarčių SF, būtina atlikti toliau nurodytą sinchronizavimo užduotį.</span><span class="sxs-lookup"><span data-stu-id="c26cc-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="c26cc-113">Sąskaitos (iš „Sales” į „Supply Chain Management”) – tiesioginis</span><span class="sxs-lookup"><span data-stu-id="c26cc-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="c26cc-114">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="c26cc-114">Entity set</span></span>

| <span data-ttu-id="c26cc-115">„Field Service“</span><span class="sxs-lookup"><span data-stu-id="c26cc-115">Field Service</span></span>  | <span data-ttu-id="c26cc-116">„Supply Chain Management”</span><span class="sxs-lookup"><span data-stu-id="c26cc-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="c26cc-117">SF</span><span class="sxs-lookup"><span data-stu-id="c26cc-117">invoices</span></span>       | <span data-ttu-id="c26cc-118">CDS kliento laisvos formos sąskaitų faktūrų antraštės</span><span class="sxs-lookup"><span data-stu-id="c26cc-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="c26cc-119">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="c26cc-119">invoicedetails</span></span> | <span data-ttu-id="c26cc-120">CDS kliento laisvos formos sąskaitų faktūrų eilutės</span><span class="sxs-lookup"><span data-stu-id="c26cc-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="c26cc-121">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="c26cc-121">Entity flow</span></span>

<span data-ttu-id="c26cc-122">SF, kurios buvo sukurtos iš „Field Service“ sutarties, su „Supply Chain Management“ galima sinchronizuoti per „Common Data Service“ duomenų integravimo projektą.</span><span class="sxs-lookup"><span data-stu-id="c26cc-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Common Data Service Data integration project.</span></span> <span data-ttu-id="c26cc-123">Jei laisvos formos SF apskaitos būsena yra **Vykdoma**, šių SF naujinimai bus sinchronizuojami su „Supply Chain Management“ laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="c26cc-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="c26cc-124">„Supply Chain Management“ paskelbus laisvos formos SF ir apskaitos būseną atnaujinus į **Baigta**, daugiau nebegalėsite sinchronizuoti „Field Service“ naujinimų.</span><span class="sxs-lookup"><span data-stu-id="c26cc-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="c26cc-125">„Field Service“ CRM sprendimas</span><span class="sxs-lookup"><span data-stu-id="c26cc-125">Field Service CRM solution</span></span>

<span data-ttu-id="c26cc-126">Laukas **Yra eilučių su sutarties kilme** įtrauktas į objektą **SF**.</span><span class="sxs-lookup"><span data-stu-id="c26cc-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="c26cc-127">Šis laukas padeda užtikrinti, kad bus sinchronizuojamos tik tos SF, kurios buvo sukurtos iš sutarties.</span><span class="sxs-lookup"><span data-stu-id="c26cc-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="c26cc-128">Jei SF yra bent viena SF eilutė, kuri buvo perkelta iš sutarties, vertė yra **teisinga**.</span><span class="sxs-lookup"><span data-stu-id="c26cc-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="c26cc-129">Laukas **Nurodyta sutarties kilmė** įtrauktas į objektą **SF eilutė**.</span><span class="sxs-lookup"><span data-stu-id="c26cc-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="c26cc-130">Šis laukas padeda užtikrinti, kad bus sinchronizuojamos tik tos SF eilutės, kurios buvo sukurtos iš sutarties.</span><span class="sxs-lookup"><span data-stu-id="c26cc-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="c26cc-131">Jei SF eilutė perkeliama iš sutarties, vertė yra **teisinga**.</span><span class="sxs-lookup"><span data-stu-id="c26cc-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="c26cc-132">Laukas **SF data** programoje „Supply Chain Management“ yra privalomas.</span><span class="sxs-lookup"><span data-stu-id="c26cc-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="c26cc-133">Todėl, prieš pradedant sinchronizavimą „Field Service“ lauke turi būti nurodyta reikšmė.</span><span class="sxs-lookup"><span data-stu-id="c26cc-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="c26cc-134">Kad būtų atitiktas šis reikalavimas, įtraukiama toliau nurodyta logika.</span><span class="sxs-lookup"><span data-stu-id="c26cc-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="c26cc-135">Jei laukas **SF data** objekte **Sąskaita faktūra** yra tuščias (t. y., jame neįvesta jokia reikšmė), įtraukus SF eilutę, perkeltą iš sutarties, lauke bus įvesta dabartinė data.</span><span class="sxs-lookup"><span data-stu-id="c26cc-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="c26cc-136">Vartotojas gali pakeisti lauko **SF data** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="c26cc-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="c26cc-137">Tačiau, jei laukas **SF data** sąskaitoje faktūroje bus tuščias, vartotojui bandant įrašyti SF, perkeltą iš sutarties, bus pateikta verslo proceso klaida.</span><span class="sxs-lookup"><span data-stu-id="c26cc-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c26cc-138">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="c26cc-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="c26cc-139">„Supply Chain Management“</span><span class="sxs-lookup"><span data-stu-id="c26cc-139">In Supply Chain Management</span></span>

<span data-ttu-id="c26cc-140">Kad būtų galima atskirti „Supply Chain Management“ laisvos formos SF, kurios buvo sukurtos remiantis „Field Service“ sutarties SF, integravime turi būti nustatyta SF kilmė.</span><span class="sxs-lookup"><span data-stu-id="c26cc-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="c26cc-141">Kai sąskaitos faktūros kilmė yra **Sutarties SF integravimas** tipo, laukas **Išorinis sąskaitos faktūros numeris** rodomas lauko **Pardavimo SF** antraštėje.</span><span class="sxs-lookup"><span data-stu-id="c26cc-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="c26cc-142">Lauko **Išorinis sąskaitos faktūros numeris** informacija, rodoma sąskaitos faktūros antraštėje, taip pat galima pasinaudoti, siekiant padėti užtikrinti, kad sąskaitos faktūros, kurios sukurtos remiantis „Field Service“ sutarčių SF, bus filtruojamos „Supply Chain Management“ sinchronizavimo su „Field Service“ metu.</span><span class="sxs-lookup"><span data-stu-id="c26cc-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="c26cc-143">Eikite į **Gautinos sumos** \> **Sąranka** \> **Sąskaitų faktūrų kilmės kodai**.</span><span class="sxs-lookup"><span data-stu-id="c26cc-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="c26cc-144">Norėdami sukurti naują sąskaitos faktūros kilmę, pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="c26cc-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="c26cc-145">Lauke **Sąskaitos faktūros kilmė** įveskite sąskaitos faktūros kilmės pavadinimą, pavyzdžiui, **FS**.</span><span class="sxs-lookup"><span data-stu-id="c26cc-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="c26cc-146">Lauke **Aprašas** įveskite aprašą, pvz., **„Field Service“ sutarties sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="c26cc-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="c26cc-147">Pasirinkite žymės langelį **Kilmės tipo priskyrimas**.</span><span class="sxs-lookup"><span data-stu-id="c26cc-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="c26cc-148">Nustatykite lauko **Sąskaitos faktūros kilmės tipas** reikšmę į **Sutarties sąskaitos faktūros integravimas**.</span><span class="sxs-lookup"><span data-stu-id="c26cc-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="c26cc-149">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="c26cc-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="c26cc-150">Duomenų integravimo projekte</span><span class="sxs-lookup"><span data-stu-id="c26cc-150">In the Data Integration project</span></span>

<span data-ttu-id="c26cc-151">Užduotis: **SF eilutės**</span><span class="sxs-lookup"><span data-stu-id="c26cc-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="c26cc-152">Įsitikinkite, kad numatytoji reikšmė „Supply Chain Management“ lauke **Pagrindinės sąskaitos rodoma reikšmė** yra atnaujinama, jog atitiktų norimą vertę.</span><span class="sxs-lookup"><span data-stu-id="c26cc-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="c26cc-153">Numatytoji šablono vertė yra **401100**.</span><span class="sxs-lookup"><span data-stu-id="c26cc-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c26cc-154">Šablono susiejimas naudojant funkcija Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="c26cc-154">Template mapping in Data integration</span></span>

<span data-ttu-id="c26cc-155">Toliau pateiktose iliustracijose vaizduojamas šablono susiejimas naudojant funkciją Duomenų integravimas.</span><span class="sxs-lookup"><span data-stu-id="c26cc-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="c26cc-156">Sutarties SF („Field Service“ su „Supply Chain Management“): SF antraštės</span><span class="sxs-lookup"><span data-stu-id="c26cc-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="c26cc-157">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="c26cc-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="c26cc-158">Sutarties SF („Field Service“ su „Supply Chain Management“): SF eilutės</span><span class="sxs-lookup"><span data-stu-id="c26cc-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="c26cc-159">[![Šablono susiejimas naudojant funkcija Duomenų integravimas](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="c26cc-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>
