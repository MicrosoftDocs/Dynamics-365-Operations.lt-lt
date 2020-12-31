---
title: ER LIST funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) LIST funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7f8e701ec2836206d2299abba5e5b8542b4cf92
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683092"
---
# <a name="list-er-function"></a><span data-ttu-id="632ca-103">ER LIST funkcija</span><span class="sxs-lookup"><span data-stu-id="632ca-103">LIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="632ca-104">`LIST` funkcija pateikia tipo *Įrašų sąrašas* reikšmę, sudarytą iš naujo įrašų sąrašo, sukurto iš nurodytų argumentų.</span><span class="sxs-lookup"><span data-stu-id="632ca-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="632ca-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="632ca-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="632ca-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="632ca-106">Arguments</span></span>

<span data-ttu-id="632ca-107">`record 1`: *Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="632ca-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="632ca-108">Nuoroda į duomenų tipo *Įrašas* duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="632ca-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="632ca-109">Šis argumentas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="632ca-109">This argument is required.</span></span>

<span data-ttu-id="632ca-110">`record N`: *Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="632ca-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="632ca-111">Nuoroda į duomenų tipo *Įrašas* duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="632ca-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="632ca-112">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="632ca-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="632ca-113">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="632ca-113">Return values</span></span>

<span data-ttu-id="632ca-114">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="632ca-114">*Record list*</span></span>

<span data-ttu-id="632ca-115">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="632ca-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="632ca-116">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="632ca-116">Usage notes</span></span>

<span data-ttu-id="632ca-117">Sukurto sąrašo struktūroje yra tik tie laukai, kurie pateikiami kiekvieno argumentuose paminėto įrašo struktūroje.</span><span class="sxs-lookup"><span data-stu-id="632ca-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="632ca-118">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="632ca-118">Example</span></span>

<span data-ttu-id="632ca-119">Įvedate tipo *Konteineris* duomenų šaltinį **1-asis įrašas**.</span><span class="sxs-lookup"><span data-stu-id="632ca-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="632ca-120">Šiame duomenų šaltinyje yra tolesni įdėtieji tipo *Apskaičiuotasis laukas* laukai.</span><span class="sxs-lookup"><span data-stu-id="632ca-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="632ca-121">**Kodas.** Šiame lauke yra reiškinys, pateikiantis tipo *Eilutė* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="632ca-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="632ca-122">**Suma.** Šiame lauke yra reiškinys, pateikiantis tipo *Realusis skaičius* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="632ca-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="632ca-123">Tada įvedate tipo *Konteineris* duomenų šaltinį **2-asis įrašas**.</span><span class="sxs-lookup"><span data-stu-id="632ca-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="632ca-124">Šiame duomenų šaltinyje yra tolesni įdėtieji tipo *Apskaičiuotasis laukas* laukai.</span><span class="sxs-lookup"><span data-stu-id="632ca-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="632ca-125">**Suma.** Šiame lauke yra reiškinys, pateikiantis tipo *Realusis skaičius* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="632ca-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="632ca-126">**IsValid.** Šiame lauke yra reiškinys, pateikiantis tipo *Bulio logika* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="632ca-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="632ca-127">Šiuo atveju reiškinys `LIST('Record 1', 'Record 2')` pateikia naują sąrašą, kuriame yra du įrašai.</span><span class="sxs-lookup"><span data-stu-id="632ca-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="632ca-128">Šio sąrašo struktūrą sudaro vienas tipo *Realusis skaičius* laukas **Suma**, nes šis laukas yra vienintelis laukas, pateikiamas kiekviename iškviestos funkcijos argumente.</span><span class="sxs-lookup"><span data-stu-id="632ca-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="632ca-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="632ca-129">Additional resources</span></span>

[<span data-ttu-id="632ca-130">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="632ca-130">List functions</span></span>](er-functions-category-list.md)
