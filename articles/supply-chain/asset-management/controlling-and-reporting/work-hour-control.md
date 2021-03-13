---
title: Darbo valandų valdymas
description: Šioje temoje paaiškinamas modulio Turto valdymas darbo valandų valdymas.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc4382d72e032fdfad05f2077ffe8e41e64c6a55
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018476"
---
# <a name="work-hour-control"></a><span data-ttu-id="af3ea-103">Darbo valandų valdymas</span><span class="sxs-lookup"><span data-stu-id="af3ea-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="af3ea-104">Modulyje Turto valdymas galite apskaičiuoti valandas, kad galėtumėte apžvelgti faktines valandas, palygintas su turto, funkcinių vietų ar darbo užsakymų biudžeto valandomis.</span><span class="sxs-lookup"><span data-stu-id="af3ea-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="af3ea-105">Faktinės valandos yra pagrįstos užregistruotomis operacijomis.</span><span class="sxs-lookup"><span data-stu-id="af3ea-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="af3ea-106">Turto, funkcinių vietų ir darbo užsakymų darbo valandų valdymas</span><span class="sxs-lookup"><span data-stu-id="af3ea-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="af3ea-107">Su turtu, funkcinėmis vietomis ir darbo užsakymais susiję skaičiavimai yra beveik identiški.</span><span class="sxs-lookup"><span data-stu-id="af3ea-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="af3ea-108">Vienintelis skirtumas – skaičiuodami turto ir funkcinių vietų valandas, galite įtraukti antrinį turtą ir antrines vietas.</span><span class="sxs-lookup"><span data-stu-id="af3ea-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="af3ea-109">Data yra operacijos, kai registracija buvo įrašyta, data.</span><span class="sxs-lookup"><span data-stu-id="af3ea-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="af3ea-110">Spustelėkite **Turto valdymas** > **Užklausos** > **Turtas** > **Turto valandų valdymas** arba **Funkcinių vietų valandų valdymas** arba **Turto valdymas** > **Užklausos** > **Darbo užsakymai** > **Darbo užsakymų valandų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="af3ea-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="af3ea-111">Dialogo lange **Turto valandų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="af3ea-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="af3ea-112">Dialogo lango **Turto valandų valdymas** / **Funkcinių vietų valandų valdymas** / **Darbo užsakymų valandų valdymas** laukuose **Pradžios data** ir **Pabaigos data** pasirinkite skaičiuotiną laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="af3ea-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="af3ea-113">Jei reikia, pasirinkite, kad skaičiuojant būtų įtrauktas **finansinių dimensijų rinkinys**.</span><span class="sxs-lookup"><span data-stu-id="af3ea-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="af3ea-114">Perjungimo mygtuke **Praleisti nulį** pasirinkite Taip, jei nenorite, kad būtų rodomi nulinių valandų rezultatai.</span><span class="sxs-lookup"><span data-stu-id="af3ea-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="af3ea-115">Galite naudoti lauką **Lygis**, kad nurodytumėte, kiek išsamios informacijos, susijusios su funkcinėmis vietomis, turi būti valandų valdymo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="af3ea-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="af3ea-116">Pavyzdžiui, jei į lauką įvesite skaičių „1“, o funkcinių vietų hierarchija yra kelių lygių, visos valandų valdymo eilutės, skirtos funkcinei vietai, bus rodomos viršutiniame lygyje, todėl valandas į eilutę galėsite įtraukti iš žemesniame lygmenyje esančių funkcinių vietų.</span><span class="sxs-lookup"><span data-stu-id="af3ea-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="af3ea-117">Jei lauke **Lygis** įvesite skaičių „0“, matysite išsamų rezultatą, rodantį visų funkcinių vietų lygių, su kuriais jos yra susijusios, valandų valdymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="af3ea-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="af3ea-118">Perjungimo mygtuke **Įtraukti antrinį turtą** pasirinkite Taip, kad atskirose eilutėse būtų rodomi su antriniu turtu susiję kaštai.</span><span class="sxs-lookup"><span data-stu-id="af3ea-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="af3ea-119">Jei norite apriboti iešką, „FastTab“ konteineryje **Įtrauktini įrašai** galite pasirinkti konkretų turtą / funkcines vietas / darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="af3ea-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="af3ea-120">Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="af3ea-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="af3ea-121">Puslapyje **Turto valandų valdymas** spustelėkite mygtukus **Grupuoti pagal**, kad būtų rodomas pageidaujamas skaičiavimo išsamumo lygis.</span><span class="sxs-lookup"><span data-stu-id="af3ea-121">On the **Asset hour control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="af3ea-122">Pažymėti mygtukai **Grupuoti pagal** yra paryškinti.</span><span class="sxs-lookup"><span data-stu-id="af3ea-122">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="af3ea-123">Norėdami suaktyvinti arba išjungti, spustelėkite mygtuką.</span><span class="sxs-lookup"><span data-stu-id="af3ea-123">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="af3ea-124">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="af3ea-124">Example</span></span>

<span data-ttu-id="af3ea-125">Toliau pateiktoje ekrano kopijoje rodomas **Turto valandų valdymas** skaičiavimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="af3ea-125">The screenshot below shows an example of an **Asset hour control** calculation.</span></span>

- <span data-ttu-id="af3ea-126">Lauke **Pradinis biudžetas** rodomos biudžeto valandos iš darbo užsakymo prognozės.</span><span class="sxs-lookup"><span data-stu-id="af3ea-126">The **Original budget** field shows budget hours from the work order forecast.</span></span> 
- <span data-ttu-id="af3ea-127">Lauke **Faktinės valandos** rodomos darbo užsakymuose užregistruotos valandos.</span><span class="sxs-lookup"><span data-stu-id="af3ea-127">The **Actual hours** field shows posted hours on work orders.</span></span> 
- <span data-ttu-id="af3ea-128">Lauke **Skirtos valandos** rodomos visos valandos, kurias jūsų įmonė skyrė pagal darbo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="af3ea-128">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

![Turto valandų valdymo skaičiavimo pavyzdys](media/04-controlling-and-reporting.png)

<span data-ttu-id="af3ea-130">Kitas būdas skaičiuoti valandas – atlikti kelis pasirinkimus srityse **Visas turtas** arba **Aktyvus turtas**.</span><span class="sxs-lookup"><span data-stu-id="af3ea-130">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="af3ea-131">Tada spustelėkite mygtuką **Valandų valdymas**, esantį „FastTab“ **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="af3ea-131">Then you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="af3ea-132">Pasirinktas turtas automatiškai įterpiamas į „FastTab“ **Įtrauktini įrašai** lauką **Turtas**.</span><span class="sxs-lookup"><span data-stu-id="af3ea-132">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="af3ea-133">Dialogo lange **Turto valandų valdymas** spustelėkite **Gerai** – bus rodomas pasirinkto turto skaičiavimas.</span><span class="sxs-lookup"><span data-stu-id="af3ea-133">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="af3ea-134">Tą pačią procedūrą galima atlikti su funkcinėmis vietomis dalyje **Visos funkcinės vietos** arba **Aktyvios funkcinės vietos** ir su darbo užsakymais dalyje **Visi darbo užsakymai** arba **Aktyvūs darbo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="af3ea-134">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


