---
title: Sukurti įrašo šabloną, kad būtų paprasčiau įvesti duomenis
description: Šioje procedūroje parodoma, kaip sukurti įrašo šabloną, kad dėl kiekvieno naujo įrašo nereikėtų tiesiogiai įvedinėti dažnai naudojamų laukų reikšmių.
author: margoc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36d14c386322adab0cc0ba9b7b47c874aefbe519
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544257"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="0216e-103">Sukurti įrašo šabloną, kad būtų paprasčiau įvesti duomenis</span><span class="sxs-lookup"><span data-stu-id="0216e-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0216e-104">Šioje procedūroje parodoma, kaip sukurti įrašo šabloną, kad dėl kiekvieno naujo įrašo nereikėtų tiesiogiai įvedinėti dažnai naudojamų laukų reikšmių.</span><span class="sxs-lookup"><span data-stu-id="0216e-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="0216e-105">Atlikdami šią procedūrą sukursite naują įrašą apie naujus nešiojamuosius kompiuterius, kurie turėtų būti įtraukti į jūsų ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="0216e-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="0216e-106">Šioje procedūroje naudojama pavyzdinė įmonė USMF.</span><span class="sxs-lookup"><span data-stu-id="0216e-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="0216e-107">Eikite į dalį Ilgalaikis turtas > Ilgalaikis turtas > Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="0216e-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="0216e-108">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="0216e-108">Click New.</span></span>
3. <span data-ttu-id="0216e-109">Lauke Ilgalaikio turto grupė įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0216e-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="0216e-110">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0216e-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="0216e-111">Pavyzdžiui, įveskite „Įmonės pagrindinis nešiojamasis kompiuteris”.</span><span class="sxs-lookup"><span data-stu-id="0216e-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="0216e-112">Lauke Ieškos pavadinimas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0216e-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="0216e-113">Pavyzdžiui, įveskite „nešiojamasis kompiuteris.”</span><span class="sxs-lookup"><span data-stu-id="0216e-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="0216e-114">Išplėskite dalį Techninė informacija.</span><span class="sxs-lookup"><span data-stu-id="0216e-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="0216e-115">Lauke Gamintojas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0216e-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="0216e-116">Lauke Modelis įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0216e-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="0216e-117">Lauke Modelio metai įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0216e-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="0216e-118">Veiksmų srityje spustelėkite Parinktys.</span><span class="sxs-lookup"><span data-stu-id="0216e-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="0216e-119">Spustelėkite Įrašo informacija.</span><span class="sxs-lookup"><span data-stu-id="0216e-119">Click Record info.</span></span>
12. <span data-ttu-id="0216e-120">Spustelėkite Vartotojo šablonas.</span><span class="sxs-lookup"><span data-stu-id="0216e-120">Click User template.</span></span>
13. <span data-ttu-id="0216e-121">Lauke Pavadinimas surinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0216e-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="0216e-122">Pavyzdžiui, įveskite „Įmonės nešiojamasis kompiuteris.”</span><span class="sxs-lookup"><span data-stu-id="0216e-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="0216e-123">Lauke Aprašas įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0216e-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="0216e-124">Pavyzdžiui, įveskite „Įmonės nešiojamasis kompiuteris”.</span><span class="sxs-lookup"><span data-stu-id="0216e-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="0216e-125">Spustelėkite GERAI.</span><span class="sxs-lookup"><span data-stu-id="0216e-125">Click OK.</span></span>
16. <span data-ttu-id="0216e-126">Spustelėkite Uždaryti.</span><span class="sxs-lookup"><span data-stu-id="0216e-126">Click Close.</span></span>

