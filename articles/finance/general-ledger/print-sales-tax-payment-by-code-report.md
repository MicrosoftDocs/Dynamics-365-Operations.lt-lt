---
title: Spausdinti PVM mokėjimo pagal kodą ataskaitą
description: Šioje temoje pateikiama informacija apie parametrus ir veiksmus, kurių reikia norint išspausdinti PVM mokėjimo pagal kodą ataskaitą, pateikiamą apskaitos arba PVM kodo valiuta.
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eb3ee4a12d2d29c2769f1ae22e11dc05608b47c1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815457"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a><span data-ttu-id="b13cb-103">Spausdinti PVM mokėjimo pagal kodą ataskaitą</span><span class="sxs-lookup"><span data-stu-id="b13cb-103">Print the Sales tax payment by code report</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b13cb-104">Norėdami spausdinti **PVM mokėjimo pagal kodą** ataskaitą, eikite į **Mokestis** \> **Užklausos ir ataskaitos** \> **PVM ataskaitos** \> **PVM mokėjimas pagal kodą**.</span><span class="sxs-lookup"><span data-stu-id="b13cb-104">To print the **Sales tax payment by code** report, go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span> <span data-ttu-id="b13cb-105">Pagal numatytuosius nustatymus ataskaitos sumos generuojamos juridinio subjekto apskaitos valiuta visiems ataskaitų kodams, kurie nustatyti puslapyje **PVM ataskaitų kodai**.</span><span class="sxs-lookup"><span data-stu-id="b13cb-105">By default, report amounts are generated in the accounting currency of the legal entity for all reporting codes that are set up on the **Sales tax reporting codes** page.</span></span>

<span data-ttu-id="b13cb-106">Taip pat galite generuoti šią ataskaitą taip, kad joje nurodyta PVM kodų valiuta būtų rodomos visų ataskaitų kodų, priskirtų PVM kodams puslapyje **PVM kodai**, PVM mokėjimų sumos.</span><span class="sxs-lookup"><span data-stu-id="b13cb-106">You can also generate this report so that it shows the sales tax payment amounts in the currencies of sales tax codes for all reporting codes that are assigned to sales tax codes on the **Sales tax codes** page.</span></span>

## <a name="turn-on-the-feature"></a><span data-ttu-id="b13cb-107">Funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="b13cb-107">Turn on the feature</span></span>

<span data-ttu-id="b13cb-108">Darbo srityje **Funkcijų valdymas** įjunkite šią funkciją: **Generuoti PVM mokėjimo pagal kodą ataskaitą, pateikiamą PVM kodo valiuta**.</span><span class="sxs-lookup"><span data-stu-id="b13cb-108">In the **Feature management** workspace, turn on the following feature: **Generate the Sales tax payment by code report in the sales tax code currency**.</span></span>

## <a name="run-the-report"></a><span data-ttu-id="b13cb-109">Paleiskite ataskaitą</span><span class="sxs-lookup"><span data-stu-id="b13cb-109">Run the report</span></span>

1. <span data-ttu-id="b13cb-110">Eikite į **Mokestis** \> **Užklausos ir ataskaitos** \> **PVM ataskaitos** \> **PVM mokėjimas pagal kodą**.</span><span class="sxs-lookup"><span data-stu-id="b13cb-110">Go to **Tax** \> **Inquiries and reports** \> **Sales tax reports** \> **Sales tax payment by code**.</span></span>
2. <span data-ttu-id="b13cb-111">Lauke **Ataskaitos valiuta** pasirinkite vieną iš toliau pateiktų reikšmių.</span><span class="sxs-lookup"><span data-stu-id="b13cb-111">In the **Report currency** field, select one of the following values:</span></span>

    - <span data-ttu-id="b13cb-112">**Apskaitos valiuta** – spausdinti ataskaitos sumas apskaitos valiuta.</span><span class="sxs-lookup"><span data-stu-id="b13cb-112">**Accounting currency** – Print the report amounts in the accounting currency.</span></span>
    - <span data-ttu-id="b13cb-113">**PVM kodo valiuta** – spausdinti ataskaitos sumas PVM kodų valiuta.</span><span class="sxs-lookup"><span data-stu-id="b13cb-113">**Sales tax code currency** – Print the report amounts in the currencies of sales tax codes.</span></span>

    ![Dialogo langas PVM mokėjimas pagal kodą](media/Sales-tax-payment-by-code.png)

<span data-ttu-id="b13cb-115">Toliau pateikiamoje iliustracijoje rodomas pavyzdys, kaip generuojama ataskaita.</span><span class="sxs-lookup"><span data-stu-id="b13cb-115">The following illustration shows an example of the report that is generated.</span></span> <span data-ttu-id="b13cb-116">Ataskaita nurodo, kad ataskaitos kodas **101** pateiktas **EUR** valiuta, jei laukas **PVM valiuta** nustatytas į **EUR** PVM kodui, kuriam priskirtas ataskaitos kodas.</span><span class="sxs-lookup"><span data-stu-id="b13cb-116">The report shows that reporting code **101** has the **EUR** currency if the **Sales tax currency** field is set to **EUR** for the sales tax code that the reporting code is assigned to.</span></span>

![PVM mokėjimo pagal kodą ataskaitos pavyzdys](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]