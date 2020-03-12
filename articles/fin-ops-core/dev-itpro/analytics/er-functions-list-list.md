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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee51b6da008d1c0fcfb303e9659f507629237333
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042026"
---
# <span data-ttu-id="3b15f-103"><a name="LIST">ER LIST funkcija</a></span><span class="sxs-lookup"><span data-stu-id="3b15f-103"><a name="LIST">LIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b15f-104">`LIST` funkcija pateikia tipo *Įrašų sąrašas* reikšmę, sudarytą iš naujo įrašų sąrašo, sukurto iš nurodytų argumentų.</span><span class="sxs-lookup"><span data-stu-id="3b15f-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b15f-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="3b15f-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="3b15f-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="3b15f-106">Arguments</span></span>

<span data-ttu-id="3b15f-107">`record 1`: *Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="3b15f-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="3b15f-108">Nuoroda į duomenų tipo *Įrašas* duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="3b15f-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="3b15f-109">Šis argumentas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="3b15f-109">This argument is required.</span></span>

<span data-ttu-id="3b15f-110">`record N`: *Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="3b15f-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="3b15f-111">Nuoroda į duomenų tipo *Įrašas* duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="3b15f-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="3b15f-112">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="3b15f-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="3b15f-113">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="3b15f-113">Return values</span></span>

<span data-ttu-id="3b15f-114">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="3b15f-114">*Record list*</span></span>

<span data-ttu-id="3b15f-115">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="3b15f-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3b15f-116">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="3b15f-116">Usage notes</span></span>

<span data-ttu-id="3b15f-117">Sukurto sąrašo struktūroje yra tik tie laukai, kurie pateikiami kiekvieno argumentuose paminėto įrašo struktūroje.</span><span class="sxs-lookup"><span data-stu-id="3b15f-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="3b15f-118">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="3b15f-118">Example</span></span>

<span data-ttu-id="3b15f-119">Įvedate tipo *Konteineris* duomenų šaltinį **1-asis įrašas**.</span><span class="sxs-lookup"><span data-stu-id="3b15f-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="3b15f-120">Šiame duomenų šaltinyje yra tolesni įdėtieji tipo *Apskaičiuotasis laukas* laukai.</span><span class="sxs-lookup"><span data-stu-id="3b15f-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="3b15f-121">**Kodas.** Šiame lauke yra reiškinys, pateikiantis tipo *Eilutė* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3b15f-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="3b15f-122">**Suma.** Šiame lauke yra reiškinys, pateikiantis tipo *Realusis skaičius* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3b15f-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="3b15f-123">Tada įvedate tipo *Konteineris* duomenų šaltinį **2-asis įrašas**.</span><span class="sxs-lookup"><span data-stu-id="3b15f-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="3b15f-124">Šiame duomenų šaltinyje yra tolesni įdėtieji tipo *Apskaičiuotasis laukas* laukai.</span><span class="sxs-lookup"><span data-stu-id="3b15f-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="3b15f-125">**Suma.** Šiame lauke yra reiškinys, pateikiantis tipo *Realusis skaičius* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3b15f-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="3b15f-126">**IsValid.** Šiame lauke yra reiškinys, pateikiantis tipo *Bulio logika* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="3b15f-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="3b15f-127">Šiuo atveju reiškinys `LIST('Record 1', 'Record 2')` pateikia naują sąrašą, kuriame yra du įrašai.</span><span class="sxs-lookup"><span data-stu-id="3b15f-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="3b15f-128">Šio sąrašo struktūrą sudaro vienas tipo *Realusis skaičius* laukas **Suma**, nes šis laukas yra vienintelis laukas, pateikiamas kiekviename iškviestos funkcijos argumente.</span><span class="sxs-lookup"><span data-stu-id="3b15f-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b15f-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3b15f-129">Additional resources</span></span>

[<span data-ttu-id="3b15f-130">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="3b15f-130">List functions</span></span>](er-functions-category-list.md)
