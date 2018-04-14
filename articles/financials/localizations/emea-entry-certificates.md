---
title: "ES įrašų sertifikatai"
description: "Šiame straipsnyje pateikiama informacijos apie įvežimo į Europos Sąjungą (ES) sertifikatus."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0919cdeb54b0dade68a9caba89b172c0663381da
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="eu-entry-certificates"></a><span data-ttu-id="9d32c-103">Įvežimo į ES sertifikatai</span><span class="sxs-lookup"><span data-stu-id="9d32c-103">EU entry certificates</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="9d32c-104">Šiame straipsnyje pateikiama informacijos apie įvežimo į Europos Sąjungą (ES) sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="9d32c-104">This article provides information about European Union (EU) entry certificates.</span></span>

<span data-ttu-id="9d32c-105">Galite atlikti toliau nurodytas užduotis, susijusias su Europos Sąjungos (ES) įrašo sertifikatu.</span><span class="sxs-lookup"><span data-stu-id="9d32c-105">You can complete the following tasks for a European Union (EU) entry certificate:</span></span>

-   <span data-ttu-id="9d32c-106">Kurti ir išduoti ES įrašo sertifikatą kartu su važtaraščiu arba kliento SF, susijusia su prekių tiekimu arba paslaugų teikimu ES šalyse / regionuose.</span><span class="sxs-lookup"><span data-stu-id="9d32c-106">Create and issue an EU entry certificate together with a packing slip or customer invoice for the delivery of items or services to EU countries/regions.</span></span>
-   <span data-ttu-id="9d32c-107">Gauti ES įrašo sertifikatą, kurį pasirašė ES klientas.</span><span class="sxs-lookup"><span data-stu-id="9d32c-107">Receive the EU entry certificate that is signed by an EU customer.</span></span>
-   <span data-ttu-id="9d32c-108">Nusiųsti pasirašytą ES įrašo sertifikatą, gautą iš kliento arba trečiosios šalies, atsakingos už prekių pristatymą klientui.</span><span class="sxs-lookup"><span data-stu-id="9d32c-108">Upload the signed EU entry certificate that is received either from the customer or from a third party who is responsible for delivering items to the customer.</span></span>
-   <span data-ttu-id="9d32c-109">Susieti nusiųstą ES įrašo sertifikatą su kliento SF.</span><span class="sxs-lookup"><span data-stu-id="9d32c-109">Associate the uploaded EU entry certificate with a customer invoice.</span></span>
-   <span data-ttu-id="9d32c-110">Atnaujinti nusiųsto ES įrašo sertifikato būseną.</span><span class="sxs-lookup"><span data-stu-id="9d32c-110">Update the status of the uploaded EU entry certificate.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9d32c-111">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="9d32c-111">Prerequisites</span></span>
<span data-ttu-id="9d32c-112">Pateiktoje lentelėje parodytos būtinosios sąlygos, kurias reikia įvykdyti prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="9d32c-112">The following table shows the prerequisites that must be in place before you start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d32c-113">Kategorija</span><span class="sxs-lookup"><span data-stu-id="9d32c-113">Category</span></span></th>
<th><span data-ttu-id="9d32c-114">Būtinoji sąlyga</span><span class="sxs-lookup"><span data-stu-id="9d32c-114">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d32c-115">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="9d32c-115">Country/region</span></span></td>
<td><span data-ttu-id="9d32c-116">Pagrindinis juridinio subjekto adresas turi būti ES valstybėje narėje.</span><span class="sxs-lookup"><span data-stu-id="9d32c-116">The primary address of the legal entity must be in a EU member state.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9d32c-117">Susijusios nustatymo užduotys</span><span class="sxs-lookup"><span data-stu-id="9d32c-117">Related set up tasks</span></span></td>
<td><ul>
<li><span data-ttu-id="9d32c-118"><strong>Gautinų sumų parametrų</strong> puslapyje pasirinkite parinktis <strong>Įgalinti įrašų sertifikatų valdymą</strong> ir <strong>Įgalinti įrašų sertifikatų išdavimą</strong>.</span><span class="sxs-lookup"><span data-stu-id="9d32c-118">On the <strong>Accounts receivable parameters</strong> page, select the <strong>Enable entry certificate management</strong> and <strong>Enable entry certificate issuing</strong> options.</span></span></li>
<li><span data-ttu-id="9d32c-119"><strong>Klientų</strong> puslapyje, <strong>SF ir pristatymo</strong> „FastTab‟ pasirinkite parinktį <strong>Įrašo sertifikatas būtinas</strong> , kad nurodytumėte, jog klientui būtinas ES įrašo sertifikatas.</span><span class="sxs-lookup"><span data-stu-id="9d32c-119">On the <strong>Customers</strong> page, on the <strong>Invoice and delivery</strong> FastTab, select the <strong>Entry certificate required</strong> option to indicate that an EU entry certificate is mandatory for the customer.</span></span> <span data-ttu-id="9d32c-120">Pasirinkite parinktį <strong>Išduoti įrašo sertifikatą</strong>, kad klientui išduotumėte juridinio subjekto ES įrašo sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="9d32c-120">Select the <strong>Issue entry certificate</strong> option to issue an EU entry certificate of the legal entity to the customer.</span></span></li>
<li><span data-ttu-id="9d32c-121"><strong>Gautinų sumų parametrų</strong> puslapyje pasirinkite <strong>Įrašo sertifikato</strong> nuorodos numeracijos kodą.</span><span class="sxs-lookup"><span data-stu-id="9d32c-121">On the <strong>Accounts receivable parameters</strong> page, select a number sequence code for the <strong>Entry certificate</strong> reference.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9d32c-122">Susijusios operacijos</span><span class="sxs-lookup"><span data-stu-id="9d32c-122">Related transactions</span></span></td>
<td><ul>
<li><span data-ttu-id="9d32c-123">Kurkite kliento kodą.</span><span class="sxs-lookup"><span data-stu-id="9d32c-123">Create a customer account.</span></span></li>
<li><span data-ttu-id="9d32c-124">Sukurkite pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="9d32c-124">Create a sales order.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a><span data-ttu-id="9d32c-125">ES įrašo sertifikato kūrimas, registravimas ir įkėlimas</span><span class="sxs-lookup"><span data-stu-id="9d32c-125">Creating, registering, and uploading an EU entry certificate</span></span>
<span data-ttu-id="9d32c-126">Galite sukurti ES įrašo sertifikatą automatiškai arba rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="9d32c-126">You can create an EU entry certificate automatically or manually.</span></span> <span data-ttu-id="9d32c-127">ES įrašo sertifikatas sukuriamas ir užregistruojamas automatiškai, kai užregistruojate važtaraštį arba SF, skirtą klientui, naudodami puslapį **Važtaraščio registravimas** arba **SF registravimas**.</span><span class="sxs-lookup"><span data-stu-id="9d32c-127">An EU entry certificate is created and printed automatically when you post a packing slip or invoice for a customer by using the **Packing slip posting** page or the **Posting invoice** page.</span></span> <span data-ttu-id="9d32c-128">Norėdami kliento SF ES įrašo sertifikatą kurti arba perspausdinti neautomatiškai, naudokite puslapį **SF žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="9d32c-128">To manually create or reprint an EU entry certificate for a customer invoice, use the **Invoice journal** page.</span></span> <span data-ttu-id="9d32c-129">Be to, galite naudoti **Įrašų sertifikatų žurnalo** puslapį, kad įvestumėte informaciją apie trečiosios šalies išduotą ES įrašo sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="9d32c-129">Additionally, you can use the **Entry certificate journal** page to enter details about an EU entry certificate that is issued by a third party.</span></span>

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a><span data-ttu-id="9d32c-130">ES įrašo sertifikato kūrimas automatiškai arba rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="9d32c-130">Creating an EU entry certificate automatically or manually</span></span>

