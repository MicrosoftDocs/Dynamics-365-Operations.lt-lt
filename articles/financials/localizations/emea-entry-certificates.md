---
title: ES įrašų sertifikatai
description: Šiame straipsnyje pateikiama informacijos apie įvežimo į Europos Sąjungą (ES) sertifikatus.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b3346a5229d0cc9e7af74f17ea6a327e5ba253a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "371202"
---
# <a name="eu-entry-certificates"></a><span data-ttu-id="c9f92-103">Įvežimo į ES sertifikatai</span><span class="sxs-lookup"><span data-stu-id="c9f92-103">EU entry certificates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9f92-104">Šiame straipsnyje pateikiama informacijos apie įvežimo į Europos Sąjungą (ES) sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="c9f92-104">This article provides information about European Union (EU) entry certificates.</span></span>

<span data-ttu-id="c9f92-105">Galite atlikti toliau nurodytas užduotis, susijusias su Europos Sąjungos (ES) įrašo sertifikatu.</span><span class="sxs-lookup"><span data-stu-id="c9f92-105">You can complete the following tasks for a European Union (EU) entry certificate:</span></span>

-   <span data-ttu-id="c9f92-106">Kurti ir išduoti ES įrašo sertifikatą kartu su važtaraščiu arba kliento SF, susijusia su prekių tiekimu arba paslaugų teikimu ES šalyse / regionuose.</span><span class="sxs-lookup"><span data-stu-id="c9f92-106">Create and issue an EU entry certificate together with a packing slip or customer invoice for the delivery of items or services to EU countries/regions.</span></span>
-   <span data-ttu-id="c9f92-107">Gauti ES įrašo sertifikatą, kurį pasirašė ES klientas.</span><span class="sxs-lookup"><span data-stu-id="c9f92-107">Receive the EU entry certificate that is signed by an EU customer.</span></span>
-   <span data-ttu-id="c9f92-108">Nusiųsti pasirašytą ES įrašo sertifikatą, gautą iš kliento arba trečiosios šalies, atsakingos už prekių pristatymą klientui.</span><span class="sxs-lookup"><span data-stu-id="c9f92-108">Upload the signed EU entry certificate that is received either from the customer or from a third party who is responsible for delivering items to the customer.</span></span>
-   <span data-ttu-id="c9f92-109">Susieti nusiųstą ES įrašo sertifikatą su kliento SF.</span><span class="sxs-lookup"><span data-stu-id="c9f92-109">Associate the uploaded EU entry certificate with a customer invoice.</span></span>
-   <span data-ttu-id="c9f92-110">Atnaujinti nusiųsto ES įrašo sertifikato būseną.</span><span class="sxs-lookup"><span data-stu-id="c9f92-110">Update the status of the uploaded EU entry certificate.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c9f92-111">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="c9f92-111">Prerequisites</span></span>
<span data-ttu-id="c9f92-112">Pateiktoje lentelėje parodytos būtinosios sąlygos, kurias reikia įvykdyti prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="c9f92-112">The following table shows the prerequisites that must be in place before you start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9f92-113">Kategorija</span><span class="sxs-lookup"><span data-stu-id="c9f92-113">Category</span></span></th>
<th><span data-ttu-id="c9f92-114">Būtinoji sąlyga</span><span class="sxs-lookup"><span data-stu-id="c9f92-114">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9f92-115">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="c9f92-115">Country/region</span></span></td>
<td><span data-ttu-id="c9f92-116">Pagrindinis juridinio subjekto adresas turi būti ES valstybėje narėje.</span><span class="sxs-lookup"><span data-stu-id="c9f92-116">The primary address of the legal entity must be in a EU member state.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9f92-117">Susijusios nustatymo užduotys</span><span class="sxs-lookup"><span data-stu-id="c9f92-117">Related set up tasks</span></span></td>
<td><ul>
<li><span data-ttu-id="c9f92-118"><strong>Gautinų sumų parametrų</strong> puslapyje pasirinkite parinktis <strong>Įgalinti įrašų sertifikatų valdymą</strong> ir <strong>Įgalinti įrašų sertifikatų išdavimą</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9f92-118">On the <strong>Accounts receivable parameters</strong> page, select the <strong>Enable entry certificate management</strong> and <strong>Enable entry certificate issuing</strong> options.</span></span></li>
<li><span data-ttu-id="c9f92-119"><strong>Klientų</strong> puslapyje, <strong>SF ir pristatymo</strong> „FastTab‟ pasirinkite parinktį <strong>Įrašo sertifikatas būtinas</strong> , kad nurodytumėte, jog klientui būtinas ES įrašo sertifikatas.</span><span class="sxs-lookup"><span data-stu-id="c9f92-119">On the <strong>Customers</strong> page, on the <strong>Invoice and delivery</strong> FastTab, select the <strong>Entry certificate required</strong> option to indicate that an EU entry certificate is mandatory for the customer.</span></span> <span data-ttu-id="c9f92-120">Pasirinkite parinktį <strong>Išduoti įrašo sertifikatą</strong>, kad klientui išduotumėte juridinio subjekto ES įrašo sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="c9f92-120">Select the <strong>Issue entry certificate</strong> option to issue an EU entry certificate of the legal entity to the customer.</span></span></li>
<li><span data-ttu-id="c9f92-121"><strong>Gautinų sumų parametrų</strong> puslapyje pasirinkite <strong>Įrašo sertifikato</strong> nuorodos numeracijos kodą.</span><span class="sxs-lookup"><span data-stu-id="c9f92-121">On the <strong>Accounts receivable parameters</strong> page, select a number sequence code for the <strong>Entry certificate</strong> reference.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9f92-122">Susijusios operacijos</span><span class="sxs-lookup"><span data-stu-id="c9f92-122">Related transactions</span></span></td>
<td><ul>
<li><span data-ttu-id="c9f92-123">Kurkite kliento kodą.</span><span class="sxs-lookup"><span data-stu-id="c9f92-123">Create a customer account.</span></span></li>
<li><span data-ttu-id="c9f92-124">Sukurkite pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="c9f92-124">Create a sales order.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a><span data-ttu-id="c9f92-125">ES įrašo sertifikato kūrimas, registravimas ir įkėlimas</span><span class="sxs-lookup"><span data-stu-id="c9f92-125">Creating, registering, and uploading an EU entry certificate</span></span>
<span data-ttu-id="c9f92-126">Galite sukurti ES įrašo sertifikatą automatiškai arba rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="c9f92-126">You can create an EU entry certificate automatically or manually.</span></span> <span data-ttu-id="c9f92-127">ES įrašo sertifikatas sukuriamas ir užregistruojamas automatiškai, kai užregistruojate važtaraštį arba SF, skirtą klientui, naudodami puslapį **Važtaraščio registravimas** arba **SF registravimas**.</span><span class="sxs-lookup"><span data-stu-id="c9f92-127">An EU entry certificate is created and printed automatically when you post a packing slip or invoice for a customer by using the **Packing slip posting** page or the **Posting invoice** page.</span></span> <span data-ttu-id="c9f92-128">Norėdami kliento SF ES įrašo sertifikatą kurti arba perspausdinti neautomatiškai, naudokite puslapį **SF žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="c9f92-128">To manually create or reprint an EU entry certificate for a customer invoice, use the **Invoice journal** page.</span></span> <span data-ttu-id="c9f92-129">Be to, galite naudoti **Įrašų sertifikatų žurnalo** puslapį, kad įvestumėte informaciją apie trečiosios šalies išduotą ES įrašo sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="c9f92-129">Additionally, you can use the **Entry certificate journal** page to enter details about an EU entry certificate that is issued by a third party.</span></span>

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a><span data-ttu-id="c9f92-130">ES įrašo sertifikato kūrimas automatiškai arba rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="c9f92-130">Creating an EU entry certificate automatically or manually</span></span>

