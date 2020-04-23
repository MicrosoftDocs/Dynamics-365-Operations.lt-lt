---
title: Sunaudojimo ataskaitų kūrimas
description: Šioje temoje aiškinama, kaip kurti sunaudojimo ataskaitas turto valdyme.
author: josaw1
manager: tfehr
ms.date: 08/21/2019
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
ms.openlocfilehash: d28acbccc35b3f59f9cca7236dd721a1d9bdead8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216441"
---
# <a name="create-consumption-reports"></a><span data-ttu-id="6c46c-103">Sunaudojimo ataskaitų kūrimas</span><span class="sxs-lookup"><span data-stu-id="6c46c-103">Create consumption reports</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6c46c-104">Kai sukūrėte ir užregistravote sunaudojimo registracijas darbo užsakymuose turto valdyme, prieinamos dvi ataskaitos, kuriose rodoma sunaudojimo išsami informacija.</span><span class="sxs-lookup"><span data-stu-id="6c46c-104">When you've created and posted consumption registrations on work orders in Asset Management, two reports are available to display consumption details.</span></span>


## <a name="asset-consumption-report"></a><span data-ttu-id="6c46c-105">Turto sunaudojimo ataskaita</span><span class="sxs-lookup"><span data-stu-id="6c46c-105">Asset consumption report</span></span>

<span data-ttu-id="6c46c-106">Kai užregistravote sunaudojimą darbo užsakymuose, galite atsispausdinti turto sunaudojimo ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="6c46c-106">When you have posted consumption on work orders, you can print an asset consumption report.</span></span> <span data-ttu-id="6c46c-107">Šioje ataskaitoje rodomos valandos, valandos kaštai, elemento kaštai ir užregistruotos turto išlaidos.</span><span class="sxs-lookup"><span data-stu-id="6c46c-107">The report displays hours, hour costs, item costs, and expenses posted on assets.</span></span>

1. <span data-ttu-id="6c46c-108">Spustelėkite **Turto valdymas** > **Ataskaitos** > **Turtas** > **Turto sunaudojimas**.</span><span class="sxs-lookup"><span data-stu-id="6c46c-108">Click **Asset management** > **Reports** > **Assets** > **Asset consumption**.</span></span>

2. <span data-ttu-id="6c46c-109">Dialogo lange **Turto sunaudojimas** pažymėkite parametrus ir išsamumo lygį, kurį norite matyti, atitinkamuose perjungimo mygtukuose pažymėdami **Taip** ir įterpdami funkcinės vietos lygmenį dalyje **Rodyti**.</span><span class="sxs-lookup"><span data-stu-id="6c46c-109">In the **Asset consumption** dialog, select the parameters and detail level you want to see by selecting **Yes** on the relevant toggle buttons, and inserting a functional location level in the **Show** section.</span></span>
    - <span data-ttu-id="6c46c-110">Galite naudoti lauką **Lygiai**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti turto eilutėse.</span><span class="sxs-lookup"><span data-stu-id="6c46c-110">You can use the **Levels** field to indicate how detailed you want the asset lines to be regarding functional locations.</span></span> 
    
        <span data-ttu-id="6c46c-111">Pavyzdžiui, jei lauke įvesite skaičių „1“, o funkcinės vietos struktūra yra kelių lygių, visas turtas, skirtas funkcinei vietai, bus rodomas viršuje, todėl eilutę galėsite įtraukti iš žemesniame lygmenyje esančių funkcinių vietų.</span><span class="sxs-lookup"><span data-stu-id="6c46c-111">For example, if you enter the number "1" in the field, and you have a multi-level functional location structure, all assets for a functional location will be shown on the top level, and therefore a line may be added up from functional locations located at a lower level.</span></span> 
        
        <span data-ttu-id="6c46c-112">Jei lauke **Lygiai** įrašysite skaičių „0“, matysite išsamų rezultatą, rodant visą turtą visuose funkcinių vietų lygiuose, su kuriais jis yra susijęs.</span><span class="sxs-lookup"><span data-stu-id="6c46c-112">If you enter the number "0" in the **Levels** field, you will see a detailed result showing all assets on all the functional location levels to which they are related.</span></span> 
        
    - <span data-ttu-id="6c46c-113">Perjungimo mygtuke **Viso antrinio turto suma** pažymėkite **Taip**, kad ataskaitoje matytumėte kiekvieno antrinio turto sumą.</span><span class="sxs-lookup"><span data-stu-id="6c46c-113">Select **Yes** on the **Sum on all sub assets** toggle button to see sums for each sub asset in the report.</span></span>

