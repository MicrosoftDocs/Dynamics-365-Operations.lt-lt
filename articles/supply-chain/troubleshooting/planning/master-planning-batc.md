---
title: Negalite filtruoti bendrojo planavimo prekių pagal jų susijusias padengimo grupės reikšmes
description: Negalite filtruoti bendrojo planavimo prekių pagal jų susijusias padengimo grupės reikšmes.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049481"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a><span data-ttu-id="3873b-103">Negalite filtruoti bendrojo planavimo prekių pagal jų susijusias padengimo grupės reikšmes</span><span class="sxs-lookup"><span data-stu-id="3873b-103">You can't filter master planning items by their related coverage group values</span></span>

<span data-ttu-id="3873b-104">KB numeris: 4612572</span><span class="sxs-lookup"><span data-stu-id="3873b-104">KB number: 4612572</span></span>

## <a name="symptoms"></a><span data-ttu-id="3873b-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="3873b-105">Symptoms</span></span>

<span data-ttu-id="3873b-106">Norite filtruoti prekes, kurios bus įtrauktos į bendrojo planavimo paketinę užduotį, remiantis susijusių įrašų reikšmėmis iš prekių padengimo lentelės.</span><span class="sxs-lookup"><span data-stu-id="3873b-106">You want to filter the items that will be included in a master planning batch job, based on the values of related records from the item coverage table.</span></span> <span data-ttu-id="3873b-107">(Pavyzdžiui, norite filtruoti prekes pagal jų **Tiekėjo** ir (arba) **Padengimo grupės** reikšmę).</span><span class="sxs-lookup"><span data-stu-id="3873b-107">(For example, you want to filter items by their **Vendor** and/or **Coverage group** value).</span></span> <span data-ttu-id="3873b-108">Paketinės užduoties filtro nustatymas leidžia jums sukurti jungtį iš **Prekių** lentelės į **Prekių padengimo** lentelę, o tada nurodyti laukų reikšmės iš prekių padengimo lentelės jūsų užklausoje.</span><span class="sxs-lookup"><span data-stu-id="3873b-108">The filter setup for the batch job lets you create a join from the **Items** table to the **Item coverage** table, and then specify field values from the item coverage table in your query.</span></span> <span data-ttu-id="3873b-109">Tačiau, jums užbaigus šį nustatymą, sistema vis tiek kuria suplanuotus užsakymus visam prekių padengimui, o ne tik prekėms, kurios atitinka nurodytas laukų reikšmes iš prekių padengimo lentelės.</span><span class="sxs-lookup"><span data-stu-id="3873b-109">However, after you complete this setup, the system still creates planned orders for the whole item coverage, not just for the items that match the specified field values from the item coverage table.</span></span>

## <a name="resolution"></a><span data-ttu-id="3873b-110">Paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="3873b-110">Resolution</span></span>

<span data-ttu-id="3873b-111">Paketinių užduočių filtras gali filtruoti tik prekes.</span><span class="sxs-lookup"><span data-stu-id="3873b-111">The batch job filter can filter only on items.</span></span> <span data-ttu-id="3873b-112">Nors galite įtraukti sujungimą į **Prekės padengimo** lentelę, filtravimo parametrai, kuriuos taikote tai lentelei, nepaveiks užklausos išeigos.</span><span class="sxs-lookup"><span data-stu-id="3873b-112">Although you can add a join to the **Item coverage** table, filter settings that you make against that table won't affect the query output.</span></span> <span data-ttu-id="3873b-113">Vykdymo metu sistema vykdo visų padengimo grupių ir visų filtruotų prekių variantų planavimą.</span><span class="sxs-lookup"><span data-stu-id="3873b-113">At runtime, the system runs planning for all the coverage groups and all the variations that the filtered items have.</span></span> <span data-ttu-id="3873b-114">Kai prekė jau yra įtraukta į vykdymą, visos į prekės filtrą įtrauktos padengimo grupės nebus paveiktos planavimo išeigos.</span><span class="sxs-lookup"><span data-stu-id="3873b-114">After an item is already included in the run, any coverage groups that are included in the item filter a won't affect the planning output.</span></span>
