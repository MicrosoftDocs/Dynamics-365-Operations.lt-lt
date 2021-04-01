---
title: Nustatykite visuotinį išskaitymo mokestį
description: Šioje temoje išvardyti žingsniai, kuriais galima nustatyti visuotinį išskaitymo mokestį pardavimams ir pirkimams.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 00c472e90f4926c52ffe9b19661e68cbfa6bd493
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204838"
---
# <a name="set-up-global-withholding-tax"></a><span data-ttu-id="f3eaa-103">Nustatykite visuotinį išskaitymo mokestį</span><span class="sxs-lookup"><span data-stu-id="f3eaa-103">Set up global withholding tax</span></span>

<span data-ttu-id="f3eaa-104">Šioje temoje išvardyti žingsniai, kuriais galima nustatyti visuotinį išskaitymo mokestį pardavimams ir pirkimams.</span><span class="sxs-lookup"><span data-stu-id="f3eaa-104">This topic lists the steps for setting up global withholding tax for sales and purchases.</span></span> 

1. <span data-ttu-id="f3eaa-105">Nustatykite išskaitomo mokesčio įstaigas **Mokesčių išskaitymo įstaigų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f3eaa-105">Set up withholding tax authorities on the **Withholding tax authorities** page.</span></span>

2. <span data-ttu-id="f3eaa-106">Nustatykite išskaitymo nustatymo laikotarpius **Mokesčių išskaitymo nustatymo laikotarpių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f3eaa-106">Set up withholding settlement periods on the **Withholding tax settlement periods** page.</span></span>

3. <span data-ttu-id="f3eaa-107">Nustatykite išskaitymo buhalterinės knygos publikavimo grupę **Išskaitymo mokesčio > buhalterinės knygos publikavimo grupė** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f3eaa-107">Set up withholding ledger posting group on the **Withholding tax > ledger posting group** page.</span></span>

   > [!Note] 
   >
   > <span data-ttu-id="f3eaa-108">**Išskaitymo mokesčio** paskyra bus priskirta su pagrindine sąskaita su išskaitomo mokesčio **Publikavimo tipu**.</span><span class="sxs-lookup"><span data-stu-id="f3eaa-108">**Withholding tax** account will be assigned with a main account with **Posting type** of Withholding tax.</span></span> <span data-ttu-id="f3eaa-109">**Išskaitymo mokesčio nustatymas** paskyra taip pat bus priskirta su pagrindine sąskaita su išskaitomo mokesčio **Išskaitomo mokesčio nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="f3eaa-109">**Withholding tax offset** account will also be assigned with a main account with **Posting type** "Withholding tax offset".</span></span> <span data-ttu-id="f3eaa-110">Eikite į **Bendra buhalterinė knyga > Sąskaitų grafikas > Sąskaitos > Pagrindinės sąskaitos**, nustatykite **Publikavimo tipą** papildomos formos **Publikavimo patvirtinimas** pagrindinėms sąskaitoms.</span><span class="sxs-lookup"><span data-stu-id="f3eaa-110">Go to **General ledger > Chart of accounts > Accounts > Main accounts**, set up the **Posting type** in the **Posting validation** sub-form for the main accounts.</span></span>

4. <span data-ttu-id="f3eaa-111">Nustatykite išskaitomo mokesčio kodus **Mokesčių išskaitymo kodų** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f3eaa-111">Set up withholding tax codes on the **Withholding tax codes** page.</span></span>

5. <span data-ttu-id="f3eaa-112">Nustatykite išskaitomo mokesčio grupes **Mokesčių išskaitymo grupių** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f3eaa-112">Set up withholding tax groups on the **Withholding tax groups** page.</span></span>

6. <span data-ttu-id="f3eaa-113">Nustatykite išskaitomo mokesčio pajamų tipus **Išskaitomo mokesčio pajamos** **tipai** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f3eaa-113">Set up withholding tax revenue types on the **Withholding tax revenue** **types** page.</span></span>

7. <span data-ttu-id="f3eaa-114">Nustatykite išskaitomo mokesčio grupes **Prekės išskaitymo mokesčio grupių** puslapyje prekei ar paslaugoms.</span><span class="sxs-lookup"><span data-stu-id="f3eaa-114">Set up withholding tax groups on the **Item withholding tax groups** page for an item or service.</span></span>

8. <span data-ttu-id="f3eaa-115">Nustatykite **Mažiausią sąskaitos sumą** puslapyje **Bendrosios apskaitos knygos parametrai > Išskaitymo mokesčio** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="f3eaa-115">Set up **Minimum invoice amount** on the **General ledger parameters > Withholding tax** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]