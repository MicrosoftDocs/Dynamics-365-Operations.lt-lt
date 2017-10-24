---
title: "Susijusių vienetų apskaitos subalansuoti žurnalai"
description: "Šiame straipsnyje parodoma, kaip automatiškai subalansuojamas žurnalas, kai puslapyje Didžioji knyga pasirinkema balansavimo finansinė dimensija."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="76339-103">Susijusių vienetų apskaitos subalansuoti žurnalai</span><span class="sxs-lookup"><span data-stu-id="76339-103">Balanced journals for interunit accounting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="76339-104">Šiame straipsnyje parodoma, kaip automatiškai subalansuojamas žurnalas, kai puslapyje Didžioji knyga pasirinkema balansavimo finansinė dimensija.</span><span class="sxs-lookup"><span data-stu-id="76339-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="76339-105">Jei apskaitos įrašai nesubalansuoti finansinės dimensijos reikšmių lygiu, papildomi sąskaitos įrašai yra sukuriami automatiškai, kad būtų subalansuotas žurnalas.</span><span class="sxs-lookup"><span data-stu-id="76339-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="76339-106">Šiuose sąskaitos įrašuose siekiant nustatyti pagrindinę sąskaitą naudojami puslapyje **Automatinių operacijų sąskaitos** esantys registravimo tipai **Susiję vienetai – debetas** ir**Susiję vienetai – kreditas**.</span><span class="sxs-lookup"><span data-stu-id="76339-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="76339-107">Pavyzdžiui, kaip balansavimo finansinė dimensija pažymėtas Filialas, kuris yra antrasis DK sąskaitos segmentas, ir netrukus bus sukurti kiti apskaitos įrašai.</span><span class="sxs-lookup"><span data-stu-id="76339-107">For example, Branch, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="76339-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="76339-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="76339-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="76339-109">100.00 DR</span></span> |
| <span data-ttu-id="76339-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="76339-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="76339-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="76339-111">100.00 DR</span></span> |
| <span data-ttu-id="76339-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="76339-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="76339-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="76339-113">200.00 CR</span></span> |

<span data-ttu-id="76339-114">Šiuo atveju nustatomi šie balansai:</span><span class="sxs-lookup"><span data-stu-id="76339-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="76339-115">Filialas MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="76339-115">For Branch MSP = 100.00 CR</span></span>
-   <span data-ttu-id="76339-116">Filialas NY = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="76339-116">For Branch NY = 100.00 DR</span></span>

<span data-ttu-id="76339-117">Taigi toliau nurodyti apskaitos įrašai sukuriami automatiškai, siekiant subalansuoti žurnalą finansinių dimensijų reikšmių lygiu.</span><span class="sxs-lookup"><span data-stu-id="76339-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="76339-118">(Susiję vienetai – debetas) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="76339-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="76339-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="76339-119">100.00 DR</span></span> |
| <span data-ttu-id="76339-120">(Susiję vienetai – kreditas) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="76339-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="76339-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="76339-121">100.00 CR</span></span> |






