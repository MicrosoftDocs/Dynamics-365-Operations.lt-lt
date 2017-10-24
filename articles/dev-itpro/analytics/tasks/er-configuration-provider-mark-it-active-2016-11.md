--- 
title: "Konfigūracijų teikėjo sukūrimas ir pažymėjimas aktyviu elektroninėse ataskaitose (ER)"
description: "Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigoms priskirtas naudotojas gali sukurti elektroninių ataskaitų (ER) konfigūracijų teikėją."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bdb3a3857a7293828a7766b6988c123a43e0673c
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-configuration-providand-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="63ec3-103">Konfigūracijų teikėjo sukūrimas ir pažymėjimas aktyviu elektroninėse ataskaitose (ER)</span><span class="sxs-lookup"><span data-stu-id="63ec3-103">Create a configuration providand mark it as active for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="63ec3-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigoms priskirtas naudotojas gali sukurti elektroninių ataskaitų (ER) konfigūracijų teikėją.</span><span class="sxs-lookup"><span data-stu-id="63ec3-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="63ec3-105">Kiekviena ER konfigūracija į teikėją nurodys kaip į konfigūracijos autorių.</span><span class="sxs-lookup"><span data-stu-id="63ec3-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="63ec3-106">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūracijų teikėją. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijų teikėjų paslaugas visos įmonės naudoja bendrai.</span><span class="sxs-lookup"><span data-stu-id="63ec3-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="63ec3-107">Kurti teikėją</span><span class="sxs-lookup"><span data-stu-id="63ec3-107">Create a provider</span></span>
1. <span data-ttu-id="63ec3-108">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="63ec3-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="63ec3-109">Spustelėkite Konfigūracijų teikėjai.</span><span class="sxs-lookup"><span data-stu-id="63ec3-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="63ec3-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="63ec3-110">Click New.</span></span>
    * <span data-ttu-id="63ec3-111">Teikėjo įrašas turi unikalų pavadinimą ir URL.</span><span class="sxs-lookup"><span data-stu-id="63ec3-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="63ec3-112">Apžvelkite šio puslapio turinį ir praleiskite šią procedūrą, jei jau yra įrašas, skirtas Litware, Inc. (http://www.litware.com).</span><span class="sxs-lookup"><span data-stu-id="63ec3-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="63ec3-113">Lauke Pavadinimas surinkite „Litware, Inc.‟.</span><span class="sxs-lookup"><span data-stu-id="63ec3-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="63ec3-114">„Litware, Inc.‟</span><span class="sxs-lookup"><span data-stu-id="63ec3-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="63ec3-115">Lauke Interneto adresas surinkite „http://www.litware.com‟.</span><span class="sxs-lookup"><span data-stu-id="63ec3-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * <span data-ttu-id="63ec3-116">http://www.litware.com</span><span class="sxs-lookup"><span data-stu-id="63ec3-116">http://www.litware.com</span></span>  
6. <span data-ttu-id="63ec3-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="63ec3-117">Click Save.</span></span>
7. <span data-ttu-id="63ec3-118">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="63ec3-118">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="63ec3-119">Pasirinkti kaip aktyvų teikėją</span><span class="sxs-lookup"><span data-stu-id="63ec3-119">Select as an active provider</span></span>
1. <span data-ttu-id="63ec3-120">Pasirinkite teikėją „Litware, Inc.“.</span><span class="sxs-lookup"><span data-stu-id="63ec3-120">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="63ec3-121">Spustelėkite Nustatyti kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="63ec3-121">Click Set active.</span></span>


