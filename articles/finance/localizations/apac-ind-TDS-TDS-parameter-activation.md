---
title: Nustatykite TDS parametrus
description: Šioje temoje paaiškinama, kaip nustatyti parametrus, siekiant suaktyvinti išskaitytų mokesčių (TDS) funkciją nurodytose operacijose. Tai yra būtinas žingsnis norint naudoti iš šaltinio TDS priemonę atskaityti mokesčius.
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
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023446"
---
# <a name="set-the-tds-parameters"></a><span data-ttu-id="ef3c5-104">Nustatykite TDS parametrus</span><span class="sxs-lookup"><span data-stu-id="ef3c5-104">Set the TDS parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef3c5-105">Šioje temoje paaiškinama, kaip nustatyti parametrus, siekiant suaktyvinti išskaitytų mokesčių (TDS) funkciją nurodytose operacijose.</span><span class="sxs-lookup"><span data-stu-id="ef3c5-105">This topic explains how to set parameters to activate Tax Deducted at Source (TDS) functionality in specified transactions.</span></span> <span data-ttu-id="ef3c5-106">Tai yra būtinas žingsnis norint naudoti iš šaltinio TDS priemonę atskaityti mokesčius.</span><span class="sxs-lookup"><span data-stu-id="ef3c5-106">This is a necessary step to use the Tax Deducted at Source TDS feature.</span></span>

1. <span data-ttu-id="ef3c5-107">Eikite į **Didžioji knyga \> Didžiosios knygos nustatymas \> DK parametrai**.</span><span class="sxs-lookup"><span data-stu-id="ef3c5-107">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="ef3c5-108">Skirtuko **Tiesioginiai mokesčiai** dalyje **Šaltinio atskaityti mokesčiai** nustatykite **Suaktyvinti TDS** parinktį į **Taip** norėdami suaktyvinti TDS funkciją, ir jai naudojamus puslapius ir laukus.</span><span class="sxs-lookup"><span data-stu-id="ef3c5-108">On the **Direct taxes** tab, in the **Tax Deducted at Source** section, set the **Activate TDS** option to **Yes** to activate the TDS functionality, and the pages and fields that are used for it.</span></span>
3. <span data-ttu-id="ef3c5-109">Nustatykite **SF** parinktį į **Taip** norėdami suaktyvinti laukus, kurie naudojami TDS apskaičiuoti ir atskaityti SF lygiu.</span><span class="sxs-lookup"><span data-stu-id="ef3c5-109">Set the **Invoice** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the invoice level.</span></span>
4. <span data-ttu-id="ef3c5-110">Nustatykite **Mokėjimas** parinktį į **Taip** norėdami suaktyvinti laukus, kurie naudojami TDS apskaičiuoti ir atskaityti mokėjimo lygiu.</span><span class="sxs-lookup"><span data-stu-id="ef3c5-110">Set the **Payment** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the payment level.</span></span>

    <span data-ttu-id="ef3c5-111">[![Skirtukas tiesioginiai mokesčiai](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span><span class="sxs-lookup"><span data-stu-id="ef3c5-111">[![Direct taxes tab](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span></span>

5. <span data-ttu-id="ef3c5-112">Numeracijų **skirtuke raskite** eilutę, kurioje **nuorodos** lauke nustatyta **išskaitomo mokesčio mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="ef3c5-112">On the **Number sequences** tab, find the row where the **Reference** field is set to **Withholding tax payment**.</span></span> <span data-ttu-id="ef3c5-113">Lauke **Numerio sekos kodas** eilutei, pasirinkite numerio sekos kodą.</span><span class="sxs-lookup"><span data-stu-id="ef3c5-113">In the **Number sequence code** field for the row, select the number sequence code.</span></span> <span data-ttu-id="ef3c5-114">Numeracijos kodas naudojamas periodinio TDS sudengimo proceso kvitų numeriams generuoti.</span><span class="sxs-lookup"><span data-stu-id="ef3c5-114">The number sequence code is used to generate voucher numbers for the periodic TDS settlement process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef3c5-115">Norėdami vykdyti periodinio TDS sudengimo procesą, eikite į **Mokesčių \> Deklaracijos \> Išskaitomas mokestis \> Išskaitomo mokesčio mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="ef3c5-115">To run the periodic TDS settlement process, go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="ef3c5-116">[![Numeracijų skirtukas](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span><span class="sxs-lookup"><span data-stu-id="ef3c5-116">[![Number sequences tab](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span></span>

6. <span data-ttu-id="ef3c5-117">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="ef3c5-117">Close the page.</span></span>
