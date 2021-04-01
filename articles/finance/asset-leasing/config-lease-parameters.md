---
title: Nuomos parametrų konfigūravimas (peržiūros versija)
description: Šioje temoje aprašomi modulio Turto nuoma konfigūracijos parametrai, pvz., saugos informacijos ir apskaitos parametrai.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4bb8372c5e4a1d7183b5d793b142fed92e833d5a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210438"
---
# <a name="configure-lease-parameters"></a><span data-ttu-id="f9f55-103">Nuomos parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="f9f55-103">Configure lease parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9f55-104">Keletas konfigūracijos parametrų lemia modulio Turto nuoma veikimą.</span><span class="sxs-lookup"><span data-stu-id="f9f55-104">Several configuration settings affect how Asset leasing behaves.</span></span> <span data-ttu-id="f9f55-105">Šie parametrai apima žurnalų pavadinimus, bendruosius parametrus ir registravimo šablonų parametrus.</span><span class="sxs-lookup"><span data-stu-id="f9f55-105">These settings include journal names, general parameters, and posting profile settings.</span></span>

1. <span data-ttu-id="f9f55-106">Eikite į **Turto nuoma \> Sąranka \> Turto nuomos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="f9f55-106">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="f9f55-107">Skirtuke **Nuomos** pasirinkite „FastTab“ **Bendra**.</span><span class="sxs-lookup"><span data-stu-id="f9f55-107">On the **Leases** tab, select the **General** FastTab.</span></span>

    <span data-ttu-id="f9f55-108">Parametras **Leisti neautomatinį klasifikacijos keitimą** nurodo, ar nuomos klasifikaciją galima pakeisti prieš patvirtintant mokėjimo grafiką.</span><span class="sxs-lookup"><span data-stu-id="f9f55-108">The **Allow manual classification override** parameter determines whether the lease classification can be overridden before the payment schedule is confirmed.</span></span>

    <span data-ttu-id="f9f55-109">Parametras **Kelių objektų paketas** nurodo, ar galite registruoti į kitus juridinius subjektus iš dabartinio juridinio subjekto.</span><span class="sxs-lookup"><span data-stu-id="f9f55-109">The **Cross-entity batch** parameter determines whether you can post to other legal entities from the current legal entity.</span></span> <span data-ttu-id="f9f55-110">Jei šis parametras įjungtas, galite kurti juridinių subjektų, prie kurių turite prieigą, žurnalo įrašus.</span><span class="sxs-lookup"><span data-stu-id="f9f55-110">If this parameter is turned on, you can create journal entries for the legal entities that you have access to.</span></span>

3. <span data-ttu-id="f9f55-111">Nustatykite parinktį **Leisti panaikinti patvirtintas nuomas** kaip **Taip**, kad būtų galima panaikinti patvirtintų mokėjimo grafikų nuomas.</span><span class="sxs-lookup"><span data-stu-id="f9f55-111">Set the **Allow delete of confirmed leases** option to **Yes** to allow leases that have confirmed payment schedules to be deleted.</span></span> <span data-ttu-id="f9f55-112">Nuomų negalima panaikinti, jei su jomis susietos užregistruotos arba neužregistruotos operacijos, nepaisant šios pasirinkties parametro.</span><span class="sxs-lookup"><span data-stu-id="f9f55-112">Leases can't be deleted if posted or unposted transactions are associated with them, regardless of the setting of this option.</span></span> <span data-ttu-id="f9f55-113">Po to, kai nuomos įrašas panaikinamas, jo atkurti negalima.</span><span class="sxs-lookup"><span data-stu-id="f9f55-113">You can't restore a lease record after it's deleted.</span></span> <span data-ttu-id="f9f55-114">Jei nusiunčiate panaikintos nuomos įrašų neautomatiniu būdu arba per duomenų objektus, nusiųsta informacija laikoma nauja, o ne esamos nuomos atnaujinimu.</span><span class="sxs-lookup"><span data-stu-id="f9f55-114">If you upload any records for a deleted lease, either manually or through data entities, the uploaded information is treated as new, not as an update to an existing lease.</span></span>

    <span data-ttu-id="f9f55-115">Jei šią parinktį nustatote kaip **Taip**, o knygos perėjimo tipas yra **Kaupiamoji atgalinės datos A arba B parinktis**, sistema nustato lauką **Apskaičiuota skolinimosi palūkanų norma** kaip puslapio **Knygų sąranka** lauko **Apskaičiuota skolinimosi palūkanų norma pereinant** reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f9f55-115">If you set this option to **Yes**, and the transition type of the book is **Cumulative Catchup Option A or B**, the system sets the **Incremental borrowing rate** field to the value of the **Incremental borrowing rate at transition** field on the **Book setup** page.</span></span> <span data-ttu-id="f9f55-116">Jei ši parinktis nustatyta kaip **Ne**, pagrindinės nuomos norma nustatoma kaip puslapio **Knygų informacija** lauko **Apskaičiuota skolinimosi palūkanų norma** reikšmė, neatsižvelgiant į knygos perėjimo tipą.</span><span class="sxs-lookup"><span data-stu-id="f9f55-116">If this option is set to **No**, the rate on the head lease is set to the value of the **Incremental borrowing rate** field on the **Book details** page, regardless of the transition type of the book.</span></span>

4. <span data-ttu-id="f9f55-117">Nustatykite parinktį **Leisti nusidėvėjimo atšaukimus uždarytos knygos versijoje** kaip **Taip**, kad būtų galima atšaukti nusidėvėjimo išlaidų operacijas.</span><span class="sxs-lookup"><span data-stu-id="f9f55-117">Set the **Allow depreciation reversals on closed book version** option to **Yes** to allow depreciation expense transactions to be reversed.</span></span> <span data-ttu-id="f9f55-118">Išlaidų operacijos gali būti atšauktos net uždarius knygos versiją.</span><span class="sxs-lookup"><span data-stu-id="f9f55-118">Expense transactions can be reversed even when the book version is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f9f55-119">Rekomenduojame šią pasirinktį palikti nustatytą kaip **Ne**.</span><span class="sxs-lookup"><span data-stu-id="f9f55-119">We recommend that you keep this option set to **No**.</span></span> <span data-ttu-id="f9f55-120">Šios parinkties nustatymas naudojamas kaip patikra ir valdiklis, siekiant apsaugoti uždarytos knygos versiją nuo netyčinio nusidėvėjimo.</span><span class="sxs-lookup"><span data-stu-id="f9f55-120">The setting of this option is used as a validation and control to prevent a closed book version from being accidently depreciated.</span></span> <span data-ttu-id="f9f55-121">Palikdami parametrą nustatytą kaip **Ne**, padėsite išsaugoti tikslią balansinę vertę ir būsimus nusidėvėjimo skaičiavimus.</span><span class="sxs-lookup"><span data-stu-id="f9f55-121">By keeping the option set to **No**, you help keep the net book value and future depreciation calculations accurate.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]