---
title: Prieš patvirtinant suplanuotą gamybos užsakymą, reikia sudaryti jo grafiką
description: Kai bandote patvirtinti suplanuotą užsakymą, gaunate klaidos pranešimą, kuriame teigiama, kad prieš patvirtinant užsakymą, turi būti sudarytas jo grafikas.
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
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294141"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a><span data-ttu-id="79172-103">Prieš patvirtinant suplanuotą gamybos užsakymą, reikia sudaryti jo grafiką</span><span class="sxs-lookup"><span data-stu-id="79172-103">Planned production order must be scheduled before it can be firmed</span></span>

<span data-ttu-id="79172-104">Klaidos kodas: SYS309802</span><span class="sxs-lookup"><span data-stu-id="79172-104">Error code: SYS309802</span></span>

## <a name="symptoms"></a><span data-ttu-id="79172-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="79172-105">Symptoms</span></span>

<span data-ttu-id="79172-106">Kai bandote patvirtinti suplanuotą užsakymą, gaunate tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="79172-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="79172-107">Prieš patvirtinant suplanuotą gamybos užsakymą, reikia sudaryti jo grafiką.</span><span class="sxs-lookup"><span data-stu-id="79172-107">The planned production order must be scheduled before it can be firmed.</span></span>

## <a name="cause"></a><span data-ttu-id="79172-108">Priežastis</span><span class="sxs-lookup"><span data-stu-id="79172-108">Cause</span></span>

<span data-ttu-id="79172-109">Suplanuotos pradžios ir pabaigos datos negali būti tuščios.</span><span class="sxs-lookup"><span data-stu-id="79172-109">The scheduled start and end dates can't be blank.</span></span>

## <a name="resolution"></a><span data-ttu-id="79172-110">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="79172-110">Resolution</span></span>

<span data-ttu-id="79172-111">Norėdami nurodyti suplanuoto užsakymo pradžios ir pabaigos datas, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="79172-111">To specify start and end dates for the planned order, follow these steps.</span></span>

1. <span data-ttu-id="79172-112">Eikite į **Pagrindinis planavimas \> Pagrindinis planavimas \> Suplanuoti užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="79172-112">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="79172-113">Atidarykite reikalingą suplanuotą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="79172-113">Open the relevant planned order.</span></span>
1. <span data-ttu-id="79172-114">„FastTab” skirtuko **Bendra** skyriuje **Suplanuota** nurodykite datas **Pradžios data** ir **Pabaigos data** laukuose.</span><span class="sxs-lookup"><span data-stu-id="79172-114">On the **General** FastTab, in the **Scheduled** section, specify dates in the **Start date** and **End date** fields.</span></span>
