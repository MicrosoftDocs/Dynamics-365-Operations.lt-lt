---
title: Suplanuotų darbo užsakymų pajėgumo skaičiavimas
description: Šioje temoje aiškinama, kaip skaičiuoti suplanuotų darbo užsakymų pajėgumą turto valdyme.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5a6063db7a63975f439da9f20adec07de9103014
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264903"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="473c6-103">Suplanuotų darbo užsakymų pajėgumo skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="473c6-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="473c6-104">Galite skaičiuoti suplanuotų darbo užsakymų pajėgumą, kad peržiūrėtumėte išteklių darbo pajėgumą konkrečiu laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="473c6-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="473c6-105">Galima atlikti šių išteklių skaičiavimą: priežiūros darbuotojai, darbuotojų grupės, įrankiai ir turtas.</span><span class="sxs-lookup"><span data-stu-id="473c6-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="473c6-106">Spustelėkite **Turto valdymas** > **Užklausos** > **Grafikas** > **Pajėgumas**.</span><span class="sxs-lookup"><span data-stu-id="473c6-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="473c6-107">Dialogo lango **Skaičiuoti pajėgumą** > lauke **Rodyti** pasirinkite, kurį pajėgumo tipą norite skaičiuoti: **Pajėgumas**, **Rezervuota** arba **Likutis**.</span><span class="sxs-lookup"><span data-stu-id="473c6-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: **Capacity**, **Reserved**, or **Remainder**.</span></span>

3. <span data-ttu-id="473c6-108">Perjungimo mygtuke **Praleisti nulį** pasirinkite **Taip**, jei nenorite, kad būtų rodomi nuliniai rezultatai.</span><span class="sxs-lookup"><span data-stu-id="473c6-108">Select **Yes** on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="473c6-109">Pasirinkite išteklių tipus, kurių pajėgumą norite skaičiuoti, atitinkamuose perjungimo mygtukuose **Darbuotojas**, **Priežiūros darbuotojų grupė**, **Įrankis** ir **Turtas** pasirinkdami **Taip**.</span><span class="sxs-lookup"><span data-stu-id="473c6-109">Select the resource types for which you want to calculate capacity load by selecting **Yes** on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="473c6-110">Lauke **Pradžios data** pažymėkite skaičiavimo pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="473c6-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="473c6-111">Lauke **Intervalo tipas** pasirinkite skaičiavimo intervalą: **Diena**, **Savaitė**, **Mėnuo** arba **Ketvirtis**.</span><span class="sxs-lookup"><span data-stu-id="473c6-111">In the **Interval type** field, select the interval for the calculation: **Day**, **Week**, **Month**, or **Quarter**.</span></span>

7. <span data-ttu-id="473c6-112">Lauke **Laikotarpio dažnumas** įveskite intervalų, kuriuos norite skaičiuoti, skaičių.</span><span class="sxs-lookup"><span data-stu-id="473c6-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="473c6-113">Pavyzdžiui, jei kaip intervalo tipą pasirinkote **Diena** ir lauke įvedėte skaičių „5“, bus atliktas penkių dienų nuo pradžios datos skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="473c6-113">For example, if you have selected **Day** as the interval type, and you enter the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="473c6-114">Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="473c6-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="473c6-115">Toliau esančiame paveikslėlyje pateiktas trijų savaičių pajėgumo tipo **Rezervuota** skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="473c6-115">The figure below shows the result of a calculation covering three weeks for the load type **Reserved**.</span></span>

![1 pav.](media/08-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="473c6-117">Jei skaičiavimui pasirinkote pajėgumo tipus **Pajėgumas** arba **Likutis**, jei pasirinktu laikotarpiu nebuvo rezervuota išteklių, bus rodomas tas pats rezultatas.</span><span class="sxs-lookup"><span data-stu-id="473c6-117">If you select the load types **Capacity** or **Remainder** for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="473c6-118">Informacijos apie tai, kaip skaičiuoti priežiūros grafiko eilučių ir nesuplanuotų darbo užsakymų pajėgumą, žr. [Pajėgumo skaičiavimas](../capacity-planning/calculate-capacity-load.md).</span><span class="sxs-lookup"><span data-stu-id="473c6-118">For information about how to calculate capacity load on maintenance schedule lines and not scheduled work orders, refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md).</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]