---
title: Aptarnavimo intervalų nustatymas
description: Aptarnavimo intervalas nurodo dažnumą, kokiu kuriamos aptarnavimo sutarčių eilučių aptarnavimo užsakymo eilutės, kai kuriate aptarnavimo užsakymus.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementinterval
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aee440226c4bda40f9f14b3b6b1edc2cc495574d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242474"
---
# <a name="set-up-service-intervals"></a><span data-ttu-id="c7bbf-103">Aptarnavimo intervalų nustatymas</span><span class="sxs-lookup"><span data-stu-id="c7bbf-103">Set up service intervals</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7bbf-104">Aptarnavimo intervalas nurodo dažnumą, kokiu kuriamos aptarnavimo sutarčių eilučių aptarnavimo užsakymo eilutės, kai kuriate aptarnavimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-104">Service interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders.</span></span>

1. <span data-ttu-id="c7bbf-105">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo sutartys** \> **Aptarnavimo intervalai**.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-105">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="c7bbf-106">Sukurkite naują aptarnavimo intervalą.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-106">Create a new service interval.</span></span>
3. <span data-ttu-id="c7bbf-107">Įveskite aptarnavimo intervalo ID ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-107">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="c7bbf-108">Pasirinkite diapazoną lauke **Diapazonas**.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-108">In the **Range** field, select the range.</span></span>
5. <span data-ttu-id="c7bbf-109">Lauke **Dažnumas** įrašykite dažnumą.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-109">In the **Frequency** field, type the frequency.</span></span> <span data-ttu-id="c7bbf-110">Dažnumas yra koeficientas, iš kurio turite dauginti diapazoną, kad gautumėte aptarnavimo sutarties intervalą.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-110">The frequency is the factor by which you must multiply the range to obtain the interval for a service agreement.</span></span>
6. <span data-ttu-id="c7bbf-111">Norėdami įrašyti aptarnavimo intervalą, paspauskite **ALT + S**.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-111">Press **Alt+S** to save the service interval.</span></span>

## <a name="example"></a><span data-ttu-id="c7bbf-112">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="c7bbf-112">Example</span></span>

<span data-ttu-id="c7bbf-113">Norite sukurti 10 dienų aptarnavimo intervalą.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-113">You want to create a service interval of 10 days.</span></span>

<span data-ttu-id="c7bbf-114">**Sukurkite 10 dienų aptarnavimo intervalą**</span><span class="sxs-lookup"><span data-stu-id="c7bbf-114">**Create a 10-day service interval**</span></span>

1. <span data-ttu-id="c7bbf-115">Spustelėkite **Aptarnavimo valdymas** \> **Sąranka** \> **Aptarnavimo sutartys** \> **Aptarnavimo intervalai**.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-115">Click **Service management** \> **Setup** \> **Service agreements** \> **Service intervals**.</span></span>
2. <span data-ttu-id="c7bbf-116">Sukurkite naują aptarnavimo intervalą.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-116">Create a new service interval.</span></span>
3. <span data-ttu-id="c7bbf-117">Įveskite aptarnavimo intervalo ID ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-117">Enter the ID and description of the service interval.</span></span>
4. <span data-ttu-id="c7bbf-118">Lauke **Diapazonas** pasirinkite **Kasdien**.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-118">In the **Range** field, select **Daily**.</span></span>
5. <span data-ttu-id="c7bbf-119">Lauke **Dažnumas** įveskite 10.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-119">In the **Frequency** field, type 10.</span></span>
6. <span data-ttu-id="c7bbf-120">Norėdami įrašyti aptarnavimo intervalą, paspauskite **ALT + S**.</span><span class="sxs-lookup"><span data-stu-id="c7bbf-120">Press **Alt+S** to save the service interval.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7bbf-121">Susijusios temos</span><span class="sxs-lookup"><span data-stu-id="c7bbf-121">Related topics</span></span>

[<span data-ttu-id="c7bbf-122">Aptarnavimo intervalai </span><span class="sxs-lookup"><span data-stu-id="c7bbf-122">Service intervals</span></span>](service-intervals.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]