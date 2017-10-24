--- 
title: "Elektroninių ataskaitų (ER) formato konfigūracijos kūrimas"
description: "Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: efdb64fa157af0d96c2ff0e5de3db5a98190bc68
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-formate-for-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="dbbee-103">Elektroninių ataskaitų (ER) formato konfigūracijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="dbbee-103">Create formate for counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dbbee-104">Toliau nurodytuose veiksmuose paaiškinta, kaip vartotojas, kuriam priskirtas sistemos administratoriaus arba elektroninių ataskaitų kūrėjo vaidmuo, gali konfigūruoti elektroninių ataskaitų (ER) formatą, norėdamas atlikti skaičiavimo ir sumavimo veiksmus pagal jau sugeneruotos teksto išvesties duomenis.</span><span class="sxs-lookup"><span data-stu-id="dbbee-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="dbbee-105">Šiuos veiksmus galima atlikti bet kurioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="dbbee-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="dbbee-106">Norėdami atlikti šiuos veiksmus, pirmiausia turite juos užbaigti procedūroje „Sukurti konfigūracijos teikėją ir pažymėti jį kaip aktyvų“.</span><span class="sxs-lookup"><span data-stu-id="dbbee-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

<span data-ttu-id="dbbee-107">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="dbbee-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="dbbee-108">Gaukite prieigą prie „Microsoft“ teikiamų konfigūracijų sąrašo</span><span class="sxs-lookup"><span data-stu-id="dbbee-108">Get access to the list of configurations provided by Microsoft</span></span>
1. <span data-ttu-id="dbbee-109">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="dbbee-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="dbbee-110">Įsitikinkite, kad teikėjas „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="dbbee-110">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="dbbee-111">yra pasiekiamas ir pažymėtas kaip aktyvus.</span><span class="sxs-lookup"><span data-stu-id="dbbee-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="dbbee-112">Pasirinkite „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="dbbee-112">Select the “Litware, Inc.”</span></span> <span data-ttu-id="dbbee-113">„Litware, Inc.“.</span><span class="sxs-lookup"><span data-stu-id="dbbee-113">provider.</span></span>
3. <span data-ttu-id="dbbee-114">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="dbbee-114">Click Repositories.</span></span>
    * <span data-ttu-id="dbbee-115">Jei tipo Operacijų ištekliai saugykla jau yra, praleiskite likusius dabartinės antrinės užduoties veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dbbee-115">If a repository of the "Operations resources" type already exists, skip the remaining steps of the current sub-task.</span></span>  
4. <span data-ttu-id="dbbee-116">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="dbbee-116">Click Add to open the drop dialog.</span></span>
5. <span data-ttu-id="dbbee-117">Lauke Konfigūracijų saugyklos tipas įveskite Operacijų ištekliai.</span><span class="sxs-lookup"><span data-stu-id="dbbee-117">In the Configuration repository type field, enter 'Operations resources'.</span></span>
6. <span data-ttu-id="dbbee-118">Spustelėkite Kurti saugyklą.</span><span class="sxs-lookup"><span data-stu-id="dbbee-118">Click Create repository.</span></span>
7. <span data-ttu-id="dbbee-119">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="dbbee-119">Click OK.</span></span>

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a><span data-ttu-id="dbbee-120">Gaukite „Microsoft“ teikiamas „Intrastat“ konfigūracijas</span><span class="sxs-lookup"><span data-stu-id="dbbee-120">Get the Intrastat configurations provided by Microsoft</span></span>
1. <span data-ttu-id="dbbee-121">Spustelėkite Atidaryti.</span><span class="sxs-lookup"><span data-stu-id="dbbee-121">Click Open.</span></span>
2. <span data-ttu-id="dbbee-122">Medyje pasirinkite Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="dbbee-122">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
3. <span data-ttu-id="dbbee-123">Spustelėkite Importuoti.</span><span class="sxs-lookup"><span data-stu-id="dbbee-123">Click Import.</span></span>
    * <span data-ttu-id="dbbee-124">Spustelėkite Importuoti 1.1 pasirinktos konfigūracijos versiją.</span><span class="sxs-lookup"><span data-stu-id="dbbee-124">Click Import for version 1.1 of the selected configuration.</span></span>  
4. <span data-ttu-id="dbbee-125">Spustelėkite Taip.</span><span class="sxs-lookup"><span data-stu-id="dbbee-125">Click Yes.</span></span>
5. <span data-ttu-id="dbbee-126">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="dbbee-126">Close the page.</span></span>
6. <span data-ttu-id="dbbee-127">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="dbbee-127">Close the page.</span></span>
7. <span data-ttu-id="dbbee-128">Spustelėkite Ataskaitų konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="dbbee-128">Click Reporting configurations.</span></span>
8. <span data-ttu-id="dbbee-129">Medyje išplėskite „Intrastat“ modelis.</span><span class="sxs-lookup"><span data-stu-id="dbbee-129">In the tree, expand 'Intrastat model'.</span></span>
9. <span data-ttu-id="dbbee-130">Medyje pasirinkite Intrastat model\Intrastat (DE).</span><span class="sxs-lookup"><span data-stu-id="dbbee-130">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>


