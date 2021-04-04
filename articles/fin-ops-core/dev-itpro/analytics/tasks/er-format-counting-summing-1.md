---
title: 'ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (1 dalis – Formato kūrimas)'
description: Šioje temoje aprašoma, kaip konfigūruoti elektroninės ataskaitos formatą, kad būtų galima atlikti skaičiavimą ir sumuoti remiantis jau sugeneruoto teksto išvesties duomenimis. (1 dalis)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 64bf9f48319029e835f9e3fe2b888625100cc408
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565147"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a><span data-ttu-id="224f1-104">ER: formato konfigūravimas skaičiavimo ir sumavimo veiksmams atlikti (1 dalis – Formato kūrimas)</span><span class="sxs-lookup"><span data-stu-id="224f1-104">ER Configure format to do counting and summing (Part 1 - Create format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="224f1-105">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis.</span><span class="sxs-lookup"><span data-stu-id="224f1-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="224f1-106">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="224f1-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="224f1-107">Norėdami atlikti šiuos veiksmus, pirmiausia turite atlikti veiksmus, nurodytus procedūroje „Konfigūracijos teikėjo kūrimas ir pažymėjimas aktyviu“.</span><span class="sxs-lookup"><span data-stu-id="224f1-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

<span data-ttu-id="224f1-108">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="224f1-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="224f1-109">Gaukite prieigą prie „Microsoft“ teikiamų konfigūracijų sąrašo</span><span class="sxs-lookup"><span data-stu-id="224f1-109">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="224f1-110">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="224f1-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="224f1-111">Įsitikinkite, kad „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="224f1-111">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="224f1-112">yra pasiekiamas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="224f1-112">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="224f1-113">Pasirinkite „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="224f1-113">Select the "Litware, Inc."</span></span> <span data-ttu-id="224f1-114">„Litware, Inc.“.</span><span class="sxs-lookup"><span data-stu-id="224f1-114">provider.</span></span>
3. <span data-ttu-id="224f1-115">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="224f1-115">Click Repositories.</span></span>
    * <span data-ttu-id="224f1-116">Jei tipo Operacijų ištekliai saugykla jau yra, praleiskite likusius dabartinės antrinės užduoties veiksmus.</span><span class="sxs-lookup"><span data-stu-id="224f1-116">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="224f1-117">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="224f1-117">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="224f1-118">Lauke Konfigūracijų saugyklos tipas įveskite Operacijų ištekliai.</span><span class="sxs-lookup"><span data-stu-id="224f1-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="224f1-119">Spustelėkite Kurti saugyklą.</span><span class="sxs-lookup"><span data-stu-id="224f1-119">Click Create repository.</span></span>
7. <span data-ttu-id="224f1-120">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="224f1-120">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="224f1-121">Gaukite „Microsoft“ teikiamas „Intrastat“ konfigūracijas</span><span class="sxs-lookup"><span data-stu-id="224f1-121">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="224f1-122">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="224f1-122">Click Open.</span></span>
2. <span data-ttu-id="224f1-123">Medyje pasirinkite Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="224f1-123">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="224f1-124">Spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="224f1-124">Click Import.</span></span>
    * <span data-ttu-id="224f1-125">Spustelėkite Importuoti 1.1 pasirinktos konfigūracijos versiją.</span><span class="sxs-lookup"><span data-stu-id="224f1-125">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="224f1-126">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="224f1-126">Click Yes.</span></span>
5. <span data-ttu-id="224f1-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="224f1-127">Close the page.</span></span>
6. <span data-ttu-id="224f1-128">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="224f1-128">Close the page.</span></span>
7. <span data-ttu-id="224f1-129">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="224f1-129">Click Reporting configurations.</span></span>
8. <span data-ttu-id="224f1-130">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="224f1-130">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="224f1-131">Medyje pasirinkite Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="224f1-131">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]