---
title: ER ALLITEMS funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama modulio Elektroninės ataskaitos (ER) ALLITEMS funkcija.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 3aa226be8bc27817b4369b9e5b24faee8ea52b88
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042233"
---
# <span data-ttu-id="553ed-103"><a name="ALLITEMS">ER ALLITEMS funkcija</a></span><span class="sxs-lookup"><span data-stu-id="553ed-103"><a name="ALLITEMS">ALLITEMS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="553ed-104">`ALLITEMS` funkcija veikia kaip atminties pasirinkimas ir pateikia naują plokščia padarytą tipo *Įrašų sąrašas* reikšmę kaip įrašų sąrašą, kuris nurodo visus elementus, atitinkančius nurodytą kelią.</span><span class="sxs-lookup"><span data-stu-id="553ed-104">The `ALLITEMS` function runs as an in-memory selection and returns a new flattened *Record list* value as a list of records that represents all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="553ed-105">Sintaksė</span><span class="sxs-lookup"><span data-stu-id="553ed-105">Syntax</span></span>

```vb
ALLITEMS (path)
```

## <a name="arguments"></a><span data-ttu-id="553ed-106">Argumentai</span><span class="sxs-lookup"><span data-stu-id="553ed-106">Arguments</span></span>

<span data-ttu-id="553ed-107">`path`: *Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="553ed-107">`path`: *Record list*</span></span>

<span data-ttu-id="553ed-108">Tinkamas *Įrašų sąrašo* duomenų tipo duomenų šaltinio elemento maršrutas.</span><span class="sxs-lookup"><span data-stu-id="553ed-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="553ed-109">Pateikiamos reikšmės</span><span class="sxs-lookup"><span data-stu-id="553ed-109">Return values</span></span>

<span data-ttu-id="553ed-110">*Įrašų sąrašas*</span><span class="sxs-lookup"><span data-stu-id="553ed-110">*Record list*</span></span>

<span data-ttu-id="553ed-111">Gautas įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="553ed-111">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="553ed-112">Naudojimo pastabos</span><span class="sxs-lookup"><span data-stu-id="553ed-112">Usage notes</span></span>

<span data-ttu-id="553ed-113">Kelias turi būti nurodytas kaip tinkamas duomenų tipo *Įrašų sąrašas* duomenų šaltinio elemento kelias.</span><span class="sxs-lookup"><span data-stu-id="553ed-113">The path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="553ed-114">Duomenų elementai, pvz., kelio eilutė ir data, kūrimo metu modulio Elektroninės ataskaitos (ER) reiškinių daryklėje turėtų pateikti klaidą.</span><span class="sxs-lookup"><span data-stu-id="553ed-114">Data elements such as the path string and date should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="553ed-115">Nerekomenduojame šios funkcijos naudoti su operacijų duomenų šaltiniais, kuriuose gali būti daug duomenų.</span><span class="sxs-lookup"><span data-stu-id="553ed-115">We don't recommend that you use this function for transactional data sources that might contain a large volume of data.</span></span> <span data-ttu-id="553ed-116">Vietoj to apsvarstykite galimybę naudoti funkciją [ALLTEMSQUERY](er-functions-list-allitemsquery.md).</span><span class="sxs-lookup"><span data-stu-id="553ed-116">Instead, consider using the [ALLTEMSQUERY](er-functions-list-allitemsquery.md) function.</span></span>

## <a name="example-1"></a><span data-ttu-id="553ed-117">1 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="553ed-117">Example 1</span></span>

<span data-ttu-id="553ed-118">Jei `SPLIT("abcdef" , 2)`įvesite kaip duomenų šaltinį **DS**, reiškinys `COUNT( ALLITEMS (DS))` pateiks **3**.</span><span class="sxs-lookup"><span data-stu-id="553ed-118">If you enter `SPLIT("abcdef" , 2)` as data source **DS**, the expression `COUNT( ALLITEMS (DS))` returns **3**.</span></span>

## <a name="example-2"></a><span data-ttu-id="553ed-119">2 pavyzdys</span><span class="sxs-lookup"><span data-stu-id="553ed-119">Example 2</span></span>

<span data-ttu-id="553ed-120">Jei kaip duomenų tipo *Įrašų sąrašas* duomenų šaltinį įvedate **Vend**, nurodantį programos lentelę VendTable, reiškinys `ALLITEMS (Vend.'<Relations'.ContactPerson)` pateikia plokščiu padarytą įrašų sąrašą, turintį lentelės **ContactPerson** struktūrą ir kuriame yra visi kontaktiniai asmenys, kuriuos galima pasiekti naudojant ryšį **ContactPerson.ContactForParty == VendTable.Party**, ir kuris visiems tiekėjams pasiekiamas nurodytoje tiekėjų lentelėje.</span><span class="sxs-lookup"><span data-stu-id="553ed-120">If you enter **Vend** as the data source of the *Record list* data type that refers to the VendTable application table, the expression `ALLITEMS (Vend.'<Relations'.ContactPerson)` returns a flattened list of records that has the **ContactPerson** table structure and contains all contact persons that can be accessed by using the **ContactPerson.ContactForParty == VendTable.Party** relation, and that is available for all vendors from the referenced vendor table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="553ed-121">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="553ed-121">Additional resources</span></span>

[<span data-ttu-id="553ed-122">Sąrašo funkcijos</span><span class="sxs-lookup"><span data-stu-id="553ed-122">List functions</span></span>](er-functions-category-list.md)
