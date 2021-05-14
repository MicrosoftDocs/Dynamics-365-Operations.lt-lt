---
title: Įgalinti kliento įregistravimo pranešimus kasos punkte (EKA)
description: Šioje temoje aprašoma, kaip įgalinti kliento įregistravimo pranešimus į „Microsoft Dynamics 365 Commerce“ kasos kodą (EKA).
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e4defc15d9ef198a361934d51e31016747dbb5ab
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937603"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a><span data-ttu-id="d531d-103">Įgalinti kliento įregistravimo pranešimus kasos punkte (EKA)</span><span class="sxs-lookup"><span data-stu-id="d531d-103">Enable customer check-in notifications in point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="d531d-104">Šioje temoje aprašoma, kaip įgalinti kliento įregistravimo pranešimus į „Microsoft Dynamics 365 Commerce“ kasos kodą (EKA).</span><span class="sxs-lookup"><span data-stu-id="d531d-104">This topic describes how to enable customer check-in notifications in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="d531d-105">Savo el. laiškų „užsakymas paruoštas paimti" organizacijos gali pateikti saitą ar mygtuką, kuris leidžia klientams informuoti parduotuvę, kad jie yra patalpose ir laukia, kol jų pakuotė bus jiems parengta.</span><span class="sxs-lookup"><span data-stu-id="d531d-105">In their "order ready for pickup" emails, organizations can provide a link or button that lets customers notify the store that they are on the premises and waiting for their package to be brought out to them.</span></span> <span data-ttu-id="d531d-106">Tada klientai gauna įregistravimo patvirtinimą, o parduotuvė savo EKA programoje gauna pranešimą kaip užduotį.</span><span class="sxs-lookup"><span data-stu-id="d531d-106">Customers then receive a check-in confirmation, and the store receives a notification as a task in its POS application.</span></span> <span data-ttu-id="d531d-107">Ši užduotis naudojama kaip raginimas susieti pardavimą ir pristatyti užsakymą kliento transporto priemonei.</span><span class="sxs-lookup"><span data-stu-id="d531d-107">This task serves as a prompt for a sales associate to deliver the order to the customer's vehicle.</span></span> <span data-ttu-id="d531d-108">Todėl klientas neturi įvesti parduotuvės.</span><span class="sxs-lookup"><span data-stu-id="d531d-108">Therefore, the customer doesn't have to enter the store.</span></span>

<span data-ttu-id="d531d-109">Kliento įregistravimo darbo eigą taip pat galima konfigūruoti, kad iš klientų būtų renkama papildoma informacija, pvz., automobilio stovėjimo vietos numeris, transporto priemonės gamintojas, modelis ir spalva bei pristatymo instrukcijos.</span><span class="sxs-lookup"><span data-stu-id="d531d-109">The customer check-in workflow can also be configured to collect additional information from customers, such as their parking spot number, the make, model, and color of their vehicle, and delivery instructions.</span></span> <span data-ttu-id="d531d-110">Parduotuvės lankomumo centras gali naudoti šią informaciją, kad galėtų lengviau įvykdyti užsakymą.</span><span class="sxs-lookup"><span data-stu-id="d531d-110">The retail store attendant can use this information to facilitate order fulfillment.</span></span>

## <a name="enable-customer-check-in"></a><span data-ttu-id="d531d-111">Įjungti kliento įregistravimą</span><span class="sxs-lookup"><span data-stu-id="d531d-111">Enable customer check-in</span></span>

<span data-ttu-id="d531d-112">Kai kliento įregistravimo funkcija įjungta, „Commerce" sugeneruoja užsakymo patvirtinimo ID (dar vadinamą kanalo nuorodos ID).</span><span class="sxs-lookup"><span data-stu-id="d531d-112">When the customer check-in feature is turned on, Commerce generates an order confirmation ID (also known as the channel reference ID).</span></span> <span data-ttu-id="d531d-113">Ji taip pat generuoja užsakymų, kurie kuriami naudojant kasos kodą (EKA) arba skambučių centro kanalus, užsakymų patvirtinimo ID.</span><span class="sxs-lookup"><span data-stu-id="d531d-113">It also generates order confirmation IDs for orders that are created through point of sale (POS) or call center channels.</span></span> 

<span data-ttu-id="d531d-114">Norėdami įjungti kliento registravimo funkciją „Commerce“ štabe, atlikite šiuos žingsnius.</span><span class="sxs-lookup"><span data-stu-id="d531d-114">To turn on the customer check-in feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="d531d-115">Eikite į **Darbo sritys \> Funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="d531d-115">Go to **Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="d531d-116">Ieškoti nuosekliojo **kanalo nuorodos ID formato kanalų** funkcijai generuoti.</span><span class="sxs-lookup"><span data-stu-id="d531d-116">Search for the **Generate a consistent channel reference ID format across channels** feature.</span></span> 
3. <span data-ttu-id="d531d-117">Pasirinkite norimą įjungti funkciją, tada dešinioje ypatybių juostoje pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="d531d-117">Select the feature, and then select **Enable now** in the properties pane.</span></span> 

