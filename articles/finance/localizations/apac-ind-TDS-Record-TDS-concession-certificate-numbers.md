---
title: Įrašykite TDS koncesijos sertifikato numerius
description: Šioje temoje paaiškinama, kaip įrašyti iš šaltinio (TDS) koncesijos sertifikato numerius, išduotus tiekėjams.
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
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023436"
---
# <a name="record-tds-concession-certificate-numbers"></a><span data-ttu-id="a70ee-103">Įrašykite TDS koncesijos sertifikato numerius</span><span class="sxs-lookup"><span data-stu-id="a70ee-103">Record TDS concession certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a70ee-104">Šioje temoje paaiškinama, kaip įrašyti iš šaltinio (TDS) koncesijos sertifikato numerius, išduotus tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="a70ee-104">This topic explains how to record the Tax Deducted at Source (TDS) concession certificate numbers that are issued to vendors.</span></span>

1. <span data-ttu-id="a70ee-105">Pasirinkite **Mokestis \> Netiesioginiai mokesčiai \> Išskaitomas mokestis \> Išskaitomo mokesčio leidimai**.</span><span class="sxs-lookup"><span data-stu-id="a70ee-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax concessions**.</span></span>
2. <span data-ttu-id="a70ee-106">Mokesčių **tipo lauke** pasirinkite **TDS** norėdami įrašyti TDS mokesčių tipo koncesijos sertifikatus.</span><span class="sxs-lookup"><span data-stu-id="a70ee-106">In the **Tax type** field, select **TDS** to record concession certificates for the TDS tax type.</span></span>
3. <span data-ttu-id="a70ee-107">Norėdami **Peržiūra** eilutę, skirtuke Skaičiavimas pasirinkite **Alt+N**.</span><span class="sxs-lookup"><span data-stu-id="a70ee-107">On the **Overview** tab, select **Alt+N** to create a line.</span></span>

    <span data-ttu-id="a70ee-108">[![Naujos eilutės antraštė](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span><span class="sxs-lookup"><span data-stu-id="a70ee-108">[![Header of the new line](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span></span>

4. <span data-ttu-id="a70ee-109">Lauke **Išskaitomo mokesčio kodas** pasirinkite TDS mokesčio kodą, pagal kurį išduodami tiekėjo koncesijos sertifikatai.</span><span class="sxs-lookup"><span data-stu-id="a70ee-109">In the **Withholding tax code** field, select the TDS tax code that the vendor concession certificates are issued for.</span></span> <span data-ttu-id="a70ee-110">Lauke **Išskaitomo mokesčio kodo pavadinimas** rodomas TDS mokesčio pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="a70ee-110">The **Withholding tax code name** field shows the name of the TDS tax code.</span></span>
5. <span data-ttu-id="a70ee-111">Laukuose **Pradžios data** ir **Iki** nurodykite koncesijos sertifikato, kuris naudoja TDS mokesčio kodą tiekėjo TDS apskaičiuoti koncesijos pagrindu, galiojimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="a70ee-111">In the **From date** and **To date** fields, define the period of validity for the concession certificate that uses the TDS tax code to calculate TDS for the vendor on a concessional basis.</span></span>
6. <span data-ttu-id="a70ee-112">Lauke **Failo** įveskite bet kurią pagal datą.</span><span class="sxs-lookup"><span data-stu-id="a70ee-112">In the **Remarks** field, enter any remarks.</span></span>
7. <span data-ttu-id="a70ee-113">Skyriaus **lauke** įveskite juridinio skyriaus kodą, pagal kurį naudojamas TDS koncesijos sertifikatas.</span><span class="sxs-lookup"><span data-stu-id="a70ee-113">In the **Section** field, enter the legal section code that the TDS concession certificate is availed under.</span></span>

    <span data-ttu-id="a70ee-114">Jei skyriaus kodas yra 197, vertė A atsiranda formos 26Q stulpelyje „Atskaitymo/apatinio atskaitymo priežastis", ir 27Q formos stulpelyje „Atskaitymo/mažesnio atskaitymo/brutojimo priežastis".</span><span class="sxs-lookup"><span data-stu-id="a70ee-114">If the section code is 197, the value "A" appears in both the "Reason for non-deduction/lower deduction" column in Form 26Q and the "Reason for non-deduction/lower deduction/grossing up (if any)" column in Form 27Q.</span></span> <span data-ttu-id="a70ee-115">Jei skyriaus kodas yra 197A, vertė „B" atsiranda abiejose vietose.</span><span class="sxs-lookup"><span data-stu-id="a70ee-115">If the section code is 197A, the value "B" appears in both those places.</span></span>

8. <span data-ttu-id="a70ee-116">Norėdami įrašyti **tiekėjų** TDS koncesijos sertifikato numerius, pasirinkite sertifikato „FastTab".</span><span class="sxs-lookup"><span data-stu-id="a70ee-116">Select the **Certificate** FastTab to record TDS concession certificate numbers for vendors.</span></span>
9. <span data-ttu-id="a70ee-117">Lauke **Tiekėjo sąskaita** pasirinkite tiekėjo sąskaitą, pagal kurią išduotas TDS koncesijos sertifikatas.</span><span class="sxs-lookup"><span data-stu-id="a70ee-117">In the **Vendor account** field, select the vendor account that the TDS concession certificate is issued for.</span></span>
10. <span data-ttu-id="a70ee-118">Laukuose **Pradžios data** ir **Iki** nurodykite TDS koncesijos sertifikato galiojimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="a70ee-118">In the **From date** and **To date** fields, define the period of validity for the TDS concession certificate.</span></span>

    <span data-ttu-id="a70ee-119">Koncesijos pagrindu TDS skaičiuojama pagal laikotarpį, kai tiekėjui sukuriamas sertifikatas.</span><span class="sxs-lookup"><span data-stu-id="a70ee-119">The calculation of TDS on a concessional basis is based on the period when the certificate is created for the vendor.</span></span>

11. <span data-ttu-id="a70ee-120">Lauke **Sertifikatas** įveskite TDS koncesijos sertifikato numerį.</span><span class="sxs-lookup"><span data-stu-id="a70ee-120">In the **Certificate** field, enter the TDS concession certificate number.</span></span>

    <span data-ttu-id="a70ee-121">[![Sertifikato „FastTab"](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span><span class="sxs-lookup"><span data-stu-id="a70ee-121">[![Certificate FastTab](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span></span>

12. <span data-ttu-id="a70ee-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="a70ee-122">Close the page.</span></span>
