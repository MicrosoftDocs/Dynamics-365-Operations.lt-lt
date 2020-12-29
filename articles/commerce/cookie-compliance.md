---
title: Slapukų atitiktis
description: Šioje temoje apžvelgiama slapukų atitiktis ir numatytosios strategijos, įtrauktos į „Microsoft Dynamics 365 Commerce“.
author: BrianShook
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f54b9b8130a167dbecdb13fccd7039f827f6ed0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414247"
---
# <a name="cookie-compliance"></a><span data-ttu-id="863b4-103">Slapukų atitiktis</span><span class="sxs-lookup"><span data-stu-id="863b4-103">Cookie compliance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="863b4-104">Šioje temoje apžvelgiama slapukų atitiktis ir numatytosios strategijos, įtrauktos į „Microsoft Dynamics 365 Commerce“.</span><span class="sxs-lookup"><span data-stu-id="863b4-104">This topic describes considerations for cookie compliance and the default policies that are included in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="863b4-105">Peržiūra</span><span class="sxs-lookup"><span data-stu-id="863b4-105">Overview</span></span>

<span data-ttu-id="863b4-106">Kai sekamos technologijos, veikiančios el. prekybos klientus, privatumas yra svarbus veiksnys.</span><span class="sxs-lookup"><span data-stu-id="863b4-106">Privacy is an important factor when tracking technologies that affect e-Commerce customers.</span></span> <span data-ttu-id="863b4-107">Dėl privatumo atitikties standartų, pvz., Europos Sąjungos (ES) bendrojo duomenų apsaugos reglamento (BDAR), administruojant bet kurią šiuo metu aktyvią svetainę reikia apsvarstyti elektroninio privatumo rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="863b4-107">Because of privacy compliance standards such as the General Data Protection Regulation (GDPR) in the European Union (EU), electronic privacy guidelines must be considered for any site that is active today.</span></span> <span data-ttu-id="863b4-108">Kadangi daugelis el. prekybos svetainių pagal numatytuosius parametrus yra pasiekiamos visame pasaulyje, svarbu peržiūrėti el. prekybos svetainės atitikties standartus.</span><span class="sxs-lookup"><span data-stu-id="863b4-108">Because many e-Commerce sites are globally accessible by default, it's important that you review the compliance standards for your e-Commerce site.</span></span>

