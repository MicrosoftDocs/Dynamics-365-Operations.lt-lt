--- 
title: "PVM priskyrimas ir perrašymai"
description: "Šioje procedūroje parodoma, kaip PVM grupes priskirti mažmeninės prekybos kanalams."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 8b3dc0beec17d80f7bbbcf234656a537a445789f
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---
# <a name="sales-tax-assignment-and-overrides"></a><span data-ttu-id="bbc74-103">PVM priskyrimas ir perrašymai</span><span class="sxs-lookup"><span data-stu-id="bbc74-103">Sales tax assignment and overrides</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bbc74-104">Šioje procedūroje parodoma, kaip PVM grupes priskirti mažmeninės prekybos kanalams.</span><span class="sxs-lookup"><span data-stu-id="bbc74-104">This procedure demonstrates how to assign sales tax groups to retail channels.</span></span> <span data-ttu-id="bbc74-105">Joje taip pat paaiškinamas procesas, kurio metu sukuriamas naujas PVM perrašymas ir priskiriamas esamai PVM perrašymo grupei.</span><span class="sxs-lookup"><span data-stu-id="bbc74-105">It also walks through the process of creating a new sales tax override and assigning it to an existing sales tax override group.</span></span> <span data-ttu-id="bbc74-106">Šiai procedūrai</span><span class="sxs-lookup"><span data-stu-id="bbc74-106">This procedure</span></span>

<span data-ttu-id="bbc74-107">naudojama įmonė USRT demonstraciniams duomenims.</span><span class="sxs-lookup"><span data-stu-id="bbc74-107">uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="bbc74-108">Eikite į Mažmeninė prekyba ir prekyba > Kanalai > Mažmeninės prekybos parduotuvės > Visos mažmeninės prekybos parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="bbc74-108">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
2. <span data-ttu-id="bbc74-109">Sąraše spustelėkite „Houston“ saitą Mažmeninės prekybos kanalo ID.</span><span class="sxs-lookup"><span data-stu-id="bbc74-109">In the list, click the Retail Channel ID link for "Houston."</span></span>
3. <span data-ttu-id="bbc74-110">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="bbc74-110">Click Edit.</span></span>
    * <span data-ttu-id="bbc74-111">Lauke PVM grupė pateikiamas dabartinės įmonės PVM grupių sąrašas.</span><span class="sxs-lookup"><span data-stu-id="bbc74-111">The "Sales tax group" field contains the list of sales tax groups for the current company.</span></span> <span data-ttu-id="bbc74-112">Šiuo metu priskirta grupė yra bendroji PVM grupė „Texas“.</span><span class="sxs-lookup"><span data-stu-id="bbc74-112">The currently assigned group is a generic "Texas" sales tax group.</span></span> <span data-ttu-id="bbc74-113">Taip pat galimos PVM grupės „Washington“ ir „Washington, King County“.</span><span class="sxs-lookup"><span data-stu-id="bbc74-113">There are also sales tax groups for "Washington" and "Washington, King County."</span></span> <span data-ttu-id="bbc74-114">PVM grupės gali apimti keliose savivaldybėse taikomus mokesčius.</span><span class="sxs-lookup"><span data-stu-id="bbc74-114">Sales tax groups can include applicable taxes for multiple municipalities.</span></span>  
    * <span data-ttu-id="bbc74-115">Lauke PVM perrašymas PVM perrašymo grupes galima susieti su kanalu.</span><span class="sxs-lookup"><span data-stu-id="bbc74-115">The "Sales tax override" field is where sales tax override groups can be mapped to the channel.</span></span> <span data-ttu-id="bbc74-116">PVM perrašymo grupes galima naudoti norint grupuoti PVM perrašymus, taikomus kelioms parduotuvėms.</span><span class="sxs-lookup"><span data-stu-id="bbc74-116">Sales tax override groups can be used to group together sales tax overrides that work for multiple stores.</span></span> <span data-ttu-id="bbc74-117">Užuot neautomatiniu būdu priskyrus atskirus PVM perrašymus, galima sutaupyti laiko sukuriant grupę ir ją tiesiogiai priskiriant kanalams.</span><span class="sxs-lookup"><span data-stu-id="bbc74-117">Rather than manually assigning sales tax overrides one by one, the group can be created and assigned directly to the channels to save time.</span></span>  
