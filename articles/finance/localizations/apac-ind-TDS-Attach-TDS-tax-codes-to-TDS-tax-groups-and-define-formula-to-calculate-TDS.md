---
title: Pridėti TDS mokesčių kodus prie TDS mokesčių grupių ir nustatyti TDS apskaičiavimo formulę
description: Šioje temoje paaiškinama, kaip nustatyti iš šaltinio (TDS) mokesčių grupes atskaičius mokesčius ir TDS mokesčių kodus pridėti prie TDS mokesčių grupių. Norėdami skaičiuoti TDS mokesčių grupės TDS, turite nurodyti prie jos pridėtų TDS mokesčių kodų formulę.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: ec0d683153bd5ab731035159d32881fbdb352d70
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023457"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a><span data-ttu-id="23410-104">Pridėti TDS mokesčių kodus prie TDS mokesčių grupių ir nustatyti TDS apskaičiavimo formulę</span><span class="sxs-lookup"><span data-stu-id="23410-104">Attach TDS tax codes to TDS tax groups and define the formula for calculating TDS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23410-105">Šioje temoje paaiškinama, kaip nustatyti iš šaltinio (TDS) mokesčių grupes atskaičius mokesčius ir TDS mokesčių kodus pridėti prie TDS mokesčių grupių.</span><span class="sxs-lookup"><span data-stu-id="23410-105">This topic explains how to set up Tax Deducted at Source (TDS) tax groups and attach TDS tax codes to TDS tax groups.</span></span> <span data-ttu-id="23410-106">Norėdami skaičiuoti TDS mokesčių grupės TDS, turite nurodyti prie jos pridėtų TDS mokesčių kodų formulę.</span><span class="sxs-lookup"><span data-stu-id="23410-106">To calculate TDS for a TDS tax group, you must define the formula for TDS tax codes that are attached to it.</span></span>

<span data-ttu-id="23410-107">Norėdami nustatyti TDS mokesčių grupę, pridėti TDS mokesčių kodus ir nustatyti TDS skaičiavimo formulę, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="23410-107">Follow these steps to set up a TDS tax group, attach TDS tax codes to it, and define the formula for calculating TDS.</span></span>

