---
title: "Finansinių ataskaitų duomenų srities nustatymas iš naujo"
description: "Šioje temoje aprašoma, kaip iš naujo nustatyti finansinių ataskaitų duomenų sritį."
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: lt-lt
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="2277a-103">Finansinių ataskaitų duomenų srities nustatymas iš naujo</span><span class="sxs-lookup"><span data-stu-id="2277a-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2277a-104">Šioje temoje aiškinama, kaip iš naujo nustatyti finansinių ataskaitų duomenų sritį naudojant šias versijas:</span><span class="sxs-lookup"><span data-stu-id="2277a-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="2277a-105">„Microsoft Dynamics 365 for Finance and Operations‟ finansinių ataskaitų leidimas 7.2.6.0 ir naujesnė versija</span><span class="sxs-lookup"><span data-stu-id="2277a-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="2277a-106">„Microsoft Dynamics 365 for Finance and Operations‟ finansinių ataskaitų leidimas 7.0.10000.4 ir naujesnė versija</span><span class="sxs-lookup"><span data-stu-id="2277a-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="2277a-107">„Microsoft Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidimas (vietinis)</span><span class="sxs-lookup"><span data-stu-id="2277a-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="2277a-108">Norėdami gauti „Finance and Operations“ finansinių ataskaitų leidimą 7.2.6.0, galite atsisiųsti KB 4052514 iš <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.</span><span class="sxs-lookup"><span data-stu-id="2277a-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="2277a-109">„Finance and Operations“ finansinių ataskaitų leidimo 7.2.6.0 ir naujesnės versijos finansinių ataskaitų duomenų srities nustatymas iš naujo</span><span class="sxs-lookup"><span data-stu-id="2277a-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="2277a-110">Finansinių ataskaitų duomenų srities nustatymas iš naujo ataskaitų kūrimo įrankyje</span><span class="sxs-lookup"><span data-stu-id="2277a-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="2277a-111">Šio proceso veiksmai palaikomi „Finance and Operations“ finansinių ataskaitų leidime 7.2.6.0 ir naujesnėse versijose.</span><span class="sxs-lookup"><span data-stu-id="2277a-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="2277a-112">Jei turite ankstesnį leidimą, kreipkitės pagalbos į palaikymo komandą.</span><span class="sxs-lookup"><span data-stu-id="2277a-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="2277a-113">Konkrečiais atvejais gali tekti iš naujo nustatyti finansinių ataskaitų duomenų sritį.</span><span class="sxs-lookup"><span data-stu-id="2277a-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="2277a-114">Galite atlikti šią užduotį naudodami ataskaitų kūrimo įrankio klientą.</span><span class="sxs-lookup"><span data-stu-id="2277a-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="2277a-115">Čia pateikti kai kurie atvejai, kai gali teikti iš naujo nustatyti duomenų sritį:</span><span class="sxs-lookup"><span data-stu-id="2277a-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="2277a-116">„Finance and Operations“ duomenų bazė buvo atkurta, tačiau nebuvo atkurta duomenų srities duomenų bazė.</span><span class="sxs-lookup"><span data-stu-id="2277a-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="2277a-117">Matote neteisingus laikotarpio duomenis.</span><span class="sxs-lookup"><span data-stu-id="2277a-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="2277a-118">Palaikymo komanda nurodo nustatyti duomenų sritį iš naujo kaip dalį trikčių šalinimo veiksmo.</span><span class="sxs-lookup"><span data-stu-id="2277a-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="2277a-119">Duomenų srities nustatymą iš naujo reikėtų atlikti tik tuo metu, kai duomenų bazėje duomenų apdorojama nedaug.</span><span class="sxs-lookup"><span data-stu-id="2277a-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="2277a-120">Nustatant iš naujo, finansinės ataskaitų bus nepasiekiamos.</span><span class="sxs-lookup"><span data-stu-id="2277a-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="2277a-121">Duomenų srities nustatymas iš naujo</span><span class="sxs-lookup"><span data-stu-id="2277a-121">Reset the data mart</span></span>

