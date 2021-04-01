---
title: Atskaitymo mokestis pirkimo perlaidose
description: Pardavėjams, kuriems taikomas atskaitymo mokestis, galite priskirti numatytą **Atskaitomo mokesčio grupę** puslapyje **Visi pardavėjai**.
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
ms.openlocfilehash: 06c18e6b0779539a6da7ae7afbe000c4cfc78d9e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256672"
---
# <a name="withholding-tax-in-purchase-transactions"></a><span data-ttu-id="e2643-103">Atskaitymo mokestis pirkimo perlaidose</span><span class="sxs-lookup"><span data-stu-id="e2643-103">Withholding tax in purchase transactions</span></span>

<span data-ttu-id="e2643-104">Pardavėjams, kuriems taikomas atskaitymo mokestis, galite priskirti numatytą **Atskaitomo mokesčio grupę** puslapyje **Visi pardavėjai**.</span><span class="sxs-lookup"><span data-stu-id="e2643-104">For vendors who are liable to withholding tax, you can assign the default **Withholding tax group** on the **All vendors** page.</span></span>

1. <span data-ttu-id="e2643-105">Eikite į **Naršymo juosta > Moduliai > Mokėtinos sąskaitos > Pardavėjai > Visi pardavėjai**.</span><span class="sxs-lookup"><span data-stu-id="e2643-105">Go to **Navigation pane > Modules > Accounts payable > Vendors > All vendors**.</span></span>

2. <span data-ttu-id="e2643-106">Paspauskite atitinkamą Pardavėjo sąskaitą, spauskite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="e2643-106">Click the respective Vendor account, click **Edit**.</span></span>

3. <span data-ttu-id="e2643-107">Skirtuke **Sąskaita ir pristatymas** nustatykite **Skaičiuoti atskaitomą mokestį** laukelį į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="e2643-107">In **Invoice and delivery** tab, set the **Calculate withholding tax** field to **Yes**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="e2643-108">Atskaitomas mokestis nebus skaičiuojamas, jei **Skaičiuoti atskaitomą mokestį** nėra perjungiamas pardavėjui pagrindiniuose duomenyse.</span><span class="sxs-lookup"><span data-stu-id="e2643-108">Withholding tax will not be calculated if **Calculate withholding tax** is not switched on for this vendor in the data.</span></span>

4. <span data-ttu-id="e2643-109">Rinkitės atskaitomą mokesčio grupę **Mokesčių išskaitymo grupėje**.</span><span class="sxs-lookup"><span data-stu-id="e2643-109">Select a withholding tax group in **Withholding tax group**.</span></span>

5. <span data-ttu-id="e2643-110">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e2643-110">Click **Save**.</span></span>

<span data-ttu-id="e2643-111">Prekėms ir paslaugoms, kurioms taikomas atskaitomas mokestis, galite priskirti numatytą **Prekės atskaitomo mokesčio grupę** **Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="e2643-111">For items/services which are liable to withholding tax, you can assign the default **Item withholding tax group** in **Released Products**.</span></span>

1. <span data-ttu-id="e2643-112">Eikite į **Naršymo sritis > Moduliai > Produkto informacijos valdymas > Produktai > Patvirtinti produktai**.</span><span class="sxs-lookup"><span data-stu-id="e2643-112">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>

2. <span data-ttu-id="e2643-113">Paspauskite atitinkamą prekės numerį, spauskite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="e2643-113">Click the respective Item number, click **Edit**.</span></span>

3. <span data-ttu-id="e2643-114">Skirtuke **Įsigyti** spauskite **Skaičiuoti atskaitomą mokestį**.</span><span class="sxs-lookup"><span data-stu-id="e2643-114">In **Purchase** tab, click **Calculate withholding tax**.</span></span>

   > [!NOTE] 
   > <span data-ttu-id="e2643-115">Atskaitomas mokestis nebus skaičiuojamas, jei **Skaičiuoti atskaitomą mokestį** nėra nustatomas į **Taip** šiai prekei **Pirkti** skirtuke **Išleistas produktas** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e2643-115">Withholding tax will not be calculated if **Calculate withholding tax** isn't set to **Yes** for this Item in the **Purchase** tab on the **Released product** page.</span></span>

