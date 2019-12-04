---
title: Išorinių katalogų naudojimas el. įsigijimų išėjimo laikui žymėti
description: Šioje temoje paaiškinama, kaip galite naudoti išorinius katalogus norėdami sukurti ir pateikti paraiškas.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec2874fb21184ccbf4f7039acf20db399e5cf5fb
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813344"
---
# <a name="use-external-catalogs-for-punchout-eprocurement"></a><span data-ttu-id="61eb6-103">Išorinių katalogų naudojimas el. įsigijimų išėjimo laikui žymėti</span><span class="sxs-lookup"><span data-stu-id="61eb6-103">Use external catalogs for PunchOut eProcurement</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61eb6-104">Naudojant išorinius katalogus el. įsigijimų išėjimui žymėti, jums nereikės tvarkyti informacijos apie tiekėjų produktus savo bendruosiuose duomenyse.</span><span class="sxs-lookup"><span data-stu-id="61eb6-104">By using external catalogs for PunchOut e-procurement, you don't have to maintain information about your vendors' products in your own master data.</span></span> <span data-ttu-id="61eb6-105">Vietoj to pirkimo krepšelis tiekėjo svetainėje konvertuojamas į paraiškos eilutes, kuriose yra teisinga produkto informacija.</span><span class="sxs-lookup"><span data-stu-id="61eb6-105">Instead, the shopping cart on a vendor's website is converted to requisition lines that have the correct product information.</span></span> 

<span data-ttu-id="61eb6-106">Turėtumėte vengti tvarkyti tiekėjo produktų aprašymus ir kainas savo bendrųjų produktų duomenyse.</span><span class="sxs-lookup"><span data-stu-id="61eb6-106">You should avoid maintaining the descriptions and prices of your vendors’ products in your own product master data.</span></span> <span data-ttu-id="61eb6-107">Verčiau el. įsigijimų išėjimui žymėti naudokite išorinius katalogus.</span><span class="sxs-lookup"><span data-stu-id="61eb6-107">Instead, use external catalogs for PunchOut e-procurement.</span></span> <span data-ttu-id="61eb6-108">Tada, kai darbuotojai kuria paraiškas, jie gali „pažymėti išėjimą“ į tiekėjo išorinio katalogo svetainę (kitaip sakant, jie palieka jūsų sistemą ir eina į tiekėjo svetainę).</span><span class="sxs-lookup"><span data-stu-id="61eb6-108">Then, when employees create requisitions, they can “punch out” to a vendor’s external catalog site (in other words, they leave your system and go to the vendor’s site).</span></span> <span data-ttu-id="61eb6-109">Produktus, kurie yra įtraukiami į pirkimo krepšelį tiekėjo svetainėje, galima konvertuoti į paraiškos eilutes.</span><span class="sxs-lookup"><span data-stu-id="61eb6-109">The products that are added to the shopping cart on the vendor’s website can then be converted to requisition lines.</span></span> <span data-ttu-id="61eb6-110">Todėl galite gauti teisingą produkto informaciją: produkto ID, pavadinimas, kaina ir t. t.</span><span class="sxs-lookup"><span data-stu-id="61eb6-110">Therefore, you get the correct product information: product ID, name, price, and so on.</span></span>

<span data-ttu-id="61eb6-111">Norėdamas naudoti išorinius katalogus darbuotojas turi sukurti paraišką puslapyje **Mano pirkimo paraiškos**.</span><span class="sxs-lookup"><span data-stu-id="61eb6-111">To use external catalogs, an employee must create a requisition on the **My purchase requisitions** page.</span></span>

<span data-ttu-id="61eb6-112">Darbuotojas, kuris sukuria paraišką, paraiškoje nurodomas kaip rengėjas.</span><span class="sxs-lookup"><span data-stu-id="61eb6-112">The employee who creates a requisition is referred to as the preparer of the requisition.</span></span> <span data-ttu-id="61eb6-113">Kaip rengėjas galite atlikti nurodytas užduotis.</span><span class="sxs-lookup"><span data-stu-id="61eb6-113">As a preparer, you can complete the following tasks.</span></span>

<span data-ttu-id="61eb6-114">Naudokite eilutės veiksmą **Išoriniai katalogai** norėdami atidaryti puslapį, kuriame yra visi išoriniai katalogai, pasiekiami nurodytam prašytojui, perkančiam juridiniam subjektui ir gaunančiam valdymo vienetui.</span><span class="sxs-lookup"><span data-stu-id="61eb6-114">Use the **External catalogs** line action to open a page that includes all external catalogs that are available for the specified requester, buying legal entity, and receiving operating unit.</span></span>

