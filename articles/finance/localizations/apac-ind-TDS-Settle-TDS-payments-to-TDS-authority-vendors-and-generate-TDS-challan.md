---
title: TDS mokėjimų TDS valdžios tiekėjams nustatymas ir TDS išdavimo generavimas
description: Šioje temoje paaiškinama, kaip sudengti iš šaltinio (TDS) mokėjimus TDS valdžios institucijų tiekėjams.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 5b77985a75d2930267cf94d6f218d53b47e6e705
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023455"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a><span data-ttu-id="9c4b2-103">TDS mokėjimų TDS valdžios tiekėjams nustatymas ir TDS išdavimo generavimas</span><span class="sxs-lookup"><span data-stu-id="9c4b2-103">Settle TDS payments to TDS authority vendors and generate TDS challan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c4b2-104">Šioje temoje paaiškinama, kaip sudengti iš šaltinio (TDS) mokėjimus TDS valdžios institucijų tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-104">This topic explains how to settle Tax Deducted at Source (TDS) payments to TDS authority vendors.</span></span>

1. <span data-ttu-id="9c4b2-105">Eikite į **Mokėtinos sumos \> Mokėjimai \> Tiekėjo mokėjimų žurnalas**.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-105">Go to **Accounts payable \> Payments \> Vendor payment journal**.</span></span>

    <span data-ttu-id="9c4b2-106">[![Tiekėjo mokėjimų žurnalo puslapis](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span><span class="sxs-lookup"><span data-stu-id="9c4b2-106">[![Vendor payment journal page](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span></span>

2. <span data-ttu-id="9c4b2-107">Puslapyje **Tiekėjo mokėjimų žurnalas** pasirinkite **Naujas,** kad sukurtumėte žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-107">On the **Vendor payment journal** page, select **New** to create a journal line.</span></span>
3. <span data-ttu-id="9c4b2-108">Lauke **Sąskaita** rinkitės TDS valdžios tiekėją, sudengsią su TDS mokėjimais.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-108">In the **Account** field, select the TDS authority vendor to settle TDS payments to.</span></span>
4. <span data-ttu-id="9c4b2-109">Rinkitės **Sudengimo operacijas** norėdami atidaryti **Sudengimo operacijų** puslapį, kur galėsite peržiūrėti TDS institucijos tiekėjo sudengtas TDS operacijas.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-109">Select **Settlement transactions** to open the **Settlement transactions** page, where you can view the settled TDS transactions for the TDS authority vendor.</span></span>

    <span data-ttu-id="9c4b2-110">Sudengimo laikotarpio sudengtos TDS operacijos parodomos tokiu būdu:</span><span class="sxs-lookup"><span data-stu-id="9c4b2-110">The settled TDS transactions for a settlement period are shown in the following way:</span></span>

    - <span data-ttu-id="9c4b2-111">TDS operacijos, kai vertinimo kategorijos pobūdis yra **Įmonė**, rodoma kaip viena operacijos eilutė.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-111">TDS transactions where the nature of assessee category is **Company** are shown as one transaction line.</span></span>
    - <span data-ttu-id="9c4b2-112">TDS operacijos, kai vertinimo kategorijos pobūdis yra **HUF**, **Firma**, **Asmenys**, **AOP**, **BOI**, **vietos valdžios institucijos** ar **Kiti**, rodomos kaip viena operacijos eilutė.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-112">TDS transactions where the nature of assessee category is **HUF**, **Firm**, **Individual**, **AOP**, **BOI**, **Local authority**, or **Others** are shown as one transaction line.</span></span>
    - <span data-ttu-id="9c4b2-113">Lauke **Suma** rodoma bendroji TDS suma, kurią reikia sumokėti TDS institucijos tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-113">The **Amount** field shows the total TDS amount that is due to be paid to the TDS authority vendor.</span></span>

5. <span data-ttu-id="9c4b2-114">Norėdami peržiūrėti **išsamią informaciją** apie kitas TDS operacijas, kurios įtrauktos į sudengimo įrašą.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-114">Select **Withholding tax transactions** to view the different TDS transactions that are included for the settlement record.</span></span> <span data-ttu-id="9c4b2-115">Šiame puslapyje galite peržiūrėti kiekvienos TDS operacijos, įtrauktos į sudengimo laikotarpio sudengimo procesą, skaidimą.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-115">You can view the split of each TDS transaction that has been included in the settlement process for the settlement period on this page.</span></span>
6. <span data-ttu-id="9c4b2-116">Skirtuke **Peržiūra** pažymėkite **Žymės** TDS operacijų langelį, norėdami sudengti TDS institucijos tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-116">On the **Overview** tab, select the **Mark** check box for the TDS transactions to settle to the TDS authority vendor.</span></span>

    <span data-ttu-id="9c4b2-117">Skirtuke **Peržiūros** rodoma ši kiekvienos atvertos TDS operacijos informacija:</span><span class="sxs-lookup"><span data-stu-id="9c4b2-117">The **Overview** tab shows the following information for each open TDS transaction:</span></span>

    - <span data-ttu-id="9c4b2-118">**Data** – TDS perlaidos data.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-118">**Date** – The TDS transaction date.</span></span>
    - <span data-ttu-id="9c4b2-119">**Kvitas** – Kvito numeris.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-119">**Voucher** – The voucher number.</span></span>
    - <span data-ttu-id="9c4b2-120">**Šaltinis** – modulis, kuriame publikuota TDS operacija.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-120">**Source** – The module that the TDS transaction is posted in.</span></span>
    - <span data-ttu-id="9c4b2-121">**Tiekėjas/klientas** – tiekėjo arba kliento kodas, iš kurio atimtas TDS.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-121">**Vendor/Customer** – The vendor or customer account number that the TDS is deducted from.</span></span>
    - <span data-ttu-id="9c4b2-122">**Atskaitymo/šalies pavadinimas** – tiekėjo arba kliento, iš kurio atimtas TDS, pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-122">**Name of deductee/party** – The name of the vendor or customer that the TDS is deducted from.</span></span>
    - <span data-ttu-id="9c4b2-123">**Vertinimo pobūdis** – vertinimo kategorijos, kuriai priklauso atskaitymas, pobūdis.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-123">**Nature of assessee** – The nature of assessee category that the deductee belongs to.</span></span>
    - <span data-ttu-id="9c4b2-124">**Suma** – Sąskaitos suma, kuriai buvo suskaičiuota TDS.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-124">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="9c4b2-125">**Mokesčio suma** – TDS mokesčio suma, apskaičiuota operacijai.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-125">**Tax amount** – The TDS amount that was calculated for the transaction.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9c4b2-126">Išvalykite **Žymę** kurios TDS operacijų, kurios neturi būti sudengtos TDS institucijos tiekėjui, žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-126">Clear the **Mark** check box for any TDS transactions that should not be settled to the TDS authority vendor.</span></span>

    <span data-ttu-id="9c4b2-127">Skirtuko **Bendra** lauke **PAN** rodomas nuolatinės išskaitomos sąskaitos numeris (PAN).</span><span class="sxs-lookup"><span data-stu-id="9c4b2-127">On the **General** tab, the **PAN** field shows the permanent account number (PAN) of the deductee.</span></span> <span data-ttu-id="9c4b2-128">Lauke **Data** rodoma TDS skaičiavimo data, o vertės lauke rodomas bendrasis procentas, kuris buvo naudojamas **vertė** skaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-128">The **Date** field shows the date of the TDS calculation, and the **Value** field shows the total percentage that was used for the TDS calculation.</span></span>

7. <span data-ttu-id="9c4b2-129">Pasirinkite **kvitą**, norėdami peržiūrėti TDS operacijos kvitų įrašus.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-129">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
8. <span data-ttu-id="9c4b2-130">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-130">Close the page.</span></span>
10. <span data-ttu-id="9c4b2-131">Rinkitės **išskaitomo mokesčio komponentų** norėdami atidaryti **Išskaitomo mokesčio komponentų** puslapį, kur galėsite peržiūrėti TDS mokesčio komponento, apskaičiuoto konkretaus TDS mokesčio kodo, TDS.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-131">Select **Withholding tax components** to open the **Withholding tax components** page, where you can view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>

    <span data-ttu-id="9c4b2-132">Skirtuko **Peržiūra** lauke **Mokesčio komponentas** TDS mokesčio komponentas, kuris buvo naudojamas operacijai.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-132">On the **Overview** tab, the **Tax component** field shows the TDS tax component that was used for the transaction.</span></span> <span data-ttu-id="9c4b2-133">Lauke **Suma** rodoma TDS suma, apskaičiuota TDS mokesčio komponentui bazine valiuta.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-133">The **Amount** field shows the TDS amount that was calculated for the TDS tax component, in the base currency.</span></span> <span data-ttu-id="9c4b2-134">Lauke **Sukaupta suma** rodoma bendroji TDS suma, apskaičiuota visų sudengtų operacijų TDS mokesčio komponentui.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-134">The **Accumulated amount** field shows the total TDS amount that was calculated for the TDS tax component for all settled transactions.</span></span>

    <span data-ttu-id="9c4b2-135">Skirtuke **Suma** skyriuje **Numatytoji valiuta** rodoma TDS suma, apskaičiuota TDS mokesčio komponentui numatytąja valiuta.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-135">On the **Amount** tab, the **Default currency** section shows the TDS amount that was calculated for the TDS tax component, in the default currency.</span></span> <span data-ttu-id="9c4b2-136">Skyriuje **Antrinė valiuta** rodoma antrinės valiutos suma.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-136">The **Secondary currency** section shows the amount in the secondary currency.</span></span>

11. <span data-ttu-id="9c4b2-137">Uždarykite **Išskaitomo mokesčio komponentų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-137">Close the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="9c4b2-138">Puslapyje **Atviros operacijos redagavimas** lauke **Suma** atkreipkite dėmesį, kad atnaujinama sudengimo laikotarpio bendroji suma, kurią reikia sudengti TDS institucijos tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-138">On the **Open transaction editing** page, in the **Amount** field, notice that the total amount to settle to the TDS authority vendor for the settlement period is updated.</span></span>
13. <span data-ttu-id="9c4b2-139">Norėdami sudengti skirtingų TDS sudengimo laikotarpių TDS operacijas TDS institucijos tiekėjui, **pažymėkite** operacijų žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-139">To settle the TDS transactions of different TDS settlement periods to the TDS authority vendor, select the **Mark** check box for the transactions.</span></span>
14. <span data-ttu-id="9c4b2-140">Uždarykite **atviros operacijos redagavimo** puslapį.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-140">Close the **Open transaction editing** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9c4b2-141">Jei pasirinktos tik kelios operacijos sudengti **Išskaitymo mokesčio operacijų** puslapyje, bendroji pasirinktų operacijų TDS suma atnaujinama puslapio **Redagavimas** lauke **Atvirų operacijų redagavimas** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-141">If only a few transactions are selected for settlement on the **Withholding tax transactions** page, the total TDS amount of the selected transactions is updated in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="9c4b2-142">Koregavimo suma atnaujinama žurnalo eilutėje, kuri yra **žurnalo kvito** puslapyje, ir **atidarytos operacijos redagavimo** puslapis yra uždarytas.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-142">The correction amount is updated on the journal line on the **Journal voucher** page, and the **Open transaction editing** page is closed.</span></span>

    <span data-ttu-id="9c4b2-143">**Žurnalo kvito** puslapyje, **debeto** lauke rodoma bendroji suma, kurią reikia sumokėti TDS valdžios institucijos tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-143">On the **Journal voucher** page, the **Debit** field shows the total amount to pay to the TDS authority vendor.</span></span>

15. <span data-ttu-id="9c4b2-144">Įvesti korespondentinės sąskaitos informaciją.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-144">Enter the offset account details.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9c4b2-145">Jei TDS operacijos turi skirtingus mokesčių sąskaitų numerius (TAN), žurnalo eilutės kiekvienam TAN sukuriamos **žurnalo kvito** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-145">If TDS transactions have different Tax Account Numbers (TANs), journal lines are created per TAN on the **Journal voucher** page.</span></span>

16. <span data-ttu-id="9c4b2-146">Skirtuke **Mokėjimo mokestis** lauke **Mokesčio ID** rinkitės ID mokestį, kurio mokesčio tipas **Palūkanos** ar **Kitas** norėdami apmokestinti mokėjimo mokestį už atidėtus mokėjimus, kurie atlikti TDS valdžios tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-146">On the **Payment fee** tab, in the **Fee ID** field, select a fee ID that has a fee type of **Interest** or **Others** to charge the payment fee for delayed payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="9c4b2-147">Skirtuko **Mokesčių informacijos**, esančio **Įmonės informacija** skyriuje **pavadinimas** yra rodomas įmonės pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-147">On the **Tax information** tab, in the **Company information** section, the **Name** field shows the company name.</span></span> <span data-ttu-id="9c4b2-148">**Išskaitomo mokesčio** skyriuje, mokesčių **sąskaitos numerio (TAN)** laukas rodo TAN, kuris pridėtas prie operacijos eilutės.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-148">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the TAN that is attached to the transaction line.</span></span>

17. <span data-ttu-id="9c4b2-149">Patikrinkite ir užregistruokite žurnalą.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-149">Validate and post the journal.</span></span>
18. <span data-ttu-id="9c4b2-150">Norėdami **įvesti operacijos \> išskaitomo mokesčio** išskaitomo mokesčio informaciją, pasirinkite Išskaitomo mokesčio informaciją.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-150">Select **Withholding tax \> Challan information** to enter the challan details for the transaction.</span></span>

    <span data-ttu-id="9c4b2-151">**Kvitas** – laukelis, kuriame rodomas operacijos kvito numeris.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-151">The **Voucher** field shows the voucher number of the transaction.</span></span>
    
19. <span data-ttu-id="9c4b2-152">Pažymėkite **TDS, deponuotais pagal knygos įrašą** žymės langelį, jei TDS suma yra pervesti naudojant knygos įrašą.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-152">Select the **TDS deposited by book entry** check box if the TDS amount is deposited by using book entry.</span></span>
20. <span data-ttu-id="9c4b2-153">Lauke TDS numeris įveskite **šanalų numerį** naudojamą mokėjimui TDS institucijos tiekėjui atlikti.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-153">In the **Challan number** field, enter the challan number that is used to make the payment to the TDS authority vendor.</span></span>
21. <span data-ttu-id="9c4b2-154">Lauke **Datos** įveskite šalano datą.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-154">In the **Date** field, enter the challan date.</span></span>
22. <span data-ttu-id="9c4b2-155">Lauke **Banko pavadinimas** pasirinkite banko pavadinimą, į kurį TDS suma, mokėtina TDS institucijos tiekėjui, turėtų būti pervesti į depozitą.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-155">In the **Bank name** field, select the name of the bank that the TDS amount that is payable to the TDS authority vendor should be deposited to.</span></span> <span data-ttu-id="9c4b2-156">Šiame lauke pateikiamos visos banko sąskaitos, nustatytos TDS valdžios tiekėjui mokėtinomis su **mokėtinomis sąskaitomis \> Visi tiekėjai \> Nustatyti \> banko sąskaitos**.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-156">This field lists all the bank accounts that were set up for the TDS authority vendor at **Accounts payable \> All vendors \> Set up \> Bank accounts**.</span></span>
23. <span data-ttu-id="9c4b2-157">Lauke **BSR kodas** įveskite banko pagrindinį statistinės grąžinimo (BSR) kodą.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-157">In the **BSR code** field, enter the Basic Statistical Return (BSR) code of the bank.</span></span>
24. <span data-ttu-id="9c4b2-158">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-158">Close the page.</span></span>

### <a name="example"></a><span data-ttu-id="9c4b2-159">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="9c4b2-159">Example</span></span>

<span data-ttu-id="9c4b2-160">Laikotarpis 2009 04 01 sudengtas **nuomos** TDS komponentų grupei naudojant periodinį TDS sudengimo procesą.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-160">The period 04/01/2009 is settled for the **Rent** TDS component group by using the periodic TDS settlement process.</span></span> <span data-ttu-id="9c4b2-161">Bendroji TDS suma, 141 625,00 TDS sudengimo laikotarpio TDS tiekėjo institucijos sąskaitoje.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-161">The total TDS amount of 141,625.00 is posted to the TDS vendor authority account for the TDS settlement period.</span></span> <span data-ttu-id="9c4b2-162">Šią **sumą** galite peržiūrėti TDS institucijos tiekėjo **atvirų operacijų redagavimo** puslapio lauke Suma.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-162">You can view this amount in the **Amount** field on the **Open transaction editing** page for the TDS authority vendor.</span></span>

<span data-ttu-id="9c4b2-163">Jei pasirenkate **Išskaitomo mokesčio operacijas** norėdami peržiūrėti skirtingas to laikotarpio TDS operacijas, rodoma ši informacija.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-163">If you select **Withholding tax transactions** to view the different TDS transactions that were settled for the period, the following information is shown.</span></span>

| <span data-ttu-id="9c4b2-164">TDS suma</span><span class="sxs-lookup"><span data-stu-id="9c4b2-164">TDS amount</span></span> |
|------------|
| <span data-ttu-id="9c4b2-165">16,995.00</span><span class="sxs-lookup"><span data-stu-id="9c4b2-165">16,995.00</span></span>  |
| <span data-ttu-id="9c4b2-166">22,660.00</span><span class="sxs-lookup"><span data-stu-id="9c4b2-166">22,660.00</span></span>  |
| <span data-ttu-id="9c4b2-167">28,325.00</span><span class="sxs-lookup"><span data-stu-id="9c4b2-167">28,325.00</span></span>  |
| <span data-ttu-id="9c4b2-168">16,995.00</span><span class="sxs-lookup"><span data-stu-id="9c4b2-168">16,995.00</span></span>  |
| <span data-ttu-id="9c4b2-169">28,325.00</span><span class="sxs-lookup"><span data-stu-id="9c4b2-169">28,325.00</span></span>  |
| <span data-ttu-id="9c4b2-170">16,995.00</span><span class="sxs-lookup"><span data-stu-id="9c4b2-170">16,995.00</span></span>  |
| <span data-ttu-id="9c4b2-171">11,330.00</span><span class="sxs-lookup"><span data-stu-id="9c4b2-171">11,330.00</span></span>  |

<span data-ttu-id="9c4b2-172">Norėdami peržiūrėti konkrečią pasirinktą TDS sumą, apskaičiuotą pagal konkretaus TDS mokesčio kodo TDS mokesčio komponentą, pasirinkite **išskaitomo mokesčio komponentus**.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-172">For a specific TDS amount, you can select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span> <span data-ttu-id="9c4b2-173">Kaip pavyzdį, TDS sumos pasirenkate **išskaitomo mokesčio komponentus** , 16995,00.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-173">For this example, you select **Withholding tax components** for the TDS amount 16,995.00.</span></span> <span data-ttu-id="9c4b2-174">Rodoma mokesčio suma, apskaičiuota kiekvienam operacijos komponentui.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-174">The tax amount that was calculated per component for the transaction is shown.</span></span>

| <span data-ttu-id="9c4b2-175">Mokesčių komponentas</span><span class="sxs-lookup"><span data-stu-id="9c4b2-175">Tax component</span></span> | <span data-ttu-id="9c4b2-176">Suma</span><span class="sxs-lookup"><span data-stu-id="9c4b2-176">Amount</span></span>    | <span data-ttu-id="9c4b2-177">Sukaupta suma</span><span class="sxs-lookup"><span data-stu-id="9c4b2-177">Accumulated amount</span></span> |
|---------------|-----------|--------------------|
| <span data-ttu-id="9c4b2-178">TDS</span><span class="sxs-lookup"><span data-stu-id="9c4b2-178">TDS</span></span>           | <span data-ttu-id="9c4b2-179">1,5000.00</span><span class="sxs-lookup"><span data-stu-id="9c4b2-179">1,5000.00</span></span> | <span data-ttu-id="9c4b2-180">125,000.00</span><span class="sxs-lookup"><span data-stu-id="9c4b2-180">125,000.00</span></span>         |
| <span data-ttu-id="9c4b2-181">Papildomos išlaidos</span><span class="sxs-lookup"><span data-stu-id="9c4b2-181">Surcharge</span></span>     | <span data-ttu-id="9c4b2-182">1,500.00</span><span class="sxs-lookup"><span data-stu-id="9c4b2-182">1,500.00</span></span>  | <span data-ttu-id="9c4b2-183">12,500.00</span><span class="sxs-lookup"><span data-stu-id="9c4b2-183">12,500.00</span></span>          |
| <span data-ttu-id="9c4b2-184">PE įrašai</span><span class="sxs-lookup"><span data-stu-id="9c4b2-184">PE-Cess</span></span>       | <span data-ttu-id="9c4b2-185">330.00</span><span class="sxs-lookup"><span data-stu-id="9c4b2-185">330.00</span></span>    | <span data-ttu-id="9c4b2-186">2,750.00</span><span class="sxs-lookup"><span data-stu-id="9c4b2-186">2,750.00</span></span>           |
| <span data-ttu-id="9c4b2-187">SHE Įrašai</span><span class="sxs-lookup"><span data-stu-id="9c4b2-187">SHE Cess</span></span>      | <span data-ttu-id="9c4b2-188">165.00</span><span class="sxs-lookup"><span data-stu-id="9c4b2-188">165.00</span></span>    | <span data-ttu-id="9c4b2-189">1,375.00</span><span class="sxs-lookup"><span data-stu-id="9c4b2-189">1,375.00</span></span>           |

<span data-ttu-id="9c4b2-190">Jei pasirinkote tik TDS sumas, 16995,00, 22660,00, 28325,00 sudengti **išskaitomo mokesčio operacijų** puslapyje, bendra sudengimo suma rodoma kaip **67 980,00** lauke **Taisymai** puslapyje **Atidaryti operacijos redagavimo** puslapį.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-190">If you selected only the TDS amounts 16,995.00, 22,660.00, and 2,8325.00 for settlement on the **Withholding tax transactions** page, the total amount for settlement is shown as **67,980.00** in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="9c4b2-191">Jeigu ši operacija pažymėta sudengti ir uždarytas **atvirų operacijų redagavimo** puslapis, suma **67 980,00** rodoma **Debeto** lauke **žurnalo kvito** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-191">If this transaction is marked for settlement, and the **Open transaction editing** page is closed, the amount **67,980.00** is shown in the **Debit** field on the **Journal voucher** page.</span></span>

<span data-ttu-id="9c4b2-192">Dabar galite registruoti žurnalą ir generuoti TDS ištas.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-192">You can now post the journal and generate the TDS challan.</span></span>

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a><span data-ttu-id="9c4b2-193">TDS valdžios tiekėjų išankstinių mokėjimų koregavimas</span><span class="sxs-lookup"><span data-stu-id="9c4b2-193">Adjustment of advance payments that are made to TDS authority vendors</span></span>

<span data-ttu-id="9c4b2-194">Norėdami koreguoti išankstinį mokėjimą, kuris buvo atliktas TDS valdžios institucijos tiekėjui kaip faktinis mokėjimas, eikite į **mokėtinos sumos \> Tiekėjai \> Visi tiekėjai \> Operacijų redagavimas**</span><span class="sxs-lookup"><span data-stu-id="9c4b2-194">To adjust an advance payment that was made to the TDS authority vendor to an actual payment, go to **Accounts payable \> Vendors \> All vendors \> Transactions editing**.</span></span> <span data-ttu-id="9c4b2-195">Jei faktinis atliktas mokėjimas viršija išankstinį mokėjimą, operacijai sugeneruojami du išankstinti numeriai.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-195">If the actual payment that is made exceeds the advance payment, two challan numbers are generated for the transaction.</span></span> <span data-ttu-id="9c4b2-196">Tačiau TDS užklausoje rodomas tik pirmasis iškleidimas.</span><span class="sxs-lookup"><span data-stu-id="9c4b2-196">However, only the first challan number is shown in the TDS inquiry.</span></span>
