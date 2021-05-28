---
title: Skaičiuoti TDS SF naudojant pirkimo užsakymo formą ir pardavimo užsakymo formą
description: Šioje temoje pateikiami žurnalų iš šaltinio (TDS) išskaityamų mokesčių skaičiavimo veiksmai su įvairių rūšių sąskaitomis.
author: kailiang
ms.date: 02/12/2021
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
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023438"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a><span data-ttu-id="fdde7-103">Skaičiuoti TDS SF naudojant pirkimo užsakymo formą ir pardavimo užsakymo formą</span><span class="sxs-lookup"><span data-stu-id="fdde7-103">Calculate TDS invoices using purchase order form and sales order form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fdde7-104">Šioje temoje pateikiami veiksmai, kaip apskaičiuoti iš šaltinio (TDS) atskaičius mokesčius įvairių tipų SF, naudojant **pirkimo užsakymą**, **pirkimo žurnalą**, **bendrą užsakymą**, ir **Pardavimo užsakymą** puslapius.</span><span class="sxs-lookup"><span data-stu-id="fdde7-104">This topic lists the steps for calculating Tax Deducted at Source (TDS) on various types of invoices using the **Purchase order**, **Purchase journal**, **Blanket order**, and **Sales order** pages.</span></span>

1. <span data-ttu-id="fdde7-105">Naudodami šį puslapį sukurkite pirkimo užsakymą, pirkimo žurnalą, bendrą pirkimo užsakymą arba pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="fdde7-105">Create a purchase order, purchase journal, purchase blanket order, or a sales order using the page listed.</span></span> <span data-ttu-id="fdde7-106">Įveskite reikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="fdde7-106">Enter the required details.</span></span>

2. <span data-ttu-id="fdde7-107">Norėdami **peržiūrėti** tiekėjo arba kliento vertinimo pobūdį, pasirinkite nustatymo skirtuką.</span><span class="sxs-lookup"><span data-stu-id="fdde7-107">Select the **Setup** tab to view the nature of the assessee of the vendor or customer.</span></span> <span data-ttu-id="fdde7-108">Ši informacija pateikta **apmokestinimo pobūdžio** lauke, išskaitomo **mokesčio grupės laukų** grupėje.</span><span class="sxs-lookup"><span data-stu-id="fdde7-108">This information is listed in the **Nature of assessee** field, under the **Withholding tax group** field group.</span></span>

3. <span data-ttu-id="fdde7-109">Lauke **TDS grupė** peržiūrėkite arba modifikuokite numatytąją TDS grupę, nurodytą tiekėjui ar klientui.</span><span class="sxs-lookup"><span data-stu-id="fdde7-109">In the **TDS group** field, view or modify the default TDS group defined for the vendor or customer.</span></span>

   > [!NOTE]
   > <span data-ttu-id="fdde7-110">Lauke **TCS grupės** negalimas, kai TDS grupės lauke pasirenkate **TDS grupę**.</span><span class="sxs-lookup"><span data-stu-id="fdde7-110">The **TCS group** field isn't available when you select a TDS group in the **TDS group** field.</span></span> <span data-ttu-id="fdde7-111">TDS skaičiuojamas tik jei **Skaičiuoti išskaitomą mokestį** žymimas laukelis yra pažymėtas tiekėjui ar klientui **Visi tiekėjai** ar **Visi klientai** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="fdde7-111">TDS is calculated only if the **Calculate withholding tax** check box is selected for the vendor or customer on the **All vendors** or **All customers** page.</span></span>  

4. <span data-ttu-id="fdde7-112">Sukurkite prekės eilutes skirtuke **Eilutės** ir įveskite reikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="fdde7-112">Create item lines on the **Lines** tab and enter the required details.</span></span>

