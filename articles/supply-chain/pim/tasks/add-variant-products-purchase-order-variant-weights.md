---
title: Įtraukti produktų variantus į pirkimo užsakymus naudojant variantų svorius
description: Ši procedūra padės atlikti veiksmus norint variantų svorius naudoti kiekvieno produkto varianto pirkimo užsakymo eilutėms automatiškai įvesti.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27ff3784074a36d073930ba68c8dec8b1121356e
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4433997"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a><span data-ttu-id="98145-103">Įtraukti produktų variantus į pirkimo užsakymus naudojant variantų svorius</span><span class="sxs-lookup"><span data-stu-id="98145-103">Add variant products to purchase orders using variant weights</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98145-104">Ši procedūra padės atlikti veiksmus norint variantų svorius naudoti kiekvieno produkto varianto pirkimo užsakymo eilutėms automatiškai įvesti.</span><span class="sxs-lookup"><span data-stu-id="98145-104">This procedure walks through the steps for using variant weights to auto populate purchase order lines for each variant of a product.</span></span> <span data-ttu-id="98145-105">Kai pasirenkate norimo pirkti produkto kiekį, sukuriamos visų produkto variantų pirkimo užsakymo eilutės su siūlomais kiekiais, atsižvelgiant į kiekius, sukonfigūruotus produkto variantuose.</span><span class="sxs-lookup"><span data-stu-id="98145-105">When you select the quantity of the product you want to purchase, purchase order lines are created for all the variants of the product with suggested quantities based on the weights configured on the product variants.</span></span> <span data-ttu-id="98145-106">Ši procedūra neapima veiksmų kiekio reikšmėms produkto dimensijose ir produkto variantuose sukonfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="98145-106">This procedure doesn't include steps to configure weight values on product dimensions and product variants.</span></span> <span data-ttu-id="98145-107">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="98145-107">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="98145-108">Eikite į Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai.</span><span class="sxs-lookup"><span data-stu-id="98145-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="98145-109">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="98145-109">Click New.</span></span>
3. <span data-ttu-id="98145-110">Lauke Tiekėjo sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="98145-110">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="98145-111">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="98145-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="98145-112">Perjunkite dalies Bendra išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="98145-112">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="98145-113">Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="98145-113">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="98145-114">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="98145-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="98145-115">Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="98145-115">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="98145-116">Sąraše raskite ir pasirinkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="98145-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="98145-117">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="98145-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="98145-118">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="98145-118">Click OK.</span></span>
12. <span data-ttu-id="98145-119">Perjunkite dalies Išsami eilučių informacija išplėtimą.</span><span class="sxs-lookup"><span data-stu-id="98145-119">Toggle the expansion of the Line details section.</span></span>
13. <span data-ttu-id="98145-120">Spustelėkite skirtuką Variantai.</span><span class="sxs-lookup"><span data-stu-id="98145-120">Click the Variants tab.</span></span>
14. <span data-ttu-id="98145-121">Spustelėkite Pridėti eilutę.</span><span class="sxs-lookup"><span data-stu-id="98145-121">Click Add line.</span></span>
15. <span data-ttu-id="98145-122">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="98145-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="98145-123">Lauke Prekės numeris įveskite „0140“.</span><span class="sxs-lookup"><span data-stu-id="98145-123">In the Item number field, type '0140'.</span></span>
17. <span data-ttu-id="98145-124">Nustatykite kiekį – 1000.</span><span class="sxs-lookup"><span data-stu-id="98145-124">Set Quantity to '1000'.</span></span>
18. <span data-ttu-id="98145-125">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="98145-125">Click Save.</span></span>

