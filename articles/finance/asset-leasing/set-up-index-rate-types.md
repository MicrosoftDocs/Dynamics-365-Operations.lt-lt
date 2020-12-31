---
title: Indeksuojamos palūkanų normos nustatymas
description: Šioje temoje paaiškinama, kaip nustatyti indeksuojamą palūkanų normą. Indekso tarifai reikalingi, jei jūsų organizacija sieja nuomos įmokų sumas su indeksų kursų rinkiniu.
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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 16b83102aa76f46473138f89ea487e71668a188c
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4446189"
---
# <a name="set-up-index-rates"></a><span data-ttu-id="22fc3-104">Indeksuojamos palūkanų normos nustatymas</span><span class="sxs-lookup"><span data-stu-id="22fc3-104">Set up index rates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22fc3-105">Jei nuomos mokėjimai priklauso nuo indekso, sistemoje galima įtraukti ir tvarkyti indekso tarifo tipus.</span><span class="sxs-lookup"><span data-stu-id="22fc3-105">If lease payments depend on an index, the index rate types can be added and maintained in the system.</span></span> <span data-ttu-id="22fc3-106">Norint perkainoti nuomos mokėjimus iš puslapio **Indeksuojamos palūkanų normos tipas**, indeksuojamos palūkanų normos perkainojimo procesas naudoja naujausią indeksuojamą palūkanų normą nuo perkainojimo datos.</span><span class="sxs-lookup"><span data-stu-id="22fc3-106">To revalue the lease payments from the **Index rate type** page, the index rate revaluation process uses the most recent index rate from the date of revaluation.</span></span>

<span data-ttu-id="22fc3-107">Norėdami pridėti indekso kurso tipus ir indeksų tarifus, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="22fc3-107">To add index rate types and index rates, follow these steps.</span></span>

1. <span data-ttu-id="22fc3-108">Eikite į **Turto nuoma \> Sąranka \> Indeksuojamos palūkanų normos tipas**.</span><span class="sxs-lookup"><span data-stu-id="22fc3-108">Go to **Asset leasing \> Setup \> Index rate type**.</span></span>
2. <span data-ttu-id="22fc3-109">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="22fc3-109">Select **New**.</span></span>
3. <span data-ttu-id="22fc3-110">Atitinkamuose laukuose įveskite indekso koeficiento, kurio koeficientas, tarifo tipą ir pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="22fc3-110">In the appropriate fields, enter the rate type and the name of the index rate.</span></span>
4. <span data-ttu-id="22fc3-111">Norėdami pridėti naują indekso tarifo vertę, pasirinkite indeksuojamos palūkanų normos tipą ir pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="22fc3-111">To add a new index rate value, select the index rate type, and then select **Add**.</span></span>
5. <span data-ttu-id="22fc3-112">Pasirinkite normos galiojimo pradžios datą ir pasirinkite tarifo vertę.</span><span class="sxs-lookup"><span data-stu-id="22fc3-112">Select the effective start date of the rate, and select the rate value.</span></span>

<span data-ttu-id="22fc3-113">Turite pasirinkti **indeksuojamos palūkanų normos vertės skirtumą** arba **indeksuojamos palūkanų normos vertę** kaip indeksuojamos palūkanų normos metodą.</span><span class="sxs-lookup"><span data-stu-id="22fc3-113">You must select either **Index rate value difference** or **Index rate value** as the index rate method.</span></span>

- <span data-ttu-id="22fc3-114">Pasirinkite metodą **Indeksuojamos palūkanų normos vertės skirtumas** naujam nuomos mokėjimui apskaičiuoti, atsižvelgiant į skirtumą tarp indekso kurso pradžios data ir naujausio indekso kurso.</span><span class="sxs-lookup"><span data-stu-id="22fc3-114">Select the **Index rate value difference** method to calculate a new lease payment, based on the difference between the index rate on the start date and the most recent index rate.</span></span> <span data-ttu-id="22fc3-115">Indeksuojama palūkanų norma nustatoma lauke **Indeksuojama palūkanų norma (%)**.</span><span class="sxs-lookup"><span data-stu-id="22fc3-115">The index rate is defined in the **Index rate (%)** field.</span></span>
- <span data-ttu-id="22fc3-116">Pasirinkite metodą **Indeksuojamos palūkanų normos vertė**, norėdami apskaičiuoti nuomos mokestį pagal procentinę dalį, nurodytą lauke **Indeksuojama palūkanų norma (%)**.</span><span class="sxs-lookup"><span data-stu-id="22fc3-116">Select the **Index rate value** method to calculate the lease payment by using the percentage that is specified in the **Index rate (%)** field.</span></span>
