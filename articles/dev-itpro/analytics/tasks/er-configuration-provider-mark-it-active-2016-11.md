--- 
title: "Konfigūracijų teikėjo sukūrimas ir pažymėjimas aktyviu elektroninėse ataskaitose (ER)"
description: "Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigoms priskirtas naudotojas gali sukurti elektroninių ataskaitų (ER) konfigūracijų teikėją."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9ed6f62318cd6806de1b4c9d6aa314c5f0a25500
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-configuration-provider-and-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="b1f6b-103">Konfigūracijų teikėjo sukūrimas ir pažymėjimas aktyviu elektroninėse ataskaitose (ER)</span><span class="sxs-lookup"><span data-stu-id="b1f6b-103">Create a configuration provider and mark it as active for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b1f6b-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigoms priskirtas naudotojas gali sukurti elektroninių ataskaitų (ER) konfigūracijų teikėją.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="b1f6b-105">Kiekviena ER konfigūracija į teikėją nurodys kaip į konfigūracijos autorių.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="b1f6b-106">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūracijų teikėją. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijų teikėjų paslaugas visos įmonės naudoja bendrai.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="b1f6b-107">Kurti teikėją</span><span class="sxs-lookup"><span data-stu-id="b1f6b-107">Create a provider</span></span>
1. <span data-ttu-id="b1f6b-108">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b1f6b-109">Spustelėkite Konfigūracijų teikėjai.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="b1f6b-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-110">Click New.</span></span>
    * <span data-ttu-id="b1f6b-111">Teikėjo įrašas turi unikalų pavadinimą ir URL.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="b1f6b-112">Peržiūrėkite šio puslapio turinį ir praleiskite šią procedūrą, jei „Litware, Inc.“ (`http://www.litware.com`) įrašas jau egzistuoja.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (`http://www.litware.com`) already exists.</span></span>  
4. <span data-ttu-id="b1f6b-113">Lauke Pavadinimas surinkite „Litware, Inc.‟.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="b1f6b-114">„Litware, Inc.‟</span><span class="sxs-lookup"><span data-stu-id="b1f6b-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="b1f6b-115">Lauke Interneto adresas įrašykite `http://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-115">In the Internet address field, type `http://www.litware.com`.</span></span>
6. <span data-ttu-id="b1f6b-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-116">Click Save.</span></span>
7. <span data-ttu-id="b1f6b-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="b1f6b-118">Pasirinkti kaip aktyvų teikėją</span><span class="sxs-lookup"><span data-stu-id="b1f6b-118">Select as an active provider</span></span>
1. <span data-ttu-id="b1f6b-119">Pasirinkite teikėją „Litware, Inc.“.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="b1f6b-120">Spustelėkite Nustatyti kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="b1f6b-120">Click Set active.</span></span>


