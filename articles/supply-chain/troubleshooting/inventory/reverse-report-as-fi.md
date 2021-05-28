---
title: Atšaukus ataskaitą kaip baigtą sukuriama netikėta atvira operacija
description: Skelbimo baigtu su žymėjimu atšaukimas sukuria atvirą operaciją, kurioje atšauktas kiekis turi tas pačias atsargų dimensijas kaip ir atšaukta operacija.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026757"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a><span data-ttu-id="86101-103">Atšaukus ataskaitą kaip baigtą sukuriama netikėta atvira operacija</span><span class="sxs-lookup"><span data-stu-id="86101-103">Reversal of reporting as finished creates an unexpected open transaction</span></span>

<span data-ttu-id="86101-104">KB numeris: 4612469</span><span class="sxs-lookup"><span data-stu-id="86101-104">KB number: 4612469</span></span>

## <a name="symptoms"></a><span data-ttu-id="86101-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="86101-105">Symptoms</span></span>

<span data-ttu-id="86101-106">Jei pakeičiate ataskaitą kaip baigtą su žymėjimu, sistema sukuria atvirą operaciją, kai pakeistas kiekis turi tas pačias atsargų dimensijas, kaip operacija, kuri buvo pakeista.</span><span class="sxs-lookup"><span data-stu-id="86101-106">If you reverse reporting as finished that has marking, the system creates an open transaction where the reversed quantity has the same inventory dimensions as the transaction that was reversed.</span></span>

## <a name="resolution"></a><span data-ttu-id="86101-107">Skiriamoji geba</span><span class="sxs-lookup"><span data-stu-id="86101-107">Resolution</span></span>

<span data-ttu-id="86101-108">Kai atšaukiate skelbimo baigtu operaciją, atsargų dimensija inicijuojama iš gamybos žurnalo.</span><span class="sxs-lookup"><span data-stu-id="86101-108">When you reverse a report-as-finished operation, the inventory dimension is initialized from the production journal.</span></span> <span data-ttu-id="86101-109">Todėl jis gauna paketo numerį.</span><span class="sxs-lookup"><span data-stu-id="86101-109">Therefore, it gets the batch number.</span></span> <span data-ttu-id="86101-110">Dėl žymėjimo pardavimo užsakymo operacijos paveldės paketo numerį.</span><span class="sxs-lookup"><span data-stu-id="86101-110">Because of marking, the sales order transactions will inherit the batch number.</span></span>

<span data-ttu-id="86101-111">Dimensiją galima nustatyti iš naujo registruojant ataskaitą kaip baigtą.</span><span class="sxs-lookup"><span data-stu-id="86101-111">The dimension can be reset when the reporting as finished is posted.</span></span>
