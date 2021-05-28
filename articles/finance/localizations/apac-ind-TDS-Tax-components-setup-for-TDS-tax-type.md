---
title: Nustatykite komponentus TDS mokesčių tipui
description: Šioje temoje paaiškinama, kaip nustatyti šaltinio išskaitomo mokesčio komponentus priemonės mokesčių išskaitomos išskaitomo mokesčio šaltinio mokesčių tipui. Taip pat paaiškinama, kaip nustatyti ribinę ribą, naudojamą skaičiuojant kiekvieno TDS komponento TDS.
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
ms.openlocfilehash: 6e0a6a05fcb4afb8c8965e25c3089bc1b3d98431
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023443"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a><span data-ttu-id="47bd5-104">Nustatykite komponentus TDS mokesčių tipui</span><span class="sxs-lookup"><span data-stu-id="47bd5-104">Set up tax components for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47bd5-105">Šioje temoje paaiškinama, kaip nustatyti šaltinio išskaitomo mokesčio komponentus priemonės mokesčių išskaitomos išskaitomo mokesčio šaltinio mokesčių tipui.</span><span class="sxs-lookup"><span data-stu-id="47bd5-105">This topic explains how to set up withholding tax components for the Tax Deducted at Source (TDS) tax type.</span></span> <span data-ttu-id="47bd5-106">TDS komponentai yra TDS, papildomas mokestis, PE-Jaus ir SHE paslaugos.</span><span class="sxs-lookup"><span data-stu-id="47bd5-106">The TDS components are TDS, surcharge, PE-Cess, and SHE Cess.</span></span> <span data-ttu-id="47bd5-107">Taip pat temoje paaiškinama, kaip nustatyti ribinę ribą, naudojamą skaičiuojant kiekvieno TDS komponento TDS.</span><span class="sxs-lookup"><span data-stu-id="47bd5-107">This topic also explains how to define the threshold that is used to calculate TDS for each TDS component.</span></span> <span data-ttu-id="47bd5-108">Be to, galite nustatyti išimties ribinę vertę, naudojamą skaičiuojant kiekvieno TDS komponento TDS.</span><span class="sxs-lookup"><span data-stu-id="47bd5-108">Additionally, you can define an exception threshold that is used to calculate TDS for each TDS component.</span></span>

<span data-ttu-id="47bd5-109">Atlikite šiuos veiksmus TDS komponentams nustatyti.</span><span class="sxs-lookup"><span data-stu-id="47bd5-109">Follow these steps to set up TDS components.</span></span>

