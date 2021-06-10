---
title: Laukimo laikotarpių konfigūravimas
description: Programoje „Microsoft Dynamics 365 Human Resources“, laukimo dienos nustato etapą, kuris bus taikomas išmokų planams.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4973a2a3b2fcedcf2301c80b362cfb22c912bc49
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058493"
---
# <a name="configure-waiting-periods"></a><span data-ttu-id="f62e9-103">Laukimo laikotarpių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="f62e9-103">Configure waiting periods</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f62e9-104">Programoje „Microsoft Dynamics 365 Human Resources“, laukimo dienos nustato etapą, kuris bus taikomas išmokų planams.</span><span class="sxs-lookup"><span data-stu-id="f62e9-104">In Microsoft Dynamics 365 Human Resources, waiting days establish a milestone to use for benefit plans.</span></span> <span data-ttu-id="f62e9-105">Pavyzdžiui, trys mėnesiai nuo samdos dienos, pirma kiekvieno mėnesio diena arba šeši mėnesiai.</span><span class="sxs-lookup"><span data-stu-id="f62e9-105">For example, three months from hire date, the first of each month, or six months.</span></span>   

1. <span data-ttu-id="f62e9-106">Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Laukimo laikotarpiai**.</span><span class="sxs-lookup"><span data-stu-id="f62e9-106">In the **Benefits management** workspace, under **Setup**, select **Waiting periods**.</span></span>

2. <span data-ttu-id="f62e9-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f62e9-107">Select **New**.</span></span>

3. <span data-ttu-id="f62e9-108">Nurodyti šių laukų vertes:</span><span class="sxs-lookup"><span data-stu-id="f62e9-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f62e9-109">Laukas</span><span class="sxs-lookup"><span data-stu-id="f62e9-109">Field</span></span> | <span data-ttu-id="f62e9-110">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="f62e9-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f62e9-111">**Laukimo kodas**</span><span class="sxs-lookup"><span data-stu-id="f62e9-111">**Waiting code**</span></span> | <span data-ttu-id="f62e9-112">Laukimo laikotarpio unikalusis identifikatorius.</span><span class="sxs-lookup"><span data-stu-id="f62e9-112">A unique identifier for the waiting period.</span></span> |
   | <span data-ttu-id="f62e9-113">**Aprašymas**</span><span class="sxs-lookup"><span data-stu-id="f62e9-113">**Description**</span></span> | <span data-ttu-id="f62e9-114">Laukimo laikotarpio aprašymas.</span><span class="sxs-lookup"><span data-stu-id="f62e9-114">A description of the waiting period.</span></span> |
   | <span data-ttu-id="f62e9-115">**Laukimo metodas**</span><span class="sxs-lookup"><span data-stu-id="f62e9-115">**Waiting method**</span></span> | <span data-ttu-id="f62e9-116">Išplečiamajame verčių sąraše pasirinkite tinkamą laukimo metodą.</span><span class="sxs-lookup"><span data-stu-id="f62e9-116">Select the appropriate waiting method from the drop-down list of values.</span></span> <span data-ttu-id="f62e9-117">Pasirinktys yra tokios: grynasis, šis mėnuo, šis ketvirtis, šie metai ir ši savaitė.</span><span class="sxs-lookup"><span data-stu-id="f62e9-117">Options are Net, Current month, Current quarter, Current year, and Current week.</span></span> |
   | <span data-ttu-id="f62e9-118">**Mėnesiai**</span><span class="sxs-lookup"><span data-stu-id="f62e9-118">**Months**</span></span> | <span data-ttu-id="f62e9-119">Įvesti mėnesių, pridedamų prie laukimo metodo skaičiuojant laukimo datą, skaičių.</span><span class="sxs-lookup"><span data-stu-id="f62e9-119">Enter the number of months to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="f62e9-120">**Dienos**</span><span class="sxs-lookup"><span data-stu-id="f62e9-120">**Days**</span></span> | <span data-ttu-id="f62e9-121">Įvesti dienų, pridedamų prie laukimo metodo skaičiuojant laukimo datą, skaičių.</span><span class="sxs-lookup"><span data-stu-id="f62e9-121">Enter the number of days to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="f62e9-122">**Laukimo diena**</span><span class="sxs-lookup"><span data-stu-id="f62e9-122">**Waiting day**</span></span> | <span data-ttu-id="f62e9-123">Pasirinkti laukimo dieną, naudojamą laukimo datai skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="f62e9-123">Select the waiting day to use to calculate the waiting date.</span></span> |

4. <span data-ttu-id="f62e9-124">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f62e9-124">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]