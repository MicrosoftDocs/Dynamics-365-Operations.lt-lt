---
title: Ilgalaikio turto susiejimas su nuomomis
description: Temoje paaiškinama, kaip susieti esamą ilgalaikį turtą su nauja nuoma.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5c4f14d38b3cfc2c4d09cfeb5854204701250757
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260858"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="b04d9-103">Ilgalaikio turto susiejimas su nuomomis</span><span class="sxs-lookup"><span data-stu-id="b04d9-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b04d9-104">Temoje paaiškinama, kaip susieti esamą ilgalaikį turtą su nauja nuoma.</span><span class="sxs-lookup"><span data-stu-id="b04d9-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="b04d9-105">Kai susiejate ilgalaikį turtą su nuoma, ilgalaikio turto įsigijimo kaina bus naudojimo teise valdomo turto pirminio pripažinimo vertė.</span><span class="sxs-lookup"><span data-stu-id="b04d9-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="b04d9-106">Kad galėtumėte susieti ilgalaikį turtą su nuoma, turite sukurti ilgalaikio turto įrašą dalyje Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="b04d9-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="b04d9-107">Tada puslapyje **Nuomos suvestinė** turite sukurti nuomą ir susieti turtą su ta nuoma.</span><span class="sxs-lookup"><span data-stu-id="b04d9-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="b04d9-108">Įtraukite nuomą, atlikdami veiksmus, nurodytus temoje [Nuomų įtraukimas arba kopijavimas](add-lease.md).</span><span class="sxs-lookup"><span data-stu-id="b04d9-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="b04d9-109">Puslapio **Nuomos įtraukimas** lauke **Ilgalaikio turto numeris** pasirinkite turtą, kuris dar nebuvo įsigytas.</span><span class="sxs-lookup"><span data-stu-id="b04d9-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="b04d9-110">Pasirinkite **Knygos** ir patvirtinkite mokėjimo grafiką.</span><span class="sxs-lookup"><span data-stu-id="b04d9-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="b04d9-111">Pasirinkite **Pradinis pripažinimas**.</span><span class="sxs-lookup"><span data-stu-id="b04d9-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="b04d9-112">Pasirinkite **Turto nuomos žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="b04d9-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="b04d9-113">Nuomos pradinio pripažinimo žurnalo įrašas debetuoja ilgalaikio turto sumą, kuri paprastai debetuojama į naudojimo teise valdomo turto sąskaitą.</span><span class="sxs-lookup"><span data-stu-id="b04d9-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="b04d9-114">Dabar galite peržiūrėti ilgalaikio turto operacijos tipą ir knygą.</span><span class="sxs-lookup"><span data-stu-id="b04d9-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="b04d9-115">Pasirinkite **Žurnalo informacija**.</span><span class="sxs-lookup"><span data-stu-id="b04d9-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="b04d9-116">Pasirinkite **Eilutės**, norėdami peržiūrėti atskiras žurnalo įrašo eilutes.</span><span class="sxs-lookup"><span data-stu-id="b04d9-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="b04d9-117">Pasirinkite žurnalo eilutę, kurioje yra turtas, tada pasirinkite skirtuką **Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="b04d9-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="b04d9-118">Skirtuke **Ilgalaikis turtas** rodomas operacijos tipas ir knyga.</span><span class="sxs-lookup"><span data-stu-id="b04d9-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="b04d9-119">Numatyta, kad laukas **Operacijos tipas** nustatytas kaip **Įsigijimas**, o laukas **Knyga** nustatytas kaip dabartinė ilgalaikio turto knyga.</span><span class="sxs-lookup"><span data-stu-id="b04d9-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="b04d9-120">Užregistravus pradinio pripažinimo žurnalo įrašą, operacija rodoma kaip ilgalaikio turto įsigijimo operacija.</span><span class="sxs-lookup"><span data-stu-id="b04d9-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="b04d9-121">Norėdami peržiūrėti operacijų lentelę, eikite į **Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**, pasirinkite reikiamą turtą ir **Vertinimai**.</span><span class="sxs-lookup"><span data-stu-id="b04d9-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="b04d9-122">Turėtumėte matyti, kad pradinio pripažinimo žurnalo įrašas sukūrė nurodyto ilgalaikio turto įsigijimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="b04d9-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="b04d9-123">Ilgalaikį turtą dabar galima nudėvėti naudojant standartinę ilgalaikio turto nusidėvėjimo funkciją dalyje Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="b04d9-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="b04d9-124">Daugiau informacijos apie nusidėvėjimą žr. [Nusidėvėjimo metodai ir konvencijos](../fixed-assets/depreciation-methods-conventions.md).</span><span class="sxs-lookup"><span data-stu-id="b04d9-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b04d9-125">Jei susiejate ilgalaikį turtą su nuoma, mygtukai **Turto nusidėvėjimas** ir **Nuomos nuvertėjimas** modulyje Turto nuoma yra išjungti.</span><span class="sxs-lookup"><span data-stu-id="b04d9-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="b04d9-126">Ilgalaikio turto nusidėvėjimo ir nuomos nuvertėjimo operacijas galite peržiūrėti dalyje Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="b04d9-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="b04d9-127">Mygtukas **Turto operacijos**, kuriuo atidaroma užklausos forma, taip pat išjungtas.</span><span class="sxs-lookup"><span data-stu-id="b04d9-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="b04d9-128">Taip pat galite atidaryti **ilgalaikio turto operacijų** užklausos formą dalyje Ilgalaikis turtas.</span><span class="sxs-lookup"><span data-stu-id="b04d9-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]