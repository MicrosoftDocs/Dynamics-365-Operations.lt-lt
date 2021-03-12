---
title: Tiekėjo bendradarbiavimo SF išrašymo darbo srities peržiūra
description: Šioje temoje paaiškinama, kaip galite peržiūrėti tiekėjo sąskaitas faktūras ir pateikti sąskaitas faktūras iš tiekėjo bendradarbiavimo SF išrašymo darbo srities.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 30e9012845838a4d1df5f1308740b356a64433e9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993168"
---
# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="7d445-103">Tiekėjo bendradarbiavimo SF išrašymo darbo srities peržiūra</span><span class="sxs-lookup"><span data-stu-id="7d445-103">Vendor collaboration invoicing workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d445-104">Šioje temoje paaiškinama, kaip galite peržiūrėti tiekėjo sąskaitas faktūras ir pateikti sąskaitas faktūras iš tiekėjo bendradarbiavimo SF išrašymo darbo srities.</span><span class="sxs-lookup"><span data-stu-id="7d445-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="7d445-105">Darbo sritį **Tiekėjo bendradarbiavimo SF išrašymas** galima naudoti norint peržiūrėti tiekėjo sąskaitos faktūros informaciją ir pateikti sąskaitas faktūras sistemai naudojantis darbo srities galimybėmis.</span><span class="sxs-lookup"><span data-stu-id="7d445-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to the system using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="7d445-106">Tiekėjo bendradarbiavimo SF išrašymo darbo sritis</span><span class="sxs-lookup"><span data-stu-id="7d445-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="7d445-107">Suvestinės išklotinės</span><span class="sxs-lookup"><span data-stu-id="7d445-107">Summary tiles</span></span>

<span data-ttu-id="7d445-108">Išklotinėse **Suvestinė** pateikiama pasirinkto tiekėjo sąskaitų faktūrų apžvalga.</span><span class="sxs-lookup"><span data-stu-id="7d445-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="7d445-109">Sąskaitas faktūras galite peržiūrėti pagal jų būseną.</span><span class="sxs-lookup"><span data-stu-id="7d445-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="7d445-110">Sąskaitų faktūrų juodraščiai darbo eigai nepateikti.</span><span class="sxs-lookup"><span data-stu-id="7d445-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="7d445-111">Pateiktos, bet nepatvirtintos SF yra tiekėjo pateiktos SF, kurios dar neužregistruotos programoje.</span><span class="sxs-lookup"><span data-stu-id="7d445-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in the application.</span></span>
-   <span data-ttu-id="7d445-112">Patvirtintos, bet neapmokėtos, SF yra užregistruotos SF, kurios dar nėra visiškai apmokėtos.</span><span class="sxs-lookup"><span data-stu-id="7d445-112">Approved, not paid invoices are those that have been posted, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="7d445-113">Apmokėtos SF yra programoje visiškai apmokėtos SF.</span><span class="sxs-lookup"><span data-stu-id="7d445-113">Paid invoices are those that have been fully paid in the application.</span></span>

<span data-ttu-id="7d445-114">Spustelėjus išklotinę atveriamas filtruotas puslapio **Sąskaitų faktūrų sąrašas** rodinys.</span><span class="sxs-lookup"><span data-stu-id="7d445-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>

### <a name="tabular-lists"></a><span data-ttu-id="7d445-115">Sąrašų lentelės</span><span class="sxs-lookup"><span data-stu-id="7d445-115">Tabular lists</span></span>

<span data-ttu-id="7d445-116">Skyriuje **Sąrašų lentelės** sąskaitos faktūros būsena suskirstoma į panašias dalis kaip ir suvestinės išklotinės: juodraščiai ir pateikti, nepatvirtinti sąrašai.</span><span class="sxs-lookup"><span data-stu-id="7d445-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="7d445-117">Jeigu būsena Juodraštis, sąskaitą faktūrą galima pateikti darbo eigai arba panaikinti.</span><span class="sxs-lookup"><span data-stu-id="7d445-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="7d445-118">Paskutinė sąrašų lentelė naudojama SF surasti.</span><span class="sxs-lookup"><span data-stu-id="7d445-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="7d445-119">Ieškodami galite išfiltruoti ir greičiau surasti.</span><span class="sxs-lookup"><span data-stu-id="7d445-119">You can filter as you search, to allow for faster searches.</span></span>

### <a name="all-vendor-invoices-list-page"></a><span data-ttu-id="7d445-120">Visų tiekėjo SF sąrašo puslapis</span><span class="sxs-lookup"><span data-stu-id="7d445-120">All vendor invoices list page</span></span>

<span data-ttu-id="7d445-121">Sąrašo puslapyje **Tiekėjo bendradarbiavimo SF** galite peržiūrėti visas užregistruotas ir neužregistruotas tiekėjo sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="7d445-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="7d445-122">Naudodami šį sąrašo puslapį galite peržiūrėti sąskaitų faktūrų mokėjimo būseną.</span><span class="sxs-lookup"><span data-stu-id="7d445-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="7d445-123">Apmokėjimo būsenos yra šios: neužregistruota, neapmokėta, apmokėta iš dalies, visiškai apmokėta.</span><span class="sxs-lookup"><span data-stu-id="7d445-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="7d445-124">Naujos tiekėjo SF kūrimas naudojant pirkimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="7d445-124">Creating a new invoice from a purchase order</span></span>

<span data-ttu-id="7d445-125">Naują tiekėjo sąskaitą faktūrą galite sukurti pažymėdami darbo srities **Tiekėjo bendradarbiavimo SF išrašymas** veiksmą **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="7d445-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="7d445-126">Pirkimo užsakymo numerį ir sąskaitos faktūros numerį privalo pateikti tiekėjas.</span><span class="sxs-lookup"><span data-stu-id="7d445-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="7d445-127">Pagal numatytąjį nustatymą visos tiekėjo pirkimo užsakymo eilutės rodomos naujoje SF.</span><span class="sxs-lookup"><span data-stu-id="7d445-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="7d445-128">Kiekio ir kainos informaciją galima redaguoti prieš pateikiant tiekėjo SF darbo eigai.</span><span class="sxs-lookup"><span data-stu-id="7d445-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="7d445-129">Prieš pateikdami SF prie jos galite pridėti failų, pastabų, vaizdų ir URL.</span><span class="sxs-lookup"><span data-stu-id="7d445-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>

<span data-ttu-id="7d445-130">Jei reikia daugiau informacijos, žr. temą [Tiekėjų bendradarbiavimas su išoriniais tiekėjais](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span><span class="sxs-lookup"><span data-stu-id="7d445-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>



