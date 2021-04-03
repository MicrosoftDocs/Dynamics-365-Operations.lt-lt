---
title: Atliekant pradinį diegimą nepavyko sukonfigūruoti „Commerce” svetainių daryklės saugos grupės
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai „Microsoft Azure Active Directory” („Azure AD”) „Commerce” svetainių daryklės saugos grupė neodoma kaip parinktis, kai kuriate el. prekybos komponentus „Microsoft Dynamics Lifecycle Services” (LCS) pirmą kartą diegdami naują el. prekybos nuomininką.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36ea43e19f395e3914d3eda1a9b8f5487b0926c5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585450"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a><span data-ttu-id="09e16-103">Atliekant pradinį diegimą nepavyko sukonfigūruoti „Commerce” svetainių daryklės saugos grupės</span><span class="sxs-lookup"><span data-stu-id="09e16-103">Can't configure a security group for Commerce site builder during initial deployment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09e16-104">Šioje temoje pateikiamos trikčių diagnostikos priemonės, kurios gali padėti, kai „Microsoft Azure Active Directory” („Azure AD”) „Commerce” svetainių daryklės saugos grupė neodoma kaip parinktis, kai kuriate el. prekybos komponentus „Microsoft Dynamics Lifecycle Services” (LCS) pirmą kartą diegdami naują el. prekybos nuomininką.</span><span class="sxs-lookup"><span data-stu-id="09e16-104">This topic provides troubleshooting guidance that can help when the Microsoft Azure Active Directory (Azure AD) security group for Commerce site builder doesn't appear as an option when you create e-commerce components in Microsoft Dynamics Lifecycle Services (LCS) during initial deployment of a new e-commerce tenant.</span></span>

## <a name="description"></a><span data-ttu-id="09e16-105">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="09e16-105">Description</span></span>

<span data-ttu-id="09e16-106">Kai kuriate el. prekybos komponentus, diegdami naują el. prekybos nuomininką, kuriame yra „Commerce“ svetainių daryklės komponentas, „Azure AD“ saugos grupė nerodoma kaip parinktis dialogo lange.</span><span class="sxs-lookup"><span data-stu-id="09e16-106">When you create the e-commerce components as part of the process of deploying a new e-commerce tenant that includes the Commerce site builder component, the Azure AD security group doesn't appear as an option in the dialog box.</span></span>

## <a name="resolution"></a><span data-ttu-id="09e16-107">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="09e16-107">Resolution</span></span>

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a><span data-ttu-id="09e16-108">Parengti el. prekybos svetainę tinkamo nuomininko vartotoju</span><span class="sxs-lookup"><span data-stu-id="09e16-108">Provision the e-commerce site with a user in the correct tenant</span></span>

1. <span data-ttu-id="09e16-109">Eikite į [„Azure“ portalą](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="09e16-109">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="09e16-110">Nuomininke, kuriam buvo parengtas jūsų el. prekybos svetainės LCS projektas, vykdykite instrukcijas, pateiktas [Pagrindinės grupės kūrimas ir narių įtraukimas naudojant „Azure Active Directory”](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="09e16-110">Under the tenant that the LCS project for your e-commerce site was provisioned for, follow the instructions in [Create a basic group and add members using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span>
1. <span data-ttu-id="09e16-111">Eikite į [LCS](https://lcs.dynamics.com/) ir prisijunkite naudodami sąskaitą, naudojančią tą patį nuomininką kaip ir ką tik sukurta „Azure AD” saugos grupė.</span><span class="sxs-lookup"><span data-stu-id="09e16-111">Go to [LCS](https://lcs.dynamics.com/), and sign in by using an account that shares the same tenant as the Azure AD security group that you just created.</span></span> <span data-ttu-id="09e16-112">Sąskaita turi turėti prieigą peržiūrėti „Azure AD” saugos grupę.</span><span class="sxs-lookup"><span data-stu-id="09e16-112">The account must have access to view the Azure AD security group.</span></span>
1. <span data-ttu-id="09e16-113">Norėdami sukonfigūruoti el. prekybos svetainę, užbaikite sąrankos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="09e16-113">Complete the setup steps to configure the e-commerce site.</span></span> <span data-ttu-id="09e16-114">Kai parengiate el. prekybos komponentus, saugos grupė turėtų būti rodoma kaip dialogo lango parinktis.</span><span class="sxs-lookup"><span data-stu-id="09e16-114">When you provision the e-commerce components, the security group should now appear as an option in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="09e16-115">Norėdami užtikrinti, kad dialogo lange esantis laukas būtų užpildytas saugos grupių sąrašu, įvesdami sukurtos „Azure AD” saugos grupės pavadinimą, turite pasirinkti **Įvesti**.</span><span class="sxs-lookup"><span data-stu-id="09e16-115">To ensure that the field in the dialog box is filled with the list of security groups, you must select **Enter** after you enter the name of the Azure AD security group that you created.</span></span> <span data-ttu-id="09e16-116">Ieškos rezultatuose bus pateiktos visos „Azure AD” saugos grupės, kurios prasideda ieškos tekstu ir prie kurių vartotojas turi prieigą.</span><span class="sxs-lookup"><span data-stu-id="09e16-116">The search results will list all the Azure AD security groups that start with the search text, and that the user has access to.</span></span> <span data-ttu-id="09e16-117">Galite naudoti trumpesnį ieškos terminą, kad būtų galima gauti platesnes ieškos rezultatų.</span><span class="sxs-lookup"><span data-stu-id="09e16-117">You can use a shorter search term to allow for broader search results.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09e16-118">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="09e16-118">Additional resources</span></span>

[<span data-ttu-id="09e16-119">Pagrindinės grupės kūrimas ir narių įtraukimas naudojant „Azure Active Directory”</span><span class="sxs-lookup"><span data-stu-id="09e16-119">Create a basic group and add members using Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[<span data-ttu-id="09e16-120">Naujo el. prekybos nuomotojo diegimas</span><span class="sxs-lookup"><span data-stu-id="09e16-120">Deploy a new e-commerce tenant</span></span>](../deploy-ecommerce-site.md)
