---
title: Mobiliojo įrenginio meniu elemento, skirto numerių lentelėms konsoliduoti, kūrimas
description: Šioje procedūroje parodoma, kaip kurti mobiliojo įrenginio meniu elementą, skirtą numerių lentelių konsolidavimui atlikti.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cc610a16f4b0e574b5d5e7f8fc9ecf1e12534645
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847308"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="bda57-103">Mobiliojo įrenginio meniu elemento, skirto numerių lentelėms konsoliduoti, kūrimas</span><span class="sxs-lookup"><span data-stu-id="bda57-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bda57-104">Šioje procedūroje parodoma, kaip kurti mobiliojo įrenginio meniu elementą, skirtą numerių lentelių konsolidavimui atlikti.</span><span class="sxs-lookup"><span data-stu-id="bda57-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="bda57-105">Tai sandėlio darbuotojams suteikia galimybę konsoliduoti prekes vienoje numerio lentelėje su tos pačios vietos prekėmis kitoje numerio lentelėje.</span><span class="sxs-lookup"><span data-stu-id="bda57-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="bda57-106">Pavyzdžiui, jie gali naudoti šią funkciją, jei abiejų darbo užsakymų paskesni paruošimo veiksmai buvo vienodi, kad darbą su sulietomis prekėmis reikėtų atlikti tik vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="bda57-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="bda57-107">Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="bda57-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="bda57-108">Užduotį paprastai turėtų atlikti sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="bda57-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="bda57-109">Ši procedūra yra skirta į 1611 „Dynamics 365 for Operations“ versiją įtrauktai funkcijai aprašyti.</span><span class="sxs-lookup"><span data-stu-id="bda57-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="bda57-110">Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai.</span><span class="sxs-lookup"><span data-stu-id="bda57-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="bda57-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bda57-111">Click New.</span></span>
3. <span data-ttu-id="bda57-112">Lauke Meniu elemento pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bda57-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="bda57-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="bda57-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="bda57-114">Lauke Režimas pasirinkite Netiesioginis.</span><span class="sxs-lookup"><span data-stu-id="bda57-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="bda57-115">Lauke Veiklos kodas pasirinkite Konsoliduoti numerių lenteles.</span><span class="sxs-lookup"><span data-stu-id="bda57-115">In the Activity code field, select 'Consolidate license plates'.</span></span>