<span data-ttu-id="61eb6-115">Priklausomai nuo jūsų teisų pakeiskite prašytoją, perkantį juridinį subjektą ir gaunantį valdymo vienetą.</span><span class="sxs-lookup"><span data-stu-id="61eb6-115">Depending on your permissions, change the requester, buying legal entity, and receiving operating unit.</span></span> <span data-ttu-id="61eb6-116">Tų verčių pakeitimas gali pakeisti prašytojui pasiekiamą išorinių katalogų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="61eb6-116">A change in those values might change the list of external catalogs that are available to a requester.</span></span> <span data-ttu-id="61eb6-117">Pasiekiami išoriniai katalogai priklauso nuo šiuo metu aktyvių perkančio juridinio subjekto arba gaunančio valdymo vieneto pirkimo strategijų.</span><span class="sxs-lookup"><span data-stu-id="61eb6-117">The external catalogs that are available depend on the current active purchasing policies for the buying legal entity or the receiving operating unit.</span></span> <span data-ttu-id="61eb6-118">Šios strategijos gali leisti arba neleisti pasiekti konkrečias įsigijimo kategorijas.</span><span class="sxs-lookup"><span data-stu-id="61eb6-118">These policies can allow or prevent access to specific procurement categories.</span></span> <span data-ttu-id="61eb6-119">Todėl gali būti paveiktas išorinių katalogų, susietų su šiomis įsigijimo kategorijomis, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="61eb6-119">Therefore, the list of external catalogs that are mapped to these procurement categories can be affected.</span></span>

<span data-ttu-id="61eb6-120">Daugiau informacijos apie strategijas žr. [Pirkimo strategijų apžvalga](../procurement/purchase-policies.md).</span><span class="sxs-lookup"><span data-stu-id="61eb6-120">For more information about policies, see [Purchasing policies overview](../procurement/purchase-policies.md).</span></span>

- <span data-ttu-id="61eb6-121">Norėdami rasti konkrečių įsigijimo kategorijų išorinių katalogų, katalogo paieškos lauke įveskite tekstą.</span><span class="sxs-lookup"><span data-stu-id="61eb6-121">To find external catalogs for specific procurement categories, enter text in the catalog search field.</span></span>
- <span data-ttu-id="61eb6-122">Norėdami įtraukti produktų iš tiekėjo išorinio katalogo tiekėjo svetainėje, spustelėkite išorinį katalogą.</span><span class="sxs-lookup"><span data-stu-id="61eb6-122">To add products from a vendor’s external catalog on the vendor’s website, click the external catalog.</span></span> <span data-ttu-id="61eb6-123">Tada įtraukite produktų į pirkimo krepšelį ir išsiregistruokite. Pirkimo krepšelio eilutės bus perkeltos į „Microsoft Dynamics 365“.</span><span class="sxs-lookup"><span data-stu-id="61eb6-123">Then add products to the shopping cart, and check out. The shopping cart lines will be transferred to Microsoft Dynamics 365.</span></span>

<span data-ttu-id="61eb6-124">Jei yra kelios įsigijimo kategorijų parinktys, pasirinkite tinkamą įsigijimo kategoriją prieš įtraukdami į paraišką eilutes.</span><span class="sxs-lookup"><span data-stu-id="61eb6-124">If there are multiple options for procurement categories, select the correct procurement category before you add the lines to the requisition.</span></span>
<span data-ttu-id="61eb6-125">Kai eilutės įtraukiamos į paraišką, galite įtraukti daugiau eilučių nenaudodami išorinių katalogų.</span><span class="sxs-lookup"><span data-stu-id="61eb6-125">After lines have been added to a requisition, you can add more lines without using external catalogs.</span></span> <span data-ttu-id="61eb6-126">Arba galite toliau naudoti išorinius katalogus, kad įtrauktumėte eilučių.</span><span class="sxs-lookup"><span data-stu-id="61eb6-126">Alternatively, you can continue to use external catalogs to add lines.</span></span>

<span data-ttu-id="61eb6-127">Kai paraiška paruošta, naudokite veiksmą **Darbo eiga** > **Pateikti** norėdami pateikti tvirtinti.</span><span class="sxs-lookup"><span data-stu-id="61eb6-127">When the requisition is ready, use the **Workflow** > **Submit** action to submit it for approval.</span></span>