5. <span data-ttu-id="fdde7-113">Norėdami **peržiūrėti** arba pakeisti antraštės lygyje nurodytą TDS grupę, pasirinkite nustatymo skirtuką (eilutės lygis).</span><span class="sxs-lookup"><span data-stu-id="fdde7-113">Select the **Setup** tab (line-level) to view or change the TDS group defined at the header-level.</span></span> <span data-ttu-id="fdde7-114">TDS grupė rodoma **TDS grupės** lauke, kuris yra išskaitomo **mokesčio grupės laukų** grupėje.</span><span class="sxs-lookup"><span data-stu-id="fdde7-114">The TDS group is displayed in the **TDS group** field, which is under the **Withholding tax group** field group.</span></span>

6. <span data-ttu-id="fdde7-115">Pasirinkite **mokesčių informacijos** skirtuką ir rinkitės alternatyvius įmonės, nustatytos įmonės pavadinimus, kurie rodomi šiame lauke.</span><span class="sxs-lookup"><span data-stu-id="fdde7-115">Select the **Tax information** tab and select alternate addresses that are set up for the company name that's displayed in this field.</span></span> <span data-ttu-id="fdde7-116">Įmonės pavadinimas rodomas lauke **Pavadinimas**, kuris yra **įmonės informacijos** laukų grupėje.</span><span class="sxs-lookup"><span data-stu-id="fdde7-116">The company name is displayed in the **Name** field, which is under the **Company information** field group.</span></span> 

   <span data-ttu-id="fdde7-117">Pasirinktos įmonės pavadinimo TAN rodomas **mokesčių sąskaitos numerio** (**TAN**) lauke, išskaitomo **mokesčio lauko** grupėje.</span><span class="sxs-lookup"><span data-stu-id="fdde7-117">The TAN of the selected company name is displayed in the **Tax Account Number** (**TAN**) field, under the **Withholding tax** field group.</span></span> 

7. <span data-ttu-id="fdde7-118">Rinkitės **Išskaitomas mokestis** norėdami atverti **Laikino išskaitomo mokesčio operacijų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="fdde7-118">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="fdde7-119">Peržiūrėti šiuos laukus, rodomus viršutinėje laikino išskaitomo **mokesčio operacijų puslapio** srityje.</span><span class="sxs-lookup"><span data-stu-id="fdde7-119">View the following fields on the upper pane of the **Temporary withholding tax transactions** page.</span></span>

   - <span data-ttu-id="fdde7-120">**Išskaitomo** **mokesčio** **suma** **iš** **viso** - bendroji TDS grupės operacijos TDS suma.</span><span class="sxs-lookup"><span data-stu-id="fdde7-120">**Withholding** **tax** **amount** **in** **total** - The total TDS calculated for the transaction for the TDS group.</span></span>

   - <span data-ttu-id="fdde7-121">**Vertė** – bendrasis procentas, naudojamas operacijos TDS apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="fdde7-121">**Value** - The total percentage used to calculate TDS for the transaction.</span></span> <span data-ttu-id="fdde7-122">Bendrasis procentas remiasi formule, kuri nustatyta TDS mokesčių kodams, pridėtiems prie TDS grupės.</span><span class="sxs-lookup"><span data-stu-id="fdde7-122">The total percentage is based on the formula that is defined for TDS tax codes attached to the TDS group.</span></span>

   - <span data-ttu-id="fdde7-123">**Pakoreguota išskaitomo mokesčio suma visa** – bendroji koreguota TDS suma, skirta visiems TDS grupės mokesčių kodams.</span><span class="sxs-lookup"><span data-stu-id="fdde7-123">**Adjusted withholding tax amount in total** - The total adjusted TDS amount for all tax codes in the TDS group.</span></span>

   - <span data-ttu-id="fdde7-124">**TDS** – jei pasirinkta, prie operacijos pridedama TDS grupė.</span><span class="sxs-lookup"><span data-stu-id="fdde7-124">**TDS** - If selected, a TDS group is attached to the transaction.</span></span>

