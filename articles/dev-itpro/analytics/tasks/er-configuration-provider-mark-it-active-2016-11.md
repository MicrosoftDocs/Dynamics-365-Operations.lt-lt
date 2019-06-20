---
title: Konfigūracijų teikėjų kūrimas ir jų pažymėjimas kaip aktyviais
description: Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigoms priskirtas naudotojas gali sukurti elektroninių ataskaitų (ER) konfigūracijų teikėją.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4b1cd7a02cdf4c650af50199f4425eb53cef0a8
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595400"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="ff6e8-103">Konfigūracijų teikėjų kūrimas ir jų pažymėjimas kaip aktyviais</span><span class="sxs-lookup"><span data-stu-id="ff6e8-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ff6e8-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigoms priskirtas naudotojas gali sukurti elektroninių ataskaitų (ER) konfigūracijų teikėją.</span><span class="sxs-lookup"><span data-stu-id="ff6e8-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="ff6e8-105">Kiekviena ER konfigūracija į teikėją nurodys kaip į konfigūracijos autorių.</span><span class="sxs-lookup"><span data-stu-id="ff6e8-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="ff6e8-106">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūracijų teikėją. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijų teikėjų paslaugas visos įmonės naudoja bendrai.</span><span class="sxs-lookup"><span data-stu-id="ff6e8-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="ff6e8-107">Kurti teikėją</span><span class="sxs-lookup"><span data-stu-id="ff6e8-107">Create a provider</span></span>
1. <span data-ttu-id="ff6e8-108">Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="ff6e8-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ff6e8-109">Spustelėkite Konfigūracijų teikėjai.</span><span class="sxs-lookup"><span data-stu-id="ff6e8-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="ff6e8-110">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="ff6e8-110">Click New.</span></span>
    * <span data-ttu-id="ff6e8-111">Teikėjo įrašas turi unikalų pavadinimą ir URL.</span><span class="sxs-lookup"><span data-stu-id="ff6e8-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="ff6e8-112">Peržiūrėkite šio puslapio turinį ir praleiskite šią procedūrą, jei „Litware, Inc.“ (https://www.litware.com) įrašas jau egzistuoja.</span><span class="sxs-lookup"><span data-stu-id="ff6e8-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="ff6e8-113">Lauke Pavadinimas surinkite „Litware, Inc.‟.</span><span class="sxs-lookup"><span data-stu-id="ff6e8-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="ff6e8-114">„Litware, Inc.‟</span><span class="sxs-lookup"><span data-stu-id="ff6e8-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="ff6e8-115">Lauke Interneto adresas įrašykite „https://www.litware.com“.</span><span class="sxs-lookup"><span data-stu-id="ff6e8-115">In the Internet address field, type 'https://www.litware.com'.</span></span>
    * https://www.litware.com  
6. <span data-ttu-id="ff6e8-116">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="ff6e8-116">Click Save.</span></span>
7. <span data-ttu-id="ff6e8-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ff6e8-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="ff6e8-118">Pasirinkti kaip aktyvų teikėją</span><span class="sxs-lookup"><span data-stu-id="ff6e8-118">Select as an active provider</span></span>
1. <span data-ttu-id="ff6e8-119">Pasirinkite teikėją „Litware, Inc.“.</span><span class="sxs-lookup"><span data-stu-id="ff6e8-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="ff6e8-120">Spustelėkite Nustatyti kaip aktyvų.</span><span class="sxs-lookup"><span data-stu-id="ff6e8-120">Click Set active.</span></span>