4. <span data-ttu-id="bbc74-118">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bbc74-118">Click Save.</span></span>
5. <span data-ttu-id="bbc74-119">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bbc74-119">Close the page.</span></span>
6. <span data-ttu-id="bbc74-120">Pasirinkite Mažmeninė prekyba ir prekyba > Kanalo sąranka > PVM > PVM perrašymai.</span><span class="sxs-lookup"><span data-stu-id="bbc74-120">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax overrides.</span></span>
7. <span data-ttu-id="bbc74-121">Spustelėkite Naujas.</span><span class="sxs-lookup"><span data-stu-id="bbc74-121">Click New.</span></span>
8. <span data-ttu-id="bbc74-122">Lauke PVM perrašymas nurodykite naujo perrašymo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="bbc74-122">In the Sales tax override field, provide a name for your new override.</span></span>
9. <span data-ttu-id="bbc74-123">Lauke Aprašas nurodykite perrašymo aprašą.</span><span class="sxs-lookup"><span data-stu-id="bbc74-123">In the Description field, provide a description of the override.</span></span>
10. <span data-ttu-id="bbc74-124">Nustatykite būseną į Įjungta.</span><span class="sxs-lookup"><span data-stu-id="bbc74-124">Set the status to "Enable."</span></span>
11. <span data-ttu-id="bbc74-125">Išplėskite arba sutraukite sekciją Perrašymas.</span><span class="sxs-lookup"><span data-stu-id="bbc74-125">Expand or collapse the Override section.</span></span>
12. <span data-ttu-id="bbc74-126">Lauke „Tipas“ pasirinkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="bbc74-126">In the Type field, select an option.</span></span>
    * <span data-ttu-id="bbc74-127">Prekės PVM grupes galima naudoti norint perrašyti konkrečių grupei priklausančių prekių mokesčius.</span><span class="sxs-lookup"><span data-stu-id="bbc74-127">Item sales tax groups can be used to override taxes for specific items that belong to the group.</span></span> <span data-ttu-id="bbc74-128">Pvz., maisto prekės paprastai apmokestinamos kitaip nei fizinės medžiagos ir tikėtina, kad jos priklauso atskirai PVM grupei.</span><span class="sxs-lookup"><span data-stu-id="bbc74-128">For example, food items are typically taxed differently from hard goods, and would likely have their own sales tax group.</span></span>     <span data-ttu-id="bbc74-129">PVM grupės yra mokesčių, kurie taikomi konkrečiam kanalui, grupės.</span><span class="sxs-lookup"><span data-stu-id="bbc74-129">Sales tax groups are groups of taxes that are applicable to a particular channel.</span></span> <span data-ttu-id="bbc74-130">Pvz., jei kanale vykdoma tiek mažmeninė, „verslo verslui“ prekyba, gali būti naudojamos skirtingos prekių PVM grupės.</span><span class="sxs-lookup"><span data-stu-id="bbc74-130">For example, if a channel sells both retail and business-to-business, different items sales tax groups may be used.</span></span> <span data-ttu-id="bbc74-131">Visi taikomi mokesčiai būtų susieti su PVM grupe.</span><span class="sxs-lookup"><span data-stu-id="bbc74-131">All the applicable taxes would be mapped to the sales tax group.</span></span>  
    * <span data-ttu-id="bbc74-132">Dabar gali būti pasirinkti mokesčiai Iš ir Į arba Iš mokesčių grupės ir Į mokesčių grupę, kad būtų sukurtas PVM perrašymas.</span><span class="sxs-lookup"><span data-stu-id="bbc74-132">Now you can select the "From" and "To" taxes or "From tax group" and "To tax group" to create your sales tax override.</span></span>    <span data-ttu-id="bbc74-133">Lauke Iš nurodomi mokesčiai arba mokesčių grupė, kurią reikia perrašyti.</span><span class="sxs-lookup"><span data-stu-id="bbc74-133">The "From" field indicates the tax or tax group to be overridden.</span></span> <span data-ttu-id="bbc74-134">Perrašant pagal prekės PVM grupę galima naudoti kitas parinktis nei perrašant pagal PVM grupę.</span><span class="sxs-lookup"><span data-stu-id="bbc74-134">Overriding by Item sales tax group provides different options than overriding by sales tax group.</span></span>    <span data-ttu-id="bbc74-135">Galima nustatyti, kad PVM perrašymai perrašytų visų operacijų mokesčius arba konkrečių operacijos eilučių mokesčius.</span><span class="sxs-lookup"><span data-stu-id="bbc74-135">Sales tax overrides can be set up to override taxes on entire transactions or on particular lines in the transaction.</span></span>  
13. <span data-ttu-id="bbc74-136">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bbc74-136">Click Save.</span></span>
14. <span data-ttu-id="bbc74-137">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="bbc74-137">Close the page.</span></span>
15. <span data-ttu-id="bbc74-138">Pasirinkite Mažmeninė prekyba ir prekyba > Kanalo sąranka > PVM > PVM perrašymų grupės.</span><span class="sxs-lookup"><span data-stu-id="bbc74-138">Go to Retail and commerce > Channel setup > Sales taxes > Sales tax override groups.</span></span>
    * <span data-ttu-id="bbc74-139">Atlikdami šį veiksmą jūs priskirsite naujai sukurtą PVM perrašymą PVM perrašymo grupei, priskirtai kanalui „Houston“.</span><span class="sxs-lookup"><span data-stu-id="bbc74-139">In this step you will assigned the newly created sales tax override to the sales tax override group assigned to the Houston channel.</span></span>  
16. <span data-ttu-id="bbc74-140">Spustelėkite Redaguoti.</span><span class="sxs-lookup"><span data-stu-id="bbc74-140">Click Edit.</span></span>
17. <span data-ttu-id="bbc74-141">Išplėskite arba sutraukite sekciją Sąranka.</span><span class="sxs-lookup"><span data-stu-id="bbc74-141">Expand or collapse the Setup section.</span></span>
18. <span data-ttu-id="bbc74-142">Spustelėkite Pridėti.</span><span class="sxs-lookup"><span data-stu-id="bbc74-142">Click Add.</span></span>
19. <span data-ttu-id="bbc74-143">Lauke PVM perrašymas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.</span><span class="sxs-lookup"><span data-stu-id="bbc74-143">In the Sales tax override field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="bbc74-144">Sąraše pasirinkite anksčiau sukurtą PVM perrašymą.</span><span class="sxs-lookup"><span data-stu-id="bbc74-144">Select the previously created sales tax override from the list.</span></span>
21. <span data-ttu-id="bbc74-145">Sąraše spustelėkite saitą pasirinktoje eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bbc74-145">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="bbc74-146">Spustelėkite Įrašyti.</span><span class="sxs-lookup"><span data-stu-id="bbc74-146">Click Save.</span></span>


