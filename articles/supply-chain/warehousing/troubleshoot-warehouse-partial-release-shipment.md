---
title: Trikčių šalinimo daliniai leidimai ir dalinis siuntimas
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su daliniais leidimai ir daliniais siuntimais „Microsoft Dynamics 365 Supply Chain Management“.
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
ms.openlocfilehash: 1c9246376505e163a4a41bf141a98deed0fd511f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263246"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="4eb87-103">Trikčių šalinimo daliniai leidimai ir dalinis siuntimas</span><span class="sxs-lookup"><span data-stu-id="4eb87-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4eb87-104">Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti dirbdami su daliniais leidimai ir daliniais siuntimais „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="4eb87-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="4eb87-105">Prekybos užsakymo paleidimo būsena išlieka dalinai paleista net ir po prekybos užsakymo įtraukimo į sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="4eb87-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="4eb87-106">Problemos aprašas</span><span class="sxs-lookup"><span data-stu-id="4eb87-106">Issue description</span></span>

<span data-ttu-id="4eb87-107">Pardavimo užsakymas yra pristatymo užsakymas, bet vienas ar keletas prekių jame turi skirtingą pristatymo būdą.</span><span class="sxs-lookup"><span data-stu-id="4eb87-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="4eb87-108">Įtraukus į sąskaitą užsakymą, jis vis dar turi išleidimo būseną *Iš dalies išleistas*.</span><span class="sxs-lookup"><span data-stu-id="4eb87-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="4eb87-109">Pavyzdžiui, pardavimo užsakymas turi dvi prekes: vieną pristatymui ir kitą paėmimui.</span><span class="sxs-lookup"><span data-stu-id="4eb87-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="4eb87-110">Tiek pristatymas, tiek paėmimas buvo atlikti.</span><span class="sxs-lookup"><span data-stu-id="4eb87-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="4eb87-111">Dėl to, abi eilutės buvo įtrauktos į sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="4eb87-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="4eb87-112">Nepaisant to, išleidimo būsena vis dar rodoma kaip *Iš dalies išleistas*, o tai neteisinga.</span><span class="sxs-lookup"><span data-stu-id="4eb87-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="4eb87-113">Problemos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="4eb87-113">Issue resolution</span></span>

<span data-ttu-id="4eb87-114">Išleidimo būsena taikoma tik užsakymo eilutėms, kurioje prekės buvo įjungtos sandėlio valdymui.</span><span class="sxs-lookup"><span data-stu-id="4eb87-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="4eb87-115">Dėl to, išleidimo būsena išlieka *Iš dalies išleista* šiame scenarijuje.</span><span class="sxs-lookup"><span data-stu-id="4eb87-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="4eb87-116">„Microsoft“ įvertino šią klaidą ir nustatė jos funkcijos apribojimą.</span><span class="sxs-lookup"><span data-stu-id="4eb87-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="4eb87-117">Išplėtimas gali būti įtrauktas kaip paėmimo praleidimo dalis ir sąskaitos procesas siekiant atnaujinti išleidimo būseną.</span><span class="sxs-lookup"><span data-stu-id="4eb87-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]