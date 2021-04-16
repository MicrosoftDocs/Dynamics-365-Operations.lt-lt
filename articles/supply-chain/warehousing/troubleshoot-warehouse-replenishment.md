---
title: Trikčių šalinimo sandėlio papildymas
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su sandėlio papildymą „Microsoft Dynamics 365 Supply Chain Management“.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8940f729e1115405e8d6e50eccc92d9fffe37f3e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828087"
---
# <a name="troubleshoot-warehouse-replenishment"></a><span data-ttu-id="0cf30-103">Trikčių šalinimo sandėlio papildymas</span><span class="sxs-lookup"><span data-stu-id="0cf30-103">Troubleshoot warehouse replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0cf30-104">Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su sandėlio papildymą „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="0cf30-104">This topic describes how to fix common issues that you might encounter while you work with warehouse replenishment in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a><span data-ttu-id="0cf30-105">Gaunu tolesnį klaidos pranešimą: „Darbas %1 negali būti atblokuotas dėl to, kad turi nepabaigtą papildymo darbą."</span><span class="sxs-lookup"><span data-stu-id="0cf30-105">I receive the following error message: "Work %1 cannot be unblocked because it has unfinished replenishment work."</span></span>

### <a name="issue-description"></a><span data-ttu-id="0cf30-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="0cf30-106">Issue description</span></span>

<span data-ttu-id="0cf30-107">Paėmimo darbas blokuojamas dėl priklausančio papildymo darbo.</span><span class="sxs-lookup"><span data-stu-id="0cf30-107">Picking work is blocked because of dependent replenishment work.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="0cf30-108">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="0cf30-108">Issue resolution</span></span>

<span data-ttu-id="0cf30-109">Jums naudojant bangos poreikio papildymą, jei paėmimo vieta turi būti papildoma siekiant įgyvendinti šaltinio užsakymo poreikį, sistema sukuria papildymo darbą ir paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="0cf30-109">When you use wave demand replenishment, if a picking location must be replenished to fulfill the source order demand, the system creates both the replenishment work and the picking work.</span></span> <span data-ttu-id="0cf30-110">Nepaisant to, ji blokuoja paėmimo darbą, kol bus užbaigtas papildymo darbas.</span><span class="sxs-lookup"><span data-stu-id="0cf30-110">However, it blocks the picking work until the replenishment work is completed.</span></span> <span data-ttu-id="0cf30-111">Šis elgesys yra tyčinis, nes paėmimo vieta neturės pakankamai inventoriaus, nebent papildymo darbas bus užbaigtas.</span><span class="sxs-lookup"><span data-stu-id="0cf30-111">This behavior is intentional, because the picking location won't have enough inventory unless the replenishment work is completed.</span></span> <span data-ttu-id="0cf30-112">Užbaikite papildymo darbą ir tada apdorokite paėmimo darbą.</span><span class="sxs-lookup"><span data-stu-id="0cf30-112">Complete the replenishment work, and then process the picking work.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]