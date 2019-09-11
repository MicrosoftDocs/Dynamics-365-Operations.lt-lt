---
title: Suplanuotų darbo užsakymų pajėgumo skaičiavimas
description: Šioje temoje aiškinama, kaip skaičiuoti suplanuotų darbo užsakymų pajėgumą turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0c0dd1e306c54d3f99b86ad6f1816d5acabe6c18
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887164"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="c9f32-103">Suplanuotų darbo užsakymų pajėgumo skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="c9f32-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="c9f32-104">Galite skaičiuoti suplanuotų darbo užsakymų pajėgumą, kad peržiūrėtumėte išteklių darbo pajėgumą konkrečiu laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="c9f32-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="c9f32-105">Galima atlikti šių išteklių skaičiavimą: priežiūros darbuotojai, darbuotojų grupės, įrankiai ir turtas.</span><span class="sxs-lookup"><span data-stu-id="c9f32-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="c9f32-106">Spustelėkite **Turto valdymas** > **Užklausos** > **Grafikas** > **Pajėgumas**.</span><span class="sxs-lookup"><span data-stu-id="c9f32-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="c9f32-107">Dialogo lango **Skaičiuoti konkretų pajėgumą** lauke **Rodyti** pažymėkite, kurį pajėgumo tipą norite skaičiuoti: Pajėgumas, Rezervuota arba Likutis.</span><span class="sxs-lookup"><span data-stu-id="c9f32-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: "Capacity", "Reserved", or "Remainder".</span></span>

3. <span data-ttu-id="c9f32-108">Perjungimo mygtuke **Praleisti nulį** pažymėkite taip, jei nenorite, kad būtų rodomi nuliniai rezultatai.</span><span class="sxs-lookup"><span data-stu-id="c9f32-108">Select "Yes" on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="c9f32-109">Pasirinkite išteklių tipus, kurių pajėgumą norite skaičiuoti, atitinkamuose perjungimo mygtukuose – **Darbuotojas**, **Priežiūros darbuotojų grupė**, **Įrankis** ir **Turtas** – pažymėdami Taip.</span><span class="sxs-lookup"><span data-stu-id="c9f32-109">Select the resource types for which you want to calculate capacity load by selecting "Yes" on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="c9f32-110">Lauke **Pradžios data** pažymėkite skaičiavimo pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="c9f32-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="c9f32-111">Lauke **Intervalo tipas** pažymėkite skaičiavimo intervalą: Diena, Savaitė, Mėnuo arba Ketvirtis.</span><span class="sxs-lookup"><span data-stu-id="c9f32-111">In the **Interval type** field, select the interval for the calculation: "Day", "Week", "Month", or "Quarter".</span></span>

7. <span data-ttu-id="c9f32-112">Lauke **Laikotarpio dažnumas** įveskite intervalų, kuriuos norite skaičiuoti, skaičių.</span><span class="sxs-lookup"><span data-stu-id="c9f32-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="c9f32-113">Pavyzdžiui, jei kaip intervalo tipą pasirinkote Diena ir lauke įvedėte skaičių 5, bus atliktas penkių dienų nuo pradžios datos skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="c9f32-113">For example, if you have selected "Day" as the interval type, and you insert the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="c9f32-114">Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="c9f32-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="c9f32-115">Paveiksle toliau pateikiamas trijų savaičių pajėgumo tipo Rezervuota skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="c9f32-115">The figure below shows the result of a calculation covering three weeks for the load type "Reserved".</span></span>

![1 pav.](media/08-work-order-scheduling.png)

>[!NOTE]
><span data-ttu-id="c9f32-117">Jei skaičiavimui pasirenkate Pajėgumas arba Likutis pajėgumo tipus, bus rodomas tas pats rezultatas, jei pasirinktu laikotarpiu nebuvo rezervuota išteklių.</span><span class="sxs-lookup"><span data-stu-id="c9f32-117">If you select the load types "Capacity" or "Remainder" for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="c9f32-118">Daugiau informacijos, kaip skaičiuoti priežiūros grafiko eilučių ir nesuplanuotų darbo užsakymų pajėgumą, žr. [Pajėgumo skaičiavimas](../capacity-planning/calculate-capacity-load.md).</span><span class="sxs-lookup"><span data-stu-id="c9f32-118">Refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md) for information on how to calculate capacity load on maintenance schedule lines and not scheduled work orders.</span></span>

