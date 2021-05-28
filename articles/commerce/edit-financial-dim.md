---
title: Mažmeninės prekybos operacijų finansinių dimensijų redagavimas
description: Šioje temoje aprašoma, kaip redaguoti mažmeninės prekybos operacijų finansines dimensijas „Microsoft Dynamics 365 Commerce“.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 381d8bb0939f6c4c163477990e49382201487375
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019912"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="3abbf-103">Mažmeninės prekybos operacijų finansinių dimensijų redagavimas</span><span class="sxs-lookup"><span data-stu-id="3abbf-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3abbf-104">Šioje temoje aprašoma, kaip redaguoti mažmeninės prekybos operacijų finansines dimensijas „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="3abbf-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="3abbf-105">Finansinių dimensijų redagavimas</span><span class="sxs-lookup"><span data-stu-id="3abbf-105">Edit financial dimensions</span></span>

<span data-ttu-id="3abbf-106">Norėdami „Commerce“ būstinėje redaguoti mažmeninės prekybos operacijų finansines dimensijas, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3abbf-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="3abbf-107">Atidarykite puslapį **Finansinių dimensijų konfigūravimas, kad būtų galima integruoti programas**.</span><span class="sxs-lookup"><span data-stu-id="3abbf-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="3abbf-108">Pasirinkite aktyvų įrašą **Numatytųjų dimensijų integravimas**.</span><span class="sxs-lookup"><span data-stu-id="3abbf-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="3abbf-109">Įsitikinkite, kad „FastTab“ **Finansinės dimensijos** visos dimensijos, kurias norite redaguoti „Excel“ darbalapyje, yra sąraše **Pasirinkta**.</span><span class="sxs-lookup"><span data-stu-id="3abbf-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="3abbf-110">Daugiau informacijos žr. skyriuje [Duomenų objektai](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).</span><span class="sxs-lookup"><span data-stu-id="3abbf-110">For more information, see [Data entities](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).</span></span>
1. <span data-ttu-id="3abbf-111">Atsisiųskite ir atidarykite „Excel“ failą iš puslapio **Išrašai**, puslapio **Mažmeninės prekybos operacijos** arba plytelės **Operacijų tikrinimo klaidos** darbo srityje **Parduotuvės finansai**.</span><span class="sxs-lookup"><span data-stu-id="3abbf-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="3abbf-112">Norėdami pakeisti operacijos finansinę dimensiją, pasirinkite **Dizainas**, tada pasirinkite pieštuko simbolį, esantį prie eilutės **Operacijos (patikrinamos)**.</span><span class="sxs-lookup"><span data-stu-id="3abbf-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="3abbf-113">Suraskite ir pasirinkite lauką **FinancialDimensionDisplayValue**, pasirinkite „Excel“ darbalapio antraštės dalyje esantį langelį ir pasirinkite **Įtraukti žymą**.</span><span class="sxs-lookup"><span data-stu-id="3abbf-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="3abbf-114">Pasirinkite langelį, esantį po langeliu, kurį pasirinkote ankstesniame veiksme, pasirinkite **Įtraukti vertę** ir tada pasirinkite **Atnaujinti**.</span><span class="sxs-lookup"><span data-stu-id="3abbf-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="3abbf-115">Finansinės dimensijos įtraukiamos į „Excel“ darbalapį ir jas galima redaguoti bei publikuoti.</span><span class="sxs-lookup"><span data-stu-id="3abbf-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="3abbf-116">Norėdami pakeisti operacijų eilučių dimensijas, pasirinkite eilutę **Pardavimo operacijos (patikrinama)**, pasirinkite pieštuko simbolį ir pakartokite 6 ir 7 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3abbf-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="3abbf-117">Norėdami pakeisti mokėjimo eilučių dimensijas, pasirinkite eilutę **Mokėjimo operacijos (patikrinama)**, pasirinkite pieštuko simbolį ir pakartokite 6 ir 7 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="3abbf-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3abbf-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="3abbf-118">Additional resources</span></span>

[<span data-ttu-id="3abbf-119">Atsiskaitymo grynaisiais ir grynųjų pinigų valdymo operacijų redagavimas ir tikrinimas</span><span class="sxs-lookup"><span data-stu-id="3abbf-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="3abbf-120">Internetinio užsakymo ir asinchroninio kliento užsakymo operacijų redagavimas ir tikrinimas</span><span class="sxs-lookup"><span data-stu-id="3abbf-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="3abbf-121">„Excel“ darbaknygės kūrimas norint redaguoti mažmeninės prekybos operacijas</span><span class="sxs-lookup"><span data-stu-id="3abbf-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="3abbf-122">Laukų įtraukimas į „Excel“ darbaknygę norint redaguoti mažmeninės prekybos operacijas</span><span class="sxs-lookup"><span data-stu-id="3abbf-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]