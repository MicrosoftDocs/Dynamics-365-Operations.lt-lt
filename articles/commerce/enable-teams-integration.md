---
title: „ Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas
description: Šioje temoje aprašoma, kaip įgalinti „Microsoft Dynamics 365 Commerce” ir „Microsoft Teams” integravimą.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c0dbf7a3c7fa3532e35cac240c1abb8adbdbe489
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842710"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a><span data-ttu-id="6ed65-103">„ Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="6ed65-103">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="6ed65-104">Šioje temoje aprašoma, kaip įgalinti „Microsoft Dynamics 365 Commerce” ir „Microsoft Teams” integravimą.</span><span class="sxs-lookup"><span data-stu-id="6ed65-104">This topic describes how to enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="6ed65-105">Norėdami sukonfigūruoti „Teams” su informacija iš „Dynamics 365 Commerce” ir sinchronizuoti užduočių valdymo funkcijas tarp „Teams” ir elektroninio kasos aparato (EKA) programos, turite įgalinti integravimo funkcijas „Commerce” būstinėje.</span><span class="sxs-lookup"><span data-stu-id="6ed65-105">To provision Teams with information from Dynamics 365 Commerce and synchronize the task management features between Teams and the point of sale (POS) application, you must enable the integration features in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="6ed65-106">Kai įgalinate „Teams” integravimą, sutinkate su „Teams” bendrinti savo duomenis.</span><span class="sxs-lookup"><span data-stu-id="6ed65-106">When you enable Teams integration, you consent to share your data with Teams.</span></span> <span data-ttu-id="6ed65-107">Su „Teams” bendrinami duomenys gali priklausyti kitai šaliai nei jūsų „Commerce” duomenys ir jiems gali būti taikomi skirtingi atitikties standartai.</span><span class="sxs-lookup"><span data-stu-id="6ed65-107">Data that is shared with Teams might reside in a different country than your Commerce data, and it might be subject to different compliance standards.</span></span> <span data-ttu-id="6ed65-108">Daugiau informacijos rasite [„Microsoft” patikimumo centras](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="6ed65-108">For more information, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="6ed65-109">Daugiau informacijos apie „Microsoft” privatumo politikas rasite [„Microsoft” privatumo nuostatos](https://aka.ms/privacy).</span><span class="sxs-lookup"><span data-stu-id="6ed65-109">For information about Microsoft privacy policies, see the [Microsoft Privacy Statement](https://aka.ms/privacy).</span></span>

## <a name="enable-teams-integration"></a><span data-ttu-id="6ed65-110">„Teams” integravimo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="6ed65-110">Enable Teams integration</span></span>

<span data-ttu-id="6ed65-111">Prieš įgalindami „Microsoft Teams” integravimą su „Commerce”, turite užregistruoti „Teams” programą jūsų nuomotojui „Azure” portale.</span><span class="sxs-lookup"><span data-stu-id="6ed65-111">Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.</span></span>

<span data-ttu-id="6ed65-112">Norėdami užregistruoti „Teams” programą savo nuomotojui „Azure” portale, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6ed65-112">To register the Teams application with your tenant in the Azure portal, follow these steps.</span></span>

1. <span data-ttu-id="6ed65-113">Atlikite skyriuje [Greitas pasirengimas darbui: Registruoti programą „Microsoft” tapatybės platformoje](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) pateiktus veiksmus, norėdami užregistruoti „Teams” programą jūsų nuomotojui „Azure” portale.</span><span class="sxs-lookup"><span data-stu-id="6ed65-113">Follow the steps in [Quickstart: Register an app in the Microsoft identity platform](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) to register the Teams application with your tenant in the Azure portal.</span></span>
1. <span data-ttu-id="6ed65-114">Nukopijuokite **Programos (kliento) ID** reikšmę iš **Apžvalgos** puslapio užregistruotai programai.</span><span class="sxs-lookup"><span data-stu-id="6ed65-114">Copy the **Application (client) ID** value from the **Overview** page for the registered app.</span></span> <span data-ttu-id="6ed65-115">Šią reikšmę naudosite „Teams” integravimo įgalinimui „Commerce” būstinėje.</span><span class="sxs-lookup"><span data-stu-id="6ed65-115">You will use this value to enable Teams integration in Commerce headquarters.</span></span>
1. <span data-ttu-id="6ed65-116">Nukopijuokite sertifikato reikšmę, kuri buvo įvesta, kai [įtraukėte sertifikatą](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) 1 veiksme.</span><span class="sxs-lookup"><span data-stu-id="6ed65-116">Copy the certificate value that was entered when you [added a certificate](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) in step 1.</span></span> <span data-ttu-id="6ed65-117">Sertifikatas taip pat vadinamas viešuoju raktu arba programos raktu.</span><span class="sxs-lookup"><span data-stu-id="6ed65-117">The certificate is also known as the public key or application key.</span></span> <span data-ttu-id="6ed65-118">Šią reikšmę naudosite „Teams” integravimo įgalinimui „Commerce” būstinėje.</span><span class="sxs-lookup"><span data-stu-id="6ed65-118">You will use this value to enable Teams integration in Commerce headquarters.</span></span>