<span data-ttu-id="9d32c-131">Automatiškai sukurti ES įrašo sertifikatą galite naudodami važtaraštį **Visų pardavimo užsakymų** puslapyje arba naudodami SF  **Pardavimo užsakymo** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9d32c-131">You can create an EU entry certificate automatically by using a packing slip on the **All sales orders** page or by using an invoice on the **Sales order** page.</span></span> <span data-ttu-id="9d32c-132">Norėdami ES įrašo sertifikatą sukurti rankiniu būdu, galite naudoti SF **SF žurnalo** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9d32c-132">To manually create an EU entry certificate, you can use an invoice on the **Invoice journal** page.</span></span> <span data-ttu-id="9d32c-133">Tačiau prieš rankiniu būdu kurdami ES įrašo sertifikatą, turite pakeisti SF sertifikato būseną.</span><span class="sxs-lookup"><span data-stu-id="9d32c-133">However, you must change the certification status of the invoice before you manually create an EU entry certificate.</span></span>

### <a name="registering-an-eu-entry-certificate"></a><span data-ttu-id="9d32c-134">ES įrašo sertifikato registravimas</span><span class="sxs-lookup"><span data-stu-id="9d32c-134">Registering an EU entry certificate</span></span>

<span data-ttu-id="9d32c-135">Jei reikalingas registravimas, galite naudoti **Įrašų sertifikatų žurnalo** puslapį, kad registruotumėte trečiosios šalies išduotą ES įrašo sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="9d32c-135">If registration is required, you can use the **Entry certificate journal** page to register an EU entry certificate that is issued by a third party.</span></span>

