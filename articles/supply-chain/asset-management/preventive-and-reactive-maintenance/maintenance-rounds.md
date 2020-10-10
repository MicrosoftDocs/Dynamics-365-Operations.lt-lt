---
title: Priežiūros ciklai
description: Šioje temoje aprašomi priežiūros ciklai skiltyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRoundTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 63cb2614b2037fac1129c7d2f82a26dac41a3490
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889966"
---
# <a name="maintenance-rounds"></a><span data-ttu-id="e0b4a-103">Priežiūros ciklai</span><span class="sxs-lookup"><span data-stu-id="e0b4a-103">Maintenance rounds</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e0b4a-104">Skiltyje **Turto valdymas** galite sukurti priežiūros ciklus įvairiam turtui, kuriam būtina atlikti panašias užduotis reguliariais intervalais.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-104">In **Asset Management**, you can create maintenance rounds for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="e0b4a-105">Pavyzdžiui, sutepimo darbai arba saugos tikrinimo darbai, kurie turi būti atliekami keletui mašinų tais pačiais intervalais. </span><span class="sxs-lookup"><span data-stu-id="e0b4a-105">For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals.</span></span> <span data-ttu-id="e0b4a-106">Pirmas žingsnis – sukurti priežiūros ciklą, apimantį turtą, kuriam reikalinga tokia pati priežiūros užduoties forma.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-106">First step is to create a maintenance round, including assets that require the same form of maintenance job.</span></span> <span data-ttu-id="e0b4a-107">Kitame žingsnyje planuokite priežiūros ciklus.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-107">Next, you schedule the maintenance rounds.</span></span> <span data-ttu-id="e0b4a-108">Kai įvykdysite priežiūros ciklų grafiką, galėsite matyti visus užduoties įrašus, susijusius su ciklu, skiltyse **Visi priežiūros grafikai** ir **Atidaryti priežiūros grafiko eilutes**.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-108">When you have completed the maintenance rounds schedule, you can see all the job records relating to the round in the **All maintenance schedule** and **Open maintenance schedule lines**.</span></span>

>[!NOTE]
><span data-ttu-id="e0b4a-109">Priežiūros ciklai taip pat gali būti nustatyti funkcinėms vietoms, kuriose priežiūra atliekama funkcinėje vietoje įdiegtam turtui, kai sukuriamas pasikartojantis darbo užsakymas.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-109">Maintenance rounds can also be set up on functional locations to be completed on the assets installed on the functional location at the time of creation of the round-based work order.</span></span> <span data-ttu-id="e0b4a-110">Daugiau informacijos apie priežiūros ciklų arba funkcinių vietų sąranką žr. [Kurti funkcines vietas](../functional-locations/create-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="e0b4a-110">Refer to [Create functional locations](../functional-locations/create-functional-locations.md) for more information on the setup of maintenance rounds on functional locations.</span></span>

## <a name="set-up-a-maintenance-round"></a><span data-ttu-id="e0b4a-111">Kaip nustatyti priežiūros ciklą</span><span class="sxs-lookup"><span data-stu-id="e0b4a-111">Set up a maintenance round</span></span>

1. <span data-ttu-id="e0b4a-112">Spustelėkite **Turto valdymas** > **Sąranka** > **Prevencinė priežiūra** > **Priežiūros ciklai**.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-112">Click **Asset management** > **Setup** > **Preventive maintenance** > **Maintenance rounds**.</span></span>

2. <span data-ttu-id="e0b4a-113">Spustelėkite **Naujas**, kad sukurtumėte naują priežiūros ciklą.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-113">Click **New** to create a new maintenance round.</span></span>

3. <span data-ttu-id="e0b4a-114">Įterpkite ID lauke **Priežiūros ciklas** ir priežiūros ciklo pavadinimą lauke **Pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-114">Insert and ID in the **Maintenance round** field, and a name for the maintenance round in the **Name** field.</span></span>

4. <span data-ttu-id="e0b4a-115">Lauke **Pradžios data** pažymėkite ciklo pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-115">Select a start date for the round in the **Start date** field.</span></span>

5. <span data-ttu-id="e0b4a-116">Laukuose **Baigti per dienas** ir **Baigti per valandas** galite įterpti numatomą pabaigos datą dienomis arba valandomis.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-116">In the **Finish within days** and **Finish within hours** fields, you can insert expected end date in days or hours.</span></span> <span data-ttu-id="e0b4a-117">Numatoma pabaigos data apskaičiuojama atitinkamai kaip ir pradžios data, kuri apskaičiuojama kuriant priežiūros grafiko eilutes.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-117">The expected end date is calculated relative to the start date, which is calculated when maintenance schedule lines are created.</span></span> <span data-ttu-id="e0b4a-118">Pavyzdžiui, galite įterpti „7“ į lauką **Baigti per dienas**, kad nurodytumėte, jog susijęs darbas turi būti atliktas per savaitę nuo pradžios datos.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-118">For example, you can insert "7" in the **Finish within days** field to indicate that the related job should be completed within a week from the start date.</span></span>

