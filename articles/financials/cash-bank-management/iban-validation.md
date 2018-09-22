---
title: "Tarptautinio banko sąskaitos numerio (IBAN) sąskaitos tikrinimo valdymas"
description: "Šioje temoje paaiškinama, kaip valdyti tarptautinio banko sąskaitos numerio (IBAN) sąskaitos tikrinimą."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: lt-lt
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="de69d-103">Tarptautinio banko sąskaitos numerio (IBAN) sąskaitos tikrinimo valdymas</span><span class="sxs-lookup"><span data-stu-id="de69d-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de69d-104">Taikant tarptautinio banko sąskaitos numerio (IBAN) sąskaitos tikrinimą padaugėja tikrinimų, kurie yra atliekami, kai įtraukiate IBAN į banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="de69d-104">International Bank Account Number (IBAN) account validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="de69d-105">IBAN struktūra saugoma „Dynamics 365 for Finance and Operations“ ir įkeliama automatiškai, kai pirmą kartą naudojate IBAN banko sąskaitose.</span><span class="sxs-lookup"><span data-stu-id="de69d-105">The structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operation, and is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="de69d-106">Banko sąskaitos numeris yra nurodytos IBAN numerio struktūros dalis.</span><span class="sxs-lookup"><span data-stu-id="de69d-106">The bank account number is part of the structure defined for an IBAN number.</span></span> <span data-ttu-id="de69d-107">Priklausomai nuo tos struktūros, jei IBAN sąskaitos numerio vieta ir ilgis neatitinka vietos, nurodytos kiekvienos šalies ar regiono struktūroje, matysite perspėjimo pranešimus.</span><span class="sxs-lookup"><span data-stu-id="de69d-107">Based on that structure, if the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you will receive warning messages.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="de69d-108">IBAN struktūrų nustatymas</span><span class="sxs-lookup"><span data-stu-id="de69d-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="de69d-109">Pasirinkite **Grynųjų pinigų ir banko valdymas \> Nustatymas \> IBAN struktūros**.</span><span class="sxs-lookup"><span data-stu-id="de69d-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="de69d-110">Atkreipkite dėmesį, kad kiekvienos šalies ar regiono IBAN struktūros nustatomos automatiškai.</span><span class="sxs-lookup"><span data-stu-id="de69d-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="de69d-111">Jei reikia tinkinti konkrečios šalies ar regiono struktūras, galite jas redaguoti.</span><span class="sxs-lookup"><span data-stu-id="de69d-111">If you must customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="de69d-112">Struktūrų aprašai bus kiekvieno naujo leidimo dalis.</span><span class="sxs-lookup"><span data-stu-id="de69d-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="de69d-113">Galite naudoti meniu **Struktūrų nustatymas iš naujo**, kad po kiekvieno atnaujinimo įkeltumėte naujausius aprašus.</span><span class="sxs-lookup"><span data-stu-id="de69d-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="de69d-114">Banko sąskaitos IBAN struktūros tikrinimas</span><span class="sxs-lookup"><span data-stu-id="de69d-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="de69d-115">Pasirinkite **Grynųjų pinigų ir banko valdymas \> Banko sąskaitos \> Banko sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="de69d-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="de69d-116">Sukurkite banko sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="de69d-116">Create a bank account.</span></span>
3. <span data-ttu-id="de69d-117">„FastTab“ skirtuke **Papildoma informacija** įveskite IBAN.</span><span class="sxs-lookup"><span data-stu-id="de69d-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="de69d-118">Jei IBAN sąskaitos numerio vieta ir ilgis neatitinka vietos, nurodytos kiekvienos šalies ar regiono struktūroje, matysite pranešimą.</span><span class="sxs-lookup"><span data-stu-id="de69d-118">If the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you receive a message.</span></span> <span data-ttu-id="de69d-119">Negalima tęsti, jei IBAN ilgis neatitinka IBAN struktūros ilgio.</span><span class="sxs-lookup"><span data-stu-id="de69d-119">You can't continue if the length of the IBAN doesn't match the length in the IBAN structure.</span></span>

    <span data-ttu-id="de69d-120">Tikrinimo metu taip pat patikrinama, ar banko sąskaitos numeris sutampa su IBAN dalimi, kuri nurodo banko sąskaitos numerį.</span><span class="sxs-lookup"><span data-stu-id="de69d-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="de69d-121">Jei banko sąskaitos numeris nesutampa, matysite perspėjimo pranešimą.</span><span class="sxs-lookup"><span data-stu-id="de69d-121">If the bank account number doesn't match, you receive a warning message.</span></span> <span data-ttu-id="de69d-122">Šis pranešimas yra tik perspėjimas.</span><span class="sxs-lookup"><span data-stu-id="de69d-122">This message is only a warning.</span></span> <span data-ttu-id="de69d-123">Galite tęsti net jei banko sąskaitos numeris nesutampa.</span><span class="sxs-lookup"><span data-stu-id="de69d-123">You can continue even if the bank account number doesn't match.</span></span>

