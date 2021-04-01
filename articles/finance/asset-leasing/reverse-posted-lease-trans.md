---
title: Užregistruotų nuomos operacijų atšaukimas
description: Šioje temoje paaiškinama, kaip atšaukti užregistruotą nuomos operaciją. Bet kokia operacija, sukurta naudojant turto nuomą, gali būti atšaukta.
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
ms.openlocfilehash: 22d8eee22221efaf5e7a715c8b95dff261bee62f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249730"
---
# <a name="reverse-posted-lease-transactions"></a><span data-ttu-id="00614-104">Užregistruotų nuomos operacijų atšaukimas</span><span class="sxs-lookup"><span data-stu-id="00614-104">Reverse posted lease transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00614-105">Bet kokia operacija, sukurta naudojant turto nuomą, gali būti atšaukta.</span><span class="sxs-lookup"><span data-stu-id="00614-105">Any transaction that is created through Asset leasing can be reversed.</span></span> <span data-ttu-id="00614-106">Operacijos, kurios atšaukiamos naudojant turto nuomos informaciją.</span><span class="sxs-lookup"><span data-stu-id="00614-106">Transactions that are reversed through Asset leasing update your lease data.</span></span> <span data-ttu-id="00614-107">Todėl jie taip pat atnaujina nuomos įsipareigojimo ir naudojimo teise valdomo turto balansinę vertę.</span><span class="sxs-lookup"><span data-stu-id="00614-107">Therefore, they also update the carrying values of the lease liability and right-of-use (ROU) asset.</span></span>

<span data-ttu-id="00614-108">Norėdami sukurti nuomos operaciją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="00614-108">To create a reversing transaction for a lease, follow these steps.</span></span>

1. <span data-ttu-id="00614-109">Puslapyje **Turto operacijos** arba **Įsipareigojimų operacijos** pasirinkite operaciją ir pasirinkite **Atšaukti operaciją**.</span><span class="sxs-lookup"><span data-stu-id="00614-109">On either the **Asset transactions** page or the **Liability transactions** page, select the transaction, and then select **Reverse transaction**.</span></span>
2. <span data-ttu-id="00614-110">Pasirodžiusiame dialogo lange galite redaguoti atšaukiamos įrašo registravimo datą.</span><span class="sxs-lookup"><span data-stu-id="00614-110">In the dialog box that appears, you can edit the date when the reversing entry will be posted.</span></span> <span data-ttu-id="00614-111">Pagal numatytuosius parametrus kopijas **Data** nustatomas į operacijos, kurią pasirinkote, operacijos registravimo datą.</span><span class="sxs-lookup"><span data-stu-id="00614-111">By default, the **Date** field is set to the transaction posting date of the transaction that you selected.</span></span> <span data-ttu-id="00614-112">Atšaukiamos įrašo negalima registruoti anksčiau nei pradinė pasirinkto operacijos registravimo data.</span><span class="sxs-lookup"><span data-stu-id="00614-112">The reversing entry can't be posted earlier than the original posting date of the selected transaction.</span></span>
3. <span data-ttu-id="00614-113">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="00614-113">Select **OK**.</span></span> <span data-ttu-id="00614-114">Užregistruojamas žurnalo įrašas, kuris anuliuoja jūsų pasirinkto įrašo įrašą.</span><span class="sxs-lookup"><span data-stu-id="00614-114">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="00614-115">Atšaukimas rodomas puslapyje **Turto operacijos** ar **Įsipareigojimų operacijos**, o grynoji dabartinio balanso suma, rodoma puslapyje, atnaujinama.</span><span class="sxs-lookup"><span data-stu-id="00614-115">The reversal is shown on the **Asset transactions** or **Liability transactions** page, and the net total of the current balance that is shown on the page is updated.</span></span>

<span data-ttu-id="00614-116">Pasirinkus **Atšaukti sekimą**, pasirodo langas, rodantis pradines operacijas ir atšauktas operacijas, kartu su susijusiu numeriu, kuris žinomas kaip *sekimo numeris*.</span><span class="sxs-lookup"><span data-stu-id="00614-116">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked number that is known as a *trace number*.</span></span> <span data-ttu-id="00614-117">Norėdami, kad pakeitimai būtų suprantamesni, taip pat galite sekti mažinimo naudodami nuomos grafikus.</span><span class="sxs-lookup"><span data-stu-id="00614-117">To make the reversals easier to understand and to improve visibility, you can also track reversals by using the lease schedules.</span></span>

<span data-ttu-id="00614-118">Laukas **Naujausias žurnalo numeris** puslapyje **Grafikas** rodo operacijų žurnalų numerius.</span><span class="sxs-lookup"><span data-stu-id="00614-118">The **Latest journal number** field on the **Schedule** page shows the journal numbers of transactions.</span></span> <span data-ttu-id="00614-119">Kai operacija atšaukiama, šis laukas atnaujinamas, naudojant atšaukiamos operacijos žurnalo numerį.</span><span class="sxs-lookup"><span data-stu-id="00614-119">When a transaction is reversed, this field is updated with the journal number of a reversing transaction.</span></span> <span data-ttu-id="00614-120">Be to, žymės langelis **Atšaukta** pasirenkamas, kad būtų galima nurodyti, jog operacija atšaukiama, o pasirenkamas laukas **Užregistruota**.</span><span class="sxs-lookup"><span data-stu-id="00614-120">Additionally, the **Reversed** check box is selected to indicate that the transaction is reversed, and the **Posted** field is selected.</span></span>

