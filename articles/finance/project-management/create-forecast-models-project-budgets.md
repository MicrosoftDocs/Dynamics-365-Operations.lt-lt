---
title: Prognozės modelių kūrimas projektų biudžetams
description: Šioje temoje aprašoma, kaip sukurti likusių biudžetų prognozės modelį.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321784"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="ac7d7-103">Prognozės modelių kūrimas projektų biudžetams</span><span class="sxs-lookup"><span data-stu-id="ac7d7-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac7d7-104">Šioje temoje aprašoma, kaip sukurti likusių biudžetų prognozės modelį.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="ac7d7-105">Projekte, kuriam taikoma biudžeto kontrolė, naudojama dviejų tipų biudžetai: pradinis ir likęs.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="ac7d7-106">Kai kuriate projekto biudžetą, turite nurodyti pradinio ir likusio biudžeto prognozės modelius, kurie buvo sukurti puslapyje **Prognozės modeliai**.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="ac7d7-107">Projekto biudžetas, pagrįstas nurodytais modeliais, sukuriamas, kai projekto biudžetas užfiksuojamas.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="ac7d7-108">Prognozės modelyje, kuris naudojamas biudžeto kontrolei, negali būti submodelių ir jo negalima naudoti kaip submodelio.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="ac7d7-109">Pasirinkite **Projektų valdymas ir apskaita** > **Sąranka** > **Prognozės**  > **Prognozės modeliai**.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="ac7d7-110">Pasirinkite **Naujas**, kad sukurtumėte naują prognozės modelį, tada įveskite modelio ID numerį ir naujo modelio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="ac7d7-111">Nustatykite parinktį **Sustabdyta** į **Taip**, kad būtų išvengta bet kokių prognozės modelio prognozės eilučių pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="ac7d7-112">Jei prognozės eilutės, su kuriomis susietas modelis, turi generuoti pinigų srauto prognozes DK, nustatykite **Įtraukti į pinigų srautų prognozes** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="ac7d7-113">Norėdami naudoti projekto datą kaip SF datą, nustatykite **Prognozės SF data** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="ac7d7-114">Lauke **Biudžeto tipas** pasirinkite vieną iš toliau nurodytų modelių tipų.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="ac7d7-115">**Pradinis biudžetas** – naudokite pradinio biudžeto sumas, kurios užfiksuojamos, kai pradinis biudžetas sukuriamas ir patvirtinamas.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="ac7d7-116">**Biudžeto likutis** – naudokite likusias biudžeto sumas projekto laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="ac7d7-117">Balansai šiame prognozės modelyje yra sumažinami faktinių operacijų ir padidinami arba sumažinami tikslinant biudžetą.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="ac7d7-118">**Perkėlimas** – naudokite projekto perkeliamo biudžeto sumas.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="ac7d7-119">Perkėlimas yra pasirinktinis procesas, kuris gali būti vykdomas norint perkelti nepanaudotas biudžeto sumas iš vienų finansinių metų į kitus.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="ac7d7-120">Nustatykite tolesnes parinktis kaip reikia.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-120">Set the following options as required:</span></span>

   - <span data-ttu-id="ac7d7-121">Norėdami naudoti projekto datą kaip SF datą, įjunkite **Prognozės SF data**.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="ac7d7-122">Įjunkite **NG prognozė**, kad būtų prognozuojama remiantis nebaigta gamyba (NG), tada pasirinkite NG tipą.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="ac7d7-123">Galite palikti numatytąją **Biudžeto tipas** reikšmę **Nėra** arba įvesti naują tipą.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="ac7d7-124">Pakeitus įrašą, biudžeto tipo pakeisti negalima.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="ac7d7-125">Pakeitus numatytąjį biudžeto tipą, visos kitos parinktys nebus pasiekiamos naujinimuose ir negalėsite pakartotinai naudoti šio prognozės modelio.</span><span class="sxs-lookup"><span data-stu-id="ac7d7-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

