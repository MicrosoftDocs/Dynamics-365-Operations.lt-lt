---
title: Atskaytimo mokestis pardavimo perlaidose
description: Šioje temoje išvardyti žingsniai, kuriais galima išvengti išskaitymo mokesčio skaičiavimo pasirinktiems klientams. Klientams, kurie nurodo išskaitymo mokestį jų mokėjimuose jums, galite priskirti numatytą išskaitymo mokesčio grupę.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: c50f6df1c63c91107da65f463934565f786d6ccd
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060771"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="eb08d-104">Atskaytimo mokestis pardavimo perlaidose</span><span class="sxs-lookup"><span data-stu-id="eb08d-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="eb08d-105">Šioje temoje išvardyti žingsniai, kuriais galima išvengti išskaitymo mokesčio skaičiavimo pasirinktiems klientams.</span><span class="sxs-lookup"><span data-stu-id="eb08d-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="eb08d-106">Klientams, kurie nurodo išskaitymo mokestį jų mokėjimuose jums, galite priskirti numatytą numatytą **Išskaitymo mokesčio grupę** puslapyje **Klientai**.</span><span class="sxs-lookup"><span data-stu-id="eb08d-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="eb08d-107">Eikite į **Naršymo juosta > Moduliai > Gautinos sąskaitos > Klientai > Visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="eb08d-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="eb08d-108">Paspauskite atitinkamą kliento sąskaitą, spauskite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="eb08d-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="eb08d-109">Skirtuke **Sąskaita ir pristatymas** nustatykite **Skaičiuoti atskaitomą mokestį** laukelį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="eb08d-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="eb08d-110">Atskaitomas mokestis nebus skaičiuojamas, jei **Skaičiuoti atskaitomą mokestį** nėra perjungiamas klientui pagrindiniuose duomenyse.</span><span class="sxs-lookup"><span data-stu-id="eb08d-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="eb08d-111">Rinkitės atskaitomą mokesčio grupę **Mokesčių išskaitymo grupėje**.</span><span class="sxs-lookup"><span data-stu-id="eb08d-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="eb08d-112">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="eb08d-112">Click **Save**.</span></span>

<span data-ttu-id="eb08d-113">Prekėms ir paslaugoms, kurioms taikomas atskaitomas mokestis, galite priskirti numatytą **Prekės atskaitomo mokesčio grupę** **Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="eb08d-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="eb08d-114">Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="eb08d-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="eb08d-115">Paspauskite atitinkamą prekės numerį, spauskite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="eb08d-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="eb08d-116">Skirtuke **Parduoti** spauskite **Skaičiuoti atskaitomą mokestį**.</span><span class="sxs-lookup"><span data-stu-id="eb08d-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="eb08d-117">Atskaitomas mokestis nebus skaičiuojamas, jei **Skaičiuoti atskaitomą mokestį** nėra nustatomas į **Taip** šiai prekei **Parduoti** skirtuke **Išleistas produktas** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="eb08d-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="eb08d-118">Rinkitės prekės atskaitomą mokesčio grupę **Prekės atskaitymo mokesčio grupės** sąraše.</span><span class="sxs-lookup"><span data-stu-id="eb08d-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="eb08d-119">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="eb08d-119">Click **Save**.</span></span>

<span data-ttu-id="eb08d-120">Atskaitymo mokesčio grupės ir Prekės atskaitymo mokesčio grupės gali būti priskirtos naudojant **Prekybos užsakymą** puslapį.</span><span class="sxs-lookup"><span data-stu-id="eb08d-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="eb08d-121">Numatyta Atskaitomo mokesčio grupė ir prekės atskaitomo mokesčio grupė bus naudojamos kaip numatytieji objektai prekybos užsakymo eilutėse, kai kuriate naują prekybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="eb08d-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="eb08d-122">Atskaitomas mokestis yra skaičiuojamas ir publikuojamas **Kliento mokėjimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="eb08d-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="eb08d-123">Galite rankiniu būdu keisti taikomą atskaitomo mokesčio kodą, taip pat kaip realią atskaitomo mokesčio sumą **Atskaitomo mokesčio** skirtuke **Nustatytos transakcijos** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="eb08d-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="eb08d-124">Apskaičiuota atskaitoma mokesčio suma bus atskaičiuojama iš kliento mokėjimo ir publikuojama **Atskaitomo mokesčio nustatymas** sąskaita susijusiame kvite.</span><span class="sxs-lookup"><span data-stu-id="eb08d-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>
