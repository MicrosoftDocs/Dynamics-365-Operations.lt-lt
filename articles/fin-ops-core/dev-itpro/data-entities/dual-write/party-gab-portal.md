---
title: „Power Portal“ naudojimas su šalies duomenų modeliu
description: Šioje temoje aprašomi „Power Portal“ tinklo vaidmenų pakeitimai dėl dvigubo rašymo šalies duomenų modelio.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833095"
---
# <a name="using-power-portal-with-the-party-data-model"></a><span data-ttu-id="995bf-103">„Power Portal“ naudojimas su šalies duomenų modeliu</span><span class="sxs-lookup"><span data-stu-id="995bf-103">Using Power Portal with the Party data model</span></span>

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="995bf-104">Dvigubo rašymo programos instrumentavimo sprendimo 2.0.999.0 vėlesniuose versijose yra įrašo ir visuotinės adresų knygelės, skirti sąskaitų ir kontaktų lentelėms, duomenų modelio keitimai.</span><span class="sxs-lookup"><span data-stu-id="995bf-104">The Dual-write application orchestration solution version 2.0.999.0 and later includes data model changes to party and global address book for the Account and Contact tables.</span></span> <span data-ttu-id="995bf-105">Pakeitimai leidžia atlikti daug ryšių, kurie palaiko išplėstinius verslo scenarijus.</span><span class="sxs-lookup"><span data-stu-id="995bf-105">The changes allow many-to-many relationships that support advanced business scenarios.</span></span> <span data-ttu-id="995bf-106">Šių pakeitimų nepalaiko portalo žiniatinklio vaidmenys, įskaitant klientų portalą, kurie išsiųsti be lango arba kurie prieš įdiegdami dvigubą rašymo programą buvo jūsų aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="995bf-106">These changes are not supported by portal web roles, including the customer portal, that are shipped out-of-the-box or that existed in your environment before you installed dual-write.</span></span> <span data-ttu-id="995bf-107">Kad žiniatinklio vaidmenys veiktų kaip tikėjotės, turėsite sukurti naujus žiniatinklio vaidmenis naudodami naują duomenų modelį.</span><span class="sxs-lookup"><span data-stu-id="995bf-107">For the web roles to work as expected, you need to create new web roles using the new data model.</span></span> 

<span data-ttu-id="995bf-108">Apibendrinant, kokiu būdu lentelės sąveikauja, bet kliento portale lentelės teisės nepasikeitė.</span><span class="sxs-lookup"><span data-stu-id="995bf-108">In summary, the way the tables interact has changed, but the table permissions in the customer portal haven't changed.</span></span> <span data-ttu-id="995bf-109">Šioje temoje paaiškinama, kaip sukurti naujus žiniatinklio vaidmenis, kurie veikia su naujuoju išplėstiniu duomenų modeliu.</span><span class="sxs-lookup"><span data-stu-id="995bf-109">This topic explains how to create new web roles that work with the new advanced data model.</span></span>

<span data-ttu-id="995bf-110">Šioje diagramoje rodomas lentelės ryšys **be šalies ir visuotinės adresų** knygelės duomenų modelio:</span><span class="sxs-lookup"><span data-stu-id="995bf-110">This diagram shows the table relationship **without** the party and global address book data model:</span></span>

   ![Be šalies modelio](media/without-party-model.PNG)