<span data-ttu-id="c9f92-131">Automatiškai sukurti ES įrašo sertifikatą galite naudodami važtaraštį **Visų pardavimo užsakymų** puslapyje arba naudodami SF  **Pardavimo užsakymo** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="c9f92-131">You can create an EU entry certificate automatically by using a packing slip on the **All sales orders** page or by using an invoice on the **Sales order** page.</span></span> <span data-ttu-id="c9f92-132">Norėdami ES įrašo sertifikatą sukurti rankiniu būdu, galite naudoti SF **SF žurnalo** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="c9f92-132">To manually create an EU entry certificate, you can use an invoice on the **Invoice journal** page.</span></span> <span data-ttu-id="c9f92-133">Tačiau prieš rankiniu būdu kurdami ES įrašo sertifikatą, turite pakeisti SF sertifikato būseną.</span><span class="sxs-lookup"><span data-stu-id="c9f92-133">However, you must change the certification status of the invoice before you manually create an EU entry certificate.</span></span>

### <a name="registering-an-eu-entry-certificate"></a><span data-ttu-id="c9f92-134">ES įrašo sertifikato registravimas</span><span class="sxs-lookup"><span data-stu-id="c9f92-134">Registering an EU entry certificate</span></span>

<span data-ttu-id="c9f92-135">Jei reikalingas registravimas, galite naudoti **Įrašų sertifikatų žurnalo** puslapį, kad registruotumėte trečiosios šalies išduotą ES įrašo sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="c9f92-135">If registration is required, you can use the **Entry certificate journal** page to register an EU entry certificate that is issued by a third party.</span></span>

