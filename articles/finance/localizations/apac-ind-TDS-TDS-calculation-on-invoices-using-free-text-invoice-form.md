---
title: TDS skaičiavimas SF iš laisvos formos SF puslapio
description: Šioje temoje paaiškinama, kaip apskaičiuoti iš šaltinio (TDS) atskaičius mokesčius, naudojant laisvos formos SF puslapį.
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
ms.openlocfilehash: 7d551a8ba6ba9ca282fd9de3fa7d7c7303e394ed
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023454"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a><span data-ttu-id="0a849-103">TDS skaičiavimas SF iš laisvos formos SF puslapio</span><span class="sxs-lookup"><span data-stu-id="0a849-103">TDS calculation on invoices from the Free text invoice page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a849-104">Šioje temoje paaiškinama, kaip apskaičiuoti iš šaltinio (TDS) atskaičius mokesčius, naudojant **laisvos formos SF** puslapį.</span><span class="sxs-lookup"><span data-stu-id="0a849-104">This topic explains how to calculate Tax Deducted at Source (TDS) on invoices by using the **Free text invoice** page.</span></span>

1. <span data-ttu-id="0a849-105">Pasirinkite **Gautinos sumos \> Sąskaitos faktūros \> Visos laisvos formos SF**.</span><span class="sxs-lookup"><span data-stu-id="0a849-105">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>

    <span data-ttu-id="0a849-106">[![Laisvos formos SF puslapis](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span><span class="sxs-lookup"><span data-stu-id="0a849-106">[![Free text invoice page](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)</span></span>

2. <span data-ttu-id="0a849-107">Rinkitės **Nauja** norėdami sukurti laisvo teksto sąskaitą ir įvesti reikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="0a849-107">Select **New** to create a free text invoice, and enter the required details.</span></span>
3. <span data-ttu-id="0a849-108">Rinkitės **SF** skirtuką. Skyriuje **Išskaitomo mokesčio grupė** lauke **Vertinamo pobūdis** lauke rodomas vertinamos kliento kategorijos pobūdis.</span><span class="sxs-lookup"><span data-stu-id="0a849-108">Select the **Invoice** tab. In the **Withholding tax group** section, the **Nature of assessee** field shows the nature of assessee category of the customer.</span></span>
4. <span data-ttu-id="0a849-109">Lauke **TDS grupė** peržiūrėkite arba keiskite numatytąją TDS grupę, nurodytą tiekėjui ar klientui.</span><span class="sxs-lookup"><span data-stu-id="0a849-109">In the **TDS group** field, review or change the default TDS group that is defined for the customer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0a849-110">Jums pasirinkus vertę **TDS grupės** laukelyje, **TCS grupės** laukelis tampa nebeprieinamas.</span><span class="sxs-lookup"><span data-stu-id="0a849-110">When you select a value in the **TDS group** field, the **TCS group** field becomes unavailable.</span></span> <span data-ttu-id="0a849-111">TDS skaičiuojamas tik jei **Skaičiuoti išskaitomą mokestį** parinktis yra nustatyta į **Taip** klientui **Visi klientai** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="0a849-111">TDS is calculated only if the **Calculate withholding tax** option is set to **Yes** for the customer on the **All customers** page.</span></span>

5. <span data-ttu-id="0a849-112">Skirtuke **Mokesčių informacija** ir **Įmonės informacija** skyrius, lauke **Pavadinimas** pasirinkite įmonės pavadinimą alternatyviam adresui, kuris nustatytas įmonei.</span><span class="sxs-lookup"><span data-stu-id="0a849-112">On the **Tax information** tab, in the **Company information** section, in the **Name** field, select the company name for an alternate address that has been set up for the company.</span></span>

    <span data-ttu-id="0a849-113">**Išskaitomo mokesčio** skyriuje, laukas **Mokesčių sąskaitos numeris (TAN)** rodo pasirinktos įmonės mokesčių sąskaitos numerį (TAN).</span><span class="sxs-lookup"><span data-stu-id="0a849-113">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the tax account number (TAN) for the selected company.</span></span>

6. <span data-ttu-id="0a849-114">Skirtuke **SF eilutės** kurkite SF eilutes ir įveskite būtiną informaciją.</span><span class="sxs-lookup"><span data-stu-id="0a849-114">On the **Invoice lines** tab, create invoice lines, and enter the required details.</span></span>

    <span data-ttu-id="0a849-115">**Išskaitomų mokesčių grupės** skyriuje laukas **Mokesčių sąskaitos numeris (TAN)** rodo TAN, o **TDS grupės** lauke rodoma TDS grupė.</span><span class="sxs-lookup"><span data-stu-id="0a849-115">In the **Withholding tax group** section, the **Tax Account Number (TAN)** field shows the TAN, and the **TDS group** field shows the TDS group.</span></span>

7. <span data-ttu-id="0a849-116">Rinkitės **Išskaitomas mokestis** norėdami atverti **Laikino išskaitomo mokesčio operacijų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="0a849-116">Select **Withholding tax** to open the **Temporary withholding tax transactions** page.</span></span> <span data-ttu-id="0a849-117">Viršutinėje šio puslapio dalyje yra šie laukai:</span><span class="sxs-lookup"><span data-stu-id="0a849-117">The upper part of this page has the following fields:</span></span>

    - <span data-ttu-id="0a849-118">**Bendroji išskaitomo mokesčio suma** – bendroji TDS grupės operacijos TDS apskaičiuota suma.</span><span class="sxs-lookup"><span data-stu-id="0a849-118">**Withholding tax amount in total** – The total TDS that was calculated for the transaction for the TDS group.</span></span>
    - <span data-ttu-id="0a849-119">**Vertė** – bendrasis procentas, kuris buvo naudojamas operacijos TDS apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="0a849-119">**Value** – The total percentage that was used to calculate TDS for the transaction.</span></span> <span data-ttu-id="0a849-120">Bendrasis procentas remiasi formule, kuri nustatyta TDS mokesčių kodams, pridėtiems prie TDS grupės.</span><span class="sxs-lookup"><span data-stu-id="0a849-120">The total percentage is based on the formula that is defined for the TDS tax codes and attached to the TDS group.</span></span>
    - <span data-ttu-id="0a849-121">**Pakoreguota išskaitomo mokesčio suma visa** – bendroji koreguota TDS suma, skirta visiems TDS grupės mokesčių kodams.</span><span class="sxs-lookup"><span data-stu-id="0a849-121">**Adjusted withholding tax amount in total** – The total adjusted TDS amount for all tax codes in the TDS group.</span></span>
    - <span data-ttu-id="0a849-122">**TDS** – pasirinktas žymės langelis rodo, kad prie operacijos pridėta TDS grupė.</span><span class="sxs-lookup"><span data-stu-id="0a849-122">**TDS** – A selected checkbox indicates that a TDS group is attached to the transaction.</span></span>

    <span data-ttu-id="0a849-123">Laukeliai **Peržiūra**, **Bendra** ir **Koreguota** skirtukuose išskaitomo mokesčių operacijų puslapyje rodo apskaičiuotos TDS sumos informaciją ir pakoreguotos TDS sumos informaciją kiekvienam TDS mokesčių kodui, pridėtame prie TDS grupės.</span><span class="sxs-lookup"><span data-stu-id="0a849-123">The fields on the **Overview**, **General**, and **Adjustment** tabs show the calculated TDS amount and details of the adjusted TDS amount for each TDS tax code that is attached to the TDS group.</span></span>

8. <span data-ttu-id="0a849-124">Norėdami atidaryti **ribinės vertės** puslapį, rinkitės **Ribinė vertė** puslapį, kur galite peržiūrėti TDS mokesčio komponento, pridėto prie konkretaus TDS mokesčio kodo, vertės limitą, pasirinkite Ribinę vertę.</span><span class="sxs-lookup"><span data-stu-id="0a849-124">Select **Threshold** to open the **Threshold** page, where you can review the threshold limit that is defined for the TDS tax component that is attached to a specific TDS tax code.</span></span>
9. <span data-ttu-id="0a849-125">Pasirinkite **formulės konstruktorių,** norėdami atverti **Formulės konstruktoriaus** puslapį, kuriame galite peržiūrėti formulę nurodytą konkrečiam TDS mokesčio kodui.</span><span class="sxs-lookup"><span data-stu-id="0a849-125">Select **Formula designer** to open the **Formula designer** page, where you can review the formula that is defined for a specific TDS tax code.</span></span>
10. <span data-ttu-id="0a849-126">Registruoti laisvos formos SF.</span><span class="sxs-lookup"><span data-stu-id="0a849-126">Post the free text invoice.</span></span> <span data-ttu-id="0a849-127">TDS suma, apskaičiuota pardavimo laisvo teksto sąskaitai, užregistruojama gautinų sumų sąskaitoje, kuri nustatoma kiekvienam TDS mokesčio kodui TDS grupėje.</span><span class="sxs-lookup"><span data-stu-id="0a849-127">The TDS amount that is calculated for the free text invoice is posted to the receivable account that is defined for each TDS tax code in the TDS group.</span></span> <span data-ttu-id="0a849-128">TDS mokesčių kodų mokėtinos sumos arba gautinos sąskaitos nustatomos puslapyje **Išskaitomo mokesčio kodai**.</span><span class="sxs-lookup"><span data-stu-id="0a849-128">The receivable accounts for TDS tax codes are defined on the **Withholding tax codes** page.</span></span>
11. <span data-ttu-id="0a849-129">Rinkitės **Publikuotas išskaitomas mokestis** norėdami atverti **Išskaitomo mokesčio perlaidų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="0a849-129">Select **Posted withholding tax** to open the **Withholding tax transactions** page.</span></span> <span data-ttu-id="0a849-130">Laukelis **Vertė** – bendrasis procentas, kuris buvo naudojamas operacijos TDS apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="0a849-130">The **Value** field shows the total percentage that was used to calculate TDS for the transaction.</span></span>

    <span data-ttu-id="0a849-131">Skirtuko **Peržiūra**, **Bendra** ir **Suma** rodo apskaičiuotas pagal SF eilutes TDS sumas, apskaičiuotas SF eilutėse.</span><span class="sxs-lookup"><span data-stu-id="0a849-131">The fields on the **Overview**, **General**, and **Amount** tabs show the TDS amounts that were calculated on the invoice lines.</span></span>

12. <span data-ttu-id="0a849-132">Peržiūrėti TDS skaičiavimo informaciją apie kiekvieną TDS mokesčių kodą, pridėtą prie TDS grupės.</span><span class="sxs-lookup"><span data-stu-id="0a849-132">Review the TDS calculation information for each TDS tax code that is attached to the TDS group.</span></span>
