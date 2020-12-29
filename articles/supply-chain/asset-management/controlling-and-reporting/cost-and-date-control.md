---
title: Kaštų ir datos valdymas
description: Šioje temoje aiškinamas kaštų ir datos valdymas turto valdyme.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 18373ff16b63ea61a3a4bc38ee7fa0b5e33154b5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4433491"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="da225-103">Kaštų ir datos valdymas</span><span class="sxs-lookup"><span data-stu-id="da225-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="da225-104">Turto valdyme galite apskaičiuoti kaštus, kad galėtumėte peržiūrėti faktinius kaštus, palygintus su turto, funkcinių vietų ir darbo užsakymų biudžeto kaštais.</span><span class="sxs-lookup"><span data-stu-id="da225-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="da225-105">Faktiniai kaštai pagrįsti užregistruotomis operacijomis.</span><span class="sxs-lookup"><span data-stu-id="da225-105">Actual costs are based on posted transactions.</span></span> 

<span data-ttu-id="da225-106">Taip galite apskaičiuoti datą, jei norite palyginti darbo užsakymų suplanuotas pradžios ir pabaigos datas su faktinėmis pradžios ir pabaigos datomis.</span><span class="sxs-lookup"><span data-stu-id="da225-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="da225-107">Turto, funkcinių vietų ir dar užsakymų kaštų valdymas</span><span class="sxs-lookup"><span data-stu-id="da225-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="da225-108">Su turtu, funkcinėmis vietomis ir darbo užsakymais susiję skaičiavimai yra beveik identiški.</span><span class="sxs-lookup"><span data-stu-id="da225-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="da225-109">Vienintelis skirtumas – atliekant turto ir funkcinių vietų skaičiavimą, į skaičiavimą galite įtraukti antrinį turtą ir antrines vietas.</span><span class="sxs-lookup"><span data-stu-id="da225-109">The only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="da225-110">Data yra operacijos, kai registracija buvo įrašyta, data.</span><span class="sxs-lookup"><span data-stu-id="da225-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="da225-111">Spustelėkite **Turto valdymas** > **Užklausos** > **Turtas** > **Turto kaštų valdymas** arba **Funkcinės vietos kaštų valdymas** arba **Turto valdymas** > **Užklausos** > **Darbo užsakymai** > **Darbo užsakymo kaštų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="da225-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="da225-112">Dialogo lange **Turto kaštų valdymas** / **Funkcinės vietos kaštų valdymas** / **Darbo užsakymo kaštų valdymas** pasirinkite skaičiuotiną laiko intervalą.</span><span class="sxs-lookup"><span data-stu-id="da225-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a time range to be calculated.</span></span>

