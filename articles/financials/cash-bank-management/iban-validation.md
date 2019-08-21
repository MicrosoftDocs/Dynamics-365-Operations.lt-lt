---
title: Tarptautinio banko sąskaitos numerio (IBAN) sąskaitos tikrinimo valdymas
description: Šioje temoje paaiškinama, kaip valdyti tarptautinio banko sąskaitos numerio (IBAN) sąskaitos tikrinimą.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 70c497ec575ffcaa6f2fdc3fe77bae7b41dc02fb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842430"
---
# <a name="manage-international-bank-account-number-iban-validation"></a><span data-ttu-id="42874-103">Tarptautinio banko sąskaitos numerio (IBAN) tikrinimo valdymas</span><span class="sxs-lookup"><span data-stu-id="42874-103">Manage International Bank Account Number (IBAN) validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42874-104">Taikant tarptautinio banko sąskaitos numerio (IBAN) tikrinimą padaugėja tikrinimų, kurie yra atliekami, kai įtraukiate IBAN į banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="42874-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="42874-105">Informacija apie IBAN struktūrą saugoma „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="42874-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="42874-106">Ši informacija automatiškai įkeliama pirmą kartą naudojantis IBAN banko sąskaitose.</span><span class="sxs-lookup"><span data-stu-id="42874-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="42874-107">Ji apima IBAN ilgį, banko sąskaitos numerio ir įmonės registracijos numerio pradžios taškus, taip pat banko sąskaitos numerio ir įmonės registracijos numerio ilgį.</span><span class="sxs-lookup"><span data-stu-id="42874-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="42874-108">IBAN struktūrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="42874-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="42874-109">Pasirinkite **Grynųjų pinigų ir banko valdymas \> Nustatymas \> IBAN struktūros**.</span><span class="sxs-lookup"><span data-stu-id="42874-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="42874-110">Atkreipkite dėmesį, kad kiekvienos šalies ar regiono IBAN struktūros nustatomos automatiškai.</span><span class="sxs-lookup"><span data-stu-id="42874-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="42874-111">Jei norite tinkinti konkrečios šalies ar regiono struktūras, galite jas redaguoti.</span><span class="sxs-lookup"><span data-stu-id="42874-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="42874-112">Struktūrų aprašai bus kiekvieno naujo leidimo dalis.</span><span class="sxs-lookup"><span data-stu-id="42874-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="42874-113">Galite naudoti meniu **Struktūrų nustatymas iš naujo**, kad po kiekvieno atnaujinimo įkeltumėte naujausius aprašus.</span><span class="sxs-lookup"><span data-stu-id="42874-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="42874-114">Banko sąskaitos IBAN struktūros tikrinimas</span><span class="sxs-lookup"><span data-stu-id="42874-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="42874-115">Pasirinkite **Grynųjų pinigų ir banko valdymas \> Banko sąskaitos \> Banko sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="42874-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="42874-116">Sukurkite banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="42874-116">Create a bank account.</span></span>
3. <span data-ttu-id="42874-117">„FastTab“ skirtuke **Papildoma informacija** įveskite IBAN.</span><span class="sxs-lookup"><span data-stu-id="42874-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="42874-118">Jei IBAN ilgis neatitinka nurodyto kiekvienai šaliai ar regionui būdingo ilgio, gausite įspėjamąjį pranešimą.</span><span class="sxs-lookup"><span data-stu-id="42874-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="42874-119">Negalima tęsti, jei IBAN ilgis neatitinka IBAN struktūroje nurodyto ilgio.</span><span class="sxs-lookup"><span data-stu-id="42874-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="42874-120">Tikrinimo metu taip pat patikrinama, ar banko sąskaitos numeris sutampa su IBAN dalimi, kuri nurodo banko sąskaitos numerį.</span><span class="sxs-lookup"><span data-stu-id="42874-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="42874-121">Jei banko sąskaitos numeris nesutampa, gausite įspėjamąjį pranešimą.</span><span class="sxs-lookup"><span data-stu-id="42874-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="42874-122">Šis pranešimas yra tik perspėjimas.</span><span class="sxs-lookup"><span data-stu-id="42874-122">This message is only a warning.</span></span> <span data-ttu-id="42874-123">Galite tęsti net jei banko sąskaitos numeris nesutampa.</span><span class="sxs-lookup"><span data-stu-id="42874-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="42874-124">Tikrinimo metu taip pat patikrinama, ar banko įmonės registracijos numeris sutampa su ta IBAN dalimi, kurioje nurodomas banko įmonės registracijos numeris.</span><span class="sxs-lookup"><span data-stu-id="42874-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="42874-125">Įmonės registracijos numeris apima banko numerį ir (dažnai) papildomą banko filialą.</span><span class="sxs-lookup"><span data-stu-id="42874-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="42874-126">Jei banko įmonės registracijos numeris nesutampa, gausite įspėjamąjį pranešimą.</span><span class="sxs-lookup"><span data-stu-id="42874-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="42874-127">Šis pranešimas yra tik perspėjimas.</span><span class="sxs-lookup"><span data-stu-id="42874-127">This message is only a warning.</span></span> <span data-ttu-id="42874-128">Galite tęsti net jei banko įmonės registracijos numeris nesutampa.</span><span class="sxs-lookup"><span data-stu-id="42874-128">You can continue even if the bank routing number doesn't match.</span></span>
