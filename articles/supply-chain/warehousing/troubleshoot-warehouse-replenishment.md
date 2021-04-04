---
title: Trikčių šalinimo sandėlio papildymas
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su sandėlio papildymą „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8dfb58c9156df106f58dfdc0ee2e0ef8defb9d9f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263209"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="9ecb8-103">Trikčių šalinimo sandėlio papildymas</span><span class="sxs-lookup"><span data-stu-id="9ecb8-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ecb8-104">Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su sandėlio papildymą „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="9ecb8-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="9ecb8-105">Gaunu tolesnį klaidos pranešimą: „Darbas %1 negali būti atblokuotas dėl to, kad turi nepabaigtą papildymo darbą."</span><span class="sxs-lookup"><span data-stu-id="9ecb8-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="9ecb8-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="9ecb8-106">Issue description</span></span>

<span data-ttu-id="9ecb8-107">Paėmimo darbas blokuojamas dėl priklausančio papildymo darbo.</span><span class="sxs-lookup"><span data-stu-id="9ecb8-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="9ecb8-108">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="9ecb8-108">Issue resolution</span></span>

<span data-ttu-id="9ecb8-109">Jums naudojant bangos poreikio papildymą, jei paėmimo vieta turi būti papildoma siekiant įgyvendinti šaltinio užsakymo poreikį, sistema sukuria papildymo darbą ir paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="9ecb8-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="9ecb8-110">Nepaisant to, ji blokuoja paėmimo darbą, kol bus užbaigtas papildymo darbas.</span><span class="sxs-lookup"><span data-stu-id="9ecb8-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="9ecb8-111">Šis elgesys yra tyčinis, nes paėmimo vieta neturės pakankamai inventoriaus, nebent papildymo darbas bus užbaigtas.</span><span class="sxs-lookup"><span data-stu-id="9ecb8-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="9ecb8-112">Užbaikite papildymo darbą ir tada apdorokite paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="9ecb8-112">Complete the replenishment work, and then process the picking work.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]