### <a name="uploading-a-received-eu-entry-certificate"></a><span data-ttu-id="9d32c-136">Gauto ES įrašo sertifikato įkėlimas</span><span class="sxs-lookup"><span data-stu-id="9d32c-136">Uploading a received EU entry certificate</span></span>

<span data-ttu-id="9d32c-137">Naudodami puslapį **Priedai** galite įkelti gautą ES įrašo sertifikatą, kurį pasirašė ES klientas.</span><span class="sxs-lookup"><span data-stu-id="9d32c-137">Use the **Attachments** page to upload a received EU entry certificate that is signed by an EU customer.</span></span> <span data-ttu-id="9d32c-138">Įkėlę sertifikatą, jį galite susieti su SF kaip įrodymą, kad prekės buvo pristatytos.</span><span class="sxs-lookup"><span data-stu-id="9d32c-138">After the certificate is uploaded, you can associate it with an invoice as proof that the items were delivered.</span></span> <span data-ttu-id="9d32c-139">Šio įrodymo reikia, jei turite išduoti SF, kurioje nėra pridėtinės vertės mokesčio (PVM), ir jis taip pat naudojamas atliekant auditą.</span><span class="sxs-lookup"><span data-stu-id="9d32c-139">This proof is required if you must issue an invoice that doesn't include value-added tax (VAT), and it's also used during auditing.</span></span>

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a><span data-ttu-id="9d32c-140">Neprivaloma: sertifikato būsenos ir SF spausdinimo būsenos naujinimas</span><span class="sxs-lookup"><span data-stu-id="9d32c-140">Optional: Updating the certification status and printing status of an invoice</span></span>

<span data-ttu-id="9d32c-141">Atnaujinti įrašo sertifikato būseną ir kliento SF spausdinimo būseną galite naudodami **SF žurnalo** puslapį.</span><span class="sxs-lookup"><span data-stu-id="9d32c-141">You can update the entry certification status and printing status of a customer invoice by using the **Invoice journal** page.</span></span>

## <a name="technical-information-for-system-administrators"></a><span data-ttu-id="9d32c-142">Techninė informacija sistemos administratoriams</span><span class="sxs-lookup"><span data-stu-id="9d32c-142">Technical information for system administrators</span></span>
<span data-ttu-id="9d32c-143">Jei neturite prieigos prie puslapių, kurie naudojami užduočiai atlikti, kreipkitės į sistemos administratorių ir pateikite informaciją, kuri yra rodoma toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="9d32c-143">If you don't have access to the pages that are used to complete this task, contact your system administrator, and provide the information that is shown in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d32c-144">Kategorija</span><span class="sxs-lookup"><span data-stu-id="9d32c-144">Category</span></span></th>
<th><span data-ttu-id="9d32c-145">Būtinoji sąlyga</span><span class="sxs-lookup"><span data-stu-id="9d32c-145">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9d32c-146">Saugos vaidmenys ir pareigos</span><span class="sxs-lookup"><span data-stu-id="9d32c-146">Security roles and duties</span></span></td>
<td><span data-ttu-id="9d32c-147">Norėdami nustatyti ir sukurti ES įrašų sertifikatus, skirtus prekėms arba paslaugoms, jums turi būti priskirtas saugos vaidmuo, kuris paprastai priklauso šioms pareigybėms:</span><span class="sxs-lookup"><span data-stu-id="9d32c-147">To set up and create EU entry certificates for items or services, you must be a member of a security role that includes the following duties:</span></span>
<ul>
<li><span data-ttu-id="9d32c-148"><strong>Gautinų sumų klerkas</strong> (CustInvoiceAccountsReceivableClerk)</span><span class="sxs-lookup"><span data-stu-id="9d32c-148"><strong>Accounts receivable clerk</strong> (CustInvoiceAccountsReceivableClerk)</span></span></li>
<li><span data-ttu-id="9d32c-149"><strong>Klientų aptarnavimo atstovas</strong> (TradeCustomerServiceRepresentative)</span><span class="sxs-lookup"><span data-stu-id="9d32c-149"><strong>Customer service representative</strong> (TradeCustomerServiceRepresentative)</span></span></li>
<li><span data-ttu-id="9d32c-150"><strong>Pardavimo klerkas</strong> (TradeSalesClerk)</span><span class="sxs-lookup"><span data-stu-id="9d32c-150"><strong>Sales clerk</strong> (TradeSalesClerk)</span></span></li>
<li><span data-ttu-id="9d32c-151"><strong>Siuntimo klerkas</strong> (InventShippingClerk)</span><span class="sxs-lookup"><span data-stu-id="9d32c-151"><strong>Shipping clerk</strong> (InventShippingClerk)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