## <a name="revoke-a-reversed-transaction"></a><span data-ttu-id="00614-121">Atšauktos operacijos anuliavimas</span><span class="sxs-lookup"><span data-stu-id="00614-121">Revoke a reversed transaction</span></span>

<span data-ttu-id="00614-122">Norėdami atšaukti atšauktą operaciją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="00614-122">To revoke a reversed transaction, follow these steps.</span></span>

1. <span data-ttu-id="00614-123">Puslapyje **Grafikas** arba puslapyje **Operacijos** pasirinkite pradinę operaciją.</span><span class="sxs-lookup"><span data-stu-id="00614-123">On either the **Schedule** page or the **Transactions** page, select the original transaction.</span></span>
2. <span data-ttu-id="00614-124">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="00614-124">Follow one of these steps:</span></span>

    - <span data-ttu-id="00614-125">Jei pasirinkote operaciją puslapyje **Grafikas**, atlikite žurnalo kūrimo veiksmus iš temos [Paketinis mėnesio žurnalo įrašų kūrimas](create-monthly-journals-batch.md).</span><span class="sxs-lookup"><span data-stu-id="00614-125">If you selected the transaction on the **Schedule** page, follow the steps for creating a journal in [Create monthly journal entries in a batch](create-monthly-journals-batch.md).</span></span> <span data-ttu-id="00614-126">Žurnalą turite registruoti neautomatiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="00614-126">You must manually post the journal.</span></span>
    - <span data-ttu-id="00614-127">Jei puslapyje **Operacijos** pasirinkote operaciją, pasirinkite **atšaukti operaciją**.</span><span class="sxs-lookup"><span data-stu-id="00614-127">If you selected the transaction on the **Transactions** page, select **Reverse transaction**.</span></span> <span data-ttu-id="00614-128">Gausite pranešimą, kuriame nurodoma, kad šis atšaukimas yra ankstesnio atšaukimo atšaukimas ir kad galite redaguoti šio atšaukimo registravimo datą.</span><span class="sxs-lookup"><span data-stu-id="00614-128">You receive a message that states that this revocation is a revocation of an earlier reversal, and that you can edit the posting date for this revocation.</span></span> <span data-ttu-id="00614-129">Tačiau bendri verslo tikrinimai turi įtakos datoms, kurias galima įvesti į lauką **Data**.</span><span class="sxs-lookup"><span data-stu-id="00614-129">However, general business validations affect the dates that can be entered in the **Date** field.</span></span> 

3. <span data-ttu-id="00614-130">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="00614-130">Select **OK**.</span></span> <span data-ttu-id="00614-131">Užregistruojamas žurnalo įrašas, kuris anuliuoja jūsų pasirinkto įrašo įrašą.</span><span class="sxs-lookup"><span data-stu-id="00614-131">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="00614-132">Atšaukimas rodomas puslapyje **Operacijos**, o grynasis visas dabartinis balansas atkuriamas iki pirmo atšaukimo.</span><span class="sxs-lookup"><span data-stu-id="00614-132">The reversal is shown on the **Transactions** page, and the net total current balance is restored to what it was before the first reversal.</span></span> <span data-ttu-id="00614-133">Todėl poveikis, kurį atšaukė balansai, neigiamas.</span><span class="sxs-lookup"><span data-stu-id="00614-133">Therefore, the impact that the reversal had on the balances is negated.</span></span>

<span data-ttu-id="00614-134">Pasirinkus **Atšaukti sekimą**, pasirodo langas, rodantis pradines operacijas ir atšauktas operacijas, kartu su sekimo numeriu.</span><span class="sxs-lookup"><span data-stu-id="00614-134">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked trace number.</span></span>

<span data-ttu-id="00614-135">Taip pat galite sekti atšaukimus naudodami atitinkamus puslapį **Grafikai**.</span><span class="sxs-lookup"><span data-stu-id="00614-135">You can also track revocations by using the appropriate **Schedules** page.</span></span> <span data-ttu-id="00614-136">Laukas **Atšaukti** panaikintas, o laukas **Žurnalas užregistruotas** yra pasirinktas.</span><span class="sxs-lookup"><span data-stu-id="00614-136">The **Reverse** field is cleared, whereas the **Journal posted** field is selected.</span></span> <span data-ttu-id="00614-137">Be to, laukas **Naujausias žurnalo numeris** atnaujinamas naudojant atšaukimo operacijos žurnalo numerį, o laukas **Žurnalo numeris** atnaujinamas, atšaukiant žurnalo numerį.</span><span class="sxs-lookup"><span data-stu-id="00614-137">Additionally, the **Latest journal number** field is updated with the journal number of the revocation transaction, and the **Journal number** field is updated with the reversal journal number.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]