<span data-ttu-id="fdde7-125">Laukeliai **Peržiūra**, **Bendra**, ir **Koregavimas** laikinų išskaitomo **mokesčių operacijų puslapyje** rodo apskaičiuotą TDS sumą ir pakoreguotos TDS sumos informaciją kiekvienam TDS mokesčių kodui, pridėtame prie TDS grupės.</span><span class="sxs-lookup"><span data-stu-id="fdde7-125">The fields on the **Overview**, **General**, and **Adjustment** tabs on the **Temporary withholding tax transactions** page display the calculated TDS amount and adjusted TDS amount details for each TDS tax code attached to the TDS group.</span></span>

8. <span data-ttu-id="fdde7-126">Pasirinkite **Ribinės vertės** lauką, kad atidarytumėte **slenkstį**.</span><span class="sxs-lookup"><span data-stu-id="fdde7-126">Select **Threshold** to open the **Threshold** page.</span></span> <span data-ttu-id="fdde7-127">Peržiūrėkite šiame puslapyje nurodytą TDS mokesčio komponento, pridėto prie konkretaus TDS mokesčio kodo, ribinės vertės ir išimties ribą.</span><span class="sxs-lookup"><span data-stu-id="fdde7-127">View the threshold limit defined for the TDS tax component attached to a specific TDS tax code on this page.</span></span>

9. <span data-ttu-id="fdde7-128">Norėdami **atidaryti formulės** konstruktoriaus puslapį, pasirinkite **Formulės konstruktorius**.</span><span class="sxs-lookup"><span data-stu-id="fdde7-128">Select **Formula designer** to open the **Formula designer** page.</span></span> <span data-ttu-id="fdde7-129">Peržiūrėkite šiame puslapyje nurodytą konkretaus TDS mokesčio kodo formulę.</span><span class="sxs-lookup"><span data-stu-id="fdde7-129">View the formula that is defined for a specific TDS tax code on this page.</span></span> 

10. <span data-ttu-id="fdde7-130">Registruoti SF.</span><span class="sxs-lookup"><span data-stu-id="fdde7-130">Post the invoice.</span></span> <span data-ttu-id="fdde7-131">Pirkimo SF apskaičiuota TDS suma užregistruojama mokėtinoje sąskaitoje, o pardavimo SF apskaičiuota TDS suma užregistruojama gautinų sumų sąskaitoje, kuri nustatyta kiekvienam TDS mokesčio kodui TDS grupėje.</span><span class="sxs-lookup"><span data-stu-id="fdde7-131">The TDS amount calculated on purchase invoices is posted to the payable account and the TDS amount calculated on sales invoices is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="fdde7-132">TDS mokesčių kodų mokėtinos sumos arba gautinos sąskaitos nustatomos puslapyje **Išskaitomo mokesčio kodai**.</span><span class="sxs-lookup"><span data-stu-id="fdde7-132">The payable accounts or receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>

11. <span data-ttu-id="fdde7-133">Rinkitės **Užklausos** mygtukas **> Sąskaita > Publikuotas išskaitomas mokestis** mygtuką norėdami atverti **Išskaitomo mokesčio perlaidų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="fdde7-133">Select **Inquiry** button **> Invoice > Posted withholding tax** button to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="fdde7-134">Galite peržiūrėti **Vertė** laukelyje bendrąjį procentą, naudojamą rodyti operacijas ir TDS apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="fdde7-134">You can view the total percentage used to calculate TDS for the transaction in the **Value** field.</span></span>

<span data-ttu-id="fdde7-135">Laukeliai **Peržiūra**, **Bendra** ir **Suma** skirtukuose **Išskaitomo mokesčio operacijų** puslapyje rodo apskaičiuotos operacijos TDS informaciją.</span><span class="sxs-lookup"><span data-stu-id="fdde7-135">The fields on the **Overview**, **General**, and **Amount** tabs on the **Withholding tax transactions** page display the information of TDS calculated for the transaction.</span></span> <span data-ttu-id="fdde7-136">Peržiūrėti TDS skaičiavimo informaciją apie kiekvieną TDS mokesčių kodą, pridėtą prie TDS grupės.</span><span class="sxs-lookup"><span data-stu-id="fdde7-136">View the TDS calculation information for each TDS tax code attached to the TDS group.</span></span>
