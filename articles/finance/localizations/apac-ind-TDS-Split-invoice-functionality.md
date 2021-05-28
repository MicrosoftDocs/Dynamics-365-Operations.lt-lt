---
title: Skaidyti SF funkcijas
description: Šioje temoje aprašomos SF skaidymo pagal pristatymo adresą ir mokesčių sąskaitos numerį (TAN) funkcijos.
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
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023453"
---
# <a name="split-invoice-functionality"></a><span data-ttu-id="7e157-103">Skaidyti SF funkcijas</span><span class="sxs-lookup"><span data-stu-id="7e157-103">Split invoice functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e157-104">Šioje temoje aprašomos SF skaidymo pagal pristatymo adresą ir mokesčių sąskaitos numerį (TAN) funkcijos.</span><span class="sxs-lookup"><span data-stu-id="7e157-104">This topic describes the setup and functionality for splitting invoices by delivery address and tax account number (TAN).</span></span>

<span data-ttu-id="7e157-105">Puslapyje **Mokėtinų sąskaitų parametrai** skirtuke **Bendri** rinkitės **Produkto gavimo kvitas** ar **SF** žymimą laukelį, kad publikuotumėte ir išskirstytumėte produkto gavimo kvitą ir SF, kurių pirstatymo adresai ir TAN skiriasi **Pirkimo užsakymo** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="7e157-105">On the **Accounts payable parameters** page, on the **General** tab, select the **Product receipt** or **Invoice** checkbox to post and split a product receipt or invoice that has different delivery addresses and TANs on the **Purchase order** page.</span></span> <span data-ttu-id="7e157-106">Užregistruota SF bus padalinta pagal pristatymo adresą ir TAN.</span><span class="sxs-lookup"><span data-stu-id="7e157-106">The posted invoice will then be split by delivery address and TAN.</span></span>

<span data-ttu-id="7e157-107">Skirtuke **Suminis atnaujinimas** „FastTab“ **Skaidymas pagrįstas pagal** eilutėje **Pristatymo informacija** nustatykite **Patvirtinimas**, **Paėmimo sąrašas**, **Važtaraštis**, ar **SF** parinktį į **Taip** norėdami publikuoti ir išskaidyti patvirtinimą, paėmimo sąrašą, važtaraštį ar sąskaitą, turinčius kitus pristatymo adresus ir TAN nei nustatyta kitose sąskaitų eilutėse **Pardavimo užsakymas** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="7e157-107">On the **Summary update** tab, on the **Split based on** FastTab, in the **Delivery information** row, set the **Confirmation**, **Picking list**, **Packing slip**, or **Invoice** option to **Yes** to post and split a confirmation, picking list, packing slip, or invoice where different delivery addresses and TANs are defined for different invoice lines on the **Sales order** page.</span></span> <span data-ttu-id="7e157-108">Užregistruota SF bus padalinta pirma pagal pristatymo adresą ir TAN.</span><span class="sxs-lookup"><span data-stu-id="7e157-108">The invoice will be split first by delivery address and then by TAN.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="7e157-109">Jei **pristatymo informacijos** pasirinktys nėra nustatytos kaip **Taip**, SF bus registruojama kaip viena SF.</span><span class="sxs-lookup"><span data-stu-id="7e157-109">If no options for **Delivery information** are set to **Yes**, the invoice will be posted as a single invoice.</span></span> <span data-ttu-id="7e157-110">SF nebus padalyta.</span><span class="sxs-lookup"><span data-stu-id="7e157-110">No invoice splitting will occur.</span></span>
> - <span data-ttu-id="7e157-111">Norėdami suskaidyti ir užregistruoti važtaraštį, kuriame SF eilučių pristatymo adresai ir TAN skiriasi, turite nustatyti **pristatymo informacijos** parinkties **Važtaraštis funkciją** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7e157-111">To split and post a packing slip where the invoice lines have different delivery addresses and TANs, you must set the **Packing slip** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="7e157-112">Norėdami suskaidyti ir užregistruoti sąskaitą, kuriame SF eilučių pristatymo adresai ir TAN skiriasi, turite nustatyti **Sąskaita** parinkties **Važtaraštis funkciją** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7e157-112">To split and post an invoice where the invoice lines have different delivery addresses and TANs, you must set the **Invoice** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="7e157-113">Norėdami suskaidyti ir užregistruoti sąskaitą, kuriame SF eilučių pristatymo adresai ir TAN tas pats, turite nustatyti **Sąskaita** parinkties **Važtaraštis funkciją** į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="7e157-113">To post an invoice where the invoice lines have different delivery addresses but the same TAN, set the **Invoice** option for **Delivery information** to **No**.</span></span> <span data-ttu-id="7e157-114">Užregistruota SF bus padalinta pirma pagal pristatymo adresą ir TAN.</span><span class="sxs-lookup"><span data-stu-id="7e157-114">The invoice will be split by delivery address.</span></span>

## <a name="example"></a><span data-ttu-id="7e157-115">Pavyzdys</span><span class="sxs-lookup"><span data-stu-id="7e157-115">Example</span></span>

<span data-ttu-id="7e157-116">Šiame pavyzdyje **Sąskaita** parinktis **Pristatymo informacijai** yra nustatyta į **Taip** skirtuke **Santraukos naujinimas** puslapyje **Mokėtinų sąskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="7e157-116">In this example, the **Invoice** option for **Delivery information** is set to **Yes** on the **Summary update** tab of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="7e157-117">Užregistruojama pirkimo SF, kurios eilutėse nustatyti šie pristatymo adresai ir TAN:</span><span class="sxs-lookup"><span data-stu-id="7e157-117">A purchase invoice is posted that has the following setup for delivery addresses and TANs on the lines:</span></span>

- <span data-ttu-id="7e157-118">**1 prekės eilutė 1:** pristatymo adresas, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="7e157-118">**Item line 1:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="7e157-119">**2 prekės eilutė 1:** pristatymo adresas, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="7e157-119">**Item line 2:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="7e157-120">**3 prekės eilutė 2:** pristatymo adresas, TAN-ABCE12345B</span><span class="sxs-lookup"><span data-stu-id="7e157-120">**Item line 3:** Delivery address 2, TAN-ABCE12345B</span></span>
- <span data-ttu-id="7e157-121">**4 prekės eilutė 3:** pristatymo adresas, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="7e157-121">**Item line 4:** Delivery address 3, TAN-ABCD12345A</span></span>

<span data-ttu-id="7e157-122">Tokiu atveju originali SF suskaidoma į dvi SF ir registruojama tokiu būdu:</span><span class="sxs-lookup"><span data-stu-id="7e157-122">In this case, the original invoice is split into two invoices and posted in the following way:</span></span>

- <span data-ttu-id="7e157-123">Registruojama 1 prekės eilutės ir 2 prekės eilutės SF, nes abiejų eilučių pristatymo adresas ir TAN yra vienodi.</span><span class="sxs-lookup"><span data-stu-id="7e157-123">Invoice 1 is posted for item line 1 and item line 2, because both lines have the same delivery address and TAN.</span></span>
- <span data-ttu-id="7e157-124">Užregistruota 3 prekės eilutės 2 SF.</span><span class="sxs-lookup"><span data-stu-id="7e157-124">Invoice 2 is posted for item line 3.</span></span>
- <span data-ttu-id="7e157-125">Užregistruota 4 prekės eilutės 3 SF.</span><span class="sxs-lookup"><span data-stu-id="7e157-125">Invoice 3 is posted for item line 4.</span></span>
