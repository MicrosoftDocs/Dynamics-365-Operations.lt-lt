---
title: Biudžeto pasiūlymų įjungimas (peržiūros versija)
description: Šioje temoje paaiškinama, kaip įjungti modulio Finansinės įžvalgos funkciją Biudžeto pasiūlymas.
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
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222539"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="0b673-103">Biudžeto pasiūlymų įjungimas (peržiūros versija)</span><span class="sxs-lookup"><span data-stu-id="0b673-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="0b673-104">Šioje temoje paaiškinama, kaip įjungti modulio Finansinės įžvalgos funkciją Biudžeto pasiūlymas.</span><span class="sxs-lookup"><span data-stu-id="0b673-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="0b673-105">Naudokite informaciją iš aplinkos puslapio portale „Microsoft Dynamics Lifecycle Services“ (LCS), kad prisijungtumėte prie pirminio „Azure SQL“ tos aplinkos egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="0b673-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="0b673-106">Norėdami įjungti smėlio dėžės aplinkos testus, vykdykite tolesnę Transact-SQL (T-SQL) komandą.</span><span class="sxs-lookup"><span data-stu-id="0b673-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="0b673-107">(Gali reikėti įjungti prieigą prie savo IP adreso portale LCS, kad galėtumėte nuotoliniu būdu prisijungti prie programos objektų serverio \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="0b673-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="0b673-108">Praleiskite šį veiksmą, jei naudojate 10.0.20 ar vėlesnę versiją arba jei naudojate „Service Fabric“ diegimą.</span><span class="sxs-lookup"><span data-stu-id="0b673-108">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="0b673-109">Modulio „Finance Insights” komanda jums jau turėjo įjungti testą.</span><span class="sxs-lookup"><span data-stu-id="0b673-109">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="0b673-110">Jei nematote funkcijos darbo srityje **Funkcijų valdymas** arba jei kyla problemų bandant ją įjungti, kreipkitės adresu <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="0b673-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="0b673-111">Atidarykite darbo sritį **Funkcijų valdymas** ir atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0b673-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="0b673-112">Pasirinkite **Tikrinti, ar yra naujinimų**.</span><span class="sxs-lookup"><span data-stu-id="0b673-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="0b673-113">Ieškokite **Biudžeto pasiūlymas** ir įjunkite šią funkciją.</span><span class="sxs-lookup"><span data-stu-id="0b673-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="0b673-114">Nueikite į **Biudžeto sudarymas \> Sąranka \> Pagrindinio biudžeto sudarymas \> Biudžeto pasiūlymas (peržiūros versija)** ir pasirinkite **Įjungti funkciją**.</span><span class="sxs-lookup"><span data-stu-id="0b673-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
