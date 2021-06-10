---
title: Jūs esate paraginamas įrašyti prekės padengimo parametrus, net jei neatlikote jokių pakeitimų
description: Jūs esate paraginamas įrašyti prekės padengimo parametrus, net jei neatlikote jokių pakeitimų.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049480"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a><span data-ttu-id="21e8d-103">Jūs esate paraginamas įrašyti prekės padengimo parametrus, net jei neatlikote jokių pakeitimų</span><span class="sxs-lookup"><span data-stu-id="21e8d-103">You're prompted to save item coverage settings even though you made no changes</span></span>

<span data-ttu-id="21e8d-104">KB numeris: 4615588</span><span class="sxs-lookup"><span data-stu-id="21e8d-104">KB number: 4615588</span></span>

## <a name="symptoms"></a><span data-ttu-id="21e8d-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="21e8d-105">Symptoms</span></span>

<span data-ttu-id="21e8d-106">Kai kuriais scenarijais galite gauti toliau pateiktą pranešimą, kai atidarote **Prekės padengimo** puslapį po prekių importavimo per *Prekės padengimo V2* objektą:</span><span class="sxs-lookup"><span data-stu-id="21e8d-106">In some scenarios, you might receive the following message when you open the **Item coverage** page after you import items through the *Item coverage V2* entity:</span></span>

> <span data-ttu-id="21e8d-107">Ar prieš uždarant įrašyti konfigūracijos keitimus?</span><span class="sxs-lookup"><span data-stu-id="21e8d-107">Do you want to save your changes before closing?</span></span>

<span data-ttu-id="21e8d-108">Jūs gaunate šį pranešimą, nors neatlikote jokių pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="21e8d-108">You receive this message even though you haven't made any changes.</span></span>

## <a name="resolution"></a><span data-ttu-id="21e8d-109">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="21e8d-109">Resolution</span></span>

<span data-ttu-id="21e8d-110">**Prekių padengimo** puslapyje įtraukta sudėtinga numatytoji logika, kuri gali sąlygoti pranešimo rodymą po to, kai atliksite tiesioginius pakeitimus duomenų bazėje, pavyzdžiui, importuodami objektą.</span><span class="sxs-lookup"><span data-stu-id="21e8d-110">The **Item coverage** page includes complex defaulting logic that might cause the message to be shown after direct changes have recently been made in the database, such as through entity import.</span></span> <span data-ttu-id="21e8d-111">Pavyzdžiui, objekto „`AREGENERALSETTINGSOVERRIDDEN`” laukas nustatytas į *Ne*, tačiau importuojate failą, pateikiantį naujas arba modifikuotas laukų reikšmes, tokias kaip „`PRODUCTCOVERAGEGROUPID`” ir (arba) „`VENDORACCOUNTNUMBER`”.</span><span class="sxs-lookup"><span data-stu-id="21e8d-111">For example, the `AREGENERALSETTINGSOVERRIDDEN` entity field is set to *No*, but you import a file that provides new or modified values for fields such as `PRODUCTCOVERAGEGROUPID` and/or `VENDORACCOUNTNUMBER`.</span></span> <span data-ttu-id="21e8d-112">Šiuo atveju, kadangi laukas „`AREGENERALSETTINGSOVERRIDDEN`” nustatytas į *Ne*, reikšmės yra automatiškai išvalomos iš laukų, kai pirmą kartą atidarote **Prekių padengimo** puslapį po importavimo.</span><span class="sxs-lookup"><span data-stu-id="21e8d-112">In this case, because the `AREGENERALSETTINGSOVERRIDDEN` field is set to *No*, the values are automatically cleared from the fields when you open the **Item coverage** page for the first time after the import.</span></span> <span data-ttu-id="21e8d-113">Jeigu įrašote pakeitimus kaip pranešimų langelio raginimus, jie yra saugomi duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="21e8d-113">If you save the changes as the message box prompts, they are stored in the database.</span></span> <span data-ttu-id="21e8d-114">Kitu atveju, gausite tą patį pranešimą, kai atidarysite puslapį kitą kartą.</span><span class="sxs-lookup"><span data-stu-id="21e8d-114">Otherwise, you will receive the same message the next time that you open the page.</span></span>

<span data-ttu-id="21e8d-115">Norėdami išvengti tokio veikimo būdo, bet įtraukti ir tokių laukų, kaip „`PRODUCTCOVERAGEGROUPID`” reikšmes per objekto importavimą, nustatykite „`AREGENERALSETTINGSOVERRIDDEN`” į *Taip*, kai importuojate.</span><span class="sxs-lookup"><span data-stu-id="21e8d-115">To prevent this behavior but also include values for fields such as `PRODUCTCOVERAGEGROUPID` through entity import, set `AREGENERALSETTINGSOVERRIDDEN` to *Yes* when you import.</span></span>