3. <span data-ttu-id="da225-113">Jei reikia, pažymėkite finansinių matmenų rinkinį, kad jis būtų įtrauktas į skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="da225-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="da225-114">Perjungimo mygtuke **Praleisti nulį** pažymėkite Taip, jei nenorite, kad būtų rodomi nulinių kaštų rezultatai.</span><span class="sxs-lookup"><span data-stu-id="da225-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="da225-115">Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti kaštų valdymo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="da225-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="da225-116">Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinės vietos struktūra turi kelių lygių hierarchiją, visos kaštų valdymo eilutės, skirtos funkcinei vietai, bus rodomos viršuje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje patalpintų funkcinių vietų.</span><span class="sxs-lookup"><span data-stu-id="da225-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="da225-117">Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, kaštų valdymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="da225-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="da225-118">Perjungimo mygtuke **Rodyti atvirus patvirtintus** pažymėkite Taip, jei norite į skaičiavimą įtraukti tą stulpelį.</span><span class="sxs-lookup"><span data-stu-id="da225-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="da225-119">Perjungimo mygtuke **Įtraukti antrinį turtą** pasirinkite Taip, kad atskirose eilutėse būtų rodomi su antriniu turtu susiję kaštai.</span><span class="sxs-lookup"><span data-stu-id="da225-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="da225-120">Jei norite apriboti iešką, „FastTab“ konteineryje **Įtrauktini įrašai** galite pasirinkti konkretų turtą / funkcines vietas / darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="da225-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="da225-121">Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="da225-121">Click **OK** to start the calculation.</span></span>

    <span data-ttu-id="da225-122">Toliau pateiktame paveiksle rodomas dialogo langas **Turto kaštų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="da225-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

    ![Dialogo langas „Turto kaštų valdymas“](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="da225-124">Puslapyje **Turto kaštų valdymas** spustelėkite mygtukus **Grupuoti pagal**, kad būtų rodomas pageidaujamas skaičiavimo išsamumo lygis.</span><span class="sxs-lookup"><span data-stu-id="da225-124">On the **Asset cost control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="da225-125">Pažymėti mygtukai **Grupuoti pagal** yra paryškinti.</span><span class="sxs-lookup"><span data-stu-id="da225-125">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="da225-126">Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.</span><span class="sxs-lookup"><span data-stu-id="da225-126">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="da225-127">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="da225-127">Example</span></span>

<span data-ttu-id="da225-128">Toliau pateiktoje ekrano kopijoje rodomas **Turto kaštų valdymas** skaičiavimo rezultatų pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="da225-128">The screenshot below shows an example of calculation results in **Asset cost control**.</span></span>

- <span data-ttu-id="da225-129">Lauke **Originalus biudžetas** rodomi biudžeto kaštai iš darbo užsakymo prognozės.</span><span class="sxs-lookup"><span data-stu-id="da225-129">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="da225-130">Lauke **Patvirtinti kaštai** rodoma bendra išlaidų suma, kurią juridinis asmuo įsipareigojo sau sumokėti.</span><span class="sxs-lookup"><span data-stu-id="da225-130">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> 
- <span data-ttu-id="da225-131">Laukuose **Atviri patvirtinti kaštai** rodomi įsipareigojimai sumokėti už elementus, valandas ir paslaugas, kurias užsakėte arba gavote, bet neapmokėjote.</span><span class="sxs-lookup"><span data-stu-id="da225-131">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> 
- <span data-ttu-id="da225-132">Kai visos naudojimo registracijos užregistruotos, lauke **Faktiniai kaštai** rodomi susiję kaštai.</span><span class="sxs-lookup"><span data-stu-id="da225-132">The **Actual cost** field shows related costs after all consumption registrations have been posted.</span></span>

![„Turto kaštų valdymas“ skaičiavimo rezultatų pavyzdys](media/02-controlling-and-reporting.png)

<span data-ttu-id="da225-134">Kitas būdas skaičiuoti kaštus – atlikti kelis pasirinkimus **Visas turtas** arba **Aktyvus turtas**.</span><span class="sxs-lookup"><span data-stu-id="da225-134">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="da225-135">Tada skirtuke **Bendra** spustelėkite mygtuką **Kaštų valdymas**. Dialogo lange **Turto kaštų valdymas** pažymėtas turtas yra automatiškai įtraukiamas į „FastTab“ **Įtrauktini įrašai** lauką **Turtas**.</span><span class="sxs-lookup"><span data-stu-id="da225-135">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="da225-136">Spustelėkite **Gerai** ir rodomas pasirinkto turto kaštų skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="da225-136">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="da225-137">Tą pačią procedūrą galima atlikti su funkcinėmis vietomis dalyje **Visos funkcinės vietos** arba **Aktyvios funkcinės vietos** ir su darbo užsakymais dalyje **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="da225-137">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


## <a name="work-order-date-control"></a><span data-ttu-id="da225-138">Darbo užsakymo datos kontrolė</span><span class="sxs-lookup"><span data-stu-id="da225-138">Work order date control</span></span>

<span data-ttu-id="da225-139">Naudokite šį puslapį, kad galėtumėte peržiūrėti numatytas pradžios ir pabaigos datas, palygintas su darbo užsakymų pradžios ir pabaigos datomis.</span><span class="sxs-lookup"><span data-stu-id="da225-139">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="da225-140">Spustelėkite **Turto valdymas** > **Užklausos** > **Darbo užsakymai** > **Darbo užsakymo datos valdymas**.</span><span class="sxs-lookup"><span data-stu-id="da225-140">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="da225-141">Spustelėkite **Skaičiuoti**.</span><span class="sxs-lookup"><span data-stu-id="da225-141">Click **Calculate**.</span></span>

3. <span data-ttu-id="da225-142">Lauke **Funkcinė sritis** pažymėkite funkcinę vietą.</span><span class="sxs-lookup"><span data-stu-id="da225-142">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="da225-143">Laukuose **Pradžios data** ir **Pabaigos data** įveskite intervalą, kuriam norite atlikti skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="da225-143">Insert the range for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="da225-144">Bus įtraukti visi darbo užsakymai, kurių numatoma pradžios data patenka į intervalą.</span><span class="sxs-lookup"><span data-stu-id="da225-144">All work orders with expected start date within the range will be included.</span></span>

5. <span data-ttu-id="da225-145">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="da225-145">Click **OK**.</span></span>

6. <span data-ttu-id="da225-146">Spustelėkite mygtukus **Grupuoti pagal**, kad būtų rodomas pageidaujamas išsamus skaičiavimo lygis.</span><span class="sxs-lookup"><span data-stu-id="da225-146">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="da225-147">Pažymėti mygtukai **Grupuoti pagal** yra paryškinti.</span><span class="sxs-lookup"><span data-stu-id="da225-147">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="da225-148">Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.</span><span class="sxs-lookup"><span data-stu-id="da225-148">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="da225-149">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="da225-149">Example</span></span>

<span data-ttu-id="da225-150">Toliau pateiktoje ekrano kopijoje rodomas rezultatų **Darbo užsakymo datos valdymas** pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="da225-150">The screenshot below shows an example of calculation results in **Work order date control**.</span></span>

- <span data-ttu-id="da225-151">Lauke **Vid. pradžios delsa** rodomas dienų tarp darbo užsakymo suplanuotos pradžios datos, palygintos su faktine pradžios data, skirtumas.</span><span class="sxs-lookup"><span data-stu-id="da225-151">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="da225-152">Jei, pavyzdžiui, faktinė pradžios data buvo dvi dienos iki suplanuotos pradžios datos, lauke bus rodoma „-2“.</span><span class="sxs-lookup"><span data-stu-id="da225-152">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="da225-153">Lauke **Vid. pabaigos delsa** rodomas dienų tarp darbo užsakymo suplanuotos pabaigos datos, palygintos su faktine pabaigos data, skirtumas.</span><span class="sxs-lookup"><span data-stu-id="da225-153">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="da225-154">Jei, pavyzdžiui, faktinė pabaigos data buvo trys dienos iki suplanuotos pabaigos datos, lauke bus rodoma „3“.</span><span class="sxs-lookup"><span data-stu-id="da225-154">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="da225-155">Laukuose **Įvykiai** rodomas laiko nuokrypių, susijusių su darbo užsakymo suplanuota ir faktine pradžios data ir suplanuota ir faktine pradžios data, skaičius.</span><span class="sxs-lookup"><span data-stu-id="da225-155">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

![„Darbo užsakymo datos valdymas“ skaičiavimo rezultatų pavyzdys](media/03-controlling-and-reporting.png)


