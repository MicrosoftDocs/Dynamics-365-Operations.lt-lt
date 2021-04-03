---
title: Prisijungimo saitas nukreipia atgal į el. prekybos svetainę
description: Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti, kai prisijungimo saitas nukreipia atgal į el. prekybos svetainę, o ne prisijungimo puslapį.
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
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36f10c9f68570a6c67da6b4b6e4155f4634f633a
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585439"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="0ddd7-103">Prisijungimo saitas nukreipia atgal į el. prekybos svetainę</span><span class="sxs-lookup"><span data-stu-id="0ddd7-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0ddd7-104">Šioje temoje pateikiamos trikčių diagnostikos priemonės, galinčios padėti, kai prisijungimo saitas nukreipia atgal į el. prekybos svetainę, o ne prisijungimo puslapį.</span><span class="sxs-lookup"><span data-stu-id="0ddd7-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="0ddd7-105">Aprašymas</span><span class="sxs-lookup"><span data-stu-id="0ddd7-105">Description</span></span>

<span data-ttu-id="0ddd7-106">Sukonfigūravę naują „Microsoft Azure Active Directory B2C“ („Azure AD B2C“) nuomininką „Commerce“ svetainių daryklėje, nuorodą **Prisijungti** pasirinkę vartotojai nukreipiami atgal į pagrindinį el. prekybos nukreipimo puslapį, o ne prisijungimo puslapį.</span><span class="sxs-lookup"><span data-stu-id="0ddd7-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="0ddd7-107">Sprendimas</span><span class="sxs-lookup"><span data-stu-id="0ddd7-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="0ddd7-108">Patvirtinti, kad atsakymo URL tinkamai sukonfigūruotas „Azure AD” B2C programoje</span><span class="sxs-lookup"><span data-stu-id="0ddd7-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="0ddd7-109">Norėdami patvirtinti, kad atsakymo URL tinkamai sukonfigūruotas „Azure AD” B2C programoje, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0ddd7-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="0ddd7-110">Eikite į [„Azure“ portalą](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="0ddd7-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="0ddd7-111">Pasirinkite „Azure AD” B2C programą, kurią sukūrėte jūsų svetainės prieigai.</span><span class="sxs-lookup"><span data-stu-id="0ddd7-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="0ddd7-112">Pasirinkite programą, kurią sukūrėte „Azure AD” B2C nustatymo metu.</span><span class="sxs-lookup"><span data-stu-id="0ddd7-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="0ddd7-113">Dalyje **Atsakymo URL** patikrinkite, kad sąraše yra ir svetainės domeno URL, ir el. prekybos sugeneruoto URL įrašai, kaip parodyta toliau pateiktos iliustracijos pavyzdyje.</span><span class="sxs-lookup"><span data-stu-id="0ddd7-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![„Azure AD” B2C atsakymo URL įrašai](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="0ddd7-115">Svetainės domeno URL ir el. prekybos sugeneruotas URL turi būti tinkamo URL formato, kuris neįtraukia priekinių arba pabaigos pasvirųjų brūkšnių.</span><span class="sxs-lookup"><span data-stu-id="0ddd7-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ddd7-116">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="0ddd7-116">Additional resources</span></span>

[<span data-ttu-id="0ddd7-117">Žiniatinklio programos užregistravimas „Azure Active Directory” B2C</span><span class="sxs-lookup"><span data-stu-id="0ddd7-117">Register a web application in Azure Active Directory B2C</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="0ddd7-118">„Commerce” B2C nuomotojo sąranka</span><span class="sxs-lookup"><span data-stu-id="0ddd7-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)