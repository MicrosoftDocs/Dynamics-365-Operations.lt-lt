---
title: "Sumų rodymo ataskaitose ir dokumentuose būdo naujinimas"
description: "Šioje temoje pateikiama informacija apie tai, kaip naujinti sumų rodymą ataskaitose ir kituose dokumentuose, skirtuose Estijai, Latvijai, Lietuvai, Lenkijai, Čekijos Respublikai, Vengrijai, ir Rusijai."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 264254
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a9e63af61b42ef3f5ef1d05a659cbec572e04a4f
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a><span data-ttu-id="b7742-103">Sumų rodymo ataskaitose ir dokumentuose būdo naujinimas</span><span class="sxs-lookup"><span data-stu-id="b7742-103">Update how amounts are displayed on reports and documents</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b7742-104">Šioje temoje pateikiama informacija apie tai, kaip naujinti sumų rodymą ataskaitose ir kituose dokumentuose, skirtuose Estijai, Latvijai, Lietuvai, Lenkijai, Čekijos Respublikai, Vengrijai, ir Rusijai.</span><span class="sxs-lookup"><span data-stu-id="b7742-104">This topic provides information about how to update how amounts are displayed on reports and other documents for Estonia, Latvia, Lithuania, Poland, Czech Republic, Hungary, and Russia.</span></span>

<span data-ttu-id="b7742-105">Jei pagrindinis juridinio subjekto adresas yra Estijoje,Latvijoje, Lietuvoje, Lenkijoje, Čekijos Respublikoje, Vengrijoje arba Rusijoje, galite nustatyti valiutos vienetų ir antrinių vienetų visus pavadinimus bei trumpus pavadinimus.</span><span class="sxs-lookup"><span data-stu-id="b7742-105">For legal entities in Estonia, Latvia, Lithuania, Poland, Czech Republic, Hungary, and Russia, you can set up full names and short names for currency units and subunits.</span></span> <span data-ttu-id="b7742-106">Šiuos pavadinimus galima naudoti norint pakeisti sumų rodymo dokumentuose ir ataskaitose būdą.</span><span class="sxs-lookup"><span data-stu-id="b7742-106">These names can be used to transform how amounts are represented on documents and reports.</span></span> <span data-ttu-id="b7742-107">Pvz., **100,20 LT** suma gali būti rodoma kaip **100 litų ir 20 centų**.</span><span class="sxs-lookup"><span data-stu-id="b7742-107">For example: The amount **LTL 100.20** can be displayed as **100 Litas 20 Centas**.</span></span>

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a><span data-ttu-id="b7742-108">Valiutos vienetų ir antrinių vienetų visų pavadinimų bei trumpų pavadinimų nustatymas</span><span class="sxs-lookup"><span data-stu-id="b7742-108">Set up full and short names for currency units and subunits</span></span>
<span data-ttu-id="b7742-109">Norėdami nustatyti valiutos vienetų ir antrinių vienetų visus pavadinimus bei trumpus pavadinimus, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b7742-109">To set up full and short names for currency units and subunits for a language, complete the following steps:</span></span>

