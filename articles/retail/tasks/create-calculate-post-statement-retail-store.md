--- 
title: " Mažmeninės prekybos parduotuvės išrašo kūrimas, skaičiavimas ir registravimas"
description: "Ši procedūra padeda neautomatiškai kurti, apskaičiuoti ir registruoti parduotuvės išrašą."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 3b49ef7f6545193e40ae00dae4bbaead7ee4b7b9
ms.contentlocale: lt-lt
ms.lasthandoff: 01/19/2018

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a><span data-ttu-id="3b9b1-103"> Mažmeninės prekybos parduotuvės išrašo kūrimas, skaičiavimas ir registravimas</span><span class="sxs-lookup"><span data-stu-id="3b9b1-103">Create, calculate, and post a statement for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3b9b1-104">Ši procedūra padeda neautomatiškai kurti, apskaičiuoti ir registruoti parduotuvės išrašą.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="3b9b1-105">Taip pat galima sukonfigūruoti tų pačių užduočių paketines užduotis.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="3b9b1-106">Paketinių užduočių konfigūravimo ir paleidimo veiksmai aprašyti kitose temose.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="3b9b1-107">Norint atlikti šią procedūrą, reikalingos operacijos, kurios atliktos naudojant EKA ir įtrauktos į „Dynamics AX“.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="3b9b1-108">Šiame įraše naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="3b9b1-109">Šioje procedūroje gali būti nurodyta „Microsoft Dynamics AX“.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="3b9b1-110">Atkreipkite dėmesį, kad „Dynamics AX“ dabar vadinama „Microsoft Dynamics 365 for Operations“.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="3b9b1-111">Eikite į Visos darbo sritys > ..</span><span class="sxs-lookup"><span data-stu-id="3b9b1-111">Go to All workspaces > ..</span></span> <span data-ttu-id="3b9b1-112">> Mažmeninės prekybos parduotuvės finansai.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-112">> Retail store financials.</span></span>
2. <span data-ttu-id="3b9b1-113">Spustelėkite Naujas išrašas.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-113">Click New statement.</span></span>
3. <span data-ttu-id="3b9b1-114">Lauke Parduotuvės numeris spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3b9b1-115">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="3b9b1-116">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-116">Click OK.</span></span>
    * <span data-ttu-id="3b9b1-117">Tam tikri nustatymo grupės parametrai kontroliuoja, kurios operacijos įtraukiamos į išrašą ir kaip jos bus grupuojamos išrašo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="3b9b1-118">Galite atidaryti nustatymo grupę ir keisti šiuos parametrus arba galite naudoti numatytuosius.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="3b9b1-119">Laukas Išrašo metodas nurodo, kaip bus grupuojamos išrašo eilutės.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="3b9b1-120">Pasirinkite darbuotoją arba registrą, jei norite apskaičiuoti tik konkretaus darbuotojo arba registro išrašą.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="3b9b1-121">Lauke Uždarymo metodas pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="3b9b1-122">Spustelėkite Skaičiuoti išrašą.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="3b9b1-123">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-123">Click Yes.</span></span>
    * <span data-ttu-id="3b9b1-124">Apskaičiavus išrašą, turėtų būti sukurtos eilutės su kiekvieno naudoto mokėjimo metodo ir išrašo metodo bendrosiomis sumomis.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="3b9b1-125">Įveskite apskaičiuotą sumą kiekvienoje eilutėje, jei ji turi būti įvesta arba atnaujinta.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="3b9b1-126">Apskaičiuotas laukas užpildomas naudojant sumas iš EKA atliktų mokėjimo priemonių deklaracijų.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="3b9b1-127">Spustelėkite Registruoti išrašą.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-127">Click Post statement.</span></span>
10. <span data-ttu-id="3b9b1-128">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-128">Click Close.</span></span>
11. <span data-ttu-id="3b9b1-129">Eikite į Mažmeninė prekyba ir prekyba > Kanalai > Mažmeninės prekybos parduotuvės finansai.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="3b9b1-130">Spustelėkite skirtuką Užregistruoti išrašai.</span><span class="sxs-lookup"><span data-stu-id="3b9b1-130">Click the Posted statements tab.</span></span>


