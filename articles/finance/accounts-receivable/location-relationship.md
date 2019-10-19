---
title: Vietos ir šalies ryšių tipo įtraukimas
description: Šioje temoje paaiškinta, kaip įtraukti naują vietą ir šalies ryšio tipą.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8c359c5c33bed5b5abe7fc0c8e362c3399e9051a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179081"
---
# <a name="add-location-roles-and-party-relationship-types"></a><span data-ttu-id="3d19e-103">Vietų vaidmenų ir šalių ryšių tipų įtraukimas</span><span class="sxs-lookup"><span data-stu-id="3d19e-103">Add location roles and party relationship types</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a><span data-ttu-id="3d19e-104">Vietų vaidmenų įtraukimas</span><span class="sxs-lookup"><span data-stu-id="3d19e-104">Add location roles</span></span>

<span data-ttu-id="3d19e-105">Norėdami galite įtraukti naujų vietos vaidmenų adresą ir kontaktinę informaciją dviem būdais:</span><span class="sxs-lookup"><span data-stu-id="3d19e-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="3d19e-106">Įtraukite jį puslapyje **Adreso ir kontaktinės informacijos paskirtis**.</span><span class="sxs-lookup"><span data-stu-id="3d19e-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="3d19e-107">Naujas vaidmuo bus įrašytas į lentelę **LogisticsLocationRole**, kurios tipas = 0, tai rodo, kad vaidmuo nėra sistemos vaidmuo, nurodytas į **LogisticsLocationRoleType** išvardijimo ir jo plėtinius.</span><span class="sxs-lookup"><span data-stu-id="3d19e-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="3d19e-108">Vartotojas galės naudotis šiuo vaidmeniu kurdamas adresą arba kontaktinę informaciją.</span><span class="sxs-lookup"><span data-stu-id="3d19e-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![Adreso ir turinio informacijos paskirtis](media/Address-Contact.PNG)

-  <span data-ttu-id="3d19e-110">Įtraukite jį į išvardijimo plėtinį **LogisticsLocationRoleType** ir leiskite jam automatiškai įvesti duomenų bazės sinchronizavimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="3d19e-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="3d19e-111">Sukurkite išvardijimo **LogisticsLocationRoleType** plėtinį ir įtraukite naująjį vaidmenį į plėtinį.</span><span class="sxs-lookup"><span data-stu-id="3d19e-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. <span data-ttu-id="3d19e-113">Sukurkite naują naujojo vaidmens išteklių failą ir tada jo ypatybėms priskirkite vertę.</span><span class="sxs-lookup"><span data-stu-id="3d19e-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![Naujas išteklių failas](media/Resource.PNG)
        
    3.  <span data-ttu-id="3d19e-115">Sukurkite automatinio duomenų įvedimo klasę ir pateikite apdorojimo programos metodą automatiniam naujojo vaidmens įvedimui.</span><span class="sxs-lookup"><span data-stu-id="3d19e-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![Automatinis duomenų įvedimas](media/Dirdata.PNG)

    4.  <span data-ttu-id="3d19e-117">Norėdami patikrinti naujojo vietos vaidmens automatinį įvedimą, galite sukurti vykdomą klasę ir iškviesti DirDataPopulation::insertLogisticsLocationRoles() in Main().</span><span class="sxs-lookup"><span data-stu-id="3d19e-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="3d19e-118">Atlikę šį procesą, pamatysite naująjį vaidmenį automatiškai įvestą lentelėje **LogisticsLocationRole**, kurios tipas \>0.</span><span class="sxs-lookup"><span data-stu-id="3d19e-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="3d19e-119">Naujasis vaidmuo bus rodomas puslapyje **Adreso ir kontaktinės informacijos paskirtis**.</span><span class="sxs-lookup"><span data-stu-id="3d19e-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![Naujos vietos įterpimas](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a><span data-ttu-id="3d19e-121">Šalių ryšių tipų įtraukimas</span><span class="sxs-lookup"><span data-stu-id="3d19e-121">Add party relationship types</span></span> 

<span data-ttu-id="3d19e-122">Yra du būdai, kaip įtraukti naują ryšio tipą:</span><span class="sxs-lookup"><span data-stu-id="3d19e-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="3d19e-123">Įtraukite jį puslapyje **Ryšių tipai**.</span><span class="sxs-lookup"><span data-stu-id="3d19e-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="3d19e-124">Naujasis ryšys bus įrašytas į **DirRelationshipTypeTable**, kurios sistemos tipas = 0.</span><span class="sxs-lookup"><span data-stu-id="3d19e-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![Ryšių tipai](media/Relationship.PNG)

-  <span data-ttu-id="3d19e-126">Įtraukite jį į išvardijimo plėtinį **DirSystemRelationshipType** ir leiskite jam automatiškai įvesti duomenų bazės sinchronizavimo proceso metu.</span><span class="sxs-lookup"><span data-stu-id="3d19e-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="3d19e-127">Sukurkite išvardijimo **DirSystemRelationshipType** plėtinį ir įtraukite naująjį ryšio tipą.</span><span class="sxs-lookup"><span data-stu-id="3d19e-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="3d19e-128">Sukurkite šio naujo tipo iniciatorių.</span><span class="sxs-lookup"><span data-stu-id="3d19e-128">Create an initializer for this new type.</span></span> <span data-ttu-id="3d19e-129">Pagrindiniame kode rasite keletą pavyzdžių, vienas iš jų yra **DirRelationshipTypeChildInitialize**.</span><span class="sxs-lookup"><span data-stu-id="3d19e-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="3d19e-130">Tai yra šalies ryšio, kurio tipas „Antrinis“, iniciatoriaus klasė.</span><span class="sxs-lookup"><span data-stu-id="3d19e-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="3d19e-131">Galite pradėti nuo savo iniciatoriaus, nukopijavę ir įklijavę šį kodą ir tuomet atnaujinę paryškintas sritis.</span><span class="sxs-lookup"><span data-stu-id="3d19e-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  <span data-ttu-id="3d19e-133">Norėdami patikrinti naujojo ryšio tipo automatinį įvedimą, galite sukurti vykdomą klasę ir iškviesti DirDataPopulation::insertDirRelationshipTypes() in Main().</span><span class="sxs-lookup"><span data-stu-id="3d19e-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="3d19e-134">Naująjį ryšio tipą turėtumėte pamatyti **DirRelationshipTypeTable**, be to, naujasis ryšio tipas bus pasiekiamas puslapyje **Ryšių tipai**.</span><span class="sxs-lookup"><span data-stu-id="3d19e-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![Vykdoma klasė](media/Runnable.PNG)
