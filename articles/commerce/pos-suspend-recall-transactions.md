---
title: Elektroninio kasos aparato (EKA) operacijos sustabdymas ir pratęsimas
description: Šioje temoje paaiškinama, kaip vartotojai gali sustabdyti vykdomas operacijas, o paskui jas tęsti vėliau arba kitame kasos aparate naudodami „Dynamics 365 Commerce“.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f513e2d857908f2b95d27bf48ff1e826724d7cbf
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414431"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a><span data-ttu-id="23ac5-103">Elektroninio kasos aparato (EKA) operacijos sustabdymas ir pratęsimas</span><span class="sxs-lookup"><span data-stu-id="23ac5-103">Suspend and resume a transaction in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="23ac5-104">Elektroninio kasos aparato (EKA) vartotojai gali sustabdyti vykdomas operacijas, o paskui jas tęsti vėliau arba kitame kasos aparate.</span><span class="sxs-lookup"><span data-stu-id="23ac5-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="23ac5-105">Operacijos dažnai sustabdomos tam, kad būtų galima greitai atlaisvinti kasos aparatą kitai užduočiai, neprarandant dabartinės operacijos vykdymo eigos.</span><span class="sxs-lookup"><span data-stu-id="23ac5-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="23ac5-106">Pavyzdžiui, parduotuvės atstovas pradeda apdoroti kliento operaciją mobiliajame įrenginyje, bet turi ją užbaigti kasos aparate, kuriame yra kasos stalčius.</span><span class="sxs-lookup"><span data-stu-id="23ac5-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="23ac5-107">Šiuo atveju parduotuvės atstovas gali sustabdyti operaciją mobiliajame įrenginyje, o paskui atšaukti ir ją tęsti kasos aparate.</span><span class="sxs-lookup"><span data-stu-id="23ac5-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="23ac5-108">Sustabdymo ir pratęsimo funkcijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="23ac5-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="23ac5-109">POS operacijos</span><span class="sxs-lookup"><span data-stu-id="23ac5-109">POS operations</span></span>

<span data-ttu-id="23ac5-110">Dvi [EKA operacijos](pos-operations.md) leidžia EKA palaikyti sustabdymo ir pratęsimo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="23ac5-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="23ac5-111">Šias operacijas galite priskirti [mygtukynams](pos-screen-layouts.md) operacijų arba darbo pradžios puslapiuose.</span><span class="sxs-lookup"><span data-stu-id="23ac5-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="23ac5-112">503: sustabdyti operaciją</span><span class="sxs-lookup"><span data-stu-id="23ac5-112">503: Suspend transaction</span></span>
- <span data-ttu-id="23ac5-113">504: atšaukti operaciją</span><span class="sxs-lookup"><span data-stu-id="23ac5-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="23ac5-114">Kvito šablonas</span><span class="sxs-lookup"><span data-stu-id="23ac5-114">Receipt template</span></span>

<span data-ttu-id="23ac5-115">EKA galima konfigūruoti važtaraščiui generuoti, kai operacija sustabdyta.</span><span class="sxs-lookup"><span data-stu-id="23ac5-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="23ac5-116">Paskui šį kvitą galima naudoti norint greitai identifikuoti ir vėliau atšaukti operaciją.</span><span class="sxs-lookup"><span data-stu-id="23ac5-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="23ac5-117">Norėdami įgalinti EKA spausdinti kvitą, turite įtraukti kvito formatą **Sustabdyta operacija** į parduotuvės kvitų šabloną.</span><span class="sxs-lookup"><span data-stu-id="23ac5-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="23ac5-118">Kvito formatą galite sudaryti taip, kad jis apimtų arba neįtrauktų konkrečių duomenų apie operaciją.</span><span class="sxs-lookup"><span data-stu-id="23ac5-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="23ac5-119">Pavyzdžiui, formatas gali apimti brūkšninį kodą nuskaitymui palaikyti.</span><span class="sxs-lookup"><span data-stu-id="23ac5-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="23ac5-120">Kvitų numeravimas</span><span class="sxs-lookup"><span data-stu-id="23ac5-120">Receipt numbering</span></span>

<span data-ttu-id="23ac5-121">Kaip ir kitiems EKA operacijų tipams, generuojantiems spausdintą kvitą, galite nurodyti sustabdytų operacijų numerių seką parduotuvės funkcijų šablono dalyje **Kvitų numeravimas**.</span><span class="sxs-lookup"><span data-stu-id="23ac5-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="23ac5-122">Anuliuoti uždarant pamainą</span><span class="sxs-lookup"><span data-stu-id="23ac5-122">Void when closing shift</span></span>

