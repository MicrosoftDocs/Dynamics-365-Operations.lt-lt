---
title: Ilgalaikių išteklių kūrimas
description: Šioje temoje paaiškinama, kaip sukurti naują ilgalaikio turto įrašą sąrašo puslapyje Ilgalaikis turtas.
author: saraschi2
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b7d65a047251fa036242fb456725bc8cba957b9
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000248"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="0a435-103">Ilgalaikių išteklių kūrimas</span><span class="sxs-lookup"><span data-stu-id="0a435-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a435-104">Šioje temoje paaiškinama, kaip sukurti naują ilgalaikio turto įrašą sąrašo puslapyje **Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="0a435-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="0a435-105">Sistema priskiria turto numerį, pagrįstą numeracija, priskirta ilgalaikio turto grupei.</span><span class="sxs-lookup"><span data-stu-id="0a435-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="0a435-106">Jei naudojate ilgalaikio turto šabloną turto importavimo naudojant „Microsoft Excel” papildinį metu arba jei naudojate kitą importavimo užduotį, sistema automatiškai sukuria ilgalaikio turto įrašus ir padidina turto numerį.</span><span class="sxs-lookup"><span data-stu-id="0a435-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="0a435-107">Norėdami rankiniu būdu sukurti turto įrašą, atlikite toliau pateiktus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0a435-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="0a435-108">Eikite į **Naršymo sritis \> Moduliai \> Ilgalaikis turtas \> Ilgalaikis turtas \> Ilgalaikis turtas**.</span><span class="sxs-lookup"><span data-stu-id="0a435-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="0a435-109">**Veiksmų srityje** pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="0a435-109">On the **Action pane** , select **New**.</span></span>
3. <span data-ttu-id="0a435-110">Lauke **Ilgalaikio turto grupė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0a435-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="0a435-111">Laukas **Numeris** bus numatytasis, jei įjungėte **Automatiškai sunumeruotas ilgalaikio turto funkcionalumas** parinktyse **Ilgalaikio turto parametrai** ir **Ilgalaikio turto grupė**.</span><span class="sxs-lookup"><span data-stu-id="0a435-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="0a435-112">Jei neįgalinote, turite įvesti unikalų numerį, kad identifikuotumėte ilgalaikį turtą.</span><span class="sxs-lookup"><span data-stu-id="0a435-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="0a435-113">Lauke **Pavadinimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="0a435-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="0a435-114">Įveskite papildomą šio turto informaciją, kurios reikia jūsų verslui.</span><span class="sxs-lookup"><span data-stu-id="0a435-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="0a435-115">**Veiksmų srityje** pasirinkite **Knygos**.</span><span class="sxs-lookup"><span data-stu-id="0a435-115">On the **Action pane** , select **Books**.</span></span>
6. <span data-ttu-id="0a435-116">Lauke **Įsigijimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="0a435-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="0a435-117">Lauke **Įsigijimo kaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="0a435-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="0a435-118">Įveskite papildomą šios knygos informaciją, kurios reikia jūsų verslui.</span><span class="sxs-lookup"><span data-stu-id="0a435-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="0a435-119">Įveskite papildomą likusių knygų informaciją, kurios reikia jūsų verslui.</span><span class="sxs-lookup"><span data-stu-id="0a435-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="0a435-120">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="0a435-120">Close the page.</span></span>

<span data-ttu-id="0a435-121">Taip pat galite importuoti ilgalaikį turtą naudodami „Excel” papildinį arba vykdydami importavimo užduotį iš darbo srities **Duomenų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="0a435-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="0a435-122">Prieš paleisdami importavimą, įveskite reikiamų šablono laukų vertes.</span><span class="sxs-lookup"><span data-stu-id="0a435-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="0a435-123">Jei nenurodėte ilgalaikio turto numerio „Excel” papildinio šablone arba duomenų valdyme, sistema sukuria kiekvieno importuoto turto ilgalaikio turto numerį ir automatiškai padidina kiekvieno numeraciją.</span><span class="sxs-lookup"><span data-stu-id="0a435-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="0a435-124">Tačiau, jei importuojate turtą ir nurodote turto numerius šablone, sistema automatiškai **nepadidina** numeracijos.</span><span class="sxs-lookup"><span data-stu-id="0a435-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="0a435-125">Tokiu atveju administratoriui gali tekti rankiniu būdu atnaujinti numeraciją.</span><span class="sxs-lookup"><span data-stu-id="0a435-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="0a435-126">Jei nurodėte ilgalaikio turto numerį „Excel” papildinio šablone, sistema naudoja nurodytą ilgalaikio turto numerį ir padidina numeraciją.</span><span class="sxs-lookup"><span data-stu-id="0a435-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>
