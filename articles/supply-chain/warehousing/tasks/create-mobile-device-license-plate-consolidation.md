--- 
title: "Mobiliojo įrenginio meniu elemento, skirto numerių lentelėms konsoliduoti, kūrimas"
description: "Šioje procedūroje parodoma, kaip kurti mobiliojo įrenginio meniu elementą, skirtą numerių lentelių konsolidavimui atlikti."
author: YuyuScheller
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 4d7e1115d8a53a6667768dd5da1dc0cffded61cd
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="0e3a2-103">Mobiliojo įrenginio meniu elemento, skirto numerių lentelėms konsoliduoti, kūrimas</span><span class="sxs-lookup"><span data-stu-id="0e3a2-103">Create a mobile device menu item for license plate consolidation</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e3a2-104">Šioje procedūroje parodoma, kaip kurti mobiliojo įrenginio meniu elementą, skirtą numerių lentelių konsolidavimui atlikti.</span><span class="sxs-lookup"><span data-stu-id="0e3a2-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="0e3a2-105">Tai sandėlio darbuotojams suteikia galimybę konsoliduoti prekes vienoje numerio lentelėje su tos pačios vietos prekėmis kitoje numerio lentelėje.</span><span class="sxs-lookup"><span data-stu-id="0e3a2-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="0e3a2-106">Pavyzdžiui, jie gali naudoti šią funkciją, jei abiejų darbo užsakymų paskesni paruošimo veiksmai buvo vienodi, kad darbą su sulietomis prekėmis reikėtų atlikti tik vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="0e3a2-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="0e3a2-107">Šią procedūrą galite naudoti demonstracinių duomenų įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="0e3a2-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="0e3a2-108">Užduotį paprastai turėtų atlikti sandėlio vadovas.</span><span class="sxs-lookup"><span data-stu-id="0e3a2-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="0e3a2-109">Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.</span><span class="sxs-lookup"><span data-stu-id="0e3a2-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="0e3a2-110">Pasirinkite Sandėlio valdymas > Nustatymas > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai.</span><span class="sxs-lookup"><span data-stu-id="0e3a2-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="0e3a2-111">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0e3a2-111">Click New.</span></span>
3. <span data-ttu-id="0e3a2-112">Lauke Meniu elemento pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0e3a2-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="0e3a2-113">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0e3a2-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="0e3a2-114">Lauke Režimas pasirinkite Netiesioginis.</span><span class="sxs-lookup"><span data-stu-id="0e3a2-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="0e3a2-115">Lauke Veiklos kodas pasirinkite Konsoliduoti numerių lenteles.</span><span class="sxs-lookup"><span data-stu-id="0e3a2-115">In the Activity code field, select 'Consolidate license plates'.</span></span>


