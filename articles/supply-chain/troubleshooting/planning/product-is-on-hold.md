---
title: Produktas yra sulaikytas operacijoms
description: Kai tvirtinate planavimo užsakymus, gaunate klaidos pranešimą, kuriame teigiama, kad prekė yra sulaikyta operacijoms.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301284"
---
# <a name="product-is-on-hold-for-transactions"></a><span data-ttu-id="f445d-103">Produktas yra sulaikytas operacijoms</span><span class="sxs-lookup"><span data-stu-id="f445d-103">Product is on hold for transactions</span></span>

<span data-ttu-id="f445d-104">Klaidos kodas: SYS13295</span><span class="sxs-lookup"><span data-stu-id="f445d-104">Error code: SYS13295</span></span>

## <a name="symptoms"></a><span data-ttu-id="f445d-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="f445d-105">Symptoms</span></span>

<span data-ttu-id="f445d-106">Kai tvirtinate suplanuotus užsakymus, gaunate tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="f445d-106">After you firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="f445d-107">Prekė %1 sulaikoma dėl %2 esančių operacijų.</span><span class="sxs-lookup"><span data-stu-id="f445d-107">Item %1 is on hold for transactions in %2.</span></span>

## <a name="cause"></a><span data-ttu-id="f445d-108">Priežastis</span><span class="sxs-lookup"><span data-stu-id="f445d-108">Cause</span></span>

<span data-ttu-id="f445d-109">Užblokuotų prekių apibūdinimui sistema naudoja terminus *užblokuota*, *sustabdyta* ir *sulaikyta* pakaitomis.</span><span class="sxs-lookup"><span data-stu-id="f445d-109">When describing blocked items, system uses the terms *blocked*, *stopped*, and *on hold* interchangeably.</span></span> <span data-ttu-id="f445d-110">Ši klaida reiškia, kad prekė nustatyta kaip **Sustabdyta** numatytuose užsakymo parametruose.</span><span class="sxs-lookup"><span data-stu-id="f445d-110">This error means that the item is set as **Stopped** in its default order settings.</span></span>

<span data-ttu-id="f445d-111">Jei prekė užblokuota ir ją pridedate prie pirkimo užsakymo arba pardavimo užsakymo eilutės, gaunate perspėjimo pranešimą.</span><span class="sxs-lookup"><span data-stu-id="f445d-111">If an item is blocked, and you add it to a purchase order or sales order line, you receive a warning message.</span></span> <span data-ttu-id="f445d-112">Kai prekė užblokuota, negalima modifikuoti su pirkimo užsakymo arba pardavimo užsakymo eilute susijusių atsargų operacijų (pavyzdžiui, registruojant važtaraštį arba sąskaitą faktūrą).</span><span class="sxs-lookup"><span data-stu-id="f445d-112">When an item is blocked, inventory transactions that are related to the purchase order or sales order line can't be modified (for example, when you post a packing slip or an invoice).</span></span> <span data-ttu-id="f445d-113">Galite užblokuoti nusipirktą prekę ir tuo pačiu metu prekę parduoti.</span><span class="sxs-lookup"><span data-stu-id="f445d-113">You can block a purchased item, and, at the same time, sell the item.</span></span> <span data-ttu-id="f445d-114">Tokiu atveju pirkimo užsakyme pasirenkamas **Sustabdyta** žymės langelis, bet prekė nėra blokuojama atsargose arba pardavimo užsakyme.</span><span class="sxs-lookup"><span data-stu-id="f445d-114">In this case, the **Stopped** check box is selected on a purchase order, but the item isn't blocked in inventory or on a sales order.</span></span>

<span data-ttu-id="f445d-115">Štai keletas sąlygų, dėl kurių prekės numeris gali būti užblokuotas pardavimui:</span><span class="sxs-lookup"><span data-stu-id="f445d-115">Here are some of the conditions that can cause an item number to be blocked from being sold:</span></span>

- <span data-ttu-id="f445d-116">Prekė vis dar gaminama.</span><span class="sxs-lookup"><span data-stu-id="f445d-116">The item is still under development or manufacture.</span></span> <span data-ttu-id="f445d-117">Todėl nenorite jos parduoti ar rezervuoti.</span><span class="sxs-lookup"><span data-stu-id="f445d-117">Therefore, you don't want it to be sold or reserved.</span></span>
- <span data-ttu-id="f445d-118">Gavote daug brokuotų prekių ir defektai turi būti ištaisyti prieš parduodant prekę.</span><span class="sxs-lookup"><span data-stu-id="f445d-118">You've received many defective items, and the defects must be corrected before the item can be sold.</span></span>

<span data-ttu-id="f445d-119">Tokio tipo atvejais prekę galite blokuoti, kol problema bus išspręsta.</span><span class="sxs-lookup"><span data-stu-id="f445d-119">In cases of this type, you can block the item until the issue is resolved.</span></span>

<span data-ttu-id="f445d-120">Jei prekė blokuojama, o jūs kuriate grąžinimo užsakymo eilutę, gaunate pranešimą.</span><span class="sxs-lookup"><span data-stu-id="f445d-120">If an item is blocked, and you create a return order line, you receive a message.</span></span> <span data-ttu-id="f445d-121">Jūs negalite užblokuoti prekės serijos arba partijos.</span><span class="sxs-lookup"><span data-stu-id="f445d-121">You can't block a series or a lot of an item.</span></span> <span data-ttu-id="f445d-122">Jeigu prekės dalys turi būti užblokuotos, jas galima užblokuoti perkeliant atsargas arba užblokuojant visas to laikotarpio prekės atsargas.</span><span class="sxs-lookup"><span data-stu-id="f445d-122">If parts of an item must be blocked, you can block them by moving inventory or by blocking the full stock of the item for that period.</span></span>

## <a name="resolution"></a><span data-ttu-id="f445d-123">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="f445d-123">Resolution</span></span>

- <span data-ttu-id="f445d-124">Atidarykite prekės **Numatytųjų užsakymo parametrų** puslapį ir išvalykite **Sustabdyta** žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="f445d-124">Open the **Default order settings** page for the item, and clear the **Stopped** checkbox.</span></span>
