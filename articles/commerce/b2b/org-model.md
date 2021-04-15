---
title: Kurkite organizacijos modeliavimo hierarchijas B2B organizacijoms
description: Šioje temoja aprašoma, kaip kurti organizacijos modelio hierarchijas verslo su verslu (B2B) organizacijoms.
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 487af939f92ece8bc3e543b3beeffa239baa1863
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799834"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a><span data-ttu-id="493c9-103">Kurkite organizacijos modeliavimo hierarchijas B2B organizacijoms</span><span class="sxs-lookup"><span data-stu-id="493c9-103">Create org modeling hierarchies for B2B organizations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="493c9-104">Šioje temoja aprašoma, kaip kurti organizacijos modelio hierarchijas verslo su verslu (B2B) organizacijoms programoje „Microsoft Dynamics 365 Commerce”.</span><span class="sxs-lookup"><span data-stu-id="493c9-104">This topic describes how to create organizational modeling hierarchies for business-to-business (B2B) organizations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="493c9-105">„Commerce“ štabe, verslo partnerio organizacijos yra atstovaujamos kliento ir kliento hierarchijos objektų.</span><span class="sxs-lookup"><span data-stu-id="493c9-105">In Commerce headquarters, business partner organizations are represented by customer and customer hierarchy entities.</span></span> <span data-ttu-id="493c9-106">Verslo partnerio organizacija ir jos vartotojai yra atstovaujami kaip klientai ir kliento hierarchijos yra naudojamas siekiant susieti klientus tarpusavyje.</span><span class="sxs-lookup"><span data-stu-id="493c9-106">The business partner organization and its users are represented as customers, and customer hierarchies are used to associate those customers with each other.</span></span>

<span data-ttu-id="493c9-107">Kai verslo partneris užklausa prisijungti B2B el. komercijos saitas yra patvirtintas, atliekami tolesni veiksmai:</span><span class="sxs-lookup"><span data-stu-id="493c9-107">When a business partner request to join a B2B e-commerce site is approved, the following actions are performed:</span></span>

- <span data-ttu-id="493c9-108">Du nauji kliento įrašai yra sukuriami sistemoje: **Organizacijos tipo** kliento įrašas verslo partnerio organizacijai ir **Asmens tipas** kliento įrašo besikreipiančiam asmeniui (tai reiškia, verslo partnerio vartotojas, kuris pateikė užklausą).</span><span class="sxs-lookup"><span data-stu-id="493c9-108">Two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor (that is, the business partner user who submitted the request).</span></span>
- <span data-ttu-id="493c9-109">Naujas kliento hierarchijos įrašas yra sukuriamas **Klientas \> Kliento hierarchija**.</span><span class="sxs-lookup"><span data-stu-id="493c9-109">A new customer hierarchy record is created under **Customer \> Customer hierarchy**.</span></span> <span data-ttu-id="493c9-110">Šis įrašas turi tolesnes antraštės ypatybes:</span><span class="sxs-lookup"><span data-stu-id="493c9-110">This record has the following header properties:</span></span>

    - <span data-ttu-id="493c9-111">**Kliento hierarchijos ID** – Unikalus ID kliento hierarchijai.</span><span class="sxs-lookup"><span data-stu-id="493c9-111">**Customer hierarchy ID** – A unique ID for the customer hierarchy.</span></span> <span data-ttu-id="493c9-112">Šis ID naudoja skaičių seką, kuris yra nustatyta „Commerce“ bendrintuose parametruose „Commerce“ būstinėje.</span><span class="sxs-lookup"><span data-stu-id="493c9-112">This ID uses the number sequence that is defined in Commerce shared parameters in Commerce headquarters.</span></span>
    - <span data-ttu-id="493c9-113">**Pavadinimas** – Verslo partnerio organizacijos pavadinimas, kaip nurodytas samdymo užklausoje.</span><span class="sxs-lookup"><span data-stu-id="493c9-113">**Name** – The organization name of the business partner, as specified in the onboarding request.</span></span>
    - <span data-ttu-id="493c9-114">**Tikslas** – Ši nuosavybė yra nustatytas iš anksto nustatytai vertei **B2B organizacija**.</span><span class="sxs-lookup"><span data-stu-id="493c9-114">**Purpose** – This property is set to the predefined value **B2B organization**.</span></span>
    - <span data-ttu-id="493c9-115">**Organizacija** – Verslo partnerio kliento ID.</span><span class="sxs-lookup"><span data-stu-id="493c9-115">**Organization** – The customer ID of the business partner.</span></span>

<span data-ttu-id="493c9-116">Toliau pateikiama kliento hierarchijos įrašo išsami informacija:</span><span class="sxs-lookup"><span data-stu-id="493c9-116">Here are the details of the customer hierarchy record:</span></span>

