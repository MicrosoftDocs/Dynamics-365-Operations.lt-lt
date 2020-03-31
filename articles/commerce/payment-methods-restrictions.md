---
title: Grąžinimo mokėjimo metodų be kvito apribojimas
description: Šioje temoje aprašoma, kaip tam tikrus grąžinimo mokėjimo tipus galima apriboti, jei grąžinimai vykdomi be kvito.
author: rapraj
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: dfc49e3c3132fe2687ea71e5da75fe31753d57f9
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023475"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="bca4e-103">Grąžinimo mokėjimo metodų be kvito apribojimas</span><span class="sxs-lookup"><span data-stu-id="bca4e-103">Restrict payment methods for returns without a receipt</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="bca4e-104">Nustačius sistemą, reikia sukonfigūruoti kiekvieną pardavėjo priimamą mokėjimo tipą.</span><span class="sxs-lookup"><span data-stu-id="bca4e-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="bca4e-105">Šioje temoje aprašoma, kaip tam tikrus grąžinimo mokėjimo tipus galima apriboti, jei grąžinimai vykdomi be kvito.</span><span class="sxs-lookup"><span data-stu-id="bca4e-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="bca4e-106">Nustatyti mokėjimo būdus</span><span class="sxs-lookup"><span data-stu-id="bca4e-106">Set up payment methods</span></span>

<span data-ttu-id="bca4e-107">Norėdami nustatyti mokėjimo būdus, turite atlikti toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="bca4e-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="bca4e-108">Sukurkite mokėjimo būdus, priimamus visos organizacijos.</span><span class="sxs-lookup"><span data-stu-id="bca4e-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="bca4e-109">Sukurkite visai organizacijai taikomų kortelių tipus ir kortelių numerius.</span><span class="sxs-lookup"><span data-stu-id="bca4e-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="bca4e-110">Jei priimamos kredito ar debeto kortelės, turite sukurti vieną mokėjimo būdą, naudojamą atsiskaitant kortelėmis, o po to sukurti visai organizacijai taikomus kortelių tipus ir kortelių numerius.</span><span class="sxs-lookup"><span data-stu-id="bca4e-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="bca4e-111">Nustatykite parduotuvės mokėjimo būdus.</span><span class="sxs-lookup"><span data-stu-id="bca4e-111">Set up store payment methods.</span></span> <span data-ttu-id="bca4e-112">Susiekite mokėjimo būdus su kiekviena parduotuve, o po to įveskite kiekvienos parduotuvės mokėjimo būdo parametrus.</span><span class="sxs-lookup"><span data-stu-id="bca4e-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="bca4e-113">Nustatykite parduotuvių mokėjimo kortelėmis būdus.</span><span class="sxs-lookup"><span data-stu-id="bca4e-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="bca4e-114">Nustatykite kiekvieno parduotuvės priimamo mokėjimo kortele būdo kortelę.</span><span class="sxs-lookup"><span data-stu-id="bca4e-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="bca4e-115">![Parduotuvės konfigūracija](media/NoReceiptReturns1.png "„Retail“ parduotuvės sąranka")</span><span class="sxs-lookup"><span data-stu-id="bca4e-115">![Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="bca4e-116">Grąžinimo mokėjimo metodų be kvito apribojimas</span><span class="sxs-lookup"><span data-stu-id="bca4e-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="bca4e-117">Už kiekvieną parduotuvės apmokėjimo būdą, puslapyje **Parduotuvės valdymas**, skiltyje **Grąžinimai be kvito**, nustatykite **Grąžinimų be kvito ribojimas** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="bca4e-117">For each store payment method, on the **Store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="bca4e-118">Numatytoji jungiklio reikšmė yra **Ne**, kuri užtikrina, kad mokėjimo būdą galima naudoti grąžinant.</span><span class="sxs-lookup"><span data-stu-id="bca4e-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="bca4e-119">Kai parametras **Riboti grąžinimus be kvito** nustatytas į parinktį **Taip**, pasirinktas mokėjimo būdas nebus leidžiamas naudoti grąžinant.</span><span class="sxs-lookup"><span data-stu-id="bca4e-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="bca4e-120">![Mokėjimo būdas parduotuvėje](media/NoReceiptReturns3.png "„Retail“ parduotuvės mokėjimo būdas")</span><span class="sxs-lookup"><span data-stu-id="bca4e-120">![Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="bca4e-121">Kai kasininkas pasirenka mokėjimo būdą, kuris yra apribotas naudoti grąžinant be kvito, rodomas pranešimas, kuriame reikia patvirtinti priimtinus mokėjimo būdus.</span><span class="sxs-lookup"><span data-stu-id="bca4e-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="bca4e-122">![Galimi mokėjimo būdai](media/NoReceiptReturns4.png "Galimi mokėjimo būdai")</span><span class="sxs-lookup"><span data-stu-id="bca4e-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="bca4e-123">Jei operacijai priskiriami grąžinimai su kvitu ir be kvito, apribojimo sąlygos nebus taikomos, nes operacija bus grąžinimo darbo eiga su kvitu.</span><span class="sxs-lookup"><span data-stu-id="bca4e-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 
