---
title: Vidinės įmonės planavimas
description: Šiame skyriuje paaiškintas vidinės įmonės planavimas ir tai, kaip konfigūruoti jos planavimą su „Planning Optimization“ „Microsoft Dynamics 365 Supply Chain Management“.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 25c80ce27498131c6eb92174ab14a592bfa9915a
ms.sourcegitcommit: fe21a3a98dcf6fe4eb9351941493f2c0443d8696
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672198"
---
# <a name="intercompany-planning"></a><span data-ttu-id="bef7d-103">Vidinės įmonės planavimas</span><span class="sxs-lookup"><span data-stu-id="bef7d-103">Intercompany planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bef7d-104">Kai kurios organizacijose, logistinės operacijos priklauso nuo kitų juridinių asmenų (įmonių) organizacijos viduje.</span><span class="sxs-lookup"><span data-stu-id="bef7d-104">For some organizations, logistics operations depend on other legal entities (companies) in the organization.</span></span> <span data-ttu-id="bef7d-105">Šie veiksmai tvarkomi naudojant vidinės įmonės pardavimus ir pirkimus, nes kiekvienas juridnis asmuo yra atskiras sąskaitų grafikas.</span><span class="sxs-lookup"><span data-stu-id="bef7d-105">These operations are handled by using intercompany sales and purchases, because each legal entity has a separate chart of accounts.</span></span>

<span data-ttu-id="bef7d-106">Šiame skyriuje paaiškintas vidinės įmonės planavimas ir tai, kaip konfigūruoti jos planavimą su „Planning Optimization“ „Microsoft Dynamics 365 Supply Chain Management“.</span><span class="sxs-lookup"><span data-stu-id="bef7d-106">This topic describes intercompany planning and explains how to configure intercompany planning with Planning Optimization in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="bef7d-107">Šioje temoje naudojami tolesnės svarbios vidinės įmonės sąvokos:</span><span class="sxs-lookup"><span data-stu-id="bef7d-107">This topic uses the following important intercompany terms:</span></span>

- <span data-ttu-id="bef7d-108">**Prieš srovę** – Atitinkama nuoroda firmoje ar tiekimo grandinėje.</span><span class="sxs-lookup"><span data-stu-id="bef7d-108">**Upstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="bef7d-109">Jis rodo judėjimą žaliavų tiekėjo kryptimi.</span><span class="sxs-lookup"><span data-stu-id="bef7d-109">It indicates movement in the direction of the raw material supplier.</span></span>
- <span data-ttu-id="bef7d-110">**Pagal srovę** – Atitinkama nuoroda firmoje ar tiekimo grandinėje.</span><span class="sxs-lookup"><span data-stu-id="bef7d-110">**Downstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="bef7d-111">Jis rodo judėjimą kliento kryptimi.</span><span class="sxs-lookup"><span data-stu-id="bef7d-111">It indicates movement in the direction of the customer.</span></span>
- <span data-ttu-id="bef7d-112">**Suplanuota vidinės įmonės paklausa** – Suplanuota gaminio įmonėje paklausa pagal suplanuotą paklausą gaminiui iš pagal srovę įmonės.</span><span class="sxs-lookup"><span data-stu-id="bef7d-112">**Planned intercompany demand** – Planned demand for a product in a company, based on planned demand for the product from a downstream company.</span></span>

<span data-ttu-id="bef7d-113">Pagrindiniame planavime, planavimas vienoje įmonėje gali apimti planavimą vidinės įmonės paklausoje, kuri yra susieta su suplanuotais užsakymais pagal planą kitoje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="bef7d-113">In master planning, a plan in one company can include planned intercompany demand that is related to planned orders from a plan in another company.</span></span> <span data-ttu-id="bef7d-114">Pajėgumas naudingas, nes jis pateikia pilną planuojamų užsakymų visose įmonėse vaizdą.</span><span class="sxs-lookup"><span data-stu-id="bef7d-114">This capability is useful, because it provides full visibility into planned orders across companies.</span></span> <span data-ttu-id="bef7d-115">Jis taip pat užtikrini, kad visi suplanuoti tiekimo užsakymai yra sukurti, bet be poreikio suplanuotus užsakymus patvirtinti vidinės įmonės paklausai.</span><span class="sxs-lookup"><span data-stu-id="bef7d-115">It also ensures that all required planned supply orders are created, but without requiring that planned orders be firmed for the intercompany demand.</span></span>

<span data-ttu-id="bef7d-116">Jei vykdote pagrindinį planavimą iš pagrindinio plano, kuris apima suplanuotą pagal srovę paklausą, suplanuoti prikimo užsakymai iš susijusių vidinės įmonės pardavėjų bus įtraukti į planą pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="bef7d-116">If you run master planning from a master plan that includes planned downstream demand, planned purchase orders from the related intercompany vendors will be included in the plan as demand.</span></span>

