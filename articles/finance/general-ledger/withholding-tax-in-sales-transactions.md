---
title: Atskaytimo mokestis pardavimo perlaidose
description: Šioje temoje išvardyti žingsniai, kuriais galima išvengti išskaitymo mokesčio skaičiavimo pasirinktiems klientams. Klientams, kurie nurodo išskaitymo mokestį jų mokėjimuose jums, galite priskirti numatytą išskaitymo mokesčio grupę.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8e11ce10faa9b450b6f36a856b34b06b4ee1838d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842349"
---
# <a name="withholding-tax-in-sales-transactions"></a><span data-ttu-id="1e92a-104">Atskaytimo mokestis pardavimo perlaidose</span><span class="sxs-lookup"><span data-stu-id="1e92a-104">Withholding tax in sales transactions</span></span>

<span data-ttu-id="1e92a-105">Šioje temoje išvardyti žingsniai, kuriais galima išvengti išskaitymo mokesčio skaičiavimo pasirinktiems klientams.</span><span class="sxs-lookup"><span data-stu-id="1e92a-105">This topic lists the steps for avoiding the calculation of withholding tax for selected customers.</span></span> <span data-ttu-id="1e92a-106">Klientams, kurie nurodo išskaitymo mokestį jų mokėjimuose jums, galite priskirti numatytą numatytą **Išskaitymo mokesčio grupę** puslapyje **Klientai**.</span><span class="sxs-lookup"><span data-stu-id="1e92a-106">For customers who specify withholding tax in their payments to you, you can assign the default **Withholding tax group** on the **Customers** page.</span></span> 

1. <span data-ttu-id="1e92a-107">Eikite į **Naršymo juosta > Moduliai > Gautinos sąskaitos > Klientai > Visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="1e92a-107">Go to **Navigation pane > Modules > Accounts receivable > Customers > All customers**.</span></span>

2. <span data-ttu-id="1e92a-108">Paspauskite atitinkamą kliento sąskaitą, spauskite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="1e92a-108">Click the respective customer account, click **Edit**.</span></span>

3. <span data-ttu-id="1e92a-109">Skirtuke **Sąskaita ir pristatymas** nustatykite **Skaičiuoti atskaitomą mokestį** laukelį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="1e92a-109">In the **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="1e92a-110">Atskaitomas mokestis nebus skaičiuojamas, jei **Skaičiuoti atskaitomą mokestį** nėra perjungiamas klientui pagrindiniuose duomenyse.</span><span class="sxs-lookup"><span data-stu-id="1e92a-110">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this customer in the master data.</span></span>

4. <span data-ttu-id="1e92a-111">Rinkitės atskaitomą mokesčio grupę **Mokesčių išskaitymo grupėje**.</span><span class="sxs-lookup"><span data-stu-id="1e92a-111">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="1e92a-112">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1e92a-112">Click **Save**.</span></span>

<span data-ttu-id="1e92a-113">Prekėms ir paslaugoms, kurioms taikomas atskaitomas mokestis, galite priskirti numatytą **Prekės atskaitomo mokesčio grupę** **Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="1e92a-113">For items/services, which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="1e92a-114">Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="1e92a-114">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="1e92a-115">Paspauskite atitinkamą prekės numerį, spauskite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="1e92a-115">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="1e92a-116">Skirtuke **Parduoti** spauskite **Skaičiuoti atskaitomą mokestį**.</span><span class="sxs-lookup"><span data-stu-id="1e92a-116">In the **Sell** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="1e92a-117">Atskaitomas mokestis nebus skaičiuojamas, jei **Skaičiuoti atskaitomą mokestį** nėra nustatomas į **Taip** šiai prekei **Parduoti** skirtuke **Išleistas produktas** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="1e92a-117">Withholding tax will not be calculated if **Calculate withholding tax** is not set to **Yes** for this Item in the **Sell** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="1e92a-118">Rinkitės prekės atskaitomą mokesčio grupę **Prekės atskaitymo mokesčio grupės** sąraše.</span><span class="sxs-lookup"><span data-stu-id="1e92a-118">Select an Item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="1e92a-119">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="1e92a-119">Click **Save**.</span></span>

<span data-ttu-id="1e92a-120">Atskaitymo mokesčio grupės ir Prekės atskaitymo mokesčio grupės gali būti priskirtos naudojant **Prekybos užsakymą** puslapį.</span><span class="sxs-lookup"><span data-stu-id="1e92a-120">Withholding tax groups and Item withholding tax groups can be assigned using the **Sales order** page.</span></span> 

<span data-ttu-id="1e92a-121">Numatyta Atskaitomo mokesčio grupė ir prekės atskaitomo mokesčio grupė bus naudojamos kaip numatytieji objektai prekybos užsakymo eilutėse, kai kuriate naują prekybos užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1e92a-121">The default Withholding tax group and Item withholding tax group will be used as default entries on sales order lines when you create a new sales order.</span></span>

<span data-ttu-id="1e92a-122">Atskaitomas mokestis yra skaičiuojamas ir publikuojamas **Kliento mokėjimo žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="1e92a-122">Withholding tax is calculated and posted with **Customer payment journal**.</span></span> <span data-ttu-id="1e92a-123">Galite rankiniu būdu keisti taikomą atskaitomo mokesčio kodą, taip pat kaip realią atskaitomo mokesčio sumą **Atskaitomo mokesčio** skirtuke **Nustatytos transakcijos** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="1e92a-123">You can manually adjust the applicable withholding tax code, as well as the actual withholding tax amount in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

<span data-ttu-id="1e92a-124">Apskaičiuota atskaitoma mokesčio suma bus atskaičiuojama iš kliento mokėjimo ir publikuojama **Atskaitomo mokesčio nustatymas** sąskaita susijusiame kvite.</span><span class="sxs-lookup"><span data-stu-id="1e92a-124">The calculated withholding tax amount will be deducted from the customer payment and posted to the **Withholding tax offset** account in a related voucher.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]