- <span data-ttu-id="493c9-117">Kliento užklausos teikėjo įrašas yra susietas su kliento hierarchija.</span><span class="sxs-lookup"><span data-stu-id="493c9-117">The customer record of the requestor is associated with the customer hierarchy.</span></span>
- <span data-ttu-id="493c9-118">Administratoriaus vaidmuo yra susietas su užklausos teikėju.</span><span class="sxs-lookup"><span data-stu-id="493c9-118">The administrator role is associated with the requestor.</span></span>

<span data-ttu-id="493c9-119">Kai administratorius įtraukia daugiau naudotojų į verslo partnerio organizaciją B2B vietoje, naujas kiekvieno naudotojo kliento įrašas yra sukuriamas „Commerce“ būstinėje.</span><span class="sxs-lookup"><span data-stu-id="493c9-119">When the administrator adds more users are to the business partner organization on a B2B site, a new customer record for each user is created in Commerce headquarters.</span></span> <span data-ttu-id="493c9-120">Kliento įrašas taip pat įtraukiamas į atitinkamą kliento hierarchijos įrašą verslo partneriui, o jo vaidmuo yra „vartotojas“.</span><span class="sxs-lookup"><span data-stu-id="493c9-120">This customer record is also added to the relevant customer hierarchy record for the business partner and has the role of a "user."</span></span>

> [!NOTE]
> <span data-ttu-id="493c9-121">Didžiojoje dalyje atvejų, atitinkamos nuosavybės visų kliento įrašų vertės hierarchijoje turėtų sutapti.</span><span class="sxs-lookup"><span data-stu-id="493c9-121">In most cases, the corresponding property values of all customer records in a hierarchy should match.</span></span> <span data-ttu-id="493c9-122">Pavyzdžiui, kadangi visi verslo partnerio vartotojai turėtų gauti panašias kainas už produktus, jų kainos grupė ir susieti konfigūravimai turėtų sutapti.</span><span class="sxs-lookup"><span data-stu-id="493c9-122">For example, because all business partner users should get similar prices for products, their price group and associated configurations should match.</span></span> <span data-ttu-id="493c9-123">Nepaisant to, sistema neįgalina tokio nuoseklumo.</span><span class="sxs-lookup"><span data-stu-id="493c9-123">However, the system doesn't enforce this consistency.</span></span> <span data-ttu-id="493c9-124">Dėl to, atitinkami „Commerce“ štabo vartotojai yra atsakingi už nuosavybės verčių ir konfigūravimo atitikimą visiems klientams toje hierarchijoje.</span><span class="sxs-lookup"><span data-stu-id="493c9-124">Therefore, the relevant Commerce headquarters users are responsible for ensuring that the property values and configurations match for all customers in a given hierarchy.</span></span>

<span data-ttu-id="493c9-125">„Commerce“ štabo vartotojai gali ieškoti nuosavybės verčių visuose kliento įrašuose hierarchijoje šalia esančiame rodinyje.</span><span class="sxs-lookup"><span data-stu-id="493c9-125">Commerce headquarters users can look at the property values for all customer records in the hierarchy in a side-by-side view.</span></span> <span data-ttu-id="493c9-126">Rinkitės atitinkamą kliento įrašo nuosavybę pasirinkdami skirtuko pavadinimus iškrentančiame meniu.</span><span class="sxs-lookup"><span data-stu-id="493c9-126">Select the relevant customer record properties by selecting the tab names on the drop-down menu.</span></span> <span data-ttu-id="493c9-127">Vartotojai gali tiesiogiai peržiūrėti ir redaguoti nuosavybės vertes šiame rodinyje.</span><span class="sxs-lookup"><span data-stu-id="493c9-127">Users can directly view and edit the property values from this view.</span></span> <span data-ttu-id="493c9-128">Kitu atveju, jei norite taikyti vertes iš administratoriaus kliento įrašo visiems klientų įrašams, rinkitės **Viršyti** kliento išsamios informacijos hierarchijoje.</span><span class="sxs-lookup"><span data-stu-id="493c9-128">Alternatively, if you want to apply all the values from the administrator customer record to all the user customer records, select **Override** in the customer hierarchy details.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="493c9-129">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="493c9-129">Additional resources</span></span>

[<span data-ttu-id="493c9-130">Nustatykite B2B el. komercijos saitą</span><span class="sxs-lookup"><span data-stu-id="493c9-130">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="493c9-131">Valdykite verslo partnerio vartotojus B2B el. komercijos saituose</span><span class="sxs-lookup"><span data-stu-id="493c9-131">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="493c9-132">Konfigūruoti kliento sąskaitos mokėjimo metodą B2B el. komercijos saitams</span><span class="sxs-lookup"><span data-stu-id="493c9-132">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="493c9-133">Nustatykite produkto kiekio apribojimus B2B el. komercijos saitams</span><span class="sxs-lookup"><span data-stu-id="493c9-133">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]