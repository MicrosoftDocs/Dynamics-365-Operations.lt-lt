---
title: "Planavimas, kaip konfigūruoti visuotinę adresų knygelę ir papildomas adresų knygeles"
description: "Šioje temoje aprašomos aplinkybės ir sprendimai, kuriuos turite priimti planavimo proceso metu prieš nustatydami ir konfigūruodami visuotinę adresų knygelę ir bet kokias papildomas adresų knygeles programoje „Microsoft Dynamics 365 for Finance and Operations“. Dėl kai kurių sprendimų reikės patvirtinti sprendimus, kurie buvo atlikti kitose produkto srityse, pvz., organizacijos hierarchijoje."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shiva.pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b872603f987b72faacc0a987aa44c31e773636f8
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="plan-how-to-configure-the-global-address-book-and-additional-address-books"></a><span data-ttu-id="02667-104">Planavimas, kaip konfigūruoti visuotinę adresų knygelę ir papildomas adresų knygeles</span><span class="sxs-lookup"><span data-stu-id="02667-104">Plan how to configure the global address book and additional address books</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="02667-105">Šioje temoje aprašomos aplinkybės ir sprendimai, kuriuos turite priimti planavimo proceso metu prieš nustatydami ir konfigūruodami visuotinę adresų knygelę ir bet kokias papildomas adresų knygeles programoje „Microsoft Dynamics 365 for Finance and Operations“.</span><span class="sxs-lookup"><span data-stu-id="02667-105">This topic describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="02667-106">Dėl kai kurių sprendimų reikės patvirtinti sprendimus, kurie buvo atlikti kitose produkto srityse, pvz., organizacijos hierarchijoje.</span><span class="sxs-lookup"><span data-stu-id="02667-106">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

<a name="global-address-book"></a><span data-ttu-id="02667-107">Visuotinė adresų knygelė</span><span class="sxs-lookup"><span data-stu-id="02667-107">Global address book</span></span>
-------------------

<span data-ttu-id="02667-108">Prieš pradėdami dirbti su visuotine adresų knygele, turite nustatyti numatytąsias jos reikšmes.</span><span class="sxs-lookup"><span data-stu-id="02667-108">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="02667-109">Šios numatytosios reikšmės tada naudojamos bet kokioms papildomoms jūsų sukurtoms adresų knygelėms.</span><span class="sxs-lookup"><span data-stu-id="02667-109">These default values are then used for any additional address books that you create.</span></span> 

<span data-ttu-id="02667-110">**Sprendimai:**</span><span class="sxs-lookup"><span data-stu-id="02667-110">**Decisions:**</span></span>

