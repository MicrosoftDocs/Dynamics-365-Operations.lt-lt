---
title: Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius
description: Šioje temoje paaiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigoms priskirtas naudotojas gali sukurti elektroninių ataskaitų (ER) konfigūracijos teikėją.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2c092414f058a27cde963b1e8befd41ab3d1e3c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249209"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="49997-103">Konfigūracijos teikėjų kūrimas, pažymint juos kaip aktyvius</span><span class="sxs-lookup"><span data-stu-id="49997-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="49997-104">Šioje temoje paaiškinama, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo pareigoms priskirtas naudotojas gali sukurti elektroninių ataskaitų (ER) konfigūracijos teikėją.</span><span class="sxs-lookup"><span data-stu-id="49997-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="49997-105">Kiekviena ER konfigūracija į teikėją nurodys kaip į konfigūracijos autorių.</span><span class="sxs-lookup"><span data-stu-id="49997-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="49997-106">Šiame pavyzdyje sukursite pavyzdinės įmonės „Litware, Inc“ konfigūracijų teikėją. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijų teikėjų paslaugas visos įmonės naudoja bendrai.</span><span class="sxs-lookup"><span data-stu-id="49997-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="49997-107">Kurti teikėją</span><span class="sxs-lookup"><span data-stu-id="49997-107">Create a provider</span></span>
1. <span data-ttu-id="49997-108">Viršutiniame kairiajame kampe eikite į **naršymo sritį** ir pasirinkite **Organizacijos administravimas**.</span><span class="sxs-lookup"><span data-stu-id="49997-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="49997-109">Eikite į **Darbo sritis > Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="49997-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="49997-110">Eikite į **Susiję saitai > Konfigūracijos teikėjai**.</span><span class="sxs-lookup"><span data-stu-id="49997-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="49997-111">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="49997-111">Select **New**.</span></span>
    - <span data-ttu-id="49997-112">Teikėjo įrašas turi unikalų pavadinimą ir URL.</span><span class="sxs-lookup"><span data-stu-id="49997-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="49997-113">Peržiūrėkite šio puslapio turinį ir praleiskite šią procedūrą, jei „Litware, Inc.“ (https://www.litware.com) įrašas jau egzistuoja.</span><span class="sxs-lookup"><span data-stu-id="49997-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="49997-114">Lauke Pavadinimas įveskite `Litware, Inc.`.</span><span class="sxs-lookup"><span data-stu-id="49997-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="49997-115">Lauke Interneto adresas įveskite `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="49997-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="49997-116">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="49997-116">Select **Save**.</span></span>
8. <span data-ttu-id="49997-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="49997-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="49997-118">Pasirinkti kaip aktyvų teikėją</span><span class="sxs-lookup"><span data-stu-id="49997-118">Select as an active provider</span></span>
1. <span data-ttu-id="49997-119">Pasirinkite teikėją „Litware, Inc.“.</span><span class="sxs-lookup"><span data-stu-id="49997-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="49997-120">Pasirinkite **Nustatyti kaip aktyvų**.</span><span class="sxs-lookup"><span data-stu-id="49997-120">Select **Set active**.</span></span>

![Elektroninių ataskaitų darbo srities puslapis](../media/GER-Task-ActiveProvider-1.png)
