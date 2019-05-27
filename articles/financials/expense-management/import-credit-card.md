---
title: Kredito kortelės operacijų importavimas ir tvarkymas
description: Šioje temoje paaiškinama, kaip importuoti ir tvarkyti su išlaidomis susijusias kredito kortelių operacijas. Šias operacijas galima nustatyti taip, kad jos būtų automatiškai importuojamos pasikartojančiu grafiku, arba jas galima pagal poreikį importuoti rankiniu būdu.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 9674cf495b7fdd40d8672580b9d10e9ebe626bb0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565118"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="21b8f-104">Kredito kortelės operacijų importavimas ir tvarkymas</span><span class="sxs-lookup"><span data-stu-id="21b8f-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21b8f-105">Su išlaidomis susijusias kredito kortelių operacijas galima nustatyti taip, kad jos būtų automatiškai importuojamos pasikartojančiu grafiku.</span><span class="sxs-lookup"><span data-stu-id="21b8f-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="21b8f-106">Taip pat operacijas galima pagal poreikį importuoti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="21b8f-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="21b8f-107">Kredito kortelių operacijos importuojamos naudojant duomenų objektą Kredito kortelių operacijos.</span><span class="sxs-lookup"><span data-stu-id="21b8f-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="21b8f-108">Norėdami gauti daugiau informacijos apie duomenų objektus, žr. [Duomenų objektai](../../dev-itpro/data-entities/data-entities.md).</span><span class="sxs-lookup"><span data-stu-id="21b8f-108">For more information about data entities, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="21b8f-109">Importuoti kredito kortelės operacijas</span><span class="sxs-lookup"><span data-stu-id="21b8f-109">Import credit card transactions</span></span>

1. <span data-ttu-id="21b8f-110">Puslapyje **Kredito kortelių operacijos** pasirinkite **Importuoti operacijas**.</span><span class="sxs-lookup"><span data-stu-id="21b8f-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="21b8f-111">Jei duomenų valdymo sritį atidarote pirmą kartą, kad galėtumėte tęsti, sistema turi atnaujinti duomenų objektų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="21b8f-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="21b8f-112">Lauke **Pavadinimas** įveskite unikalų importavimo užduoties pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="21b8f-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="21b8f-113">Lauke **Šaltinio duomenų formatas** pasirinkite failo, kuriame yra importuotinos kredito kortelių operacijos, formatą.</span><span class="sxs-lookup"><span data-stu-id="21b8f-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="21b8f-114">Pasirinkite **Nusiųsti**, tada raskite ir pasirinkite importuotiną failą.</span><span class="sxs-lookup"><span data-stu-id="21b8f-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="21b8f-115">Nusiuntę failą, pasirinkdami plytelės saitą **Peržiūrėti schemą**, patikrinkite kredito kortelių operacijų failo ir duomenų objekto Kredito kortelių operacijos stulpelių susiejimą.</span><span class="sxs-lookup"><span data-stu-id="21b8f-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="21b8f-116">Jei yra susiejimo klaidų arba jei susiejimą turite keisti, tai darykite skirtukuose **Susiejimo vizualizacija** arba **Susiejimo informacija**.</span><span class="sxs-lookup"><span data-stu-id="21b8f-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="21b8f-117">Norėdami kredito kortelių operacijas automatizuoti, pasirinkite **Kurti pasikartojančią duomenų užduotį**.</span><span class="sxs-lookup"><span data-stu-id="21b8f-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="21b8f-118">Tada galite nustatyti pasikartojimą, apibėžiantį, kaip dažnai kredito kortelių operacijas reikia importuoti.</span><span class="sxs-lookup"><span data-stu-id="21b8f-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="21b8f-119">Baigę pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="21b8f-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="21b8f-120">Norėdami dabar importuoti pasirinktą failą, pasirinkite **Importuoti**.</span><span class="sxs-lookup"><span data-stu-id="21b8f-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="21b8f-121">Jei importuojant įvyksta klaidų, galite peržiūrėti vykdymo žurnalą arba išdėstymo duomenis, kad matytumėte klaidas, kurias turite ištaisyti, kad padėtumėte užtikrinti sėkmingą importavimo procesą.</span><span class="sxs-lookup"><span data-stu-id="21b8f-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="21b8f-122">Jei turite importuoti daugiau nei vieną failo formatą, kiekvienam formato tipui turite sukurti atskiras importavimo užduotis.</span><span class="sxs-lookup"><span data-stu-id="21b8f-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="21b8f-123">Pakartotinis atleistų darbuotojų kredito kortelių operacijų priskyrimas</span><span class="sxs-lookup"><span data-stu-id="21b8f-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="21b8f-124">Nutraukus darbuotojo įrašą, darbuotojo „Active Directory“ domenų tarnybos (AD DS) paskyra išjungiama.</span><span class="sxs-lookup"><span data-stu-id="21b8f-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="21b8f-125">Tačiau gali būti aktyvių kredito kortelių operacijų, kurias vis dar reikia įtraukti į išlaidas ir kurias reikia kompensuoti.</span><span class="sxs-lookup"><span data-stu-id="21b8f-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="21b8f-126">Kai susietasis darbuotojas atleidžiamas, naudodami puslapį **Kredito kortelių operacijos** bet kuriai kredito kortelių operacijai galite iš naujo priskirti darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="21b8f-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="21b8f-127">Pasirinkite vieną ar kelias kredito kortelių operacijas ir pasirinkite **Iš naujo priskirti operacijas**.</span><span class="sxs-lookup"><span data-stu-id="21b8f-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="21b8f-128">Tada galite pasirinkti kitą darbuotoją, kuriam priskirsite kredito kortelių operacijas.</span><span class="sxs-lookup"><span data-stu-id="21b8f-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="21b8f-129">Iš naujo priskyrus kredito kortelių operacijas, jas galima pasirinkti įtraukti į išlaidų ataskaitą ir apmokėti įprastu išlaidų ataskaitos kompensacijos procesu.</span><span class="sxs-lookup"><span data-stu-id="21b8f-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
