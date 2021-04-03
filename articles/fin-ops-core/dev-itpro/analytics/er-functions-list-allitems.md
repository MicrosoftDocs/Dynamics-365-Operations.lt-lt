---
title: ER ALLITEMS funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ALLITEMS funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 1eae005a71f50a08c1ef85a7a93c3b2c407c8848
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559229"
---
# <a name="allitems-er-function"></a><span data-ttu-id="47e63-103">ER ALLITEMS funkcija</span><span class="sxs-lookup"><span data-stu-id="47e63-103">ALLITEMS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47e63-104">`ALLITEMS` funkcija veikia kaip atminties pasirinkimas ir pateikia naują plokščia padarytą tipo *Įrašų sąrašas* reikšmę kaip įrašų sąrašą, kuris nurodo visus elementus, atitinkančius nurodytą kelią.</span><span class="sxs-lookup"><span data-stu-id="47e63-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="47e63-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="47e63-105">Syntax</span></span>

```vb
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="47e63-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="47e63-106">Arguments</span></span>

<span data-ttu-id="47e63-107">`path`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="47e63-107">`path`: *Record list*</span></span>

<span data-ttu-id="47e63-108">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="47e63-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="47e63-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="47e63-109">Return values</span></span>

<span data-ttu-id="47e63-110">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="47e63-110">*Record list*</span></span>

<span data-ttu-id="47e63-111">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="47e63-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="47e63-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="47e63-112">Usage notes</span></span>

<span data-ttu-id="47e63-113">Kelias turi būti nurodytas kaip tinkamas duomenų tipo *Įrašų sąrašas* duomenų šaltinio elemento kelias.</span><span class="sxs-lookup"><span data-stu-id="47e63-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="47e63-114">Duomenų elementai, pvz., kelio eilutė ir data, kūrimo metu modulio Elektroninės ataskaitos (ER) reiškinių daryklėje turėtų pateikti klaidą.</span><span class="sxs-lookup"><span data-stu-id="47e63-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="47e63-115">Nerekomenduojame šios funkcijos naudoti su operacijų duomenų šaltiniais, kuriuose gali būti daug duomenų.</span><span class="sxs-lookup"><span data-stu-id="47e63-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="47e63-116">Vietoj to apsvarstykite galimybę naudoti funkciją [ALLTEMSQUERY](er-functions-list-allitemsquery.md).</span><span class="sxs-lookup"><span data-stu-id="47e63-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="47e63-117">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="47e63-117">Example 1</span></span>

<span data-ttu-id="47e63-118">Jei `SPLIT("abcdef" , 2)`įvesite kaip duomenų šaltinį **DS**, reiškinys `COUNT( ALLITEMS (DS))` pateiks **3**.</span><span class="sxs-lookup"><span data-stu-id="47e63-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="47e63-119">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="47e63-119">Example 2</span></span>

<span data-ttu-id="47e63-120">Jei kaip duomenų tipo *Įrašų sąrašas* duomenų šaltinį įvedate **Vend**, nurodantį programos lentelę VendTable, reiškinys `ALLITEMS (Vend.'<Relations'.ContactPerson)` pateikia plokščiu padarytą įrašų sąrašą, turintį lentelės **ContactPerson** struktūrą ir kuriame yra visi kontaktiniai asmenys, kuriuos galima pasiekti naudojant ryšį **ContactPerson.ContactForParty == VendTable.Party**, ir kuris visiems tiekėjams pasiekiamas nurodytoje tiekėjų lentelėje.</span><span class="sxs-lookup"><span data-stu-id="47e63-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47e63-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="47e63-121">Additional resources</span></span>

[<span data-ttu-id="47e63-122">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="47e63-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]