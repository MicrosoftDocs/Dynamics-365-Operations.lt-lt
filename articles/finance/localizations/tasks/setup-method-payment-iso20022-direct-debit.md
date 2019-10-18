---
title: ISO20022 tiesioginio debeto mokėjimo būdo nustatymas
description: Šioje procedūroje parodoma, kaip nustatyti kliento mokėjimo būdą, skirtą atlikti ISO20022 tiesioginio debeto arba bet kokio kito tipo mokėjimą, naudojant elektronines ataskaitas.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d3c6d8157803e0a8d33520a0cd64fb725e8c9a3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174966"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="a69af-103">ISO20022 tiesioginio debeto mokėjimo būdo nustatymas</span><span class="sxs-lookup"><span data-stu-id="a69af-103">Setup method of payment for ISO20022 direct debit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a69af-104">Šioje procedūroje parodoma, kaip nustatyti kliento mokėjimo būdą, skirtą atlikti ISO20022 tiesioginio debeto arba bet kokio kito tipo mokėjimą, naudojant elektronines ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="a69af-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="a69af-105">Prieš atlikdami šią užduotį, turite nustatyti eksporto formato konfigūracijas ir mokėjimo sąskaitas.</span><span class="sxs-lookup"><span data-stu-id="a69af-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="a69af-106">Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonės DEMF.</span><span class="sxs-lookup"><span data-stu-id="a69af-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="a69af-107">Tai yra trečioji iš penkių procedūrų, kuriose apibūdinamas kliento mokėjimo naudojant elektroninių ataskaitų konfigūracijas procesas.</span><span class="sxs-lookup"><span data-stu-id="a69af-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="a69af-108">Pasirinkite Gautinos sumos > Mokėjimų sąranka > Mokėjimo būdai.</span><span class="sxs-lookup"><span data-stu-id="a69af-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="a69af-109">Norėdami rasti įrašus, naudokite spartųjį filtrą.</span><span class="sxs-lookup"><span data-stu-id="a69af-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a69af-110">Pvz., filtruokite lauką Mokėjimo būdas reikšme „ELEKTRONINIS“.</span><span class="sxs-lookup"><span data-stu-id="a69af-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="a69af-111">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="a69af-111">Click Edit.</span></span>
4. <span data-ttu-id="a69af-112">Lauke Mokėjimo sąskaita nurodykite reikšmes „DEMF OPER‟.</span><span class="sxs-lookup"><span data-stu-id="a69af-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="a69af-113">Išplėskite dalį Failo formatai.</span><span class="sxs-lookup"><span data-stu-id="a69af-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="a69af-114">Lauke Bendrosios elektroninės ataskaitos pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="a69af-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="a69af-115">Lauke Eksportuoti formato konfigūraciją įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="a69af-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="a69af-116">Sąraše pasirinkite ISO20022 tiesioginis debetas (DE).</span><span class="sxs-lookup"><span data-stu-id="a69af-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="a69af-117">Jei sąrašas yra tuščias, nėra importuotos ir aktyvios kliento mokėjimų eksporto formato konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="a69af-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="a69af-118">Lauke Reikalauti įgaliojimo pasirinkite Taip.</span><span class="sxs-lookup"><span data-stu-id="a69af-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="a69af-119">Pasirinkite kliento mokėjimo formatų parametrą Reikalauti įgaliojimo, kurį nustačius į mokėjimo pranešimą reikia įtraukti įgaliojimo informaciją, pvz., SEPA tiesioginis debetą.</span><span class="sxs-lookup"><span data-stu-id="a69af-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="a69af-120">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="a69af-120">Click Save.</span></span>

