---
title: Kelios paketo numerių atsargų operacijos, kai išjungtas faktinis atnaujinimas
description: Koreguous prekių, kurių paketo numerių grupės pasirinktis Faktiškai atnaujinus nustatyta kaip Ne, pirkimo užsakymo eilutę sukuriamos kelios atsargų operacijos.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026759"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a><span data-ttu-id="634d7-103">Kelios paketo numerių atsargų operacijos, kai išjungtas faktinis atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="634d7-103">Multiple inventory transactions for batch numbers when On physical update is disabled</span></span>

<span data-ttu-id="634d7-104">KB numeris: 4613390</span><span class="sxs-lookup"><span data-stu-id="634d7-104">KB number: 4613390</span></span>

## <a name="symptoms"></a><span data-ttu-id="634d7-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="634d7-105">Symptoms</span></span>

<span data-ttu-id="634d7-106">Koreguous prekių, kurių paketo numerių grupės pasirinktis Faktiškai atnaujinus nustatyta kaip **Ne pirkimo užsakymo** eilutę sukuriamos kelios atsargų *operacijos*.</span><span class="sxs-lookup"><span data-stu-id="634d7-106">Multiple inventory transactions are created after you adjust a purchase order line for items where the **On physical update** option of the batch number group is set to *No*.</span></span>

<span data-ttu-id="634d7-107">Kai kuriate prekę, kurios **paketo numerių grupės** pasirinktis Faktinis atnaujinimas nustatyta kaip *Ne*, sistema automatiškai sukuria naują paketo numerį, jei modifikuojate pirkimo eilutės kiekį ir išsaugote pirkimo užsakymo puslapį.</span><span class="sxs-lookup"><span data-stu-id="634d7-107">When you create an item where the **On physical update** option of the batch number group is set to *No*, the system automatically creates a new batch number if you modify a purchase line quantity and save the purchase order page.</span></span>

## <a name="resolution"></a><span data-ttu-id="634d7-108">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="634d7-108">Resolution</span></span>

<span data-ttu-id="634d7-109">Paketo **numerių grupių faktinio** atnaujinimo parametras veikia taip:</span><span class="sxs-lookup"><span data-stu-id="634d7-109">The **On physical update** setting for batch number groups works in the following way:</span></span>

- <span data-ttu-id="634d7-110">Kai pasirinktis nustatyta kaip *Taip*, nauji paketo numeriai kuriami tik po faktinio atnaujinimo (pvz., kai prekės siunčiamos arba gautos).</span><span class="sxs-lookup"><span data-stu-id="634d7-110">When the option is set to *Yes*, new batch numbers are created only after a physical update (for example, when items are shipped or received).</span></span>
- <span data-ttu-id="634d7-111">Kai pasirinktis nustatyta kaip *Ne*, kaskart, kai taikomas atnaujinimas, sukuriamas naujas paketo numeris (pavyzdžiui, kai prie pirkimo užsakymo pridedamas naujas kiekis).</span><span class="sxs-lookup"><span data-stu-id="634d7-111">When the option is set to *No*, a new batch number is created every time that an applicable update occurs (for example, when a new quantity is added to a purchase order).</span></span>
