---
title: "Moduliuose Gamybos kontrolė ir Projektų valdymo apskaita naudojamos išlaidų kategorijos"
description: "Kai kurių tipų gamybos darbą galima taikyti projekto laiko įvertinimui ir ataskaitoms. Šiame straipsnyje pateikiama informacija apie tai, kokias gamybos darbo išlaidų kategorijas turite apibrėžti gamybos ir projektų tikslais."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCategory
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 78253
ms.assetid: cfdd58a0-8afa-4a6f-a208-a76e2c162429
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 1fcc7914f2bb283a746b5e10993f91f949818473
ms.contentlocale: lt-lt
ms.lasthandoff: 07/18/2017

---

# <a name="cost-categories-used-in-production-control-and-project-management-accounting"></a><span data-ttu-id="cb011-104">Moduliuose Gamybos kontrolė ir Projektų valdymo apskaita naudojamos išlaidų kategorijos</span><span class="sxs-lookup"><span data-stu-id="cb011-104">Cost categories used in Production control and Project management accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="cb011-105">Kai kurių tipų gamybos darbą galima taikyti projekto laiko įvertinimui ir ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="cb011-105">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="cb011-106">Šiame straipsnyje pateikiama informacija apie tai, kokias gamybos darbo išlaidų kategorijas turite apibrėžti gamybos ir projektų tikslais.</span><span class="sxs-lookup"><span data-stu-id="cb011-106">This article provides information about the cost categories that you must define for these types of production work for production and project purposes.</span></span>

<span data-ttu-id="cb011-107">Kai kurių tipų gamybos darbą galima taikyti projekto laiko įvertinimui ir ataskaitoms.</span><span class="sxs-lookup"><span data-stu-id="cb011-107">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="cb011-108">Šiuo atveju gamybos ir projekto tikslais reikalinga išlaidų kategorija.</span><span class="sxs-lookup"><span data-stu-id="cb011-108">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="cb011-109">Kai gamybos ir projekto metu naudojama išlaidų kategorija, turi būti nurodyta papildoma su projektu susijusi informacija.</span><span class="sxs-lookup"><span data-stu-id="cb011-109">When a cost category is used in production and projects, additional project-related information must be defined.</span></span> <span data-ttu-id="cb011-110">Pavyzdžiui, valandinės išlaidos, kurios susijusios su projektais, gali skirtis nuo valandinių išlaidų, kurios susijusios su gamyba.</span><span class="sxs-lookup"><span data-stu-id="cb011-110">For example, the hourly costs that are associated with projects can differ from the hourly costs that are associated with production.</span></span> <span data-ttu-id="cb011-111">Naudodami puslapį **Išlaidų kategorijos** galite apibrėžti išlaidų kategoriją, naudojamą moduliuose Gamybos kontrolė ir Projektų valdymo apskaita.</span><span class="sxs-lookup"><span data-stu-id="cb011-111">You can use the **Cost categories** page to define a cost category that is used in Production control and Project management accounting.</span></span> <span data-ttu-id="cb011-112">**Pastaba.** Kaštų apskaita turi puslapį **Projektų kategorijos**, tačiau jis niekaip nesusijęs su šioje temoje aprašytomis funkcijomis.</span><span class="sxs-lookup"><span data-stu-id="cb011-112">**Note:** Cost accounting has a **Project categories** page, but this page has no relationship to the functionality that is described in this topic.</span></span> <span data-ttu-id="cb011-113">Kai išlaidų kategoriją naudojate projektuose, puslapyje **Išlaidų kategorijos** yra papildomų skirtukų, kuriuose rodoma papildoma su projektu susijusi informacija.</span><span class="sxs-lookup"><span data-stu-id="cb011-113">When you use a cost category in projects, the **Cost categories** page has additional tabs that show additional project-related information.</span></span> <span data-ttu-id="cb011-114">Ši informacija – tai kategorijų grupė, eilutės ypatybė ir DK sąskaitos, priskirtos išlaidų kategorijai.</span><span class="sxs-lookup"><span data-stu-id="cb011-114">This information includes the category group, a line property, and ledger accounts that are assigned to the cost category.</span></span>

-   <span data-ttu-id="cb011-115">Išlaidų kategorija turi būti priskirta kategorijų grupei, kuri palaiko valandinių operacijų tipą **Valandos**.</span><span class="sxs-lookup"><span data-stu-id="cb011-115">The cost category must be assigned to a category group that supports a transaction type of **Hours**.</span></span>
-   <span data-ttu-id="cb011-116">Eilutės ypatybė nurodo numatytąją informaciją apie tai, kaip galima apmokestinti nurodytą projekto laiką.</span><span class="sxs-lookup"><span data-stu-id="cb011-116">The line property indicates default information about how reported time can be charged to a project.</span></span>
-   <span data-ttu-id="cb011-117">Paprastai DK sąskaitos, susijusios su išlaidomis ir pardavimu, įprastai nurodomos pagal kategorijų grupę, kuri priskiriama išlaidų kategorijai.</span><span class="sxs-lookup"><span data-stu-id="cb011-117">Typically, the ledger accounts that are related to costs and sales are defined for the category group that is assigned to the cost category.</span></span> <span data-ttu-id="cb011-118">Tačiau specialios sąskaitos gali būti nurodytos pagal atskirą išlaidų kategoriją.</span><span class="sxs-lookup"><span data-stu-id="cb011-118">However, specific accounts can be defined for an individual cost category.</span></span>

<span data-ttu-id="cb011-119">Papildomi puslapio **Išlaidų kategorijos**mygtukai suteikia prieigą prie su projektu susijusios informacijos apie pasirinktą išlaidų kategoriją.</span><span class="sxs-lookup"><span data-stu-id="cb011-119">Additional buttons on the **Cost categories** page let you access project-related information about a selected cost category.</span></span> <span data-ttu-id="cb011-120">Pavyzdžiui, galite peržiūrėti su projektu susijusias operacijas, apibrėžti darbuotojus ar projektus, apibrėžti valandines išlaidas ir pardavimo kainas bei peržiūrėti ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="cb011-120">For example, you can view project-related transactions, define employees or projects, define hourly costs and sales prices, and view reports.</span></span>