<span data-ttu-id="863b4-109">Norėdami daugiau sužinoti apie pagrindinius „Microsoft“ naudojamus slapukų atitikties principus, apsilankykite [„Microsoft“ patikimumo centre](https://www.microsoft.com/trust-center).</span><span class="sxs-lookup"><span data-stu-id="863b4-109">To learn more about the basic principles that Microsoft uses for cookie compliance, visit the [Microsoft Trust Center](https://www.microsoft.com/trust-center).</span></span> <span data-ttu-id="863b4-110">Šioje svetainėje taip pat galite gauti daugiau informacijos apie atitikties sritis ir privatumą.</span><span class="sxs-lookup"><span data-stu-id="863b4-110">On that site, you can also get more information about areas of compliance and privacy.</span></span>

<span data-ttu-id="863b4-111">Toliau pateikiamoje lentelėje rodomas dabartinis slapukų nuorodų sąrašas, kuriuos patalpino „Dynamics 365 Commerce” svetainės.</span><span class="sxs-lookup"><span data-stu-id="863b4-111">The following table shows the current reference list of cookies placed by Dynamics 365 Commerce sites.</span></span>

| <span data-ttu-id="863b4-112">Slapuko pavadinimas</span><span class="sxs-lookup"><span data-stu-id="863b4-112">Cookie name</span></span>                               | <span data-ttu-id="863b4-113">Naudojimas</span><span class="sxs-lookup"><span data-stu-id="863b4-113">Usage</span></span>                                                        |
| ------------------------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="863b4-114">.AspNet.Slapukai</span><span class="sxs-lookup"><span data-stu-id="863b4-114">.AspNet.Cookies</span></span>                             | <span data-ttu-id="863b4-115">Parduotuvės „Microsoft Azure Active Directory” („Azure AD”) autentifikavimo slapukai vienkartiniam prisijungimui (SSO).</span><span class="sxs-lookup"><span data-stu-id="863b4-115">Store Microsoft Azure Active Directory (Azure AD) authentication cookies for single sign-on (SSO).</span></span> <span data-ttu-id="863b4-116">Parduotuvės užšifravo vartotojo pagrindinę informaciją (vardą, pavardę, el. paštą).</span><span class="sxs-lookup"><span data-stu-id="863b4-116">Stores encrypted user principal information (name, surname, email).</span></span> |
| <span data-ttu-id="863b4-117">&#95;msdyn365___krepšelis&#95;</span><span class="sxs-lookup"><span data-stu-id="863b4-117">&#95;msdyn365___cart&#95;</span></span>                           | <span data-ttu-id="863b4-118">Parduotuvės krepšelio ID naudojamas produktų, pridėtų į krepšelio egzempliorių, sąrašui gauti.</span><span class="sxs-lookup"><span data-stu-id="863b4-118">Store cart ID used to obtain list of products added to cart instance.</span></span> |
| <span data-ttu-id="863b4-119">&#95;msdyn365___ucc&#95;</span><span class="sxs-lookup"><span data-stu-id="863b4-119">&#95;msdyn365___ucc&#95;</span></span>                            | <span data-ttu-id="863b4-120">Slapuko atitikties sutikimo sekimas.</span><span class="sxs-lookup"><span data-stu-id="863b4-120">Cookie compliance consent tracking.</span></span>                          |
| <span data-ttu-id="863b4-121">ai_seansas</span><span class="sxs-lookup"><span data-stu-id="863b4-121">ai_session</span></span>                                  | <span data-ttu-id="863b4-122">Aptinka, keliuose vartotojo veiklos seansuose buvo tam tikrų programėlės puslapių ir funkcijų.</span><span class="sxs-lookup"><span data-stu-id="863b4-122">Detects how many sessions of user activity have included certain pages and features of the app.</span></span> |
| <span data-ttu-id="863b4-123">ai_vartotojas</span><span class="sxs-lookup"><span data-stu-id="863b4-123">ai_user</span></span>                                     | <span data-ttu-id="863b4-124">Aptinka, kaip daug žmonių naudojo programėlę ir jos funkcijas.</span><span class="sxs-lookup"><span data-stu-id="863b4-124">Detects how many people used the app and its features.</span></span> <span data-ttu-id="863b4-125">Vartotojai skaičiuojami naudojant anoniminius ID.</span><span class="sxs-lookup"><span data-stu-id="863b4-125">Users are counted using anonymous IDs.</span></span> |
| <span data-ttu-id="863b4-126">b2cru</span><span class="sxs-lookup"><span data-stu-id="863b4-126">b2cru</span></span>                                       | <span data-ttu-id="863b4-127">Saugomas dinamiškai peradresavimo URL.</span><span class="sxs-lookup"><span data-stu-id="863b4-127">Stores redirect URL dynamically.</span></span>                              |
| <span data-ttu-id="863b4-128">JSESSIONID</span><span class="sxs-lookup"><span data-stu-id="863b4-128">JSESSIONID</span></span>                                  | <span data-ttu-id="863b4-129">Mokėjimo jungtis naudoja „Adyen”, kad išsaugotų vartotojo seansą.</span><span class="sxs-lookup"><span data-stu-id="863b4-129">Used by payment connector Adyen to store user session.</span></span>       |
| <span data-ttu-id="863b4-130">AtvertiIdPrijungti.nonce.&#42;</span><span class="sxs-lookup"><span data-stu-id="863b4-130">OpenIdConnect.nonce.&#42;</span></span>                       | <span data-ttu-id="863b4-131">Autentifikavimas</span><span class="sxs-lookup"><span data-stu-id="863b4-131">Authentication</span></span>                                               |
| <span data-ttu-id="863b4-132">x-ms-cpim-cache:.&#42;</span><span class="sxs-lookup"><span data-stu-id="863b4-132">x-ms-cpim-cache:.&#42;</span></span>                          | <span data-ttu-id="863b4-133">Naudojama užklausos būsenai tvarkyti.</span><span class="sxs-lookup"><span data-stu-id="863b4-133">Used for maintaining the request state.</span></span>                      |
| <span data-ttu-id="863b4-134">x-ms-cpim-csrf</span><span class="sxs-lookup"><span data-stu-id="863b4-134">x-ms-cpim-csrf</span></span>                              | <span data-ttu-id="863b4-135">Kelių svetainių užklausų klastočių (CRSF) atpažinimo ženklas, naudojamas apsaugoti nuo CRSF.</span><span class="sxs-lookup"><span data-stu-id="863b4-135">Cross-site request forgery (CRSF) token used for protection from CRSF.</span></span>     |
| <span data-ttu-id="863b4-136">x-ms-cpim-dc</span><span class="sxs-lookup"><span data-stu-id="863b4-136">x-ms-cpim-dc</span></span>                                | <span data-ttu-id="863b4-137">Naudojama norint nukreipti užklausas į atitinkamą gamybos autentifikavimo serverio egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="863b4-137">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="863b4-138">x-ms-cpim-rc.&#42;</span><span class="sxs-lookup"><span data-stu-id="863b4-138">x-ms-cpim-rc.&#42;</span></span>                              | <span data-ttu-id="863b4-139">Naudojama norint nukreipti užklausas į atitinkamą gamybos autentifikavimo serverio egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="863b4-139">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="863b4-140">x-ms-cpim-slice</span><span class="sxs-lookup"><span data-stu-id="863b4-140">x-ms-cpim-slice</span></span>                             | <span data-ttu-id="863b4-141">Naudojama norint nukreipti užklausas į atitinkamą gamybos autentifikavimo serverio egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="863b4-141">Used to route requests to the appropriate production authentication server instance.</span></span> |
| <span data-ttu-id="863b4-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span><span class="sxs-lookup"><span data-stu-id="863b4-142">x-ms-cpim-sso:rushmoreb2c.onmicrosoft.com_0</span></span> | <span data-ttu-id="863b4-143">Naudojama SSO seansui tvarkyti.</span><span class="sxs-lookup"><span data-stu-id="863b4-143">Used for maintaining the SSO session.</span></span>                        |
| <span data-ttu-id="863b4-144">x-ms-cpim-trans</span><span class="sxs-lookup"><span data-stu-id="863b4-144">x-ms-cpim-trans</span></span>                             | <span data-ttu-id="863b4-145">Naudojama operacijoms stebėti (atidarytų skirtukų skaičius, kuriais autentifikuojama lyginant su įmonė–vartotojui (B2C) svetaine), įskaitant dabartinę operaciją.</span><span class="sxs-lookup"><span data-stu-id="863b4-145">Used for tracking transactions (the number of open tabs authenticating against a business-to-consumer (B2C) site), including the current transaction.</span></span> |

## <a name="site-user-cookie-consent-on-an-e-commerce-site"></a><span data-ttu-id="863b4-146">Svetainės vartotojo sutikimas dėl slapukų „e-Commerce” svetainėje</span><span class="sxs-lookup"><span data-stu-id="863b4-146">Site user cookie consent on an e-Commerce site</span></span> 

<span data-ttu-id="863b4-147">Jei „e-Commerce” svetainės funkcija ar modulis naudoja nepagrindinius slapukus, prieš naudojant juos reikia gauti svetainės vartotojo sutikimą.</span><span class="sxs-lookup"><span data-stu-id="863b4-147">If an e-Commerce site feature or module uses a non-essential cookie, a site user's consent must be obtained before the cookie is tracked.</span></span> <span data-ttu-id="863b4-148">Norint leisti svetainės vartotojams pateikti sutikimą dėl slapukų „e-Commerce” svetainėje, svetainės autorius turi įtraukti ir konfigūruoti sutikimo dėl slapukų modulį puslapio antraštės modulyje, kad būtų užtikrinta, jog sutikimo reikalaujama ir jis gaunamas.</span><span class="sxs-lookup"><span data-stu-id="863b4-148">To allow site users to provide cookie consent on the e-Commerce site, a site author must add and configure a cookie consent module in the page's header module to ensure that the consent is prompted for and received.</span></span> <span data-ttu-id="863b4-149">Svetainės vartotojo sutikimas turi būti suteiktas prieš funkcijos arba modulio, naudojančio nepagrindinius slapukus, atvaizdavimą svetainės puslapyje.</span><span class="sxs-lookup"><span data-stu-id="863b4-149">Site user consent must be given before a feature or module using a non-essential cookie can be rendered on a site page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="863b4-150">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="863b4-150">Additional resources</span></span>

[<span data-ttu-id="863b4-151">Pritaikymo neįgaliesiems funkcijos ir galimybės</span><span class="sxs-lookup"><span data-stu-id="863b4-151">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="863b4-152">Atitikties peržiūra</span><span class="sxs-lookup"><span data-stu-id="863b4-152">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="863b4-153">Privatumo strategijos puslapio įtraukimas</span><span class="sxs-lookup"><span data-stu-id="863b4-153">Add a privacy policy page</span></span>](add-privacy-page.md)

[<span data-ttu-id="863b4-154">Su sekamais turinio pakeitimais susietų vartotojo ID keitimas</span><span class="sxs-lookup"><span data-stu-id="863b4-154">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)

[<span data-ttu-id="863b4-155">Sutikimo dėl slapukų modulis</span><span class="sxs-lookup"><span data-stu-id="863b4-155">Cookie consent module</span></span>](cookie-consent-module.md) 
 
[<span data-ttu-id="863b4-156">Antraštės modulis</span><span class="sxs-lookup"><span data-stu-id="863b4-156">Header module</span></span>](author-header-module.md)
