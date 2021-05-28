---
title: Nustatyti mokėjimo grafikus su TDS paskirstymu
description: Šioje temoje paaiškinama, kaip nustatyti mokėjimo grafikus (TDS) priemonės išskaitomo mokesčio paskirstymui.
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
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023456"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a><span data-ttu-id="2b376-103">Nustatyti mokėjimo grafikus su TDS paskirstymu</span><span class="sxs-lookup"><span data-stu-id="2b376-103">Set up payment schedules with TDS allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b376-104">Šioje temoje paaiškinama, kaip nustatyti mokėjimo grafikus (TDS) priemonės išskaitomo mokesčio paskirstymui.</span><span class="sxs-lookup"><span data-stu-id="2b376-104">This topic explains how to set up payment schedules with Tax Deducted at Source (TDS) allocation.</span></span>

1. <span data-ttu-id="2b376-105">Pasirinkite **Mokėtinos sumos \> Mokėjimų sąranka \> Mokėjimo grafikas**.</span><span class="sxs-lookup"><span data-stu-id="2b376-105">Go to **Accounts payable \> Payment setup \> Payment schedules**.</span></span>

    <span data-ttu-id="2b376-106">[![Mokėjimo grafikų puslapis](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span><span class="sxs-lookup"><span data-stu-id="2b376-106">[![Payment schedules page](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span></span>

2. <span data-ttu-id="2b376-107">Veiksmų juostoje rinkitės **Naujas** norėdami sukurti mokėjimo grafiką ir įveskite reikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="2b376-107">On the Action Pane, select **New** to create a payment schedule, and enter the required details.</span></span>
3. <span data-ttu-id="2b376-108">Lauke **Paskirstymas** pasirinkite metodą, kurį naudosite paskirstyti mokėjimą mokėjimo grafikui:</span><span class="sxs-lookup"><span data-stu-id="2b376-108">In the **Allocation** field, select the method to use to allocate the payment for the payment schedule:</span></span>

    - <span data-ttu-id="2b376-109">Bendroji suma</span><span class="sxs-lookup"><span data-stu-id="2b376-109">Total</span></span>
    - <span data-ttu-id="2b376-110">Fiksuota suma</span><span class="sxs-lookup"><span data-stu-id="2b376-110">Fixed amount</span></span>
    - <span data-ttu-id="2b376-111">Fiksuotas kiekis</span><span class="sxs-lookup"><span data-stu-id="2b376-111">Fixed quantity</span></span>
    - <span data-ttu-id="2b376-112">Nurodyta</span><span class="sxs-lookup"><span data-stu-id="2b376-112">Specified</span></span>

    <span data-ttu-id="2b376-113">**Išskaitomo mokesčio paskirstymo** lauke rodomas TDS paskirstymo metodas, skirtas mokėjimo grafikui.</span><span class="sxs-lookup"><span data-stu-id="2b376-113">The **Withholding tax allocation** field shows the TDS allocation method for the payment schedule.</span></span> <span data-ttu-id="2b376-114">Jei lauke **Paskirstymas** pasirenkate **Bendroji** suma, **išskaitomo mokesčio paskirstymo** laukas automatiškai nustatomas kaip Bendroji **suma**.</span><span class="sxs-lookup"><span data-stu-id="2b376-114">If you select **Total** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Total**.</span></span> <span data-ttu-id="2b376-115">Jei lauke **Paskirstymas pasirenkate**, **Fiksuota suma** arba **Fiksuotas kiekis** esantis **Paskirstymo** lauke, **išskaitomo mokesčio paskirstymo** lauke automatiškai nustatomas **proporcingai**.</span><span class="sxs-lookup"><span data-stu-id="2b376-115">If you select **Fixed amount**, **Fixed quantity**, or **Specified** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Proportionally**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2b376-116">Jei išskaitomo mokesčio paskirstymo laukas nustatytas kaip Bendroji suma, mokėjimo mokėjimai apskaičiuojami remiantis bendra suma, į **kurią** įtraukta TDS **suma**.</span><span class="sxs-lookup"><span data-stu-id="2b376-116">If the **Withholding tax allocation** field is set to **Total**, the payment installments are calculated based on the gross amount, which includes the TDS amount.</span></span> <span data-ttu-id="2b376-117">Jei išskaitomo mokesčio paskirstymo laukas nustatytas kaip Proporcinga suma, mokėjimo mokėjimai apskaičiuojami remiantis grynoji suma, į **po** atskaičiuotos TDS **sumos**.</span><span class="sxs-lookup"><span data-stu-id="2b376-117">If the **Withholding tax allocation** field is set to **Proportionally**, the payment installments are calculated based on the net invoice amount after the TDS amount is deducted.</span></span>

4. <span data-ttu-id="2b376-118">Formoje įveskite kitą reikalingą informaciją ir tada užverkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2b376-118">Enter the other required details, and then close the page.</span></span>
