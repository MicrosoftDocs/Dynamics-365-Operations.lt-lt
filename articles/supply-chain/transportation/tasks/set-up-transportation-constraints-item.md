---
title: Prekės transportavimo apribojimų nustatymas
description: Šia procedūra bus nustatytas transportavimo apribojimas, kad pasirinktos prekės nebūtų galima transportuoti per pasirinktą tranzito punktą.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f351da832f8fa62935d09c6ce6ede277971dbbbc
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982312"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="8175e-103">Prekės transportavimo apribojimų nustatymas</span><span class="sxs-lookup"><span data-stu-id="8175e-103">Set up transportation constraints for an item</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8175e-104">Šia procedūra bus nustatytas transportavimo apribojimas, kad pasirinktos prekės nebūtų galima transportuoti per pasirinktą tranzito punktą.</span><span class="sxs-lookup"><span data-stu-id="8175e-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="8175e-105">Šią užduotį paprastai atlieka transportavimo koordinatorius.</span><span class="sxs-lookup"><span data-stu-id="8175e-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="8175e-106">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="8175e-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="8175e-107">Prekės apribojimo kūrimas</span><span class="sxs-lookup"><span data-stu-id="8175e-107">Create an item constaint</span></span>
1. <span data-ttu-id="8175e-108">Eikite į Apribojimai.</span><span class="sxs-lookup"><span data-stu-id="8175e-108">Go to Constraints.</span></span>
2. <span data-ttu-id="8175e-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="8175e-109">Click New.</span></span>
3. <span data-ttu-id="8175e-110">Lauke Prekės apribojimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8175e-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="8175e-111">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8175e-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="8175e-112">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8175e-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="8175e-113">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8175e-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="8175e-114">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8175e-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="8175e-115">Lauke Tranzito punktas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="8175e-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="8175e-116">Lauke Apribojimo veiksmas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="8175e-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="8175e-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="8175e-117">Click Save.</span></span>
11. <span data-ttu-id="8175e-118">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8175e-118">Close the page.</span></span>