### <a name="uploading-a-received-eu-entry-certificate"></a><span data-ttu-id="c9f92-136">Gauto ES įrašo sertifikato įkėlimas</span><span class="sxs-lookup"><span data-stu-id="c9f92-136">Uploading a received EU entry certificate</span></span>

<span data-ttu-id="c9f92-137">Naudodami puslapį **Priedai** galite įkelti gautą ES įrašo sertifikatą, kurį pasirašė ES klientas.</span><span class="sxs-lookup"><span data-stu-id="c9f92-137">Use the **Attachments** page to upload a received EU entry certificate that is signed by an EU customer.</span></span> <span data-ttu-id="c9f92-138">Įkėlę sertifikatą, jį galite susieti su SF kaip įrodymą, kad prekės buvo pristatytos.</span><span class="sxs-lookup"><span data-stu-id="c9f92-138">After the certificate is uploaded, you can associate it with an invoice as proof that the items were delivered.</span></span> <span data-ttu-id="c9f92-139">Šio įrodymo reikia, jei turite išduoti SF, kurioje nėra pridėtinės vertės mokesčio (PVM), ir jis taip pat naudojamas atliekant auditą.</span><span class="sxs-lookup"><span data-stu-id="c9f92-139">This proof is required if you must issue an invoice that doesn't include value-added tax (VAT), and it's also used during auditing.</span></span>

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a><span data-ttu-id="c9f92-140">Neprivaloma: sertifikato būsenos ir SF spausdinimo būsenos naujinimas</span><span class="sxs-lookup"><span data-stu-id="c9f92-140">Optional: Updating the certification status and printing status of an invoice</span></span>

<span data-ttu-id="c9f92-141">Atnaujinti įrašo sertifikato būseną ir kliento SF spausdinimo būseną galite naudodami **SF žurnalo** puslapį.</span><span class="sxs-lookup"><span data-stu-id="c9f92-141">You can update the entry certification status and printing status of a customer invoice by using the **Invoice journal** page.</span></span>

## <a name="technical-information-for-system-administrators"></a><span data-ttu-id="c9f92-142">Techninė informacija sistemos administratoriams</span><span class="sxs-lookup"><span data-stu-id="c9f92-142">Technical information for system administrators</span></span>
<span data-ttu-id="c9f92-143">Jei neturite prieigos prie puslapių, kurie naudojami užduočiai atlikti, kreipkitės į sistemos administratorių ir pateikite informaciją, kuri yra rodoma toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="c9f92-143">If you don't have access to the pages that are used to complete this task, contact your system administrator, and provide the information that is shown in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9f92-144">Kategorija</span><span class="sxs-lookup"><span data-stu-id="c9f92-144">Category</span></span></th>
<th><span data-ttu-id="c9f92-145">Būtinoji sąlyga</span><span class="sxs-lookup"><span data-stu-id="c9f92-145">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9f92-146">Saugos vaidmenys ir pareigos</span><span class="sxs-lookup"><span data-stu-id="c9f92-146">Security roles and duties</span></span></td>
<td><span data-ttu-id="c9f92-147">Norėdami nustatyti ir sukurti ES įrašų sertifikatus, skirtus prekėms arba paslaugoms, jums turi būti priskirtas saugos vaidmuo, kuris paprastai priklauso šioms pareigybėms:</span><span class="sxs-lookup"><span data-stu-id="c9f92-147">To set up and create EU entry certificates for items or services, you must be a member of a security role that includes the following duties:</span></span>
<ul>
<li><span data-ttu-id="c9f92-148"><strong>Gautinų sumų klerkas</strong> (CustInvoiceAccountsReceivableClerk)</span><span class="sxs-lookup"><span data-stu-id="c9f92-148"><strong>Accounts receivable clerk</strong> (CustInvoiceAccountsReceivableClerk)</span></span></li>
<li><span data-ttu-id="c9f92-149"><strong>Klientų aptarnavimo atstovas</strong> (TradeCustomerServiceRepresentative)</span><span class="sxs-lookup"><span data-stu-id="c9f92-149"><strong>Customer service representative</strong> (TradeCustomerServiceRepresentative)</span></span></li>
<li><span data-ttu-id="c9f92-150"><strong>Pardavimo klerkas</strong> (TradeSalesClerk)</span><span class="sxs-lookup"><span data-stu-id="c9f92-150"><strong>Sales clerk</strong> (TradeSalesClerk)</span></span></li>
<li><span data-ttu-id="c9f92-151"><strong>Siuntimo klerkas</strong> (InventShippingClerk)</span><span class="sxs-lookup"><span data-stu-id="c9f92-151"><strong>Shipping clerk</strong> (InventShippingClerk)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>





