---
title: Atostogų ir neatvykimų parametrų konfigūravimas
description: Žmogiškųjų išteklių parametrų, skirtų atostogoms ir neatvykimams, nustatymas programoje „Dynamics 365 Human Resources“.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009921"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="9dbd2-103">Atostogų ir neatvykimų parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9dbd2-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="9dbd2-104">Prieš nustatant atostogų ir neatvykimų planus „Dynamics 365 Human Resources“, naudinga patikrinti visus susijusius žmogiškųjų išteklių parametrų nustatymus, įskaitant:</span><span class="sxs-lookup"><span data-stu-id="9dbd2-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="9dbd2-105">Atostogų užklausų numeraciją</span><span class="sxs-lookup"><span data-stu-id="9dbd2-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="9dbd2-106">Nedarbingumo dėl ligos ar slaugymo akto (FMLA) parametrus</span><span class="sxs-lookup"><span data-stu-id="9dbd2-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="9dbd2-107">Darbuotojo atostogų ir neatvykimų užklausų savitarnos parametrus</span><span class="sxs-lookup"><span data-stu-id="9dbd2-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="9dbd2-108">Atostogų ir neatvykimų parametrai</span><span class="sxs-lookup"><span data-stu-id="9dbd2-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="9dbd2-109">Peržiūrėti ir keisti žmogiškųjų išteklių parametrus</span><span class="sxs-lookup"><span data-stu-id="9dbd2-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="9dbd2-110">Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="9dbd2-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="9dbd2-111">Dalyje **Sąranka** pasirinkite **Žmogiškųjų išteklių parametrai**.</span><span class="sxs-lookup"><span data-stu-id="9dbd2-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="9dbd2-112">Skirtuke **Numeracija** patikrinkite **numeracijos kodą**, skirtą **atostogų užklausos ID**, ir pakeiskite, jeigu reikia.</span><span class="sxs-lookup"><span data-stu-id="9dbd2-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="9dbd2-113">Šiuo parametru nustatoma seka, naudojama automatiškai priskirti ID atostogų užklausoms.</span><span class="sxs-lookup"><span data-stu-id="9dbd2-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="9dbd2-114">Skirtuke **FMLA** patikrinkite FMLA parametrus ir pakeiskite, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="9dbd2-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="9dbd2-115">Skirtuke **Darbuotojo savitarna** nurodykite, ar vadybininkai savo darbuotojų vardu gali įvesti atostogų ir neatvykimų užklausas.</span><span class="sxs-lookup"><span data-stu-id="9dbd2-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="9dbd2-116">Skirtuke **Atostogos ir neatvykimai** patikrinkite parametrus ir pakeiskite, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="9dbd2-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="9dbd2-117">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9dbd2-117">Select **Save**.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="9dbd2-118">Kalendoriaus parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="9dbd2-118">Configure calendar parameters</span></span>

<span data-ttu-id="9dbd2-119">Jeigu įjungėte atostogų ir neatvykimų kalendoriaus peržiūros funkciją, jums reikia sukonfigūruoti papildomus parametrus.</span><span class="sxs-lookup"><span data-stu-id="9dbd2-119">If you have enabled the Leave and absence calendar preview feature, you need to configure additional parameters.</span></span> 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> <span data-ttu-id="9dbd2-120">2020 m. vasario 3 d. peržiūros leidime įgalintos tik **Laukiančios atostogų užklausos**.</span><span class="sxs-lookup"><span data-stu-id="9dbd2-120">For the preview release on February 3, 2020, only **Pending leave requests** are enabled.</span></span>

1. <span data-ttu-id="9dbd2-121">Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.</span><span class="sxs-lookup"><span data-stu-id="9dbd2-121">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="9dbd2-122">Dalyje **Sąranka** pasirinkite **Žmogiškųjų išteklių parametrai**.</span><span class="sxs-lookup"><span data-stu-id="9dbd2-122">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="9dbd2-123">Skirtuke **Kalendorius** keiskite kalendoriaus parametrus, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="9dbd2-123">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="9dbd2-124">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="9dbd2-124">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="9dbd2-125">Taip pat žiūrėkite</span><span class="sxs-lookup"><span data-stu-id="9dbd2-125">See also</span></span>

- [<span data-ttu-id="9dbd2-126">Atostogų ir neatvykimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="9dbd2-126">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
