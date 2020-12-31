---
title: Biudžeto pasiūlymų įjungimas (peržiūros versija)
description: Šioje temoje paaiškinama, kaip įjungti modulio Finansinės įžvalgos funkciją Biudžeto pasiūlymas.
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
ms.openlocfilehash: d8443c4e3e6f3d3a90acedc7c05b2846d6b68369
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646210"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="406ee-103">Biudžeto pasiūlymų įjungimas (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="406ee-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="406ee-104">Šioje temoje paaiškinama, kaip įjungti modulio Finansinės įžvalgos funkciją Biudžeto pasiūlymas.</span><span class="sxs-lookup"><span data-stu-id="406ee-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="406ee-105">Naudokite informaciją iš aplinkos puslapio portale „Microsoft Dynamics Lifecycle Services“ (LCS), kad prisijungtumėte prie pirminio „Azure SQL“ tos aplinkos egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="406ee-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="406ee-106">Norėdami įjungti smėlio dėžės aplinkos testus, vykdykite tolesnę Transact-SQL (T-SQL) komandą.</span><span class="sxs-lookup"><span data-stu-id="406ee-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="406ee-107">(Gali reikėti įjungti prieigą prie savo IP adreso portale LCS, kad galėtumėte nuotoliniu būdu prisijungti prie programos objektų serverio \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="406ee-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="406ee-108">Jei jūsų „Microsoft Dynamics 365 Finance“ įdiegtis yra „Service Fabric“ įdiegtis, galite praleisti šį veiksmą.</span><span class="sxs-lookup"><span data-stu-id="406ee-108">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="406ee-109">Modulio Finansinės įžvalgos komanda jums jau turėjo įjungti testą.</span><span class="sxs-lookup"><span data-stu-id="406ee-109">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="406ee-110">Jei nematote funkcijos darbo srityje **Funkcijų valdymas** arba jei, bandant jas įjungti, kyla problemų, atsiųskite el. laišką [programos Finansinės įžvalgos peržiūros versijos komandai](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="406ee-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, send email to the [Finance Insights App Preview team](mailto:fiap@microsoft.com).</span></span>

2. <span data-ttu-id="406ee-111">Atidarykite darbo sritį **Funkcijų valdymas** ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="406ee-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="406ee-112">Pasirinkite **Tikrinti, ar yra naujinimų**.</span><span class="sxs-lookup"><span data-stu-id="406ee-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="406ee-113">Ieškokite **Biudžeto pasiūlymas** ir įjunkite šią funkciją.</span><span class="sxs-lookup"><span data-stu-id="406ee-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="406ee-114">Nueikite į **Biudžeto sudarymas \> Sąranka \> Pagrindinio biudžeto sudarymas \> Biudžeto pasiūlymas (peržiūros versija)** ir pasirinkite **Įjungti funkciją**.</span><span class="sxs-lookup"><span data-stu-id="406ee-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="406ee-115">Privatumo pranešimas</span><span class="sxs-lookup"><span data-stu-id="406ee-115">Privacy notice</span></span>
<span data-ttu-id="406ee-116">Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.</span><span class="sxs-lookup"><span data-stu-id="406ee-116">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
