---
title: " Skambučių centro užsakymų kūrimas"
description: Ši procedūra padeda ieškoti kliento, kurti naują užsakymą, ieškoti produkto ir surinkti mokėjimą iš kliento.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4867ad67dc570ab42420ba12fc7dc2da6b5ba503
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "334317"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="d789f-103"> Skambučių centro užsakymų kūrimas</span><span class="sxs-lookup"><span data-stu-id="d789f-103">Create call center orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d789f-104">Ši procedūra padeda ieškoti kliento, kurti naują užsakymą, ieškoti produkto ir surinkti mokėjimą iš kliento.</span><span class="sxs-lookup"><span data-stu-id="d789f-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="d789f-105">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT ir ji yra skirta pardavimo užsakymo klerkui.</span><span class="sxs-lookup"><span data-stu-id="d789f-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="d789f-106">Išankstinės sąlygos: vartotojas, vykdantis procedūrą, yra nustatomas kaip skambučių centro vartotojas ir skelbiamas Fabrikam pusės metų katalogas su bent vienu šaltinio kodu jame.</span><span class="sxs-lookup"><span data-stu-id="d789f-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="d789f-107">Pasirinkite Mažmeninė prekyba ir prekyba > Klientai > Klientų aptarnavimas.</span><span class="sxs-lookup"><span data-stu-id="d789f-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="d789f-108">Lauke Ieškos tekstas įveskite kliento ieškos kriterijus.</span><span class="sxs-lookup"><span data-stu-id="d789f-108">In the SearchText field, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="d789f-109">Atlikdami šio pavyzdžio procedūrą įveskite „karen“ ir paspauskite skirtuką.</span><span class="sxs-lookup"><span data-stu-id="d789f-109">For this example procedure type in 'karen' and press tab.</span></span>  
3. <span data-ttu-id="d789f-110">Spustelėkite Ieškoti.</span><span class="sxs-lookup"><span data-stu-id="d789f-110">Click Search.</span></span>
    * <span data-ttu-id="d789f-111">Kadangi demonstraciniuose duomenyse tik yra tik vienas klientas vardu Karen, jis bus automatiškai pažymėtas.</span><span class="sxs-lookup"><span data-stu-id="d789f-111">Since there is only one customer named Karen in demo data they will be automatically selected.</span></span>  
4. <span data-ttu-id="d789f-112">Spustelėkite Naujas pardavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="d789f-112">Click New sales order.</span></span>
5. <span data-ttu-id="d789f-113">Išplėskite arba sutraukite sekciją Pardavimo užsakymo antraštė.</span><span class="sxs-lookup"><span data-stu-id="d789f-113">Expand or collapse the Sales order header section.</span></span>
6. <span data-ttu-id="d789f-114">Pasirinkite katalogo šaltinio kodą.</span><span class="sxs-lookup"><span data-stu-id="d789f-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="d789f-115">Jei nėra jokių aktyvių šaltinio kodų, galite uždaryti lauką Šaltinis ir praleisti šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="d789f-115">If there are no active Source codes you can close the Source field and skip this step.</span></span>  
7. <span data-ttu-id="d789f-116">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="d789f-116">Click Add line.</span></span>
8. <span data-ttu-id="d789f-117">Lauke Prekės numeris įveskite prekės ieškos terminą.</span><span class="sxs-lookup"><span data-stu-id="d789f-117">In the Item number field, enter the item search term.</span></span>
    * <span data-ttu-id="d789f-118">Atlikdami šio pavyzdžio procedūrą, įveskite dalinį prekės numerį „8111“ ir paspauskite skirtuką. Pasirodys prekės ieškos langas.</span><span class="sxs-lookup"><span data-stu-id="d789f-118">For this sample procedure enter a partial item number of '8111' and press tab. This will pop up the item search window.</span></span>  
9. <span data-ttu-id="d789f-119">Pasirinkti produktą įtraukti į pardavimo užsakymą</span><span class="sxs-lookup"><span data-stu-id="d789f-119">Select the product to add to the sales order</span></span>
10. <span data-ttu-id="d789f-120">Įveskite pardavimo kiekį.</span><span class="sxs-lookup"><span data-stu-id="d789f-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="d789f-121">Spustelėkite Kurti.</span><span class="sxs-lookup"><span data-stu-id="d789f-121">Click Create.</span></span>
12. <span data-ttu-id="d789f-122">Spustelėkite Baigti, kad užfiksuotumėte kliento mokėjimą.</span><span class="sxs-lookup"><span data-stu-id="d789f-122">Click Complete to capture the customer payment.</span></span>
13. <span data-ttu-id="d789f-123">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="d789f-123">Click Add.</span></span>
    * <span data-ttu-id="d789f-124">Parinktis Įtraukti saitą yra skirtuke Mokėjimai. Išplėskite skirtuką Mokėjimai, jei jis sutrauktas.</span><span class="sxs-lookup"><span data-stu-id="d789f-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="d789f-125">Pasirinkite mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="d789f-125">Select the payment method.</span></span>
    * <span data-ttu-id="d789f-126">Atlikdami šią procedūrą, parinkite grynųjų pinigų mokėjimo metodą.</span><span class="sxs-lookup"><span data-stu-id="d789f-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="d789f-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d789f-127">Close the page.</span></span>
16. <span data-ttu-id="d789f-128">Įveskite sumą.</span><span class="sxs-lookup"><span data-stu-id="d789f-128">Enter the amount.</span></span>
    * <span data-ttu-id="d789f-129">Atlikdami šią procedūrą, įveskite sumą, lygią užsakymo balansui, kuris rodomas puslapyje Pardavimo užsakymo suvestinė, kairėje sumos lauko pusėje.</span><span class="sxs-lookup"><span data-stu-id="d789f-129">For this procedure enter an amount equal to the order balance which can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="d789f-130">Bus galima įvykdyti užsakymą kaip visiškai apmokėtą.</span><span class="sxs-lookup"><span data-stu-id="d789f-130">This will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="d789f-131">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="d789f-131">Click OK.</span></span>
18. <span data-ttu-id="d789f-132">Spustelėkite Pateikti.</span><span class="sxs-lookup"><span data-stu-id="d789f-132">Click Submit.</span></span>

