---
title: Nustatykite išskaitomo mokesčio sudengimo laikotarpius TDS mokesčių tipui
description: Šioje temoje paaiškinama, kaip nustatyti sudengimo laikotarpius (TDS) priemonės sudengimo laikotarpius.
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
ms.openlocfilehash: 9430bc1386f127d02b598d6cad1b53f66e0cf2ba
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023435"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a><span data-ttu-id="ac955-103">Nustatykite išskaitomo mokesčio sudengimo laikotarpius TDS mokesčių tipui</span><span class="sxs-lookup"><span data-stu-id="ac955-103">Set up withholding tax settlement periods for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac955-104">Šioje temoje paaiškinama, kaip nustatyti sudengimo laikotarpius (TDS) priemonės sudengimo laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="ac955-104">This topic explains how to set up settlement periods for Tax Deducted at Source (TDS) settlement periods.</span></span>

1. <span data-ttu-id="ac955-105">Pasirinkite **Mokestis \> Netiesioginiai mokesčiai \> Išskaitomas mokestis \> Išskaitomo mokesčio sudengimo laikotarpiai**.</span><span class="sxs-lookup"><span data-stu-id="ac955-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax settlement periods**.</span></span>

    <span data-ttu-id="ac955-106">[![Išskaitomo mokesčio sudengimo laikotarpių puslapis](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span><span class="sxs-lookup"><span data-stu-id="ac955-106">[![Withholding tax settlement periods page](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)</span></span>

2. <span data-ttu-id="ac955-107">Mokesčio **tipo lauke** pasirinkite **TDS** norėdami nustatyti TDS mokesčio sudengimo laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="ac955-107">In the **Tax type** field, select **TDS** to set up withholding tax settlement periods for the TDS tax type.</span></span>
3. <span data-ttu-id="ac955-108">Pasirinkite **Nauja**, kad sukurtumėte eilutę.</span><span class="sxs-lookup"><span data-stu-id="ac955-108">Select **New** to create a line.</span></span>
4. <span data-ttu-id="ac955-109">Į lauką **Sudengimo laikotarpis** įveskite TDS sudengimo laikotarpio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ac955-109">In the **Settlement period** field, enter a name for the TDS settlement period.</span></span>
5. <span data-ttu-id="ac955-110">Lauke **Aprašas** įveskite aprašą.</span><span class="sxs-lookup"><span data-stu-id="ac955-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="ac955-111">Lauke **Išskaitomo mokesčio inspekciją** pasirinkite TDS instituciją, kurios TDS sudengimo laikotarpį nustatote.</span><span class="sxs-lookup"><span data-stu-id="ac955-111">In the **Withholding tax authority** field, select the TDS authority that you're defining the TDS settlement period for.</span></span>
7. <span data-ttu-id="ac955-112">**Bendri** "FastTab" laikotarpio **intervalo lauke** pasirinkite TDS sudengimo laikotarpio intervalo tipą.</span><span class="sxs-lookup"><span data-stu-id="ac955-112">On the **General** FastTab, in the **Period interval** field, select the type of period interval for the TDS settlement period.</span></span>
8. <span data-ttu-id="ac955-113">Lauke **Vienetų skaičius** nurodykite laikotarpio intervalo tipo vienetų skaičių.</span><span class="sxs-lookup"><span data-stu-id="ac955-113">In the **Number of units** field, specify the number of units for the period interval type.</span></span>
9. <span data-ttu-id="ac955-114">**Laikotarpių** „FastTab" lauke **Pradžios data** rinkitės TDS sudengimo laikotarpio pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="ac955-114">On the **Periods** FastTab, in the **From date** field, select the start date for the TDS settlement period.</span></span> <span data-ttu-id="ac955-115">Lauke **Iki datos** rinkitės pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="ac955-115">In the **To date** field, select the end date.</span></span>
10. <span data-ttu-id="ac955-116">Norėdami sukurti vėlesnį esamo laikotarpio TDS sudengimo laikotarpį, pagrįstą laikotarpio intervalu ir laikotarpio vienetais, pasirinkite **Naujas laikotarpis**.</span><span class="sxs-lookup"><span data-stu-id="ac955-116">To create a subsequent TDS settlement period for an existing period, based on the period interval and period units, select **New period**.</span></span>
11. <span data-ttu-id="ac955-117">Norėdami peržiūrėti tam tikro sudengimo laikotarpio periodinio TDS sudengimo informaciją, pasirinkite Išskaitomo mokesčio mokėjimus, kad atidarytumėte **išskaitomo mokesčio mokėjimo** puslapį **Išskaitomo mokesčio mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="ac955-117">To view the details of the periodic TDS settlement that is run for a specific settlement period, select **Withholding tax payments** to open the **Withholding tax payment** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac955-118">Norėdami vykdyti periodinio TDS sudengimo procesą, eikite į **DK \> Periodinis \> Išskaitomas mokestis \> Išskaitomo mokesčio mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="ac955-118">To run the periodic TDS settlement process, go to **General ledger \> Periodic \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="ac955-119">[![Išskaitomo mokesčio mokėjimo puslapis](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span><span class="sxs-lookup"><span data-stu-id="ac955-119">[![Withholding tax payment page](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)</span></span>

12. <span data-ttu-id="ac955-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ac955-120">Close the page.</span></span>
