---
title: Neteisinga lauko vertė „TaxTrans“
description: Šioje temoje pateikiama informacija apie neteisingų „TaxTrans“ laukų verčių trikčių šalinimą.
author: bijian
manager: beya
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 97f9bb24d32180f2fccb69c5a13e2aa0349c1ee4
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947678"
---
# <a name="incorrect-field-value-in-taxtrans"></a><span data-ttu-id="5c4f1-103">Neteisinga lauko vertė „TaxTrans“</span><span class="sxs-lookup"><span data-stu-id="5c4f1-103">Incorrect field value in TaxTrans</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c4f1-104">Jei TaxTrans lauko vertė neteisinga, norėdami pabandyti išspręsti problemą naudokite šios **temos** informaciją.</span><span class="sxs-lookup"><span data-stu-id="5c4f1-104">If a field value in **TaxTrans** is incorrect, use the information in this topic to try to resolve the issue.</span></span>

## <a name="overview-of-values"></a><span data-ttu-id="5c4f1-105">Verčių apžvalga</span><span class="sxs-lookup"><span data-stu-id="5c4f1-105">Overview of values</span></span>
<span data-ttu-id="5c4f1-106">Šiame sąraše parodyta,  **kaip** „TaxTrans“ **TaxUncommitted** ir **TmpTaxWorkTrans yra panašūs** duomenų rinkiniai, tačiau veikia kitaip.</span><span class="sxs-lookup"><span data-stu-id="5c4f1-106">The following list shows how **TaxTrans**, **TaxUncommitted**, and **TmpTaxWorkTrans** are similar data sets, but in work differently.</span></span>

  - <span data-ttu-id="5c4f1-107">**TaxTrans** yra galutinis užregistruotas mokesčio operacijos rezultatas, išlieka duomenų bazėje.</span><span class="sxs-lookup"><span data-stu-id="5c4f1-107">**TaxTrans** is the final posted tax transaction result persisted in the database.</span></span>
  - <span data-ttu-id="5c4f1-108">**TaxUncommitted** yra tarpinis apskaičiuotas mokesčio rezultatas, išliekamas duomenų bazėje (jei taikoma), kuri bus naudojama vėliau registruojant.</span><span class="sxs-lookup"><span data-stu-id="5c4f1-108">**TaxUncommitted** is the intermediate calculated tax result persisted in the database (if applicable), which will be used later in posting.</span></span>
  - <span data-ttu-id="5c4f1-109">**TmpTaxWorkTrans yra laikinas apskaičiuotas mokesčių rezultatas atminties lentelėje** (lentelės tipas = InMemory).</span><span class="sxs-lookup"><span data-stu-id="5c4f1-109">**TmpTaxWorkTrans** is the temporary calculated tax result in the in-memory table (Table Type = InMemory).</span></span>

<span data-ttu-id="5c4f1-110">Jei radote neteisingo TaxTrans stulpelio šakninį priežastį, taip pat radote **neteisingo** TaxUncommitted **arba** **TmpTaxWorkTrans stulpelio šakninį** priežastį.</span><span class="sxs-lookup"><span data-stu-id="5c4f1-110">If you find the root cause of an incorrect **TaxTrans** column, you've also found the root cause of an incorrect **TaxUncommitted** or **TmpTaxWorkTrans** column.</span></span> <span data-ttu-id="5c4f1-111">Taip yra todėl, kad trys stulpeliai yra nukopijuoti vienas nuo kito.</span><span class="sxs-lookup"><span data-stu-id="5c4f1-111">This is because the three columns are copied from each other.</span></span>

<span data-ttu-id="5c4f1-112">Paprastai skaičiuojant mokesčius **sugeneruojamas TmpTaxWorkTrans,** tada, jei taikoma, **sugeneruojamas TaxUncommitted**.</span><span class="sxs-lookup"><span data-stu-id="5c4f1-112">Typically, during tax calculation, **TmpTaxWorkTrans** is generated, and then, if applicable, **TaxUncommitted** is generated.</span></span> <span data-ttu-id="5c4f1-113">Registruojant mokesčius **sugeneruojamas** „TaxTrans“.</span><span class="sxs-lookup"><span data-stu-id="5c4f1-113">During tax posting, **TaxTrans** is generated.</span></span>


