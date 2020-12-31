---
title: Grynųjų pinigų srautų prognozavimo įjungimas (peržiūros versija)
description: Šioje temoje paaiškinama, kaip įjungti modulio Finansinės įžvalgos funkciją Grynųjų pinigų srautų prognozės.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 321c716c10b136769ea3a48a3b60a8a717798338
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646234"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="3e724-103">Grynųjų pinigų srautų prognozavimo įjungimas (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="3e724-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3e724-104">Šioje temoje paaiškinama, kaip įjungti modulio Finansinės įžvalgos funkciją Grynųjų pinigų srautų prognozės.</span><span class="sxs-lookup"><span data-stu-id="3e724-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="3e724-105">Norėdami grynųjų pinigų sraute naudoti mokėjimo prognozes, turite nustatyti funkciją Kliento mokėjimo prognozės, kaip aprašyta temoje [Kliento mokėjimo prognozių įjungimas](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="3e724-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="3e724-106">Naudokite informaciją iš aplinkos puslapio portale „Microsoft Dynamics Lifecycle Services“ (LCS), kad prisijungtumėte prie pirminio „Azure SQL“ tos aplinkos egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="3e724-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="3e724-107">Norėdami įjungti smėlio dėžės aplinkos testus, vykdykite tolesnę Transact-SQL (T-SQL) komandą.</span><span class="sxs-lookup"><span data-stu-id="3e724-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="3e724-108">(Gali reikėti įjungti prieigą prie savo IP adreso portale LCS, kad galėtumėte nuotoliniu būdu prisijungti prie programos objektų serverio \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="3e724-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="3e724-109">Jei jūsų „Microsoft Dynamics 365 Finance“ įdiegtis yra „Service Fabric“ įdiegtis, galite praleisti šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="3e724-109">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="3e724-110">Modulio Finansinės įžvalgos komanda jums jau turėjo įjungti testą.</span><span class="sxs-lookup"><span data-stu-id="3e724-110">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="3e724-111">Jei nematote funkcijų darbo srityje **Funkcijų valdymas** arba jei kyla problemų bandant jas įjungti, kreipkitės adresu <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="3e724-111">If you don't see the features in the **Feature management** workspace, or if experience issues when you try to turn them on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="3e724-112">Atidarykite darbo sritį **Funkcijų valdymas** ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3e724-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="3e724-113">Pasirinkite **Tikrinti, ar yra naujinimų**.</span><span class="sxs-lookup"><span data-stu-id="3e724-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="3e724-114">Įjunkite tolesnes funkcijas.</span><span class="sxs-lookup"><span data-stu-id="3e724-114">Turn on the following features:</span></span>

        - <span data-ttu-id="3e724-115">Naujas tinklelio valdiklis</span><span class="sxs-lookup"><span data-stu-id="3e724-115">New grid control</span></span>
        - <span data-ttu-id="3e724-116">Grupavimas tinklelyje (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="3e724-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="3e724-117">Klientų mokėjimų numatymai (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="3e724-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="3e724-118">Grynųjų pinigų srauto prognozės (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="3e724-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="3e724-119">Eikite į **Grynųjų pinigų ir banko valdymas \> Grynųjų pinigų srautų prognozių sąranka** ir įtraukite likvidumo sąskaitas, kurios turi būti įtrauktos į prognozes.</span><span class="sxs-lookup"><span data-stu-id="3e724-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3e724-120">Jei likvidumo sąskaitos nenustatytos, grynųjų pinigų srauto sugeneruoti negalima.</span><span class="sxs-lookup"><span data-stu-id="3e724-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="3e724-121">Eikite į **Grynųjų pinigų ir banko valdymas \> Sąranka \> Finansinės įžvalgos (peržiūros versija) \> Grynųjų pinigų srautų prognozes (peržiūros versija)** ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3e724-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="3e724-122">Skirtuke **Grynųjų pinigų srautų prognozė** pasirinkite **Įjungti funkciją**.</span><span class="sxs-lookup"><span data-stu-id="3e724-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="3e724-123">Pasirinkite **Sukurti prognozavimo modelį**.</span><span class="sxs-lookup"><span data-stu-id="3e724-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="3e724-124">Daugiau informacijos apie grynųjų pinigų srautų prognozavimo galimybę žr. [Grynųjų pinigų srautų prognozavimas](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="3e724-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="3e724-125">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="3e724-125">Privacy notice</span></span>

<span data-ttu-id="3e724-126">Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.</span><span class="sxs-lookup"><span data-stu-id="3e724-126">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
