---
title: 'Vadovas: Poreikio prognozės modifikavimas rankiniu būdu'
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
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224015"
---
# <a name="guide-modify-a-demand-forecast-manually"></a><span data-ttu-id="6d1cc-103">Vadovas: Poreikio prognozės modifikavimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="6d1cc-103">Guide: Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6d1cc-104">Ši procedūra nurodo, kaip modifikuoti prekės prognozę.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="6d1cc-105">Ši procedūra yra skirta gamybos planuotojui.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-105">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="6d1cc-106">Pasirinktos prekės prognozės modifikavimas</span><span class="sxs-lookup"><span data-stu-id="6d1cc-106">Modify the forecast for a selected item</span></span>

<span data-ttu-id="6d1cc-107">Norėdami modifikuoti pasirinktos prekės prognozę:</span><span class="sxs-lookup"><span data-stu-id="6d1cc-107">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="6d1cc-108">Eikite į **Moduliai \> Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-108">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="6d1cc-109">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="6d1cc-110">Pasirinkite prekę, kurios prognozę norite modifikuoti.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-110">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="6d1cc-111">Veiksmų srityje atidarykite skirtuką **Planuoti** ir pasirinkite **Poreikio prognozė**.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-111">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="6d1cc-112">Iš sąrašo pasirinkite eilutę.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-112">In the list, select a row.</span></span> <span data-ttu-id="6d1cc-113">Jei nėra prognozės eilučių, sukurkite naują eilutę veiksmų srityje pasirinkę **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-113">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="6d1cc-114">Lauke **Pardavimo kiekis** įveskite teigiamą skaičių.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-114">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="6d1cc-115">Šis skaičius reprezentuoja prognozuojamą prekės kiekį.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-115">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="6d1cc-116">Jeigu įvesite neigiamą skaičių, bus rodoma klaida.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-116">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="6d1cc-117">Užpildykite kitus laukus taip, kaip reikia.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-117">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="6d1cc-118">Pasirinkite **Įrašyti** veiksmų srityje.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-118">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a><span data-ttu-id="6d1cc-119">Redaguokite prognozę vienai ar kelioms prekėms su „Microsoft Excel”</span><span class="sxs-lookup"><span data-stu-id="6d1cc-119">Modify the forecast for one or more items with Microsoft Excel</span></span>

<span data-ttu-id="6d1cc-120">Norėdami redaguoti prognozę vienai ar kelioms prekėms su „Microsoft Excel”:</span><span class="sxs-lookup"><span data-stu-id="6d1cc-120">To modify the forecast for one or more items with Microsoft Excel:</span></span>

1. <span data-ttu-id="6d1cc-121">Atlikite vieną iš toliau nurodytų veiksmų.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-121">Do one of the following:</span></span>
    - <span data-ttu-id="6d1cc-122">Atidarykite puslapį **Poreikio prognozė** bet kuriai prekei (nesvarbu kuriai), kaip aprašyta ankstesniame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-122">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="6d1cc-123">Eikite į **Bendrasis planavimas \> Prognozė \> Rankinis poreikio prognozės įrašas \> Poreikio prognozės eilutės**.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-123">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="6d1cc-124">Veiksmų srityje pasirinkite **Atidaryti „Microsoft Office” platformoje \> Poreikio prognozės įrašai**.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-124">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="6d1cc-125">Pasirinkite atsisiuntimo vietą, įrašykite ir atidarykite atsisiųstą failą „Excel” programoje.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-125">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="6d1cc-126">Jeigu matote įspėjimą, pasirinkite **Įgalinti redagavimą**.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-126">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="6d1cc-127">„Excel” programoje prisijunkite prie „Supply Chain Management” naudodami „Microsoft Dynamics” užduočių sritį.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-127">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="6d1cc-128">Turite prisijungti su įgalinta parinktimi **Palikti mane prisijungusį** ir turite pasitikėti duomenų ryšio programa.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-128">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="6d1cc-129">Dabar „Excel” skaičiuoklėje rodomos visos dabartinės jūsų įmonės poreikio prognozės eilutės.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-129">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="6d1cc-130">Pridėkite, naikinkite ir redaguoti poreikio prognozės eilutes taip, kaip reikia.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-130">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="6d1cc-131">„Microsoft Dynamics” užduočių srityje pasirinkite **Publikuoti**, kad savo keitimus vėl įkeltumėte į „Supply Chain Management”.</span><span class="sxs-lookup"><span data-stu-id="6d1cc-131">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
