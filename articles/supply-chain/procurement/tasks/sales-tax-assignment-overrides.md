---
title: PVM priskyrimas ir perrašymai
description: Ši procedūra parodo, kaip prekybos kanalams galima priskirti PVM grupes.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 469850d8ed9251a827e834a483653ea7926bd414
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244068"
---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="6be22-103"> PVM priskyrimas ir perrašymai​</span><span class="sxs-lookup"><span data-stu-id="6be22-103">Sales tax assignment and overrides</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6be22-104">Ši procedūra parodo, kaip prekybos kanalams galima priskirti PVM grupes.</span><span class="sxs-lookup"><span data-stu-id="6be22-104">This procedure demonstrates how to assign sales tax groups to commerce channels.</span></span> <span data-ttu-id="6be22-105">Joje taip pat paaiškinamas procesas, kurio metu sukuriamas naujas PVM perrašymas ir priskiriamas esamai PVM perrašymo grupei.</span><span class="sxs-lookup"><span data-stu-id="6be22-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="6be22-106">Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.</span><span class="sxs-lookup"><span data-stu-id="6be22-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="6be22-107">Eikite į „Retail and Commerce“ > Kanalai > Parduotuvės > Visos parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="6be22-107">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="6be22-108">Sąraše spustelėkite „Houston“ nuorodą „Kanalo ID“.</span><span class="sxs-lookup"><span data-stu-id="6be22-108">In the list, click the Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="6be22-109">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="6be22-109">Click Edit.</span></span>
    * <span data-ttu-id="6be22-110">Lauke PVM grupė pateikiamas dabartinės įmonės PVM grupių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="6be22-110">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="6be22-111">Šiuo metu priskirta grupė yra bendroji PVM grupė „Texas“.</span><span class="sxs-lookup"><span data-stu-id="6be22-111">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="6be22-112">Taip pat galimos PVM grupės „Washington“ ir „Washington, King County“.</span><span class="sxs-lookup"><span data-stu-id="6be22-112">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="6be22-113">PVM grupės gali apimti keliose savivaldybėse taikomus mokesčius.</span><span class="sxs-lookup"><span data-stu-id="6be22-113">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="6be22-114">Lauke PVM perrašymas PVM perrašymo grupes galima susieti su kanalu.</span><span class="sxs-lookup"><span data-stu-id="6be22-114">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="6be22-115">PVM perrašymo grupes galima naudoti norint grupuoti PVM perrašymus, taikomus kelioms parduotuvėms.</span><span class="sxs-lookup"><span data-stu-id="6be22-115">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="6be22-116">Užuot neautomatiniu būdu priskyrus atskirus PVM perrašymus, galima sutaupyti laiko sukuriant grupę ir ją tiesiogiai priskiriant kanalams.</span><span class="sxs-lookup"><span data-stu-id="6be22-116">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="6be22-117">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="6be22-117">Click Save.</span></span>
5. <span data-ttu-id="6be22-118">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="6be22-118">Close the page.</span></span>
6. <span data-ttu-id="6be22-119">Eikite į „Retail and Commerce“ > Kanalo sąranka > PVM > PVM perrašymai.</span><span class="sxs-lookup"><span data-stu-id="6be22-119">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="6be22-120">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="6be22-120">Click New.</span></span>
8. <span data-ttu-id="6be22-121">Lauke PVM perrašymas nurodykite naujo perrašymo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="6be22-121">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="6be22-122">Lauke Aprašas nurodykite perrašymo aprašą.</span><span class="sxs-lookup"><span data-stu-id="6be22-122">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="6be22-123">Nustatykite būseną į Įjungta.</span><span class="sxs-lookup"><span data-stu-id="6be22-123">Set the status to "Enable."</span></span>
11. <span data-ttu-id="6be22-124">Išplėskite arba sutraukite sekciją Perrašymas.</span><span class="sxs-lookup"><span data-stu-id="6be22-124">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="6be22-125">Lauke „Tipas“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="6be22-125">In the Type field, select an option.</span></span>
    * <span data-ttu-id="6be22-126">Prekės PVM grupes galima naudoti norint perrašyti konkrečių grupei priklausančių prekių mokesčius.</span><span class="sxs-lookup"><span data-stu-id="6be22-126">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="6be22-127">Pvz., maisto prekės paprastai apmokestinamos kitaip nei fizinės medžiagos ir tikėtina, kad jos priklauso atskirai PVM grupei.</span><span class="sxs-lookup"><span data-stu-id="6be22-127">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span> <span data-ttu-id="6be22-128">PVM grupės yra mokesčių, kurie taikomi konkrečiam kanalui, grupės.</span><span class="sxs-lookup"><span data-stu-id="6be22-128">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="6be22-129">Pvz., jei kanale vykdoma tiek mažmeninė, „verslo verslui“ prekyba, gali būti naudojamos skirtingos prekių PVM grupės.</span><span class="sxs-lookup"><span data-stu-id="6be22-129">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="6be22-130">Visi taikomi mokesčiai būtų susieti su PVM grupe.</span><span class="sxs-lookup"><span data-stu-id="6be22-130">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="6be22-131">Dabar gali būti pasirinkti mokesčiai Iš ir Į arba Iš mokesčių grupės ir Į mokesčių grupę, kad būtų sukurtas PVM perrašymas.</span><span class="sxs-lookup"><span data-stu-id="6be22-131">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span> <span data-ttu-id="6be22-132">Lauke Iš nurodomi mokesčiai arba mokesčių grupė, kurią reikia perrašyti.</span><span class="sxs-lookup"><span data-stu-id="6be22-132">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="6be22-133">Perrašant pagal prekės PVM grupę galima naudoti kitas parinktis nei perrašant pagal PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="6be22-133">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span> <span data-ttu-id="6be22-134">Galima nustatyti, kad PVM perrašymai perrašytų visų operacijų mokesčius arba konkrečių operacijos eilučių mokesčius.</span><span class="sxs-lookup"><span data-stu-id="6be22-134">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="6be22-135">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="6be22-135">Click Save.</span></span>
14. <span data-ttu-id="6be22-136">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="6be22-136">Close the page.</span></span>
15. <span data-ttu-id="6be22-137">Eikite į „Retail and Commerce“ > Kanalo sąranka > PVM > PVM perrašymo grupės.</span><span class="sxs-lookup"><span data-stu-id="6be22-137">Go to Retail and Commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="6be22-138">Atlikdami šį veiksmą jūs priskirsite naujai sukurtą PVM perrašymą PVM perrašymo grupei, priskirtai kanalui „Houston“.</span><span class="sxs-lookup"><span data-stu-id="6be22-138">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="6be22-139">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="6be22-139">Click Edit.</span></span>
17. <span data-ttu-id="6be22-140">Išplėskite arba sutraukite sekciją Sąranka.</span><span class="sxs-lookup"><span data-stu-id="6be22-140">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="6be22-141">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="6be22-141">Click Add.</span></span>
19. <span data-ttu-id="6be22-142">Lauke PVM perrašymas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="6be22-142">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="6be22-143">Sąraše pasirinkite anksčiau sukurtą PVM perrašymą.</span><span class="sxs-lookup"><span data-stu-id="6be22-143">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="6be22-144">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="6be22-144">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="6be22-145">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="6be22-145">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]