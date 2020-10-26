---
title: Apdoroti mokėjimo grąžinimus
description: Ši procedūra nurodo, kaip konvertuoti patvirtintus ir apdorotus grąžinimus klientams į kredito pažymas.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 981068d26d232b10efd8d7288daaf7358aee3728
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980699"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="9f5c9-103">Apdoroti mokėjimo grąžinimus</span><span class="sxs-lookup"><span data-stu-id="9f5c9-103">Process rebates for payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9f5c9-104">Ši procedūra nurodo, kaip konvertuoti patvirtintus ir apdorotus grąžinimus klientams į kredito pažymas.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="9f5c9-105">Šį vadovą galite naudoti demonstracinėje įmonėje USMF.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="9f5c9-106">Išankstinė šio vadovo sąlyga – turėti vieną ar daugiau grąžinimo pretenzijų, kurių būsena yra „Žymėti“.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="9f5c9-107">Jei naudojate USMF, prieš šį vadovą rekomenduojama įvykdyti „Generuoti ir apdoroti kliento grąžinimus“.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-107">If you're using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="9f5c9-108">Konvertuoti grąžinimo pretenzijas į kredito pažymą</span><span class="sxs-lookup"><span data-stu-id="9f5c9-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="9f5c9-109">Eikite į „Visi klientai“.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-109">Go to All customers.</span></span>
2. <span data-ttu-id="9f5c9-110">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9f5c9-111">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9f5c9-112">Veiksmų srityje spustelėkite Rinkti.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="9f5c9-113">Spustelėkite „Sudengti operacijas“.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="9f5c9-114">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-114">Click Functions.</span></span>
7. <span data-ttu-id="9f5c9-115">Spustelėkite „Grąžinimo programa“.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-115">Click Rebate program.</span></span>
    * <span data-ttu-id="9f5c9-116">Puslapyje „Grąžinimai“ surašytos grąžinimo pretenzijos, kurias apdorojote kliento grąžinimų darbo srityje ir kurių būsena yra „Žymėti“.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="9f5c9-117">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-117">Click Edit.</span></span>
    * <span data-ttu-id="9f5c9-118">Lauke „Žymėti“ nustatykite žymes pretenzijose, kurias norite įtraukti į kredito pažymą.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="9f5c9-119">Spustelėkite Funkcijos.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-119">Click Functions.</span></span>
10. <span data-ttu-id="9f5c9-120">Spustelėkite „Sukurti kredito pažymą“.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-120">Click Create credit note.</span></span>
    * <span data-ttu-id="9f5c9-121">Rodomas pranešimas, kuris jus informuoja, kad žurnalas buvo užregistruotas (tai gautinų sumų suvartojimo žurnalas, kaip nurodyta puslapyje „Gautinų sumų parametrai“).</span><span class="sxs-lookup"><span data-stu-id="9f5c9-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="9f5c9-122">Tai lemia, kad tikrosios atsakomybės (kredito) suma perkeliama į kliento balansą.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="9f5c9-123">Tai reiškia, kad kliento sąskaita kredituojama, o grąžinimo kaupimo sąskaita debetuojama.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-123">This means that the customer's account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="9f5c9-124">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-124">Close the page.</span></span>
12. <span data-ttu-id="9f5c9-125">Spustelėkite Atšaukti.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-125">Click Cancel.</span></span>
    * <span data-ttu-id="9f5c9-126">Tai atnaujina puslapį, kad matytumėte atnaujinimus.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="9f5c9-127">Veiksmų srityje spustelėkite Rinkti.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="9f5c9-128">Spustelėkite „Sudengti operacijas“.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="9f5c9-129">Atkreipkite dėmesį, kad į kliento balansą įtraukta operacija su neigiama suma, kuri atitinka bendrą grąžinimo sumą, be sąskaitos faktūros nuorodos.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="9f5c9-130">Spustelėkite Atšaukti.</span><span class="sxs-lookup"><span data-stu-id="9f5c9-130">Click Cancel.</span></span>

