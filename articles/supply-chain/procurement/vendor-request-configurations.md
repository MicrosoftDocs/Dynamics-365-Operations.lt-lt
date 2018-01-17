---
title: "Tiekėjo užklausos konfigūracijos"
description: "Šioje temoje aprašomi laukai, kuriuos reikia užpildyti naujoje tiekėjo užklausoje."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 57297a5798004f959a53513b88750866083beee7
ms.contentlocale: lt-lt
ms.lasthandoff: 01/17/2018

---

# <a name="vendor-request-configurations"></a><span data-ttu-id="cd3ea-103">Tiekėjo užklausos konfigūracijos</span><span class="sxs-lookup"><span data-stu-id="cd3ea-103">Vendor request configurations</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="cd3ea-104">Norėdamas baigti tiekėjo užklausą, tiekėjo kontaktinis asmuo turi baigti galimo tiekėjo registracijos vedlį.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="cd3ea-105">Formoje **Tiekėjo užklausos konfigūracijos** galite kurti šablonus, kurie nurodo privalomus laukus ir matomus laukus galimo tiekėjo registracijos vedlyje.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="cd3ea-106">Pirmiausia tiekėjo registracijos vedlys su galimu tiekėju susijusio vartotojo paklausia, kurioje šalyje / regione tiekėjas vykdo veiklą.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="cd3ea-107">Ši informacija padeda nustatyti taikomą konfigūraciją.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="cd3ea-108">Jei nenurodyta konkreti šalies / regiono konfigūracija, naudojama numatytoji konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="cd3ea-109">Tiekėjo užklausos konfigūracijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="cd3ea-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="cd3ea-110">Pagal numatytuosius parametrus tiekėjo konfigūracija teikiama formoje Tiekėjo užklausos konfigūracijos.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="cd3ea-111">Negalima pasirinkti numatytosios konfigūracijos šalies / regiono, todėl srities **Šalys / regionai** keisti negalima.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1.  <span data-ttu-id="cd3ea-112">Spustelėkite **Paraiškos** > **Sąranka** > **Tiekėjai**, tada spustelėkite **Tiekėjo užklausos konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="cd3ea-113">Spustelėkite skirtuką **Laukai**, norėdami nustatyti išvardytų laukų būseną.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
-   <span data-ttu-id="cd3ea-114">Paslėptas (nematomas)</span><span class="sxs-lookup"><span data-stu-id="cd3ea-114">Hidden (Not visible)</span></span>
-   <span data-ttu-id="cd3ea-115">Rodomas (matomas, bet neprivalomas)</span><span class="sxs-lookup"><span data-stu-id="cd3ea-115">Displayed (Visible but not mandatory)</span></span>
-   <span data-ttu-id="cd3ea-116">Būtinas (matomas ir privalomas)</span><span class="sxs-lookup"><span data-stu-id="cd3ea-116">Required (Visible and mandatory)</span></span>
3.  <span data-ttu-id="cd3ea-117">Spustelėkite skirtuką **Turinys**, norėdami nurodyti, ar tekstas bus rodomas vedlyje ir ar reikia nurodyti, kad su galimu tiekėju susijęs vartotojas turi su tuo sutikti prieš pereidamas prie kito vedlio veiksmo.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="cd3ea-118">Bus prašoma bet kurių sąlygų, su kuriomis vartotojas turi sutikti, patvirtinimo.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="cd3ea-119">Taip pat galite įvesti patvirtinimo pranešimą, kuris bus rodomas, kai vedlys bus baigtas, ir galite įtraukti vieną arba kelis klausimynus.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="cd3ea-120">Konkrečios šalies / regiono tiekėjo konfigūracijos kūrimas</span><span class="sxs-lookup"><span data-stu-id="cd3ea-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="cd3ea-121">Spustelėkite **Paraiškos** > **Sąranka** > **Tiekėjai**, tada spustelėkite **Tiekėjo užklausos konfigūracijos**.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="cd3ea-122">Spustelėkite parinktį **Nauja**, norėdami kurti naują konfigūraciją, ir nurodykite konfigūracijos pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="cd3ea-123">Spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-123">Click **Save**.</span></span>
4.  <span data-ttu-id="cd3ea-124">Atidarykite skirtuką **Šalis / regionas**, kad pasirinktumėte šalį / regioną, kuriam konfigūracija skirta.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="cd3ea-125">Nustatykite konfigūraciją, vadovaudamiesi numatytosios konfigūracijos nustatymo instrukcijomis.</span><span class="sxs-lookup"><span data-stu-id="cd3ea-125">Complete the configuration by following the guidelines for the default configuration.</span></span>


