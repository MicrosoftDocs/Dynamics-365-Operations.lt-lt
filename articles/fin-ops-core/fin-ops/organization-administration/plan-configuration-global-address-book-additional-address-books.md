---
title: Visuotinės adresų knygelės ir kitų adresų knygelių planas
description: Šioje temoje aprašomos aplinkybės ir sprendimai, kuriuos turite priimti planavimo proceso metu prieš nustatydami ir konfigūruodami visuotinę adresų knygelę ir bet kokias papildomas adresų knygeles.
author: msftbrking
manager: AnnBe
ms.date: 01/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f0a53e1f9b378759e0c5adbe0612a5fa8cddc82
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796951"
---
# <a name="plan-for-the-global-address-book-and-other-address-books"></a><span data-ttu-id="4ee60-103">Visuotinės adresų knygelės ir kitų adresų knygelių planavimas</span><span class="sxs-lookup"><span data-stu-id="4ee60-103">Plan for the global address book and other address books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ee60-104">Šioje temoje aprašomos aplinkybės ir sprendimai, kuriuos turite priimti planavimo proceso metu prieš nustatydami ir konfigūruodami visuotinę adresų knygelę ir bet kokias papildomas adresų knygeles.</span><span class="sxs-lookup"><span data-stu-id="4ee60-104">This topic describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books.</span></span> <span data-ttu-id="4ee60-105">Dėl kai kurių sprendimų reikės patvirtinti sprendimus, kurie buvo atlikti kitose produkto srityse, pvz., organizacijos hierarchijoje.</span><span class="sxs-lookup"><span data-stu-id="4ee60-105">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

## <a name="global-address-book"></a><span data-ttu-id="4ee60-106">Visuotinė adresų knygelė</span><span class="sxs-lookup"><span data-stu-id="4ee60-106">Global address book</span></span>

<span data-ttu-id="4ee60-107">Prieš pradėdami dirbti su visuotine adresų knygele, turite nustatyti numatytąsias jos reikšmes.</span><span class="sxs-lookup"><span data-stu-id="4ee60-107">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="4ee60-108">Šios numatytosios reikšmės tada naudojamos bet kokioms papildomoms jūsų sukurtoms adresų knygelėms.</span><span class="sxs-lookup"><span data-stu-id="4ee60-108">These default values are then used for any additional address books that you create.</span></span>

<span data-ttu-id="4ee60-109">**Sprendimai**</span><span class="sxs-lookup"><span data-stu-id="4ee60-109">**Decisions**</span></span>

- <span data-ttu-id="4ee60-110">Kokia seka turėtų būti rodomi **Asmens** tipo šalių įrašų vardai ir pavardės?</span><span class="sxs-lookup"><span data-stu-id="4ee60-110">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="4ee60-111">Pavyzdžiui, viena seka yra pavardė, antras vardas, vardas.</span><span class="sxs-lookup"><span data-stu-id="4ee60-111">For example, one sequence is last name, middle name, first name.</span></span>
- <span data-ttu-id="4ee60-112">Ar, panaikinus vaidmens įrašą, iš adresų knygelės turėtų būti panaikinti šalių įrašai?</span><span class="sxs-lookup"><span data-stu-id="4ee60-112">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="4ee60-113">Pavyzdžiui, jei panaikinamas kliento įrašas, ar taip pat turėtų būti panaikintas šalies įrašas?</span><span class="sxs-lookup"><span data-stu-id="4ee60-113">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
- <span data-ttu-id="4ee60-114">Ar, kuriant naują įrašą, naudotojams turėtų būti pranešama, jei visuotinėje adresų knygelėje aptinkamas besidubliuojantis įrašas?</span><span class="sxs-lookup"><span data-stu-id="4ee60-114">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
- <span data-ttu-id="4ee60-115">Ar į šalies įrašo informaciją turėtų būti įtrauktas Duomenų universaliosios numeravimo sistemos (DUNS) numeris?</span><span class="sxs-lookup"><span data-stu-id="4ee60-115">Should the Data Universal Numbering System (DUNS) number be included in a party record's information?</span></span>
- <span data-ttu-id="4ee60-116">Jei DUNS numeris įtraukiamas į šalies įrašą, ar turėtų būti tikrinamas numerio unikalumas?</span><span class="sxs-lookup"><span data-stu-id="4ee60-116">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
- <span data-ttu-id="4ee60-117">Kai visuotinėje adresų knygelėje kuriamas šalies įrašas, ar norite nustatyti numatytąjį įrašo tipą, asmens arba organizacijos?</span><span class="sxs-lookup"><span data-stu-id="4ee60-117">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
- <span data-ttu-id="4ee60-118">Kokie naudotojo vaidmenys turėtų turėti prieigą prie šalių įrašų privačios adresų ir kontaktinės informacijos?</span><span class="sxs-lookup"><span data-stu-id="4ee60-118">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="4ee60-119">Papildomos adresų knygelės</span><span class="sxs-lookup"><span data-stu-id="4ee60-119">Additional address books</span></span>

