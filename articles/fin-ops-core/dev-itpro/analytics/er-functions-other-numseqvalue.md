---
title: NUMSEQVALUE ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama NUMSEQVALUE elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: d68784524a5639d8d447daa2cda940680d795542
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915837"
---
# <span data-ttu-id="617b0-103"><a name="NUMSEQVALUE">NUMSEQVALUE ER funkcija</a></span><span class="sxs-lookup"><span data-stu-id="617b0-103"><a name="NUMSEQVALUE">NUMSEQVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="617b0-104">`NUMSEQVALUE` funkcija grąžina *Eilutės* reikšmę, reiškiančią naują sugeneruotą numeracijos reikšmę pagal nurodytą numeraciją, aprėptį ir aprėpties ID.</span><span class="sxs-lookup"><span data-stu-id="617b0-104">The `NUMSEQVALUE` function returns a *String* value that represents the new generated value of a number sequence, based on the specified number sequence, scope, and scope ID.</span></span> <span data-ttu-id="617b0-105">Aprėpties ID yra lygus įmonės kodui pagal kontekstą, kuriame paleistas elektroninių ataskaitų (ER) formatas.</span><span class="sxs-lookup"><span data-stu-id="617b0-105">The scope ID equals the company code that is supplied by the context that the Electronic reporting (ER) format is run under.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="617b0-106">Sintaksė 1</span><span class="sxs-lookup"><span data-stu-id="617b0-106">Syntax 1</span></span>

```
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a><span data-ttu-id="617b0-107">Sintaksė 2</span><span class="sxs-lookup"><span data-stu-id="617b0-107">Syntax 2</span></span>

```
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a><span data-ttu-id="617b0-108">Sintaksė 3</span><span class="sxs-lookup"><span data-stu-id="617b0-108">Syntax 3</span></span>