6. <span data-ttu-id="e0b4a-119">Pasirinkite Taip perjungiklyje **Sukurti automatiškai**, jei darbo užsakymai, kurie kuriami iš priežiūros ciklo, turi būti sukurti automatiškai iš priežiūros grafiko eilučių.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-119">Select "Yes" on the **Auto create** toggle button if work orders should automatically be created from maintenance schedule lines that are created from this maintenance round.</span></span>

7. <span data-ttu-id="e0b4a-120">Lauke **Darbo užsakymo tipas** pasirinkite darbo užsakymo tipą, naudotiną darbo užsakymams, sukurtiems iš priežiūros ciklo.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-120">In the **Work order type** field, select the work order type to be used on work orders created from this maintenance round.</span></span>

8. <span data-ttu-id="e0b4a-121">Lauke **Aptarnavimo lygis** pasirinkite darbo užsakymo aptarnavimo lygį, naudotiną darbo užsakymams, sukurtiems iš priežiūros ciklo.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-121">In the **Service level** field, select the work order service level to be used on work orders created from this maintenance round.</span></span>

9. <span data-ttu-id="e0b4a-122">„FastTab“ **Turto eilutės** spustelėkite **Įtraukti**, kad įtrauktumėte turtą į priežiūros ciklą.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-122">On the **Asset lines** FastTab, click **Add** to add an asset to the maintenance round.</span></span>

10. <span data-ttu-id="e0b4a-123">Eilutės numeris automatiškai įterpiamas į lauką **Eilutės numeris**, nurodant turto eilės tvarką priežiūros cikle.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-123">A line number is automatically inserted in the **Line number** field to indicate the sequence of the assets in maintenance round.</span></span>

11. <span data-ttu-id="e0b4a-124">Pasirinkite turtą lauke **Turtas**.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-124">Select the asset in the **Asset** field.</span></span>

12. <span data-ttu-id="e0b4a-125">Pasirinkite priežiūros užduoties tipą turtui lauke **Priežiūros užduoties tipas**.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-125">Select the maintenance job type for the asset in the **Maintenance job type** field.</span></span>

13. <span data-ttu-id="e0b4a-126">Jei reikia, pasirinkite **Priežiūros užduoties tipo variantas** ir **Prekybos šaka**, susijusius su priežiūros užduoties tipu.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-126">If required, select **Maintenance job typ variant** and **Trade** related to the maintenance job type.</span></span>

14. <span data-ttu-id="e0b4a-127">Pažymėkite pasikartojimą (diena, savaitė ir t. t.) lauke **Laikotarpio tipas**.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-127">Select the recurrence (day, week, etc.) in the **Period type** field.</span></span>

15. <span data-ttu-id="e0b4a-128">Lauke **Laikotarpio dažnumas** įveskite priežiūros ciklo pasikartojimų skaičių.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-128">In the **Period frequency** field, insert the number of recurrences for the maintenance round.</span></span> <span data-ttu-id="e0b4a-129">Pavyzdžiui: jei lauke **Laikotarpio tipas** pasirinkote „Diena“ ir įvedėte į lauką skaičių „7“, naujos priežiūros ciklo eilutės sukuriamos kartą per savaitę kuriant prevencinės priežiūros grafikus.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-129">Example: If you have selected "Day" in the **Period type** field, and you insert the number "7" in this field, new maintenance round lines are created during preventive maintenance scheduling once a week.</span></span>

16. <span data-ttu-id="e0b4a-130">Pasirinkite pradžios datą įtrauktinam į priežiūros ciklą turtui lauke **Pradžios data**.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-130">Select a start date for the asset to be included in the maintenance round in the **Start date** field.</span></span> <span data-ttu-id="e0b4a-131">Ši data gali skirtis nuo pradžios datos, nurodytos priežiūros cikle.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-131">This date may differ from the start date set on the maintenance round.</span></span>

17. <span data-ttu-id="e0b4a-132">Pakartokite 9–16 veiksmus norėdami į priežiūros ciklą įtraukti daugiau turto.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-132">Repeat steps 9-16 to add more assets to the maintenance round.</span></span>

