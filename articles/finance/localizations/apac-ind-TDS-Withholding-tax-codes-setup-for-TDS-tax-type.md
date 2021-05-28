---
title: Nustatykite išskaitomo mokesčio kodus TDS mokesčių tipui
description: Šioje temoje paaiškinama, kaip nustatyti (TDS) išskaitomo periodinio mokesčio kodus.
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
ms.openlocfilehash: d56a23f7af7633e1761a8a7c48f71381d6f14df2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023460"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a><span data-ttu-id="8c236-103">Nustatykite išskaitomo mokesčio kodus TDS mokesčių tipui</span><span class="sxs-lookup"><span data-stu-id="8c236-103">Set up withholding tax codes for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c236-104">Šioje temoje paaiškinama, kaip nustatyti (TDS) išskaitomo periodinio mokesčio kodus.</span><span class="sxs-lookup"><span data-stu-id="8c236-104">This topic explains how to set up tax codes for Tax Deducted at Source (TDS).</span></span>

1. <span data-ttu-id="8c236-105">Eikite į **Mokestis \> Netiesioginiai mokesčiai \> Išskaitomas mokestis \> Išskaitomo mokesčio kodai**.</span><span class="sxs-lookup"><span data-stu-id="8c236-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax codes**.</span></span>

    <span data-ttu-id="8c236-106">[![Išskaitomų mokesčių kodų puslapis](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span><span class="sxs-lookup"><span data-stu-id="8c236-106">[![Withholding tax codes page](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)</span></span>

2. <span data-ttu-id="8c236-107">Norėdami sukurti **TDS** išskaitomo mokesčio kodą, veiksmų srityje pasirinkite Naujas ir įveskite reikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="8c236-107">On the Action Pane, select **New** to create a withholding tax code for TDS, and enter the required details.</span></span>
3. <span data-ttu-id="8c236-108">Norėdami mokesčių kodą klasifikuoti kaip TDS mokesčio kodą, skirtuko **Bendra** „FastTab" **mokesčio tipo** lauke pasirinkite **TDS**.</span><span class="sxs-lookup"><span data-stu-id="8c236-108">On the **General** FastTab, in the **Tax type** field, select **TDS** to categorize the tax code as a TDS tax code.</span></span>
4. <span data-ttu-id="8c236-109">Į lauką **Sudengimo laikotarpis** rinkitės TDS sudengimo laikotarpį TDS mokesčių kodui.</span><span class="sxs-lookup"><span data-stu-id="8c236-109">In the **Settlement period** field, select the TDS settlement period for the TDS tax code.</span></span>
5. <span data-ttu-id="8c236-110">Lauke **Pagrindinė sąskaita** pasirinkite DK sąskaitą, į kurią turėtų būti registruojama TDS suma.</span><span class="sxs-lookup"><span data-stu-id="8c236-110">In the **Main account** field, select the ledger account that the TDS amount should be posted to.</span></span>
6. <span data-ttu-id="8c236-111">Gautinų **sumų sąskaitos** lauke pasirinkite gautinų sumų sąskaitą, į kurią turėtų būti registruojama TDS suma, atskaityta pardavimo operacijose.</span><span class="sxs-lookup"><span data-stu-id="8c236-111">In the **Receivable account** field, select the receivable account that the TDS amount that is deducted in sales transactions should be posted to.</span></span>

    <span data-ttu-id="8c236-112">Laukas **Šaltinis** automatiškai nustatomas į **Bendros sumos procentas**, todėl vertės keisti negalima.</span><span class="sxs-lookup"><span data-stu-id="8c236-112">The **Origin** field is automatically set to **Percentage of gross amount**, and the value can't be changed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8c236-113">TDS mokesčio tipo mokesčių kodų kilmės negalima nustatyti kaip **Grynosios sumos procentinė** išraiška.</span><span class="sxs-lookup"><span data-stu-id="8c236-113">You can't set the origin to **Percentage of net amount** for tax codes of the TDS tax type.</span></span>

7. <span data-ttu-id="8c236-114">Lauke **Išskaitomo mokesčio komponentas** pasirinkite TDS mokesčio komponentą TDS mokesčių kodui.</span><span class="sxs-lookup"><span data-stu-id="8c236-114">In the **Withholding tax component** field, select the TDS tax component for the TDS tax code.</span></span>
8. <span data-ttu-id="8c236-115">Veiksmų juostoje rinkitės **Vertės** norėdami atidaryti **Išskaitomo mokesčio vertės** puslapį.</span><span class="sxs-lookup"><span data-stu-id="8c236-115">On the Action Pane, select **Values** to open the **Withholding tax values** page.</span></span>
9. <span data-ttu-id="8c236-116">Lauke **Pradžios data** įveskite TDS vertės pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="8c236-116">In the **From date** field, enter the start date for the TDS value.</span></span> <span data-ttu-id="8c236-117">Lauke **Iki datos** įveskite pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="8c236-117">In the **To date** field, enter the end date.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8c236-118">Laukeliai **minimali riba**, **Viršutinė riba** ir **Neįtraukti %** laukeliai nėra prieinami mokesčių TDS mokesčio tipo kodams.</span><span class="sxs-lookup"><span data-stu-id="8c236-118">The **Minimum limit**, **Upper limit**, and **Exclude %** fields aren't available for tax codes of the TDS tax type.</span></span>

10. <span data-ttu-id="8c236-119">Lauke **Reikšmė** įveskite procentinę TDS dalį TDS mokesčių kodui.</span><span class="sxs-lookup"><span data-stu-id="8c236-119">In the **Value** field, enter the percentage of TDS for the TDS tax code.</span></span>
11. <span data-ttu-id="8c236-120">Norėdami grįžti į **išskaitomo mokesčio vertes** laikotarpių puslapį uždarykite **išskaitomo mokesčio kodų** puslapį.</span><span class="sxs-lookup"><span data-stu-id="8c236-120">Close the **Withholding tax values** page to return to the **Withholding tax codes** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8c236-121">Išskaitomo mokesčio kodų puslapio mygtuko **Ribos** negalima naudoti su TDS **mokesčio tipo mokesčių** kodais.</span><span class="sxs-lookup"><span data-stu-id="8c236-121">The **Limits** button on the **Withholding tax codes** page isn't available for tax codes of the TDS tax type.</span></span>

12. <span data-ttu-id="8c236-122">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="8c236-122">Close the page.</span></span>
