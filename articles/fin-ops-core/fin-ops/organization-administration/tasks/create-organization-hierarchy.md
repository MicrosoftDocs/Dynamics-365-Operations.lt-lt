---
title: Organizacijos hierarchijos kūrimas
description: Norėdami sukurti organizacinę hierarchiją, naudokite nurodytą procedūrą.
author: sericks007
manager: AnnBe
ms.date: 07/01/2019
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
ms.openlocfilehash: dde06f758be57fb646696c861218565476abcadc
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140564"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="a9a63-103">Organizacijos hierarchijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="a9a63-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a9a63-104">Norėdami sukurti organizacinę hierarchiją, naudokite nurodytą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="a9a63-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="a9a63-105">Naudodami organizacijos hierarchijas galite peržiūrėti informaciją apie įvairius savo įmonės aspektus ir sukurti atitinkamas ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="a9a63-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="a9a63-106">Pavyzdžiui, galite nustatyti vieną hierarchiją, skirtą mokesčių, juridinėms arba privalomoms ataskaitoms kurti.</span><span class="sxs-lookup"><span data-stu-id="a9a63-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="a9a63-107">Tada galite nustatyti kitą hierarchiją, kad būtų kuriamos finansinės informacijos, kurios nebūtina pateikti, bet kuri naudojama vidaus ataskaitose, ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="a9a63-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="a9a63-108">Prieš kurdami organizacijos hierarchiją turite sukurti organizacijas.</span><span class="sxs-lookup"><span data-stu-id="a9a63-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="a9a63-109">Daugiau informacijos rasite užduotyse „Juridinio subjekto kūrimas‟ arba „Valdymo vieneto kūrimas‟.</span><span class="sxs-lookup"><span data-stu-id="a9a63-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="a9a63-110">Taip pat galite kurti padalinių ir komandų.</span><span class="sxs-lookup"><span data-stu-id="a9a63-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="a9a63-111">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="a9a63-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="a9a63-112">Kurti hierarchiją</span><span class="sxs-lookup"><span data-stu-id="a9a63-112">Create a hierarchy</span></span>
1. <span data-ttu-id="a9a63-113">Eikite į **Naršymo sritis > Moduliai > Organizacijos administravimas > Organizacijos > Organizacijos hierarchijos**.</span><span class="sxs-lookup"><span data-stu-id="a9a63-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="a9a63-114">**Veiksmų sritis** spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a9a63-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="a9a63-115">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a9a63-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="a9a63-116">Skyriuje **Tikslas** spustelėkite **Priskirti tikslą**.</span><span class="sxs-lookup"><span data-stu-id="a9a63-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="a9a63-117">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a9a63-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="a9a63-118">Pasirinkite paskirtį, priskirtiną jūsų organizacijos hierarchijai.</span><span class="sxs-lookup"><span data-stu-id="a9a63-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="a9a63-119">Skyriuje **Priskirtos hierarchijos** spustelėkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="a9a63-119">In the **Assigned hierarchies** sectiom, click **Add**.</span></span>
7. <span data-ttu-id="a9a63-120">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="a9a63-120">In the list, mark the selected row.</span></span> <span data-ttu-id="a9a63-121">Suraskite ką tik savo sukurtą hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="a9a63-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="a9a63-122">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a9a63-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="a9a63-123">Organizacijų įtraukimas į hierarchiją</span><span class="sxs-lookup"><span data-stu-id="a9a63-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="a9a63-124">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="a9a63-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="a9a63-125">Pasirinkite savo hierarchiją.</span><span class="sxs-lookup"><span data-stu-id="a9a63-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="a9a63-126">Skyriuje **Priskirtos hierarchijos** spustelėkite **Peržiūrėti hierarchiją**.</span><span class="sxs-lookup"><span data-stu-id="a9a63-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="a9a63-127">Pagal poreikį įtraukite organizacijų.</span><span class="sxs-lookup"><span data-stu-id="a9a63-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="a9a63-128">Norėdami įtraukti organizaciją, spustelėkite **Redaguoti**, tada – **Įterpti**, kad įtrauktumėte organizaciją.</span><span class="sxs-lookup"><span data-stu-id="a9a63-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="a9a63-129">Atlikę keitimus, galite **Įrašyti** juodraštį ir (arba) **Publikuoti** keitimus.</span><span class="sxs-lookup"><span data-stu-id="a9a63-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  

