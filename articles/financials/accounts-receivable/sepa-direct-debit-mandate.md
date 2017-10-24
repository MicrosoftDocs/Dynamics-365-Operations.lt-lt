---
title: "SEPA tiesioginio debeto įgaliojimo nustatymas"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59491
ms.assetid: 653a135f-c515-4ae3-9da2-82b5e1f103b5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8b50c2d585c7e0bcd8dc15aa70446cd7346ad33c
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-sepa-direct-debit-mandate"></a><span data-ttu-id="a0eea-102">SEPA tiesioginio debeto įgaliojimo nustatymas</span><span class="sxs-lookup"><span data-stu-id="a0eea-102">Set up SEPA direct debit mandate</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="a0eea-103">Bendros mokėjimų eurais erdvės (SEPA) tiesioginis debetas leidžia kreditoriui surinkti lėšas iš kliento banko sąskaitos, jei klientas kreditoriui suteikė pasirašytą įgaliojimą.</span><span class="sxs-lookup"><span data-stu-id="a0eea-103">A Single Euro Payment Area (SEPA) direct debit lets a creditor collect funds from a customer's bank account, provided that the customer has granted a signed mandate to the creditor.</span></span> <span data-ttu-id="a0eea-104">Įgaliojimas, kurį pasirašo klientas, įgalioja kreditorių surinkti mokėjimą ir nurodo kliento bankui jį išmokėti.</span><span class="sxs-lookup"><span data-stu-id="a0eea-104">The mandate that the customer signs authorizes the creditor to collect a payment and instructs the customer's bank to pay the collection.</span></span> <span data-ttu-id="a0eea-105">Ši tema išdėstyta taip, kad parodytų SEPA tiesioginio debeto įgaliojimų nustatymo procesą.</span><span class="sxs-lookup"><span data-stu-id="a0eea-105">This topic is organized to show the process for setting up SEPA direct debit mandates.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a0eea-106">Būtinieji komponentai</span><span class="sxs-lookup"><span data-stu-id="a0eea-106">Prerequisites</span></span>
<span data-ttu-id="a0eea-107">Pateiktoje lentelėje parodytos būtinosios sąlygos, kurias reikia įvykdyti prieš pradedant.</span><span class="sxs-lookup"><span data-stu-id="a0eea-107">The following table shows the prerequisites that must be in place before you start.</span></span>

| <span data-ttu-id="a0eea-108">Kategorija</span><span class="sxs-lookup"><span data-stu-id="a0eea-108">Category</span></span>       | <span data-ttu-id="a0eea-109">Būtinoji sąlyga</span><span class="sxs-lookup"><span data-stu-id="a0eea-109">Prerequisite</span></span>                                                                                                                                              |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0eea-110">Šalis/regionas</span><span class="sxs-lookup"><span data-stu-id="a0eea-110">Country/region</span></span> | <span data-ttu-id="a0eea-111">Pagrindinis juridinio subjekto adresas turi būti šioje šalyje / regione: Austrija, Belgija, Nyderlandai, Ispanija, Italija, Prancūzija arba Vokietija.</span><span class="sxs-lookup"><span data-stu-id="a0eea-111">The primary address for the legal entity must be in the following countries/regions: Austria, Belgium, Germany, Spain, France, Italy, or the Netherlands.</span></span> |

1. <span data-ttu-id="a0eea-112">Nustatykite tiesioginio debeto įgaliojimų numeraciją. Kiekvienas tiesioginio debeto įgaliojimas turi turėti unikalų numerį.</span><span class="sxs-lookup"><span data-stu-id="a0eea-112">Set up a number sequence for direct debit mandates Each direct debit mandate must have a unique number.</span></span> <span data-ttu-id="a0eea-113">Naudodami puslapį **Numeracijos** sukurkite tiesioginio debeto įgaliojimų numeraciją.</span><span class="sxs-lookup"><span data-stu-id="a0eea-113">Use the **Number sequences** page to create a number sequence for direct debit mandates.</span></span> <span data-ttu-id="a0eea-114">Naudosite šį identifikatorių, kad priskirtumėte numeraciją tiesioginio debeto įgaliojimų sistemai puslapyje **Gautinų sumų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="a0eea-114">You will use this identifier to assign the number sequence to the direct debit mandate system on the **Accounts receivable parameters** page.</span></span>

