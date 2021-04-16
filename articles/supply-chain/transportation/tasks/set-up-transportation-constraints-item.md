---
title: Prekės transportavimo apribojimų nustatymas
description: Šia procedūra bus nustatytas transportavimo apribojimas, kad pasirinktos prekės nebūtų galima transportuoti per pasirinktą tranzito punktą.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8488ec154412840bf88779eeffc3d4ff52aabd22
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818997"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="2b32b-103">Prekės transportavimo apribojimų nustatymas</span><span class="sxs-lookup"><span data-stu-id="2b32b-103">Set up transportation constraints for an item</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2b32b-104">Šia procedūra bus nustatytas transportavimo apribojimas, kad pasirinktos prekės nebūtų galima transportuoti per pasirinktą tranzito punktą.</span><span class="sxs-lookup"><span data-stu-id="2b32b-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="2b32b-105">Šią užduotį paprastai atlieka transportavimo koordinatorius.</span><span class="sxs-lookup"><span data-stu-id="2b32b-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="2b32b-106">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="2b32b-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="2b32b-107">Prekės apribojimo kūrimas</span><span class="sxs-lookup"><span data-stu-id="2b32b-107">Create an item constaint</span></span>
1. <span data-ttu-id="2b32b-108">Eikite į Apribojimai.</span><span class="sxs-lookup"><span data-stu-id="2b32b-108">Go to Constraints.</span></span>
2. <span data-ttu-id="2b32b-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="2b32b-109">Click New.</span></span>
3. <span data-ttu-id="2b32b-110">Lauke Prekės apribojimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2b32b-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="2b32b-111">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2b32b-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2b32b-112">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2b32b-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="2b32b-113">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2b32b-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="2b32b-114">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2b32b-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="2b32b-115">Lauke Tranzito punktas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2b32b-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="2b32b-116">Lauke Apribojimo veiksmas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="2b32b-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="2b32b-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="2b32b-117">Click Save.</span></span>
11. <span data-ttu-id="2b32b-118">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2b32b-118">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]