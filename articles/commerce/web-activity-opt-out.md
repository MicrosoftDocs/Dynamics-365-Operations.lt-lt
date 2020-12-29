---
title: Žiniatinklio veiklos įvykių rinkimo atsisakymas
description: Šioje temoje aiškinama, kaip galite leisti savo svetainės lankytojams atsisakyti žiniatinklio veiklos įvykių rinkimo naudojant „Microsoft Dynamics 365 Commerce“.
author: aamiral
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4b0e48307527a8fea729d8dfdcdbc6337be0faf1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414366"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="7d540-103">Žiniatinklio veiklos įvykių rinkimo atsisakymas</span><span class="sxs-lookup"><span data-stu-id="7d540-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="7d540-104">Šioje temoje aiškinama informacija, kaip galite leisti klientams atsisakyti žiniatinklio veiklos įvykių rinkimo naudojant „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="7d540-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7d540-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="7d540-105">Overview</span></span>

<span data-ttu-id="7d540-106">„Dynamics 365 Commerce“ leidžia svetainių administratoriams analizuoti savo el. prekybos svetainių vartotojų veiklą žiniatinklyje.</span><span class="sxs-lookup"><span data-stu-id="7d540-106">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="7d540-107">Tokiu būdu jie gali geriau suprasti, kaip naudojamos jų svetainės, ir gali jas optimizuoti, kad būtų užtikrinta geresnė vartotojų patirtis ir pasiekti verslo tikslai.</span><span class="sxs-lookup"><span data-stu-id="7d540-107">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="7d540-108">Būdai, kaip administratoriai gali įdiegti atsisakymo funkcijas</span><span class="sxs-lookup"><span data-stu-id="7d540-108">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="7d540-109">Administratoriai atsisakymo funkcijas gali įdiegti trimis būdais.</span><span class="sxs-lookup"><span data-stu-id="7d540-109">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="7d540-110">Atsisakymas vartotojų vardu</span><span class="sxs-lookup"><span data-stu-id="7d540-110">Opt out on behalf of users</span></span>

<span data-ttu-id="7d540-111">„Commerce“ pagrindinio komponento (HQ) dalyje Paskyrų tvarkymas administratoriai gali atsisakyti vartotojų vardu.</span><span class="sxs-lookup"><span data-stu-id="7d540-111">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="7d540-112">HQ kliento puslapyje **Visi klientai** raskite ir pasirinkite klientą.</span><span class="sxs-lookup"><span data-stu-id="7d540-112">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="7d540-113">Kliento informacijos puslapyje, „FastTab“ konteinerio **Mažmeninė prekyba** dalyje **Privatumas** nustatykite parinkties **Nestebėti žiniatinklio veiklos** reikšmę kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="7d540-113">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Privatumo nustatymai](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="7d540-115">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7d540-115">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="7d540-116">Moduliais pagrįsta atsisakymo galimybė</span><span class="sxs-lookup"><span data-stu-id="7d540-116">Module-based opt-out experience</span></span>

<span data-ttu-id="7d540-117">Administratoriai gali leisti autentifikuotiems vartotojams patiems atsisakyti žiniatinklio veiklos įvykių rinkimo.</span><span class="sxs-lookup"><span data-stu-id="7d540-117">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="7d540-118">Norėdami įgalinti šią atsisakymo galimybę, pridėkite vartotojo atsisakymo modulį prie kliento sąskaitos profilio puslapių.</span><span class="sxs-lookup"><span data-stu-id="7d540-118">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="7d540-119">Pasirinktiniai plėtiniai</span><span class="sxs-lookup"><span data-stu-id="7d540-119">Custom extensions</span></span>

<span data-ttu-id="7d540-120">Administratoriai gali sukurti savo plėtinius, kad galėtų valdyti vartotojų atsisakymo galimybę.</span><span class="sxs-lookup"><span data-stu-id="7d540-120">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="7d540-121">Daugiau informacijos rasite [Skambučių mažmeninės prekybos serverio API](e-commerce-extensibility/call-retail-server-apis.md) ir [Internetinio kanalo išplėtimas](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="7d540-121">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
