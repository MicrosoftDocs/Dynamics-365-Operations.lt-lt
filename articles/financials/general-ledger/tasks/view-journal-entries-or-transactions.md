---
title: Žurnalo įrašai arba operacijos
description: Šioje procedūroje parodoma, kaip, naudojant užklausą Kvitų operacijos, ieškoti žurnalų įrašų ar operacijų.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, LedgerTransVoucher, LedgerTransBase, Originaldocuments
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 53e966a4caf6ee8907b05b5fd9c0978187d64f1d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566832"
---
# <a name="view-journal-entries-or-transactions"></a><span data-ttu-id="3f4a2-103">Žurnalo įrašai arba operacijos</span><span class="sxs-lookup"><span data-stu-id="3f4a2-103">View journal entries or transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3f4a2-104">Šioje procedūroje parodoma, kaip, naudojant užklausą Kvitų operacijos, ieškoti žurnalų įrašų ar operacijų.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-104">This procedure shows how to use the Voucher transactions inquiry to search for journal entries or transactions.</span></span>

1. <span data-ttu-id="3f4a2-105">Eikite į dalį Didžioji knyga > Užklausos ir ataskaitos > Kvitų operacijos.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-105">Go to General ledger > Inquiries and reports > Voucher transactions.</span></span>
2. <span data-ttu-id="3f4a2-106">Pasirinkite lauką, kuriame norite nustatyti filtro kriterijus.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-106">Select the field for which you want to define a filter criteria.</span></span>
3. <span data-ttu-id="3f4a2-107">Įveskite pasirinkto lauko filtro kriterijus.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-107">Enter your filter critieria for the selected field.</span></span>
    * <span data-ttu-id="3f4a2-108">Galite filtruoti pagal vieną reikšmę arba intervalą.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-108">You could filter on a single value or a range.</span></span> <span data-ttu-id="3f4a2-109">Apibrėždami intervalą patikrinkite, ar naudojama teisinga sintaksė.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-109">When defining a range, make sure the correct syntax is used.</span></span> <span data-ttu-id="3f4a2-110">Reikšmės turi būti atskirtos dviem taškais (..).</span><span class="sxs-lookup"><span data-stu-id="3f4a2-110">The values should be separated by a double period (..).</span></span>  
4. <span data-ttu-id="3f4a2-111">Spustelėkite skirtuką Sujungimai, norėdami įtraukti papildomų lentelių, pagal kurias norite filtruoti.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-111">Click the Joins tab to add additional tables from which to filter.</span></span>
5. <span data-ttu-id="3f4a2-112">Medyje pasirinkite Tables\General journal entry.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-112">In the tree, select 'Tables\General journal entry'.</span></span>
6. <span data-ttu-id="3f4a2-113">Spustelėkite Įtraukti lentelės sujungimą.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-113">Click Add table join.</span></span>
7. <span data-ttu-id="3f4a2-114">Spustelėkite Atšaukti, jei nenorite įtraukti papildomos lentelės.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-114">Click Cancel if you decide not to add an additional table.</span></span>
8. <span data-ttu-id="3f4a2-115">Spustelėkite skirtuką „Diapazonas“.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-115">Click the Range tab.</span></span>
9. <span data-ttu-id="3f4a2-116">Spustelėdami Gerai įvykdykite užklausą.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-116">Click OK to run the query.</span></span>
10. <span data-ttu-id="3f4a2-117">Spustelėkite Operacijos kilmė.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-117">Click Transaction origin.</span></span>
    * <span data-ttu-id="3f4a2-118">Galima naudoti įvairius tinklelio mygtukus, norint peržiūrėti papildomą informaciją apie pasirinktą kvito įrašą.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-118">Various buttons about the grid can be used to research additional information about the selected record of the voucher.</span></span> <span data-ttu-id="3f4a2-119">Kai kurie mygtukai gali neveikti, atsižvelgiant į operacijos tipą ir charakteristiką.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-119">Some buttons may not be available, depending on the type of transaction and characteristics of the transaction.</span></span>  
11. <span data-ttu-id="3f4a2-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-120">Close the page.</span></span>
12. <span data-ttu-id="3f4a2-121">Spustelėkite Pradinis dokumentas.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-121">Click Original document.</span></span>
13. <span data-ttu-id="3f4a2-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="3f4a2-122">Close the page.</span></span>

