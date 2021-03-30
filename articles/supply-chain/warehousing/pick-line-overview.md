---
title: Mobiliojo įrenginio meniu elemento nustatymas paėmimo eilučių peržiūrai pateikti
description: Šioje temoje paaiškinama, kaip nustatyti, kada visų darbo eilučių sąrašas bus rodomas sandėlio darbuotojams, kurie apdoroja sandėlio darbus mobiliajame įrenginyje. Ši funkcija gali būti naudinga sandėlio darbuotojams, kuriems dažnai reikia peržiūrėti paėmimo eilutes darbo užsakyme, kad jie galėtų optimizuoti savo paėmimų seką.
author: MarkusFogelberg
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 22e724b60ec5cc8bf39a520022f43784d3a328eb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232916"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a><span data-ttu-id="55ce9-104">Mobiliojo įrenginio meniu elemento nustatymas paėmimo eilučių peržiūrai pateikti</span><span class="sxs-lookup"><span data-stu-id="55ce9-104">Set up a mobile device menu item to provide a pick line overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="55ce9-105">Šioje temoje paaiškinama, kaip konfigūruoti pasirinktis, susijusias su mobiliųjų įrenginių meniu elementų, kurie naudojami išrinkimo darbui apdoroti, paėmimo eilutės peržiūra.</span><span class="sxs-lookup"><span data-stu-id="55ce9-105">This topic explains how to configure options that are related to the pick line overview for mobile device menu items that are used to process picking work.</span></span> <span data-ttu-id="55ce9-106">Paėmimo eilutės peržiūra leidžia sandėlio darbuotojams peržiūrėti ir pasirinkti iš visų darbo eilučių, susijusių su jų dabartine užduotimi, sąrašo.</span><span class="sxs-lookup"><span data-stu-id="55ce9-106">The pick line overview lets warehouse workers view and select from a list of all the work lines that are related to their current task.</span></span> <span data-ttu-id="55ce9-107">Ši funkcija gali padėti darbuotojams optimizuoti savo paėmimų seką.</span><span class="sxs-lookup"><span data-stu-id="55ce9-107">This capability can help workers optimize their picking sequence.</span></span> <span data-ttu-id="55ce9-108">Funkcija suteikia pasirinktis, kurios pakeičia standartinį **Praleidimo** mygtuką, kuris leidžia darbuotojams pereiti per eilutes po vieną pagal pastovią eilučių tvarką.</span><span class="sxs-lookup"><span data-stu-id="55ce9-108">The feature provides options that replace the standard **Skip** button that lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="55ce9-109">(Tačiau vis tiek galima naudoti šį mygtuką.)</span><span class="sxs-lookup"><span data-stu-id="55ce9-109">(However, the option to use that button is still available.)</span></span>

<span data-ttu-id="55ce9-110">Administratoriai gali konfigūruoti kiekvieną meniu elementą atskirai, kad galėtų kontroliuoti, kaip, kada ir kur sandėlio programa pateikia paėmimo eilučių peržiūrą.</span><span class="sxs-lookup"><span data-stu-id="55ce9-110">Admins can configure each menu item individually to control how, when, and where the warehouse app presents the pick line overview.</span></span>

## <a name="turn-on-the-work-pick-line-overview-feature"></a><span data-ttu-id="55ce9-111">Darbo paėmimo eilutės apžvalgos funkcijos įjungimas</span><span class="sxs-lookup"><span data-stu-id="55ce9-111">Turn on the Work pick line overview feature</span></span>

<span data-ttu-id="55ce9-112">Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje.</span><span class="sxs-lookup"><span data-stu-id="55ce9-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="55ce9-113">Administratoriai gali naudoti [funkcijų valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) parametrus, kad patikrintų funkcijos būseną ir įjungtų ją, kai reikia.</span><span class="sxs-lookup"><span data-stu-id="55ce9-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="55ce9-114">Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.</span><span class="sxs-lookup"><span data-stu-id="55ce9-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="55ce9-115">**Modulis:** _sandėlio valdymas_</span><span class="sxs-lookup"><span data-stu-id="55ce9-115">**Module:** _Warehouse management_</span></span>
- <span data-ttu-id="55ce9-116">**Funkcijos pavadinimas:** _Darbo paėmimo funkcijos apžvalga_</span><span class="sxs-lookup"><span data-stu-id="55ce9-116">**Feature name:** _Work pick line overview_</span></span>

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a><span data-ttu-id="55ce9-117">Meniu elementų konfigūravimas visų darbo eilučių sąrašui parodyti</span><span class="sxs-lookup"><span data-stu-id="55ce9-117">Configure menu items to show a list of all work lines</span></span>

