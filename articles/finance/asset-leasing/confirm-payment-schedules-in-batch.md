---
title: Paketinis modulio Turto nuoma mokėjimo grafikų patvirtinimas
description: Šioje temoje paaiškinama, kaip paketiniu būdu patvirtinti kelis mokėjimo grafikus.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9c680ea16e9f64107fde081c7e7763697356dcc1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971383"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="9b3be-103">Paketinis modulio Turto nuoma mokėjimo grafikų patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="9b3be-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b3be-104">Šioje temoje paaiškinama, kaip paketiniu būdu patvirtinti kelis mokėjimo grafikus.</span><span class="sxs-lookup"><span data-stu-id="9b3be-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="9b3be-105">Mokėjimo grafikai patvirtinami atskirai nuomai arba naudojant paketinio patvirtinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="9b3be-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="9b3be-106">Žurnalo įrašą galima registruoti tik pagal tokią nuomą, kuriai patvirtintas mokėjimo grafikas.</span><span class="sxs-lookup"><span data-stu-id="9b3be-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="9b3be-107">Mokėjimo grafiko patvirtinimas naudojamas kaip galutinis nuomos finansinės informacijos patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="9b3be-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="9b3be-108">Visi būsimi nuomos finansinės informacijos pakeitimai, pvz., mokėjimai ir nuomos terminas, sudaro nuomos koregavimą ir tokiu būdu turėtų būti apdorojami.</span><span class="sxs-lookup"><span data-stu-id="9b3be-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="9b3be-109">Norėdami patvirtinti keletą mokėjimo grafikų, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9b3be-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="9b3be-110">Nueikite į **Turto nuoma \> Periodinė \> Paketinis patvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="9b3be-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="9b3be-111">Puslapyje **Paketinis patvirtinimas** pasirinkite **Paketinis patvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="9b3be-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="9b3be-112">Pasirodžiusiame dialogo lange filtruokite knygas, kurias norite patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="9b3be-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="9b3be-113">Norėdami patvirtinti visas tam tikros nuomos grupės knygas, pasirinkite grupę lauke **Nuomos grupė**.</span><span class="sxs-lookup"><span data-stu-id="9b3be-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="9b3be-114">Norėdami patvirtinti konkrečias knygas, pasirinkite knygas lauke **Knygos ID**.</span><span class="sxs-lookup"><span data-stu-id="9b3be-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="9b3be-115">Norėdami patvirtinti visas knygas, įjunkite parametrą **Visoms knygoms**.</span><span class="sxs-lookup"><span data-stu-id="9b3be-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="9b3be-116">Naujai patvirtintų knygų informacija rodoma puslapyje **Patvirtintos knygos**.</span><span class="sxs-lookup"><span data-stu-id="9b3be-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="9b3be-117">Kai patvirtinami mokėjimo grafikai, pradinio pripažinimo žurnalo įrašai gali būti registruojami pagal nuomas.</span><span class="sxs-lookup"><span data-stu-id="9b3be-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>
