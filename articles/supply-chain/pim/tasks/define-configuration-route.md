---
title: Apibrėžti konfigūracijos maršrutą
description: Šios procedūros tikslas yra apibrėžti konfigūracijos maršrutą, kuris nulemia konfigūracijos grupių pristatymo seką.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a6ea4abcb0a9b51680e3cdbb4533eb127b3a04a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216062"
---
# <a name="define-configuration-route"></a><span data-ttu-id="f6a0d-103">Apibrėžti konfigūracijos maršrutą</span><span class="sxs-lookup"><span data-stu-id="f6a0d-103">Define configuration route</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f6a0d-104">Šios procedūros tikslas yra apibrėžti konfigūracijos maršrutą, kuris nulemia konfigūracijos grupių pristatymo seką.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-104">This procedure focuses on defining a configuration route that determines the sequence in which the configuration groups will be presented.</span></span> <span data-ttu-id="f6a0d-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f6a0d-106">Tai yra šeštoji iš aštuonių procedūrų, kuriomis paaiškinama, kaip kurti konfigūravimo pagal dimensijas kombinacijas.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-106">This is the sixth procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="f6a0d-107">Pasirinkite Produkto informacijos valdymas > Komplektavimo specifikacijos ir formulės > Komplektavimo specifikacijos.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="f6a0d-108">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f6a0d-109">Veiksmų srityje spustelėkite Parinktys.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-109">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="f6a0d-110">Spustelėkite Keisti rodinį.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-110">Click Change view.</span></span>
5. <span data-ttu-id="f6a0d-111">Spustelėkite antraštės rodinį.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-111">Click Header view.</span></span>
6. <span data-ttu-id="f6a0d-112">Išplėskite arba sutraukite sekciją Konfigūracijos maršrutas.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-112">Expand or collapse the Configuration route section.</span></span>
7. <span data-ttu-id="f6a0d-113">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-113">Click Add.</span></span>
8. <span data-ttu-id="f6a0d-114">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="f6a0d-115">Lauke „Konfigūracijos grupė“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-115">In the Configuration group field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="f6a0d-116">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-116">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="f6a0d-117">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-117">Click Add.</span></span>
12. <span data-ttu-id="f6a0d-118">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-118">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="f6a0d-119">Lauke „Konfigūracijos grupė“ spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-119">In the Configuration group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="f6a0d-120">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-120">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="f6a0d-121">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="f6a0d-122">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="f6a0d-122">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]