---
title: "Tiekėjo bendradarbiavimo SF išrašymo darbo srities peržiūra"
description: "Šioje temoje paaiškinama, kaip galite peržiūrėti tiekėjo sąskaitas faktūras ir pateikti sąskaitas faktūras iš tiekėjo bendradarbiavimo SF išrašymo darbo srities."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 6b05dbef279b06fefc1eccd87689693edf2a418e
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="248f3-103">Tiekėjo bendradarbiavimo SF išrašymo darbo srities peržiūra</span><span class="sxs-lookup"><span data-stu-id="248f3-103">Vendor collaboration invoicing workspace</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="248f3-104">Šioje temoje paaiškinama, kaip galite peržiūrėti tiekėjo sąskaitas faktūras ir pateikti sąskaitas faktūras iš tiekėjo bendradarbiavimo SF išrašymo darbo srities.</span><span class="sxs-lookup"><span data-stu-id="248f3-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="248f3-105">**Tiekėjų bendradarbiavimo SF išrašymo** darbo sritį galima naudoti norint peržiūrėti tiekėjo SF informaciją ir pateikti SF programai „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimas, naudojantis darbo eigos galimybėmis.</span><span class="sxs-lookup"><span data-stu-id="248f3-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="248f3-106">Tiekėjo bendradarbiavimo SF išrašymo darbo sritis</span><span class="sxs-lookup"><span data-stu-id="248f3-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="248f3-107">Suvestinės išklotinės</span><span class="sxs-lookup"><span data-stu-id="248f3-107">Summary tiles</span></span>

<span data-ttu-id="248f3-108">Išklotinėse **Suvestinė** pateikiama pasirinkto tiekėjo sąskaitų faktūrų apžvalga.</span><span class="sxs-lookup"><span data-stu-id="248f3-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="248f3-109">Sąskaitas faktūras galite peržiūrėti pagal jų būseną.</span><span class="sxs-lookup"><span data-stu-id="248f3-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="248f3-110">Sąskaitų faktūrų juodraščiai darbo eigai nepateikti.</span><span class="sxs-lookup"><span data-stu-id="248f3-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="248f3-111">Pateiktos, bet nepatvirtintos SF yra tiekėjo pateiktos SF, kurios dar neužregistruotos „Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="248f3-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in Finance and Operations.</span></span>
-   <span data-ttu-id="248f3-112">Patvirtintos, bet neapmokėtos SF yra „Finance and Operations“ užregistruotos SF, kurios dar nėra visiškai apmokėtos.</span><span class="sxs-lookup"><span data-stu-id="248f3-112">Approved, not paid invoices are those that have been posted in Finance and Operations, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="248f3-113">Apmokėtos SF yra visiškai apmokėtos „Finance and Operations“ SF.</span><span class="sxs-lookup"><span data-stu-id="248f3-113">Paid invoices are those that have been fully paid in Finance and Operations.</span></span>

<span data-ttu-id="248f3-114">Spustelėjus išklotinę atveriamas filtruotas puslapio **Sąskaitų faktūrų sąrašas** rodinys.</span><span class="sxs-lookup"><span data-stu-id="248f3-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>
### <a name="tabular-lists"></a><span data-ttu-id="248f3-115">Sąrašų lentelės</span><span class="sxs-lookup"><span data-stu-id="248f3-115">Tabular lists</span></span>

<span data-ttu-id="248f3-116">Skyriuje **Sąrašų lentelės** sąskaitos faktūros būsena suskirstoma į panašias dalis kaip ir suvestinės išklotinės: juodraščiai ir pateikti, nepatvirtinti sąrašai.</span><span class="sxs-lookup"><span data-stu-id="248f3-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="248f3-117">Jeigu būsena Juodraštis, sąskaitą faktūrą galima pateikti darbo eigai arba panaikinti.</span><span class="sxs-lookup"><span data-stu-id="248f3-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="248f3-118">Paskutinė sąrašų lentelė naudojama SF surasti.</span><span class="sxs-lookup"><span data-stu-id="248f3-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="248f3-119">Ieškodami galite išfiltruoti ir greičiau surasti.</span><span class="sxs-lookup"><span data-stu-id="248f3-119">You can filter as you search, to allow for faster searches.</span></span>
<span data-ttu-id="248f3-120">Visų tiekėjo SF sąrašo puslapis</span><span class="sxs-lookup"><span data-stu-id="248f3-120">All vendor invoices list page</span></span>
-----------------------------

<span data-ttu-id="248f3-121">Sąrašo puslapyje **Tiekėjo bendradarbiavimo SF** galite peržiūrėti visas užregistruotas ir neužregistruotas tiekėjo sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="248f3-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="248f3-122">Naudodami šį sąrašo puslapį galite peržiūrėti sąskaitų faktūrų mokėjimo būseną.</span><span class="sxs-lookup"><span data-stu-id="248f3-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="248f3-123">Apmokėjimo būsenos yra šios: neužregistruota, neapmokėta, apmokėta iš dalies, visiškai apmokėta.</span><span class="sxs-lookup"><span data-stu-id="248f3-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="248f3-124">Naujos tiekėjo SF kūrimas naudojant pirkimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="248f3-124">Creating a new invoice from a purchase order</span></span>
--------------------------------------------

<span data-ttu-id="248f3-125">Naują tiekėjo sąskaitą faktūrą galite sukurti pažymėdami darbo srities **Tiekėjo bendradarbiavimo SF išrašymas** veiksmą **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="248f3-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="248f3-126">Pirkimo užsakymo numerį ir sąskaitos faktūros numerį privalo pateikti tiekėjas.</span><span class="sxs-lookup"><span data-stu-id="248f3-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="248f3-127">Pagal numatytąjį nustatymą visos tiekėjo pirkimo užsakymo eilutės rodomos naujoje SF.</span><span class="sxs-lookup"><span data-stu-id="248f3-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="248f3-128">Kiekio ir kainos informaciją galima redaguoti prieš pateikiant tiekėjo SF darbo eigai.</span><span class="sxs-lookup"><span data-stu-id="248f3-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="248f3-129">Prieš pateikdami SF prie jos galite pridėti failų, pastabų, vaizdų ir URL.</span><span class="sxs-lookup"><span data-stu-id="248f3-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>



<span data-ttu-id="248f3-130">Jei reikia daugiau informacijos, žr. temą [Bendradarbiavimas su tiekėjais naudojant tiekėjų portalą](../../supply-chain/procurement/collaborate-vendors-vendor-portal.md)</span><span class="sxs-lookup"><span data-stu-id="248f3-130">For more information, see [Collaborating with vendors by using the Vendor portal](../../supply-chain/procurement/collaborate-vendors-vendor-portal.md)</span></span>