18. <span data-ttu-id="e0b4a-133">„FastTab“ **Funkcinės vietos eilutės** pasirinkite **Įtraukti**, kad įtrauktumėte funkcinę vietą į priežiūros ciklą.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-133">On the **Functional location lines** FastTab, click **Add** to add a functional location to the maintenance round.</span></span> <span data-ttu-id="e0b4a-134">Žr. ankstesnį susijusių laukų aprašą.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-134">Refer to the description of the related fields above.</span></span> <span data-ttu-id="e0b4a-135">Tie patys laukai yra pasiekiami kuriant turto eilutę, tačiau, jei reikia, taip pat galite funkcinei vietai parinkti **Gamintojas** ir **Modelis** reikšmes.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-135">The same fields are available as for creating an asset line, but you can also select **Manufacturer** and **Model** for a functional location, if required.</span></span> <span data-ttu-id="e0b4a-136">Jei pasirinksite tik funkcinę vietą eilutėje, bet nustatysite reikšmes **Turto tipas**, **Gamintojas**, **Modelis**, **Priežiūros darbo tipą**, **Priežiūros darbo tipo variantas** ir **Prekybos šaka**, visas, susijęs su funkcine vieta, turtas bus įtrauktas į priežiūros ciklą kuriant priežiūros grafiką.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-136">If you only select a functional location on a line, but make no selections in **Asset type**, **Manufacturer**, **Model**, **Maintenance job type**, **Maintenance job type variant** and **Trade**, all assets related to that functional location at the time of maintenance scheduling will be included in the maintenance round.</span></span>

19. <span data-ttu-id="e0b4a-137">„FastTab“ **Telkiniai** spustelėkite **Įtraukti**, kad įtrauktumėte darbo užsakymo telkinį, įtrauktiną į priežiūros ciklą.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-137">On the **Pools** FastTab, click **Add** to select a work order pool to be included in the maintenance round.</span></span> <span data-ttu-id="e0b4a-138">Keletas darbo užsakymų telkinių gali būti prijungti prie priežiūros ciklo.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-138">Several work order pools can be connected to one maintenance round.</span></span>

20. <span data-ttu-id="e0b4a-139">Įrašykite sąranką.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-139">Save your setup.</span></span>

>[!NOTE]
><span data-ttu-id="e0b4a-140">Laukai **Turtas** ir **Eilutės** yra grupėje **Išsami informacija**, kuri yra „FastTab“ **Antraštė**, ir nurodo bendrą turto ir eilučių, susijusių su pasirinktu priežiūros ciklu, skaičių.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-140">The **Assets** and **Lines** fields located in the **Details** group on the **Header** FastTab show the total number of assets and lines related to the selected maintenance round.</span></span>

<span data-ttu-id="e0b4a-141">Toliau pateiktame paveikslėlyje parodytas priežiūros ciklo, kuriame yra trys turto vienetai, pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-141">The illustration below shows and example of a maintenance round containing three assets.</span></span>

