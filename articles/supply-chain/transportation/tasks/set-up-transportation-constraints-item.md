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
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 244cf7337ec856f7517a3c0c3e055a90ab65b13f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973940"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="21f3a-103">Prekės transportavimo apribojimų nustatymas</span><span class="sxs-lookup"><span data-stu-id="21f3a-103">Set up transportation constraints for an item</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="21f3a-104">Šia procedūra bus nustatytas transportavimo apribojimas, kad pasirinktos prekės nebūtų galima transportuoti per pasirinktą tranzito punktą.</span><span class="sxs-lookup"><span data-stu-id="21f3a-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="21f3a-105">Šią užduotį paprastai atlieka transportavimo koordinatorius.</span><span class="sxs-lookup"><span data-stu-id="21f3a-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="21f3a-106">Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis.</span><span class="sxs-lookup"><span data-stu-id="21f3a-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="21f3a-107">Prekės apribojimo kūrimas</span><span class="sxs-lookup"><span data-stu-id="21f3a-107">Create an item constaint</span></span>
1. <span data-ttu-id="21f3a-108">Eikite į Apribojimai.</span><span class="sxs-lookup"><span data-stu-id="21f3a-108">Go to Constraints.</span></span>
2. <span data-ttu-id="21f3a-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="21f3a-109">Click New.</span></span>
3. <span data-ttu-id="21f3a-110">Lauke Prekės apribojimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="21f3a-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="21f3a-111">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="21f3a-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="21f3a-112">Lauke Teritorija įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="21f3a-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="21f3a-113">Lauke Sandėlis įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="21f3a-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="21f3a-114">Lauke Prekės numeris įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="21f3a-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="21f3a-115">Lauke Tranzito punktas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="21f3a-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="21f3a-116">Lauke Apribojimo veiksmas pasirinkite pasirinktį.</span><span class="sxs-lookup"><span data-stu-id="21f3a-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="21f3a-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="21f3a-117">Click Save.</span></span>
11. <span data-ttu-id="21f3a-118">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="21f3a-118">Close the page.</span></span>

