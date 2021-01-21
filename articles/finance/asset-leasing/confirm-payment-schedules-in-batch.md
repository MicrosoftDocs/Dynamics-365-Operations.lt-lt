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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b5a90b96ac598d145e2b0697627de04731b55f59
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446195"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="07252-103">Paketinis modulio Turto nuoma mokėjimo grafikų patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="07252-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07252-104">Šioje temoje paaiškinama, kaip paketiniu būdu patvirtinti kelis mokėjimo grafikus.</span><span class="sxs-lookup"><span data-stu-id="07252-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="07252-105">Mokėjimo grafikai patvirtinami atskirai nuomai arba naudojant paketinio patvirtinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="07252-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="07252-106">Žurnalo įrašą galima registruoti tik pagal tokią nuomą, kuriai patvirtintas mokėjimo grafikas.</span><span class="sxs-lookup"><span data-stu-id="07252-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="07252-107">Mokėjimo grafiko patvirtinimas naudojamas kaip galutinis nuomos finansinės informacijos patvirtinimas.</span><span class="sxs-lookup"><span data-stu-id="07252-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="07252-108">Visi būsimi nuomos finansinės informacijos pakeitimai, pvz., mokėjimai ir nuomos terminas, sudaro nuomos koregavimą ir tokiu būdu turėtų būti apdorojami.</span><span class="sxs-lookup"><span data-stu-id="07252-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="07252-109">Norėdami patvirtinti keletą mokėjimo grafikų, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="07252-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="07252-110">Nueikite į **Turto nuoma \> Periodinė \> Paketinis patvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="07252-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="07252-111">Puslapyje **Paketinis patvirtinimas** pasirinkite **Paketinis patvirtinimas**.</span><span class="sxs-lookup"><span data-stu-id="07252-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="07252-112">Pasirodžiusiame dialogo lange filtruokite knygas, kurias norite patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="07252-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="07252-113">Norėdami patvirtinti visas tam tikros nuomos grupės knygas, pasirinkite grupę lauke **Nuomos grupė**.</span><span class="sxs-lookup"><span data-stu-id="07252-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="07252-114">Norėdami patvirtinti konkrečias knygas, pasirinkite knygas lauke **Knygos ID**.</span><span class="sxs-lookup"><span data-stu-id="07252-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="07252-115">Norėdami patvirtinti visas knygas, įjunkite parametrą **Visoms knygoms**.</span><span class="sxs-lookup"><span data-stu-id="07252-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="07252-116">Naujai patvirtintų knygų informacija rodoma puslapyje **Patvirtintos knygos**.</span><span class="sxs-lookup"><span data-stu-id="07252-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="07252-117">Kai patvirtinami mokėjimo grafikai, pradinio pripažinimo žurnalo įrašai gali būti registruojami pagal nuomas.</span><span class="sxs-lookup"><span data-stu-id="07252-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>