## <a name="create-a-check-in-confirmation-page"></a><span data-ttu-id="d531d-118">Kurti įregistravimo patvirtinimo puslapį</span><span class="sxs-lookup"><span data-stu-id="d531d-118">Create a check-in confirmation page</span></span>

<span data-ttu-id="d531d-119">Savo el. komercijos svetainėje turite sukurti naują puslapį, kuris bus naudojamas kaip įregistravimo patvirtinimo patirtis.</span><span class="sxs-lookup"><span data-stu-id="d531d-119">On your e-commerce site, you must create a new page that will serve as the check-in confirmation experience.</span></span> <span data-ttu-id="d531d-120">Papildomas konfigūracijas puslapyje taip pat galima įtraukti formą, kuri renka papildomą klientų informaciją ir palengvina užsakymų vykdymą.</span><span class="sxs-lookup"><span data-stu-id="d531d-120">Through additional configuration, the page can also include a form that collects additional information from customers to facilitate order fulfillment.</span></span> <span data-ttu-id="d531d-121">Informacijos, kaip nustatyti puslapį ir modulį, ieškokite [Kliento įregistravimo modulyje](check-in-pickup-module.md).</span><span class="sxs-lookup"><span data-stu-id="d531d-121">For information about how to set up the page and module, see [Customer check-in module](check-in-pickup-module.md).</span></span>

## <a name="configure-the-transactional-email-template"></a><span data-ttu-id="d531d-122">Operacijų el. laiško šablono konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="d531d-122">Configure the transactional email template</span></span>

<span data-ttu-id="d531d-123">Turite įtraukti aš čia esantį saitą arba mygtuką į operacijų el. laiško, kurį gauna klientai, kai jų užsakymas yra **parengtas** paimti, šabloną.</span><span class="sxs-lookup"><span data-stu-id="d531d-123">You must add an **I am here** link or button to the template for the transactional email that customers receive when their order is ready for pickup.</span></span> <span data-ttu-id="d531d-124">Klientai naudoja šį saitą arba mygtuką, norėdami pranešti parduotuvei, kad ji buvo pristatyta, paimti užsakymą.</span><span class="sxs-lookup"><span data-stu-id="d531d-124">Customers will use this link or button to notify the store that they have arrived to pick up their order.</span></span> 

<span data-ttu-id="d531d-125">Pridėti saitą arba mygtuką prie šablono, susieto su pranešimo apie pakavimą pranešimo tipu ir pristatymo režimu, kurį naudojate **pasipriešinimo** užsakymui vykdyti.</span><span class="sxs-lookup"><span data-stu-id="d531d-125">Add the link or button to the template that is mapped to the **Packing completed** notification type and the mode of delivery that you're using for curbside order fulfillment.</span></span> <span data-ttu-id="d531d-126">Šablone sukurkite HTML saitą arba mygtuką, kuris nurodo jūsų sukurto patvirtinimo puslapio URL.</span><span class="sxs-lookup"><span data-stu-id="d531d-126">In the template, create an HTML link or button that points to the URL of the check-in confirmation page that you created.</span></span> <span data-ttu-id="d531d-127">Toliau pateikiamas pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="d531d-127">Here is an example.</span></span>

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
<span data-ttu-id="d531d-128">Daugiau informacijos apie el. laiškų šablonų konfigūravimą rasite [tinkinti el. laiškus pagal pristatymo](customize-email-delivery-mode.md) būdą.</span><span class="sxs-lookup"><span data-stu-id="d531d-128">For more information about how to configure email templates, see [Customize transactional emails by mode of delivery](customize-email-delivery-mode.md).</span></span> 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a><span data-ttu-id="d531d-129">EKA sukurta įregistravimo patvirtinimo užduotis</span><span class="sxs-lookup"><span data-stu-id="d531d-129">A check-in confirmation task is created in POS</span></span>

<span data-ttu-id="d531d-130">Klientui pranešus apie parduotuvę, kurioje jis yra paėmimo atveju, jis gavo įregistravimo patvirtinimo pranešimą ir užduotis sukuriama parduotuvės, kurioje klientas priima užsakymą, užduočių sąraše.</span><span class="sxs-lookup"><span data-stu-id="d531d-130">After a customer notifies the store that they are present for pickup, they receive a check-in confirmation notification, and a task is created in the tasks list in POS for the store where the customer is picking up the order.</span></span> <span data-ttu-id="d531d-131">Užduotyje yra visa kliento ir užsakymo informacija, kurios reikia norint įvykdyti užsakymą.</span><span class="sxs-lookup"><span data-stu-id="d531d-131">The task contains all the customer and order information that is required to fulfill the order.</span></span> <span data-ttu-id="d531d-132">Užduoties metu instrukcijų lauke rodoma bet kokia informacija, kliento surinkta naudojant papildomos informacijos formą.</span><span class="sxs-lookup"><span data-stu-id="d531d-132">In the task, the instructions field shows any information that was collected from the customer through the additional information form.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="d531d-133">Papildomi ištekliai</span><span class="sxs-lookup"><span data-stu-id="d531d-133">Additional resources</span></span>

[<span data-ttu-id="d531d-134">Registravimasis paėmimo moduliui</span><span class="sxs-lookup"><span data-stu-id="d531d-134">Check-in for pickup module</span></span>](check-in-pickup-module.md)
