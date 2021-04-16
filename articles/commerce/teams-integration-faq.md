---
title: „Dynamics 365 Commerce“ ir „Microsoft Teams“ integravimo DUK
description: Šioje temoje pateikiami atsakymai į dažniausiai užduodamus klausimus apie„ Microsoft Dynamics 365 Commerce” ir „Microsoft Teams” integravimą.
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
ms.openlocfilehash: 26e1dc53126c0615332457aa785415c4c7112bbd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842714"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a><span data-ttu-id="79042-103">„Dynamics 365 Commerce“ ir „Microsoft Teams“ integravimo DUK</span><span class="sxs-lookup"><span data-stu-id="79042-103">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="79042-104">Šioje temoje pateikiami atsakymai į dažniausiai užduodamus klausimus apie„ Microsoft Dynamics 365 Commerce” ir „Microsoft Teams” integravimą.</span><span class="sxs-lookup"><span data-stu-id="79042-104">This topic provides answers to frequently asked questions regarding Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a><span data-ttu-id="79042-105">Kas parduotuvėje tampa komandos savininku, kol „Teams” parengiama iš „Commerce”?</span><span class="sxs-lookup"><span data-stu-id="79042-105">Who in the store becomes an owner of a team while provisioning Teams from Commerce?</span></span> 

<span data-ttu-id="79042-106">Visi parduotuvių vadovai automatiškai įtraukiami kaip savininkai į atitinkamą komandos grupę, kad jie galėtų atlikti operacijas, pavyzdžiui, įtraukti privatų kanalą ir įtraukti ar panaikinti narius.</span><span class="sxs-lookup"><span data-stu-id="79042-106">All store managers are automatically added as owners to the corresponding team group so that they can perform operations such as adding a private channel and adding or deleting members.</span></span> 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a><span data-ttu-id="79042-107">Kaip priskirti „komunikacijos vadovo” vaidmenį darbuotojui „Commerce” būstinėje?</span><span class="sxs-lookup"><span data-stu-id="79042-107">How do I assign the "communications manager" role to an employee in Commerce headquarters?</span></span> 

<span data-ttu-id="79042-108">Komunikacijos vadovai „Microsoft Teams” platformoje turi galimybę kurti ir publikuoti užduočių sąrašus.</span><span class="sxs-lookup"><span data-stu-id="79042-108">Communication managers in Microsoft Teams have the ability to create and publish task lists.</span></span> <span data-ttu-id="79042-109">Organizacijos darbuotojams, kurie turėtų tapti komunikacijos vadovais, turi būti priskirtas „mažmeninės prekybos užduočių vadovo” vaidmuo „Commerce” būstinėje.</span><span class="sxs-lookup"><span data-stu-id="79042-109">Organization employees who need to become communication managers must have the "retail task manager" role assigned to them in Commerce headquarters.</span></span>

<span data-ttu-id="79042-110">Norėdami darbuotojui priskirti mažmeninės prekybos užduočių vadovo vaidmenį, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="79042-110">To assign the retail task manager role to an employee in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="79042-111">Eikite į **Mažmeninė prekyba ir komercija \> Darbuotojai \> Vartotojai**.</span><span class="sxs-lookup"><span data-stu-id="79042-111">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="79042-112">Pasirinkite darbuotoją.</span><span class="sxs-lookup"><span data-stu-id="79042-112">Select an employee.</span></span>
1. <span data-ttu-id="79042-113">„FastTab“ skirtuke **Vartotojo vaidmenys** pasirinkite **Priskirti vaidmenis**.</span><span class="sxs-lookup"><span data-stu-id="79042-113">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="79042-114">Dialogo lange **Priskirti vaidmenis vartotojui** pasirinkite vaidmenį **Mažmeninės prekybos užduočių vadovas**, tada pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="79042-114">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a><span data-ttu-id="79042-115">Kaip padaryti, kad būtų galima įkelti konkrečią organizacijos hierarchiją į „Microsoft Teams”?</span><span class="sxs-lookup"><span data-stu-id="79042-115">How do I make a specific organization hierarchy available to upload into Microsoft Teams?</span></span>

<span data-ttu-id="79042-116">„Commerce” būstinėje kiekviena organizacijos hierarchija yra susieta su vienu arba daugiau tikslų.</span><span class="sxs-lookup"><span data-stu-id="79042-116">In Commerce headquarters, every organization's hierarchy is associated with one or more purposes.</span></span> <span data-ttu-id="79042-117">Įsitikinkite, kad hierarchijoje, kurią norite parengti į „Microsoft Teams”, yra su ja susietas **Mažmeninės prekybos ataskaitų** tikslas, kaip parodyta toliau pateiktame pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="79042-117">Make sure the hierarchy that you want to provision into Microsoft Teams has the **Retail reporting** purpose associated with it, as shown in the following example image.</span></span> 

