---
title: Kvitas nesugeneruojamas
description: Šioje temoje pateikiama trikčių diagnostikos informacija, kuri gali padėti, kai kvitas turėtų būti generuojamas, bet jo nėra.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: eafc9110ec58be5083569188d59b67a62e86c85d
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947682"
---
# <a name="voucher-isnt-generated"></a><span data-ttu-id="aae1b-103">Kvitas nesugeneruojamas</span><span class="sxs-lookup"><span data-stu-id="aae1b-103">Voucher isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aae1b-104">Jei kvitas turi būti sugeneruotas, bet kvito operacijų puslapyje nerodyti kvitų, norėdami pašalinti šią problemą, atlikite toliau nurodytus veiksmus, nurodytus **skyriuose**.</span><span class="sxs-lookup"><span data-stu-id="aae1b-104">If a voucher should be generated, but the **Voucher transactions** page doesn't show any vouchers, follow the steps in the following sections as required to troubleshoot this issue.</span></span>

<span data-ttu-id="aae1b-105">[![Kvito operacijų puslapis, kuriame nėra kvitų](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="aae1b-105">[![Voucher transactions page that has no vouchers](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span></span>

## <a name="check-the-tax-applicability"></a><span data-ttu-id="aae1b-106">Patikrinti mokesčio taikomumą</span><span class="sxs-lookup"><span data-stu-id="aae1b-106">Check the tax applicability</span></span>

1. <span data-ttu-id="aae1b-107">Pereikite į **periodinių** \>**mokesčių užduočių** \> **papildomos knygos žurnalo įrašus, kurie dar nepervesti**.</span><span class="sxs-lookup"><span data-stu-id="aae1b-107">Go to **Tax** \> **Periodic tasks** \> **Subledger journal entries not yet transferred**.</span></span>
2. <span data-ttu-id="aae1b-108">Jei yra žurnalo įrašas, pasirinkite jį, tada pasirinkite **Perkelti** dabar.</span><span class="sxs-lookup"><span data-stu-id="aae1b-108">If there is a journal record, select it, and then select **Transfer now**.</span></span>

    <span data-ttu-id="aae1b-109">[![Perkelti dabar mygtuką papildomos knygos žurnalo įrašuose, kurie dar neperduoti puslapyje](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="aae1b-109">[![Transfer now button on the Subledger journal entries not yet transferred page](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span></span>

3. <span data-ttu-id="aae1b-110">Dar kartą **atidarykite** kvito operacijų puslapį, kad pamatytumėte, ar kvitas buvo sugeneruotas.</span><span class="sxs-lookup"><span data-stu-id="aae1b-110">Open the **Voucher transactions** page again to see whether the voucher was generated.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="aae1b-111">Nustatyti, ar yra tinkinimas</span><span class="sxs-lookup"><span data-stu-id="aae1b-111">Determine whether customization exists</span></span>

<span data-ttu-id="aae1b-112">Jei atlikote veiksmus ankstesniame skyriuje, bet neradote problemos, nustatykite, ar yra tinkinimas.</span><span class="sxs-lookup"><span data-stu-id="aae1b-112">If you've completed the steps in the previous section but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="aae1b-113">Jei tinkinimo nėra, sukurkite „Microsoft" aptarnavimo užklausą, kad ji būtų tolimesnė.</span><span class="sxs-lookup"><span data-stu-id="aae1b-113">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
