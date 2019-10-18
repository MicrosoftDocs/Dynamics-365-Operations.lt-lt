---
title: Vartotojas nerastas žmonių parinkiklyje naudojant „Attract“ arba „Onboard“
description: Šioje temoje paaiškinama, ką daryti, kai įmonės nuomotojo vartotojai nerodomi žmonių parinkiklyje naudojant „Dynamics 365 Talent“ „Attract“ arba „Onboard“ programas.
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2a3c83fcc3f48aa235ffb2db2dc492b34a306c4c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024199"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a><span data-ttu-id="8ffbb-103">„Azure Active Directory“ vartotojų žmonių parinkiklyje nerasta</span><span class="sxs-lookup"><span data-stu-id="8ffbb-103">Azure Active Directory users not found in People Picker</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="8ffbb-104">Išduoti</span><span class="sxs-lookup"><span data-stu-id="8ffbb-104">Issue</span></span>

<span data-ttu-id="8ffbb-105">Tam tikri tinkami „Microsoft Azure Active Directory“ („Azure AD“) nuomotojo vartotojai nerodomi, kai ieškoma vardų žmonių parinkiklyje naudojant „Dynamics 365 Talent: Attract“ „Dynamics 365 Talent: Onboard“ programas.</span><span class="sxs-lookup"><span data-stu-id="8ffbb-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in Dynamics 365 Talent: Attract or Dynamics 365 Talent: Onboard.</span></span>

## <a name="cause"></a><span data-ttu-id="8ffbb-106">Priežastis</span><span class="sxs-lookup"><span data-stu-id="8ffbb-106">Cause</span></span>

<span data-ttu-id="8ffbb-107">Šiuo metu tam tikrų tipų vartotojai „Attract“ ir „Onboard“ nepalaikomi.</span><span class="sxs-lookup"><span data-stu-id="8ffbb-107">Certain user types are not currently supported in Attract and Onboard.</span></span> <span data-ttu-id="8ffbb-108">Patikrinkite, ar vartotojas nėra „Azure AD“ įmonių (B2B) vartotojas svečias.</span><span class="sxs-lookup"><span data-stu-id="8ffbb-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="8ffbb-109">Vartotojo tipo informaciją galima rasti „Azure“ portalo mentėje „Azure Active Directory“.</span><span class="sxs-lookup"><span data-stu-id="8ffbb-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="8ffbb-110">Daugiau informacijos apie „Azure B2B“ rasite [Kas yra vartotojo svečio prieiga „Azure Active Directory B2B“](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span><span class="sxs-lookup"><span data-stu-id="8ffbb-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="8ffbb-111">Ne B2B vartotojai, tam tikrų vartotojų ypatybė Vartotojo tipas gali būti neišsami objekte **Vartotojas**.</span><span class="sxs-lookup"><span data-stu-id="8ffbb-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="8ffbb-112">Tai galima patikrinti ir ištaisyti naudojant „Azure AD PowerShell“ modulį.</span><span class="sxs-lookup"><span data-stu-id="8ffbb-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="8ffbb-113">Daugiau informacijos rasite [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).</span><span class="sxs-lookup"><span data-stu-id="8ffbb-113">For more information, see [Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="8ffbb-114">Nutarimas</span><span class="sxs-lookup"><span data-stu-id="8ffbb-114">Resolution</span></span>

<span data-ttu-id="8ffbb-115">Norint atlikti tolesnius veiksmus ir išspręsti problemą, jums reikia turėti tipo Visuotinis administratorius teises „Azure Active Directory“ nuomotojuje arba tipo **User.ReadWrite.All** teises.</span><span class="sxs-lookup"><span data-stu-id="8ffbb-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="8ffbb-116">Kaip patikrinti paveikto vartotojo ypatybę Vartotojo"tipas.</span><span class="sxs-lookup"><span data-stu-id="8ffbb-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="8ffbb-117">Komanda pateikia toliau nurodytą informaciją.</span><span class="sxs-lookup"><span data-stu-id="8ffbb-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="8ffbb-118">Įsidėmėkite vartotojo ypatybę **UserType**.</span><span class="sxs-lookup"><span data-stu-id="8ffbb-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="8ffbb-119">Jei laukas **UserType** yra tuščias, pavyzdžiui ne Narys arba Svečias, atnaujinkite lauką **UserType**naudodami toliau nurodytą komandą.</span><span class="sxs-lookup"><span data-stu-id="8ffbb-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
