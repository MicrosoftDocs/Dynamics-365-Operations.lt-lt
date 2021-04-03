---
title: ER LIST funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) LIST funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 4945ffd0e7bb7bbd238e2d3156c5599d3d423046
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563853"
---
# <a name="list-er-function"></a><span data-ttu-id="f9687-103">ER LIST funkcija</span><span class="sxs-lookup"><span data-stu-id="f9687-103">LIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9687-104">`LIST` funkcija pateikia tipo *Įrašų sąrašas* reikšmę, sudarytą iš naujo įrašų sąrašo, sukurto iš nurodytų argumentų.</span><span class="sxs-lookup"><span data-stu-id="f9687-104">The `LIST` function returns a *Record list* value that consists of a new list of records that is created from the specified arguments.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9687-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="f9687-105">Syntax</span></span>

```vb
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a><span data-ttu-id="f9687-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="f9687-106">Arguments</span></span>

<span data-ttu-id="f9687-107">`record 1`: *Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="f9687-107">`record 1`: *Container (record)*</span></span>

<span data-ttu-id="f9687-108">Nuoroda į duomenų tipo *Įrašas* duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="f9687-108">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="f9687-109">Šis argumentas yra būtinas.</span><span class="sxs-lookup"><span data-stu-id="f9687-109">This argument is required.</span></span>

<span data-ttu-id="f9687-110">`record N`: *Konteineris (įrašas)*</span><span class="sxs-lookup"><span data-stu-id="f9687-110">`record N`: *Container (record)*</span></span>

<span data-ttu-id="f9687-111">Nuoroda į duomenų tipo *Įrašas* duomenų šaltinį.</span><span class="sxs-lookup"><span data-stu-id="f9687-111">A reference to a data source of the *Record* data type.</span></span> <span data-ttu-id="f9687-112">Šie papildomi argumentai yra pasirinktiniai.</span><span class="sxs-lookup"><span data-stu-id="f9687-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="f9687-113">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="f9687-113">Return values</span></span>

<span data-ttu-id="f9687-114">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="f9687-114">*Record list*</span></span>

<span data-ttu-id="f9687-115">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="f9687-115">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f9687-116">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="f9687-116">Usage notes</span></span>

<span data-ttu-id="f9687-117">Sukurto sąrašo struktūroje yra tik tie laukai, kurie pateikiami kiekvieno argumentuose paminėto įrašo struktūroje.</span><span class="sxs-lookup"><span data-stu-id="f9687-117">The structure of the list that is created contains only the fields that are presented in the structure of every record that is mentioned in the arguments.</span></span>

## <a name="example"></a><span data-ttu-id="f9687-118">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="f9687-118">Example</span></span>

<span data-ttu-id="f9687-119">Įvedate tipo *Konteineris* duomenų šaltinį **1-asis įrašas**.</span><span class="sxs-lookup"><span data-stu-id="f9687-119">You enter data source **Record 1** of the *Container* type.</span></span> <span data-ttu-id="f9687-120">Šiame duomenų šaltinyje yra tolesni įdėtieji tipo *Apskaičiuotasis laukas* laukai.</span><span class="sxs-lookup"><span data-stu-id="f9687-120">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="f9687-121">**Kodas.** Šiame lauke yra reiškinys, pateikiantis tipo *Eilutė* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f9687-121">**Code:** This field contains an expression that returns a value of the *String* type.</span></span>
- <span data-ttu-id="f9687-122">**Suma.** Šiame lauke yra reiškinys, pateikiantis tipo *Realusis skaičius* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f9687-122">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>

<span data-ttu-id="f9687-123">Tada įvedate tipo *Konteineris* duomenų šaltinį **2-asis įrašas**.</span><span class="sxs-lookup"><span data-stu-id="f9687-123">You then enter data source **Record 2** of the *Container* type.</span></span> <span data-ttu-id="f9687-124">Šiame duomenų šaltinyje yra tolesni įdėtieji tipo *Apskaičiuotasis laukas* laukai.</span><span class="sxs-lookup"><span data-stu-id="f9687-124">This data source contains the following nested fields of the *Calculated field* type:</span></span>

- <span data-ttu-id="f9687-125">**Suma.** Šiame lauke yra reiškinys, pateikiantis tipo *Realusis skaičius* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f9687-125">**Amount:** This field contains an expression that returns a value of the *Real* type.</span></span>
- <span data-ttu-id="f9687-126">**IsValid.** Šiame lauke yra reiškinys, pateikiantis tipo *Bulio logika* reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f9687-126">**IsValid:** This field contains an expression that returns a value of the *Boolean* type.</span></span>

<span data-ttu-id="f9687-127">Šiuo atveju reiškinys `LIST('Record 1', 'Record 2')` pateikia naują sąrašą, kuriame yra du įrašai.</span><span class="sxs-lookup"><span data-stu-id="f9687-127">In this case, the expression `LIST('Record 1', 'Record 2')` returns a new list that contains two records.</span></span> <span data-ttu-id="f9687-128">Šio sąrašo struktūrą sudaro vienas tipo *Realusis skaičius* laukas **Suma**, nes šis laukas yra vienintelis laukas, pateikiamas kiekviename iškviestos funkcijos argumente.</span><span class="sxs-lookup"><span data-stu-id="f9687-128">The structure of this list consists of a single **Amount** field of the *Real* type, because this field is the only field that is presented in every argument of the called function.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9687-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="f9687-129">Additional resources</span></span>

[<span data-ttu-id="f9687-130">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="f9687-130">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]