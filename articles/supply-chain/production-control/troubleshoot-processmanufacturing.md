---
title: Trikčių šalinimo proceso gamyba
description: Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti su proceso gamyba.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71ff5eeb2065a67281393777937d50237ab78d5e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259727"
---
# <a name="troubleshoot-process-manufacturing"></a><span data-ttu-id="66351-103">Trikčių šalinimo proceso gamyba</span><span class="sxs-lookup"><span data-stu-id="66351-103">Troubleshoot process manufacturing</span></span>

<span data-ttu-id="66351-104">Ši tema aprašo, kaip pataisyti bendras problemas, su kuriomis galite susidurti su proceso gamyba.</span><span class="sxs-lookup"><span data-stu-id="66351-104">This topic describes how to fix issues that you might encounter while you work with process manufacturing.</span></span>

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a><span data-ttu-id="66351-105">Naudodamas darbo kortelės įrenginį siekiant pranešti apie dalinį kiekį paskutiniame darbe gamybos užsakyme visi ankstesni darbai tame užsakyme turi progreso būseną ir automatiškai užbaigiami.</span><span class="sxs-lookup"><span data-stu-id="66351-105">When I use the job card device to report a partial quantity on the last job in a production order, all the previous jobs on that order that have a status of In progress are automatically ended.</span></span>

<span data-ttu-id="66351-106">Toks veikimo būdas yra numatytas.</span><span class="sxs-lookup"><span data-stu-id="66351-106">This behavior is by design.</span></span> <span data-ttu-id="66351-107">Puslapyje **Gamybos užsakymo nustatytosios vertės** skirtuke **Pranešti kaip baigtą** yra parinktis pavadinimus **Paskutinės žymos kelias**.</span><span class="sxs-lookup"><span data-stu-id="66351-107">On the **Production order defaults** page, on the **Report as finished** tab, there is an option that is named **End-mark route**.</span></span> <span data-ttu-id="66351-108">Jei ši tema nustatyta į *Taip*, kelio kortelės žurnalas yra viešinamas kaip darbuotojas naudoja darbo kortelės įrenginį ir darbo kortelės terminalą siekiant pranešti apie paskutinę operaciją.</span><span class="sxs-lookup"><span data-stu-id="66351-108">If this topic is set to *Yes*, a route card journal is posted when a worker uses the job card device or job card terminal to report the last operation.</span></span> <span data-ttu-id="66351-109">Šis žurnalas rodo visas operacijas kaip baigtas ir užbaigia visus gamybos darbus.</span><span class="sxs-lookup"><span data-stu-id="66351-109">This journal marks all the operations as completed and ends all the production jobs.</span></span> <span data-ttu-id="66351-110">Kai **Paskutinės žymos kelio** parinktis yra nustayta į *Taip*, sistema nebeatsižvelgia į darbo būseną, kurią darbuotojas pasirinko jam pranešant apie paskutinę operaciją.</span><span class="sxs-lookup"><span data-stu-id="66351-110">When the **End-mark route** option is set to *Yes*, the system doesn't consider the job status that the worker selected when they reported the last operation.</span></span> <span data-ttu-id="66351-111">Sistema taip pat neatsižvelgia į tai, ar darbuotojas praneša visą ar dalinį kiekį.</span><span class="sxs-lookup"><span data-stu-id="66351-111">The system also doesn't consider whether the worker is reporting a full or partial quantity.</span></span>

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a><span data-ttu-id="66351-112">Bandydamas uždaryti atsargas gaunu tolesnį įspėjimo pranešimą: „Nevykdomas „Backflush“ kaštų skaičiavimas su data %1 atitikties periodo pabaiga buvo registruota."</span><span class="sxs-lookup"><span data-stu-id="66351-112">When I attempt a stock closing, I receive the following warning message: "No execution of Backflush costing calculation with a date %1 matching period end has been registered."</span></span>

<span data-ttu-id="66351-113">Ankstesnėse nei 10.0.13 versijose, jei nenaudojate pasvirų gamybos kaštų srauto, gausite tolesnį neteisingą įspėjimo pranešimą uždarant inventorių:</span><span class="sxs-lookup"><span data-stu-id="66351-113">In releases before release 10.0.13, if you aren't using the lean production costing flow, you receive the following erroneous warning message during inventory closing:</span></span>

> <span data-ttu-id="66351-114">Jūs norite atlikti inventoriaus uždarymą su data %1.</span><span class="sxs-lookup"><span data-stu-id="66351-114">You are about to execute an Inventory close with a date %1.</span></span> <span data-ttu-id="66351-115">Nevykdomas „Backflush“ kaštų skaičiavimas su data %1 atitikties periodo pabaiga buvo registruota.</span><span class="sxs-lookup"><span data-stu-id="66351-115">No execution of Backflush costing calculation with a date %1 matching period end has been registered.</span></span> <span data-ttu-id="66351-116">Prašome prisiminti, kad turite atlikti „Backflush“ kaštų skaičiavimą pagal datą %1 su atitikties periodo pabaiga.</span><span class="sxs-lookup"><span data-stu-id="66351-116">Please remember to execute a Backflush costing calculation with a date of %1 matching period end.</span></span> <span data-ttu-id="66351-117">Inventoriaus įvertinimas, parduotų prekių kaina ir pakeitimai gali būti neteisingi papildomoje ar pagrindinėje buhalterijos knygoja, kol ji nebus įgyvendinta.</span><span class="sxs-lookup"><span data-stu-id="66351-117">The valuation of inventories, cost of goods sold and variances might not be correct in Subledger or General ledger until this has been executed.</span></span>

<span data-ttu-id="66351-118">Ši klaida buvo ištaisyta 10.0.13 leidime ir vėliau.</span><span class="sxs-lookup"><span data-stu-id="66351-118">This issue has been fixed in release 10.0.13 and later.</span></span> <span data-ttu-id="66351-119">Dėl išsamesnės informacijos: [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span><span class="sxs-lookup"><span data-stu-id="66351-119">For more information, see [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]