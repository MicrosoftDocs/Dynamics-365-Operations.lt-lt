---
title: "Skambučių centro tęstinumo programos nustatymas"
description: "Šiame straipsnyje aprašyta, kaip nustatyti skambučių centro tęstinumo programą."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 0ae8eb96536538d6cb9ff8030d19a2fa54b9b2c7
ms.contentlocale: lt-lt
ms.lasthandoff: 01/17/2018

---

# <a name="set-up-a-continuity-program-for-a-call-center"></a><span data-ttu-id="890c4-103">Skambučių centro tęstinumo programos nustatymas</span><span class="sxs-lookup"><span data-stu-id="890c4-103">Set up a continuity program for a call center</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="890c4-104">Šiame straipsnyje aprašyta, kaip nustatyti skambučių centro tęstinumo programą.</span><span class="sxs-lookup"><span data-stu-id="890c4-104">This article describes how to set up a continuity program for a call center.</span></span>

<span data-ttu-id="890c4-105">Tęstinės programos, kuri taip pat vadinama pasikartojančio užsakymo programa, klientai reguliariai gauna produkto siuntas pagal iš anksto nustatytą grafiką.</span><span class="sxs-lookup"><span data-stu-id="890c4-105">In a continuity program, which is also known as a recurring order program, customers receive regular product shipments according to a predefined schedule.</span></span> <span data-ttu-id="890c4-106">Kiekvienoje siuntoje gali būtų skirtingas produktas, pvz., knygų klubo mėnesio knyga, arba tas pats produktas gali būti siunčiamas pakartotinai.</span><span class="sxs-lookup"><span data-stu-id="890c4-106">Each shipment can contain a different product, as in the case of a book-of-the-month club, or the same product can be sent repeatedly.</span></span> <span data-ttu-id="890c4-107">Norėdami nustatyti tęstinumo programą, turite atlikti toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="890c4-107">To set up a continuity program, you must complete the following tasks.</span></span>

1.  <span data-ttu-id="890c4-108">Nustatykite tęstinumo parametrus puslapyje **Skambučių centro parametrai**.</span><span class="sxs-lookup"><span data-stu-id="890c4-108">Set the continuity parameters on the **Call center parameters** page.</span></span>
2.  <span data-ttu-id="890c4-109">Sukurkite tęstinumo programą, kurioje būtų nurodyta išsami informacija, pvz., mokėjimo grafikas, siuntimo laikas ir tai, ar apmokama iš anksto.</span><span class="sxs-lookup"><span data-stu-id="890c4-109">Create a continuity program that specifies details such as the payment schedule, the timing of the shipments, and whether billing is up front.</span></span> <span data-ttu-id="890c4-110">Taip pat turite įtraukti produktų, kurie įtraukti į tęstinę programą, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="890c4-110">You must also add a list of products that are included in the continuity program.</span></span> <span data-ttu-id="890c4-111">Kiekvienas produktas gauna įvykio ID numerį, kuris priskiriamas iš eilės pradedant nuo 1.</span><span class="sxs-lookup"><span data-stu-id="890c4-111">Each product receives an event ID number that is assigned sequentially, beginning with 1.</span></span> <span data-ttu-id="890c4-112">Įvykio ID nurodo tvarką, kuria siunčiami produktai.</span><span class="sxs-lookup"><span data-stu-id="890c4-112">The event IDs determine the order that products are sent in.</span></span>
    -   <span data-ttu-id="890c4-113">Jei klientai gauna skirtingą produktą kiekvienoje siuntoje, produktai siunčiami iš eilės pagal jų įvykio ID, pradedant nuo dabartinio įvykio.</span><span class="sxs-lookup"><span data-stu-id="890c4-113">If customers receive a different product in each shipment, the products are sent in sequential order, based on their event IDs and beginning with the current event.</span></span>
    -   <span data-ttu-id="890c4-114">Jei klientai gauna tą patį produktą kiekvienoje siuntoje, sąraše yra tik vienas produktas, kuriam priskirtas vienas įvykio ID.</span><span class="sxs-lookup"><span data-stu-id="890c4-114">If customers receive the same product in each shipment, the list contains only one product that has one event ID.</span></span> <span data-ttu-id="890c4-115">Tas pats įvykis vyksta kelis kartus.</span><span class="sxs-lookup"><span data-stu-id="890c4-115">The same event occurs repeatedly.</span></span> <span data-ttu-id="890c4-116">Galite nurodyti, kiek kartų kartoti kiekvieną įvykį.</span><span class="sxs-lookup"><span data-stu-id="890c4-116">You can specify how many times each event is repeated.</span></span>

