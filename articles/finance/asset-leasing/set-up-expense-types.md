---
title: Išlaidų tipų nustatymas
description: Šioje temoje paaiškinta, kaip nustatyti išlaidų tipus turto nuomoje.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b50f406c7411ff8ed990a312fde9c2fc0ba3c3db
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819703"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="1e9b9-103">Išlaidų tipų nustatymas</span><span class="sxs-lookup"><span data-stu-id="1e9b9-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e9b9-104">Šioje temoje paaiškinta, kaip nustatyti išlaidų tipus turto nuomoje.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="1e9b9-105">Išlaidos, kurios neatstovaujamos pagal mokėjimus, yra žinomos kaip *išlaidų sąnaudos*.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="1e9b9-106">Šios išlaidos apima turto mokesčius, bendrąsias zonos priežiūros išlaidas ir draudimo išlaidas.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="1e9b9-107">Įtraukti administravimo išlaidų tipą</span><span class="sxs-lookup"><span data-stu-id="1e9b9-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="1e9b9-108">Eikite į **Turto nuoma \> Sąranka \> Išlaidų tipai**.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="1e9b9-109">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-109">Select **New**.</span></span>
3. <span data-ttu-id="1e9b9-110">Atitinkamuose laukuose įveskite naują išlaidų tipą ir aprašymą.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="1e9b9-111">Sąskaitų priskyrimas administracinėms išlaidoms</span><span class="sxs-lookup"><span data-stu-id="1e9b9-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="1e9b9-112">Tada turėtumėte susieti abonementą su išlaidų tipais.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="1e9b9-113">Šios sąskaitos bus debetuojamos, užregistravus išlaidų grafiko įrašus.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="1e9b9-114">Korespondentinė sąskaita nurodyta kiekvienos nuomos **Eksploatavimo išlaidų mokėjimo grafiko** eilutėse.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="1e9b9-115">Eikite į **Turto nuoma \> Sąranka \> Turto nuomos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="1e9b9-116">Skirtuko **Sąskaitos** „FastTab“ **Eksploatavimo išlaidos** lauke **Išlaidų tipas** pasirinkite išlaidų tipą.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="1e9b9-117">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-117">Select **Add**.</span></span>
4. <span data-ttu-id="1e9b9-118">Lauke **Knygos tipas** pasirinkite knygos tipą, kurį norite susieti su administravimo išlaidomis.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1e9b9-119">Keli knygos tipai gali būti siejami su ta pačia išlaidų sąskaita.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="1e9b9-120">Lauke **Sąskaitos kodas** nurodykite, kuri nuomos knyga turi būti taikoma.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="1e9b9-121">**Visos** – knyga taikoma visoms nuomoms.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="1e9b9-122">**Grupė** – knyga taikoma konkrečiai nuomų grupei.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="1e9b9-123">**Lentelė** – knyga taikoma konkrečioms nuomoms.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="1e9b9-124">Jei parinktis **Grupė** arba **Lentelė** pasirinkote lauke **Sąskaitos kodas**, lauke **Sąskaitos / grupės numeris** pasirinkite sąskaitos numerį arba grupės numerį.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="1e9b9-125">Atitinkamuose laukuose pasirinkite finansinės nuomos pagrindinės sąskaita ir pagrindinės veiklos nuomos abonementą.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="1e9b9-126">Atlikę šiuos veiksmus, galite pridėti išlaidų per **Eksploatavimo išlaidų mokėjimo grafiko** eilutes pasirinktos nuomos puslapyje **Nuomos informacija**.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="1e9b9-127">Taip pat galite pridėti išlaidų kurdami naujas nuomos sutartis.</span><span class="sxs-lookup"><span data-stu-id="1e9b9-127">Alternatively, you can add expenses when you create a new lease.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]