![Organizacijos hierarchijos tikslo pavyzdys „Commerce” būstinėje](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a><span data-ttu-id="79042-119">Kaip įgalinti mažmeninės prekybos parduotuvės darbuotojus prisijungti prie „Commerce” elektroninio kasos aparato (EKA) naudojant „Azure Active Directory” („Azure AD”)?</span><span class="sxs-lookup"><span data-stu-id="79042-119">How do I enable retail store workers to sign in to Commerce point of sale (POS) using Azure Active Directory (Azure AD)?</span></span>

<span data-ttu-id="79042-120">Informaciją apie tai, kaip sukonfigūruoti „Commerce” EKA prisijungimo patirtį, kad būtų naudojamas „Azure AD” autentifikavimas, rasite [„Azure Active Directory” autentifikavimo įgalinimas EKA prisijungimui](aad-pos-logon.md).</span><span class="sxs-lookup"><span data-stu-id="79042-120">For information about how to configure the Commerce POS sign-in experience to use Azure AD authentication, see [Enable Azure Active Directory authentication for POS sign-in](aad-pos-logon.md).</span></span>

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a><span data-ttu-id="79042-121">Kaip susieti parduotuves ir atitinkamas komandas „Commerce” būstinėje, jei mano organizacija jau sukūrė komandas „Microsoft Teams” platformoje?</span><span class="sxs-lookup"><span data-stu-id="79042-121">How do I map stores and corresponding teams in Commerce headquarters if my organization has already created teams in Microsoft Teams?</span></span>

<span data-ttu-id="79042-122">Informaciją apie tai, kaip susieti parduotuves ir komandas, jeigu yra išankstinių komandų, rasite [Susiekite parduotuves ir atitinkamas komandas, jeigu jūsų organizacija turi išankstinių komandų „Microsoft Teams” platformoje](map-stores-existing-teams.md).</span><span class="sxs-lookup"><span data-stu-id="79042-122">For information on how to map stores and teams if there are pre-existing teams, see [Map stores and corresponding teams if your organization has pre-existing teams in Microsoft Teams](map-stores-existing-teams.md).</span></span>

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a><span data-ttu-id="79042-123">Kaip išvalyti „Microsoft Graph API” atpažinimo ženklą, saugomą seanso saugykloje?</span><span class="sxs-lookup"><span data-stu-id="79042-123">How do I clear the Microsoft Graph API token stored in the session storage?</span></span>

<span data-ttu-id="79042-124">Vartotojas, prisijungęs prie elektroninio kasos aparato (EKA) su „Azure Active Directory” („Azure AD”) abonementu, turi atsijungti nuo EKA arba uždaryti programą, kad išvalytų seanso saugyklą.</span><span class="sxs-lookup"><span data-stu-id="79042-124">A user who has signed in to the point of sale (POS) with an Azure Active Directory (Azure AD) account should sign out from the POS or close the application to clear the session storage.</span></span> 

> [!TIP]
> <span data-ttu-id="79042-125">Rekomenduojama geriausia praktika yra ta, kad darbuotojai visada užrakintų EKA terminalą arba atsijungtų nuo seanso, kai nenaudoja terminalo.</span><span class="sxs-lookup"><span data-stu-id="79042-125">A recommended best practice is to always have store workers lock the POS terminal or sign out from a session when not using the terminal.</span></span> 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a><span data-ttu-id="79042-126">Kas atsitinka, jei parduotuvėje neturi parduotuvės vadovų?</span><span class="sxs-lookup"><span data-stu-id="79042-126">What happens if a store doesn't have store managers?</span></span>

<span data-ttu-id="79042-127">Jei parduotuvėje nėra vadovų, komandos grupė nebus sukurta parduotuvei ar „Teams” platformoje.</span><span class="sxs-lookup"><span data-stu-id="79042-127">If a store doesn't have managers, a team group will not be created for the store or in Teams.</span></span> 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a><span data-ttu-id="79042-128">Kas atsitinka, jeigu parduotuvės vadovas išeina iš įmonės?</span><span class="sxs-lookup"><span data-stu-id="79042-128">What happens if a store manager leaves the company?</span></span>

<span data-ttu-id="79042-129">Kiekvienas asmuo, turintis savininko vaidmenį, gali įtraukti naują parduotuvės vadovą „Commerce” būstinėje ir iš naujo parengti „Teams” tam, kad naujas vadovas turėtų reikiamas grupės teises „Teams” platformoje.</span><span class="sxs-lookup"><span data-stu-id="79042-129">Anyone with the owner role can add a new store manager in Commerce headquarters and reprovision Teams so that the new manager will have the necessary privileges in Teams for the group.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="79042-130">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="79042-130">Additional resources</span></span>

[<span data-ttu-id="79042-131">„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="79042-131">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="79042-132">„Dynamics 365 Commerce” ir „Microsoft Teams” integravimo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="79042-132">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="79042-133">„Microsoft Teams” parengimas iš „Dynamics 365 Commerce”</span><span class="sxs-lookup"><span data-stu-id="79042-133">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="79042-134">Užduočių valdymo sinchronizavimas tarp „Microsoft Teams” ir „Dynamics 365 Commerce” EKA</span><span class="sxs-lookup"><span data-stu-id="79042-134">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="79042-135">Vartotojų vaidmenų tvarkymas Microsoft Teams” platformoje</span><span class="sxs-lookup"><span data-stu-id="79042-135">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="79042-136">Susiekite parduotuves ir komandas, jeigu yra išankstinių komandų „Microsoft Teams” platformoje</span><span class="sxs-lookup"><span data-stu-id="79042-136">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)