3.  <span data-ttu-id="890c4-117">Sukurkite pirminį produktą, kuris nurodo tęstinumo programą, kurią sukūrėte atlikdami 2 užduotį.</span><span class="sxs-lookup"><span data-stu-id="890c4-117">Create a parent product that represents the continuity program that you created in task 2.</span></span> <span data-ttu-id="890c4-118">Jei įtrauksite šį produktą į pardavimo užsakymą, bus atidarytas puslapis **Tęstinumas**.</span><span class="sxs-lookup"><span data-stu-id="890c4-118">If you add this product to a sales order, the **Continuity** page opens.</span></span> <span data-ttu-id="890c4-119">Tada galėsite naudoti tą puslapį, kad sukurtumėte faktinį tęstinumo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="890c4-119">You can then use that page to create the actual continuity order.</span></span> <span data-ttu-id="890c4-120">Pirminis produktas nenurodo atskirų produktų, kuriuos klientas gauna kiekvienoje siuntoje.</span><span class="sxs-lookup"><span data-stu-id="890c4-120">The parent product doesn't specify the individual products that the customer receives in each shipment.</span></span>

<span data-ttu-id="890c4-121">Nustatę tęstinumo programą, kaip aprašyta aukščiau, klientui galite sukurti tęstinumo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="890c4-121">After you've set up a continuity program as described above, you can create a continuity order for a customer.</span></span> <span data-ttu-id="890c4-122">Be to, gali tekti atlikti toliau nurodytas papildomas priežiūros užduotis.</span><span class="sxs-lookup"><span data-stu-id="890c4-122">You might also have to perform the following additional maintenance tasks.</span></span>

-   <span data-ttu-id="890c4-123">**Atnaujinti dabartinio tęstinumo įvykio laikotarpį** – nustatykite paketinę užduotį, sistemai nurodančią dabartinio įvykio laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="890c4-123">**Update the current continuity event period** – Set up a batch job that tells the system what the current event period is.</span></span>
-   <span data-ttu-id="890c4-124">**Sukurti antrinius tęstinumo užsakymus** – iš pirminio tęstinumo užsakymo sukurkite antrinius užsakymus.</span><span class="sxs-lookup"><span data-stu-id="890c4-124">**Create continuity child orders** – Create child orders from the parent continuity order.</span></span>
-   <span data-ttu-id="890c4-125">**Apdoroti tęstinumo mokėjimus** – apdorokite su tęstinumo pardavimo užsakymais susietų mokėjimų sąskaitas ir pranešimus.</span><span class="sxs-lookup"><span data-stu-id="890c4-125">**Process continuity payments** – Process billing and notifications for payments that are associated with continuity sales orders.</span></span>
-   <span data-ttu-id="890c4-126">**Išplėsti tęstinumo eilutes** (jei reikia) – padidinkite tęstinumo įvykio kartojimo kartų skaičių.</span><span class="sxs-lookup"><span data-stu-id="890c4-126">**Extend continuity lines** (if required) – Extend the number of times that a continuity event can be repeated.</span></span> <span data-ttu-id="890c4-127">Tada siuntų kartojimą galima išplėsti už skambučių centro parametrų lauke **Tęstinumo kartojimo slenkstis** nustatytos ribos.</span><span class="sxs-lookup"><span data-stu-id="890c4-127">The repetition of shipments can then extend beyond the limit that was set in the **Continuity repeat threshold** field in the call center parameters.</span></span>
-   <span data-ttu-id="890c4-128">**Atlikti tęstinumo atnaujinimą** (jei reikia) – sinchronizuokite tęstinumo programos ir pirminių tęstinumo pardavimo užsakymų pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="890c4-128">**Perform a continuity update** (if required) – Synchronize changes between the continuity program and the continuity parent sales orders.</span></span>
-   <span data-ttu-id="890c4-129">**Uždaryti pirmines tęstinumo eilutes ir užsakymus** – uždarykite tęstinumo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="890c4-129">**Close continuity parent lines and orders** – Close continuity orders.</span></span>





