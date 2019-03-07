---
title: Organizacijos hierarchijos kūrimas
description: Norėdami sukurti organizacinę hierarchiją, naudokite nurodytą procedūrą.
author: sericks007
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 203a586b06a13a7c67f246384152d17627e22041
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "308810"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="70023-103">Organizacijos hierarchijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="70023-103">Create an organization hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="70023-104">Norėdami sukurti organizacinę hierarchiją, naudokite nurodytą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="70023-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="70023-105">Naudodami organizacijos hierarchijas galite peržiūrėti informaciją apie įvairius savo įmonės aspektus ir sukurti atitinkamas ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="70023-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="70023-106">Pavyzdžiui, galite nustatyti vieną hierarchiją, skirtą mokesčių, juridinėms arba privalomoms ataskaitoms kurti.</span><span class="sxs-lookup"><span data-stu-id="70023-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="70023-107">Tada galite nustatyti kitą hierarchiją, kad būtų kuriamos finansinės informacijos, kurios nebūtina pateikti, bet kuri naudojama vidaus ataskaitose, ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="70023-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 



<span data-ttu-id="70023-108">Prieš kurdami organizacijos hierarchiją turite sukurti organizacijas.</span><span class="sxs-lookup"><span data-stu-id="70023-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="70023-109">Daugiau informacijos rasite užduotyse „Juridinio subjekto kūrimas‟ arba „Valdymo vieneto kūrimas‟.</span><span class="sxs-lookup"><span data-stu-id="70023-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="70023-110">Taip pat galite kurti padalinių ir komandų.</span><span class="sxs-lookup"><span data-stu-id="70023-110">You can also create departments and teams.</span></span> 



<span data-ttu-id="70023-111">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="70023-111">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-hierarchy"></a><span data-ttu-id="70023-112">Kurti hierarchiją</span><span class="sxs-lookup"><span data-stu-id="70023-112">Create a hierarchy</span></span>
1. <span data-ttu-id="70023-113">Pasirinkite Organizacijos administravimas > Organizacijos > Organizacijų hierarchijos.</span><span class="sxs-lookup"><span data-stu-id="70023-113">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="70023-114">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="70023-114">Click New.</span></span>
3. <span data-ttu-id="70023-115">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="70023-115">In the Name field, type a value.</span></span>
4. <span data-ttu-id="70023-116">Spustelėkite Priskirti paskirtį.</span><span class="sxs-lookup"><span data-stu-id="70023-116">Click Assign purpose.</span></span>
5. <span data-ttu-id="70023-117">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="70023-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="70023-118">Pasirinkite paskirtį, priskirtiną jūsų organizacijos hierarchijai.</span><span class="sxs-lookup"><span data-stu-id="70023-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="70023-119">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="70023-119">Click Add.</span></span>
7. <span data-ttu-id="70023-120">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="70023-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="70023-121">Suraskite ką tik savo sukurtą hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="70023-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="70023-122">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="70023-122">Click OK.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="70023-123">Organizacijų įtraukimas į hierarchiją</span><span class="sxs-lookup"><span data-stu-id="70023-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="70023-124">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="70023-124">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="70023-125">Pasirinkite savo hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="70023-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="70023-126">Spustelėkite Peržiūrėti hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="70023-126">Click View hierarchy.</span></span>
    * <span data-ttu-id="70023-127">Pagal poreikį įtraukite organizacijų.</span><span class="sxs-lookup"><span data-stu-id="70023-127">Add organizations, as necessary.</span></span>  
    * <span data-ttu-id="70023-128">Norėdami įtraukti organizaciją, spustelėkite Redaguoti ir Įterpti.</span><span class="sxs-lookup"><span data-stu-id="70023-128">To add an organization, click Edit and then Insert to add the organization.</span></span>     <span data-ttu-id="70023-129">Atlikę visus norimus pakeitimus, galite įrašyti juodraštį ir / arba pakeitimus publikuoti.</span><span class="sxs-lookup"><span data-stu-id="70023-129">When you are done making changes you can save a draft and/or publish the changes.</span></span>  

