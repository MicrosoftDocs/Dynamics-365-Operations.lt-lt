--- 
title: "Konfigūracijų teikėjų kūrimas ir jų pažymėjimas kaip aktyviais"
description: "Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigoms priskirtas naudotojas gali sukurti elektroninių ataskaitų (ER) konfigūracijų teikėją."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 13a27c2fec2a2b226e9ae8d5b8f9a61e8b79ceb0
ms.contentlocale: lt-lt
ms.lasthandoff: 10/16/2018

---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="608fe-103">Konfigūracijų teikėjų kūrimas ir jų pažymėjimas kaip aktyviais</span><span class="sxs-lookup"><span data-stu-id="608fe-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="608fe-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigoms priskirtas naudotojas gali sukurti elektroninių ataskaitų (ER) konfigūracijų teikėją.</span><span class="sxs-lookup"><span data-stu-id="608fe-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="608fe-105">Kiekviena ER konfigūracija į teikėją nurodys kaip į konfigūracijos autorių.</span><span class="sxs-lookup"><span data-stu-id="608fe-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="608fe-106">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūracijų teikėją. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijų teikėjų paslaugas visos įmonės naudoja bendrai.</span><span class="sxs-lookup"><span data-stu-id="608fe-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="608fe-107">Kurti teikėją</span><span class="sxs-lookup"><span data-stu-id="608fe-107">Create a provider</span></span>
1. <span data-ttu-id="608fe-108">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="608fe-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="608fe-109">Spustelėkite Konfigūracijų teikėjai.</span><span class="sxs-lookup"><span data-stu-id="608fe-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="608fe-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="608fe-110">Click New.</span></span>
    * <span data-ttu-id="608fe-111">Teikėjo įrašas turi unikalų pavadinimą ir URL.</span><span class="sxs-lookup"><span data-stu-id="608fe-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="608fe-112">Peržiūrėkite šio puslapio turinį ir praleiskite šią procedūrą, jei „Litware, Inc.“ (http://www.litware.com) įrašas jau egzistuoja.</span><span class="sxs-lookup"><span data-stu-id="608fe-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="608fe-113">Lauke Pavadinimas surinkite „Litware, Inc.‟.</span><span class="sxs-lookup"><span data-stu-id="608fe-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="608fe-114">„Litware, Inc.‟</span><span class="sxs-lookup"><span data-stu-id="608fe-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="608fe-115">Lauke Interneto adresas įrašykite „http://www.litware.com“.</span><span class="sxs-lookup"><span data-stu-id="608fe-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * http://www.litware.com  
6. <span data-ttu-id="608fe-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="608fe-116">Click Save.</span></span>
7. <span data-ttu-id="608fe-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="608fe-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="608fe-118">Pasirinkti kaip aktyvų teikėją</span><span class="sxs-lookup"><span data-stu-id="608fe-118">Select as an active provider</span></span>
1. <span data-ttu-id="608fe-119">Pasirinkite teikėją „Litware, Inc.“.</span><span class="sxs-lookup"><span data-stu-id="608fe-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="608fe-120">Spustelėkite Nustatyti kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="608fe-120">Click Set active.</span></span>


