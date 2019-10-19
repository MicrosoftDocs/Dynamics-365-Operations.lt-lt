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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32c9c17d8b63e4c0806559c2dcc2e11ae9825a53
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184628"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="76d29-103">(ER) Konfigūracijų importavimas iš RCS</span><span class="sxs-lookup"><span data-stu-id="76d29-103">(ER) Import configurations from RCS</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76d29-104">Šie veiksmai paaiškina, kaip sistemos administratoriaus arba elektroninių ataskaitų kūrėjo rolę turintis vartotojas gali importuoti naują elektroninių ataskaitų (ER) versiją iš „Microsoft Regulatory Configuration Service“ (RCS).</span><span class="sxs-lookup"><span data-stu-id="76d29-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="76d29-105">Šiame pavyzdyje jūs pasirinksite ER konfigūracijos versiją, kuri buvo sukonfigūruota RCS egzemplioriuje, ir importuosite ją į dabartinį tos pačios įmonės („Litware, Inc.“) egzempliorių. Šiuos veiksmus galima atlikti bet kurioje įmonėje, nes ER konfigūracijas įmonės naudoja bendrai.</span><span class="sxs-lookup"><span data-stu-id="76d29-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="76d29-106">Norint atlikti šiuos veiksmus, pirmiausia reikia atlikti veiksmus, nurodytus temoje [Sukurti konfigūracijų teikėją ir jį pažymėti kaip aktyvų](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="76d29-106">To complete these steps, you must first complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="76d29-107">Norėdami atlikti šiuos veiksmus, taip pat turite turėti prieigą prie RCS egzemplioriaus, kuriame yra bent viena būsenos **Baigta** arba **Bendrinama** konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="76d29-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="76d29-108">Eikite į **Organizacijos administravimas** > **Darbo sritys** > **Elektroninės ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="76d29-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="76d29-109">Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip **Aktyvus**.</span><span class="sxs-lookup"><span data-stu-id="76d29-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="76d29-110">Jei nematote šio konfigūracijos teikėjo, atlikite temos [Sukurti konfigūracijų teikėją ir jį pažymėti kaip aktyvų](er-configuration-provider-mark-it-active-2016-11.md) veiksmus.</span><span class="sxs-lookup"><span data-stu-id="76d29-110">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="76d29-111">Jei jūsų įmonėje nėra sukonfigūruotos RKS aplinkos, spustelėkite išorinį saitą **Regulatory Services – Configuration** ir vykdykite instrukcijas, kad sukonfigūruotumėte RCS aplinką.</span><span class="sxs-lookup"><span data-stu-id="76d29-111">If you have no RCS environment provisioned to your company, click **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="76d29-112">Spustelėkite **Elektroninių ataskaitų parametrai**.</span><span class="sxs-lookup"><span data-stu-id="76d29-112">Click **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="76d29-113">Spustelėkite skirtuką **RCS**.</span><span class="sxs-lookup"><span data-stu-id="76d29-113">Click the **RCS** tab.</span></span> 
6. <span data-ttu-id="76d29-114">Jei RCS aplinka jūsų įmonėje jau sukonfigūruota, norėdami ją pasiekti naudokite puslapyje pateiktus URL.</span><span class="sxs-lookup"><span data-stu-id="76d29-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="76d29-115">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="76d29-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="76d29-116">Užregistruokite naują ER saugyklą.</span><span class="sxs-lookup"><span data-stu-id="76d29-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="76d29-117">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="76d29-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="76d29-118">Pasirinkite teikėją „Litware, Inc.“.</span><span class="sxs-lookup"><span data-stu-id="76d29-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="76d29-119">Spustelėkite Saugyklos.</span><span class="sxs-lookup"><span data-stu-id="76d29-119">Click Repositories.</span></span> 
4. <span data-ttu-id="76d29-120">Spustelėdami Įtraukti atidarykite išplečiamąjį dialogo langą.</span><span class="sxs-lookup"><span data-stu-id="76d29-120">Click Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="76d29-121">Lauke Konfigūracijų saugyklos tipas įveskite „RCS“.</span><span class="sxs-lookup"><span data-stu-id="76d29-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="76d29-122">Spustelėkite Kurti saugyklą.</span><span class="sxs-lookup"><span data-stu-id="76d29-122">Click Create repository.</span></span> 
7. <span data-ttu-id="76d29-123">Lauke RCS aplinkos rodomas pavadinimas įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="76d29-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="76d29-124">Pasirinkite norimą RCS egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="76d29-124">Select the desired RCS instance.</span></span> <span data-ttu-id="76d29-125">Atkreipkite dėmesį, kad galite turėti kelis iš jų.</span><span class="sxs-lookup"><span data-stu-id="76d29-125">Note that you can have several of them.</span></span> 
9. <span data-ttu-id="76d29-126">Spustelėkite Gerai.</span><span class="sxs-lookup"><span data-stu-id="76d29-126">Click OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="76d29-127">ER konfigūracijų importavimas iš RCS saugyklos</span><span class="sxs-lookup"><span data-stu-id="76d29-127">Import ER configurations from RCS based repository</span></span>
1. <span data-ttu-id="76d29-128">Spustelėkite **Rodyti filtrus**.</span><span class="sxs-lookup"><span data-stu-id="76d29-128">Click **Show filters**.</span></span> 
2. <span data-ttu-id="76d29-129">Įveskite filtro reikšmę „RCS“ lauke **Pavadinimas** naudodami filtro operatorių **prasideda**.</span><span class="sxs-lookup"><span data-stu-id="76d29-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="76d29-130">Atidarę pažymėtą saugyklą, puslapyje **Prijungimas prie „Regulatory Configuration Services“** spustelėkite saitą **Spustelėkite čia norėdami prijungti prie „Regulatory Configuration Services“**.</span><span class="sxs-lookup"><span data-stu-id="76d29-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, click **Click here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="76d29-131">Spustelėkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="76d29-131">Click **Open**.</span></span> 
5. <span data-ttu-id="76d29-132">Spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="76d29-132">Click **Close**.</span></span> 
6. <span data-ttu-id="76d29-133">Pasirinkite norimą ER konfigūracijos versiją ir spustelėkite **Importuoti**, kad importuotumėte ją į dabartinį egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="76d29-133">Select the desired version of ER configuration and click **Import** to bring it in the current instance.</span></span>