1. <span data-ttu-id="23410-108">Pasirinkite **Mokestis \> Netiesioginiai mokesčiai \> Išskaitomas mokestis \> Išskaitomo mokesčio grupės**.</span><span class="sxs-lookup"><span data-stu-id="23410-108">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax groups**.</span></span>

    <span data-ttu-id="23410-109">[![Išskaitomo mokesčio grupių puslapis](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span><span class="sxs-lookup"><span data-stu-id="23410-109">[![Withholding tax groups page](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)</span></span>

2. <span data-ttu-id="23410-110">Norėdami sukurti **TDS** išskaitomo mokesčio grupę, veiksmų srityje pasirinkite Naujas ir įveskite reikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="23410-110">On the Action Pane, select **New** to create a withholding tax group for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="23410-111">Lauke **Mokesčio tipas** pasirinkite **TDS**.</span><span class="sxs-lookup"><span data-stu-id="23410-111">In the **Tax type** field, select **TDS**.</span></span>
4. <span data-ttu-id="23410-112">Norėdami sukurti eilutę, „FastTab” **Nustatymai** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="23410-112">On the **Setup** FastTab, select **Add** to create a line.</span></span>
5. <span data-ttu-id="23410-113">Lauke **Išskaitomo mokesčio kodas** pasirinkite TDS mokesčio kodą TDS mokesčių grupei.</span><span class="sxs-lookup"><span data-stu-id="23410-113">In the **Withholding tax code** field, select the TDS tax code for the TDS tax group.</span></span> <span data-ttu-id="23410-114">Laukelyje **Išskaitomo mokesčio pavadinimas** lauke rodomas TDS mokesčio kodo pavadinimas, o lauke **Vertė** rodoma vertė.</span><span class="sxs-lookup"><span data-stu-id="23410-114">The **Withholding tax name** field shows the name of the TDS tax code, and the **Value** field shows the value.</span></span>
6. <span data-ttu-id="23410-115">Norėdami nepaisyti ribinės ribos ir išimties ribinės vertės, nustatytos TDS mokesčio komponentui, kuris pridėtas prie TDS mokesčio kodo TDS operacijose, pažymėkite žymės langelį **Peržiūros** slenkstis.</span><span class="sxs-lookup"><span data-stu-id="23410-115">To ignore the threshold limit and exception threshold limit that are defined for the TDS tax component that is attached to the TDS tax code in TDS transactions, select the **Overlook threshold** check box.</span></span>
7. <span data-ttu-id="23410-116">Norėdami apsaugoti mokesčių grupę nuo skaičiavimo perlaidose, pasirinkite **Netaikoma** žymimą laukelį.</span><span class="sxs-lookup"><span data-stu-id="23410-116">To prevent the tax group from being calculated in transactions, select the **Exempt** check box.</span></span>
8. <span data-ttu-id="23410-117">Veiksmų srityje pasirinkite **Konstruktorius** kad atidarytumėte formulės konstruktorių, kad būtų galima nustatyti TDS mokesčių grupės TDS skaičiavimo formulę.</span><span class="sxs-lookup"><span data-stu-id="23410-117">On the Action Pane, select **Designer** to open the formula designer, so that you can define the formula for calculating TDS for the TDS tax group.</span></span> <span data-ttu-id="23410-118">Puslapyje **Konstruktorius** puslapyje, skirtuke Mokesčiai rodomi TDS mokesčių kodai, **pasirinkti** TDS mokesčių grupei.</span><span class="sxs-lookup"><span data-stu-id="23410-118">On the **Designer** page, the **Taxes** tab shows the TDS tax codes that have been selected for the TDS tax group.</span></span>

    <span data-ttu-id="23410-119">[![Konstruktoriaus puslapis](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span><span class="sxs-lookup"><span data-stu-id="23410-119">[![Designer page](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)</span></span>

9. <span data-ttu-id="23410-120">Norėdami **sukurti** eilutę, skirtuke Skaičiavimas pasirinkite **Alt+N**.</span><span class="sxs-lookup"><span data-stu-id="23410-120">On the **Calculation** tab, select **Alt+N** to create a line.</span></span> <span data-ttu-id="23410-121">ID **laukas** rodo automatiškai sugeneruotą TDS skaičiavimo prioriteto ID.</span><span class="sxs-lookup"><span data-stu-id="23410-121">The **ID** field shows the automatically generated priority ID for TDS calculation.</span></span>
10. <span data-ttu-id="23410-122">Lauke **Mokesčio kodas** pasirinkite TDS mokesčio kodą norėdami nustatyti formulę.</span><span class="sxs-lookup"><span data-stu-id="23410-122">In the **Tax code** field, select the TDS tax code to define the formula for.</span></span> <span data-ttu-id="23410-123">Visus TDS mokesčių kodus, pasirinktus TDS mokesčių grupei, galima pasirinkti šiame lauke.</span><span class="sxs-lookup"><span data-stu-id="23410-123">All the TDS tax codes that have been selected for the TDS tax group are available for selection in this field.</span></span>
11. <span data-ttu-id="23410-124">**Apmokestinamo pagrindo** lauke pasirinkite TDS skaičiavimo pagrindą:</span><span class="sxs-lookup"><span data-stu-id="23410-124">In the **Taxable basis** field, select the basis for calculating TDS:</span></span>

    - <span data-ttu-id="23410-125">**Bendra suma** – skaičiuoti TDS pagal bendrą operacijos sumą (t. y. SF sumą) naudojant mokesčio kodui nustatytą skaičiavimo išraišką.</span><span class="sxs-lookup"><span data-stu-id="23410-125">**Gross amount** – Calculate TDS based on the gross transaction amount (that is, the invoice amount) by using the calculation expression that is defined for the tax code.</span></span>
    - <span data-ttu-id="23410-126">**Neįskaitant bendros sumos**– skaičiuoti TDS remiantis skaičiavimo išraiška, nustatyta mokesčio kodui.</span><span class="sxs-lookup"><span data-stu-id="23410-126">**Excl Gross amount** – Calculate TDS based on the calculation expression that is defined for the tax code.</span></span>

    > [!NOTE]
    > <span data-ttu-id="23410-127">Laukelis **Apmokestinamas pagrindas** negali būti nustatytas į **Excl bendra suma** TDS mokesčio kodui, kurio ID prioritetas yra **1**.</span><span class="sxs-lookup"><span data-stu-id="23410-127">The **Taxable basis** field can't be set to **Excl Gross amount** for the TDS tax code that has a priority ID of **1**.</span></span>

12. <span data-ttu-id="23410-128">TDS skaičiavimas remiasi formule, kuri nurodyta kiekvieno prie TDS mokesčių grupės **pridėto mokesčio** kodo skaičiavimo išraiškos lauke.</span><span class="sxs-lookup"><span data-stu-id="23410-128">The TDS calculation is based on the formula that is defined in the **Calculation expression** field for each tax code that is attached to the TDS tax group.</span></span> <span data-ttu-id="23410-129">Rinkitės pliuso ženklą (**+**), minuso ženklą (**-**), daugybos ženklą (**\**_), ar dalybos ženklo (_*/**) mygtuką norėdami įvesti skaičiuoklės išraišką pasirinktam TDS mokesčio kodui **Skaičiavimo išraiškos** lauke.</span><span class="sxs-lookup"><span data-stu-id="23410-129">Select the plus sign (**+**), minus sign (**-**), multiplication sign (**\**_), or division sign (_*/**) button to enter the calculation expression for the selected TDS tax code in the **Calculation expression** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="23410-130">Negalima nustatyti TDS mokesčio kodo, kurio prioriteto ID **1** skaičiavimo išraiškos.</span><span class="sxs-lookup"><span data-stu-id="23410-130">No calculation expression can be defined for the TDS tax code that has a priority ID of **1**.</span></span>

13. <span data-ttu-id="23410-131">Norėdami nustatyti TDS mokesčio kodo skaičiavimo išraišką lauke Skaičiavimo išraiška, pridėkite TDS **mokesčių kodus,** kurie galimi skirtuke **Mokesčiai**. Norėdami įtraukti TDS mokesčių kodus į **skaičiavimo išraiškos** lauką, galite naudoti bet kurį iš šių metodų:</span><span class="sxs-lookup"><span data-stu-id="23410-131">To define the calculation expression for the TDS tax code in the **Calculation expression** field, add TDS tax codes that are available on the **Taxes** tab. To add TDS tax codes in the **Calculation expression** field, you can use any of the following methods:</span></span>

    - <span data-ttu-id="23410-132">Nuvilkite reikiamą mokesčio kodą iš skirtuko **Mokesčiai** į lauką **Skaičiavimo išraiška**.</span><span class="sxs-lookup"><span data-stu-id="23410-132">Drag the required tax code from the **Taxes** tab to the **Calculation expression** field.</span></span>
    - <span data-ttu-id="23410-133">Dukart pažymėkite (arba du kartus spustelėkite) reikiamą mokesčio kodą skirtuke **Mokesčiai**.</span><span class="sxs-lookup"><span data-stu-id="23410-133">Double-tap (or double-click) the required tax code on the **Taxes** tab.</span></span>
    - <span data-ttu-id="23410-134">Paspauskite ir laikykite (ar dešiniu klavišu) spauskite reikiamą mokesčio kodą **Mokesčiai** skirtuke ir tada rinkitės **Įtraukti mokesčio kodą**.</span><span class="sxs-lookup"><span data-stu-id="23410-134">Select and hold (or right-click) the required tax code on the **Taxes** tab, and then select **Add tax code**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="23410-135">Įterpti skaičiavimo išraišką prieš kiekvieną TDS mokesčio kodą.</span><span class="sxs-lookup"><span data-stu-id="23410-135">Insert a calculation expression before each TDS tax code.</span></span> <span data-ttu-id="23410-136">TDS mokesčių kodai, įtraukti į skaičiavimo išraišką, rodomi skliausteliuose (\[... \]).</span><span class="sxs-lookup"><span data-stu-id="23410-136">The TDS tax codes that have been added to the calculation expression appear in brackets (\[...\]).</span></span>

14. <span data-ttu-id="23410-137">Norėdami išvalyti skaičiavimo išraišką, nurodytą mokesčio kodui lauke **Skaičiavimo išraiška**, pasirinkite mygtuką **C**.</span><span class="sxs-lookup"><span data-stu-id="23410-137">To clear the calculation expression that is defined for a tax code in the **Calculation expression** field, select the **C** button.</span></span>
15. <span data-ttu-id="23410-138">Norėdami panaikinti įrašą skirtuke **Skaičiavimas**, pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="23410-138">To delete a record on the **Calculation** tab, select **Delete**.</span></span>
16. <span data-ttu-id="23410-139">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="23410-139">Close the page.</span></span>
