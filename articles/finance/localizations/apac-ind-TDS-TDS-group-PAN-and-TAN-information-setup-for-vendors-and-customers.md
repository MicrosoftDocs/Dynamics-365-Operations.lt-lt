---
title: Nustatyti TDS grupę, PAN ir TAN informaciją tiekėjams ir klientams
description: Šioje temoje aiškinama, kaip nustatyti informaciją apie grupę Išskaičiuotas mokestis pagal šaltinį (TDS), nuolatinės sąskaitos numerį (PAN) ir mokesčių sąskaitos numerį (TAN) tiekėjams ir pirkėjams.
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
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023449"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a><span data-ttu-id="73dde-103">Nustatyti TDS grupę, PAN ir TAN informaciją tiekėjams ir klientams</span><span class="sxs-lookup"><span data-stu-id="73dde-103">TDS group, PAN, and TAN information setup for vendors and customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73dde-104">Šioje temoje aiškinama, kaip nustatyti informaciją apie grupę Išskaičiuotas mokestis pagal šaltinį (TDS), nuolatinės sąskaitos numerį (PAN) ir mokesčių sąskaitos numerį (TAN) tiekėjams ir pirkėjams.</span><span class="sxs-lookup"><span data-stu-id="73dde-104">This topic explains how to set up information about the Tax Deducted at Source (TDS) group, permanent account number (PAN), and tax account number (TAN) for vendors and customers.</span></span>

