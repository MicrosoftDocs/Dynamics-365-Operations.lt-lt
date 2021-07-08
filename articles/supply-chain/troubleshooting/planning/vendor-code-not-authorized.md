---
title: Tiekėjo kodas nėra įgaliotas konkrečiam produktui ir datai
description: Kai bandote patvirtinti suplanuotą užsakymą arba prie pirkimo užsakymo pridėti eilutę, gaunate klaidos pranešimą, kuriame teigiama, kad tiekėjo kodas nėra įgaliotas produktui ir datai.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294140"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a><span data-ttu-id="b1ede-103">Tiekėjo kodas nėra įgaliotas konkrečiam produktui ir datai</span><span class="sxs-lookup"><span data-stu-id="b1ede-103">Vendor code isn't authorized for a specific product and date</span></span>

<span data-ttu-id="b1ede-104">Klaidos kodas: SYP4881415</span><span class="sxs-lookup"><span data-stu-id="b1ede-104">Error code: SYP4881415</span></span>

## <a name="symptoms"></a><span data-ttu-id="b1ede-105">Požymiai</span><span class="sxs-lookup"><span data-stu-id="b1ede-105">Symptoms</span></span>

<span data-ttu-id="b1ede-106">Kai bandote patvirtinti suplanuotą užsakymą arba pridėti eilutę prie pirkimo užsakymo, gaunate tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="b1ede-106">When you try to firm a planned order or add a line to a purchase order, you receive the following error message:</span></span>

> <span data-ttu-id="b1ede-107">Tiekėjo kodo %1 negalima naudoti %2 ir %3.</span><span class="sxs-lookup"><span data-stu-id="b1ede-107">Vendor code %1 is not authorized for %2 on %3.</span></span>

## <a name="cause"></a><span data-ttu-id="b1ede-108">Priežastis</span><span class="sxs-lookup"><span data-stu-id="b1ede-108">Cause</span></span>

<span data-ttu-id="b1ede-109">Ši klaida įvyksta, nes laukas **Patvirtinto tiekėjo patikros metodas** yra nustatytas į *Tik įspėjimas* arba *Neleidžiama* konkrečiam produktui, o tiekėjas šiuo metu nėra įgaliotas tiekti tą produktą.</span><span class="sxs-lookup"><span data-stu-id="b1ede-109">The error occurs because the **Approved vendor check method** field is set to *Warning only* or *Not allowed* for the specified product, and the vendor isn't currently authorized to supply that product.</span></span>

## <a name="resolution"></a><span data-ttu-id="b1ede-110">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="b1ede-110">Resolution</span></span>

<span data-ttu-id="b1ede-111">Norėdami išspręsti šią problemą, išjunkite atitinkamo produkto tiekėjo patikrą arba patvirtinkite tiekėją.</span><span class="sxs-lookup"><span data-stu-id="b1ede-111">To fix this issue, either disable the vendor check for the relevant product or approve the vendor.</span></span>

<span data-ttu-id="b1ede-112">Norėdami išjungti produkto tiekėjo patikrą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b1ede-112">To disable the vendor check for a product, follow these steps.</span></span>

1. <span data-ttu-id="b1ede-113">Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="b1ede-113">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b1ede-114">Atidarykite atitinkamą produktą.</span><span class="sxs-lookup"><span data-stu-id="b1ede-114">Open the relevant product.</span></span>
1. <span data-ttu-id="b1ede-115">„FastTab” **Pirkimas** nustatykite lauko **Patvirtinto tiekėjo patikros metodas** reikšmę į kitokią nei *Tik įspėjimas* ar *Neleidžiama*.</span><span class="sxs-lookup"><span data-stu-id="b1ede-115">On the **Purchase** FastTab, set the **Approved vendor check method** field to a value other than *Warning only* or *Not allowed*.</span></span>

<span data-ttu-id="b1ede-116">Norėdami patvirtinti produkto tiekėją, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="b1ede-116">To approve a vendor for a product, follow these steps.</span></span>

1. <span data-ttu-id="b1ede-117">Eikite į **Produkto informacijos valdymas \> Produktai \> Išleisti produktai**.</span><span class="sxs-lookup"><span data-stu-id="b1ede-117">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b1ede-118">Atidarykite atitinkamą prekę.</span><span class="sxs-lookup"><span data-stu-id="b1ede-118">Open the relevant item.</span></span>
1. <span data-ttu-id="b1ede-119">Veiksmų srities skirtuko **Pirkimas** grupėje **Patvirtintas tiekėjas** pasirinkite **Nustatymas**.</span><span class="sxs-lookup"><span data-stu-id="b1ede-119">On the Action Pane, on the **Purchase** tab, in the **Approved vendor** group, select **Setup**.</span></span>
1. <span data-ttu-id="b1ede-120">**Patvirtintų tiekėjų** sąrašo puslapyje į tinklelį įtraukite eilutę ir nustatykite šias jo vertes:</span><span class="sxs-lookup"><span data-stu-id="b1ede-120">On the **Approved vendor** list page, add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="b1ede-121">**Tiekėjas** – Pasirinkite tiekėją, kuris patvirtins dabartinį produktą.</span><span class="sxs-lookup"><span data-stu-id="b1ede-121">**Vendor** – Select the vendor to approve for the current product.</span></span>
    - <span data-ttu-id="b1ede-122">**Įsigaliojimo data** – Pasirinkite pirmą datą kuriai patvirtintas tiekėjas.</span><span class="sxs-lookup"><span data-stu-id="b1ede-122">**Effective date** – Select the first date that the vendor is approved for.</span></span>
    - <span data-ttu-id="b1ede-123">**Galiojimo data** – Pasirinkite paskutinę datą kuriai patvirtintas tiekėjas.</span><span class="sxs-lookup"><span data-stu-id="b1ede-123">**Expiration date** – Select the last date that the vendor is approved for.</span></span>

<span data-ttu-id="b1ede-124">Daugiau informacijos rasite [Konkrečių produktų tiekėjų tvirtinimas](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span><span class="sxs-lookup"><span data-stu-id="b1ede-124">For more information, see [Approve vendors for specific products](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span></span>
