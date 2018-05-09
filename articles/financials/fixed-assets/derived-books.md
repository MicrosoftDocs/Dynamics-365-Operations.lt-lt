---
title: "Išvestinės knygos"
description: "Šiame straipsnyje apžvelgiamos išvestinių knygų funkcijos."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d5eafc08f793dfa4dee2ee15b9fe580e645f8f7b
ms.contentlocale: lt-lt
ms.lasthandoff: 05/08/2018

---

# <a name="derived-books"></a><span data-ttu-id="e2d25-103">Išvestinės knygos</span><span class="sxs-lookup"><span data-stu-id="e2d25-103">Derived books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2d25-104">Šiame straipsnyje apžvelgiamos išvestinių knygų funkcijos.</span><span class="sxs-lookup"><span data-stu-id="e2d25-104">This article provides an overview of derived book functionality.</span></span>

<span data-ttu-id="e2d25-105">Išvestinės knygos suteikia galimybę paprasčiau registruoti reguliariais intervalais planuojamas ilgalaikio turto knygų operacijas.</span><span class="sxs-lookup"><span data-stu-id="e2d25-105">The purpose of derived books is to simplify the posting of fixed asset book transactions that are planned for regular intervals.</span></span>  <span data-ttu-id="e2d25-106">Knygą reikia pasirinkti kaip pagrindinę knygą.</span><span class="sxs-lookup"><span data-stu-id="e2d25-106">You choose one book as the primary book.</span></span> <span data-ttu-id="e2d25-107">Paprastai tai yra knyga, naudojama apskaitos nusidėvėjimui.</span><span class="sxs-lookup"><span data-stu-id="e2d25-107">This usually is the book that is used for accounting depreciation.</span></span> <span data-ttu-id="e2d25-108">Tada prie jos pridedamos kitos knygos, kurios nustatytos operacijas registruoti tokiais pačiais intervalais kaip ir pagrindinė knyga.</span><span class="sxs-lookup"><span data-stu-id="e2d25-108">You then attach to it other books that are set up to post transactions in the same intervals as the primary book.</span></span> <span data-ttu-id="e2d25-109">Mokestinio nusidėvėjimo knygos dažnai nustatomos kaip išvestinės knygos.</span><span class="sxs-lookup"><span data-stu-id="e2d25-109">Tax depreciation books are often set up as derived books.</span></span> 

<span data-ttu-id="e2d25-110">Dažniausios operacijos, kurios nustatomos registruoti išvestinėse knygose, yra įsigijimai, įsigijimo koregavimai ir likvidavimai.</span><span class="sxs-lookup"><span data-stu-id="e2d25-110">The most common transactions to set up to post to derived books are acquisitions, acquisition adjustments, and disposals.</span></span> 

## <a name="example"></a><span data-ttu-id="e2d25-111">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="e2d25-111">Example</span></span>

<span data-ttu-id="e2d25-112">Knygos B ir C nustatomos kaip išvestinės tipo Įsigijimo operacija knygos A knygos.</span><span class="sxs-lookup"><span data-stu-id="e2d25-112">Book B and book C are set up as derived books for book A for the Acquisition transaction type.</span></span> <span data-ttu-id="e2d25-113">Knygoje A įveskite turto 123, kurio vertė 1 500,00, įsigijimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="e2d25-113">In book A, you enter an acquisition transaction for asset 123 for 1,500.00.</span></span> 

<span data-ttu-id="e2d25-114">Užregistravus operaciją, generuojama ir registruojama knygos B turto 123 ir knygos C turto 123 įsigijimo operacija, kurios 1 500,00.</span><span class="sxs-lookup"><span data-stu-id="e2d25-114">When the transaction is posted, an acquisition transaction is generated and posted in asset 123 for book B and in asset 123 for book C for 1,500.00.</span></span> <span data-ttu-id="e2d25-115">Kai ruošiate pagrindinės knygos operacijas registruoti ilgalaikio turto žurnale, taip pat galite peržiūrėti ir modifikuoti išvestinių knygų operacijas.</span><span class="sxs-lookup"><span data-stu-id="e2d25-115">When you prepare the transactions of the primary book for posting in the fixed asset journal, you can also view and modify the transactions of the derived books.</span></span> <span data-ttu-id="e2d25-116">Jei pagrindinės knygos operacijas ruošiate kitame žurnale, išvestinių nusidėvėjimo knygų operacijos nerodomos.</span><span class="sxs-lookup"><span data-stu-id="e2d25-116">If you prepare the primary book transactions in another journal, the transactions of the derived value are not displayed.</span></span> <span data-ttu-id="e2d25-117">Tačiau, kai registruojate pagrindinės knygos operacijas, jos registruojamos atitinkamose sąskaitose ir registravimo sluoksniuose.</span><span class="sxs-lookup"><span data-stu-id="e2d25-117">However, they are posted to the appropriate accounts and posting layers when you post the primary book transactions.</span></span>

> [!NOTE]                                                                                                                               
> <span data-ttu-id="e2d25-118">Knygos, nustatytos registruoti operacijas kitokiais intervalais negu pagrindinė knyga, turi būti susietos su ilgalaikiu turtu kaip atskiros knygos, o ne kaip išvestinės knygos.</span><span class="sxs-lookup"><span data-stu-id="e2d25-118">Books that are set up to post transactions at intervals other than the primary book intervals must be attached to the fixed asset as separate books and not as derived books.</span></span>  

<span data-ttu-id="e2d25-119">Daugiau informacijos žr. [Registravimas naudojant išvestines knygas](post-derived-value-models.md).</span><span class="sxs-lookup"><span data-stu-id="e2d25-119">For more information, see [Posting with derived books](post-derived-value-models.md).</span></span>