1. <span data-ttu-id="73dde-105">Eikite į **Mokėtinos sumos \> Tiekėjai \> Visi tiekėjai** ar **Gautinų sumų \> pirkėjai \> Visi pirkėjai**.</span><span class="sxs-lookup"><span data-stu-id="73dde-105">Go to **Accounts payable \> Vendors \> All vendors** or **Accounts receivable \> Customers \> All customers**.</span></span>

    <span data-ttu-id="73dde-106">[![Puslapis Visi tiekėjai](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span><span class="sxs-lookup"><span data-stu-id="73dde-106">[![All vendors page](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span></span>

2. <span data-ttu-id="73dde-107">Veiksmų juostoje rinkitės **Naujas** norėdami sukurti tiekėją ar klientą ir įveskite reikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="73dde-107">On the Action Pane, select **New** to create a vendor or customer, and enter the required details.</span></span> <span data-ttu-id="73dde-108">Arba pasirinkite esamą tiekėją arba klientą.</span><span class="sxs-lookup"><span data-stu-id="73dde-108">Alternatively, select an existing vendor or customer.</span></span>
3. <span data-ttu-id="73dde-109">„FastTab“ **Sąskaita ir pristatymas** esančiame **Mokesčio atskaičiavimas** skyriuje nustatykite **Skaičiuoti atskaitomą mokestį** parinktį į **Taip** tam, kad apskaičiuotumėte atskaičiuojamą mokestį TDS ar surinktą mokestį šaltinyje (TCS) tiekėjui ar klientui.</span><span class="sxs-lookup"><span data-stu-id="73dde-109">On the **Invoice and delivery** FastTab, in the **Withholding tax** section, set the **Calculate withholding tax** option to **Yes** to calculate withholding tax, TDS, or Tax Collected at Source (TCS) for the vendor or customer.</span></span>
4. <span data-ttu-id="73dde-110">Pirkimo SF TDS apskaičiuojama pagal numatytąją TDS grupę, kuri nustatyta tiekėjui arba klientui.</span><span class="sxs-lookup"><span data-stu-id="73dde-110">TDS for a purchase invoice is calculated based on the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="73dde-111">Lauke **TDS grupė** pasirinkite numatyta TDS grupė.</span><span class="sxs-lookup"><span data-stu-id="73dde-111">In the **TDS group** field, select the default TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="73dde-112">Kai pasirenkate TDS grupę **TDS grupės** laukelyje, **Atskaitomo mokesčio grupė** ir **TCS grupė** laukeliai tampa nebeprieinami.</span><span class="sxs-lookup"><span data-stu-id="73dde-112">When you select a TDS group in the **TDS group** field, the **Withholding tax group** and **TCS group** fields become unavailable.</span></span>

5. <span data-ttu-id="73dde-113">„FastTab“ **Mokesčių informacija** skyriuje **PAN informacija** lauke **Būsena** pasirinkite tiekėjo arba pirkėjo nuolatinės sąskaitos numerio būseną:</span><span class="sxs-lookup"><span data-stu-id="73dde-113">On the **Tax information** FastTab, in the **PAN information** section, in the **Status** field, select the status of the permanent account number for the vendor or customer:</span></span>

    - <span data-ttu-id="73dde-114">**Nepasiekiama** – tiekėjas arba klientas neturi PAN.</span><span class="sxs-lookup"><span data-stu-id="73dde-114">**Not available** – The vendor or customer doesn't have a PAN.</span></span>
    - <span data-ttu-id="73dde-115">**Gauta** – tiekėjas arba klientas turi PAN.</span><span class="sxs-lookup"><span data-stu-id="73dde-115">**Received** – The vendor or customer has a PAN.</span></span>
    - <span data-ttu-id="73dde-116">**Taikoma** – tiekėjas arba klientas kreipėsi dėl PAN.</span><span class="sxs-lookup"><span data-stu-id="73dde-116">**Applied** – The vendor or customer has applied for a PAN.</span></span>
    - <span data-ttu-id="73dde-117">**Netinkamas** – tiekėjas arba klientas turi PAN, bet jis negalioja.</span><span class="sxs-lookup"><span data-stu-id="73dde-117">**Invalid** – The vendor or customer has a PAN, but it isn't valid.</span></span>

6. <span data-ttu-id="73dde-118">Jei lauke **Būsena** pasirinkote **Gauta**, kad nurodytumėte, jog tiekėjas arba pirkėjas turi PAN, lauke įveskite PAN **numerį**.</span><span class="sxs-lookup"><span data-stu-id="73dde-118">If you selected **Received** in the **Status** field to indicate that the vendor or customer has a PAN, enter the PAN in the **Number** field.</span></span> <span data-ttu-id="73dde-119">PAN turi sudaryti penki raidiniai simboliai, tada keturi skaitiniai simboliai, o tada vienas abėcėlinis simbolis.</span><span class="sxs-lookup"><span data-stu-id="73dde-119">The PAN must consist of five alphabetic characters, then four numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="73dde-120">Toliau pateikiamas pavyzdys: **ABCDE1260A**.</span><span class="sxs-lookup"><span data-stu-id="73dde-120">Here is an example: **ABCDE1260A**.</span></span>
7. <span data-ttu-id="73dde-121">Jei lauke **Taikoma** pasirinkote **Gauta**, kad nurodytumėte, jog tiekėjas arba pirkėjas taiko PAN numerį, įvedamas nuorodos numeris **Nuorodos numerio** laukelyje.</span><span class="sxs-lookup"><span data-stu-id="73dde-121">If you selected **Applied** in the **Status** field to indicate that the vendor or customer has applied for PAN, enter the reference number in the **Reference number** field.</span></span>
8. <span data-ttu-id="73dde-122">Lauke **Vertinamo produkto** pobūdis pasirinkite vertinamo kliento kategorijos, kuriai priklauso tiekėjas arba klientas, pobūdį:</span><span class="sxs-lookup"><span data-stu-id="73dde-122">In the **Nature of assessee** field, select the nature of assessee category that the vendor or customer belongs to:</span></span>

    - <span data-ttu-id="73dde-123">Įmonė</span><span class="sxs-lookup"><span data-stu-id="73dde-123">Company</span></span>
    - <span data-ttu-id="73dde-124">HUF</span><span class="sxs-lookup"><span data-stu-id="73dde-124">HUF</span></span>
    - <span data-ttu-id="73dde-125">Patvirtinti</span><span class="sxs-lookup"><span data-stu-id="73dde-125">Firm</span></span>
    - <span data-ttu-id="73dde-126">Individualus</span><span class="sxs-lookup"><span data-stu-id="73dde-126">Individual</span></span>
    - <span data-ttu-id="73dde-127">AOP</span><span class="sxs-lookup"><span data-stu-id="73dde-127">AOP</span></span>
    - <span data-ttu-id="73dde-128">KKI</span><span class="sxs-lookup"><span data-stu-id="73dde-128">BOI</span></span>
    - <span data-ttu-id="73dde-129">Vietos valdžia</span><span class="sxs-lookup"><span data-stu-id="73dde-129">Local authority</span></span>
    - <span data-ttu-id="73dde-130">Kita</span><span class="sxs-lookup"><span data-stu-id="73dde-130">Others</span></span>

    <span data-ttu-id="73dde-131">[![Mokesčių informacijos „FastTab“](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span><span class="sxs-lookup"><span data-stu-id="73dde-131">[![Tax information FastTab](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span></span>

9. <span data-ttu-id="73dde-132">Tada, veiksmų juostoje **Tiekėjas** skirtuke, grupėje **Registracija** rinktiės **Registracijos ID** tam, kad atvertumėte **Valdyti adresus** puslapį.</span><span class="sxs-lookup"><span data-stu-id="73dde-132">On the Action Pane, on the **Vendor** tab, in the **Registration** group, select **Registration IDs** to open the **Manage addresses** page.</span></span>
10. <span data-ttu-id="73dde-133">Puslapio **Tvarkyti adresus** „FastTab“ **Mokesčių informacija** pasirinkite **Įtraukti** arba **Redaguoti,** kad atidarytumėte puslapį **Tvarkyti mokesčių informaciją**, kuriame galite tvarkyti mokesčių registracijos įrašą.</span><span class="sxs-lookup"><span data-stu-id="73dde-133">On the **Manage addresses** page, on the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>
11. <span data-ttu-id="73dde-134">Puslapio **Tvarkyti mokesčių informaciją** „FastTab“ **Išskaitomas mokestis** lauke **Mokesčių sąskaitos numeris (TAN)** įveskite TAN.</span><span class="sxs-lookup"><span data-stu-id="73dde-134">On the **Manage tax information** page, on the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the TAN.</span></span> <span data-ttu-id="73dde-135">TAN turi sudaryti keturi raidiniai simboliai, tada penki skaitiniai simboliai, o tada vienas abėcėlinis simbolis.</span><span class="sxs-lookup"><span data-stu-id="73dde-135">The TAN must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="73dde-136">Toliau pateikiamas pavyzdys: **AFGH54821T**.</span><span class="sxs-lookup"><span data-stu-id="73dde-136">Here is an example: **AFGH54821T**.</span></span>
12. <span data-ttu-id="73dde-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="73dde-137">Close the page.</span></span>