<span data-ttu-id="23ac5-123">Galite naudoti parinktį **Anuliuoti uždarant pamainą**, jei reikia, kad prieš uždarydami savo pamainą vartotojai užbaigtų arba anuliuotų visas sustabdytas operacijas.</span><span class="sxs-lookup"><span data-stu-id="23ac5-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="23ac5-124">Per operaciją **Uždaryti pamainą** EKA paragins vartotojus peržiūrėti arba anuliuoti visas neįvykdytas sustabdytas operacijas.</span><span class="sxs-lookup"><span data-stu-id="23ac5-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="23ac5-125">Sustabdyti ir tęsti operaciją</span><span class="sxs-lookup"><span data-stu-id="23ac5-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="23ac5-126">Sustabdyti operaciją</span><span class="sxs-lookup"><span data-stu-id="23ac5-126">Suspend a transaction</span></span>

<span data-ttu-id="23ac5-127">Vartotojai, turintys pakankamai teisių ir naudojantys ekrano maketą, kuris apima operaciją **Sustabdyti operaciją**, gali sustabdyti operaciją taip, kad ją būtų galima atšaukti vėliau arba kitame kasos aparate.</span><span class="sxs-lookup"><span data-stu-id="23ac5-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="23ac5-128">Operacijas galima sustabdyti tik tada, jei jose **nėra** šių eilučių tipų:</span><span class="sxs-lookup"><span data-stu-id="23ac5-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="23ac5-129">Aktyvios mokėjimo eilutės</span><span class="sxs-lookup"><span data-stu-id="23ac5-129">Active payment lines</span></span>
- <span data-ttu-id="23ac5-130">Dovanų kortelių eilutės (išduoti dovanų kortelę arba pridėti prie dovanų kortelės balanso)</span><span class="sxs-lookup"><span data-stu-id="23ac5-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="23ac5-131">Sustabdyta operacija neturi poveikio pardavimo informacijai arba informacijai apie atsargų likučius parduotuvėje.</span><span class="sxs-lookup"><span data-stu-id="23ac5-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="23ac5-132">Tęsti sustabdytą operaciją</span><span class="sxs-lookup"><span data-stu-id="23ac5-132">Resume a suspended transaction</span></span>

<span data-ttu-id="23ac5-133">Sustabdytas operacijas gali atšaukti ir toje pačioje parduotuvėje pratęsti bet kuris vartotojas, turintis pakankamai teisių ir taip pat naudojantis maketą, kuris apima operaciją **Atšaukti operaciją**.</span><span class="sxs-lookup"><span data-stu-id="23ac5-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="23ac5-134">Norėdami greitai ir lengvai atšaukti sustabdytą operaciją, nuskaitykite ant spausdinto kvito esantį brūkšninį kodą peržiūrėdami operacijos **Atšaukti operaciją** operacijų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="23ac5-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="23ac5-135">Autonominio režimo aplinkybės</span><span class="sxs-lookup"><span data-stu-id="23ac5-135">Considerations for offline mode</span></span>

- <span data-ttu-id="23ac5-136">Bet kokios sustabdytos operacijos, kol EKA veikia internetiniu režimu, negalima tęsti autonominiu režimu, nes duomenys su autonomine duomenų baze nesinchronizuojami.</span><span class="sxs-lookup"><span data-stu-id="23ac5-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="23ac5-137">Jei sustabdote operaciją, kol EKA veikia autonominiu režimu, galite ją atšaukti autonominiu režimu, jei EKA nebuvo perjungtas į internetinį režimą bet kuriuo metu nuo tada, kai sustabdėte operaciją.</span><span class="sxs-lookup"><span data-stu-id="23ac5-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="23ac5-138">EKA perjungus į internetinį režimą, duomenys apie sustabdytas operacijas perkeliami į internetinę duomenų bazę ir pašalinami iš autonominės duomenų bazės.</span><span class="sxs-lookup"><span data-stu-id="23ac5-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="23ac5-139">Todėl operacijas galima tęsti tik internetiniu režimu.</span><span class="sxs-lookup"><span data-stu-id="23ac5-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="23ac5-140">Jei perjungsite EKA į autonominį režimą, negalėsite tęsti šių sustabdytų operacijų, nes jos jau buvo pašalintos iš autonominės duomenų bazės.</span><span class="sxs-lookup"><span data-stu-id="23ac5-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="23ac5-141">Anuliuoti sustabdytą operaciją</span><span class="sxs-lookup"><span data-stu-id="23ac5-141">Void a suspended transaction</span></span>

<span data-ttu-id="23ac5-142">Galite anuliuoti sustabdytas operacijas atšaukdami operaciją, o paskui atlikdami operaciją **Anuliuoti operaciją**, arba pasirinkdami operaciją sąraše **Atšaukti operaciją** ir programos juostoje pasirinkdami **Anuliuoti**.</span><span class="sxs-lookup"><span data-stu-id="23ac5-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="23ac5-143">Taip pat galima sukonfigūruoti parduotuvę, kad vartotojai būtų raginami anuliuoti sustabdytas operacijas, kai jie baigia savo pamainą.</span><span class="sxs-lookup"><span data-stu-id="23ac5-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>
