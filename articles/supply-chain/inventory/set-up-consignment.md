---
title: Konsignacijos nustatymas
description: "Šioje temoje paaiškinama, kaip sukonfigūruoti gaunamų konsignacijos atsargų operacijas."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 41c1b8de0aae24efb30a670d3109b6d65e6abd9c
ms.contentlocale: lt-lt
ms.lasthandoff: 09/12/2017

---

# <a name="set-up-consignment"></a><span data-ttu-id="0084e-103">Konsignacijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="0084e-103">Set up consignment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0084e-104">Šioje temoje paaiškinama, kaip sukonfigūruoti gaunamų konsignacijos atsargų operacijas.</span><span class="sxs-lookup"><span data-stu-id="0084e-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="0084e-105">Konsignacijos atsargos yra tiekėjo turimos atsargos, kurios laikomos jūsų vietoje.</span><span class="sxs-lookup"><span data-stu-id="0084e-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="0084e-106">Kai esate pasiruošę vartoti ar naudoti atsargas, atsargos tampa jūsų nuosavybe.</span><span class="sxs-lookup"><span data-stu-id="0084e-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="0084e-107">Šioje temoje aprašoma sąranka, reikalinga norint įgalinti konsignacijos procesą.</span><span class="sxs-lookup"><span data-stu-id="0084e-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="0084e-108">Norėdami gauti daugiau informacijos apie konsignacijos procesus, žr. [Konsignacija](consignment.md).</span><span class="sxs-lookup"><span data-stu-id="0084e-108">For more information about consignment processes, see [Consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="0084e-109">Atsargų savininkai</span><span class="sxs-lookup"><span data-stu-id="0084e-109">Inventory owners</span></span>
<span data-ttu-id="0084e-110">Norėdami įrašyti faktines gaunamos konsignacijos atsargas, turite nurodyti tiekėją, kuriam jos priklauso.</span><span class="sxs-lookup"><span data-stu-id="0084e-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="0084e-111">Tai atliekama puslapyje **Atsargų savininkas**.</span><span class="sxs-lookup"><span data-stu-id="0084e-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="0084e-112">Pasirinkus **Tiekėjo sąskaita** sugeneruojamos numatytosios laukų **Vardas** ir **Savininkas** vertės.</span><span class="sxs-lookup"><span data-stu-id="0084e-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="0084e-113">Lauko **Savininkas** vertė matoma tiekėjui, todėl jeigu jūsų tiekėjo paskyros vardus kitiems gali būti sunku atpažinti, gali tekti juos pakeisti.</span><span class="sxs-lookup"><span data-stu-id="0084e-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="0084e-114">Lauką **Savininkas** galima redaguoti, bet tik iki veiksmo, kai išsaugomas įrašas **Atsargų savininkas**.</span><span class="sxs-lookup"><span data-stu-id="0084e-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="0084e-115">Lauke **Vardas** įrašomas su tiekėjo paskyra susietos šalies vardas ir jo negalima keisti.</span><span class="sxs-lookup"><span data-stu-id="0084e-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="0084e-116">[![atsargų savininkai](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="0084e-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="0084e-117">Sekimo dimensijų grupė</span><span class="sxs-lookup"><span data-stu-id="0084e-117">Tracking dimension group</span></span>
<span data-ttu-id="0084e-118">Konsignacijos procesuose ketinamus naudoti elementus būtina susieti su **Sekimo dimensijų grupe**, kurios dimensijos **Savininkas** nuostata **Aktyvi**.</span><span class="sxs-lookup"><span data-stu-id="0084e-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="0084e-119">Visada pažymėtos dimensijos Savininkas parinktys **Faktinės atsargos** ir **Finansinės atsargos**.</span><span class="sxs-lookup"><span data-stu-id="0084e-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="0084e-120">Parinktis **Padengimo planas pagal dimensiją** niekada nepažymimas.</span><span class="sxs-lookup"><span data-stu-id="0084e-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="0084e-121">[![sekimo dimensijų grupė](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="0084e-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="0084e-122">Atsargų nuosavybės pakeitimo žurnalas</span><span class="sxs-lookup"><span data-stu-id="0084e-122">Inventory ownership change journal</span></span>
<span data-ttu-id="0084e-123">Žurnalas **Atsargų nuosavybės pakeitimas**naudojamas norint įrašyti konsignacijos atsargų savininko pakeitimą iš tiekėjo į jį naudojantį juridinį subjektą.</span><span class="sxs-lookup"><span data-stu-id="0084e-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="0084e-124">Kaip ir bet kuriame atsargų žurnale, jame turi būti nurodytas atsargų žurnalo pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="0084e-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="0084e-125">Šie pavadinimai sukuriami puslapyje **Atsargų žurnalo pavadinimai** ir turi būti nustatyta dalies **Žurnalo tipas** parinktis **Nuosavybės pakeitimas**.</span><span class="sxs-lookup"><span data-stu-id="0084e-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="0084e-126">[![atsargų nuosavybės pakeitimo žurnalas](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="0084e-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="0084e-127">Tiekėjų bendradarbiavimas konsignacijos procesuose</span><span class="sxs-lookup"><span data-stu-id="0084e-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="0084e-128">Jei jūsų tiekėjai naudoja tiekėjų bendradarbiavimo sąsają, jie gali ją panaudoti norėdami stebėti atsargų suvartojimą jūsų vietoje.</span><span class="sxs-lookup"><span data-stu-id="0084e-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="0084e-129">Daugiau informacijos apie tiekėjų parengimą naudoti tiekėjų bendradarbiavimo funkciją rasite dalyje [Tiekėjo bendradarbiavimo funkcijos vartotojų saugos konfigūracija](../procurement/configure-security-vendor-portal-users.md).</span><span class="sxs-lookup"><span data-stu-id="0084e-129">For more information about setting up vendors to use vendor collaboration, see [Configuration of security for vendor collaboration users](../procurement/configure-security-vendor-portal-users.md).</span></span>
