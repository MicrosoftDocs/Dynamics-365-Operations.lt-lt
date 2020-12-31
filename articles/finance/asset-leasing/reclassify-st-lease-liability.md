---
title: Trumpalaikės nuomos įsipareigojimo dalies perklasifikavimas
description: Šioje temoje paaiškinama, kaip sukurti mėnesio žurnalo įrašą, siekiant perklasifikuoti nuomos įsipareigojimo dalį kaip trumpalaikį.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 46bcd396c93bc1d2944241165d438f8ccc013e20
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446186"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a><span data-ttu-id="cffba-103">Trumpalaikės nuomos įsipareigojimo dalies perklasifikavimas</span><span class="sxs-lookup"><span data-stu-id="cffba-103">Reclassify the short-term portion of lease liability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cffba-104">Šioje temoje paaiškinama, kaip sukurti mėnesio žurnalo įrašą, siekiant perklasifikuoti nuomos įsipareigojimo dalį kaip trumpalaikį.</span><span class="sxs-lookup"><span data-stu-id="cffba-104">This topic explains how to create a monthly journal entry to reclassify a portion of the lease liability as short-term.</span></span> <span data-ttu-id="cffba-105">Kai paketiniame procese pasirinktas grafikas yra **Trumpalaikės nuomos įsipareigojimo perklasifikavimas**, sukuriamas žurnalo įrašas.</span><span class="sxs-lookup"><span data-stu-id="cffba-105">When the schedule that is selected in the batch process is **Short-term lease liability reclass**, a journal entry is created.</span></span> <span data-ttu-id="cffba-106">Šis įrašas naudojamas dabartinei nuomos įsipareigojimo daliai užregistruoti paskutinę mėnesio dieną.</span><span class="sxs-lookup"><span data-stu-id="cffba-106">This entry is used to post the current portion of the lease liability on the last day of the month.</span></span> <span data-ttu-id="cffba-107">Tuo pačiu metu, atšaukimo įrašas registruojamas kaip pirmą kito mėnesio dieną.</span><span class="sxs-lookup"><span data-stu-id="cffba-107">At the same time, a reversal entry is posted as of the first day of the next month.</span></span>

<span data-ttu-id="cffba-108">Trumpalaikė nuomos įsipareigojimo dalis rodoma įsipareigojimų amortizavimo grafike.</span><span class="sxs-lookup"><span data-stu-id="cffba-108">The short-term portion of the lease liability is shown on the liability amortization schedule.</span></span> <span data-ttu-id="cffba-109">Užregistravus žurnalo įrašą, stulpelis **Įsipareigojimo perklasifikavimo žurnalas sukurtas** tampa prieinamas, o žurnalo ID taip pat įrašomas į grafiką.</span><span class="sxs-lookup"><span data-stu-id="cffba-109">When the journal entry is posted, the **Liability reclass journal created** column becomes available, and the journal ID is also filled in on the schedule.</span></span>

<span data-ttu-id="cffba-110">Norėdami sukurti ir užregistruoti trumpojo laikotarpio atsakomybės perklasifikavimo žurnalo įrašą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cffba-110">To create and post the short-term liability reclassification journal entry, follow these steps.</span></span>

1. <span data-ttu-id="cffba-111">Nueikite į **Turto nuoma \> Periodinė \> Paketinio žurnalo patvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="cffba-111">Go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span>
2. <span data-ttu-id="cffba-112">Dialogo lango **Paketinio žurnalo kūrimas** lauke **Pasirinkite grafiką** pasirinkite **Trumpalaikės nuomos įsipareigojimo perklasifikavimas**.</span><span class="sxs-lookup"><span data-stu-id="cffba-112">In the **Batch journal creation** dialog box, in the **Select schedule** field, select **Short-term lease liability reclass**.</span></span>
3. <span data-ttu-id="cffba-113">Lauke **Nuomos grupė** pasirinkite nuomos grupę.</span><span class="sxs-lookup"><span data-stu-id="cffba-113">In the **Lease group** field, select a lease group.</span></span> <span data-ttu-id="cffba-114">Arba lauke **Knygos ID** pasirinkite knygos ID.</span><span class="sxs-lookup"><span data-stu-id="cffba-114">Alternatively, in the **Book ID** field, select the book ID.</span></span>
4. <span data-ttu-id="cffba-115">Įjunkite parametrą **Registruoti**.</span><span class="sxs-lookup"><span data-stu-id="cffba-115">Turn on the **Post** parameter.</span></span> <span data-ttu-id="cffba-116">Taip pat, jei įrašas turi būti sukurtas, bet neužregistruotas, šis parametras bus išjungtas.</span><span class="sxs-lookup"><span data-stu-id="cffba-116">Alternatively, if the entry should be created but not posted, leave this parameter turned off.</span></span>
5. <span data-ttu-id="cffba-117">Norėdami peržiūrėti įrašą prieš registruodami, įjunkite parametrą **Peržiūrėti prieš registruojant**.</span><span class="sxs-lookup"><span data-stu-id="cffba-117">Turn on the **Preview before posting** parameter to view the entry before it's posted.</span></span>
6. <span data-ttu-id="cffba-118">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="cffba-118">Select **OK**.</span></span>
