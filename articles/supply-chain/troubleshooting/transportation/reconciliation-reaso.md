---
title: Dėl suderinimo priežasčių galite įtraukti tik pagrindinę sąskaitą kaip kredito sąskaitą
description: Kai transportavimo valdymo dalyje nustatote derinimo priežastį, galite įtraukti tik pagrindinę sąskaitą kaip kredito sąskaitą.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026731"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a><span data-ttu-id="3c546-103">Dėl suderinimo priežasčių galite įtraukti tik pagrindinę sąskaitą kaip kredito sąskaitą</span><span class="sxs-lookup"><span data-stu-id="3c546-103">You can add only the main account as the credit account for reconciliation reasons</span></span>

<span data-ttu-id="3c546-104">KB numeris: 4603538</span><span class="sxs-lookup"><span data-stu-id="3c546-104">KB number: 4603538</span></span>

## <a name="symptoms"></a><span data-ttu-id="3c546-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="3c546-105">Symptoms</span></span>

<span data-ttu-id="3c546-106">Kai transportavimo valdymo dalyje nustatote derinimo priežastį, galite įtraukti tik pagrindinę sąskaitą kaip kredito sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="3c546-106">When you set up a reconciliation reason in Transportation management, you can add only the main account as the credit account.</span></span> <span data-ttu-id="3c546-107">Negalima įtraukti išlaidų centro ar kitos dimensijos kaip kredito sąskaitos.</span><span class="sxs-lookup"><span data-stu-id="3c546-107">You can't add a cost center or any other dimension as the credit account.</span></span> <span data-ttu-id="3c546-108">Tačiau debeto sąskaita leidžia pasirinkti kitas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="3c546-108">However, the debit account lets you select other dimensions.</span></span>

## <a name="resolution"></a><span data-ttu-id="3c546-109">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="3c546-109">Resolution</span></span>

<span data-ttu-id="3c546-110">Jei derinimas atliekamas ne mokėti tiekėjui, bet kredituoti konkrečią pagrindinę sąskaitą, sistema neleidžia pasirinkti kredito sąskaitos finansinės dimensijos, kai nustatote derinimo priežastį.</span><span class="sxs-lookup"><span data-stu-id="3c546-110">If the reconciliation isn't done to pay the vendor but to credit a specific main account, the system doesn't allow you to select a financial dimension for the credit account when you set up the reconciliation reason.</span></span>

<span data-ttu-id="3c546-111">Jei sąskaitos struktūrai reikia konkrečios kredito pagrindinės sąskaitos finansinės dimensijos vertės, gauto tiekėjo žurnalo automatiškai registruoti negalima, nes trūksta finansinės dimensijos vertės.</span><span class="sxs-lookup"><span data-stu-id="3c546-111">If the account structure requires a specific financial dimension value for the credit main account, the resulting vendor journal can't be posted automatically, because the financial dimension value is missing.</span></span> <span data-ttu-id="3c546-112">Todėl pirmiausia, naudodami SF žurnalo puslapį, turite nurodyti kredito **sąskaitą neautomatiniu** būdu.</span><span class="sxs-lookup"><span data-stu-id="3c546-112">Therefore, you must first manually specify the credit account by using the **Invoice journal** page.</span></span>

<span data-ttu-id="3c546-113">Kadangi reikalinga kredito sąskaitos dimensijos vertė, tiekėjo SF žurnalo automatiškai registruoti negalima.</span><span class="sxs-lookup"><span data-stu-id="3c546-113">Because a dimension value is required for the credit account, the vendor invoice journal can't be automatically posted.</span></span> <span data-ttu-id="3c546-114">Rankiniu būdu pridę dimensijos vertę prie kredito eilutės pagrindinės sąskaitos, ją turite užregistruoti neautomatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="3c546-114">You must manually post it after you manually add the dimension value to the main account for the credit line.</span></span>
