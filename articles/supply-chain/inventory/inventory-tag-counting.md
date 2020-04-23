---
title: Atsargų žymių inventorizacija
description: Šioje temoje pateikiama informacija apie žymių skaičiavimą, kurį naudojate norėdami palyginti faktinį sandėlio turinį su turimomis atsargomis.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCountTag
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 11594
ms.assetid: 03772d0e-5c37-454c-ab85-82bc8b60a76d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efb555cdfbcf3fd0c10ec0e2abcdbe7f4a90d82d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212692"
---
# <a name="inventory-tag-counting"></a><span data-ttu-id="a2cc7-103">Atsargų žymių inventorizacija</span><span class="sxs-lookup"><span data-stu-id="a2cc7-103">Inventory tag counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2cc7-104">Šioje temoje pateikiama informacija apie žymių skaičiavimą, kurį naudojate norėdami palyginti faktinį sandėlio turinį su turimomis atsargomis.</span><span class="sxs-lookup"><span data-stu-id="a2cc7-104">This topic provides information about tag counting, which you use to compare the actual contents of a warehouse with the on-hand inventory.</span></span>

<span data-ttu-id="a2cc7-105">Puslapyje **Skaičiavimas pagal žymes** kurdami eilutes, kiekvienai atsargų prekei priskiriate žymės numerį, pvz., skaičių nuo 1 iki 500.</span><span class="sxs-lookup"><span data-stu-id="a2cc7-105">By creating lines on the **Tag counting** page, you place a tag number on each inventory item, such as a number from 1 to 500.</span></span> <span data-ttu-id="a2cc7-106">Skaičiuojant prekės numeris ir kiekis įvedami atitinkamoje žymėje.</span><span class="sxs-lookup"><span data-stu-id="a2cc7-106">During the count, you enter the item number and the quantity on a corresponding tag.</span></span> <span data-ttu-id="a2cc7-107">Šią žymę tada galima naudoti kaip įvesties pagrindą skaičiavimo pagal žymes žurnale.</span><span class="sxs-lookup"><span data-stu-id="a2cc7-107">This tag can then be used as the basis for input in the tag counting journal.</span></span> <span data-ttu-id="a2cc7-108">Užregistravus skaičiavimo pagal žymes žurnalą, **Skaičiavimo** puslapyje sukuriamas naujas skaičiavimo žurnalas.</span><span class="sxs-lookup"><span data-stu-id="a2cc7-108">After you post the tag counting journal, a new counting journal is created on the **Counting** page.</span></span> <span data-ttu-id="a2cc7-109">Naujasis žurnalas paremtas jūsų sukurtomis skaičiavimo pagal žymes žurnalo eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="a2cc7-109">The new journal is based on the tag counting journal lines that you created.</span></span> <span data-ttu-id="a2cc7-110">Jei, prekes skaičiuodami pagal žymę, tai norite daryti pagal konkrečią atsargų dimensiją, puslapyje **Rodyti dimensiją**, kuris rodomas, kai kuriate skaičiavimo pagal žymes žurnalą, pasirinkite dimensiją.</span><span class="sxs-lookup"><span data-stu-id="a2cc7-110">To tag-count items by a specific inventory dimension, select the dimension on the **Display dimension** page that is displayed when you create the tag counting journal.</span></span> <span data-ttu-id="a2cc7-111">Pavyzdžiui, norėdami skaičiuoti konkretaus sandėlio prekes, pasirinkite **Sandėlio** žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="a2cc7-111">For example, to count items in a specific warehouse, select the **Warehouse** check box.</span></span> <span data-ttu-id="a2cc7-112">Jei **Atsargų ir sandėlio valdymo parametrų** puslapyje pasirinktas slankikis **Blokuoti prekes jas skaičiuojant**, skaičiuojant prekes, prekių fiziškai atnaujinti negalima.</span><span class="sxs-lookup"><span data-stu-id="a2cc7-112">If the **Lock items during count** slider on the **Inventory and warehouse management parameters** page is selected, items can't be physically updated during counting.</span></span> <span data-ttu-id="a2cc7-113">Tačiau skaičiuojant skaičiavimo pagal žymes žurnalų prekės neblokuojamos.</span><span class="sxs-lookup"><span data-stu-id="a2cc7-113">However, items in tag counting journals aren't locked during counting.</span></span> <span data-ttu-id="a2cc7-114">Atsargų operacijos nekuriamos tol, kol skaičiavimo pagal žymes eilutės neregistruojamos ir neperkeliamos į skaičiavimo žurnalą.</span><span class="sxs-lookup"><span data-stu-id="a2cc7-114">Inventory transactions aren't created until the tag counting lines are posted and transferred to a counting journal.</span></span> <span data-ttu-id="a2cc7-115">Jei žymės įvedamos atsitiktine tvarka, ir norite identifikuoti trūkstamas žymes, spustelėkite stulpelio antraštę **Žymė** – eilutės bus surūšiuotos pagal žymę.</span><span class="sxs-lookup"><span data-stu-id="a2cc7-115">If tags are entered randomly, and you want to identify missing tags, click the **Tag** column header to sort the lines by tag.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2cc7-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="a2cc7-116">Additional resources</span></span>

[<span data-ttu-id="a2cc7-117">Ciklų skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="a2cc7-117">Cycle counting</span></span>](../warehousing/cycle-counting.md)
