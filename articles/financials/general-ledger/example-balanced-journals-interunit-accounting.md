---
title: Susijusių vienetų apskaitos subalansuoti žurnalai
description: Šiame straipsnyje parodoma, kaip automatiškai subalansuojamas žurnalas, kai puslapyje Didžioji knyga pasirinkema balansavimo finansinė dimensija.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e84d96b5467b38e07a9ed31f142c27b638289284
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839358"
---
# <a name="balanced-journals-for-interunit-accounting"></a><span data-ttu-id="a8dd6-103">Susijusių vienetų apskaitos subalansuoti žurnalai</span><span class="sxs-lookup"><span data-stu-id="a8dd6-103">Balanced journals for interunit accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8dd6-104">Šiame straipsnyje parodoma, kaip automatiškai subalansuojamas žurnalas, kai puslapyje Didžioji knyga pasirinkema balansavimo finansinė dimensija.</span><span class="sxs-lookup"><span data-stu-id="a8dd6-104">This article shows how a journal is automatically balanced when a balancing financial dimension is selected on the Ledger page.</span></span> 

<span data-ttu-id="a8dd6-105">Jei apskaitos įrašai nesubalansuoti finansinės dimensijos reikšmių lygiu, papildomi sąskaitos įrašai yra sukuriami automatiškai, kad būtų subalansuotas žurnalas.</span><span class="sxs-lookup"><span data-stu-id="a8dd6-105">If account entries don't balance at the level of the financial dimension values, additional account entries are created automatically to balance the journal.</span></span> <span data-ttu-id="a8dd6-106">Šiuose sąskaitos įrašuose siekiant nustatyti pagrindinę sąskaitą naudojami puslapyje **Automatinių operacijų sąskaitos** esantys registravimo tipai **Susiję vienetai – debetas** ir**Susiję vienetai – kreditas**.</span><span class="sxs-lookup"><span data-stu-id="a8dd6-106">These account entries use the **Interunit - debit** and **Interunit - credit** posting types on the **Accounts for automatic transactions** page to determine the main account.</span></span> <span data-ttu-id="a8dd6-107">Pavyzdžiui, kaip balansavimo finansinė dimensija pažymėtas Verslo struktūros vienetas, kuris yra antrasis DK sąskaitos segmentas, ir netrukus bus sukurti kiti apskaitos įrašai.</span><span class="sxs-lookup"><span data-stu-id="a8dd6-107">For example, Business Unit, which is the second segment of the ledger account, is selected as the balancing financial dimension, and the following accounting entries are about to be created.</span></span>

|                      |           |
|----------------------|-----------|
| <span data-ttu-id="a8dd6-108">6100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="a8dd6-108">6100 – MSP – OU\_256</span></span> | <span data-ttu-id="a8dd6-109">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="a8dd6-109">100.00 DR</span></span> |
| <span data-ttu-id="a8dd6-110">6100 – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="a8dd6-110">6100 – NY – OU\_249</span></span>  | <span data-ttu-id="a8dd6-111">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="a8dd6-111">100.00 DR</span></span> |
| <span data-ttu-id="a8dd6-112">2100 – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="a8dd6-112">2100 – MSP – OU\_256</span></span> | <span data-ttu-id="a8dd6-113">200,00 CR</span><span class="sxs-lookup"><span data-stu-id="a8dd6-113">200.00 CR</span></span> |

<span data-ttu-id="a8dd6-114">Šiuo atveju nustatomi šie balansai:</span><span class="sxs-lookup"><span data-stu-id="a8dd6-114">In this case, the following balances are determined:</span></span>

-   <span data-ttu-id="a8dd6-115">Verslo vieneto kodas MSP = 100,00 CR</span><span class="sxs-lookup"><span data-stu-id="a8dd6-115">For Business Unit MSP = 100.00 CR</span></span>
-   <span data-ttu-id="a8dd6-116">Verslo vieneto kodas NY = 100,00 DR</span><span class="sxs-lookup"><span data-stu-id="a8dd6-116">For Business Unit NY = 100.00 DR</span></span>

<span data-ttu-id="a8dd6-117">Taigi toliau nurodyti apskaitos įrašai sukuriami automatiškai, siekiant subalansuoti žurnalą finansinių dimensijų reikšmių lygiu.</span><span class="sxs-lookup"><span data-stu-id="a8dd6-117">Therefore, the following accounting entries are created automatically to balance the  journal at the level of the financial dimension values.</span></span>

|                                   |           |
|-----------------------------------|-----------|
| <span data-ttu-id="a8dd6-118">(Susiję vienetai – debetas) – MSP – OU\_256</span><span class="sxs-lookup"><span data-stu-id="a8dd6-118">(Interunit Debit) – MSP – OU\_256</span></span> | <span data-ttu-id="a8dd6-119">100,00 DR</span><span class="sxs-lookup"><span data-stu-id="a8dd6-119">100.00 DR</span></span> |
| <span data-ttu-id="a8dd6-120">(Susiję vienetai – kreditas) – NY – OU\_249</span><span class="sxs-lookup"><span data-stu-id="a8dd6-120">(Interunit Credit) – NY – OU\_249</span></span> | <span data-ttu-id="a8dd6-121">100,00 CR</span><span class="sxs-lookup"><span data-stu-id="a8dd6-121">100.00 CR</span></span> |





