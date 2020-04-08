---
title: 'ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (1 dalis – Formato kūrimas)'
description: Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7a2559bdadbfc74a14bd0e7add9c2f794226e0b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141930"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="78853-103">ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (1 dalis – Formato kūrimas)</span><span class="sxs-lookup"><span data-stu-id="78853-103">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78853-104">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis.</span><span class="sxs-lookup"><span data-stu-id="78853-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="78853-105">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="78853-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="78853-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“.</span><span class="sxs-lookup"><span data-stu-id="78853-106">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="78853-107">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="78853-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="78853-108">Gaukite prieigą prie „Microsoft“ teikiamų konfigūracijų sąrašo</span><span class="sxs-lookup"><span data-stu-id="78853-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="78853-109">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="78853-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="78853-110">Įsitikinkite, kad „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="78853-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="78853-111">yra pasiekiamas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="78853-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="78853-112">Pasirinkite „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="78853-112">Select the "Litware, Inc."</span></span> <span data-ttu-id="78853-113">„Litware, Inc.“.</span><span class="sxs-lookup"><span data-stu-id="78853-113">provider.</span></span>
3. <span data-ttu-id="78853-114">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="78853-114">Click Repositories.</span></span>
    * <span data-ttu-id="78853-115">Jei tipo Operacijų ištekliai saugykla jau yra, praleiskite likusius dabartinės antrinės užduoties veiksmus.</span><span class="sxs-lookup"><span data-stu-id="78853-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="78853-116">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="78853-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="78853-117">Lauke Konfigūracijų saugyklos tipas įveskite Operacijų ištekliai.</span><span class="sxs-lookup"><span data-stu-id="78853-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="78853-118">Spustelėkite Kurti saugyklą.</span><span class="sxs-lookup"><span data-stu-id="78853-118">Click Create repository.</span></span>
7. <span data-ttu-id="78853-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="78853-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="78853-120">Gaukite „Microsoft“ teikiamas „Intrastat“ konfigūracijas</span><span class="sxs-lookup"><span data-stu-id="78853-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="78853-121">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="78853-121">Click Open.</span></span>
2. <span data-ttu-id="78853-122">Medyje pasirinkite Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="78853-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="78853-123">Spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="78853-123">Click Import.</span></span>
    * <span data-ttu-id="78853-124">Spustelėkite Importuoti 1.1 pasirinktos konfigūracijos versiją.</span><span class="sxs-lookup"><span data-stu-id="78853-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="78853-125">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="78853-125">Click Yes.</span></span>
5. <span data-ttu-id="78853-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="78853-126">Close the page.</span></span>
6. <span data-ttu-id="78853-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="78853-127">Close the page.</span></span>
7. <span data-ttu-id="78853-128">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="78853-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="78853-129">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="78853-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="78853-130">Medyje pasirinkite Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="78853-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>

