---
title: Grynųjų pinigų srautų prognozavimo įjungimas (peržiūros versija)
description: Šioje temoje paaiškinama, kaip įjungti modulio Finansinės įžvalgos funkciją Grynųjų pinigų srautų prognozės.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ba8acb2191291e2abed5cabf234c19fe09e6c8ff
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222563"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="f9655-103">Grynųjų pinigų srautų prognozavimo įjungimas (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="f9655-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f9655-104">Šioje temoje paaiškinama, kaip įjungti modulio Finansinės įžvalgos funkciją Grynųjų pinigų srautų prognozės.</span><span class="sxs-lookup"><span data-stu-id="f9655-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="f9655-105">Norėdami grynųjų pinigų sraute naudoti mokėjimo prognozes, turite nustatyti funkciją Kliento mokėjimo prognozės, kaip aprašyta temoje [Kliento mokėjimo prognozių įjungimas](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="f9655-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="f9655-106">Naudokite informaciją iš aplinkos puslapio portale „Microsoft Dynamics Lifecycle Services“ (LCS), kad prisijungtumėte prie pirminio „Azure SQL“ tos aplinkos egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="f9655-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="f9655-107">Norėdami įjungti smėlio dėžės aplinkos testus, vykdykite tolesnę Transact-SQL (T-SQL) komandą.</span><span class="sxs-lookup"><span data-stu-id="f9655-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="f9655-108">(Gali reikėti įjungti prieigą prie savo IP adreso portale LCS, kad galėtumėte nuotoliniu būdu prisijungti prie programos objektų serverio \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="f9655-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="f9655-109">Praleiskite šį veiksmą, jei naudojate 10.0.20 ar vėlesnę versiją arba jei naudojate „Service Fabric“ diegimą.</span><span class="sxs-lookup"><span data-stu-id="f9655-109">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="f9655-110">Modulio „Finance Insights” komanda jums jau turėjo įjungti testą.</span><span class="sxs-lookup"><span data-stu-id="f9655-110">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="f9655-111">Jei nematote funkcijos darbo srityje **Funkcijų valdymas** arba jei kyla problemų bandant ją įjungti, kreipkitės adresu <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="f9655-111">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="f9655-112">Atidarykite darbo sritį **Funkcijų valdymas** ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f9655-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="f9655-113">Pasirinkite **Tikrinti, ar yra naujinimų**.</span><span class="sxs-lookup"><span data-stu-id="f9655-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="f9655-114">Įjunkite tolesnes funkcijas.</span><span class="sxs-lookup"><span data-stu-id="f9655-114">Turn on the following features:</span></span>

        - <span data-ttu-id="f9655-115">Naujas tinklelio valdiklis</span><span class="sxs-lookup"><span data-stu-id="f9655-115">New grid control</span></span>
        - <span data-ttu-id="f9655-116">Grupavimas tinklelyje (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="f9655-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="f9655-117">Klientų mokėjimų numatymai (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="f9655-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="f9655-118">Grynųjų pinigų srauto prognozės (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="f9655-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="f9655-119">Eikite į **Grynųjų pinigų ir banko valdymas \> Grynųjų pinigų srautų prognozių sąranka** ir įtraukite likvidumo sąskaitas, kurios turi būti įtrauktos į prognozes.</span><span class="sxs-lookup"><span data-stu-id="f9655-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f9655-120">Jei likvidumo sąskaitos nenustatytos, grynųjų pinigų srauto sugeneruoti negalima.</span><span class="sxs-lookup"><span data-stu-id="f9655-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="f9655-121">Eikite į **Grynųjų pinigų ir banko valdymas \> Sąranka \> Finansinės įžvalgos (peržiūros versija) \> Grynųjų pinigų srautų prognozes (peržiūros versija)** ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f9655-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="f9655-122">Skirtuke **Grynųjų pinigų srautų prognozė** pasirinkite **Įjungti funkciją**.</span><span class="sxs-lookup"><span data-stu-id="f9655-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="f9655-123">Pasirinkite **Sukurti prognozavimo modelį**.</span><span class="sxs-lookup"><span data-stu-id="f9655-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="f9655-124">Daugiau informacijos apie grynųjų pinigų srautų prognozavimo galimybę žr. [Grynųjų pinigų srautų prognozavimas](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="f9655-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