<span data-ttu-id="55ce9-118">Norėdami nustatyti mobiliojo įrenginio meniu elementą paėmimo eilučių peržiūrai pateikti, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="55ce9-118">To set up a mobile device menu item to provide a pick line overview, follow these steps.</span></span>

1. <span data-ttu-id="55ce9-119">Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Mobiliojo įrenginio meniu elementai**.</span><span class="sxs-lookup"><span data-stu-id="55ce9-119">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="55ce9-120">Pasirinkite arba sukurkite meniu elementą, susijusį su paėmimo darbu ir nustatykite šias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="55ce9-120">Select or create a menu item that is related to picking work, and set the following values:</span></span>

    - <span data-ttu-id="55ce9-121">**Režimas:** *Darbas*</span><span class="sxs-lookup"><span data-stu-id="55ce9-121">**Mode:** *Work*</span></span>
    - <span data-ttu-id="55ce9-122">**Naudoti esamą darbą:** *Taip*</span><span class="sxs-lookup"><span data-stu-id="55ce9-122">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="55ce9-123">**Nurodytas:** *Vartotojo nurodyta* arba *Sistemos nurodyta*</span><span class="sxs-lookup"><span data-stu-id="55ce9-123">**Directed by:** *User directed* or *System directed*</span></span>

    <span data-ttu-id="55ce9-124">Norėdami gauti daugiau informacijos apie tai, kaip kurti meniu elementus ir naudoti įvairius parametrus, galimus **Mobiliojo įrenginio meniu elementų** puslapyje, žr. [Mobiliųjų įrenginių nustatymas sandėlio darbui](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="55ce9-124">For more information about how to create menu items and use the various settings that are available on the **Mobile device menu items** page, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

1. <span data-ttu-id="55ce9-125">„FastTab” skirtuke **Bendra** konfigūruokite šią funkciją nustatydami lauką **Rodyti darbo eilučių sąrašą** į vieną iš šių reikšmių:</span><span class="sxs-lookup"><span data-stu-id="55ce9-125">On the **General** FastTab, configure the feature by setting the **Show work line list** field to one of the following values:</span></span>

    - <span data-ttu-id="55ce9-126">**Rodyti tik pateikus užklausą** – darbuotojai gali pasirinkti peržiūrėti paėmimo eilučių naudodami mygtuką **Praleisti iki** sandėlio programoje.</span><span class="sxs-lookup"><span data-stu-id="55ce9-126">**Show only upon request** – Workers can choose to view the pick line list by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="55ce9-127">**Rodyti kiekvieno paėmimo pradžioje** – darbuotojai mato sąrašą kiekvieną kartą, kai jie pradeda arba baigia paėmimo eilutę.</span><span class="sxs-lookup"><span data-stu-id="55ce9-127">**Show at the start of every pick** – Workers see the list every time that they start or finish a pick line.</span></span> <span data-ttu-id="55ce9-128">Jie taip pat gali peržiūrėti sąrašą dar kartą pasirinkdami mygtuką **Praleisti iki** sandėlio programoje.</span><span class="sxs-lookup"><span data-stu-id="55ce9-128">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="55ce9-129">**Rodyti tik pirmo paėmimo pradžioje** – darbuotojai mato sąrašą kiekvieną kartą pradėdami naują paėmimo darbą, tačiau ne po kiekvienos eilutės.</span><span class="sxs-lookup"><span data-stu-id="55ce9-129">**Show at the start of the first pick only** – Workers see the list every time that they start new picking work, but not after each line.</span></span> <span data-ttu-id="55ce9-130">Jie taip pat gali peržiūrėti sąrašą dar kartą pasirinkdami mygtuką **Praleisti iki** sandėlio programoje.</span><span class="sxs-lookup"><span data-stu-id="55ce9-130">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="55ce9-131">**Niekada nerodyti** – įprastas **Praleisti** mygtukas atsiranda sandėlio programoje, o darbo eilučių sąrašo rodymas išjungiamas.</span><span class="sxs-lookup"><span data-stu-id="55ce9-131">**Never show** – The standard **Skip** button appears in the warehouse app, and display of the work line list is turned off.</span></span> <span data-ttu-id="55ce9-132">Mygtukas **Praleisti** leidžia darbuotojui pereiti per eilutes po vieną pagal pastovią eilučių tvarką.</span><span class="sxs-lookup"><span data-stu-id="55ce9-132">The **Skip** button lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="55ce9-133">Jie taip pat gali pereiti per sąrašą tiek kartų, kiek reikia, kol visos eilutės bus apdorotos.</span><span class="sxs-lookup"><span data-stu-id="55ce9-133">They can also cycle through the list as many times as they require, until all lines have been processed.</span></span>

1. <span data-ttu-id="55ce9-134">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="55ce9-134">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="55ce9-135">Jei nustatote lauką **Rodyti darbo eilučių sąrašą** kaip bet kokią reikšmę, išskyrus *Niekada nerodyti*, mygtukas **Laukų sąrašas** tampa pasiekiamas veiksmų srityje.</span><span class="sxs-lookup"><span data-stu-id="55ce9-135">If you set the **Show work line list** field to any value except *Never show*, the **Field list** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="55ce9-136">Veiksmų srityje pasirinkite **Laukų sąrašas**.</span><span class="sxs-lookup"><span data-stu-id="55ce9-136">On the Action Pane, select **Field list**.</span></span>
1. <span data-ttu-id="55ce9-137">Puslapyje **Laukų sąrašas** konfigūruokite informaciją, kurią kiekvienai sąrašo eilutei nurodo sandėlio programa.</span><span class="sxs-lookup"><span data-stu-id="55ce9-137">On the **Field list** page, configure the information that the warehouse app shows for each line in the list.</span></span>

    - <span data-ttu-id="55ce9-138">Laukas **Pagrindinis valdiklis** visada nustatomas į *LineNum*.</span><span class="sxs-lookup"><span data-stu-id="55ce9-138">The **Primary control** field is always set to *LineNum*.</span></span> <span data-ttu-id="55ce9-139">Todėl kiekviena eilutė sąraše prasideda eilutės numeriu.</span><span class="sxs-lookup"><span data-stu-id="55ce9-139">Therefore, each row in the list begins with a line number.</span></span>
    - <span data-ttu-id="55ce9-140">Naudokite likusius **Rodymo lauko** laukus, norėdami pridėti ne daugiau septynių jums reikalingų papildomų rodymo laukų.</span><span class="sxs-lookup"><span data-stu-id="55ce9-140">Use the remaining **Display field** fields to add up to seven additional display fields, as you require.</span></span> <span data-ttu-id="55ce9-141">Kiekviename lauke **Rodymo laukas** pasirinkite darbo eilutės lauko pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="55ce9-141">In each **Display field** field, select the name of a work line field.</span></span> <span data-ttu-id="55ce9-142">Tada kiekvienoje eilutėje bus rodoma to lauko reikšmė.</span><span class="sxs-lookup"><span data-stu-id="55ce9-142">Each line will then show a value for that field.</span></span> <span data-ttu-id="55ce9-143">Reikšmės bus rodomos tokia tvarka, kurią pasirenkate čia.</span><span class="sxs-lookup"><span data-stu-id="55ce9-143">The values will be shown in the order that you select here.</span></span> <span data-ttu-id="55ce9-144">Galite palikti kai kuriuos **Rodymo lauko** laukus tuščius, jeigu jums nėra reikalingos visos septynios reikšmės.</span><span class="sxs-lookup"><span data-stu-id="55ce9-144">You can leave some of the **Display field** fields blank if you don't require all seven values.</span></span>

1. <span data-ttu-id="55ce9-145">Veiksmų srityje pasirinkite **Įrašyti** ir uždarykite **Laukų sąrašo** puslapį.</span><span class="sxs-lookup"><span data-stu-id="55ce9-145">On the Action Pane, select **Save**, and then close the **Field list** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]