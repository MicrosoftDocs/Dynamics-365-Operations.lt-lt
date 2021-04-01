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
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 244d612fa01529df4fff250df50a06526632fcf1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210928"
---
# <a name="opt-out-of-web-activity-event-collection"></a><span data-ttu-id="87737-103">Žiniatinklio veiklos įvykių rinkimo atsisakymas</span><span class="sxs-lookup"><span data-stu-id="87737-103">Opt out of web activity event collection</span></span>
[!include [banner](includes/banner.md)]

<span data-ttu-id="87737-104">Šioje temoje aiškinama informacija, kaip galite leisti klientams atsisakyti žiniatinklio veiklos įvykių rinkimo naudojant „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="87737-104">This topic explains how you can let customers opt out of web activity event collection in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="87737-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="87737-105">Overview</span></span>

<span data-ttu-id="87737-106">„Dynamics 365 Commerce“ leidžia svetainių administratoriams analizuoti savo el. prekybos svetainių vartotojų veiklą žiniatinklyje.</span><span class="sxs-lookup"><span data-stu-id="87737-106">Dynamics 365 Commerce lets site administrators analyze the web activity of users of their e-commerce sites.</span></span> <span data-ttu-id="87737-107">Tokiu būdu jie gali geriau suprasti, kaip naudojamos jų svetainės, ir gali jas optimizuoti, kad būtų užtikrinta geresnė vartotojų patirtis ir pasiekti verslo tikslai.</span><span class="sxs-lookup"><span data-stu-id="87737-107">In that way, they can better understand how their sites are used, and they can optimize the sites to provide an improved user experience and meet business objectives.</span></span>


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a><span data-ttu-id="87737-108">Būdai, kaip administratoriai gali įdiegti atsisakymo funkcijas</span><span class="sxs-lookup"><span data-stu-id="87737-108">Ways for administrators to implement an opt-out experience</span></span>

<span data-ttu-id="87737-109">Administratoriai atsisakymo funkcijas gali įdiegti trimis būdais.</span><span class="sxs-lookup"><span data-stu-id="87737-109">Administrators have three ways to implement an opt-out experience.</span></span>

### <a name="opt-out-on-behalf-of-users"></a><span data-ttu-id="87737-110">Atsisakymas vartotojų vardu</span><span class="sxs-lookup"><span data-stu-id="87737-110">Opt out on behalf of users</span></span>

<span data-ttu-id="87737-111">„Commerce“ pagrindinio komponento (HQ) dalyje Paskyrų tvarkymas administratoriai gali atsisakyti vartotojų vardu.</span><span class="sxs-lookup"><span data-stu-id="87737-111">In Account management in Commerce headquarters (HQ), administrators can opt out on behalf of users.</span></span>

1. <span data-ttu-id="87737-112">HQ kliento puslapyje **Visi klientai** raskite ir pasirinkite klientą.</span><span class="sxs-lookup"><span data-stu-id="87737-112">In the HQ client, on the **All customers** page, search for and select a customer.</span></span>
1. <span data-ttu-id="87737-113">Kliento informacijos puslapyje, „FastTab“ konteinerio **Mažmeninė prekyba** dalyje **Privatumas** nustatykite parinkties **Nestebėti žiniatinklio veiklos** reikšmę kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="87737-113">On the customer details page, on the **Retail** FastTab, in the **Privacy** section, set the **Do not track web activity** option to **Yes**.</span></span>

    ![Privatumo nustatymai](media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="87737-115">Pasirinkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="87737-115">Select **Save**, and then close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="87737-116">Moduliais pagrįsta atsisakymo galimybė</span><span class="sxs-lookup"><span data-stu-id="87737-116">Module-based opt-out experience</span></span>

<span data-ttu-id="87737-117">Administratoriai gali leisti autentifikuotiems vartotojams patiems atsisakyti žiniatinklio veiklos įvykių rinkimo.</span><span class="sxs-lookup"><span data-stu-id="87737-117">Administrators can let authenticated users opt out of web activity event collection by themselves.</span></span> <span data-ttu-id="87737-118">Norėdami įgalinti šią atsisakymo galimybę, pridėkite vartotojo atsisakymo modulį prie kliento sąskaitos profilio puslapių.</span><span class="sxs-lookup"><span data-stu-id="87737-118">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="87737-119">Pasirinktiniai plėtiniai</span><span class="sxs-lookup"><span data-stu-id="87737-119">Custom extensions</span></span>

<span data-ttu-id="87737-120">Administratoriai gali sukurti savo plėtinius, kad galėtų valdyti vartotojų atsisakymo galimybę.</span><span class="sxs-lookup"><span data-stu-id="87737-120">Administrators can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="87737-121">Daugiau informacijos rasite [Skambučių mažmeninės prekybos serverio API](e-commerce-extensibility/call-retail-server-apis.md) ir [Internetinio kanalo išplėtimas](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="87737-121">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]