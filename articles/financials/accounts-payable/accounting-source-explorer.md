---
title: Apskaitos šaltinių naršyklė
description: Šiame straipsnyje pateikiama informacija apie Apskaitos šaltinių naršyklę, kurią galite naudoti Didžiosios knygos apskaitos įrašų šaltinio informacijos išsamiai analizei atlikti.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de5de039c0e3332943bae4846768fc628810906e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "330200"
---
# <a name="accounting-source-explorer"></a><span data-ttu-id="f7f68-103">Apskaitos šaltinių naršyklė</span><span class="sxs-lookup"><span data-stu-id="f7f68-103">Accounting source explorer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7f68-104">Šiame straipsnyje pateikiama informacija apie Apskaitos šaltinių naršyklę, kurią galite naudoti Didžiosios knygos apskaitos įrašų šaltinio informacijos išsamiai analizei atlikti.</span><span class="sxs-lookup"><span data-stu-id="f7f68-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="f7f68-105">Apskaitos šaltinių naršyklė yra naujas puslapis, kuriame rodomas šaltinio informacija.</span><span class="sxs-lookup"><span data-stu-id="f7f68-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="f7f68-106">Galite naudoti apskaitos šaltinių naršyklę kaip atskirą įrankį arba su ja analizuoti DK apskaitos įrašus.</span><span class="sxs-lookup"><span data-stu-id="f7f68-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="f7f68-107">Pavyzdžiui, galite naudoti apskaitos šaltinių naršyklę, kad gautumėte išsamiausia šaltinio informaciją apie bandomąjį balansą arba kvito operaciją.</span><span class="sxs-lookup"><span data-stu-id="f7f68-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="f7f68-108">Galite naudoti eksportavimo į „MS Excel“ funkciją, kad dar labiau segmentuotumėte informaciją „Microsoft Excel“ (pvz., „PivotTable“ arba „PivotTable“ ataskaitoje).</span><span class="sxs-lookup"><span data-stu-id="f7f68-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="f7f68-109">Apskaitos šaltinių naršyklė visada rodo tą pačią bendrą sumą pagal DK sąskaitą, kurią rodo ir didžioji knyga (pvz., bandomojo balanso).</span><span class="sxs-lookup"><span data-stu-id="f7f68-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="f7f68-110">Kaip ir bandomajame balanse galima rodyti segmentus atskiruose stulpeliuose.</span><span class="sxs-lookup"><span data-stu-id="f7f68-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="f7f68-111">Tereikia pasirinkti tinkamą finansinės dimensijos rinkinį.</span><span class="sxs-lookup"><span data-stu-id="f7f68-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="f7f68-112">Galite naudoti parametrus norėdami nustatyti analizės datų intervalą.</span><span class="sxs-lookup"><span data-stu-id="f7f68-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="f7f68-113">Ši funkcija taip pat panaši į bandomojo balanso funkcijas.</span><span class="sxs-lookup"><span data-stu-id="f7f68-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="f7f68-114">Apskaitos šaltinių naršyklė rodo papildomą informaciją apie visus dokumentus, kurie naudoja šaltinio dokumentų sistemą, paremtą apskaitos paskirstymais ir, jei taikoma, projekto apskaitos paskirstymais.</span><span class="sxs-lookup"><span data-stu-id="f7f68-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="f7f68-115">Ši informacija apima piniginės sumos tipą, projektą, veiklą, kategoriją ir eilutės ypatybę.</span><span class="sxs-lookup"><span data-stu-id="f7f68-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="f7f68-116">Štai keletas analizės, kurią galite atlikti, pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="f7f68-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="f7f68-117">Nuokrypiai tarp pirkimo užsakymų ir tiekėjo SF, nes kiekvieną nuokrypį reprezentuoja piniginės sumos tipas, pvz., išlaidų nuokrypis</span><span class="sxs-lookup"><span data-stu-id="f7f68-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="f7f68-118">Apmokamos ir neapmokamos valandos ir išlaidos pagal projektą, verslo struktūros vienetą ir pagrindinę sąskaitą</span><span class="sxs-lookup"><span data-stu-id="f7f68-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="f7f68-119">Apie šaltinio dokumentus, kurie naudoja šaltinio dokumentų nuorodos tapatybės koncepciją, apskaitos šaltinių naršyklė rodo dar išsamesnę informaciją, pvz., klientą, tiekėją, darbuotoją, produktą, kiekį, vieneto tekstą ir aprašymus.</span><span class="sxs-lookup"><span data-stu-id="f7f68-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="f7f68-120">Štai keletas analizės, kurią galite atlikti, pavyzdžių:</span><span class="sxs-lookup"><span data-stu-id="f7f68-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="f7f68-121">Viešbučio išlaidos pagal verslo vienetą ir viešbučio prekės ženklą per ataskaitinį laikotarpį, remiantis išlaidų ataskaitomis</span><span class="sxs-lookup"><span data-stu-id="f7f68-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="f7f68-122">Nuolaidos pagal tiekėją, produktą, padalinį</span><span class="sxs-lookup"><span data-stu-id="f7f68-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="f7f68-123">Apskaitos šaltinių naršyklėje nuo šių dokumentų taip pat galima pereiti prie faktinio šaltinio dokumento.</span><span class="sxs-lookup"><span data-stu-id="f7f68-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>



