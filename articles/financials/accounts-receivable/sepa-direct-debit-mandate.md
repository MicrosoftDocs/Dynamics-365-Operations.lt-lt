---
title: "SEPA tiesioginio debeto įgaliojimo nustatymas"
description: "Bendros mokėjimų eurais erdvės (SEPA) tiesioginis debetas leidžia kreditoriui surinkti lėšas iš kliento banko sąskaitos, jei klientas kreditoriui suteikė pasirašytą įgaliojimą."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 84e4a714b1233a0fb4ebb04757ba12a5d14d6f44
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="f6778-103">SEPA tiesioginio debeto įgaliojimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="f6778-103">Set up SEPA direct debit mandate</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="f6778-104">Bendros mokėjimų eurais erdvės (SEPA) tiesioginis debetas leidžia kreditoriui surinkti lėšas iš kliento banko sąskaitos, jei klientas kreditoriui suteikė pasirašytą įgaliojimą.</span><span class="sxs-lookup"><span data-stu-id="f6778-104">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="f6778-105">Įgaliojimas, kurį pasirašo klientas, įgalioja kreditorių surinkti mokėjimą ir nurodo kliento bankui jį išmokėti.</span><span class="sxs-lookup"><span data-stu-id="f6778-105">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="f6778-106">Ši tema išdėstyta taip, kad parodytų SEPA tiesioginio debeto įgaliojimų nustatymo procesą.</span><span class="sxs-lookup"><span data-stu-id="f6778-106">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f6778-107">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="f6778-107">Prerequisites</span></span>
<span data-ttu-id="f6778-108">Pateiktoje lentelėje parodytos būtinosios sąlygos, kurias reikia įvykdyti prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="f6778-108">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="f6778-109">Kategorija</span><span class="sxs-lookup"><span data-stu-id="f6778-109">Category</span></span>       | <span data-ttu-id="f6778-110">Būtinoji sąlyga</span><span class="sxs-lookup"><span data-stu-id="f6778-110">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6778-111">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="f6778-111">Country/region</span></span> | <span data-ttu-id="f6778-112">Pagrindinis juridinio subjekto adresas turi būti šioje šalyje / regione: Austrija, Belgija, Nyderlandai, Ispanija, Italija, Prancūzija arba Vokietija.</span><span class="sxs-lookup"><span data-stu-id="f6778-112">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="f6778-113">Nustatykite tiesioginio debeto įgaliojimų numeraciją. Kiekvienas tiesioginio debeto įgaliojimas turi turėti unikalų numerį.</span><span class="sxs-lookup"><span data-stu-id="f6778-113">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="f6778-114">Naudodami puslapį **Numeracijos** sukurkite tiesioginio debeto įgaliojimų numeraciją.</span><span class="sxs-lookup"><span data-stu-id="f6778-114">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="f6778-115">Naudosite šį identifikatorių, kad priskirtumėte numeraciją tiesioginio debeto įgaliojimų sistemai puslapyje **Gautinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="f6778-115">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="f6778-116">Nustatykite tiesioginio debeto įgaliojimų Gautinų sumų parametrus. Puslapį **Gautinų sumų parametrai** naudokite tiesioginio debeto įgaliojimų parametrams nustatyti.</span><span class="sxs-lookup"><span data-stu-id="f6778-116">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="f6778-117">Norėdami nustatyti parametrus, skirtuke **Tiesioginis debetas** pagal poreikį pakeiskite numatytuosius parametrus.</span><span class="sxs-lookup"><span data-stu-id="f6778-117">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="f6778-118">Tada skirtuke **Numeracijos** atnaujinkite lauką **Tiesioginio debeto įgaliojimo ID** pagal anksčiau nustatytą numeraciją.</span><span class="sxs-lookup"><span data-stu-id="f6778-118">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="f6778-119">Nustatykite tiesioginio debeto įgaliojimų mokėjimo būdą. Turite nustatyti tiesioginio debeto įgaliojimų mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="f6778-119">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="f6778-120">Naudojate šį mokėjimo būdą pateikdami SF užklausas, kad būtų generuojami tiesioginio debeto mokėjimai.</span><span class="sxs-lookup"><span data-stu-id="f6778-120">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="f6778-121">Naudokite **Mokėjimo būdų** puslapį, kad nustatytumėte mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="f6778-121">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="f6778-122">Norėdami nustatyti tiesioginio debeto įgaliojimų mokėjimo būdą, turite atlikti toliau nurodytus papildomus mokėjimo būdo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f6778-122">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="f6778-123">Lauke **Mokėjimo tipas** pasirinkite **Elektroninis mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="f6778-123">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="f6778-124">Pasirinktinai: jei tikitės, kad kiekvienas jūsų klientas turės kelis įgaliojimus, lauke **Laikotarpis** pasirinkite **Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="f6778-124">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="f6778-125">Kiekvienai sąskaitai faktūrai bus sukurtas atskiras mokėjimas ir kiekvienas mokėjimas naudos tai sąskaitai faktūrai nurodytą įgaliojimą.</span><span class="sxs-lookup"><span data-stu-id="f6778-125">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="f6778-126">Pasirinkite parinktį **Reikalauti įgaliojimo**, kad sukurtumėte mokėjimus naudojant tiesioginio debeto įgaliojimus.</span><span class="sxs-lookup"><span data-stu-id="f6778-126">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="f6778-127">Parinktis **Reikalauti įgaliojimo** prieinama tik tada, jei **Mokėjimo tipo** lauke pasirenkate **Elektroninis mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="f6778-127">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="f6778-128">Taip pat žr.</span><span class="sxs-lookup"><span data-stu-id="f6778-128">See Also</span></span>

[<span data-ttu-id="f6778-129">Tiesioginio debeto apžvalga</span><span class="sxs-lookup"><span data-stu-id="f6778-129">Direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="f6778-130">Kurti kliento tiesioginio debeto įgaliojimą</span><span class="sxs-lookup"><span data-stu-id="f6778-130">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 