2. <span data-ttu-id="a0eea-115">Nustatykite tiesioginio debeto įgaliojimų Gautinų sumų parametrus. Puslapį **Gautinų sumų parametrai** naudokite tiesioginio debeto įgaliojimų parametrams nustatyti.</span><span class="sxs-lookup"><span data-stu-id="a0eea-115">Set up Accounts receivable parameters for direct debit mandates Use the **Accounts receivable parameters** page to set up parameters for direct debit mandates.</span></span> <span data-ttu-id="a0eea-116">Norėdami nustatyti parametrus, skirtuke **Tiesioginis debetas** pagal poreikį pakeiskite numatytuosius parametrus.</span><span class="sxs-lookup"><span data-stu-id="a0eea-116">To set up the parameters, on the **Direct debit** tab, change the default parameters as you require.</span></span> <span data-ttu-id="a0eea-117">Tada skirtuke **Numeracijos** atnaujinkite lauką **Tiesioginio debeto įgaliojimo ID** pagal anksčiau nustatytą numeraciją.</span><span class="sxs-lookup"><span data-stu-id="a0eea-117">Then, on the **Number sequences** tab, update the **Direct debit mandate ID** field with the number sequence that you set up earlier.</span></span>

3. <span data-ttu-id="a0eea-118">Nustatykite tiesioginio debeto įgaliojimų mokėjimo būdą. Turite nustatyti tiesioginio debeto įgaliojimų mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="a0eea-118">Set up a method of payment for direct debit mandates You must set up a method of payment for direct debit mandates.</span></span> <span data-ttu-id="a0eea-119">Naudojate šį mokėjimo būdą pateikdami SF užklausas, kad būtų generuojami tiesioginio debeto mokėjimai.</span><span class="sxs-lookup"><span data-stu-id="a0eea-119">You use this method of payment to query for invoices to generate direct debit payments for.</span></span> <span data-ttu-id="a0eea-120">Naudokite **Mokėjimo būdų** puslapį, kad nustatytumėte mokėjimo būdą.</span><span class="sxs-lookup"><span data-stu-id="a0eea-120">Use the **Methods of payment** page to set up the method of payment.</span></span> <span data-ttu-id="a0eea-121">Norėdami nustatyti tiesioginio debeto įgaliojimų mokėjimo būdą, turite atlikti toliau nurodytus papildomus mokėjimo būdo veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a0eea-121">To set up a method of payment for direct debit mandates, you must follow these additional steps for a method of payment:</span></span>

-   <span data-ttu-id="a0eea-122">Lauke **Mokėjimo tipas** pasirinkite **Elektroninis mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="a0eea-122">In the **Payment type** field, select **Electronic payment**.</span></span>
-   <span data-ttu-id="a0eea-123">Pasirinktinai: jei tikitės, kad kiekvienas jūsų klientas turės kelis įgaliojimus, lauke **Laikotarpis** pasirinkite **Sąskaita faktūra**.</span><span class="sxs-lookup"><span data-stu-id="a0eea-123">Optional: If you expect each of your customers to have multiple mandates, in the **Period** field, select **Invoice**.</span></span> <span data-ttu-id="a0eea-124">Kiekvienai sąskaitai faktūrai bus sukurtas atskiras mokėjimas ir kiekvienas mokėjimas naudos tai sąskaitai faktūrai nurodytą įgaliojimą.</span><span class="sxs-lookup"><span data-stu-id="a0eea-124">A separate payment will be created for each invoice, and each payment will use the mandate that is specified for the invoice.</span></span>
-   <span data-ttu-id="a0eea-125">Pasirinkite parinktį **Reikalauti įgaliojimo**, kad sukurtumėte mokėjimus naudojant tiesioginio debeto įgaliojimus.</span><span class="sxs-lookup"><span data-stu-id="a0eea-125">Select the **Require mandate** option to create payments by using direct debit mandates.</span></span> <span data-ttu-id="a0eea-126">Parinktis **Reikalauti įgaliojimo** prieinama tik tada, jei **Mokėjimo tipo** lauke pasirenkate **Elektroninis mokėjimas**.</span><span class="sxs-lookup"><span data-stu-id="a0eea-126">The **Require mandate** option is available only if you select **Electronic payment** in the **Payment type** field.</span></span>

<span data-ttu-id="a0eea-127">Taip pat žr.</span><span class="sxs-lookup"><span data-stu-id="a0eea-127">See Also</span></span>

[<span data-ttu-id="a0eea-128">Tiesioginio debeto apžvalga</span><span class="sxs-lookup"><span data-stu-id="a0eea-128">Direct debit overview</span></span>](sepa-direct-debit-overview.md) 

[<span data-ttu-id="a0eea-129">Kurti kliento tiesioginio debeto įgaliojimą</span><span class="sxs-lookup"><span data-stu-id="a0eea-129">Create a direct debit mandate for a customer</span></span>](tasks/create-direct-debit-mandate-customer.md) 


