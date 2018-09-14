--- 
title: " Mažmeninės prekybos parduotuvės išrašo kūrimas, skaičiavimas ir registravimas"
description: "Ši procedūra padeda neautomatiškai kurti, apskaičiuoti ir registruoti parduotuvės išrašą."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 9ea30e7e008bfcce77a7ee2f4d7d01a6cf1ababc
ms.contentlocale: lt-lt
ms.lasthandoff: 09/14/2018

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="76f3f-103"> Mažmeninės prekybos parduotuvės išrašo kūrimas, skaičiavimas ir registravimas</span><span class="sxs-lookup"><span data-stu-id="76f3f-103">Create, calculate, and post a statement for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="76f3f-104">Ši procedūra padeda neautomatiškai kurti, apskaičiuoti ir registruoti parduotuvės išrašą.</span><span class="sxs-lookup"><span data-stu-id="76f3f-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="76f3f-105">Taip pat galima sukonfigūruoti tų pačių užduočių paketines užduotis.</span><span class="sxs-lookup"><span data-stu-id="76f3f-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="76f3f-106">Paketinių užduočių konfigūravimo ir paleidimo veiksmai aprašyti kitose temose.</span><span class="sxs-lookup"><span data-stu-id="76f3f-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="76f3f-107">Norint atlikti šią procedūrą, reikalingos operacijos, kurios atliktos naudojant EKA ir įtrauktos į „Dynamics AX“.</span><span class="sxs-lookup"><span data-stu-id="76f3f-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="76f3f-108">Šiame įraše naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="76f3f-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="76f3f-109">Šioje procedūroje gali būti nurodyta „Microsoft Dynamics AX“.</span><span class="sxs-lookup"><span data-stu-id="76f3f-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="76f3f-110">Atkreipkite dėmesį, kad „Dynamics AX“ dabar vadinama „Microsoft Dynamics 365 for Operations“.</span><span class="sxs-lookup"><span data-stu-id="76f3f-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="76f3f-111">Eikite į Visos darbo sritys > ..</span><span class="sxs-lookup"><span data-stu-id="76f3f-111">Go to All workspaces > ..</span></span> <span data-ttu-id="76f3f-112">> Mažmeninės prekybos parduotuvės finansai.</span><span class="sxs-lookup"><span data-stu-id="76f3f-112">> Retail store financials.</span></span>
2. <span data-ttu-id="76f3f-113">Spustelėkite Naujas išrašas.</span><span class="sxs-lookup"><span data-stu-id="76f3f-113">Click New statement.</span></span>
3. <span data-ttu-id="76f3f-114">Lauke Parduotuvės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="76f3f-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="76f3f-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="76f3f-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="76f3f-116">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="76f3f-116">Click OK.</span></span>
    * <span data-ttu-id="76f3f-117">Tam tikri nustatymo grupės parametrai kontroliuoja, kurios operacijos įtraukiamos į išrašą ir kaip jos bus grupuojamos išrašo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="76f3f-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="76f3f-118">Galite atidaryti nustatymo grupę ir keisti šiuos parametrus arba galite naudoti numatytuosius.</span><span class="sxs-lookup"><span data-stu-id="76f3f-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="76f3f-119">Laukas Išrašo metodas nurodo, kaip bus grupuojamos išrašo eilutės.</span><span class="sxs-lookup"><span data-stu-id="76f3f-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="76f3f-120">Pasirinkite darbuotoją arba registrą, jei norite apskaičiuoti tik konkretaus darbuotojo arba registro išrašą.</span><span class="sxs-lookup"><span data-stu-id="76f3f-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="76f3f-121">Lauke Uždarymo metodas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="76f3f-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="76f3f-122">Spustelėkite Skaičiuoti išrašą.</span><span class="sxs-lookup"><span data-stu-id="76f3f-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="76f3f-123">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="76f3f-123">Click Yes.</span></span>
    * <span data-ttu-id="76f3f-124">Apskaičiavus išrašą, turėtų būti sukurtos eilutės su kiekvieno naudoto mokėjimo metodo ir išrašo metodo bendrosiomis sumomis.</span><span class="sxs-lookup"><span data-stu-id="76f3f-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="76f3f-125">Įveskite apskaičiuotą sumą kiekvienoje eilutėje, jei ji turi būti įvesta arba atnaujinta.</span><span class="sxs-lookup"><span data-stu-id="76f3f-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="76f3f-126">Apskaičiuotas laukas užpildomas naudojant sumas iš EKA atliktų mokėjimo priemonių deklaracijų.</span><span class="sxs-lookup"><span data-stu-id="76f3f-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="76f3f-127">Spustelėkite Registruoti išrašą.</span><span class="sxs-lookup"><span data-stu-id="76f3f-127">Click Post statement.</span></span>
10. <span data-ttu-id="76f3f-128">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="76f3f-128">Click Close.</span></span>
11. <span data-ttu-id="76f3f-129">Eikite į Mažmeninė prekyba ir prekyba > Kanalai > Mažmeninės prekybos parduotuvės finansai.</span><span class="sxs-lookup"><span data-stu-id="76f3f-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="76f3f-130">Spustelėkite skirtuką Užregistruoti išrašai.</span><span class="sxs-lookup"><span data-stu-id="76f3f-130">Click the Posted statements tab.</span></span>


