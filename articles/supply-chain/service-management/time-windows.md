---
title: Laiko langai
description: "Galite naudoti laiko langus, kad optimizuotumėte aptarnavimo užsakymo eilučių planavimą."
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9b215e1645c0f0f60437dc363530e2af3d262c4e
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="time-windows"></a><span data-ttu-id="05b6a-103">Laiko langai</span><span class="sxs-lookup"><span data-stu-id="05b6a-103">Time windows</span></span>  

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="05b6a-104">Galite naudoti laiko langus, kad optimizuotumėte aptarnavimo užsakymo eilučių planavimą.</span><span class="sxs-lookup"><span data-stu-id="05b6a-104">You can use time windows to optimize the scheduling of service order lines.</span></span> <span data-ttu-id="05b6a-105">Galite nustatyti sistemą taip, kad ji kurtų aptarnavimo užsakymus automatiškai.</span><span class="sxs-lookup"><span data-stu-id="05b6a-105">You can set up the system so that it automatically creates service orders.</span></span> <span data-ttu-id="05b6a-106">Pagal laiko lange nurodytus kriterijus galite prijungti kuo daugiau aptarnavimo užsakymo eilučių prie kuo mažesnio skaičiaus aptarnavimo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="05b6a-106">Based on the criteria specified by a time window, you can connect as many service order lines as possible to as few service orders as possible.</span></span>

<span data-ttu-id="05b6a-107">Laiko langai nurodo, kiek toli aptarnavimo užsakymo eilutė gali būti perkelta nuo jos apskaičiuotos datos.</span><span class="sxs-lookup"><span data-stu-id="05b6a-107">Time windows specify how far a service order line can move from its calculated date.</span></span> <span data-ttu-id="05b6a-108">Apskaičiuota data yra numatyta diena, kada turi būti įvykdyta aptarnavimo užsakymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="05b6a-108">The calculated date is the date when the service order line was scheduled to occur.</span></span> <span data-ttu-id="05b6a-109">Data nustatoma pagal jos intervalo parametrus ir aptarnavimo laikotarpį, kurį nustatėte puslapyje **Aptarnavimo užsakymų kūrimas**.</span><span class="sxs-lookup"><span data-stu-id="05b6a-109">The date is based on its interval setting and the service period that you defined in the **Create service orders** page.</span></span> <span data-ttu-id="05b6a-110">Laiko langą galima nustatyti naudojant toliau pateiktoje lentelėje nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="05b6a-110">You define a time window by using the values in the following table.</span></span>

| <span data-ttu-id="05b6a-111">Metodas</span><span class="sxs-lookup"><span data-stu-id="05b6a-111">Method</span></span> | <span data-ttu-id="05b6a-112">aprašymas</span><span class="sxs-lookup"><span data-stu-id="05b6a-112">Description</span></span>                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05b6a-113">Savaitė</span><span class="sxs-lookup"><span data-stu-id="05b6a-113">Week</span></span>   | <span data-ttu-id="05b6a-114">Aptarnavimo užsakymo eilutės data gali būti perkelta į bet kurią laisvą tos pačios savaitės kaip ir pirminė apskaičiuota data dieną.</span><span class="sxs-lookup"><span data-stu-id="05b6a-114">The date that the service order line can be moved to any open day in the same week as the initial calculated date.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="05b6a-115">Mėnuo</span><span class="sxs-lookup"><span data-stu-id="05b6a-115">Month</span></span>  | <span data-ttu-id="05b6a-116">Aptarnavimo užsakymo eilutės data gali būti perkelta į bet kurią laisvą to paties mėnesio kaip ir pirminė apskaičiuota data dieną.</span><span class="sxs-lookup"><span data-stu-id="05b6a-116">The date that the service order line can be moved to any open day in the same month as the initial calculated date.</span></span> <span data-ttu-id="05b6a-117">Pavyzdžiui, aptarnavimo užsakymo eilutės apskaičiuota data yra 2017 m. vasario 15 d.</span><span class="sxs-lookup"><span data-stu-id="05b6a-117">For example, the calculated date for a service order line is February 15, 2017.</span></span> <span data-ttu-id="05b6a-118">Aptarnavimo užsakymo eilutę galima numatyti bet kurią savaitės dieną nuo 2017 m. vasario 1 d. iki vasario 28 d.</span><span class="sxs-lookup"><span data-stu-id="05b6a-118">The service order line can be scheduled for any weekday between February 1 and February 28, 2017.</span></span> |
| <span data-ttu-id="05b6a-119">Neautomatinis</span><span class="sxs-lookup"><span data-stu-id="05b6a-119">Manual</span></span> | <span data-ttu-id="05b6a-120">Galite nurodyti didžiausią dienų iki arba po pirminės apskaičiuotos datos skaičių, per kurį gali būti perkeltas aptarnavimo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="05b6a-120">You define the maximum number of days before or after the initial calculated date that the service order line can be moved.</span></span>                                                                                                                                                                           |

<span data-ttu-id="05b6a-121">Jei aptarnavimo sutarties eilutės laiko lango nenurodysite, iš aptarnavimo sutarties išvesta aptarnavimo užsakymo eilutė turės būti įvykdyta tiksliai tą dieną, kurią ji buvo numatyta iš pradžių.</span><span class="sxs-lookup"><span data-stu-id="05b6a-121">If you do not specify a time window for a service agreement line, the service order line that is derived from the service agreement must be on the exact date for which it was originally scheduled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05b6a-122">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="05b6a-122">Related topics</span></span>

[<span data-ttu-id="05b6a-123">Laiko langų kūrimas</span><span class="sxs-lookup"><span data-stu-id="05b6a-123">Create time windows</span></span>](create-time-windows.md)