<span data-ttu-id="6ed65-119">Norėdami įgalinti „Teams” integravimą „Commerce“ būstinėje, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6ed65-119">To enable Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="6ed65-120">Eikite į **Mažmeninė prekyba ir komercija \> Kanalų sąranka \> „Microsoft Teams” integravimo konfigūracija**.</span><span class="sxs-lookup"><span data-stu-id="6ed65-120">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams integration configuration**.</span></span>
1. <span data-ttu-id="6ed65-121">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="6ed65-121">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="6ed65-122">Nustatykite parinktį **Įgalinti „Microsoft Teams” integravimą** į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="6ed65-122">Set the **Enable Microsoft Teams integration** option to **Yes**.</span></span>
1. <span data-ttu-id="6ed65-123">Laukuose **Programos ID** ir **Programos raktas** įveskite reikšmes, gautas registruojant „Teams” programą „Azure” portale.</span><span class="sxs-lookup"><span data-stu-id="6ed65-123">In the **Application ID** and **Application key** fields, enter the values you obtained when you registered the Teams application in the Azure portal.</span></span>
1. <span data-ttu-id="6ed65-124">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="6ed65-124">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="6ed65-125">Šioje iliustracijoje pateikiamas „Teams” integravimo „Commerce” būstinėje konfigūracijos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="6ed65-125">The following illustration shows an example of the configuration of Teams integration in Commerce headquarters.</span></span>

![„Teams” integravimo konfigūracija į „Commerce” būstinėje](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a><span data-ttu-id="6ed65-127">„Teams” integravimo išjungimas</span><span class="sxs-lookup"><span data-stu-id="6ed65-127">Disable Teams integration</span></span>

<span data-ttu-id="6ed65-128">Norėdami išjungti „Microsoft Teams” integravimą „Commerce“ būstinėje, atlikite nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="6ed65-128">To disable Microsoft Teams integration in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="6ed65-129">Eikite į **Mažmeninė prekyba ir komercija \> Kanalų sąranka \> „Microsoft Teams” integravimo konfigūravimas**.</span><span class="sxs-lookup"><span data-stu-id="6ed65-129">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="6ed65-130">Veiksmų srityje pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="6ed65-130">On the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="6ed65-131">Nustatykite parinktį **Įgalinti „Microsoft Teams” integravimą** į **Ne**.</span><span class="sxs-lookup"><span data-stu-id="6ed65-131">Set the **Enable Microsoft Teams integration** option to **No**.</span></span>
4. <span data-ttu-id="6ed65-132">Išvalykite laukų **Programos ID** ir **Programos raktas** reikšmes.</span><span class="sxs-lookup"><span data-stu-id="6ed65-132">Clear the values from the **Application ID** and **Application Key** fields.</span></span>
1. <span data-ttu-id="6ed65-133">Veiksmų srityje pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="6ed65-133">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="6ed65-134">Išjungus „Teams” integravimą su „Commerce”, EKA terminalai neberodys užduočių, publikuotų iš „Teams” programos.</span><span class="sxs-lookup"><span data-stu-id="6ed65-134">After you disable Teams integration with Commerce, POS terminals will no longer show tasks that are published from the Teams application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ed65-135">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="6ed65-135">Additional resources</span></span>

[<span data-ttu-id="6ed65-136">„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="6ed65-136">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="6ed65-137">„Microsoft Teams” parengimas iš „Dynamics 365 Commerce”</span><span class="sxs-lookup"><span data-stu-id="6ed65-137">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="6ed65-138">Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir „Dynamics 365 Commerce” EKA</span><span class="sxs-lookup"><span data-stu-id="6ed65-138">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="6ed65-139">Vartotojų vaidmenų tvarkymas Microsoft Teams” platformoje</span><span class="sxs-lookup"><span data-stu-id="6ed65-139">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="6ed65-140">Susiekite parduotuves ir komandas, jeigu yra išankstinių komandų „Microsoft Teams” platformoje</span><span class="sxs-lookup"><span data-stu-id="6ed65-140">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="6ed65-141">„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo DUK</span><span class="sxs-lookup"><span data-stu-id="6ed65-141">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