```
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a><span data-ttu-id="617b0-109">Argumentai</span><span class="sxs-lookup"><span data-stu-id="617b0-109">Arguments</span></span>

<span data-ttu-id="617b0-110">`number sequence code`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="617b0-110">`number sequence code`: *String*</span></span>

<span data-ttu-id="617b0-111">Tekstinė reikšmė, reiškianti numeracijos kodą, kurio reikia naujajai reikšmei.</span><span class="sxs-lookup"><span data-stu-id="617b0-111">A text value that represents the code of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="617b0-112">`number sequence record ID`: *Int64*</span><span class="sxs-lookup"><span data-stu-id="617b0-112">`number sequence record ID`: *Int64*</span></span>

<span data-ttu-id="617b0-113">*Int64* reikšmė, nurodanti įrašo ID, kurio NumberSequenceTable lentelėje yra numeracijos apibrėžtis, kurios reikia naujajai reikšmei.</span><span class="sxs-lookup"><span data-stu-id="617b0-113">An *Int64* value that represents the record ID of a record in the NumberSequenceTable table that contains the definition of the number sequence that a new value is required in.</span></span>

<span data-ttu-id="617b0-114">`scope type`: *Išvard. reikšmė*</span><span class="sxs-lookup"><span data-stu-id="617b0-114">`scope type`: *Enum value*</span></span>

<span data-ttu-id="617b0-115">Išvardijimo **ERExpressionNumberSequenceScopeType** išvardijimo reikšmė, nurodanti numeracijos, kuriai reikia naujos reikšmės, aprėptį.</span><span class="sxs-lookup"><span data-stu-id="617b0-115">An enumeration value of the **ERExpressionNumberSequenceScopeType** enumeration that defines the scope of the number sequence that a new value is required in.</span></span> <span data-ttu-id="617b0-116">Galimi aprėpties tipai yra **Bendrasis**, **Juridinis subjektas** ir **Įmonė**.</span><span class="sxs-lookup"><span data-stu-id="617b0-116">The available scope types are **Shared**, **Legal entity**, and **Company**.</span></span>

<span data-ttu-id="617b0-117">`scope ID`: *Eilutė*</span><span class="sxs-lookup"><span data-stu-id="617b0-117">`scope ID`: *String*</span></span>

<span data-ttu-id="617b0-118">*Eilutės* reikšmė, identifikuojanti aprėptį pagal nurodytą aprėpties tipą.</span><span class="sxs-lookup"><span data-stu-id="617b0-118">A *String* value that identifies the scope, based on the specified scope type.</span></span>

## <a name="return-values"></a><span data-ttu-id="617b0-119">Grįžties vertės</span><span class="sxs-lookup"><span data-stu-id="617b0-119">Return values</span></span>

<span data-ttu-id="617b0-120">*Eilutė*</span><span class="sxs-lookup"><span data-stu-id="617b0-120">*String*</span></span>

<span data-ttu-id="617b0-121">Gaunama tekstinė reikšmė.</span><span class="sxs-lookup"><span data-stu-id="617b0-121">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="617b0-122">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="617b0-122">Usage notes</span></span>

<span data-ttu-id="617b0-123">Aprėpties tipui **Bendrasis**nurodykite tuščią eilutę kaip aprėpties ID.</span><span class="sxs-lookup"><span data-stu-id="617b0-123">For the **Shared** scope type, specify an empty string as the scope ID.</span></span>

<span data-ttu-id="617b0-124">Aprėpties tipams **Įmonė** ir **Juridinis subjektas** nurodykite įmonės kodą kaip aprėpties ID.</span><span class="sxs-lookup"><span data-stu-id="617b0-124">For the **Company** and **Legal entity** scope types, specify the company code as the scope ID.</span></span> <span data-ttu-id="617b0-125">Jei šiems aprėpties tipams nurodote tuščią eilutę kaip aprėpties ID, naudojamas dabartinės įmonės kodas.</span><span class="sxs-lookup"><span data-stu-id="617b0-125">If you specify an empty string as the scope ID for these scope types, the current company code is used.</span></span>

<span data-ttu-id="617b0-126">Naudojant sintaksę 1, reikalaujama numeracija aprėpties tipui **Įmonė**, o įmonės kodas pateikiamas pagal kontekstą, kuriuo vykdomas ER formatas.</span><span class="sxs-lookup"><span data-stu-id="617b0-126">When syntax 1 is used, the number sequence is requested for the **Company** scope type, and the company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-1"></a><span data-ttu-id="617b0-127">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="617b0-127">Example 1</span></span>

<span data-ttu-id="617b0-128">JSavo ER formatu galite nustatyti duomenų šaltinį **AskNumSeq**, kurio tipas – *Vartotojo įvesties parametras*.</span><span class="sxs-lookup"><span data-stu-id="617b0-128">In your ER format, you define the **AskNumSeq** data source of the *User input parameter* type.</span></span> <span data-ttu-id="617b0-129">Šis duomenų šaltinis nurodo išplėstąjį duomenų tipą **Aprašas**.</span><span class="sxs-lookup"><span data-stu-id="617b0-129">This data source refers to the **Description** extended data type (EDT).</span></span> <span data-ttu-id="617b0-130">Toliau, apibrėžiate tipo *Apskaičiuotasis laukas* duomenų šaltinį **NumSeq**.</span><span class="sxs-lookup"><span data-stu-id="617b0-130">Next, you define the **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="617b0-131">Šiame duomenų šaltinyje yra išraiška `NUMSEQVALUE (AskNumSeq)`.</span><span class="sxs-lookup"><span data-stu-id="617b0-131">This data source contains the expression `NUMSEQVALUE (AskNumSeq)`.</span></span> <span data-ttu-id="617b0-132">Kai duomenų šaltinis **NumSeq** yra iškviečiamas, jis grąžina naują sugeneruotą numeraciją, kuri buvo nurodyta vykdymo metu įvedant jo kodą į dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="617b0-132">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that was specified at runtime by entering its code in the dialog box.</span></span> <span data-ttu-id="617b0-133">Prašoma numeracija aprėpties tipui **Įmonė**.</span><span class="sxs-lookup"><span data-stu-id="617b0-133">The number sequence is requested for the **Company** scope type.</span></span> <span data-ttu-id="617b0-134">Įmonės kodas pateikiamas atsižvelgiant į kontekstą, pagal kurį ER formatas yra vykdomas.</span><span class="sxs-lookup"><span data-stu-id="617b0-134">The company code is supplied by the context that the ER format is run under.</span></span>

## <a name="example-2"></a><span data-ttu-id="617b0-135">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="617b0-135">Example 2</span></span>

<span data-ttu-id="617b0-136">Šie duomenų šaltiniai apibrėžti jūsų modelių susiejime:</span><span class="sxs-lookup"><span data-stu-id="617b0-136">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="617b0-137">Duomenų šaltinis**LedgerParms**, priklausantis tipui *Lentelės įrašai*.</span><span class="sxs-lookup"><span data-stu-id="617b0-137">The **LedgerParms** data source of the *Table* type.</span></span> <span data-ttu-id="617b0-138">Šis duomenų šaltinis nurodo lentelę „LedgerParameters“.</span><span class="sxs-lookup"><span data-stu-id="617b0-138">This data source refers to the LedgerParameters table.</span></span>
- <span data-ttu-id="617b0-139">Tipo *Apskaičiuotasis laukas* duomenų šaltinis **NumSeq**.</span><span class="sxs-lookup"><span data-stu-id="617b0-139">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="617b0-140">Šiame duomenų šaltinyje yra išraiška `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span><span class="sxs-lookup"><span data-stu-id="617b0-140">This data source contains the expression `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)`.</span></span>