-   <span data-ttu-id="02667-111">Kokia seka turėtų būti rodomi **Asmens** tipo šalių įrašų vardai ir pavardės?</span><span class="sxs-lookup"><span data-stu-id="02667-111">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="02667-112">Pavyzdžiui, viena seka yra pavardė, antras vardas, vardas.</span><span class="sxs-lookup"><span data-stu-id="02667-112">For example, one sequence is last name, middle name, first name.</span></span>
-   <span data-ttu-id="02667-113">Ar, panaikinus vaidmens įrašą, iš adresų knygelės turėtų būti panaikinti šalių įrašai?</span><span class="sxs-lookup"><span data-stu-id="02667-113">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="02667-114">Pavyzdžiui, jei panaikinamas kliento įrašas, ar taip pat turėtų būti panaikintas šalies įrašas?</span><span class="sxs-lookup"><span data-stu-id="02667-114">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
-   <span data-ttu-id="02667-115">Ar, kuriant naują įrašą, naudotojams turėtų būti pranešama, jei visuotinėje adresų knygelėje aptinkamas besidubliuojantis įrašas?</span><span class="sxs-lookup"><span data-stu-id="02667-115">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
-   <span data-ttu-id="02667-116">Ar į šalies įrašo informaciją turėtų būti įtrauktas Duomenų universaliosios numeravimo sistemos (DUNS) numeris?</span><span class="sxs-lookup"><span data-stu-id="02667-116">Should the Data Universal Numbering System (DUNS) number be included in a party record’s information?</span></span>
-   <span data-ttu-id="02667-117">Jei DUNS numeris įtraukiamas į šalies įrašą, ar turėtų būti tikrinamas numerio unikalumas?</span><span class="sxs-lookup"><span data-stu-id="02667-117">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
-   <span data-ttu-id="02667-118">Kai visuotinėje adresų knygelėje kuriamas šalies įrašas, ar norite nustatyti numatytąjį įrašo tipą, asmens arba organizacijos?</span><span class="sxs-lookup"><span data-stu-id="02667-118">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
-   <span data-ttu-id="02667-119">Kokie naudotojo vaidmenys turėtų turėti prieigą prie šalių įrašų privačios adresų ir kontaktinės informacijos?</span><span class="sxs-lookup"><span data-stu-id="02667-119">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="02667-120">Papildomos adresų knygelės</span><span class="sxs-lookup"><span data-stu-id="02667-120">Additional address books</span></span>
<span data-ttu-id="02667-121">Sukūrę visuotinę adresų knygelę, pagal poreikį galite kurti papildomų adresų knygelių, pvz., atskirą adresų knygelę kiekvienai jūsų organizacijos įmonei ar kiekvienai verslo šakai.</span><span class="sxs-lookup"><span data-stu-id="02667-121">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="02667-122">Pavyzdžiui, „Fabrikam‟ yra tarptautinė organizacija, kuri turi kelias įmones ir dalyvauja keliose verslo šakose.</span><span class="sxs-lookup"><span data-stu-id="02667-122">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="02667-123">„Fabrikam‟ planuoja sukurti kiekvienos verslo šakos adresų knygelę.</span><span class="sxs-lookup"><span data-stu-id="02667-123">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="02667-124">Tų verslo šakų, kurių veikla vykdoma daugiau nei vienoje vietoje, pvz., pneumatinių įrankių verslo, „Fabrikam‟ planuoja sukurti kiekvienos vietos adresų knygelę.</span><span class="sxs-lookup"><span data-stu-id="02667-124">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="02667-125">Chrisas, „Fabrikam‟ IT vadovas, sukūrė toliau pateiktą reikiamų adresų knygelių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="02667-125">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="02667-126">Šiame sąraše taip pat aprašomi šalių įrašai, kurie turi būti kiekvienoje adresų knygelėje.</span><span class="sxs-lookup"><span data-stu-id="02667-126">This list also describes the party records that each address book must include.</span></span>

-   <span data-ttu-id="02667-127">**Viešojo sektoriaus sutartys (PubSC)** – visų šalių, kurios susijusios su „Fabrikam‟ turimomis viešojo sektoriaus sutartimis, įrašai.</span><span class="sxs-lookup"><span data-stu-id="02667-127">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
-   <span data-ttu-id="02667-128">**Privačiojo sektoriaus sutartys (PriSC)** – visų šalių, kurios susijusios su „Fabrikam‟ turimomis privačiojo sektoriaus sutartimis, įrašai.</span><span class="sxs-lookup"><span data-stu-id="02667-128">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
-   <span data-ttu-id="02667-129">**Elektroniniai įrankiai (ET)** – visų šalių, dalyvaujančių perkant ar parduodant elektroninius įrankius, ar kitaip sąveikaujančių su elektroniniais įrankiais, kuriuos teikia „Fabrikam‟ „Fabrikam-Japan‟ įmonėje, arba kurie jai nuperkami, įrašai.</span><span class="sxs-lookup"><span data-stu-id="02667-129">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
-   <span data-ttu-id="02667-130">**Pneumatiniai įrankiai (PTJPN)** – visų šalių, dalyvaujančių perkant ar parduodant pneumatinius įrankius, ar kitaip sąveikaujančių su pneumatiniais įrankiais, kuriuos teikia „Fabrikam‟ „Fabrikam-Japan‟ įmonėje, arba kurie jai nuperkami, įrašai.</span><span class="sxs-lookup"><span data-stu-id="02667-130">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
-   <span data-ttu-id="02667-131">**Pneumatiniai įrankiai (PTUSA)** – visų šalių, dalyvaujančių perkant ar parduodant pneumatinius įrankius, ar kitaip sąveikaujančių su pneumatiniais įrankiais, kuriuos teikia „Fabrikam‟ „Fabrikam-US‟ įmonėje, arba kurie jai nuperkami, įrašai.</span><span class="sxs-lookup"><span data-stu-id="02667-131">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="02667-132">**Sprendimas:**</span><span class="sxs-lookup"><span data-stu-id="02667-132">**Decision:**</span></span>