4. <span data-ttu-id="e2643-116">Rinkitės prekę atskaitomą mokesčio grupę **Prekės atskaitymo mokesčio grupės** sąraše.</span><span class="sxs-lookup"><span data-stu-id="e2643-116">Select an item withholding tax group in **Item withholding tax group** list.</span></span>

5. <span data-ttu-id="e2643-117">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e2643-117">Click **Save**.</span></span>

<span data-ttu-id="e2643-118">Atskaitymo mokesčio grupės ir Prekės atskaitymo mokesčio grupės gali būti priskirtos puslapiuose:</span><span class="sxs-lookup"><span data-stu-id="e2643-118">Withholding tax groups and Item withholding tax groups can be assigned in pages:</span></span> 

- <span data-ttu-id="e2643-119">**Pirkimo užsakymas**</span><span class="sxs-lookup"><span data-stu-id="e2643-119">**Purchase order**</span></span>
- <span data-ttu-id="e2643-120">**Tiekėjo SF**</span><span class="sxs-lookup"><span data-stu-id="e2643-120">**Vendor invoice**</span></span>
- <span data-ttu-id="e2643-121">**SF žurnalas**</span><span class="sxs-lookup"><span data-stu-id="e2643-121">**Invoice journal**</span></span>

<span data-ttu-id="e2643-122">Numatyta Atskaitomo mokesčio grupė ir prekės atskaitomo mokesčio grupė bus perkeliama į eilutes kuriant **Pirkimo užsakymai** ir (arba) **Laukiančios pardavėjo sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="e2643-122">The default Withholding tax group and Item withholding tax group will be carried into the lines when creating **Purchase orders** and/or **Pending Vendor invoices**.</span></span> <span data-ttu-id="e2643-123">**Pardavėjo sąskaitos žurnale**, galite perjungti **Skaičiuoti atskaitomą mokestį** ir rinkitės **Prekės atskaitymo mokesčio grupę** skirtuke **Bendri** žurnale.</span><span class="sxs-lookup"><span data-stu-id="e2643-123">For **Vendor invoice journal**, you can switch on **Calculate withholding tax** and select **Item withholding tax group** in the **General** tab in the journal.</span></span>

<span data-ttu-id="e2643-124">Laikina atskaitomo mokesčio suma yra prieinama laukelyje **Pakeistas atskaitomas mokestis** skirtuke **Bendri** puslapyje **Pirkimo užsakymas**.</span><span class="sxs-lookup"><span data-stu-id="e2643-124">The temporary amount of withholding tax is available in the field **Adjusted withholding tax** of the **Totals** tab on the **Purchase order** page.</span></span>

![Atskaitomas mokestis yra įtrauktas į pardavimo užsakymą](media/withholding-tax-adjusted.png)

<span data-ttu-id="e2643-126">Atskaitomas mokestis yra skaičiuojamas **Pardavėjo mokėjimo žurnale**.</span><span class="sxs-lookup"><span data-stu-id="e2643-126">Withholding tax is calculated on **Vendor payment journal**.</span></span> <span data-ttu-id="e2643-127">Galite rankiniu būdu keisti taikomą atskaitomo mokesčio kodus, taip pat kaip realią atskaitomo mokesčio sumas **Atskaitomo mokesčio** skirtuke **Nustatytos transakcijos** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e2643-127">You can manually adjust the applicable withholding tax codes as well as the actual withholding tax amounts in the **Withholding tax** tab on the **Settle transactions** page.</span></span>

![Atskaitymą galima rankiniu būdu valdyti Nustatymų transakcijų puslapyje](media/withholding-tax-vendor-payment-tab.png)

<span data-ttu-id="e2643-129">Išvestas atskaitoma mokesčio suma bus atskaičiuojama iš pardavėjo mokėjimo ir publikuojama **Atskaitomo mokesčio sąskaitos** susijusiame kvite.</span><span class="sxs-lookup"><span data-stu-id="e2643-129">The derived withholding tax amount will be deducted from the vendor payment and posted to the **Withholding tax account** in a related voucher.</span></span>

![Atskaitomo mokesčio sąskaita rodo susijusį kvitą](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]