<span data-ttu-id="617b0-141">Kai iškviečiamas duomenų šaltinis **NumSeq**, pateikiama nauja sukurta numeracijos, pagal DK parametrus sukonfigūruotos taip, kad būtų pritaikyta kontekstą, pagal kurį vykdomas ER formatas, teikiančiai įmonei, vertė.</span><span class="sxs-lookup"><span data-stu-id="617b0-141">When the **NumSeq** data source is called, it returns the new generated value of the number sequence that has been configured in the General ledger parameters for the company that supplies the context that the ER format is run under.</span></span> <span data-ttu-id="617b0-142">Ši numeracija unikaliai identifikuoja žurnalus ir naudojama kaip operacijas siejantis paketo numeris.</span><span class="sxs-lookup"><span data-stu-id="617b0-142">This number sequence uniquely identifies journals and acts as a batch number that links the transactions together.</span></span>

## <a name="example-3"></a><span data-ttu-id="617b0-143">3 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="617b0-143">Example 3</span></span>

<span data-ttu-id="617b0-144">Šie duomenų šaltiniai apibrėžti jūsų modelių susiejime:</span><span class="sxs-lookup"><span data-stu-id="617b0-144">The following data sources are defined in your model mapping:</span></span>

- <span data-ttu-id="617b0-145">Duomenų šaltinis **enumScope**, priklausantis „Microsoft Dynamics 365 Finance“ tipui *Išvardijimas*.</span><span class="sxs-lookup"><span data-stu-id="617b0-145">The **enumScope** data source of the Microsoft Dynamics 365 Finance *enumeration* type.</span></span> <span data-ttu-id="617b0-146">Šis duomenų šaltinis nurodo **ERExpressionNumberSequenceScopeType** išvardijimą.</span><span class="sxs-lookup"><span data-stu-id="617b0-146">This data source refers to the **ERExpressionNumberSequenceScopeType** enumeration.</span></span>
- <span data-ttu-id="617b0-147">Tipo *Apskaičiuotasis laukas* duomenų šaltinis **NumSeq**.</span><span class="sxs-lookup"><span data-stu-id="617b0-147">The **NumSeq** data source of the *Calculated field* type.</span></span> <span data-ttu-id="617b0-148">Šiame duomenų šaltinyje yra išraiška `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span><span class="sxs-lookup"><span data-stu-id="617b0-148">This data source contains the expression `NUMSEQVALUE ("Gene_1", enumScope.Company, "")`.</span></span>

<span data-ttu-id="617b0-149">Kai iškviečiamas duomenų šaltinis **NumSeq**, pateikiama nauja sukurta numeracijos **Gene\_1**, sukonfigūruotos taip, kad būtų pritaikyta kontekstą, pagal kurį vykdomas ER formatas, teikiančiai įmonei, vertė.</span><span class="sxs-lookup"><span data-stu-id="617b0-149">When the **NumSeq** data source is called, it returns the new generated value of the **Gene\_1** number sequence that has been configured for the company that supplies the context that the ER format is run under.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="617b0-150">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="617b0-150">Additional resources</span></span>

[<span data-ttu-id="617b0-151">Kitos (konkrečios verslo srities) funkcijos</span><span class="sxs-lookup"><span data-stu-id="617b0-151">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