<span data-ttu-id="4ee60-120">Sukūrę visuotinę adresų knygelę, pagal poreikį galite kurti papildomų adresų knygelių, pvz., atskirą adresų knygelę kiekvienai jūsų organizacijos įmonei ar kiekvienai verslo šakai.</span><span class="sxs-lookup"><span data-stu-id="4ee60-120">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="4ee60-121">Pavyzdžiui, „Fabrikam‟ yra tarptautinė organizacija, kuri turi kelias įmones ir dalyvauja keliose verslo šakose.</span><span class="sxs-lookup"><span data-stu-id="4ee60-121">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="4ee60-122">„Fabrikam‟ planuoja sukurti kiekvienos verslo šakos adresų knygelę.</span><span class="sxs-lookup"><span data-stu-id="4ee60-122">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="4ee60-123">Tų verslo šakų, kurių veikla vykdoma daugiau nei vienoje vietoje, pvz., pneumatinių įrankių verslo, „Fabrikam‟ planuoja sukurti kiekvienos vietos adresų knygelę.</span><span class="sxs-lookup"><span data-stu-id="4ee60-123">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="4ee60-124">Chrisas, „Fabrikam‟ IT vadovas, sukūrė toliau pateiktą reikiamų adresų knygelių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="4ee60-124">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="4ee60-125">Šiame sąraše taip pat aprašomi šalių įrašai, kurie turi būti kiekvienoje adresų knygelėje.</span><span class="sxs-lookup"><span data-stu-id="4ee60-125">This list also describes the party records that each address book must include.</span></span>

- <span data-ttu-id="4ee60-126">**Viešojo sektoriaus sutartys (PubSC)** – visų šalių, kurios susijusios su „Fabrikam‟ turimomis viešojo sektoriaus sutartimis, įrašai.</span><span class="sxs-lookup"><span data-stu-id="4ee60-126">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="4ee60-127">**Privačiojo sektoriaus sutartys (PriSC)** – visų šalių, kurios susijusios su „Fabrikam‟ turimomis privačiojo sektoriaus sutartimis, įrašai.</span><span class="sxs-lookup"><span data-stu-id="4ee60-127">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
- <span data-ttu-id="4ee60-128">**Elektroniniai įrankiai (ET)** – visų šalių, dalyvaujančių perkant ar parduodant elektroninius įrankius, ar kitaip sąveikaujančių su elektroniniais įrankiais, kuriuos teikia „Fabrikam‟ „Fabrikam-Japan‟ įmonėje, arba kurie jai nuperkami, įrašai.</span><span class="sxs-lookup"><span data-stu-id="4ee60-128">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="4ee60-129">**Pneumatiniai įrankiai (PTJPN)** – visų šalių, dalyvaujančių perkant ar parduodant pneumatinius įrankius, ar kitaip sąveikaujančių su pneumatiniais įrankiais, kuriuos teikia „Fabrikam‟ „Fabrikam-Japan‟ įmonėje, arba kurie jai nuperkami, įrašai.</span><span class="sxs-lookup"><span data-stu-id="4ee60-129">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
- <span data-ttu-id="4ee60-130">**Pneumatiniai įrankiai (PTUSA)** – visų šalių, dalyvaujančių perkant ar parduodant pneumatinius įrankius, ar kitaip sąveikaujančių su pneumatiniais įrankiais, kuriuos teikia „Fabrikam‟ „Fabrikam-US‟ įmonėje, arba kurie jai nuperkami, įrašai.</span><span class="sxs-lookup"><span data-stu-id="4ee60-130">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="4ee60-131">**Sprendimas:**</span><span class="sxs-lookup"><span data-stu-id="4ee60-131">**Decision:**</span></span>

- <span data-ttu-id="4ee60-132">Kiek sukursite papildomų adresų knygelių?</span><span class="sxs-lookup"><span data-stu-id="4ee60-132">How many additional address books will you create?</span></span>