1. <span data-ttu-id="47bd5-110">Eikite į **Mokestis \> Nustatymai \> Išskaitomas mokestis \> Išskaitomo mokesčio komponentai**.</span><span class="sxs-lookup"><span data-stu-id="47bd5-110">Go to **Tax \> Setup \> Withholding tax \> Withholding tax components**.</span></span>

    <span data-ttu-id="47bd5-111">[![Išskaitomo mokesčio komponentų puslapis](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span><span class="sxs-lookup"><span data-stu-id="47bd5-111">[![Withholding tax components page](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)</span></span>

2. <span data-ttu-id="47bd5-112">Mokesčio **tipo lauke** pasirinkite **TDS** norėdami nustatyti TDS mokesčio tipo išskaitomo mokesčio komponentus.</span><span class="sxs-lookup"><span data-stu-id="47bd5-112">In the **Tax type** field, select **TDS** to set up withholding tax components for the TDS tax type.</span></span>
3. <span data-ttu-id="47bd5-113">Veiksmų srityje pasirinkite **Nauja** eilutei sukurti.</span><span class="sxs-lookup"><span data-stu-id="47bd5-113">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="47bd5-114">Lauke **Išskaitomo mokesčio komponentas** įveskite TDS komponento pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="47bd5-114">In the **Withholding tax component** field, enter a name for the TDS component.</span></span>
5. <span data-ttu-id="47bd5-115">Lauke **Išskaitomo mokesčio komponentų grupė** pasirinkite TDS išskaitomo mokesčio komponentų grupę, prie kurios norite pridėti TDS komponentą.</span><span class="sxs-lookup"><span data-stu-id="47bd5-115">In the **Withholding tax component group** field, select the TDS withholding tax component group to attach the TDS component to.</span></span>
6. <span data-ttu-id="47bd5-116">**Bendra** „FastTab” skirtuke, **Aprašas** lauke, įveskite TDS komponento aprašą.</span><span class="sxs-lookup"><span data-stu-id="47bd5-116">On the **General** FastTab, in the **Description** field, enter a description of  the TDS component.</span></span>
7. <span data-ttu-id="47bd5-117">Veiksmų srityje pasirinkite **slenkstį** norėdami atidaryti **ribinės** vertės puslapį, kad būtų galima nustatyti ribinę vertę, naudojamą TDS komponento TDS apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="47bd5-117">On the Action Pane, select **Threshold** to open **Threshold** page, so that you can define the threshold that is used to calculate TDS for the TDS component.</span></span>
8. <span data-ttu-id="47bd5-118">Norėdami nustatyti laikotarpį, kada taikoma ribinė vertė, naudokite laukus **Nuo datos** ir **iki datos**.</span><span class="sxs-lookup"><span data-stu-id="47bd5-118">Use the **From date** and **To date** fields to define the period that the threshold is applicable to.</span></span>
9. <span data-ttu-id="47bd5-119">„FastTab“ **Bendri** ribinės **vertės** lauke įveskite ribinės vertės sumą, naudojamą TDS komponento TDS apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="47bd5-119">On the **General** FastTab, in the **Threshold** field, enter the threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="47bd5-120">Mokestis iš šaltinio bus atskaitytas tik tada, kai kaupiamoji SF suma peržengia ribinę vertę.</span><span class="sxs-lookup"><span data-stu-id="47bd5-120">The tax will be deducted at the source only when the cumulative invoice amount crosses the threshold.</span></span>

    <span data-ttu-id="47bd5-121">Pavyzdžiui, jei ribinė suma yra 10 000, TDS apskaičiuojama po kaupiamosios SF sumos, kuri viršija 10 000 (kitaip tariant, kai ji 10 001 ar daugiau).</span><span class="sxs-lookup"><span data-stu-id="47bd5-121">For example, if the threshold amount is 10,000, TDS is calculated after the cumulative invoice amount exceeds 10,000 (in other words, when it's 10,001 or more).</span></span>

10. <span data-ttu-id="47bd5-122">Laukelyje **Išimties slenkstis** įveskite ribinės vertės sumą, naudojamą TDS komponento TDS apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="47bd5-122">In the **Exception threshold** field, enter the exception threshold amount that is used to calculate TDS for the TDS component.</span></span> <span data-ttu-id="47bd5-123">Mokestis sąskaitose eilutėje iš šaltinio bus atskaitytas tik tada, kai kaupiamoji SF suma peržengia išlygos vertę.</span><span class="sxs-lookup"><span data-stu-id="47bd5-123">The tax on an invoice line will be deducted at the source only when the amount crosses the exception threshold.</span></span>

    <span data-ttu-id="47bd5-124">Pavyzdžiui, jei ribinė išimties suma yra 5000, TDS skaičiuojama pagal konkrečią SF eilutę, jei SF eilutės suma viršija 5000 (kitaip tariant, jei ji 5001 ar daugiau).</span><span class="sxs-lookup"><span data-stu-id="47bd5-124">For example, if the exception threshold amount is 5,000, TDS is calculated on a specific invoice line if the invoice line amount exceeds 5,000 (in other words, if it's 5,001 or more).</span></span>

    <span data-ttu-id="47bd5-125">[![Ribinės vertės puslapis](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span><span class="sxs-lookup"><span data-stu-id="47bd5-125">[![Threshold page](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)</span></span>

    > [!NOTE]
    > <span data-ttu-id="47bd5-126">Ribinė išimties suma turi būti mažesnė už ribinės vertės sumą arba tokia pat.</span><span class="sxs-lookup"><span data-stu-id="47bd5-126">The exception threshold amount must be less than or equal to the threshold amount.</span></span>
    >
    > <span data-ttu-id="47bd5-127">Operacijos mokestis atskaitomas, jei operacijos suma pereuoja išimties ribinę vertę, net jei kaupiamoji SF suma neišsiima ribinės vertės, nurodytos lauke **Ribinė** reikšmė.</span><span class="sxs-lookup"><span data-stu-id="47bd5-127">The tax is deducted for a transaction if the transaction amount crosses the exception threshold, even if the cumulative invoice amount doesn't cross the threshold that is specified in the **Threshold** field.</span></span>

11. <span data-ttu-id="47bd5-128">Norėdami grįžti į **puslapį** Išskaitomo mokesčio **komponentai, uždarykite puslapį** Ribinė vertė.</span><span class="sxs-lookup"><span data-stu-id="47bd5-128">Close the **Threshold** page to return to the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="47bd5-129">Veiksmų srityje pasirinkite **Kopijuoti** norėdami atidaryti **Kopijuoti išskaitomo mokesčio komponentus** dialogo lauką, kad būtų galima kopijuoti TDS komponentus, kurie buvo nustatyti vienai TDS komponentų grupei į kitą TDS komponentų grupę.</span><span class="sxs-lookup"><span data-stu-id="47bd5-129">On the Action Pane, select **Copy** to open the **Copy withholding tax components** dialog box, so that you can copy the TDS components that were set up for one TDS component group to another TDS component group.</span></span>
13. <span data-ttu-id="47bd5-130">Lauke **Iš** pasirinkite TDS komponentų grupę, iš kurios kopijuosite TDS komponentus.</span><span class="sxs-lookup"><span data-stu-id="47bd5-130">In the **From** field, select the TDS component group to copy the TDS components from.</span></span> <span data-ttu-id="47bd5-131">Lauke **Į** pasirinkiteišskaitomo mokesčio komponentų grupę, į šią grupę kopijuosite TDS komponentus.</span><span class="sxs-lookup"><span data-stu-id="47bd5-131">In the **To** field, select the withholding tax component group to copy the TDS components to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="47bd5-132">Bendrieji TDS komponentai, pridėti prie abiejų TDS komponentų grupių, nėra kopijuojami.</span><span class="sxs-lookup"><span data-stu-id="47bd5-132">Common TDS components that are attached to both TDS component groups aren't copied.</span></span>

14. <span data-ttu-id="47bd5-133">Norėdami **kopijuoti** ir kurti kitos TDS komponentų grupės TDS komponentus puslapyje **Išskaitomo mokesčio komponentai** pasirinkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="47bd5-133">Select **OK** to copy and create TDS components for the other TDS component group on the **Withholding tax components** page.</span></span>

    <span data-ttu-id="47bd5-134">[![Kopijuoti išskaitomo mokesčio komponentų dialogo langą](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span><span class="sxs-lookup"><span data-stu-id="47bd5-134">[![Copy withholding tax components dialog box](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)</span></span>

15. <span data-ttu-id="47bd5-135">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="47bd5-135">Close the page.</span></span>
