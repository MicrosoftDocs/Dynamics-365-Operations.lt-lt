---
title: Numatytas vykdymas
description: Šioje temoje paaiškintas numatytas vykdymas modulyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 976155b685498456952f7d715779d20191712103
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433623"
---
# <a name="scheduled-execution"></a><span data-ttu-id="d7944-103">Numatytas vykdymas</span><span class="sxs-lookup"><span data-stu-id="d7944-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d7944-104">Galite nustatyti numatytą vykdymą naudodami darbo užsakymo aptarnavimo lygius.</span><span class="sxs-lookup"><span data-stu-id="d7944-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="d7944-105">(Norėdami gauti daugiau informacijos apie darbo užsakymų aptarnavimo lygius, žr. [Aptarnavimo lygis ir aprašas](service-level-and-description.md).) Numatytas vykdymas suteikia lankstumo planuojant priežiūros darbuotojų darbą, nes galite nustatyti išsamesnius arba mažiau išsamius intervalo, per kurį turėtų būti baigtas darbo užsakymas, reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="d7944-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="d7944-106">Pavyzdžiui, priežiūros darbuotojas, kuris gamybos patalpoje užduotį atlieka greičiau, nei planuota, gali pereiti prie kitos netoliese esančios užduoties, kuri buvo suplanuota dabartinę savaitę, bet nebūtinai tą pačią dieną.</span><span class="sxs-lookup"><span data-stu-id="d7944-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="d7944-107">Šis metodas leidžia optimizuoti darbuotojų planavimą ir užduočių vykdymą.</span><span class="sxs-lookup"><span data-stu-id="d7944-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="d7944-108">Numatyto vykdymo sąranka, kuri yra susijusi su darbo užsakymais, gali būti bendra arba konkreti.</span><span class="sxs-lookup"><span data-stu-id="d7944-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="d7944-109">Galite nustatyti bendrų eilučių, kurios taikomos ne tik konkretiems darbo užsakymų tipams, turto tipams ir pan.</span><span class="sxs-lookup"><span data-stu-id="d7944-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="d7944-110">Arba galite sukurti numatyto vykdymo eilučių, kurios taikomos konkrečiam darbo užsakymo tipui, turto tipui, priežiūros užduoties tipui ir pan.</span><span class="sxs-lookup"><span data-stu-id="d7944-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="d7944-111">Pasirinkite **Turto valdymas** \> **Sąranka** \> **Darbo užsakymai** \> **Numatytas vykdymas**.</span><span class="sxs-lookup"><span data-stu-id="d7944-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="d7944-112">Pasirinkite **Naujas**, kad sukurtumėte numatyto vykdymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="d7944-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="d7944-113">Laukuose **Funkcinė vieta**, **Darbo užsakymo tipas**, **Turto tipas**, **Gamintojas**, **Modelis**, **Priežiūros užduoties tipo kategorija**, **Priežiūros užduoties tipas**, **Priežiūros užduoties tipo variantas** ir **Prekyba** pasirinkite reikiamas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="d7944-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="d7944-114">Lauke **Aptarnavimo lygis** pasirinkite darbo užsakymo aptarnavimo lygį.</span><span class="sxs-lookup"><span data-stu-id="d7944-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="d7944-115">Jei šį lauką paliksite tuščią, bus sukurta bendriausio tipo numatyto vykdymo eilutė.</span><span class="sxs-lookup"><span data-stu-id="d7944-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="d7944-116">Norėdami pamatyti bendrosios eilutės pavyzdį, žr. pirmąjį įrašą toliau pateiktoje iliustracijoje.</span><span class="sxs-lookup"><span data-stu-id="d7944-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="d7944-117">Ši eilutė leidžia konkrečiai datai ir laikui suplanuoti visus darbo užsakymus, kurių darbo užsakymo aptarnavimo lygis nenustatytas.</span><span class="sxs-lookup"><span data-stu-id="d7944-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="d7944-118">Lauke **Numatytas vykdymas** pasirinkite laiko intervalą.</span><span class="sxs-lookup"><span data-stu-id="d7944-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="d7944-119">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d7944-119">Select **Save**.</span></span>

![Numatytas vykdymas](media/20-setup-for-work-orders.png)