![1 pav.](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a><span data-ttu-id="e0b4a-143">Planuoti priežiūros ciklus</span><span class="sxs-lookup"><span data-stu-id="e0b4a-143">Schedule maintenance rounds</span></span>

<span data-ttu-id="e0b4a-144">Nustatę priežiūros ciklą, vykdykite grafiko užduotį, kuria planuojamos visos užduotys, susijusios su priežiūros ciklu.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-144">When you've set up a maintenance round, you run a schedule job to schedule all the jobs related to the maintenance round.</span></span>

1. <span data-ttu-id="e0b4a-145">Spustelėkite mygtukus **Turto valdymas** > **Periodiškai** > **Prevencinė priežiūra** > **Planuoti priežiūros ciklus** arba **Turto valdymas** > **Bendrieji dalykai** > **Priežiūros grafikas** > **Visi priežiūros grafikai**, arba **Atidaryti priežiūros grafiko eilutes**, arba **Atidaryti priežiūros grafiko telkinius** > pasirinkite sąraše priežiūros grafiko eilutę > **Priežiūros ciklai**.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-145">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance rounds**, or **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** > select maintenance schedule line in the list > **Maintenance rounds** button.</span></span>

2. <span data-ttu-id="e0b4a-146">Lauke **Laikotarpis** pasirinkite laikotarpio tipą, naudotiną planuojamai užduočiai.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-146">In the **Period** field, select the period type to be used for the scheduling job.</span></span>

3. <span data-ttu-id="e0b4a-147">Lauke **Laikotarpio dažnumas** įveskite laikotarpių, kuriuos norite įtraukti, skaičių.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-147">In the **Period frequency** field, insert the number of periods to be included in the scheduling job.</span></span> <span data-ttu-id="e0b4a-148">Grafiko pradžia atitinka dabartinę datą.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-148">The start of the scheduling is the current date.</span></span>

4. <span data-ttu-id="e0b4a-149">Pasirinkite Taip perjungiklyje **Sukurti automatiškai**, jei darbo užsakymas turi būti sukurtas automatiškai priežiūros ciklo pagrindu.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-149">Select "Yes" on the **Auto create** toggle button if a work order should automatically be created on the basis of a maintenance round.</span></span>

>[!NOTE]
><span data-ttu-id="e0b4a-150">Jei šiame perjungiklyje nustatyta Taip ir perjungiklyje **Kurti automatiškai** taip pat nustatyta Taip priežiūros ciklui formoje **Priežiūros ciklai**, darbo užsakymai kuriami pagal priežiūros ciklo eilutes, o priežiūros grafiko eilutės kuriamos, turinčios būseną „Darbo užsakymas sukurtas“.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-150">If this toggle button is set to "Yes", and the **Auto create** toggle button is also set to "Yes" on the maintenance round in **Maintenance rounds** form, work orders are created based on the maintenance round lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="e0b4a-151">Jei tik vienas iš perjungiklių **Kurti automatiškai** nustatytas į Taip, išplečiamajame sąraše arba skiltyje **Priežiūros ciklai**, bus sukuriamos vien būseną Sukurta turinčios priežiūros grafiko eilutės.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-151">If only one of the **Auto create** toggle buttons is set to "Yes", in this drop-down or in **Maintenance rounds**, only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="e0b4a-152">Tokiu atveju nesukuriama jokių darbo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-152">In that case, no work orders are created.</span></span>

5. <span data-ttu-id="e0b4a-153">Jei reikia, grafiko užduočiai galite pasirinkti konkrečius ciklus arba kitą pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-153">If required, you can select specific rounds or another start date for the schedule job.</span></span> <span data-ttu-id="e0b4a-154">Spustelėkite **Filtruoti** ir pridėkite reikiamų ciklų.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-154">Click **Filter**, and add the rounds to be included.</span></span>

6. <span data-ttu-id="e0b4a-155">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-155">Click **OK**.</span></span>

7. <span data-ttu-id="e0b4a-156">Dabar galite matyti priežiūros ciklų užduotis, pasirinkus **Turto valdymas** > **Bendrieji dalykai** > **Priežiūros grafikas** > **Visi priežiūros grafikai** arba **Atidaryti priežiūros grafiko eilutes**.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-156">You are now able to see the maintenance rounds jobs in **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines**.</span></span> <span data-ttu-id="e0b4a-157">Jei suplanuoti ciklai susieti su darbo užsakymų telkiniu, taip pat galite matyti priežiūros grafiko eilutes, pasirinkus **Atidaryti priežiūros grafikų telkinius**.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-157">If the scheduled rounds are connected to a work order pool, you also see maintenance schedule lines in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="e0b4a-158">Sukurtos iš ciklo priežiūros grafiko eilutės turi pirminės reikšmės tipą „Priežiūros ciklai“.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-158">Maintenance schedule lines created from a round have the reference type "Maintenance rounds".</span></span>

<span data-ttu-id="e0b4a-159">Toliau esančiuose dviejuose paveikslėliuose pavaizduota grafiko užduotis dialogo lange **Planuoti priežiūros ciklus** ir priežiūros grafiko eilutes, sukurtos naudojant **Visas priežiūros tvarkaraščius** pagal grafiko užduotį.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-159">The two illustrations below show a schedule job in the **Schedule maintenance rounds** dialog, and the maintenance schedule lines created in **All maintenance schedule** based on that schedule job.</span></span>

![2 pav.](media/14-preventive-maintenance.png)

![3 pav.](media/15-preventive-maintenance.png)

- <span data-ttu-id="e0b4a-162">Kai neautomatiniu būdu sukuriami darbo užsakymai turtui, kuriam taikoma tiekėjo garantija, rodomas dialogo langas, kad vartotojas žinotų apie garantiją.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-162">When work orders are manually created on assets that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty.</span></span> <span data-ttu-id="e0b4a-163">Darbo užsakymo kūrimas vėliau gali būti atšauktas.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-163">The creation of the work order can then be canceled.</span></span> <span data-ttu-id="e0b4a-164">Garantinis čekis neįtraukiamas automatiškai sukurtuose darbo užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-164">The check for a warranty relation is omitted for work orders that are automatically created.</span></span>  
- <span data-ttu-id="e0b4a-165">Galite nustatyti paketinę užduotį, esančią „FastTab“ **Vykdyti fone**, kad grafiko ciklai būtų vykdomi reguliariais intervalais.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-165">You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.</span></span>  
- <span data-ttu-id="e0b4a-166">Jei ciklas yra įtrauktas į kelis darbo užsakymų telkinius (žr. [Darbo užsakymų telkiniai](../work-orders/work-order-pools.md)), kiekviename įrašo telkinyje pasirinkus **Atidaryti priežiūros grafiko telkinius** rodomas vienas įrašas.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-166">If a round is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="e0b4a-167">Taip siekiama optimizuoti darbo užsakymų telkinių filtravimo parinktis.</span><span class="sxs-lookup"><span data-stu-id="e0b4a-167">This is done to optimize the filtering options for work order pools.</span></span>

