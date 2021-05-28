---
title: Nustatykite išskaitomo mokesčio kodų ataskaitos TDS mokesčių tipui
description: Išskaitomų mokesčių ataskaitų kodai naudojami 26Q formai ir 27Q formos išrašams, skirti išskaitomais mokesčiais šaltinyje (TDS), generuoti. Šioje temoje paaiškinama, kaip nustatyti išskaitomų mokesčių ataskaitų kodų veiksmus, kad būtų galima nustatyti TDS ataskaitų kodus.
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
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023458"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a><span data-ttu-id="477f9-104">Nustatykite išskaitomo mokesčio kodų ataskaitos TDS mokesčių tipui</span><span class="sxs-lookup"><span data-stu-id="477f9-104">Set up withholding tax reporting codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="477f9-105">Išskaitomų mokesčių ataskaitų kodai naudojami 26Q formai ir 27Q formos išrašams, skirti išskaitomais mokesčiais šaltinyje (TDS), generuoti.</span><span class="sxs-lookup"><span data-stu-id="477f9-105">Withholding tax reporting codes are used to generate Form 26Q and Form 27Q statements for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="477f9-106">Šioje temoje paaiškinama, kaip nustatyti išskaitomų mokesčių ataskaitų kodų veiksmus, kad būtų galima nustatyti TDS ataskaitų kodus.</span><span class="sxs-lookup"><span data-stu-id="477f9-106">This topic explains how to set up withholding tax reporting codes steps so that you can set up TDS reporting codes.</span></span>

1. <span data-ttu-id="477f9-107">Eikite į **Mokestis \> Nustatymai \> Išskaitomas mokestis \> Išskaitomo mokesčio ataskaitos kodai**.</span><span class="sxs-lookup"><span data-stu-id="477f9-107">Go to **Tax \> Setup \> Withholding tax \> Withholding tax reporting codes**.</span></span>

    <span data-ttu-id="477f9-108">[![Išskaitomų mokesčių ataskaitų kodų puslapis](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span><span class="sxs-lookup"><span data-stu-id="477f9-108">[![Withholding tax reporting codes page](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)</span></span>

2. <span data-ttu-id="477f9-109">Mokesčio **tipo lauke** pasirinkite **TDS** norėdami nustatyti TDS mokesčio tipo išskaitomo ataskaitos kodus.</span><span class="sxs-lookup"><span data-stu-id="477f9-109">In the **Tax type** field, select **TDS** to define withholding tax reporting codes for the TDS tax type.</span></span>
3. <span data-ttu-id="477f9-110">Lauke **Išskaitomo mokesčio komponentas** pasirinkite TDS komponentą, pagal kurį nustatote išskaitomo mokesčio ataskaitos kodą.</span><span class="sxs-lookup"><span data-stu-id="477f9-110">In the **Withholding tax component** field, select the TDS component to that you're defining the withholding tax reporting code for.</span></span> <span data-ttu-id="477f9-111">Išskaitomo **mokesčio komponentų grupės** laukas rodo TDS komponentų grupę, kuri buvo apibrėžta jūsų nustatytam TDS komponentui.</span><span class="sxs-lookup"><span data-stu-id="477f9-111">The **Withholding tax component group** field shows the TDS component group that was defined for the TDS component that you're defining.</span></span>

    <span data-ttu-id="477f9-112">**Skyriaus kodo** laukas **Bendrajame** „FastTab" rodo skyriaus kodą, kuris pridėtas prie TDS komponentų grupės.</span><span class="sxs-lookup"><span data-stu-id="477f9-112">The **Section code** field on the **General** FastTab shows the section code that is attached to the TDS component group.</span></span>

4. <span data-ttu-id="477f9-113">Pasirinktinai: **bendrajame** „FastTab" ataskaitos **kodo lauke pasirinkite TDs ataskaitos** kodą.</span><span class="sxs-lookup"><span data-stu-id="477f9-113">On the **General** FastTab, in the **Reporting code** field, select the TDS reporting code:</span></span>

    - <span data-ttu-id="477f9-114">TDS</span><span class="sxs-lookup"><span data-stu-id="477f9-114">TDS</span></span>
    - <span data-ttu-id="477f9-115">TCS</span><span class="sxs-lookup"><span data-stu-id="477f9-115">TCS</span></span>
    - <span data-ttu-id="477f9-116">Papildomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="477f9-116">Surcharge</span></span>
    - <span data-ttu-id="477f9-117">PE \_įrašai</span><span class="sxs-lookup"><span data-stu-id="477f9-117">PE\_Cess</span></span>
    - <span data-ttu-id="477f9-118">SHE \_Įrašai</span><span class="sxs-lookup"><span data-stu-id="477f9-118">SHE\_Cess</span></span>

5. <span data-ttu-id="477f9-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="477f9-119">Close the page.</span></span>