3. <span data-ttu-id="6c46c-114">Skyriuje **Datos** pažymėkite datos intervalą.</span><span class="sxs-lookup"><span data-stu-id="6c46c-114">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="6c46c-115">„FastTab“ **Paskirtis** pažymėkite, ar norite, kad ataskaita būtų rodoma ekrane, norite ją spausdinti ar įrašyti kaip failą arba el. laišką.</span><span class="sxs-lookup"><span data-stu-id="6c46c-115">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="6c46c-116">Jei reikia, galite pažymėti ne vieną konkretų turtą, kuris būtų rodomas ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="6c46c-116">If required, you can select specific assets to be displayed in the report.</span></span> <span data-ttu-id="6c46c-117">„FastTab“ **Įtrauktini įrašai** spustelėkite **Filtras** ir įtraukite turtą, kurį norite įtraukti į ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="6c46c-117">On the **Records to include** FastTab, click **Filter**, and add the assets you want to include in the report.</span></span>

6. <span data-ttu-id="6c46c-118">Spustelėkite **Gerai**, kad sugeneruotumėte ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="6c46c-118">Click **OK** to generate the report.</span></span>


## <a name="work-order-consumption-report"></a><span data-ttu-id="6c46c-119">Darbo užsakymo sunaudojimo ataskaita</span><span class="sxs-lookup"><span data-stu-id="6c46c-119">Work order consumption report</span></span>

<span data-ttu-id="6c46c-120">Kai užregistravote sunaudojimą darbo užsakymuose, galite atsispausdinti darbo užsakymo sunaudojimo ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="6c46c-120">When you have posted consumption on work orders, you can print a work order consumption report.</span></span> <span data-ttu-id="6c46c-121">Šioje ataskaitoje rodomos valandos, valandos kaštai, elemento kaštai ir užregistruoti darbo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="6c46c-121">The report displays hours, hour costs, item costs, and expenses posted on work orders.</span></span>

1. <span data-ttu-id="6c46c-122">Spustelėkite **Turto valdymas** > **Ataskaitos** > **Darbo užsakymai** > **Darbo užsakymo sunaudojimas**.</span><span class="sxs-lookup"><span data-stu-id="6c46c-122">Click **Asset management** > **Reports** > **Work orders** > **Work order consumption**.</span></span>

2. <span data-ttu-id="6c46c-123">Dialogo lange **Darbo užsakymo sunaudojimas** pažymėkite parametrus, kuriuos norite įtraukti į ataskaitą, dalyje **Rodyti** atitinkamuose perjungimo mygtukuose pasirinkdami **Taip**.</span><span class="sxs-lookup"><span data-stu-id="6c46c-123">In the **Work order consumption** dialog, select the parameters you want to include in the report by selecting **Yes** on the relevant toggle buttons in the **Show** section.</span></span>

3. <span data-ttu-id="6c46c-124">Skyriuje **Datos** pažymėkite datos intervalą.</span><span class="sxs-lookup"><span data-stu-id="6c46c-124">Select a date interval in the **Dates** section.</span></span>

4. <span data-ttu-id="6c46c-125">„FastTab“ **Paskirtis** pažymėkite, ar norite, kad ataskaita būtų rodoma ekrane, norite ją spausdinti ar įrašyti kaip failą arba el. laišką.</span><span class="sxs-lookup"><span data-stu-id="6c46c-125">On the **Destination** FastTab, select if you want to display the report on screen, print it, or save it as a file or email.</span></span>

5. <span data-ttu-id="6c46c-126">Jei reikia, galite pažymėti konkrečius darbo užsakymus, kurie būtų rodomi ataskaitoje.</span><span class="sxs-lookup"><span data-stu-id="6c46c-126">If required, you can select specific work orders to be displayed in the report.</span></span> <span data-ttu-id="6c46c-127">„FastTab“ **Įtrauktini įrašai** spustelėkite **Filtras** ir įtraukite darbo užsakymus, kuriuos norite įtraukti į ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="6c46c-127">On the **Records to include** FastTab, click **Filter**, and add the work orders you want to include in the report.</span></span>

6. <span data-ttu-id="6c46c-128">Spustelėkite **Gerai**, kad sugeneruotumėte ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="6c46c-128">Click **OK** to generate the report.</span></span>


>[!NOTE]
><span data-ttu-id="6c46c-129">Taip pat galite generuoti [darbo užsakymo ataskaitą](../work-orders/work-order-report.md), kurioje pateikta daugiau išsamios informacijos apie darbo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="6c46c-129">You can also generate a [work order report](../work-orders/work-order-report.md), which contains more work order details.</span></span>