-   <span data-ttu-id="02667-133">Kiek sukursite papildomų adresų knygelių?</span><span class="sxs-lookup"><span data-stu-id="02667-133">How many additional address books will you create?</span></span>

### <a name="address-book-security"></a><span data-ttu-id="02667-134">Adresų knygelių sauga</span><span class="sxs-lookup"><span data-stu-id="02667-134">Address book security</span></span>

<span data-ttu-id="02667-135">Kurti adresų knygeles galite bet kuriuo metu ir taip pat bet kuriuo metu galite nustatyti adresų knygelių saugos parametrus.</span><span class="sxs-lookup"><span data-stu-id="02667-135">You can create address books at any time, and you can also set security parameters for the address books at any time.</span></span> <span data-ttu-id="02667-136">Nebūtina nustatyti adresų knygelės saugos teisių, tačiau, jei to nepadarysite, visi jūsų organizacijos darbuotojai galės peržiūrėti visus tos adresų knygelės šalių įrašus.</span><span class="sxs-lookup"><span data-stu-id="02667-136">You aren't required to set security privileges for an address book, but if you don't, all workers in your organization can view all party records in that address book.</span></span> <span data-ttu-id="02667-137">Saugos teises į šalių įrašus galite nustatyti adresų knygelėse.</span><span class="sxs-lookup"><span data-stu-id="02667-137">You can set security privileges to party records through address books.</span></span> <span data-ttu-id="02667-138">Saugos teisės paremtos komandomis.</span><span class="sxs-lookup"><span data-stu-id="02667-138">Security privileges are based on teams.</span></span> <span data-ttu-id="02667-139">Šiuo būdu garantuojama, kad adresų knygelės šalių įrašus galėtų peržiūrėti tik tie darbuotojai, kurie priskirti komandai, turinčiai prieigą prie tos adresų knygelės.</span><span class="sxs-lookup"><span data-stu-id="02667-139">This approach guarantees that only workers who are assigned to a team that has access to an address book can view the party records in that address book.</span></span> <span data-ttu-id="02667-140">Turite pasirinkti komandas, turinčias prieigą prie kiekvienos adresų knygelės.</span><span class="sxs-lookup"><span data-stu-id="02667-140">You must select the teams that have access to each address book.</span></span> <span data-ttu-id="02667-141">Galite nustatyti kiekvienos adresų knygelės saugos teises, leidžiančias arba draudžiančias konkrečių komandų prieigą.</span><span class="sxs-lookup"><span data-stu-id="02667-141">For each address book, you can set security privileges that allow or deny access to specific teams.</span></span> <span data-ttu-id="02667-142">Jei komandai suteikiate adresų knygelės teises, visi tos komandos nariai gali peržiūrėti adresų knygelės įrašus.</span><span class="sxs-lookup"><span data-stu-id="02667-142">If you grant a team privileges to an address book, all members of that team can view the records in the address book.</span></span> <span data-ttu-id="02667-143">Jei komandai prieigos prie adresų knygelės nesuteikiate, tos komandos nariai peržiūrėti adresų knygelės ar jos turinio negali.</span><span class="sxs-lookup"><span data-stu-id="02667-143">If you don't grant a team access to an address book, the members of that team can't view the address book or its contents.</span></span> 

<span data-ttu-id="02667-144">**Sprendimas:**</span><span class="sxs-lookup"><span data-stu-id="02667-144">**Decision:**</span></span>

-   <span data-ttu-id="02667-145">Kurios komandos turėtų turėti prieigą prie kiekvienos naujos jūsų sukurtos adresų knygelės?</span><span class="sxs-lookup"><span data-stu-id="02667-145">Which teams should have access to each new address book that you will create?</span></span>