## <a name="required-setup"></a><span data-ttu-id="bef7d-117">Būtinas nustatymas</span><span class="sxs-lookup"><span data-stu-id="bef7d-117">Required setup</span></span>

<span data-ttu-id="bef7d-118">Siekiant naudoti vidinės įmonės planavimą, turite parengti savo sistemą tokiu būdu:</span><span class="sxs-lookup"><span data-stu-id="bef7d-118">To use intercompany planning, you must prepare your system in the following way:</span></span>

1. <span data-ttu-id="bef7d-119">Atitinkami produktai turi būti išleisti visose atitinkamose įmonėse.</span><span class="sxs-lookup"><span data-stu-id="bef7d-119">The relevant products must be released in all the relevant companies.</span></span> <span data-ttu-id="bef7d-120">Dėl daugiau informacijos, žr [Konfigūruoti ir naudoti vidinės įmonės prekybą „Dynamics 365 Supply Chain Management“ ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="bef7d-120">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="bef7d-121">Pagal srovę paklausa turi būti padengta pirkimo formos tiekėjo, kuris turi vidinės įmonės sąsają su pagal srovės įmonę ir atitinkamą numatytojo inventoriaus matmenis (vietą ir sandėlį) klientui.</span><span class="sxs-lookup"><span data-stu-id="bef7d-121">Downstream demand must be covered by purchases from a vendor that has an intercompany relation to the upstream company and relevant default inventory dimensions (site and warehouse) on the customer.</span></span> <span data-ttu-id="bef7d-122">Dėl daugiau informacijos, žr [Konfigūruoti ir naudoti vidinės įmonės prekybą „Dynamics 365 Supply Chain Management“ ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span><span class="sxs-lookup"><span data-stu-id="bef7d-122">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="bef7d-123">Pagrindinis planavimas prieš srovės įmonės turi apimti suplanuotą palei srovės paklausą ir atitinkamą įmonę bei pagrindinis planavimas turi būti nurodytas palei srovės planuose.</span><span class="sxs-lookup"><span data-stu-id="bef7d-123">The master plan in the upstream company must include planned downstream demand, and the relevant company and master plan must be specified in the downstream plans.</span></span>

## <a name="include-planned-downstream-demand"></a><span data-ttu-id="bef7d-124">Įtraukti proceso pabaigoje suplanuotą poreikį</span><span class="sxs-lookup"><span data-stu-id="bef7d-124">Include planned downstream demand</span></span>

<span data-ttu-id="bef7d-125">Atlikite šiuos žingsnius tam, kad sukonfigūruotumėte pagrindinį planą taip, kad jis apimtų suplanuotą pagal srovę paklausą.</span><span class="sxs-lookup"><span data-stu-id="bef7d-125">Follow these steps to configure your master plan so that it includes planned downstream demand.</span></span>

1. <span data-ttu-id="bef7d-126">Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**.</span><span class="sxs-lookup"><span data-stu-id="bef7d-126">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="bef7d-127">Pasirinkite ar sukurkite pagrindinį planą.</span><span class="sxs-lookup"><span data-stu-id="bef7d-127">Select or create a master plan.</span></span>
1. <span data-ttu-id="bef7d-128">„FastTab“ **Vidinės įmonės planavimas** nustatykite šiuos laukelius:</span><span class="sxs-lookup"><span data-stu-id="bef7d-128">On the **Intercompany planning** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="bef7d-129">**Įtraukti suplanuotą pagal srovę poreikį** – Nustatykite šią parinktį į *Taip* siekiant įjungti vidinės įmonės planavimą pagrindiniam planui.</span><span class="sxs-lookup"><span data-stu-id="bef7d-129">**Include planned downstream demand** – Set this option to *Yes* to enable intercompany planning for the master plan.</span></span>
    - <span data-ttu-id="bef7d-130">**Pagal srovę planai** – Jei nustatote **Įtraukti suplanuotą pagal srovę poreikį** parinktį į *Taip*, naudokite įrankių juostą ir tinklelį, kad įtrauktumėte norimus pagrindinius planus iš kitų įmonių.</span><span class="sxs-lookup"><span data-stu-id="bef7d-130">**Downstream plans** – If you set the **Include planned downstream demand** option to *Yes*, use the toolbar and grid to add the desired master plans from other companies.</span></span>

## <a name="peg-across-companies-by-using-multilevel-pegging"></a><span data-ttu-id="bef7d-131">Fiksavimas visose įmonėse naudojant kelių lygių fiksavimą</span><span class="sxs-lookup"><span data-stu-id="bef7d-131">Peg across companies by using multilevel pegging</span></span>

<span data-ttu-id="bef7d-132">Kelių lygių fiksavime galite peržiūrėti fiksavimą įmonėse siekiant peržvelgti pradinį paklausos šaltinį, kuris yra padengtas tiekimu.</span><span class="sxs-lookup"><span data-stu-id="bef7d-132">In multilevel pegging, you can view pegging across companies to see the initial source of demand that is being covered by a supply.</span></span>

<span data-ttu-id="bef7d-133">Norėdami peržiūrėti kelių lygių fiksavimo informaciją, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="bef7d-133">To view multilevel pegging information, follow these steps.</span></span>

1. <span data-ttu-id="bef7d-134">Eikite į **Pagrindinis planavimas \> Pagrindinis planavimas \> Suplanuoti užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="bef7d-134">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="bef7d-135">Pasirinkite ar atidarykite suplanuotą užsakymą.</span><span class="sxs-lookup"><span data-stu-id="bef7d-135">Select or open a planned order.</span></span>
1. <span data-ttu-id="bef7d-136">Veiksmų juostoje **Rodinys** skirtukas, grupėje **Reikalavimai**, pasirinkite **Kelių lygių fiksavimas**.</span><span class="sxs-lookup"><span data-stu-id="bef7d-136">On the Action Pane, on the **View** tab, in the **Requirements** group, select **Multilevel pegging**.</span></span>

### <a name="intercompany-example-that-involves-two-companies"></a><span data-ttu-id="bef7d-137">Vidinės įmonės pavyzdys apimantis dvi įmones</span><span class="sxs-lookup"><span data-stu-id="bef7d-137">Intercompany example that involves two companies</span></span>

<span data-ttu-id="bef7d-138">Šiame pavyzdyje, suplanuotas gamybos užsakymas yra sukuriamas USMF įmonėje siekiant padengti pardavimo užsakymą DEMF įmonėje.</span><span class="sxs-lookup"><span data-stu-id="bef7d-138">For this example, a planned production order is created in the USMF company to cover a sales order in the DEMF company.</span></span> <span data-ttu-id="bef7d-139">USMF tiesioginis poreikis suplanuotai vidinės įmonės paklausai.</span><span class="sxs-lookup"><span data-stu-id="bef7d-139">In USMF, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="bef7d-140">Norėdami, kad ši paklausa pasirodytų USMF, pagrindinis planavimas pirmiausia vykdomas DEMF ir tada USMF.</span><span class="sxs-lookup"><span data-stu-id="bef7d-140">To make this demand appear in USMF, master planning is run first in DEMF and then in USMF.</span></span>

<span data-ttu-id="bef7d-141">Tolesnis paveikslėlis rodo, kaip šis pavyzdys gali būti rodomas **Kelių lygių fiksavimo** puslapyje suplanuotos gamybos užsakymui.</span><span class="sxs-lookup"><span data-stu-id="bef7d-141">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Vidinės įmonės pavyzdys apimantis dvi įmones](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a><span data-ttu-id="bef7d-143">Vidinės įmonės pavyzdys apimantis tris įmones</span><span class="sxs-lookup"><span data-stu-id="bef7d-143">Intercompany example that involves three companies</span></span>

<span data-ttu-id="bef7d-144">Šiame pavyzdyje, suplanuotas pirkimo užsakymas yra sukuriamas USMF įmonėje siekiant padengti pardavimo užsakymą FRRT įmonėje.</span><span class="sxs-lookup"><span data-stu-id="bef7d-144">For this example, a planned purchase order is created in the USMF company to cover a sales order in the FRRT company.</span></span> <span data-ttu-id="bef7d-145">DEMF ir USM įmonėms, tiesioginė paklausa suplanuotai vidinės įmonės paklausai.</span><span class="sxs-lookup"><span data-stu-id="bef7d-145">In the DEMF and USMF companies, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="bef7d-146">Norėdami, kad ši paklausa pasirodytų USMF, pagrindinis planavimas pirmiausia vykdomas FRRT ir tada DEMF, o galiausiai USMF.</span><span class="sxs-lookup"><span data-stu-id="bef7d-146">To make this demand appear in USMF, master planning is run first in FRRT, then in DEMF, and finally in USMF.</span></span>

<span data-ttu-id="bef7d-147">Tolesnis paveikslėlis rodo, kaip šis pavyzdys gali būti rodomas **Kelių lygių fiksavimo** puslapyje suplanuotos gamybos užsakymui.</span><span class="sxs-lookup"><span data-stu-id="bef7d-147">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Vidinės įmonės pavyzdys apimantis tris įmones](media/IntercompanyPlanning2.png)