<span data-ttu-id="995bf-112">Šioje diagramoje rodomas lentelės ryšys **su šalies ir visuotinės adresų** knygelės duomenų modeliu:</span><span class="sxs-lookup"><span data-stu-id="995bf-112">This diagram shows the table relationship **with** the party and global address book data model:</span></span>

   ![su šalies modeliu](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a><span data-ttu-id="995bf-114">Kurti naują lentelės teisę</span><span class="sxs-lookup"><span data-stu-id="995bf-114">Create a new table permission</span></span>

<span data-ttu-id="995bf-115">Norėdami sukurti šias naujas lentelės teises, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="995bf-115">To create these new table permissions, follow these steps:</span></span>

1. <span data-ttu-id="995bf-116">Prisiregistruokite [„Power Apps“](https://make.powerapps.com) ir eikite į programėles.</span><span class="sxs-lookup"><span data-stu-id="995bf-116">Sign in to [Power Apps](https://make.powerapps.com), and go to your apps.</span></span>
2. <span data-ttu-id="995bf-117">Pasirinkite savo portalo valdymo programą.</span><span class="sxs-lookup"><span data-stu-id="995bf-117">Select your Portal Management app.</span></span>
3. <span data-ttu-id="995bf-118">Šoninioje juostoje pasirinkite **Sauga > Lentelės** teisės.</span><span class="sxs-lookup"><span data-stu-id="995bf-118">In the side bar, select **Security > Table permissions**.</span></span>

    <span data-ttu-id="995bf-119">Turite sukurti tris naujas teises:</span><span class="sxs-lookup"><span data-stu-id="995bf-119">You must create three new permissions:</span></span>

    + <span data-ttu-id="995bf-120">Kontakto ryšys su šalimi</span><span class="sxs-lookup"><span data-stu-id="995bf-120">Contact to Party connection</span></span>
    + <span data-ttu-id="995bf-121">Šalies ryšys su paskyra</span><span class="sxs-lookup"><span data-stu-id="995bf-121">Party to Account connection</span></span>
    + <span data-ttu-id="995bf-122">Paskyros ryšys su užsakymu</span><span class="sxs-lookup"><span data-stu-id="995bf-122">Account to Order connection</span></span>

4. <span data-ttu-id="995bf-123">Sukurkite ir įrašykite naują kontakto įrašo ryšio teisę, nustatydami šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="995bf-123">Create and save a new permission for the Contact to Party connection, setting these parameters:</span></span>

    + <span data-ttu-id="995bf-124">**Pavadinimas**: sąskaitos ryšio šalis (arba jūsų pasirinkimas)</span><span class="sxs-lookup"><span data-stu-id="995bf-124">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="995bf-125">**Lentelės** pavadinimas: msdyn_contactforparty</span><span class="sxs-lookup"><span data-stu-id="995bf-125">**Table Name**: msdyn_contactforparty</span></span>
    + <span data-ttu-id="995bf-126">**Svetainė**: Kliento portalas</span><span class="sxs-lookup"><span data-stu-id="995bf-126">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="995bf-127">**Tikslas**: kontaktas</span><span class="sxs-lookup"><span data-stu-id="995bf-127">**Scope**: Contact</span></span>
    + <span data-ttu-id="995bf-128">**Teisės**: pasirinkti viską</span><span class="sxs-lookup"><span data-stu-id="995bf-128">**Privileges**: Select all</span></span>
    + <span data-ttu-id="995bf-129">**Žiniatinklio** vaidmenys: autentifikuoti vartotojai, klientų atstovas (arba jūsų pasirinkimas)</span><span class="sxs-lookup"><span data-stu-id="995bf-129">**Web roles**: Authenticated Users, Customer Representative (or your choice)</span></span>

5. <span data-ttu-id="995bf-130">Sukurkite ir įrašykite naują kontakto šalies su paskyra ryšio teisę, nustatydami šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="995bf-130">Create and save a new permission for the Party to Account connection, setting these parameters:</span></span>

    + <span data-ttu-id="995bf-131">**Pavadinimas**: sąskaitos ryšio šalis (arba jūsų pasirinkimas)</span><span class="sxs-lookup"><span data-stu-id="995bf-131">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="995bf-132">**Lentelės** pavadinimas: sąskaita</span><span class="sxs-lookup"><span data-stu-id="995bf-132">**Table Name**: account</span></span>
    + <span data-ttu-id="995bf-133">**Svetainė**: Kliento portalas</span><span class="sxs-lookup"><span data-stu-id="995bf-133">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="995bf-134">**Tikslas**: pirminė</span><span class="sxs-lookup"><span data-stu-id="995bf-134">**Scope**: Parent</span></span>
    + <span data-ttu-id="995bf-135">**Teisės**: pasirinkti viską</span><span class="sxs-lookup"><span data-stu-id="995bf-135">**Privileges**: Select all</span></span>
    + <span data-ttu-id="995bf-136">**Pirminės lentelės** teisės: kontakto į šalies ryšį</span><span class="sxs-lookup"><span data-stu-id="995bf-136">**Parent Table Permission**: Contact to Party Connection</span></span>

6. <span data-ttu-id="995bf-137">Sukurkite ir įrašykite naują kontakto paskyros su užsakymu ryšio teisę, nustatydami šiuos parametrus:</span><span class="sxs-lookup"><span data-stu-id="995bf-137">Create and save a new permission for the Account to Order connection, setting these parameters:</span></span>

    + <span data-ttu-id="995bf-138">**Pavadinimas**: paskyros su užsakymo ryšys (arba jūsų pasirinkimas)</span><span class="sxs-lookup"><span data-stu-id="995bf-138">**Name**: Account to Order Connection (or your choice)</span></span>
    + <span data-ttu-id="995bf-139">**Lentelės** pavadinimas: pardavimo užsakymas</span><span class="sxs-lookup"><span data-stu-id="995bf-139">**Table Name**: salesorder</span></span>
    + <span data-ttu-id="995bf-140">**Svetainė**: Kliento portalas</span><span class="sxs-lookup"><span data-stu-id="995bf-140">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="995bf-141">**Tikslas**: pirminė</span><span class="sxs-lookup"><span data-stu-id="995bf-141">**Scope**: Parent</span></span>
    + <span data-ttu-id="995bf-142">**Teisės**: pasirinkti viską</span><span class="sxs-lookup"><span data-stu-id="995bf-142">**Privileges**: Select all</span></span>
    + <span data-ttu-id="995bf-143">**Pirminės lentelės** teisės: šalies su paskyra ryšys</span><span class="sxs-lookup"><span data-stu-id="995bf-143">**Parent Table Permission**: Party to Account Connection</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