1.  <span data-ttu-id="b7742-110">Atidarykite puslapį **Valiutos**.</span><span class="sxs-lookup"><span data-stu-id="b7742-110">Open the **Currencies** page.</span></span>
2.  <span data-ttu-id="b7742-111">Pasirinkite valiutą.</span><span class="sxs-lookup"><span data-stu-id="b7742-111">Select a currency.</span></span>
3.  <span data-ttu-id="b7742-112">Veiksmų srityje spustelėkite **Linksniavimas**.</span><span class="sxs-lookup"><span data-stu-id="b7742-112">On the Action Pane, click **Declension**.</span></span>
4.  <span data-ttu-id="b7742-113">Norėdami įtraukti kalbos visą ir trumpą pavadinimus, spustelėkite **Naujas** ir užpildykite tolesnius laukus.</span><span class="sxs-lookup"><span data-stu-id="b7742-113">To add full name and short name for a language, click **New** and complete the following fields.</span></span>
    |                                                           |                                                                                                                                                                                                                    |
    |-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="b7742-114">**Laukas**</span><span class="sxs-lookup"><span data-stu-id="b7742-114">**Field**</span></span>                                                 | <span data-ttu-id="b7742-115">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="b7742-115">**Description**</span></span>                                                                                                                                                                                                    |
    | <span data-ttu-id="b7742-116">**Kalba**</span><span class="sxs-lookup"><span data-stu-id="b7742-116">**Language**</span></span>                                              | <span data-ttu-id="b7742-117">Pasirinkti šio teksto kalbą.</span><span class="sxs-lookup"><span data-stu-id="b7742-117">Select the language for the current text.</span></span>                                                                                                                                                                          |
    | <span data-ttu-id="b7742-118">**Vienaskaitos vardininkas (laukų grupė Vienetų pavadinimas)**</span><span class="sxs-lookup"><span data-stu-id="b7742-118">**Singular nominative (Name of units field group)**</span></span>       | <span data-ttu-id="b7742-119">Įveskite valiutos pavadinimą vienaskaitos forma.</span><span class="sxs-lookup"><span data-stu-id="b7742-119">Enter the singular form of the currency.</span></span> <span data-ttu-id="b7742-120">Pvz., valiutos litas vienaskaitos forma yra litas.</span><span class="sxs-lookup"><span data-stu-id="b7742-120">For example, the singular form of Litas is Litas.</span></span>                                                                                                                         |
    | <span data-ttu-id="b7742-121">**Daugiskaitos vardininkas (laukų grupė Vienetų pavadinimas)**</span><span class="sxs-lookup"><span data-stu-id="b7742-121">**Plural nominative (Name of units field group)**</span></span>         | <span data-ttu-id="b7742-122">Įveskite valiutos pavadinimą daugiskaitos forma.</span><span class="sxs-lookup"><span data-stu-id="b7742-122">Enter the plural form of the currency.</span></span> <span data-ttu-id="b7742-123">Pavyzdžiui, įveskite litai.</span><span class="sxs-lookup"><span data-stu-id="b7742-123">For example, enter Litai.</span></span> <span data-ttu-id="b7742-124">**Pastaba**: laukai **Vienaskaitos kilmininkas** ir **Daugiskaitos kilmininkas** rodomi atsižvelgiant į lauke **Kalba** pasirinktą kalbą.</span><span class="sxs-lookup"><span data-stu-id="b7742-124">**Note**: The **Singular genitive** and **Plural genitive** fields are available based on the language that you select in the **Language** field.</span></span> |
    | <span data-ttu-id="b7742-125">**Laukas Vienaskaitos vardininkas (laukų grupė Dalių pavadinimas)**</span><span class="sxs-lookup"><span data-stu-id="b7742-125">**Singular nominative field (Name of parts field group)**</span></span> | <span data-ttu-id="b7742-126">Įveskite valiutos antrinio vieneto pavadinimą vienaskaitos forma.</span><span class="sxs-lookup"><span data-stu-id="b7742-126">Enter the singular form of the subunit of the currency.</span></span>                                                                                                                                                            |
    | <span data-ttu-id="b7742-127">**Daugiskaitos vardininkas (laukų grupė Dalių pavadinimas)**</span><span class="sxs-lookup"><span data-stu-id="b7742-127">**Plural nominative (Name of parts field group)**</span></span>         | <span data-ttu-id="b7742-128">Įveskite valiutos antrinio vieneto pavadinimą daugiskaitos forma.</span><span class="sxs-lookup"><span data-stu-id="b7742-128">Enter the plural form of the subunit of the currency.</span></span>                                                                                                                                                              |
    | <span data-ttu-id="b7742-129">**Trumpas vienetų pavadinimas (laukų grupė Trumpas pavadinimas)**</span><span class="sxs-lookup"><span data-stu-id="b7742-129">**Shortcut name of units (Short name field group)**</span></span>       | <span data-ttu-id="b7742-130">Įveskite ISO kodą, kad identifikuotumėte valiutą.</span><span class="sxs-lookup"><span data-stu-id="b7742-130">Enter the ISO code to identify the currency.</span></span> <span data-ttu-id="b7742-131">Pavyzdžiui, įveskite LTL identifikuoti litui..</span><span class="sxs-lookup"><span data-stu-id="b7742-131">For example, enter LTL to identify Litas.</span></span>                                                                                                                             |
    | <span data-ttu-id="b7742-132">**Trumpas dalių pavadinimas (laukų grupė Trumpas pavadinimas)**</span><span class="sxs-lookup"><span data-stu-id="b7742-132">**Shortcut name for parts (Short name field group)**</span></span>      | <span data-ttu-id="b7742-133">Įveskite valiutos antrinio vieneto nominaliąją vertę.</span><span class="sxs-lookup"><span data-stu-id="b7742-133">Enter the denomination of the currency subunit.</span></span> <span data-ttu-id="b7742-134">Pavyzdžiui, įveskite centas.</span><span class="sxs-lookup"><span data-stu-id="b7742-134">For example, enter Centas.</span></span>                                                                                                                                         |
    | <span data-ttu-id="b7742-135">**Jungtukas „ir“ tarp vienetų ir dalių**</span><span class="sxs-lookup"><span data-stu-id="b7742-135">**Conjunction 'and' between units and parts**</span></span>             | <span data-ttu-id="b7742-136">Pažymėkite, jei norite spausdinti jungtuką „ir“ tarp valiutos vienetų ir vieneto dalių.</span><span class="sxs-lookup"><span data-stu-id="b7742-136">Select to print the conjunction “and” between the currency units and unit parts.</span></span> <span data-ttu-id="b7742-137">Pvz., SF ir ataskaitose 100,20 LTL suma rodoma kaip 100 litų ir 20 centų.</span><span class="sxs-lookup"><span data-stu-id="b7742-137">For example, on invoices or reports, the amount for LTL 100.20 will be displayed as 100 Litas and 20 Centas.</span></span>                      |

5.  <span data-ttu-id="b7742-138">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b7742-138">Click **Save**.</span></span>





