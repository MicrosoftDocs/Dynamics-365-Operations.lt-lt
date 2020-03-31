---
title: Mažmeninės prekybos parduotuvės išrašų kūrimas, skaičiavimas ir registravimas
description: Ši procedūra padeda neautomatiškai kurti, apskaičiuoti ir registruoti parduotuvės išrašą.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3b26ea5c816339eef88bfdd9ac59701dcaa31fe4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023418"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="66155-103">Mažmeninės prekybos parduotuvės išrašų kūrimas, skaičiavimas ir registravimas</span><span class="sxs-lookup"><span data-stu-id="66155-103">Create, calculate, and post statements for a retail store</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="66155-104">Ši procedūra padeda neautomatiškai kurti, apskaičiuoti ir registruoti parduotuvės išrašą.</span><span class="sxs-lookup"><span data-stu-id="66155-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="66155-105">Taip pat galima sukonfigūruoti tų pačių užduočių paketines užduotis.</span><span class="sxs-lookup"><span data-stu-id="66155-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="66155-106">Paketinių užduočių konfigūravimo ir paleidimo veiksmai aprašyti kitose temose.</span><span class="sxs-lookup"><span data-stu-id="66155-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="66155-107">Norint atlikti šią procedūrą, reikalingos operacijos, kurios atliktos naudojant EKA ir įtrauktos į „Dynamics Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="66155-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 Commerce.</span></span> <span data-ttu-id="66155-108">Šiame įraše naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="66155-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="66155-109">Pagrindiniame puslapyje pasirinkite **Parduotuvės finansai**.</span><span class="sxs-lookup"><span data-stu-id="66155-109">Select **Store financials** from the home page.</span></span>
2. <span data-ttu-id="66155-110">Pasirinkite **Naujas išrašas**.</span><span class="sxs-lookup"><span data-stu-id="66155-110">Select **New statement**.</span></span>
3. <span data-ttu-id="66155-111">Lauke **Parduotuvės numeris** spustelėkite išplečiamąjį mygtuką, kad pasirinktumėte parinktį.</span><span class="sxs-lookup"><span data-stu-id="66155-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="66155-112">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="66155-112">Select **OK**.</span></span>
5. <span data-ttu-id="66155-113">Tam tikri grupės **Sąranka** parametrai kontroliuoja, kurios operacijos įtraukiamos į išrašą ir kaip jos bus grupuojamos išrašo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="66155-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="66155-114">Galite atidaryti grupę **Sąranka** ir keisti šiuos parametrus arba galite naudoti numatytuosius.</span><span class="sxs-lookup"><span data-stu-id="66155-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="66155-115">Laukas **Išrašo metodas** nurodo, kaip bus grupuojamos išrašo eilutės.</span><span class="sxs-lookup"><span data-stu-id="66155-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="66155-116">Pasirinkite darbuotoją arba registrą, jei lauke **darbuotojai arba registras** norite apskaičiuoti tik konkretaus darbuotojo arba registro išrašą.</span><span class="sxs-lookup"><span data-stu-id="66155-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="66155-117">Lauke **Uždarymo metodas** pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="66155-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="66155-118">Veiksmų srityje pasirinkite **Skaičiuoti išrašą**.</span><span class="sxs-lookup"><span data-stu-id="66155-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="66155-119">Pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="66155-119">Select **Yes**.</span></span>
    - <span data-ttu-id="66155-120">Apskaičiavus išrašą, turėtų būti sukurtos eilutės su kiekvieno naudoto mokėjimo metodo ir išrašo metodo bendrosiomis sumomis.</span><span class="sxs-lookup"><span data-stu-id="66155-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="66155-121">Įveskite apskaičiuotą sumą kiekvienoje eilutėje, jei ji turi būti įvesta arba atnaujinta.</span><span class="sxs-lookup"><span data-stu-id="66155-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="66155-122">Apskaičiuotas laukas užpildomas naudojant sumas iš EKA atliktų mokėjimo priemonių deklaracijų.</span><span class="sxs-lookup"><span data-stu-id="66155-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="66155-123">Veiksmų srityje pasirinkite **Registruoti išrašą**.</span><span class="sxs-lookup"><span data-stu-id="66155-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="66155-124">Pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="66155-124">Select **Close**.</span></span>
11. <span data-ttu-id="66155-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="66155-125">Close the pane.</span></span>
12. <span data-ttu-id="66155-126">Pagrindiniame puslapyje pasirinkite **Parduotuvės finansai**.</span><span class="sxs-lookup"><span data-stu-id="66155-126">At the home page, select **Store financials**.</span></span>
13. <span data-ttu-id="66155-127">Spustelėkite skirtuką **Užregistruoti išrašai**.</span><span class="sxs-lookup"><span data-stu-id="66155-127">Select the **Posted statements** tab.</span></span>