<span data-ttu-id="2277a-122">Norėdami iš naujo nustatyti duomenų sritį, ataskaitos kūrimo priemonės meniu **Įrankiai** pasirinkite **Iš naujo nustatyti duomenų sritį**.</span><span class="sxs-lookup"><span data-stu-id="2277a-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="2277a-123">Pasirodžiusiame dialogo lange yra dvi dalys: **Statistika** ir **Nustatyti iš naujo**.</span><span class="sxs-lookup"><span data-stu-id="2277a-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="2277a-124">[![Dialogo langas Nustatyti duomenų sritį iš naujo](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="2277a-124">[![Reset Data Mart dialog box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="2277a-125">Integravimo bandymai</span><span class="sxs-lookup"><span data-stu-id="2277a-125">Integration attempts</span></span>

<span data-ttu-id="2277a-126">Tinklelis **Integravimo bandymai** rodo, kiek kartų sistema bandė integruoti operacijas.</span><span class="sxs-lookup"><span data-stu-id="2277a-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="2277a-127">Jei keletas pirmų bandymų yra nesėkmingi, keletą dienų sistema toliau bando integruoti duomenis.</span><span class="sxs-lookup"><span data-stu-id="2277a-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="2277a-128">Žinosite, kad duomenų sritį reikės nustatyti iš naujo, jei bandymų skaičius yra 8 arba daugiau ir jei yra daug dimensijų kombinacijų arba operacijų įrašų.</span><span class="sxs-lookup"><span data-stu-id="2277a-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="2277a-129">Tokiu atveju duomenys į ataskaitą nebus įtraukiami.</span><span class="sxs-lookup"><span data-stu-id="2277a-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="2277a-130">Duomenų būsena</span><span class="sxs-lookup"><span data-stu-id="2277a-130">Data status</span></span>

<span data-ttu-id="2277a-131">Tinklelyje **Duomenų būsena** apžvelgiamos operacijos, valiutų kursai ir dimensijų reikšmės duomenų srityje.</span><span class="sxs-lookup"><span data-stu-id="2277a-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="2277a-132">Daug senų įrašų reiškia, kad įrašai buvo atnaujinti daug kartų.</span><span class="sxs-lookup"><span data-stu-id="2277a-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="2277a-133">Dėl to ataskaitų generavimas gali sulėtėti.</span><span class="sxs-lookup"><span data-stu-id="2277a-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="2277a-134">Nesulygiuotos pagrindinės sąskaitos kategorijos</span><span class="sxs-lookup"><span data-stu-id="2277a-134">Misaligned main account categories</span></span>

<span data-ttu-id="2277a-135">Jei naudojate leidimą, kuris yra ankstesnis nei „Microsoft Dynamics 365 for Finance and Operations“ finansinių ataskaitų leidimas 7.2.1, gali tekti nustatyti duomenų sritį iš naujo, jei pervardijate sąskaitas ir perkeliate sąskaitas iš vienos kategorijos į kitą.</span><span class="sxs-lookup"><span data-stu-id="2277a-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="2277a-136">Dėl šių veiksmų pagrindinės sąskaitos kategorijos gali tapti nesulygiuotos.</span><span class="sxs-lookup"><span data-stu-id="2277a-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="2277a-137">Laukas **Nesulygiuotos pagrindinės sąskaitos kategorijos** rodo, ar susiduriate su ta problema.</span><span class="sxs-lookup"><span data-stu-id="2277a-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="2277a-138">„Finance and Operations“ finansinių ataskaitų leidimo 7.2.6.0 duomenų srities nustatymas iš naujo</span><span class="sxs-lookup"><span data-stu-id="2277a-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="2277a-139">Norėdami nustatyti „Finance and Operations“ finansinių ataskaitų leidimo 7.2.6.0 duomenų sritį iš naujo, dialogo lange **Nustatyti duomenų sritį iš naujo** pasirinkite žymės langelį **Nustatyti duomenų sritį iš naujo** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2277a-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="2277a-140">Iš naujo nustatykite duomenų sritį tik suplanuotos prastovos metu.</span><span class="sxs-lookup"><span data-stu-id="2277a-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="2277a-141">[![Žymės langelis Nustatyti duomenų sritį iš naujo](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="2277a-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="2277a-142">„Microsoft Dynamics 365 for Finance and Operations“ finansinių ataskaitų leidimo 7.3.0 duomenų srities nustatymas iš naujo ir priežasties pasirinkimas</span><span class="sxs-lookup"><span data-stu-id="2277a-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="2277a-143">Jei nustatote, kad duomenų srities nustatymas iš naujo yra būtinas, pažymėkite žymės langelį **Nustatyti duomenų sritį iš naujo** ir pasirinkite priežastį lauke **Priežastis**.</span><span class="sxs-lookup"><span data-stu-id="2277a-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="2277a-144">Galimos toliau nurodytos parinktys.</span><span class="sxs-lookup"><span data-stu-id="2277a-144">The following options are available:</span></span>

- <span data-ttu-id="2277a-145">**Trūksta duomenų arba jie neteisingi**: remdamiesi statistika nustatėte, kad gali trūkti duomenų.</span><span class="sxs-lookup"><span data-stu-id="2277a-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="2277a-146">Prieš tęsiant, rekomenduojame dirbti su palaikymo tarnyba, kad būtų nustatyta pagrindinė priežastis.</span><span class="sxs-lookup"><span data-stu-id="2277a-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="2277a-147">**Duomenų bazės atkūrimas**: „Finance and Operations“ duomenų bazė buvo atkurta, tačiau nebuvo atkurta finansinių ataskaitų duomenų srities duomenų bazė.</span><span class="sxs-lookup"><span data-stu-id="2277a-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="2277a-148">**Kita**: iš naujo nustatote duomenų sritį dėl kitos priežasties.</span><span class="sxs-lookup"><span data-stu-id="2277a-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="2277a-149">Jei manote, kad galėjo kilti problema, susisiekite su palaikymo tarnyba, kad problema būtų identifikuota.</span><span class="sxs-lookup"><span data-stu-id="2277a-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

<span data-ttu-id="2277a-150">[![Iš naujo nustatyti duomenų sritį](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="2277a-150">[![Reset data mart](./media/Integration.png)](./media/Integration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="2277a-151">Prieš pradėdami nustatymą iš naujo patikrinkite, ar baigtas visų duomenų srities nustatymo iš naujo užduočių pirminis įkėlimas.</span><span class="sxs-lookup"><span data-stu-id="2277a-151">Verify that all data mart reset tasks have completed an initial load before you begin a reset.</span></span> <span data-ttu-id="2277a-152">Norėdami tai patikrinti, peržiūrėkite reikšmę stulpelyje Paskutinio vykdymo laikas pasirinkdami **Įrankiai** &gt; **Integravimo būsena**.</span><span class="sxs-lookup"><span data-stu-id="2277a-152">You can confirm this by looking for a value in the Last Runtime column by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="2277a-153">Išvalyti vartotojus ir įmones</span><span class="sxs-lookup"><span data-stu-id="2277a-153">Clear users and companies</span></span>

<span data-ttu-id="2277a-154">Pažymėkite žymės langelį **Išvalyti vartotojus ir įmones**, jei atkūrėte duomenų bazę, bet tada atlikote vartotojų ar įmonių keitimų.</span><span class="sxs-lookup"><span data-stu-id="2277a-154">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="2277a-155">Pažymėti šį žymės langelį turėtų tekti retai.</span><span class="sxs-lookup"><span data-stu-id="2277a-155">You should rarely have to select this check box.</span></span>

<span data-ttu-id="2277a-156">Kai būsite pasiruošę pradėti nustatymą iš naujo, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="2277a-156">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="2277a-157">Būsite paraginti patvirtinti, kad esate pasiruošę pradėti procesą.</span><span class="sxs-lookup"><span data-stu-id="2277a-157">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="2277a-158">Atkreipkite dėmesį, kad nustatymo iš naujo metu nebus galima pasiekti finansinių ataskaitų ir pradinės duomenų integracijos, kuri atsiranda po to.</span><span class="sxs-lookup"><span data-stu-id="2277a-158">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="2277a-159">Jei norite peržiūrėti integravimo būseną, pasirinkite **Įrankiai** &gt; **Integravimo būsena**, kad pamatytumėte, kada paskutinį kartą buvo vykdoma integracija ir jos būseną.</span><span class="sxs-lookup"><span data-stu-id="2277a-159">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="2277a-160">[![Peržiūrėkite integravimo būseną.](./media/New-integration.PNG)](./media/New-integration.PNG)</span><span class="sxs-lookup"><span data-stu-id="2277a-160">[![View the status of the integration](./media/New-integration.PNG)](./media/New-integration.PNG)</span></span>

> [!NOTE]
> <span data-ttu-id="2277a-161">Nustatymas iš naujo baigtas, kai visų susiejimų būsena yra RanToCompletion ir lango Integravimo būsena apatiniame kairiajame kampe nurodyta Integravimas baigtas.</span><span class="sxs-lookup"><span data-stu-id="2277a-161">The reset is finished when all mappings show the status of RanToCompletion and the Integration Status window says “Integration complete” in the bottom-left corner.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="2277a-162">„Finance and Operations“ finansinių ataskaitų leidimo 7.0.10000.4 ir naujesnės versijos finansinių ataskaitų duomenų srities nustatymas iš naujo</span><span class="sxs-lookup"><span data-stu-id="2277a-162">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="2277a-163">Jei atkuriate „Finance and Operations“ duomenų bazę iš atsarginės kopijos arba duomenų bazės iš kitos aplinkos, atlikite šiame skyriuje nurodytus veiksmus, kad padėtumėte užtikrinti tinkamą finansinių ataskaitų nustatymo naudojimą atkurtoje „Finance and Operations“ duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="2277a-163">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="2277a-164">Šio proceso veiksmai palaikomi naudojant „Microsoft Dynamics AX“ programos versiją 7.0.1 (2016 m. gegužės mėn.) (programos versija 7.0.1265.23014 ir finansinės ataskaitos versija 7.0.10000.4) ir naujesnius leidimus.</span><span class="sxs-lookup"><span data-stu-id="2277a-164">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="2277a-165">Jei naudojate ankstesnę „Finance and Operations“ versiją, pagalbos kreipkitės į palaikymo tarnybą.</span><span class="sxs-lookup"><span data-stu-id="2277a-165">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="2277a-166">Ataskaitų aprašų eksportavimas</span><span class="sxs-lookup"><span data-stu-id="2277a-166">Export report definitions</span></span>

<span data-ttu-id="2277a-167">Pirmiausia atlikite šiuos veiksmus, kad eksportuotumėte ataskaitų dizainus iš ataskaitų kūrimo įrankio.</span><span class="sxs-lookup"><span data-stu-id="2277a-167">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="2277a-168">Įjungę ataskaitų kūrimo įrankį pasirinkite **Įmonė** &gt; **Kūrimo blokų grupės**.</span><span class="sxs-lookup"><span data-stu-id="2277a-168">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="2277a-169">Norėdami eksportuoti, pasirinkite kūrimo blokų grupę, tada spustelėkite **Eksportuoti**.</span><span class="sxs-lookup"><span data-stu-id="2277a-169">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2277a-170">Naudojant „Finance and Operations“ palaikoma tik viena kūrimo blokų grupė – **Numatytoji**.</span><span class="sxs-lookup"><span data-stu-id="2277a-170">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="2277a-171">Pasirinkite norimus eksportuoti ataskaitos aprašus:</span><span class="sxs-lookup"><span data-stu-id="2277a-171">Select the report definitions to export:</span></span>

    - <span data-ttu-id="2277a-172">Norėdami eksportuoti visus ataskaitos aprašus ir susijusius kūrimo blokus, pasirinkite **Žymėti viską**.</span><span class="sxs-lookup"><span data-stu-id="2277a-172">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="2277a-173">Norėdami eksportuoti konkrečias ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius, pasirinkite atitinkamą skirtuką, tada pasirinkite norimus eksportuoti elementus.</span><span class="sxs-lookup"><span data-stu-id="2277a-173">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="2277a-174">Norėdami pasirinkti keletą skirtuko elementų, paspauskite ir laikykite klavišą „Ctrl“. Pažymėjus norimas eksportuoti ataskaitas, pažymimos susietos eilutės, stulpeliai, medžiai ir dimensijų rinkiniai.</span><span class="sxs-lookup"><span data-stu-id="2277a-174">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="2277a-175">Pasirinkite **Eksportuoti**.</span><span class="sxs-lookup"><span data-stu-id="2277a-175">Select **Export**.</span></span>
5. <span data-ttu-id="2277a-176">Įveskite failo pavadinimą ir pasirinkite saugią vietą, kurioje norite įrašyti eksportuotus ataskaitų aprašus.</span><span class="sxs-lookup"><span data-stu-id="2277a-176">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="2277a-177">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="2277a-177">Select **Save**.</span></span>

<span data-ttu-id="2277a-178">Failą galėsite nukopijuoti arba nusiųsti į saugią vietą.</span><span class="sxs-lookup"><span data-stu-id="2277a-178">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="2277a-179">Tokiu būdu failas vėliau gali būti importuojamas į kitą aplinką.</span><span class="sxs-lookup"><span data-stu-id="2277a-179">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="2277a-180">Informacijos apie tai, kaip naudoti „Microsoft Azure“ saugyklos abonementą, žr. [Duomenų perkėlimas naudojant „AzCopy“ komandų eilučių programą](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="2277a-180">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="2277a-181">Pasirašius „Finance and Operations“ sutartį, „Microsoft“ nesuteikia saugyklos abonemento.</span><span class="sxs-lookup"><span data-stu-id="2277a-181">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="2277a-182">Turite įsigyti saugyklos abonementą arba naudoti saugyklos abonementą iš atskiros „Azure“ prenumeratos.</span><span class="sxs-lookup"><span data-stu-id="2277a-182">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="2277a-183">Atkreipkite dėmesį į D disko elgseną „Azure“ virtualiuosiuose įrenginiuose (VM).</span><span class="sxs-lookup"><span data-stu-id="2277a-183">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="2277a-184">Visam laikui nesaugokite savo eksportuotų kūrimo blokų grupių diske D. Daugiau informacijos apie laikinuosius diskus žr. [Kaip veikia laikinasis diskas „Windows Azure“ virtualiuosiuose kompiuteriuose](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="2277a-184">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="2277a-185">Tarnybų stabdymas</span><span class="sxs-lookup"><span data-stu-id="2277a-185">Stop services</span></span>

<span data-ttu-id="2277a-186">Šios „Microsoft Windows“ tarnybos turės atvirus ryšius su „Finance and Operations“ duomenų baze.</span><span class="sxs-lookup"><span data-stu-id="2277a-186">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="2277a-187">Todėl, norėdami prisijungti prie visų aplinkos kompiuterių, turite naudoti „Microsoft“ nuotolinį darbalaukį, tada norėdami sustabdyti toliau nurodytas tarnybas – services.msc.</span><span class="sxs-lookup"><span data-stu-id="2277a-187">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="2277a-188">Žiniatinklio publikavimo tarnyba (visuose programos objektų serverių (AOS) kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="2277a-188">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="2277a-189">„Microsoft Dynamics 365 for Finance and Operations“ paketų valdymo tarnyba (tik neasmeniniuose AOS kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="2277a-189">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="2277a-190">„Management Reporter 2012“ proceso tarnyba (tik verslo įžvalgų [BI] kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="2277a-190">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="2277a-191">Nustatyti iš naujo</span><span class="sxs-lookup"><span data-stu-id="2277a-191">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="2277a-192">Naujausio MinorVersionDataUpgrade.zip paketo atsisiuntimas</span><span class="sxs-lookup"><span data-stu-id="2277a-192">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="2277a-193">Atsisiųskite naujausią MinorVersionDataUpgrade.zip paketą.</span><span class="sxs-lookup"><span data-stu-id="2277a-193">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="2277a-194">Instrukcijas, kaip rasti ir atsisiųsti duomenų naujinimo paketo versija, žr. toliau[Atsisiųskite naujausią duomenų išskleidimo naujinimo paketą](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="2277a-194">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> 

<span data-ttu-id="2277a-195">Norint atsisiųsti MinorVersionDataUpgrade.zip paketą, naujinimas nėra būtinas.</span><span class="sxs-lookup"><span data-stu-id="2277a-195">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="2277a-196">Todėl tereikia atlikti veiksmus, nurodytus šios temos skyriuje „Naujausių duomenų naujinimo diegimo paketų atsisiuntimas“.</span><span class="sxs-lookup"><span data-stu-id="2277a-196">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="2277a-197">Galite praleisti visus kitus veiksmus šioje temoje.</span><span class="sxs-lookup"><span data-stu-id="2277a-197">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="2277a-198">„Finance and Operations“ duomenų bazės scenarijų vykdymas</span><span class="sxs-lookup"><span data-stu-id="2277a-198">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="2277a-199">Vykdykite toliau nurodytus „Finance and Operations“ duomenų bazės scenarijus (ne finansinių ataskaitų duomenų bazės):</span><span class="sxs-lookup"><span data-stu-id="2277a-199">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="2277a-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="2277a-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="2277a-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="2277a-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="2277a-202">Naudojant šiuos scenarijus padedama užtikrinti, kad naudojami tinkami vartotojų, vaidmenų ir keitimų sekimo parametrai.</span><span class="sxs-lookup"><span data-stu-id="2277a-202">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="2277a-203">Paleiskite „Windows PowerShell“ komandą, kad iš naujo nustatytumėte duomenų bazę</span><span class="sxs-lookup"><span data-stu-id="2277a-203">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="2277a-204">AOS kompiuteryje paleiskite „Microsoft PowerShell“ administratoriaus teisėmis ir vykdykite toliau nurodytas komandas, kad iš naujo nustatytumėte „Finance and Operations“ ir finansinių ataskaitų integravimą.</span><span class="sxs-lookup"><span data-stu-id="2277a-204">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="2277a-205">Čia pateikiamas komandos **Reset-DatamartIntegration** parametrų paaiškinimas:</span><span class="sxs-lookup"><span data-stu-id="2277a-205">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="2277a-206">Tinkamos **-Reason** reikšmes yra **SERVICING**, **BADDATA** ir **OTHER**.</span><span class="sxs-lookup"><span data-stu-id="2277a-206">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="2277a-207">Parametras **-ReasonDetail** yra laisvos formos.</span><span class="sxs-lookup"><span data-stu-id="2277a-207">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="2277a-208">„Reason“ ir „reasonDetail“ bus įrašyti atliekant telemetriją / aplinkos stebėjimą.</span><span class="sxs-lookup"><span data-stu-id="2277a-208">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="2277a-209">Įvykdę komandas, būsite paprašyti įvesti **Y**, kad patvirtintumėte, jog norite iš naujo nustatyti duomenų bazę.</span><span class="sxs-lookup"><span data-stu-id="2277a-209">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="2277a-210">Tarnybų paleidimas iš naujo</span><span class="sxs-lookup"><span data-stu-id="2277a-210">Restart services</span></span>

<span data-ttu-id="2277a-211">Naudokite services.msc norėdami iš naujo paleisti pirmiau sustabdytas tarnybas:</span><span class="sxs-lookup"><span data-stu-id="2277a-211">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="2277a-212">Žiniatinklio tarnybos publikavimo paslauga (visuose AOS kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="2277a-212">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="2277a-213">„Microsoft Dynamics 365 for Finance and Operations“ paketų valdymo tarnyba (tik neasmeniniuose AOS kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="2277a-213">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="2277a-214">„Management Reporter 2012“ proceso tarnyba (tik BI kompiuteriuose)</span><span class="sxs-lookup"><span data-stu-id="2277a-214">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="2277a-215">Ataskaitų aprašų importavimas</span><span class="sxs-lookup"><span data-stu-id="2277a-215">Import report definitions</span></span>

<span data-ttu-id="2277a-216">Importuokite savo ataskaitos dizainus iš ataskaitų kūrimo įrankio naudodami eksportuojant sukurtą failą.</span><span class="sxs-lookup"><span data-stu-id="2277a-216">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="2277a-217">Įjungę ataskaitų kūrimo įrankį pasirinkite **Įmonė** &gt; **Kūrimo blokų grupės**.</span><span class="sxs-lookup"><span data-stu-id="2277a-217">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="2277a-218">Norėdami eksportuoti, pasirinkite kūrimo blokų grupę, tada spustelėkite **Eksportuoti**.</span><span class="sxs-lookup"><span data-stu-id="2277a-218">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2277a-219">Naudojant „Finance and Operations“ palaikoma tik viena kūrimo blokų grupė – **Numatytoji**.</span><span class="sxs-lookup"><span data-stu-id="2277a-219">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="2277a-220">Pasirinkite kūrimo bloką **Numatytasis**, tada pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="2277a-220">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="2277a-221">Pasirinkite failą, kuriame yra eksportuoti ataskaitos aprašai, tada pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="2277a-221">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="2277a-222">Dialogo lange **Importuoti** pasirinkite importuotinus ataskaitos aprašus:</span><span class="sxs-lookup"><span data-stu-id="2277a-222">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="2277a-223">Norėdami importuoti visus ataskaitos aprašus ir susijusius kūrimo blokus, pasirinkite **Žymėti viską**.</span><span class="sxs-lookup"><span data-stu-id="2277a-223">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="2277a-224">Norėdami importuoti tam tikras ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius pasirinkite importuotinas ataskaitas, eilutes, stulpelius, medžius arba dimensijų rinkinius.</span><span class="sxs-lookup"><span data-stu-id="2277a-224">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="2277a-225">Pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="2277a-225">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="2277a-226">„Finance and Operations“ (vietinės versijos) finansinių ataskaitų duomenų srities nustatymas iš naujo</span><span class="sxs-lookup"><span data-stu-id="2277a-226">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="2277a-227">Nurodykite visiems vartotojams išeiti iš ataskaitų kūrimo įrankio ir „Finance and Operations“ finansinių ataskaitų srities.</span><span class="sxs-lookup"><span data-stu-id="2277a-227">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="2277a-228">Vykdykite toliau nurodytą finansinių ataskaitų duomenų bazės (MRDB) scenarijų.</span><span class="sxs-lookup"><span data-stu-id="2277a-228">Run the following script against the Financial reporting database (MRDB).</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. <span data-ttu-id="2277a-229">Sutrumpinkite arba panaikinkite visus įrašus iš lentelės FINANCIALREPORTS „Finance and Operations“ duomenų bazėje (AXDB).</span><span class="sxs-lookup"><span data-stu-id="2277a-229">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="2277a-230">Sutrumpinkite arba panaikinkite visus įrašus iš lentelės FINANCIALREPORTVERSION, jei ši lentelė yra „Finance and Operations“ duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="2277a-230">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="2277a-231">Jei lentelės nėra „Finance and Operations“ duomenų bazėje, praleiskite šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="2277a-231">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="2277a-232">Vykdykite finansinių ataskaitų duomenų bazės scenarijų **ResetDatamart.sql**.</span><span class="sxs-lookup"><span data-stu-id="2277a-232">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="2277a-233">Šis scenarijus išjungia duomenų srities integravimą, panaikina visus duomenų srities duomenis, tada iš naujo įgalina duomenų srities integravimą.</span><span class="sxs-lookup"><span data-stu-id="2277a-233">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. <span data-ttu-id="2277a-234">Nustačius iš naujo, galite neautomatiniu būdu patikrinti duomenis, paleisdami toliau nurodytą finansinių ataskaitų duomenų bazės užklausą.</span><span class="sxs-lookup"><span data-stu-id="2277a-234">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="2277a-235">Užtikrinkite, kad visose eilutėse yra **LastRunTime** reikšmė ir kad **StateType** nustatyta kaip **5**.</span><span class="sxs-lookup"><span data-stu-id="2277a-235">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="2277a-236">**StateType** reikšmė **5** nurodo, kad duomenys buvo sėkmingai įkelti iš naujo.</span><span class="sxs-lookup"><span data-stu-id="2277a-236">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="2277a-237">Reikšmė **7** nurodo triktį.</span><span class="sxs-lookup"><span data-stu-id="2277a-237">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="2277a-238">Kartais organizacijos hierarchijos schema yra šios būsenos, kai ji vykdoma pirmą kartą.</span><span class="sxs-lookup"><span data-stu-id="2277a-238">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="2277a-239">Tačiau trikties būsena turėtų būti pašalinta automatiškai.</span><span class="sxs-lookup"><span data-stu-id="2277a-239">However, the faulted state but should be automatically resolved.</span></span>

