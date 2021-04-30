---
title: Poreikio prognozės modifikavimas rankiniu būdu
description: Šioje temoje aprašoma, kaip modifikuoti prekės prognozę
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889029"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="d16b8-103">Poreikio prognozės modifikavimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="d16b8-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d16b8-104">Ši procedūra nurodo, kaip modifikuoti prekės prognozę.</span><span class="sxs-lookup"><span data-stu-id="d16b8-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="d16b8-105">Kuriant šią procedūrą naudojama demonstracinių duomenų įmonė yra USMF.</span><span class="sxs-lookup"><span data-stu-id="d16b8-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d16b8-106">Ši procedūra yra skirta gamybos planuotojui.</span><span class="sxs-lookup"><span data-stu-id="d16b8-106">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="d16b8-107">Pasirinktos prekės prognozės modifikavimas</span><span class="sxs-lookup"><span data-stu-id="d16b8-107">Modify the forecast for a selected item</span></span>

<span data-ttu-id="d16b8-108">Norėdami modifikuoti pasirinktos prekės prognozę:</span><span class="sxs-lookup"><span data-stu-id="d16b8-108">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="d16b8-109">Eikite į **Moduliai \> Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="d16b8-109">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="d16b8-110">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="d16b8-110">In the list, find and select the desired record.</span></span> <span data-ttu-id="d16b8-111">Pasirinkite prekę, kurios prognozę norite modifikuoti.</span><span class="sxs-lookup"><span data-stu-id="d16b8-111">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="d16b8-112">Veiksmų srityje atidarykite skirtuką **Planuoti** ir pasirinkite **Poreikio prognozė**.</span><span class="sxs-lookup"><span data-stu-id="d16b8-112">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="d16b8-113">Iš sąrašo pasirinkite eilutę.</span><span class="sxs-lookup"><span data-stu-id="d16b8-113">In the list, select a row.</span></span> <span data-ttu-id="d16b8-114">Jei nėra prognozės eilučių, sukurkite naują eilutę veiksmų srityje pasirinkę **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="d16b8-114">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="d16b8-115">Lauke **Pardavimo kiekis** įveskite teigiamą skaičių.</span><span class="sxs-lookup"><span data-stu-id="d16b8-115">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="d16b8-116">Šis skaičius reprezentuoja prognozuojamą prekės kiekį.</span><span class="sxs-lookup"><span data-stu-id="d16b8-116">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="d16b8-117">Jeigu įvesite neigiamą skaičių, bus rodoma klaida.</span><span class="sxs-lookup"><span data-stu-id="d16b8-117">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="d16b8-118">Užpildykite kitus laukus taip, kaip reikia.</span><span class="sxs-lookup"><span data-stu-id="d16b8-118">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="d16b8-119">Pasirinkite **Įrašyti** veiksmų srityje.</span><span class="sxs-lookup"><span data-stu-id="d16b8-119">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a><span data-ttu-id="d16b8-120">Vieno ar daugiau „Microsoft Excel” elemento prognozės modifikavimas</span><span class="sxs-lookup"><span data-stu-id="d16b8-120">Modify the forecast for one or more items Microsoft Excel</span></span>

<span data-ttu-id="d16b8-121">Norėdami modifikuoti vieno ar daugiau „Microsoft Excel” elementų prognozę:</span><span class="sxs-lookup"><span data-stu-id="d16b8-121">To modify the forecast for one or more items Microsoft Excel:</span></span>

1. <span data-ttu-id="d16b8-122">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="d16b8-122">Do one of the following:</span></span>
    - <span data-ttu-id="d16b8-123">Atidarykite puslapį **Poreikio prognozė** bet kuriai prekei (nesvarbu kuriai), kaip aprašyta ankstesniame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="d16b8-123">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="d16b8-124">Eikite į **Bendrasis planavimas \> Prognozė \> Rankinis poreikio prognozės įrašas \> Poreikio prognozės eilutės**.</span><span class="sxs-lookup"><span data-stu-id="d16b8-124">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="d16b8-125">Veiksmų srityje pasirinkite **Atidaryti „Microsoft Office” platformoje \> Poreikio prognozės įrašai**.</span><span class="sxs-lookup"><span data-stu-id="d16b8-125">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="d16b8-126">Pasirinkite atsisiuntimo vietą, įrašykite ir atidarykite atsisiųstą failą „Excel” programoje.</span><span class="sxs-lookup"><span data-stu-id="d16b8-126">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="d16b8-127">Jeigu matote įspėjimą, pasirinkite **Įgalinti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="d16b8-127">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="d16b8-128">„Excel” programoje prisijunkite prie „Supply Chain Management” naudodami „Microsoft Dynamics” užduočių sritį.</span><span class="sxs-lookup"><span data-stu-id="d16b8-128">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="d16b8-129">Turite prisijungti su įgalinta parinktimi **Palikti mane prisijungusį** ir turite pasitikėti duomenų ryšio programa.</span><span class="sxs-lookup"><span data-stu-id="d16b8-129">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="d16b8-130">Dabar „Excel” skaičiuoklėje rodomos visos dabartinės jūsų įmonės poreikio prognozės eilutės.</span><span class="sxs-lookup"><span data-stu-id="d16b8-130">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="d16b8-131">Pridėkite, naikinkite ir redaguoti poreikio prognozės eilutes taip, kaip reikia.</span><span class="sxs-lookup"><span data-stu-id="d16b8-131">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="d16b8-132">„Microsoft Dynamics” užduočių srityje pasirinkite **Publikuoti**, kad savo keitimus vėl įkeltumėte į „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="d16b8-132">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
