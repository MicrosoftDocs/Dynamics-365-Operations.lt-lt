---
title: Darbo užsakymo išsiuntimas
description: Šioje temoje aiškinama, kaip išsiųsti darbo užsakymą turto valdyme.
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3412b447876d5cd0b16bdbfc0a30ae1afa3e33c0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215314"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="51543-103">Darbo užsakymo išsiuntimas</span><span class="sxs-lookup"><span data-stu-id="51543-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="51543-104">Naudodami funkciją **Išsiųsti** galite suplanuoti vieną darbo užsakymą arba darbo užsakymo užduotis vienam darbuotojui.</span><span class="sxs-lookup"><span data-stu-id="51543-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="51543-105">Spustelėkite **Turto valdymas** > **Bendrieji dalykai** > **Darbo užsakymai** > **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="51543-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="51543-106">Sąraše pasirinkite darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="51543-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="51543-107">Skirtuke **Bendra** spustelėkite **Išsiųsti**.</span><span class="sxs-lookup"><span data-stu-id="51543-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="51543-108">Dialogo lange **Suplanuoti darbo užsakymą** pasirinkite darbuotoją lauke **Darbuotojas**.</span><span class="sxs-lookup"><span data-stu-id="51543-108">In the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="51543-109">Lauke **Suplanuoti valandas** galite įvesti numatomas darbo valandas tokiu atveju, kai numatomos darbo valandos skiriasi nuo prognozuojamų valandų.</span><span class="sxs-lookup"><span data-stu-id="51543-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="51543-110">Jei reikia, lauke **Suplanuota pradžia** galite redaguoti pradžios datą ir laiką.</span><span class="sxs-lookup"><span data-stu-id="51543-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="51543-111">Jei planavimo proceso metu reikia atsižvelgti į pajėgumo apribojimus, susijusius su jau suplanuotais kitų užduočių ištekliais, įsitikinkite, kad nustatytos perjungimo mygtukų **Turtas**, **Įrankis** ir **Darbuotojas** reikšmės **Taip**.</span><span class="sxs-lookup"><span data-stu-id="51543-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to **Yes**.</span></span> <span data-ttu-id="51543-112">Jei norite peržiūrėti išsamią informaciją apie planavimo procesą, pasirinkite perjungimo mygtuko **Daugiažodis** reikšmę **Taip**.</span><span class="sxs-lookup"><span data-stu-id="51543-112">If you want to see detailed information about the scheduling process, select **Yes** on the **Verbose** toggle button.</span></span> <span data-ttu-id="51543-113">Tai reiškia, kad išsami informacija apie darbo užsakymo apskaičiuotą rezultatą rodoma sistemos pranešime.</span><span class="sxs-lookup"><span data-stu-id="51543-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="51543-114">Pasirinkite perjungimo mygtuko **Nepaisyti grafiko** reikšmę **Taip**, kad nepaisytumėte uždarytų dienų kalendoriuje (taikoma turtui, darbuotojui ir įrankiams).</span><span class="sxs-lookup"><span data-stu-id="51543-114">Select **Yes** on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="51543-115">Pasirinkite perjungimo mygtuko **Nepaisyti suplanuoto vykdymo** reikšmę **Taip**, kad nepaisytumėte apribojimų, kurie gali būti pasirinkti darbo užsakyme dėl planavimo.</span><span class="sxs-lookup"><span data-stu-id="51543-115">Select **Yes** on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> 

    <span data-ttu-id="51543-116">Informacijos apie suplanuoto vykdymo sąranką ieškokite skyriuje [Suplanuotas vykdymas](../setup-for-work-orders/scheduled-execution.md).</span><span class="sxs-lookup"><span data-stu-id="51543-116">For information on the setup of scheduled execution, see the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section.</span></span>

9. <span data-ttu-id="51543-117">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="51543-117">Click **OK**.</span></span> <span data-ttu-id="51543-118">Darbo užsakymo ciklo būsena automatiškai atnaujinama į ciklo būseną **Suplanuota**, nurodyta **Turto valdymas** > **Sąranka** > **Darbo užsakymai** > **Ciklo modeliai**.</span><span class="sxs-lookup"><span data-stu-id="51543-118">The work order lifecycle state is automatically updated to the **Scheduled** lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="51543-119">Žemiau pateiktame paveikslėlyje rodomas išsiuntimo žymėjimų pavyzdys dialogo lange **Suplanuoti darbo užsakymą**.</span><span class="sxs-lookup"><span data-stu-id="51543-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![1 pav.](media/04-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="51543-121">Jei norite panaikinti darbo užsakymo grafiką, pasirinkite darbo užsakymą **Visi darbo užsakymai**, o tada spustelėkite **Panaikinti grafiką** skirtuke **Bendra**. Jei ištrinate grafiką, nepamirškite atnaujinti darbo užsakymo ciklo būsenos rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="51543-121">If you want to delete the schedule on a work order, select the work order in **All work orders**, and then click **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>

