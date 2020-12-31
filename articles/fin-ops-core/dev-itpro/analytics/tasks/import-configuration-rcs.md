---
title: (ER) Konfigūracijų importavimas iš RCS
description: Šioje temoje pateikiama informacija apie tai, kaip vartotojas gali importuoti naują ER konfigūracijos versiją iš RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b591df3d384e8dc59646ebb9d0205001db040a55
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684192"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="2ed67-103">(ER) Konfigūracijų importavimas iš RCS</span><span class="sxs-lookup"><span data-stu-id="2ed67-103">(ER) Import configurations from RCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ed67-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo rolę turintis vartotojas gali importuoti naują elektroninių ataskaitų (ER) versiją iš „Microsoft Regulatory Configuration Service“ (RCS).</span><span class="sxs-lookup"><span data-stu-id="2ed67-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="2ed67-105">Šiame pavyzdyje jūs pasirinksite ER konfigūracijos versiją, kuri buvo sukonfigūruota RCS egzemplioriuje, ir importuosite ją į dabartinį tos pačios įmonės („Litware, Inc.“) egzempliorių. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas įmonės naudoja bendrai.</span><span class="sxs-lookup"><span data-stu-id="2ed67-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="2ed67-106">Norint atlikti šiuos veiksmus, pirmiausia reikia atlikti veiksmus, nurodytus temoje [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="2ed67-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="2ed67-107">Norėdami atlikti šiuos veiksmus, taip pat turite turėti prieigą prie RCS egzemplioriaus, kuriame yra bent viena būsenos **Baigta** arba **Bendrinama** konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="2ed67-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="2ed67-108">Eikite į **Organizacijos administravimas** > **Darbo sritys** > **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="2ed67-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="2ed67-109">Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="2ed67-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="2ed67-110">Jei nematote šio konfigūracijos teikėjo, atlikite veiksmus, nurodytus temoje [Sukurti konfigūracijų teikėjus ir juos pažymėti kaip aktyvius](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="2ed67-110">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="2ed67-111">Jei jūsų įmonėje nėra sukonfigūruotos RKS aplinkos, pasirinkite išorinį saitą **Regulatory Services – Configuration** ir vykdykite instrukcijas, kad sukonfigūruotumėte RCS aplinką.</span><span class="sxs-lookup"><span data-stu-id="2ed67-111">If you have no RCS environment provisioned to your company, select **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="2ed67-112">Pasirinkite **Elektroninių ataskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="2ed67-112">Select **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="2ed67-113">Pasirinkite skirtuką **RCS**.</span><span class="sxs-lookup"><span data-stu-id="2ed67-113">Select the **RCS** tab.</span></span> 
6. <span data-ttu-id="2ed67-114">Jei RCS aplinka jūsų įmonėje jau sukonfigūruota, norėdami ją pasiekti naudokite puslapyje pateiktus URL.</span><span class="sxs-lookup"><span data-stu-id="2ed67-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="2ed67-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="2ed67-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="2ed67-116">Užregistruokite naują ER saugyklą.</span><span class="sxs-lookup"><span data-stu-id="2ed67-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="2ed67-117">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="2ed67-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="2ed67-118">Pasirinkite teikėją „Litware, Inc.“.</span><span class="sxs-lookup"><span data-stu-id="2ed67-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="2ed67-119">Pasirinkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="2ed67-119">Select Repositories.</span></span> 
4. <span data-ttu-id="2ed67-120">Pasirinkite Įtraukti ir atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="2ed67-120">Select Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="2ed67-121">Lauke Konfigūracijų saugyklos tipas įveskite „RCS“.</span><span class="sxs-lookup"><span data-stu-id="2ed67-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="2ed67-122">Pasirinkite Kurti saugyklą.</span><span class="sxs-lookup"><span data-stu-id="2ed67-122">Select Create repository.</span></span> 
7. <span data-ttu-id="2ed67-123">Lauke RCS aplinkos rodomas pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="2ed67-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="2ed67-124">Pasirinkite norimą RCS egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="2ed67-124">Select the desired RCS instance.</span></span> <span data-ttu-id="2ed67-125">Galite turėti kelis iš jų.</span><span class="sxs-lookup"><span data-stu-id="2ed67-125">You can have several of them.</span></span> 
9. <span data-ttu-id="2ed67-126">Pasirinkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="2ed67-126">Select OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="2ed67-127">ER konfigūracijų importavimas iš RCS saugyklos</span><span class="sxs-lookup"><span data-stu-id="2ed67-127">Import ER configurations from RCS-based repository</span></span>
1. <span data-ttu-id="2ed67-128">Pasirinkite **Rodyti filtrus**.</span><span class="sxs-lookup"><span data-stu-id="2ed67-128">Select **Show filters**.</span></span> 
2. <span data-ttu-id="2ed67-129">Įveskite filtro reikšmę „RCS“ lauke **Pavadinimas** naudodami filtro operatorių **prasideda**.</span><span class="sxs-lookup"><span data-stu-id="2ed67-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="2ed67-130">Atidarę pažymėtą saugyklą, puslapyje **Prijungimas prie „Regulatory Configuration Services“** pasirinkite saitą **Pasirinkite čia norėdami prijungti prie „Regulatory Configuration Services“**.</span><span class="sxs-lookup"><span data-stu-id="2ed67-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, select **Select here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="2ed67-131">Pasirinkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="2ed67-131">Select **Open**.</span></span> 
5. <span data-ttu-id="2ed67-132">Pasirinkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="2ed67-132">Select **Close**.</span></span> 
6. <span data-ttu-id="2ed67-133">Pasirinkite norimą ER konfigūracijos versiją ir pasirinkite **Importuoti**, kad importuotumėte ją į dabartinį egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="2ed67-133">Select the desired version of ER configuration and select **Import** to bring it in the current instance.</span></span>

