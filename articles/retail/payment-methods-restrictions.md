---
title: Grąžinimo mokėjimo metodų be kvito apribojimas
description: Šioje temoje aprašoma, kaip tam tikrus grąžinimo mokėjimo tipus galima apriboti, jei grąžinimai vykdomi be kvito.
author: rapraj
manager: AnnBe
ms.date: 013/05/2019
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
ms.openlocfilehash: 6e2c32aae06ce7bbdde30809d7a197f43b856af1
ms.sourcegitcommit: bacec397ee48ac583596be156c87ead474ee07df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/05/2019
ms.locfileid: "777182"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="ab100-103">Grąžinimo mokėjimo metodų be kvito apribojimas</span><span class="sxs-lookup"><span data-stu-id="ab100-103">Restrict payment methods for returns without a receipt</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ab100-104">Nustačius sistemą, reikia sukonfigūruoti kiekvieną pardavėjo priimamą mokėjimo tipą.</span><span class="sxs-lookup"><span data-stu-id="ab100-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="ab100-105">Šioje temoje aprašoma, kaip tam tikrus grąžinimo mokėjimo tipus galima apriboti, jei grąžinimai vykdomi be kvito.</span><span class="sxs-lookup"><span data-stu-id="ab100-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="ab100-106">Nustatyti mokėjimo būdus</span><span class="sxs-lookup"><span data-stu-id="ab100-106">Set up payment methods</span></span>

<span data-ttu-id="ab100-107">Norėdami nustatyti mokėjimo būdus, turite atlikti toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ab100-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="ab100-108">Sukurkite mokėjimo būdus, priimamus visos organizacijos.</span><span class="sxs-lookup"><span data-stu-id="ab100-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="ab100-109">Sukurkite visai organizacijai taikomų kortelių tipus ir kortelių numerius.</span><span class="sxs-lookup"><span data-stu-id="ab100-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="ab100-110">Jei priimamos kredito ar debeto kortelės, turite sukurti vieną mokėjimo būdą, naudojamą atsiskaitant kortelėmis, o po to sukurti visai organizacijai taikomus kortelių tipus ir kortelių numerius.</span><span class="sxs-lookup"><span data-stu-id="ab100-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="ab100-111">Nustatykite parduotuvės mokėjimo būdus.</span><span class="sxs-lookup"><span data-stu-id="ab100-111">Set up store payment methods.</span></span> <span data-ttu-id="ab100-112">Susiekite mokėjimo būdus su kiekviena parduotuve, o po to įveskite kiekvienos parduotuvės mokėjimo būdo parametrus.</span><span class="sxs-lookup"><span data-stu-id="ab100-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="ab100-113">Nustatykite parduotuvių mokėjimo kortelėmis būdus.</span><span class="sxs-lookup"><span data-stu-id="ab100-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="ab100-114">Nustatykite kiekvieno parduotuvės priimamo mokėjimo kortele būdo kortelę.</span><span class="sxs-lookup"><span data-stu-id="ab100-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="ab100-115">![Parduotuvės sąranka](media/NoReceiptReturns1.png "Parduotuvės sąranka")</span><span class="sxs-lookup"><span data-stu-id="ab100-115">![Retail Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="ab100-116">Grąžinimo mokėjimo metodų be kvito apribojimas</span><span class="sxs-lookup"><span data-stu-id="ab100-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="ab100-117">Puslapyje **Parduotuvės valdymas**, prie parinkties **Grąžinimai be kvito** pasirinkite kiekvieno parduotuvės mokėjimo būdo parametro **Riboti grąžinimus be kvito** į parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="ab100-117">For each store payment method, on the **Retail store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="ab100-118">Numatytoji jungiklio reikšmė yra **Ne**, kuri užtikrina, kad mokėjimo būdą galima naudoti grąžinant.</span><span class="sxs-lookup"><span data-stu-id="ab100-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="ab100-119">Kai parametras **Riboti grąžinimus be kvito** nustatytas į parinktį **Taip**, pasirinktas mokėjimo būdas nebus leidžiamas naudoti grąžinant.</span><span class="sxs-lookup"><span data-stu-id="ab100-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="ab100-120">![Parduotuvės mokėjimo būdas](media/NoReceiptReturns3.png "Parduotuvės mokėjimo būdas")</span><span class="sxs-lookup"><span data-stu-id="ab100-120">![Retail Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="ab100-121">Kai kasininkas pasirenka mokėjimo būdą, kuris yra apribotas naudoti grąžinant be kvito, rodomas pranešimas, kuriame reikia patvirtinti priimtinus mokėjimo būdus.</span><span class="sxs-lookup"><span data-stu-id="ab100-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="ab100-122">![Priimtini mokėjimo būdai](media/NoReceiptReturns4.png "Priimtini mokėjimo būdai")</span><span class="sxs-lookup"><span data-stu-id="ab100-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="ab100-123">Jei operacijai priskiriami grąžinimai su kvitu ir be kvito, apribojimo sąlygos nebus taikomos, nes operacija bus grąžinimo darbo eiga su kvitu.</span><span class="sxs-lookup"><span data-stu-id="ab100-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 