## <a name="add-breakpoints"></a><span data-ttu-id="5c4f1-114">Įtraukti stabdos taškus</span><span class="sxs-lookup"><span data-stu-id="5c4f1-114">Add breakpoints</span></span>
<span data-ttu-id="5c4f1-115">Norėdami įtraukti pertrūkio taškus, užbaikite tolesnius žingsnius:</span><span class="sxs-lookup"><span data-stu-id="5c4f1-115">To add breakpoints, complete the following steps:</span></span> 

1. <span data-ttu-id="5c4f1-116">Įtraukite plėtinius ir stabdos taškus *įterpimo* () *ir atnaujinimo ()* plėtinius, kaip parodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="5c4f1-116">Add extensions and breakpoints in *insert()* and *update()* in the extensions as shown below.</span></span>

     - <span data-ttu-id="5c4f1-117">**TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="5c4f1-117">**TaxTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="5c4f1-118">**TaxUncommitted**</span><span class="sxs-lookup"><span data-stu-id="5c4f1-118">**TaxUncommitted**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="5c4f1-119">**TmpTaxWorkTrans**</span><span class="sxs-lookup"><span data-stu-id="5c4f1-119">**TmpTaxWorkTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. <span data-ttu-id="5c4f1-120">Arba galite tiesiogiai pridėti stabdos taškus, kai **TaxUncommitted** neįtraukta.</span><span class="sxs-lookup"><span data-stu-id="5c4f1-120">Alternatively, you can add breakpoints directly when **TaxUncommitted** is not included.</span></span>

     - <span data-ttu-id="5c4f1-121">*TaxTrans.insert()*, *TaxTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="5c4f1-121">*TaxTrans.insert()*, *TaxTrans.update()*</span></span>
     - <span data-ttu-id="5c4f1-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="5c4f1-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span></span>

## <a name="reproduce-and-debug"></a><span data-ttu-id="5c4f1-123">Perkurti ir derinti</span><span class="sxs-lookup"><span data-stu-id="5c4f1-123">Reproduce and debug</span></span>

<span data-ttu-id="5c4f1-124">Nustačius stabdos taškus, derinant visi duomenų pastovumo pokyčiai matomi.</span><span class="sxs-lookup"><span data-stu-id="5c4f1-124">After the breakpoints are set, every data persistency change is visible during debugging.</span></span> <span data-ttu-id="5c4f1-125">Norėdami rasti neteisingo **TaxTrans**, **TaxUncommitted arba** **TmpTaxWorkTrans** stulpelio šakninį priežastį, peržiūrėkite ir atkreipkite dėmesį į šiuos elementus:</span><span class="sxs-lookup"><span data-stu-id="5c4f1-125">To find the root cause of an incorrect column of **TaxTrans**, **TaxUncommitted**, or **TmpTaxWorkTrans**, review and note the following items:</span></span>

- <span data-ttu-id="5c4f1-126">Paskutinis stabdos taškas, kuriame stulpelis teisingas.</span><span class="sxs-lookup"><span data-stu-id="5c4f1-126">The last breakpoint where the column is correct.</span></span>
- <span data-ttu-id="5c4f1-127">Pirmasis stabdos taškas, kuriame stulpelis neteisingas.</span><span class="sxs-lookup"><span data-stu-id="5c4f1-127">The first breakpoint where the column is incorrect.</span></span>
- <span data-ttu-id="5c4f1-128">Kas atsitinka tarp šių dviejų taškų.</span><span class="sxs-lookup"><span data-stu-id="5c4f1-128">What happens in between those two points.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="5c4f1-129">Nustatyti, ar yra tinkinimas</span><span class="sxs-lookup"><span data-stu-id="5c4f1-129">Determine whether customization exists</span></span>
<span data-ttu-id="5c4f1-130">Jei atlikote veiksmus ankstesniuose skyriuose, bet negalėjote išspręsti problemos, nustatykite, ar yra tinkinimas.</span><span class="sxs-lookup"><span data-stu-id="5c4f1-130">If you've completed the steps in the previous sections but have not been able to resolve the issue, determine whether customization exists.</span></span> <span data-ttu-id="5c4f1-131">Jei tinkinimo nėra, pagalbos kreipkitės į "Microsoft" palaikymo tarnybą.</span><span class="sxs-lookup"><span data-stu-id="5c4f1-131">If no customization exists, contact Microsoft Support for assistance.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

